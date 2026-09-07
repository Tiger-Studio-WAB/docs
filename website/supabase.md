---
title: Supabase
description: Where Join data lives, and the checklist after connecting Supabase on Vercel.
order: 4
---

# Supabase

Supabase is the **store** for Proj.Help: Postgres rows (ideas, replies) plus Auth (GitHub or Microsoft). File buckets are not required for the current hub.

The Marketplace integration on Vercel only copies keys into environment variables. You still run SQL and configure OAuth in **Supabase Studio**.

## After connecting on Vercel

1. Confirm env vars — [Vercel deploys](/docs/website/vercel)
2. **Redeploy** so `NEXT_PUBLIC_` keys are in the build
3. Vercel project → Storage → Supabase → **Open in Supabase**
4. **SQL Editor** (not Vercel Query). Run each file in full, in order:
   - `supabase/migrations/20260904112922_init_proj_help.sql`
   - `supabase/migrations/20260904140000_allow_github_auth.sql`  
   Those paths are in **Tiger-Studio-Website**, not this docs repo.
5. **Authentication → URL configuration**
   - Site URL: `https://tiger-studio-website.vercel.app`
   - Redirect URLs (keep `**` so query strings and previews match):
     - `https://tiger-studio-website.vercel.app/auth/callback**`
     - `http://localhost:3000/auth/callback**`
6. **Authentication → Providers**
   - Disable Email
   - Enable **GitHub** (below)
   - Keep **Azure** only if an Entra app exists

## GitHub OAuth for Join

If GitHub sign-in “doesn’t finish”, the Authorization callback URL is usually wrong.

1. GitHub → Settings → Developer settings → [OAuth Apps](https://github.com/settings/developers) → **New OAuth App**
2. Homepage URL: `https://tiger-studio-website.vercel.app`
3. Authorization callback URL must be **Supabase**, not Vercel:

   ```text
   https://<project-ref>.supabase.co/auth/v1/callback
   ```

   `<project-ref>` is the subdomain in `NEXT_PUBLIC_SUPABASE_URL`. Do **not** use `https://tiger-studio-website.vercel.app/auth/callback` here.
4. Generate a client secret. Paste Client ID and secret into Supabase → Authentication → Providers → GitHub
5. Redeploy, then try Join. Failures surface on `/auth/error` with the callback URL to paste.

Microsoft/Azure still needs an Entra app. If Azure portal is blocked, use GitHub.

## What you never put in Git

- `service_role` / secret keys
- OAuth client secrets
- `.env.local`

The publishable/anon key is public by design. Row Level Security in those SQL migrations is what protects rows.

## Related

- [Join the ideas board](/docs/getting-started/join)
- [Vercel deploys](/docs/website/vercel)
