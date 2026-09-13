---
title: 议题
description: 用 gh 创建并列出 GitHub 议题。
order: 5
---

# 议题

议题用在 **代码** 仓库上的缺陷与任务。社团帮助（“我登不进去”）属于 [支持](/support)，它读取 [`support`](https://github.com/Tiger-Studio-WAB/support) 仓库。

## 创建议题

在已克隆的仓库内：

```bash
gh issue create --title "Pause menu ignores Esc on first frame" --body "Godot 4.7.2, Windows. Steps: start level, press Esc immediately."
```

或按提示操作：

```bash
gh issue create
```

WAB-Project-1 有议题模板（缺陷、功能）。如果你想用那些表单，优先在 GitHub 上点 **New issue**；`gh` 仍可用于普通议题。

## 列出与查看

```bash
gh issue list
gh issue view 3
gh issue view 3 --web
```

## 文档 vs 支持 vs 议题

| 情况 | 去哪 |
| --- | --- |
| Git / Godot / 网站如何工作 | 本手册 |
| 账号、页面损坏、需要真人 | [/support](/support) |
| 某个具体仓库的缺陷或功能 | 该仓库的议题 |

## 相关

- [拉取请求](/docs/github-cli/pull-requests)
- [产品](/docs/products)
