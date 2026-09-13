---
title: 拉取请求
description: 在终端里打开并查看拉取请求。
order: 4
---

# 拉取请求

拉取请求（PR）请求把你的 [分支](/docs/git/branch) 合并进 `main`。评审在 GitHub 上进行；`gh` 负责创建和查看 PR。

## 打开之前

1. [提交并推送](/docs/git/commit) 该分支
2. 留在仓库文件夹里
3. 已经 [登录](/docs/github-cli/sign-in)

## 创建

```bash
gh pr create --fill
```

`--fill` 用你的提交说明作为标题和正文。要自己写：

```bash
gh pr create --title "Add Git how-to pages" --body "Handbook section for Git, clone, commit, and branches."
```

除非你传入 `--base`，否则目标分支是 `main`。

## 查看

```bash
gh pr status
gh pr view
gh pr diff
```

`gh pr view --web` 在浏览器中打开该 PR。

## 检出别人的 PR

```bash
gh pr checkout 12
```

把 `12` 换成 PR 编号。

## 相关

- [议题](/docs/github-cli/issues)
- 如果 PR 针对枢纽，见 [管理网站](/docs/website)
