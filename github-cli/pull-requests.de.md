---
title: Pull Requests
description: Pull Requests vom Terminal aus öffnen und prüfen.
order: 4
review_status: draft-for-mingli29
---

# Pull Requests

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Ein Pull Request (PR) bittet darum, deinen [Branch](/docs/git/branch) in `main` zu mergen. Die Review passiert auf GitHub; `gh` erstellt und prüft den PR.

## Bevor du einen öffnest

1. Den Branch [committen und pushen](/docs/git/commit)
2. Im Repo-Ordner bleiben
3. [Angemeldet](/docs/github-cli/sign-in) sein

## Erstellen

```bash
gh pr create --fill
```

`--fill` nutzt deine Commit-Nachrichten für Titel und Text. Um sie selbst zu schreiben:

```bash
gh pr create --title "Add Git how-to pages" --body "Handbook section for Git, clone, commit, and branches."
```

Der Basisbranch ist `main`, sofern du nicht `--base` übergibst.

## Prüfen

```bash
gh pr status
gh pr view
gh pr diff
```

`gh pr view --web` öffnet den PR im Browser.

## Den PR einer anderen Person auschecken

```bash
gh pr checkout 12
```

`12` durch die PR-Nummer ersetzen.

## Verwandt

- [Issues](/docs/github-cli/issues)
- [Die Website verwalten](/docs/website), wenn der PR den Hub betrifft
