---
title: Branches
description: An einem Feature arbeiten, ohne main zu ändern, bis ein Pull Request landet.
order: 5
review_status: draft-for-mingli29
---

# Branches

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

`main` ist der Standardbranch für Studio-Repos. Neue Arbeit liegt auf einem benannten Branch; ein Pull Request merged sie.

## Einen Branch anlegen

Vom aktuellen `main`:

```bash
git checkout main
git pull origin main
git checkout -b docs/git-handbook
```

Nutze einen kurzen Namen, der die Änderung sagt: `docs/…`, `fix/…`, `feature/…`. Godot-Mitarbeitende an WAB-Project-1 nutzen `feature/<short-description>` und `fix/<short-description>` — siehe `CONTRIBUTING.md` in diesem Repo.

## Wechseln und aktualisieren

```bash
git checkout docs/git-handbook
git pull origin main
```

Zieh `main` in deinen Branch, bevor du einen PR öffnest, falls `main` weitergegangen ist — sonst kämpft die Review gegen alten Code.

## Typischer Ablauf

1. Von `main` branchen
2. [Committen und pushen](/docs/git/commit)
3. [Einen Pull Request öffnen](/docs/github-cli/pull-requests)
4. Nach dem Merge zurückwechseln: `git checkout main && git pull`

## Verwandt

- [GitHub CLI](/docs/github-cli)
- [Committen und pushen](/docs/git/commit)
