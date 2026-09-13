---
title: 安装 Godot
description: 为工作室项目安装 Standard 版 Godot 4.7 编辑器。
order: 2
---

# 安装 Godot

WAB-Project-1 目标是 Godot **4.7 或更新**。较旧的 4.x 版本也许能打开项目，但不在支持范围。

## 1. 下载编辑器

1. 打开 [godotengine.org/download](https://godotengine.org/download/)。
2. 下载 **Standard** 构建，而不是 .NET / C# 构建，除非维护者让你用 C#。
3. 解压或安装到你找得到的位置（macOS 上的 Applications，Windows 上的某个文件夹）。

运行工作室模板不需要 Steam 或 Asset Library。

## 2. 可选：把 Godot 放到 PATH

模板里的无头检查需要 `godot` 命令：

```bash
godot --version
```

在 macOS 上，二进制文件通常是：

```text
/Applications/Godot.app/Contents/MacOS/Godot
```

如果该路径可用，你可以在 shell 里把它别名为 `godot`。

## 3. 接下来

[克隆](/docs/git/clone) `WAB-Project-1`，然后 [打开它](/docs/godot/open)。
