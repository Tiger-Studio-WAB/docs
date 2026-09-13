---
title: Ein Projekt öffnen und ausführen
description: WAB-Project-1 in Godot importieren und vom Hauptmenü aus spielen.
order: 3
review_status: draft-for-mingli29
---

# Ein Projekt öffnen und ausführen

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

## 1. Das Repo klonen

```bash
gh repo clone Tiger-Studio-WAB/WAB-Project-1
cd WAB-Project-1
```

HTTPS mit `git clone` ist dasselbe. Siehe [Ein Repository klonen](/docs/git/clone).

## 2. In Godot importieren

1. [Godot 4.7](/docs/godot/install) starten.
2. Project Manager → **Import**.
3. `project.godot` im geklonten Ordner auswählen.
4. **Import & Edit**.

Beim ersten Öffnen entsteht `.godot/` (Cache und Imports). Dieser Ordner ist gitignored.

## 3. Spielen

- **F5** oder den Play-Button drücken
- Hauptszene: `res://ui/main_menu.tscn`
- **Start Game** lädt das Beispiellevel

| Aktion | Tasten |
| --- | --- |
| Bewegen | `A` / `D` oder Pfeile |
| Springen | `Space`, `W` oder Hoch |
| Pause | `Esc` |

## Optionale Headless-Checks

Wenn `godot` auf dem PATH liegt:

```bash
godot --headless --path . --script res://tests/validate_load.gd
godot --headless --path . --script res://tests/validate_gameplay.gd
```

Beide sollten eine Zeile „validation passed“ ausgeben.

## Pinke Texturen oder fehlender Boden

Godot schließen, `.godot/` löschen, erneut öffnen und auf Imports warten. Weitere Fixes stehen in `docs/GETTING_STARTED.md` des Repos.

## Verwandt

- [Szenen, Skripte und Git](/docs/godot/scenes)
