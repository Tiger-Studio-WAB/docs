---
title: 场景、脚本与 Git
description: 改什么、提交什么，以及 Godot 文件如何对应到 Git。
order: 4
---

# 场景、脚本与 Git

Godot 项目是文本场景（`.tscn`）、脚本（`.gd`）和资源组成的文件夹。Git 把它们当成普通文件。

## 东西放哪里（WAB-Project-1）

| 文件夹 | 放这里 |
| --- | --- |
| `entities/` | 玩家和其他角色 |
| `levels/` | 关卡场景与图块集 |
| `scenes/` | 游戏流程（例如正在运行的游戏） |
| `ui/` | 菜单与 HUD |
| `autoloads/` | 单例，例如 `GameState` |
| `assets/` | 美术 |

把脚本和它的场景放在一起。`.gd` 文件的缩进与现有制表符一致。优先用 Input Map 动作，而不是写死按键。

## 要提交这些

- `.gd`、`.tscn`、`.tres`、`project.godot`
- `.uid` 文件（Godot 4 资源 ID — 让引用保持稳定）

## 不要提交这些

| 路径 | 原因 |
| --- | --- |
| `.godot/` | 本地编辑器缓存 |
| 导出的二进制 / 构建产物 | 需要时再重建 |
| 系统垃圾 | 噪音 |

## 受邀协作者的分支方式

游戏仓库是 All Rights Reserved。只有受邀协作者提交 PR。他们的模式：

- `feature/<short-description>`
- `fix/<short-description>`
- 目标分支：`main`

打开 PR 前先看 WAB-Project-1 里的 `CONTRIBUTING.md`。

## 相关

- [提交并推送](/docs/git/commit)
- [拉取请求](/docs/github-cli/pull-requests)
