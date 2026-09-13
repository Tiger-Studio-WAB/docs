---
title: Ein Repository klonen
description: Ein Tiger-Studio-GitHub-Repo auf den Rechner kopieren.
order: 3
review_status: draft-for-mingli29
---

# Ein Repository klonen

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Klonen lädt das Projekt und seine Historie herunter. Du brauchst zuerst [Git installiert](/docs/git/install).

## 1. Das Repo wählen

Studio-Arbeit liegt unter [Tiger-Studio-WAB](https://github.com/Tiger-Studio-WAB). Häufige:

| Repo | Was es ist |
| --- | --- |
| [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website) | Öffentlicher Hub (Vercel + TypeScript) |
| [`docs`](https://github.com/Tiger-Studio-WAB/docs) | Dieses Handbuch |
| [`WAB-Project-1`](https://github.com/Tiger-Studio-WAB/WAB-Project-1) | Godot-4.7-Plattformer |

Auf GitHub **Code** klicken → die HTTPS-URL kopieren.

## 2. Mit Git klonen

```bash
git clone https://github.com/Tiger-Studio-WAB/docs.git
cd docs
```

`docs` durch den benötigten Repo-Namen ersetzen.

## 3. Mit GitHub CLI klonen

Wenn die [GitHub CLI](/docs/github-cli) angemeldet ist:

```bash
gh repo clone Tiger-Studio-WAB/docs
cd docs
```

## Nach dem Klonen

- **Website** — siehe [Die Website lokal ausführen](/docs/website/local)
- **Godot** — siehe [Ein Godot-Projekt öffnen](/docs/godot/open)

Nicht in einen Ordner klonen, der bereits ein `.git`-Verzeichnis hat. Ein leeres Verzeichnis oder einen neuen Ordnernamen wählen.
