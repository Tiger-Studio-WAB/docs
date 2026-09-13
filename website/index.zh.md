---
title: 管理网站
description: Tiger Studio 枢纽如何托管在 Vercel 上，以及数据如何存在 Supabase。
order: 1
---

# 管理网站

公开枢纽是 [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website)。线上地址：[tiger-studio-website.vercel.app](https://tiger-studio-website.vercel.app)。

## 谁负责什么

| 层 | 产品 | 存放内容 |
| --- | --- | --- |
| 托管 / CDN / 构建 | **Vercel** | Next.js 应用、预览、环境变量、从 GitHub 部署 |
| 数据 / 鉴权 | **Supabase** | Proj.Help 想法、回复、会话（Postgres + Auth） |
| 手册文案 | **本 `docs` 仓库** | Markdown 文件夹；网站去拉取它们 |
| 支持文案 | [`support`](https://github.com/Tiger-Studio-WAB/support) | 帮助页 / 议题模板 |

Vercel **不**存储想法板。Vercel Marketplace 的 Supabase 集成只同步环境变量。架构与 OAuth 仍在 Supabase Studio。

## 本分区页面

1. [本地运行](/docs/website/local)
2. [Vercel 部署](/docs/website/vercel)
3. [Supabase](/docs/website/supabase)
4. [枢纽上的文档](/docs/website/docs)

改代码：[TypeScript](/docs/typescript) 加一个 [拉取请求](/docs/github-cli/pull-requests)。只改手册文案：在这里加 Markdown — [如何排版文档](/docs/how-to-format)。
