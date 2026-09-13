---
title: 网站上的 TypeScript
description: 枢纽里类型放在哪里，以及如何安全地改它们。
order: 3
---

# 网站上的 TypeScript

仓库：[`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website)。App Router 文件在 `src/` 下。

## 你会碰到的文件夹

| 路径 | 是什么 |
| --- | --- |
| `src/app/` | 路由（`page.tsx`、`layout.tsx`、路由处理程序） |
| `src/components/` | UI |
| `src/lib/` | GitHub 拉取、文档加载器、Supabase 辅助函数 |
| `src/lib/supabase/` | 浏览器 / 服务器 Supabase 客户端 |
| `vercel.ts` | Vercel 项目配置（带类型） |
| `supabase/migrations/` | Join / Proj.Help 的 SQL，不是 TypeScript |

## 让构建保持绿色的习惯

1. 复用 `src/lib/types.ts` 和附近模块里的类型，而不是 `any`。
2. 仅服务端密钥不要用 `NEXT_PUBLIC_` 名称。公开的 Supabase URL 与可发布 / anon 密钥是例外 — 见 [Supabase](/docs/website/supabase)。
3. 改完 UI 后，能跑的话在本地执行 `npm run lint` 和 `npm run build`。
4. 不要为了加文档页去改 Next.js 内部。改为在 **这个** 仓库里加 Markdown。

## 配置提示

`tsconfig.json` 已经为 App Router 配好。普通功能不必改 `strict` 或 paths。

## 相关

- [管理网站](/docs/website)
- [如何排版文档](/docs/how-to-format)
