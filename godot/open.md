---
title: Open and run a project
description: Import WAB-Project-1 in Godot and play from the main menu.
order: 3
---

# Open and run a project

## 1. Clone the repo

```bash
gh repo clone Tiger-Studio-WAB/WAB-Project-1
cd WAB-Project-1
```

HTTPS with `git clone` is the same. See [Clone a repository](/docs/git/clone).

## 2. Import in Godot

1. Launch [Godot 4.7](/docs/godot/install).
2. Project Manager → **Import**.
3. Select `project.godot` in the cloned folder.
4. **Import & Edit**.

First open generates `.godot/` (cache and imports). That folder is gitignored.

## 3. Play

- Press **F5** or the Play button
- Main scene: `res://ui/main_menu.tscn`
- **Start Game** loads the sample level

| Action | Keys |
| --- | --- |
| Move | `A` / `D` or arrows |
| Jump | `Space`, `W`, or Up |
| Pause | `Esc` |

## Optional headless checks

If `godot` is on your PATH:

```bash
godot --headless --path . --script res://tests/validate_load.gd
godot --headless --path . --script res://tests/validate_gameplay.gd
```

Both should print a “validation passed” line.

## Pink textures or a missing floor

Close Godot, delete `.godot/`, reopen, and wait for imports. More fixes are in the repo’s `docs/GETTING_STARTED.md`.

## Related

- [Scenes, scripts, and Git](/docs/godot/scenes)
