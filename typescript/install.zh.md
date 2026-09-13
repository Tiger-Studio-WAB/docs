---
title: 安装 Node.js 与 TypeScript
description: 安装 Node.js，以便 npm、Next.js 和 TypeScript 能在网站仓库上工作。
order: 2
---

# 安装 Node.js 与 TypeScript

枢纽用 **Node.js** 安装软件包并运行 Next.js。TypeScript **内置**在网站仓库里（`devDependencies`）。先装 Node；然后 `npm install` 会拉取 TypeScript。

## 1. 安装 Node.js

从 [nodejs.org](https://nodejs.org/) 使用当前 **LTS**。Vercel 新项目的默认 Node 是 **24 LTS**；本机用较新的 LTS 做本地开发即可。

检查：

```bash
node -v
npm -v
```

两者都应打印出版本号。

## 2. 安装网站软件包

```bash
gh repo clone Tiger-Studio-WAB/Tiger-Studio-Website
cd Tiger-Studio-Website
npm install
```

这会从 `package.json` 安装 `typescript`、`next`、React 以及其他依赖。

## 3. 你很少自己跑 `tsc`

本地循环：

```bash
npm run dev
```

生产类型检查发生在 `npm run build` 期间（也就是 Vercel 跑的那一步）。如果编辑器显示类型错误，推送前先修好。

## 相关

- [网站上的 TypeScript](/docs/typescript/website)
- [在本地运行网站](/docs/website/local)
