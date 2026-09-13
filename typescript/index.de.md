---
title: TypeScript
description: Typisiertes JavaScript, das auf der Tiger-Studio-Website verwendet wird.
order: 1
review_status: draft-for-mingli29
---

# TypeScript

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Der öffentliche Hub ist eine **Next.js**-App in **TypeScript** (`.ts` / `.tsx`). Godot-Spiele in diesem Studio nutzen GDScript, nicht TypeScript.

Du brauchst TypeScript nur, wenn du [Tiger-Studio-Website](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website) (oder ein anderes Node-Projekt) änderst. Markdown in **dieses** `docs`-Repo hinzuzufügen braucht kein TypeScript — siehe [Docs formatieren](/docs/how-to-format).

## Seiten in diesem Abschnitt

1. [Node.js und TypeScript installieren](/docs/typescript/install)
2. [TypeScript auf der Website](/docs/typescript/website)

## Was „TypeScript“ hier bedeutet

| Datei | Rolle |
| --- | --- |
| `.ts` | Logik, Helfer, Konfiguration |
| `.tsx` | React-Seiten und Komponenten |
| `tsconfig.json` | Compiler-Optionen für das Repo |
| `package.json` | `typescript` als Dev-Abhängigkeit |

Die Website enthält TypeScript bereits. Du installierst kein globales `tsc`, außer du willst es. `npm install` im Website-Repo reicht.
