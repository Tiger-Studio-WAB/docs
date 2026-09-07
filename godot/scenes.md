---
title: Scenes, scripts, and Git
description: What to edit, what to commit, and how Godot files map to Git.
order: 4
---

# Scenes, scripts, and Git

Godot projects are folders of text scenes (`.tscn`), scripts (`.gd`), and resources. Git sees them as normal files.

## Where things live (WAB-Project-1)

| Folder | Put here |
| --- | --- |
| `entities/` | Players and other actors |
| `levels/` | Level scenes and tilesets |
| `scenes/` | Game flow (e.g. the running game) |
| `ui/` | Menus and HUD |
| `autoloads/` | Singletons such as `GameState` |
| `assets/` | Art |

Co-locate a script with its scene. Match existing tab indentation in `.gd` files. Prefer Input Map actions over hardcoded keys.

## Commit these

- `.gd`, `.tscn`, `.tres`, `project.godot`
- `.uid` files (Godot 4 resource IDs — they keep references stable)

## Do not commit these

| Path | Why |
| --- | --- |
| `.godot/` | Local editor cache |
| Export binaries / builds | Rebuild when you need them |
| OS junk | Noise |

## Branching for invited collaborators

The game repo is All Rights Reserved. Only invited collaborators send PRs. Their pattern:

- `feature/<short-description>`
- `fix/<short-description>`
- Base: `main`

See `CONTRIBUTING.md` in WAB-Project-1 before you open a PR.

## Related

- [Commit and push](/docs/git/commit)
- [Pull requests](/docs/github-cli/pull-requests)
