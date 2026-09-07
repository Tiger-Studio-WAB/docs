---
title: Clone a repository
description: Copy a Tiger Studio GitHub repo onto your computer.
order: 3
---

# Clone a repository

Cloning downloads the project and its history. You need [Git installed](/docs/git/install) first.

## 1. Pick the repo

Studio work lives under [Tiger-Studio-WAB](https://github.com/Tiger-Studio-WAB). Common ones:

| Repo | What it is |
| --- | --- |
| [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website) | Public hub (Vercel + TypeScript) |
| [`docs`](https://github.com/Tiger-Studio-WAB/docs) | This handbook |
| [`WAB-Project-1`](https://github.com/Tiger-Studio-WAB/WAB-Project-1) | Godot 4.7 platformer |

On GitHub, click **Code** → copy the HTTPS URL.

## 2. Clone with Git

```bash
git clone https://github.com/Tiger-Studio-WAB/docs.git
cd docs
```

Replace `docs` with the repo name you need.

## 3. Clone with GitHub CLI

If [GitHub CLI](/docs/github-cli) is signed in:

```bash
gh repo clone Tiger-Studio-WAB/docs
cd docs
```

## After a clone

- **Website** — see [Run the website locally](/docs/website/local)
- **Godot** — see [Open a Godot project](/docs/godot/open)

Do not clone into a folder that already has a `.git` directory. Pick an empty directory or a new folder name.
