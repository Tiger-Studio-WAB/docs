---
title: Branches
description: Work on a feature without changing main until a pull request lands.
order: 5
---

# Branches

`main` is the default branch for studio repos. New work goes on a named branch, then a pull request merges it.

## Create a branch

From the latest `main`:

```bash
git checkout main
git pull origin main
git checkout -b docs/git-handbook
```

Use a short name that says what the change is: `docs/…`, `fix/…`, `feature/…`. Godot collaborators on WAB-Project-1 use `feature/<short-description>` and `fix/<short-description>` — see that repo’s `CONTRIBUTING.md`.

## Switch and update

```bash
git checkout docs/git-handbook
git pull origin main
```

Pull `main` into your branch before a PR if `main` moved, so the review is not fighting old code.

## Typical flow

1. Branch off `main`
2. [Commit and push](/docs/git/commit)
3. [Open a pull request](/docs/github-cli/pull-requests)
4. After merge, switch back: `git checkout main && git pull`

## Related

- [GitHub CLI](/docs/github-cli)
- [Commit and push](/docs/git/commit)
