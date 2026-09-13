---
title: 提交并推送
description: 先在本地保存快照，再发送到 GitHub。
order: 4
---

# 提交并推送

**提交（commit）** 是你电脑上的一份快照。**推送（push）** 把这些快照发到 GitHub，工作室其他人才能看到。

在 [分支](/docs/git/branch) 上工作，而不是 `main`，除非维护者让你改 `main`。

## 1. 查看改了什么

```bash
git status
git diff
```

`status` 列出文件。`diff` 显示具体改动。

## 2. 暂存并提交

```bash
git add .
git commit -m "Add clone steps to the Git handbook"
```

- `git add .` 暂存当前文件夹里的所有改动。只想提交部分文件时，优先用 `git add path/to/file.md`。
- 写简短的祈使语气主题：「Add…」「Fix…」「Document…」。

## 3. 推送分支

```bash
git push -u origin HEAD
```

新分支的第一次推送用 `-u`，之后就可以直接 `git push`，不必再加额外参数。

如果 GitHub 要求登录，用浏览器提示或 [GitHub CLI](/docs/github-cli/sign-in)。

## 4. 打开拉取请求

分支到了 GitHub 之后，打开一个 PR。最快路径：[GitHub CLI 拉取请求](/docs/github-cli/pull-requests)。

## 不要提交的内容

| 排除 | 原因 |
| --- | --- |
| `.env.local`、密钥、API keys | 它们能打开生产环境 |
| `node_modules/` | 用 `npm install` 重建 |
| `.godot/` | Godot 编辑器缓存 |
| 系统垃圾（`.DS_Store`） | 噪音 |

每个仓库的 `.gitignore` 已经覆盖了其中大部分。

## 相关

- [分支](/docs/git/branch)
- 如果你在改本手册，见 [如何排版文档](/docs/how-to-format)
