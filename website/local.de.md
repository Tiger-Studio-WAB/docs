---
title: Lokal ausführen
description: Den Hub klonen, Pakete installieren und localhost öffnen.
order: 2
review_status: draft-for-mingli29
---

# Lokal ausführen

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Du brauchst [Git](/docs/git/install) und [Node.js](/docs/typescript/install).

## 1. Klonen und installieren

```bash
gh repo clone Tiger-Studio-WAB/Tiger-Studio-Website
cd Tiger-Studio-Website
npm install
```

## 2. Umgebungsdatei

```bash
cp .env.example .env.local
```

| Variable | Zweck |
| --- | --- |
| `GITHUB_ORG` | Standard ist `Tiger-Studio-WAB` |
| `GITHUB_TOKEN` | Optional. Hebt GitHub-API-Limits für den öffentlichen Hub (Produkte, News). **Nicht** für Join. |
| `NEXT_PUBLIC_SUPABASE_URL` | Ideenboard. Aus der Vercel-/Supabase-Integration. |
| `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY` oder `NEXT_PUBLIC_SUPABASE_ANON_KEY` | Öffentlicher Supabase-Schlüssel |
| `ALLOWED_EMAIL_DOMAIN` | Optionales Microsoft-Domain-Tor |

Ohne Supabase-Variablen laufen die Marketingseiten trotzdem. **Join / Proj.Help** braucht sie.

Für einen vollständigen Join-Stack auf deinem Rechner dieselben Provider wie in Produktion nutzen (GitHub-OAuth in Supabase). Lokales Microsoft/Azure ist Extra-Setup; GitHub-Anmeldung braucht keine Schul-Admin-Freigabe.

## 3. Dev-Server

```bash
npm run dev
```

[http://localhost:3000](http://localhost:3000) öffnen.

Nützliche Skripte aus `package.json`: `npm run lint`, `npm run build`.

## Verwandt

- [Vercel-Deploys](/docs/website/vercel)
- [Supabase](/docs/website/supabase)
