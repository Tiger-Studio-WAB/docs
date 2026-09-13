---
title: 本地运行
description: 克隆枢纽、安装软件包，并打开 localhost。
order: 2
---

# 本地运行

你需要 [Git](/docs/git/install) 和 [Node.js](/docs/typescript/install)。

## 1. 克隆并安装

```bash
gh repo clone Tiger-Studio-WAB/Tiger-Studio-Website
cd Tiger-Studio-Website
npm install
```

## 2. 环境文件

```bash
cp .env.example .env.local
```

| 变量 | 用途 |
| --- | --- |
| `GITHUB_ORG` | 默认是 `Tiger-Studio-WAB` |
| `GITHUB_TOKEN` | 可选。提高公开枢纽（产品、新闻）的 GitHub API 限额。**不**用于 Join。 |
| `NEXT_PUBLIC_SUPABASE_URL` | 想法板。来自 Vercel / Supabase 集成。 |
| `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` 或 `NEXT_PUBLIC_SUPABASE_ANON_KEY` | 公开的 Supabase 密钥 |
| `ALLOWED_EMAIL_DOMAIN` | 可选的 Microsoft 域名门禁 |

没有 Supabase 变量时，营销页仍能跑。**Join / Proj.Help** 需要它们。

要在本机跑完整的 Join 栈，使用与生产相同的提供方（Supabase 里的 GitHub OAuth）。本地 Microsoft/Azure 需要额外配置；GitHub 登录不需要学校管理员。

## 3. 开发服务器

```bash
npm run dev
```

打开 [http://localhost:3000](http://localhost:3000)。

`package.json` 里有用的脚本：`npm run lint`、`npm run build`。

## 相关

- [Vercel 部署](/docs/website/vercel)
- [Supabase](/docs/website/supabase)
