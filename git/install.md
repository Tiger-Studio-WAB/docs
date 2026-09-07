---
title: Install Git
description: Put Git on your computer and check that it runs.
order: 2
---

# Install Git

## 1. Download it

- **Windows** — [git-scm.com/download/win](https://git-scm.com/download/win). Keep the defaults. Git Bash is fine.
- **macOS** — install [Xcode Command Line Tools](https://developer.apple.com/xcode/resources/) (`xcode-select --install`) or [Git for macOS](https://git-scm.com/download/mac).
- **Linux** — use the distro package, for example `sudo apt install git`.

GitHub’s [Git handbook](https://docs.github.com/en/get-started/git-basics/set-up-git) covers the same steps with screenshots.

## 2. Check it

Open a terminal and run:

```bash
git --version
```

You should see a version number. If the command is not found, close the terminal, reopen it, and try again.

## 3. Set your name and email

Git stores these on every commit. Use the same email as your GitHub account.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Related

- [Clone a repository](/docs/git/clone)
- [GitHub CLI install](/docs/github-cli/install)
