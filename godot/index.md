---
title: Godot
description: Open and run Tiger Studio Godot projects, starting with WAB-Project-1.
order: 1
---

# Godot

Godot is the game engine the studio uses for 2D work. The first public game repo is [`WAB-Project-1`](https://github.com/Tiger-Studio-WAB/WAB-Project-1): a Godot **4.7** 2D platformer template (GDScript, not C#).

You edit scenes and scripts in the Godot editor. Git still stores the project. Do not commit the editor cache.

## Pages in this section

1. [Install Godot](/docs/godot/install)
2. [Open and run a project](/docs/godot/open)
3. [Scenes, scripts, and Git](/docs/godot/scenes)

## Studio conventions (short)

- Engine version: **4.7+** (template tested on 4.7.2)
- Language: **GDScript**, Standard (non-.NET) editor
- Renderer: **GL Compatibility** for this template
- `.uid` files: commit them
- `.godot/`: never commit it

Full layout, physics layers, and PR rules live in that repo: `docs/GETTING_STARTED.md`, `docs/ARCHITECTURE.md`, and `CONTRIBUTING.md`.
