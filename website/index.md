---
title: Manage the website
description: How the Tiger Studio hub is hosted on Vercel and stored in Supabase.
order: 1
---

# Manage the website

The public hub is [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website). Live URL: [tiger-studio-website.vercel.app](https://tiger-studio-website.vercel.app).

## Who does what

| Layer | Product | Holds |
| --- | --- | --- |
| Host / CDN / builds | **Vercel** | Next.js app, previews, env vars, deploys from GitHub |
| Data / auth | **Supabase** | Proj.Help ideas, replies, sessions (Postgres + Auth) |
| Handbook copy | **This `docs` repo** | Markdown folders; the site fetches them |
| Support copy | [`support`](https://github.com/Tiger-Studio-WAB/support) | Help page / issue templates |

Vercel does **not** store the ideas board. The Vercel Marketplace Supabase integration only syncs environment variables. Schema and OAuth still live in Supabase Studio.

## Pages in this section

1. [Run locally](/docs/website/local)
2. [Vercel deploys](/docs/website/vercel)
3. [Supabase](/docs/website/supabase)
4. [Docs on the hub](/docs/website/docs)

Code changes: [TypeScript](/docs/typescript) and a [pull request](/docs/github-cli/pull-requests). Copy-only handbook edits: add Markdown here — [How to format docs](/docs/how-to-format).
