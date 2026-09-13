---
title: Issues
description: GitHub-Issues mit gh anlegen und listen.
order: 5
review_status: draft-for-mingli29
---

# Issues

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Nutze Issues für Bugs und Aufgaben an einem **Code**-Repo. Club-Hilfe („Ich kann mich nicht anmelden“) gehört zu [Support](/support), das das [`support`](https://github.com/Tiger-Studio-WAB/support)-Repo liest.

## Ein Issue anlegen

Aus einem geklonten Repo heraus:

```bash
gh issue create --title "Pause menu ignores Esc on first frame" --body "Godot 4.7.2, Windows. Steps: start level, press Esc immediately."
```

Oder den Fragen folgen:

```bash
gh issue create
```

WAB-Project-1 hat Issue-Vorlagen (Bug, Feature). Bevorzuge **New issue** auf GitHub, wenn du diese Formulare willst; `gh` funktioniert weiterhin für ein schlichtes Issue.

## Listen und ansehen

```bash
gh issue list
gh issue view 3
gh issue view 3 --web
```

## Docs vs Support vs Issues

| Situation | Wo |
| --- | --- |
| Wie Git / Godot / die Site funktioniert | Diese Docs |
| Konto, kaputte Seite, einen Menschen brauchen | [/support](/support) |
| Bug oder Feature an einem bestimmten Repo | Die Issues dieses Repos |

## Verwandt

- [Pull Requests](/docs/github-cli/pull-requests)
- [Produkte](/docs/products)
