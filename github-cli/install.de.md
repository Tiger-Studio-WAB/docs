---
title: GitHub CLI installieren
description: Den gh-Befehl auf den PATH bringen.
order: 2
review_status: draft-for-mingli29
---

# GitHub CLI installieren

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Folge GitHubs [Installationsanleitung](https://github.com/cli/cli#installation) für dein Betriebssystem. Kurzfassung:

## Windows

```powershell
winget install --id GitHub.cli
```

Oder den Installer von [cli.github.com](https://cli.github.com/) herunterladen.

## macOS

```bash
brew install gh
```

## Linux

```bash
sudo apt install gh
```

Wenn `apt` kein Paket hat, nutze die [Debian/Ubuntu-Anleitung](https://github.com/cli/cli/blob/trunk/docs/install_linux.md) aus dem CLI-Repo.

## Prüfen

```bash
gh --version
```

Dann [anmelden](/docs/github-cli/sign-in).
