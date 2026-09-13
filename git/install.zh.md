---
title: 安装 Git
description: 在电脑上安装 Git 并确认可以运行。
order: 2
---

# 安装 Git

## 1. 下载

- **Windows** — [git-scm.com/download/win](https://git-scm.com/download/win)。保持默认即可。Git Bash 没问题。
- **macOS** — 安装 [Xcode Command Line Tools](https://developer.apple.com/xcode/resources/)（`xcode-select --install`）或 [Git for macOS](https://git-scm.com/download/mac)。
- **Linux** — 用发行版软件包，例如 `sudo apt install git`。

GitHub 的 [Git handbook](https://docs.github.com/en/get-started/git-basics/set-up-git) 用截图覆盖了同样的步骤。

## 2. 检查

打开终端并运行：

```bash
git --version
```

你应该看到版本号。如果提示找不到命令，关掉终端、重新打开，再试一次。

## 3. 设置姓名和邮箱

Git 会把这些写进每一次提交。请使用与 GitHub 账号相同的邮箱。

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## 相关

- [克隆仓库](/docs/git/clone)
- [安装 GitHub CLI](/docs/github-cli/install)
