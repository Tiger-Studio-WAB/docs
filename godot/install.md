---
title: Install Godot
description: Install the Standard Godot 4.7 editor for studio projects.
order: 2
---

# Install Godot

WAB-Project-1 targets Godot **4.7 or newer**. Older 4.x builds may open the project but are not supported.

## 1. Download the editor

1. Open [godotengine.org/download](https://godotengine.org/download/).
2. Get the **Standard** build, not the .NET / C# build, unless a maintainer asked you to use C#.
3. Unzip or install it somewhere you can find (Applications on macOS, a folder on Windows).

You do not need Steam or the Asset Library to run the studio template.

## 2. Optional: put Godot on your PATH

Headless checks in the template need the `godot` command:

```bash
godot --version
```

On macOS the binary is often:

```text
/Applications/Godot.app/Contents/MacOS/Godot
```

If that path works, you can alias it to `godot` in your shell.

## 3. Next

[Clone](/docs/git/clone) `WAB-Project-1`, then [open it](/docs/godot/open).
