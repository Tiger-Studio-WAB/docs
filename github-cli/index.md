---
title: GitHub CLI
description: Talk to GitHub from the terminal — clone, pull requests, and issues.
order: 1
---

# GitHub CLI

[`gh`](https://cli.github.com/) is GitHub’s command-line tool. Use it after [Git](/docs/git) is installed when you want pull requests, issues, and clones without clicking through the website.

The studio org is [`Tiger-Studio-WAB`](https://github.com/Tiger-Studio-WAB).

## Pages in this section

1. [Install GitHub CLI](/docs/github-cli/install)
2. [Sign in](/docs/github-cli/sign-in)
3. [Pull requests](/docs/github-cli/pull-requests)
4. [Issues](/docs/github-cli/issues)

## Common commands

| Task | Command |
| --- | --- |
| Clone a studio repo | `gh repo clone Tiger-Studio-WAB/docs` |
| Open a PR | `gh pr create` |
| View a PR | `gh pr view` |
| List your PRs | `gh pr list --author @me` |
| Open an issue | `gh issue create` |

`gh` does **not** replace Git. You still `git add`, `git commit`, and `git push`. CLI handles GitHub-only jobs.
