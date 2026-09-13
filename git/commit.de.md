---
title: Committen und pushen
description: Einen Snapshot lokal speichern und dann zu GitHub senden.
order: 4
review_status: draft-for-mingli29
---

# Committen und pushen

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Ein **Commit** ist ein Snapshot auf deinem Rechner. Ein **Push** sendet diese Snapshots zu GitHub, damit der Rest des Studios sie sehen kann.

Arbeite auf einem [Branch](/docs/git/branch), nicht auf `main`, sofern nicht eine Maintainerin oder ein Maintainer das verlangt hat.

## 1. Sehen, was sich geändert hat

```bash
git status
git diff
```

`status` listet Dateien. `diff` zeigt die Änderungen.

## 2. Stagen und committen

```bash
git add .
git commit -m "Add clone steps to the Git handbook"
```

- `git add .` staged jede Änderung im aktuellen Ordner. Bevorzuge `git add path/to/file.md`, wenn du nur manche Dateien willst.
- Schreibe einen kurzen, imperativen Betreff: „Add…“, „Fix…“, „Document…“.

## 3. Den Branch pushen

```bash
git push -u origin HEAD
```

Der erste Push auf einem neuen Branch nutzt `-u`, damit du später `git push` ohne Extra-Flags ausführen kannst.

Wenn GitHub dich zur Anmeldung auffordert, nutze die Browser-Aufforderung oder die [GitHub CLI](/docs/github-cli/sign-in).

## 4. Einen Pull Request öffnen

Wenn der Branch auf GitHub ist, öffne einen PR. Schnellster Weg: [GitHub-CLI-Pull-Requests](/docs/github-cli/pull-requests).

## Was du nicht committen sollst

| Draußen lassen | Warum |
| --- | --- |
| `.env.local`, Geheimnisse, API-Keys | Sie öffnen die Produktion |
| `node_modules/` | Wird mit `npm install` neu gebaut |
| `.godot/` | Godot-Editor-Cache |
| OS-Müll (`.DS_Store`) | Rauschen |

Die `.gitignore` jedes Repos deckt das meiste bereits ab.

## Verwandt

- [Branches](/docs/git/branch)
- [Docs formatieren](/docs/how-to-format), wenn du dieses Handbuch bearbeitest
