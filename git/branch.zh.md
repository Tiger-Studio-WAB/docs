---
title: 分支
description: 在拉取请求合并之前，在功能分支上工作，不改 main。
order: 5
---

# 分支

`main` 是工作室仓库的默认分支。新工作放在命名分支上，再由拉取请求合并进去。

## 创建分支

从最新的 `main` 出发：

```bash
git checkout main
git pull origin main
git checkout -b docs/git-handbook
```

用能说明改动的短名称：`docs/…`、`fix/…`、`feature/…`。WAB-Project-1 上的 Godot 协作者使用 `feature/<short-description>` 和 `fix/<short-description>` — 见该仓库的 `CONTRIBUTING.md`。

## 切换与更新

```bash
git checkout docs/git-handbook
git pull origin main
```

如果 `main` 已经前进，开 PR 前先把 `main` 拉进你的分支，这样评审不会跟旧代码打架。

## 典型流程

1. 从 `main` 拉出分支
2. [提交并推送](/docs/git/commit)
3. [打开拉取请求](/docs/github-cli/pull-requests)
4. 合并后切回去：`git checkout main && git pull`

## 相关

- [GitHub CLI](/docs/github-cli)
- [提交并推送](/docs/git/commit)
