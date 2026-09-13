---
title: 克隆仓库
description: 把 Tiger Studio 的 GitHub 仓库复制到你的电脑。
order: 3
---

# 克隆仓库

克隆会下载项目及其历史。你需要先 [安装 Git](/docs/git/install)。

## 1. 选择仓库

工作室的工作在 [Tiger-Studio-WAB](https://github.com/Tiger-Studio-WAB) 下。常见的有：

| 仓库 | 是什么 |
| --- | --- |
| [`Tiger-Studio-Website`](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website) | 公开枢纽（Vercel + TypeScript） |
| [`docs`](https://github.com/Tiger-Studio-WAB/docs) | 本手册 |
| [`WAB-Project-1`](https://github.com/Tiger-Studio-WAB/WAB-Project-1) | Godot 4.7 平台跳跃 |

在 GitHub 上点击 **Code** → 复制 HTTPS URL。

## 2. 用 Git 克隆

```bash
git clone https://github.com/Tiger-Studio-WAB/docs.git
cd docs
```

把 `docs` 换成你需要的仓库名。

## 3. 用 GitHub CLI 克隆

如果 [GitHub CLI](/docs/github-cli) 已登录：

```bash
gh repo clone Tiger-Studio-WAB/docs
cd docs
```

## 克隆之后

- **网站** — 见 [在本地运行网站](/docs/website/local)
- **Godot** — 见 [打开 Godot 项目](/docs/godot/open)

不要克隆到已经有 `.git` 目录的文件夹里。选一个空目录或新的文件夹名。
