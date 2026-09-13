---
title: GitHub CLI
description: 在终端里与 GitHub 对话 — 克隆、拉取请求与议题。
order: 1
---

# GitHub CLI

[`gh`](https://cli.github.com/) 是 GitHub 的命令行工具。在 [Git](/docs/git) 装好之后，想不用点网站就能处理拉取请求、议题和克隆时使用它。

工作室组织是 [`Tiger-Studio-WAB`](https://github.com/Tiger-Studio-WAB)。

## 本分区页面

1. [安装 GitHub CLI](/docs/github-cli/install)
2. [登录](/docs/github-cli/sign-in)
3. [拉取请求](/docs/github-cli/pull-requests)
4. [议题](/docs/github-cli/issues)

## 常用命令

| 任务 | 命令 |
| --- | --- |
| 克隆工作室仓库 | `gh repo clone Tiger-Studio-WAB/docs` |
| 打开 PR | `gh pr create` |
| 查看 PR | `gh pr view` |
| 列出你的 PR | `gh pr list --author @me` |
| 打开议题 | `gh issue create` |

`gh` **不能**替代 Git。你仍然要 `git add`、`git commit` 和 `git push`。CLI 只处理仅属于 GitHub 的工作。
