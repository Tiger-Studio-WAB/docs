---
title: TypeScript
description: Tiger Studio 网站使用的带类型 JavaScript。
order: 1
---

# TypeScript

公开枢纽是一个用 **TypeScript**（`.ts` / `.tsx`）写的 **Next.js** 应用。本工作室的 Godot 游戏用 GDScript，不用 TypeScript。

只有在改 [Tiger-Studio-Website](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website)（或其他 Node 项目）时才需要 TypeScript。往 **这个** `docs` 仓库加 Markdown 不需要 TypeScript — 见 [如何排版文档](/docs/how-to-format)。

## 本分区页面

1. [安装 Node.js 与 TypeScript](/docs/typescript/install)
2. [网站上的 TypeScript](/docs/typescript/website)

## 这里的 “TypeScript” 指什么

| 文件 | 作用 |
| --- | --- |
| `.ts` | 逻辑、辅助函数、配置 |
| `.tsx` | React 页面与组件 |
| `tsconfig.json` | 该仓库的编译器选项 |
| `package.json` | 把 `typescript` 作为开发依赖 |

网站已经包含 TypeScript。除非你想要，否则不必安装全局 `tsc`。在网站仓库里执行 `npm install` 就够了。
