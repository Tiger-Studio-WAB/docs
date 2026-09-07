---
title: TypeScript on the website
description: Where types live in the hub and how to change them safely.
order: 3
---

# TypeScript on the website

Repo: [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website). App Router files live under `src/`.

## Folders you will touch

| Path | What it is |
| --- | --- |
| `src/app/` | Routes (`page.tsx`, `layout.tsx`, route handlers) |
| `src/components/` | UI |
| `src/lib/` | GitHub fetch, docs loader, Supabase helpers |
| `src/lib/supabase/` | Browser/server Supabase clients |
| `vercel.ts` | Vercel project config (typed) |
| `supabase/migrations/` | SQL for Join / Proj.Help, not TypeScript |

## Habits that keep the build green

1. Reuse types in `src/lib/types.ts` and nearby modules instead of `any`.
2. Server-only secrets stay **off** `NEXT_PUBLIC_` names. Public Supabase URL and publishable/anon key are the exception — see [Supabase](/docs/website/supabase).
3. After UI changes, run `npm run lint` and `npm run build` locally when you can.
4. Do not edit Next.js internals to add a docs page. Add Markdown in **this** repo instead.

## Config pointer

`tsconfig.json` is already set for the App Router. You should not need to change `strict` or paths for a normal feature.

## Related

- [Manage the website](/docs/website)
- [How to format docs](/docs/how-to-format)
