---
title: TypeScript auf der Website
description: Wo Typen im Hub leben und wie du sie sicher änderst.
order: 3
review_status: draft-for-mingli29
---

# TypeScript auf der Website

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Repo: [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website). App-Router-Dateien liegen unter `src/`.

## Ordner, die du anfassen wirst

| Pfad | Was es ist |
| --- | --- |
| `src/app/` | Routen (`page.tsx`, `layout.tsx`, Route-Handler) |
| `src/components/` | UI |
| `src/lib/` | GitHub-Fetch, Docs-Loader, Supabase-Helfer |
| `src/lib/supabase/` | Browser-/Server-Supabase-Clients |
| `vercel.ts` | Vercel-Projektkonfiguration (typisiert) |
| `supabase/migrations/` | SQL für Join / Proj.Help, nicht TypeScript |

## Gewohnheiten, die den Build grün halten

1. Typen in `src/lib/types.ts` und benachbarten Modulen wiederverwenden statt `any`.
2. Nur-Server-Geheimnisse bleiben **ohne** `NEXT_PUBLIC_`-Namen. Öffentliche Supabase-URL und Publishable-/Anon-Key sind die Ausnahme — siehe [Supabase](/docs/website/supabase).
3. Nach UI-Änderungen lokal `npm run lint` und `npm run build` ausführen, wenn du kannst.
4. Keine Next.js-Internals bearbeiten, um eine Docs-Seite hinzuzufügen. Stattdessen Markdown in **diesem** Repo anlegen.

## Konfigurationshinweis

`tsconfig.json` ist bereits für den App Router gesetzt. Für ein normales Feature solltest du `strict` oder Paths nicht ändern müssen.

## Verwandt

- [Die Website verwalten](/docs/website)
- [Docs formatieren](/docs/how-to-format)
