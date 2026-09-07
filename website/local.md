---
title: Run locally
description: Clone the hub, install packages, and open localhost.
order: 2
---

# Run locally

You need [Git](/docs/git/install) and [Node.js](/docs/typescript/install).

## 1. Clone and install

```bash
gh repo clone Tiger-Studio-WAB/Tiger-Studio-Website
cd Tiger-Studio-Website
npm install
```

## 2. Environment file

```bash
cp .env.example .env.local
```

| Variable | Purpose |
| --- | --- |
| `GITHUB_ORG` | Defaults to `Tiger-Studio-WAB` |
| `GITHUB_TOKEN` | Optional. Raises GitHub API limits for the public hub (products, news). **Not** used for Join. |
| `NEXT_PUBLIC_SUPABASE_URL` | Ideas board. From the Vercel/Supabase integration. |
| `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` or `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Public Supabase key |
| `ALLOWED_EMAIL_DOMAIN` | Optional Microsoft-domain gate |

Without Supabase vars, the marketing pages still run. **Join / Proj.Help** needs them.

For a full Join stack on your machine, use the same providers as production (GitHub OAuth in Supabase). Local Microsoft/Azure is extra setup; GitHub sign-in is the path that does not need school admin.

## 3. Dev server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

Useful scripts from `package.json`: `npm run lint`, `npm run build`.

## Related

- [Vercel deploys](/docs/website/vercel)
- [Supabase](/docs/website/supabase)
