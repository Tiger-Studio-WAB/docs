---
title: Commit and push
description: Save a snapshot locally, then send it to GitHub.
order: 4
---

# Commit and push

A **commit** is a snapshot on your computer. A **push** sends those snapshots to GitHub so the rest of the studio can see them.

Work on a [branch](/docs/git/branch), not `main`, unless a maintainer asked you to.

## 1. See what changed

```bash
git status
git diff
```

`status` lists files. `diff` shows the edits.

## 2. Stage and commit

```bash
git add .
git commit -m "Add clone steps to the Git handbook"
```

- `git add .` stages every change in the current folder. Prefer `git add path/to/file.md` when you only want some files.
- Write a short, imperative subject: “Add…”, “Fix…”, “Document…”.

## 3. Push the branch

```bash
git push -u origin HEAD
```

The first push on a new branch uses `-u` so later you can run `git push` with no extra flags.

If GitHub asks you to sign in, use the browser prompt or [GitHub CLI](/docs/github-cli/sign-in).

## 4. Open a pull request

After the branch is on GitHub, open a PR. Fastest path: [GitHub CLI pull requests](/docs/github-cli/pull-requests).

## What not to commit

| Keep out | Why |
| --- | --- |
| `.env.local`, secrets, API keys | They unlock production |
| `node_modules/` | Rebuilt with `npm install` |
| `.godot/` | Godot editor cache |
| OS junk (`.DS_Store`) | Noise |

Each repo’s `.gitignore` already covers most of this.

## Related

- [Branches](/docs/git/branch)
- [How to format docs](/docs/how-to-format) if you are editing this handbook
