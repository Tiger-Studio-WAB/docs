---
title: Pull requests
description: Open and inspect pull requests from the terminal.
order: 4
---

# Pull requests

A pull request (PR) asks to merge your [branch](/docs/git/branch) into `main`. Review happens on GitHub; `gh` creates and inspects the PR.

## Before you open one

1. [Commit and push](/docs/git/commit) the branch
2. Stay in the repo folder
3. Be [signed in](/docs/github-cli/sign-in)

## Create

```bash
gh pr create --fill
```

`--fill` uses your commit messages for title and body. To write them yourself:

```bash
gh pr create --title "Add Git how-to pages" --body "Handbook section for Git, clone, commit, and branches."
```

Base branch is `main` unless you pass `--base`.

## Inspect

```bash
gh pr status
gh pr view
gh pr diff
```

`gh pr view --web` opens the PR in the browser.

## Checkout someone else’s PR

```bash
gh pr checkout 12
```

Replace `12` with the PR number.

## Related

- [Issues](/docs/github-cli/issues)
- [Manage the website](/docs/website) if the PR is for the hub
