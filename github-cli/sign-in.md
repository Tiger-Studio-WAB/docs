---
title: Sign in
description: Authenticate gh so it can act as your GitHub user.
order: 3
---

# Sign in

GitHub CLI needs a logged-in account before it can clone private repos, open PRs, or file issues.

## 1. Start login

```bash
gh auth login
```

## 2. Answer the prompts

1. **GitHub.com**
2. **HTTPS** (simplest on school machines)
3. Authenticate **Login with a web browser**
4. Copy the one-time code, press Enter, and approve in the browser

SSH is fine if you already use SSH keys. HTTPS + browser is the path that works without extra key setup.

## 3. Confirm

```bash
gh auth status
```

You should see your GitHub username and `Logged in to github.com`.

## If login fails

- Complete the browser step; do not close the tab early
- School machines sometimes block the redirect — try another browser or a personal device
- Account problems are [Support](/support), not a docs bug

## Related

- [Pull requests](/docs/github-cli/pull-requests)
- [Clone a repository](/docs/git/clone)
