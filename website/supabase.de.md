---
title: Supabase
description: Wo Join-Daten liegen und die Checkliste nach dem Verbinden von Supabase auf Vercel.
order: 4
review_status: draft-for-mingli29
---

# Supabase

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Supabase ist der **Speicher** für Proj.Help: Postgres-Zeilen (Ideen, Antworten) plus Auth (GitHub oder Microsoft). Datei-Buckets sind für den aktuellen Hub nicht nötig.

Die Marketplace-Integration auf Vercel kopiert nur Schlüssel in Umgebungsvariablen. SQL und OAuth konfigurierst du weiterhin in **Supabase Studio**.

## Nach dem Verbinden auf Vercel

1. Umgebungsvariablen bestätigen — [Vercel-Deploys](/docs/website/vercel)
2. **Redeploy**, damit `NEXT_PUBLIC_`-Schlüssel im Build sind
3. Vercel-Projekt → Storage → Supabase → **Open in Supabase**
4. **SQL Editor** (nicht Vercel Query). Jede Datei vollständig und der Reihe nach ausführen:
   - `supabase/migrations/20260904112922_init_proj_help.sql`
   - `supabase/migrations/20260904140000_allow_github_auth.sql`  
   Diese Pfade liegen in **Tiger-Studio-Website**, nicht in diesem Docs-Repo.
5. **Authentication → URL configuration**
   - Site URL: `https://tiger-studio-website.vercel.app`
   - Redirect URLs (`**` behalten, damit Query-Strings und Previews passen):
     - `https://tiger-studio-website.vercel.app/auth/callback**`
     - `http://localhost:3000/auth/callback**`
6. **Authentication → Providers**
   - E-Mail deaktivieren
   - **GitHub** aktivieren (unten)
   - **Azure** nur behalten, wenn eine Entra-App existiert

## GitHub-OAuth für Join

Wenn die GitHub-Anmeldung „nicht durchläuft“, ist die Authorization callback URL meist falsch.

1. GitHub → Settings → Developer settings → [OAuth Apps](https://github.com/settings/developers) → **New OAuth App**
2. Homepage URL: `https://tiger-studio-website.vercel.app`
3. Die Authorization callback URL muss **Supabase** sein, nicht Vercel:

   ```text
   https://<project-ref>.supabase.co/auth/v1/callback
   ```

   `<project-ref>` ist die Subdomain in `NEXT_PUBLIC_SUPABASE_URL`. Hier **nicht** `https://tiger-studio-website.vercel.app/auth/callback` verwenden.
4. Ein Client-Secret erzeugen. Client-ID und Secret in Supabase → Authentication → Providers → GitHub einfügen
5. Redeployen, dann Join versuchen. Fehler erscheinen auf `/auth/error` mit der einzufügenden Callback-URL.

Microsoft/Azure braucht weiterhin eine Entra-App. Wenn das Azure-Portal blockiert ist, GitHub nutzen.

## Was du niemals in Git legst

- `service_role` / geheime Schlüssel
- OAuth-Client-Secrets
- `.env.local`

Der Publishable-/Anon-Key ist absichtlich öffentlich. Row Level Security in diesen SQL-Migrationen schützt die Zeilen.

## Verwandt

- [Dem Ideenboard beitreten](/docs/getting-started/join)
- [Vercel-Deploys](/docs/website/vercel)
