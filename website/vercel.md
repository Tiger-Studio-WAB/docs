---
title: Vercel deploys
description: How production and preview deploys work, and what to change in the Vercel dashboard.
order: 3
---

# Vercel deploys

GitHub is the source of truth. Vercel builds **Tiger-Studio-Website** on `main` (production) and on pull requests (preview URLs).

Config lives in `vercel.ts` in that repo: framework **Next.js**, build command `npm run build`.

## First-time project (maintainers)

1. Import the GitHub repo in the [Vercel dashboard](https://vercel.com/dashboard) **or** from the repo root:

   ```bash
   npx vercel
   ```

2. Root Directory stays the repo root (empty).
3. Framework Preset: **Next.js**. If an old project shows Other, set it under **Settings → General**.

## Everyday shipping

1. Open a PR against `main` in `Tiger-Studio-Website`
2. Wait for the Vercel preview
3. Merge
4. Production updates at [tiger-studio-website.vercel.app](https://tiger-studio-website.vercel.app)

Docs-only PRs in **this** `docs` repo do not rebuild Next.js. The hub refetches Markdown on a short cache (about two minutes). See [Docs on the hub](/docs/website/docs).

## Environment variables

**Settings → Environment Variables**. After the Supabase Marketplace integration, confirm at least:

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` (or `NEXT_PUBLIC_SUPABASE_ANON_KEY`)

Scope them to Production, Preview, and Development.

`NEXT_PUBLIC_` values are baked in at **build** time. After they appear or change, **Redeploy**.

`GITHUB_TOKEN` is only for public org stats. It is not Join auth.

## Logs and rollbacks

- Dashboard → project → **Deployments** → a deployment → **Logs**
- CLI (from a linked clone): `npx vercel logs` / inspect a URL with `npx vercel inspect <url>`
- Redeploy an older deployment from the same Deployments list if a release is bad

## Related

- [Supabase](/docs/website/supabase)
- [Run locally](/docs/website/local)
