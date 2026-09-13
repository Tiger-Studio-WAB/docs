---
title: Git installieren
description: Git auf den Rechner bringen und prüfen, dass es läuft.
order: 2
review_status: draft-for-mingli29
---

# Git installieren

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

## 1. Herunterladen

- **Windows** — [git-scm.com/download/win](https://git-scm.com/download/win). Die Vorgaben belassen. Git Bash ist in Ordnung.
- **macOS** — [Xcode Command Line Tools](https://developer.apple.com/xcode/resources/) installieren (`xcode-select --install`) oder [Git for macOS](https://git-scm.com/download/mac).
- **Linux** — das Distro-Paket nutzen, zum Beispiel `sudo apt install git`.

GitHubs [Git handbook](https://docs.github.com/en/get-started/git-basics/set-up-git) beschreibt dieselben Schritte mit Screenshots.

## 2. Prüfen

Ein Terminal öffnen und ausführen:

```bash
git --version
```

Du solltest eine Versionsnummer sehen. Wenn der Befehl nicht gefunden wird, das Terminal schließen, neu öffnen und erneut versuchen.

## 3. Namen und E-Mail setzen

Git speichert diese Angaben in jedem Commit. Nutze dieselbe E-Mail wie bei deinem GitHub-Konto.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Verwandt

- [Ein Repository klonen](/docs/git/clone)
- [GitHub CLI installieren](/docs/github-cli/install)
