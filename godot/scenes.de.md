---
title: Szenen, Skripte und Git
description: Was du bearbeitest, was du committest, und wie Godot-Dateien auf Git abgebildet werden.
order: 4
review_status: draft-for-mingli29
---

# Szenen, Skripte und Git

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Godot-Projekte sind Ordner aus Text-Szenen (`.tscn`), Skripten (`.gd`) und Ressourcen. Git sieht sie als normale Dateien.

## Wo Dinge liegen (WAB-Project-1)

| Ordner | Hier ablegen |
| --- | --- |
| `entities/` | Spielerinnen/Spieler und andere Akteure |
| `levels/` | Level-Szenen und Tilesets |
| `scenes/` | Spielfluss (z. B. das laufende Spiel) |
| `ui/` | Menüs und HUD |
| `autoloads/` | Singletons wie `GameState` |
| `assets/` | Artwork |

Lege ein Skript neben seine Szene. Halte die vorhandene Tab-Einrückung in `.gd`-Dateien ein. Bevorzuge Input-Map-Aktionen statt fest kodierter Tasten.

## Diese committen

- `.gd`, `.tscn`, `.tres`, `project.godot`
- `.uid`-Dateien (Godot-4-Ressourcen-IDs — sie halten Referenzen stabil)

## Diese nicht committen

| Pfad | Warum |
| --- | --- |
| `.godot/` | Lokaler Editor-Cache |
| Export-Binaries / Builds | Bei Bedarf neu bauen |
| OS-Müll | Rauschen |

## Branching für eingeladene Mitarbeitende

Das Spiel-Repo ist All Rights Reserved. Nur eingeladene Collaborators senden PRs. Ihr Muster:

- `feature/<short-description>`
- `fix/<short-description>`
- Basis: `main`

Siehe `CONTRIBUTING.md` in WAB-Project-1, bevor du einen PR öffnest.

## Verwandt

- [Committen und pushen](/docs/git/commit)
- [Pull Requests](/docs/github-cli/pull-requests)
