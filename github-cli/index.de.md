---
title: GitHub CLI
description: Mit GitHub vom Terminal aus sprechen — klonen, Pull Requests und Issues.
order: 1
review_status: draft-for-mingli29
---

# GitHub CLI

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

[`gh`](https://cli.github.com/) ist GitHubs Kommandozeilen-Werkzeug. Nutze es, nachdem [Git](/docs/git) installiert ist, wenn du Pull Requests, Issues und Klone ohne Klicken durch die Website willst.

Die Studio-Organisation ist [`Tiger-Studio-WAB`](https://github.com/Tiger-Studio-WAB).

## Seiten in diesem Abschnitt

1. [GitHub CLI installieren](/docs/github-cli/install)
2. [Anmelden](/docs/github-cli/sign-in)
3. [Pull Requests](/docs/github-cli/pull-requests)
4. [Issues](/docs/github-cli/issues)

## Häufige Befehle

| Aufgabe | Befehl |
| --- | --- |
| Ein Studio-Repo klonen | `gh repo clone Tiger-Studio-WAB/docs` |
| Einen PR öffnen | `gh pr create` |
| Einen PR ansehen | `gh pr view` |
| Deine PRs listen | `gh pr list --author @me` |
| Ein Issue öffnen | `gh issue create` |

`gh` ersetzt Git **nicht**. Du machst weiterhin `git add`, `git commit` und `git push`. Die CLI übernimmt nur GitHub-eigene Jobs.
