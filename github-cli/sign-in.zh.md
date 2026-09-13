---
title: 登录
description: 验证 gh，让它以你的 GitHub 用户身份操作。
order: 3
---

# 登录

GitHub CLI 需要已登录的账号，才能克隆私有仓库、打开 PR 或提交议题。

## 1. 开始登录

```bash
gh auth login
```

## 2. 回答提示

1. **GitHub.com**
2. **HTTPS**（学校电脑上最简单）
3. 用 **Login with a web browser** 验证
4. 复制一次性代码，按 Enter，并在浏览器里批准

如果你已经在用 SSH 密钥，SSH 也可以。HTTPS + 浏览器这条路不需要额外配密钥。

## 3. 确认

```bash
gh auth status
```

你应该看到自己的 GitHub 用户名以及 `Logged in to github.com`。

## 如果登录失败

- 完成浏览器步骤；不要过早关标签页
- 学校电脑有时会拦截重定向 — 换一个浏览器或用个人设备
- 账号问题属于 [支持](/support)，不是文档缺陷

## 相关

- [拉取请求](/docs/github-cli/pull-requests)
- [克隆仓库](/docs/git/clone)
