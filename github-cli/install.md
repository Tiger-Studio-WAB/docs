---
title: Install GitHub CLI
description: Put the gh command on your PATH.
order: 2
---

# Install GitHub CLI

Follow GitHub’s [installation guide](https://github.com/cli/cli#installation) for your OS. Short version:

## Windows

```powershell
winget install --id GitHub.cli
```

Or download the installer from [cli.github.com](https://cli.github.com/).

## macOS

```bash
brew install gh
```

## Linux

```bash
sudo apt install gh
```

If `apt` has no package, use the [Debian/Ubuntu instructions](https://github.com/cli/cli/blob/trunk/docs/install_linux.md) from the CLI repo.

## Check it

```bash
gh --version
```

Then [sign in](/docs/github-cli/sign-in).
