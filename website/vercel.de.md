---
title: Vercel-Deploys
description: Wie Produktions- und Preview-Deploys funktionieren und was du im Vercel-Dashboard ändern musst.
order: 3
review_status: draft-for-mingli29
---

# Vercel-Deploys

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

GitHub ist die Quelle der Wahrheit. Vercel baut **Tiger-Studio-Website** auf `main` (Produktion) und auf Pull Requests (Preview-URLs).

Die Konfiguration liegt in `vercel.ts` in diesem Repo: Framework **Next.js**, Build-Befehl `npm run build`.

## Erstes Projekt (Maintainer)

1. Das GitHub-Repo im [Vercel-Dashboard](https://vercel.com/dashboard) importieren **oder** vom Repo-Stamm:

   ```bash
   npx vercel
   ```

2. Root Directory bleibt der Repo-Stamm (leer).
3. Framework Preset: **Next.js**. Wenn ein altes Projekt Other zeigt, unter **Settings → General** setzen.

## Alltag beim Ausliefern

1. Einen PR gegen `main` in `Tiger-Studio-Website` öffnen
2. Auf die Vercel-Preview warten
3. Mergen
4. Produktion aktualisiert sich unter [tiger-studio-website.vercel.app](https://tiger-studio-website.vercel.app)

Nur-Docs-PRs in **diesem** `docs`-Repo bauen Next.js nicht neu. Der Hub holt Markdown nach einem kurzen Cache erneut (etwa zwei Minuten). Siehe [Docs auf dem Hub](/docs/website/docs).

## Umgebungsvariablen

**Settings → Environment Variables**. Nach der Supabase-Marketplace-Integration mindestens bestätigen:

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` (oder `NEXT_PUBLIC_SUPABASE_ANON_KEY`)

Auf Production, Preview und Development scopen.

`NEXT_PUBLIC_`-Werte werden zur **Build**-Zeit eingebacken. Nachdem sie erscheinen oder sich ändern: **Redeploy**.

`GITHUB_TOKEN` ist nur für öffentliche Org-Statistiken. Es ist keine Join-Auth.

## Logs und Rollbacks

- Dashboard → Projekt → **Deployments** → ein Deployment → **Logs**
- CLI (aus einem verknüpften Clone): `npx vercel logs` / eine URL prüfen mit `npx vercel inspect <url>`
- Ein älteres Deployment aus derselben Deployments-Liste erneut ausrollen, wenn ein Release schlecht ist

## Verwandt

- [Supabase](/docs/website/supabase)
- [Lokal ausführen](/docs/website/local)
