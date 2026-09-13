---
title: 打开并运行项目
description: 在 Godot 中导入 WAB-Project-1，并从主菜单开始游玩。
order: 3
---

# 打开并运行项目

## 1. 克隆仓库

```bash
gh repo clone Tiger-Studio-WAB/WAB-Project-1
cd WAB-Project-1
```

用 HTTPS 的 `git clone` 效果相同。见 [克隆仓库](/docs/git/clone)。

## 2. 在 Godot 中导入

1. 启动 [Godot 4.7](/docs/godot/install)。
2. Project Manager → **Import**。
3. 选择克隆文件夹里的 `project.godot`。
4. **Import & Edit**。

第一次打开会生成 `.godot/`（缓存与导入）。该文件夹已被 gitignore。

## 3. 游玩

- 按 **F5** 或 Play 按钮
- 主场景：`res://ui/main_menu.tscn`
- **Start Game** 加载示例关卡

| 操作 | 按键 |
| --- | --- |
| 移动 | `A` / `D` 或方向键 |
| 跳跃 | `Space`、`W` 或上方向键 |
| 暂停 | `Esc` |

## 可选的无头检查

如果 `godot` 已在 PATH 上：

```bash
godot --headless --path . --script res://tests/validate_load.gd
godot --headless --path . --script res://tests/validate_gameplay.gd
```

两者都应打印一行 “validation passed”。

## 粉色贴图或地面缺失

关闭 Godot，删除 `.godot/`，重新打开，等待导入完成。更多修复见该仓库的 `docs/GETTING_STARTED.md`。

## 相关

- [场景、脚本与 Git](/docs/godot/scenes)
