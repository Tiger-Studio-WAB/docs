---
title: Issues
description: File and list GitHub issues with gh.
order: 5
---

# Issues

Use issues for bugs and tasks on a **code** repo. Club help (“I cannot sign in”) belongs on [Support](/support), which reads the [`support`](https://github.com/Tiger-Studio-WAB/support) repo.

## Create an issue

From inside a cloned repo:

```bash
gh issue create --title "Pause menu ignores Esc on first frame" --body "Godot 4.7.2, Windows. Steps: start level, press Esc immediately."
```

Or follow prompts:

```bash
gh issue create
```

WAB-Project-1 has issue templates (bug, feature). Prefer **New issue** on GitHub if you want those forms; `gh` still works for a plain issue.

## List and view

```bash
gh issue list
gh issue view 3
gh issue view 3 --web
```

## Docs vs Support vs Issues

| Situation | Where |
| --- | --- |
| How Git / Godot / the site works | These docs |
| Account, broken page, need a human | [/support](/support) |
| Bug or feature on a specific repo | That repo’s issues |

## Related

- [Pull requests](/docs/github-cli/pull-requests)
- [Products](/docs/products)
