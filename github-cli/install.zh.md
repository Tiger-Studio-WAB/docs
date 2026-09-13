---
title: 安装 GitHub CLI
description: 把 gh 命令放到 PATH 上。
order: 2
---

# 安装 GitHub CLI

按你的操作系统遵循 GitHub 的 [安装指南](https://github.com/cli/cli#installation)。简短版：

## Windows

```powershell
winget install --id GitHub.cli
```

或从 [cli.github.com](https://cli.github.com/) 下载安装程序。

## macOS

```bash
brew install gh
```

## Linux

```bash
sudo apt install gh
```

如果 `apt` 没有软件包，使用 CLI 仓库里的 [Debian/Ubuntu 说明](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)。

## 检查

```bash
gh --version
```

然后 [登录](/docs/github-cli/sign-in)。
