---
title: Supabase
description: Join 数据存在哪里，以及在 Vercel 上连接 Supabase 之后的检查清单。
order: 4
---

# Supabase

Supabase 是 Proj.Help 的 **存储**：Postgres 行（想法、回复）加上 Auth（GitHub 或 Microsoft）。当前枢纽不需要文件桶。

Vercel 上的 Marketplace 集成只把密钥复制进环境变量。SQL 和 OAuth 仍要在 **Supabase Studio** 里配置。

## 在 Vercel 上连接之后

1. 确认环境变量 — [Vercel 部署](/docs/website/vercel)
2. **Redeploy**，让 `NEXT_PUBLIC_` 密钥进入构建
3. Vercel 项目 → Storage → Supabase → **Open in Supabase**
4. **SQL Editor**（不是 Vercel Query）。按顺序完整运行每个文件：
   - `supabase/migrations/20260904112922_init_proj_help.sql`
   - `supabase/migrations/20260904140000_allow_github_auth.sql`  
   这些路径在 **Tiger-Studio-Website** 里，不在本 docs 仓库。
5. **Authentication → URL configuration**
   - Site URL：`https://tiger-studio-website.vercel.app`
   - Redirect URLs（保留 `**`，以便查询字符串和预览能匹配）：
     - `https://tiger-studio-website.vercel.app/auth/callback**`
     - `http://localhost:3000/auth/callback**`
6. **Authentication → Providers**
   - 关闭 Email
   - 启用 **GitHub**（见下方）
   - 只有已有 Entra 应用时才保留 **Azure**

## Join 的 GitHub OAuth

如果 GitHub 登录“完不成”，通常是 Authorization callback URL 写错了。

1. GitHub → Settings → Developer settings → [OAuth Apps](https://github.com/settings/developers) → **New OAuth App**
2. Homepage URL：`https://tiger-studio-website.vercel.app`
3. Authorization callback URL 必须是 **Supabase**，不是 Vercel：

   ```text
   https://<project-ref>.supabase.co/auth/v1/callback
   ```

   `<project-ref>` 是 `NEXT_PUBLIC_SUPABASE_URL` 里的子域名。这里 **不要** 用 `https://tiger-studio-website.vercel.app/auth/callback`。
4. 生成 client secret。把 Client ID 和 secret 贴进 Supabase → Authentication → Providers → GitHub
5. Redeploy，然后试 Join。失败会显示在 `/auth/error`，并给出要粘贴的 callback URL。

Microsoft/Azure 仍然需要 Entra 应用。如果 Azure 门户被拦，就用 GitHub。

## 永远不要放进 Git 的内容

- `service_role` / 密钥
- OAuth client secrets
- `.env.local`

可发布 / anon 密钥按设计就是公开的。那些 SQL 迁移里的 Row Level Security 才保护行数据。

## 相关

- [加入想法板](/docs/getting-started/join)
- [Vercel 部署](/docs/website/vercel)
