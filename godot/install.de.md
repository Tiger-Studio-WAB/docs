---
title: Godot installieren
description: Den Standard-Godot-4.7-Editor für Studio-Projekte installieren.
order: 2
review_status: draft-for-mingli29
---

# Godot installieren

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

WAB-Project-1 zielt auf Godot **4.7 oder neuer**. Ältere 4.x-Builds öffnen das Projekt möglicherweise, werden aber nicht unterstützt.

## 1. Den Editor herunterladen

1. [godotengine.org/download](https://godotengine.org/download/) öffnen.
2. Den **Standard**-Build holen, nicht den .NET-/C#-Build, sofern nicht eine Maintainerin oder ein Maintainer C# verlangt hat.
3. Entpacken oder an einem auffindbaren Ort installieren (Applications auf macOS, ein Ordner unter Windows).

Du brauchst weder Steam noch die Asset Library, um die Studio-Vorlage zu starten.

## 2. Optional: Godot auf den PATH legen

Headless-Checks in der Vorlage brauchen den Befehl `godot`:

```bash
godot --version
```

Unter macOS liegt die Binary oft hier:

```text
/Applications/Godot.app/Contents/MacOS/Godot
```

Wenn dieser Pfad funktioniert, kannst du ihn in der Shell als `godot` aliasen.

## 3. Als Nächstes

`WAB-Project-1` [klonen](/docs/git/clone) und dann [öffnen](/docs/godot/open).
