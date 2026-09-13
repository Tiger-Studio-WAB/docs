---
title: Docs auf dem Hub
description: Wie Ordner in diesem Repo nach einer Aktualisierung zu /docs-Seiten werden.
order: 5
review_status: draft-for-mingli29
---

# Docs auf dem Hub

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Das Handbuch unter `/docs` ist **kein** eigenes Vercel-Projekt. Die Website lädt Markdown aus [`Tiger-Studio-WAB/docs`](https://github.com/Tiger-Studio-WAB/docs) (dieses Repo). Fehlende Dateien können auf einen Starter-Baum zurückfallen, der mit dem Hub ausgeliefert wird.

## Eine Seite hinzufügen oder ändern

1. [Docs formatieren](/docs/how-to-format) folgen: Ordner, `index.md`, optionales `_category.json`
2. In **diesem** Repo nach `main` mergen
3. Etwa zwei Minuten warten, dann `/docs` öffnen und die Seitenleiste prüfen

Für nur-textliche Handbuchänderungen öffnest du keinen PR auf `Tiger-Studio-Website`.

## Wann du das Website-Repo *doch* änderst

Ändere `Tiger-Studio-Website` nur, wenn die **Docs-App** falsch ist (Seitenleisten-Renderer, Fetch, Routing). Das ist TypeScript unter `src/lib/docs.ts` und `src/app/docs/`. Mit einer [Vercel](/docs/website/vercel)-Preview ausliefern.

## Support ist getrennt

Lege hier keinen `support`-Ordner an. Hilfe und Tickets sind [/support](/support) und das [`support`](https://github.com/Tiger-Studio-WAB/support)-Repo.

## Verwandt

- [Docs formatieren](/docs/how-to-format)
- [Die Website verwalten](/docs/website)
