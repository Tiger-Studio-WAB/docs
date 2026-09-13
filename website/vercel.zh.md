---
title: Vercel 部署
description: 生产与预览部署如何工作，以及要在 Vercel 控制台改什么。
order: 3
---

# Vercel 部署

GitHub 是事实来源。Vercel 在 `main` 上构建 **Tiger-Studio-Website**（生产），并在拉取请求上构建（预览 URL）。

配置在该仓库的 `vercel.ts`：框架 **Next.js**，构建命令 `npm run build`。

## 首次建项目（维护者）

1. 在 [Vercel 控制台](https://vercel.com/dashboard) 导入 GitHub 仓库，**或**在仓库根目录：

   ```bash
   npx vercel
   ```

2. Root Directory 保持仓库根（空）。
3. Framework Preset：**Next.js**。如果旧项目显示 Other，到 **Settings → General** 改过来。

## 日常发布

1. 在 `Tiger-Studio-Website` 对 `main` 打开 PR
2. 等 Vercel 预览
3. 合并
4. 生产更新到 [tiger-studio-website.vercel.app](https://tiger-studio-website.vercel.app)

**本** `docs` 仓库里只改文档的 PR 不会重建 Next.js。枢纽会按短缓存（大约两分钟）重新拉取 Markdown。见 [枢纽上的文档](/docs/website/docs)。

## 环境变量

**Settings → Environment Variables**。Supabase Marketplace 集成之后，至少确认：

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY`（或 `NEXT_PUBLIC_SUPABASE_ANON_KEY`）

把它们的作用域设为 Production、Preview 和 Development。

`NEXT_PUBLIC_` 的值在 **构建** 时写入。它们出现或变更后，要 **Redeploy**。

`GITHUB_TOKEN` 只用于公开组织统计。它不是 Join 鉴权。

## 日志与回滚

- Dashboard → 项目 → **Deployments** → 某次部署 → **Logs**
- CLI（在已关联的克隆里）：`npx vercel logs` / 用 `npx vercel inspect <url>` 检查某个 URL
- 如果某次发布有问题，从同一 Deployments 列表重新部署更早的一次

## 相关

- [Supabase](/docs/website/supabase)
- [本地运行](/docs/website/local)
