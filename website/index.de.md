---
title: Die Website verwalten
description: Wie der Tiger-Studio-Hub auf Vercel gehostet und in Supabase gespeichert wird.
order: 1
review_status: draft-for-mingli29
---

# Die Website verwalten

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Der öffentliche Hub ist [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website). Live-URL: [tiger-studio-website.vercel.app](https://tiger-studio-website.vercel.app).

## Wer macht was

| Schicht | Produkt | Enthält |
| --- | --- | --- |
| Host / CDN / Builds | **Vercel** | Next.js-App, Previews, Umgebungsvariablen, Deploys von GitHub |
| Daten / Auth | **Supabase** | Proj.Help-Ideen, Antworten, Sitzungen (Postgres + Auth) |
| Handbuchtext | **Dieses `docs`-Repo** | Markdown-Ordner; die Site holt sie |
| Support-Text | [`support`](https://github.com/Tiger-Studio-WAB/support) | Hilfeseite / Issue-Vorlagen |

Vercel speichert das Ideenboard **nicht**. Die Vercel-Marketplace-Supabase-Integration synchronisiert nur Umgebungsvariablen. Schema und OAuth leben weiterhin in Supabase Studio.

## Seiten in diesem Abschnitt

1. [Lokal ausführen](/docs/website/local)
2. [Vercel-Deploys](/docs/website/vercel)
3. [Supabase](/docs/website/supabase)
4. [Docs auf dem Hub](/docs/website/docs)

Code-Änderungen: [TypeScript](/docs/typescript) und ein [Pull Request](/docs/github-cli/pull-requests). Nur-Text-Handbuchedits: Markdown hier hinzufügen — [Docs formatieren](/docs/how-to-format).
