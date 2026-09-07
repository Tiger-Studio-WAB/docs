---
title: Docs on the hub
description: How folders in this repo become /docs pages after a refresh.
order: 5
---

# Docs on the hub

The handbook at `/docs` is **not** a separate Vercel project. The website loads Markdown from [`Tiger-Studio-WAB/docs`](https://github.com/Tiger-Studio-WAB/docs) (this repo). Missing files can fall back to a starter tree shipped with the hub.

## Add or change a page

1. Follow [How to format docs](/docs/how-to-format): folder, `index.md`, optional `_category.json`
2. Merge to `main` in **this** repo
3. Wait about two minutes, then open `/docs` and check the sidebar

You do not open a PR on `Tiger-Studio-Website` for copy-only handbook edits.

## When you *do* change the website repo

Change `Tiger-Studio-Website` only if the **docs app** is wrong (sidebar renderer, fetch, routing). That is TypeScript under `src/lib/docs.ts` and `src/app/docs/`. Ship it with a [Vercel](/docs/website/vercel) preview.

## Support is separate

Do not add a `support` folder here. Help and tickets are [/support](/support) and the [`support`](https://github.com/Tiger-Studio-WAB/support) repo.

## Related

- [How to format docs](/docs/how-to-format)
- [Manage the website](/docs/website)
