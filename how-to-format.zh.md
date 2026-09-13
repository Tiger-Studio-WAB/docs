---
title: 如何排版文档
description: 文件夹与 Markdown 规则，任何人都能加分区而无需改网站代码。
order: 90
sidebar_label: 如何排版文档
---

# 如何排版文档

如果公开的 [`docs`](https://github.com/Tiger-Studio-WAB/docs) 仓库里还没有本文件，请把它复制进去。网站先读该仓库，再用枢纽自带的同一棵目录树补齐缺失页面。

这是你唯一需要的写作指南。加分区不必改 Next.js 文件。

## 1. 添加一个分区（文件夹）

```text
docs/
  getting-started/          ← section
    _category.json          ← optional
    index.md                ← landing page
    join.md                 ← another page
  git/
    index.md
    install.md
  products/
    index.md
    proj-help.md
```

在 GitHub 上创建文件夹，加入 `index.md` 并提交。下次刷新后（大约两分钟）它会出现在侧栏。

## 2. 给文件起名，让 URL 保持干净

| 文件 | URL |
| --- | --- |
| 根目录的 `README.md` | `/docs` |
| `how-to-format.md` | `/docs/how-to-format` |
| `getting-started/index.md` | `/docs/getting-started` |
| `getting-started/join.md` | `/docs/getting-started/join` |
| `01-overview.md` | `/docs/overview`（`01-` 只负责排序） |

英文原文是源文件。中文与德文译本放在旁边：`join.md`、`join.zh.md`、`join.de.md`；根目录则是 `README.md`、`README.zh.md`、`README.de.md`。不要给 `_category.json` 加语言后缀。

使用小写、连字符和短名称。不要空格。

## 3. 每页都以标题开头

```md
# Getting started
```

可选的 front matter 写在该标题上方。当侧栏标签应与标题不同，或你在意排序时再用。

```md
---
title: Getting started
description: What Tiger Studio is and how to join.
order: 1
sidebar_label: Start here
---

# Getting started
```

`order` 是数字。数字越小越靠前。文件夹顺序也可以在 `_category.json` 里设置。

## 4. 可选的分区文件

把下面内容放到文件夹中的 `_category.json`：

```json
{
  "label": "Getting started",
  "order": 1
}
```

如果省略，文件夹名会变成标签（`getting-started` → “Getting started”）。

## 5. 像其他开发者文档那样写

页面保持简短。一页一件事。

- **概述 / index** — 主题是什么，然后向下链接
- **入门** — 别人能做完的步骤
- **操作指南** — 一项任务
- **参考** — 事实，不是故事

请使用：

- 标题（`##`、`###`），不要用加粗段落冒充标题
- 步骤用编号列表
- 选项用项目符号
- 命令、JSON 和 Markdown 示例用围栏代码块
- 对照关系用表格（文件 → URL、字段 → 含义）
- 用站点路径链接其他页面：`[Join](/docs/getting-started/join)`

相对链接也可以：`[Join](./join.md)`。

## 6. 不要写在这里的内容

| 放进文档 | 放进支持 |
| --- | --- |
| 产品如何工作 | “我登不进去” |
| 如何加一页 | “这页错了 / 打不开” |
| 社团的发布流程 | “我需要真人帮忙” |

支持是单独的站点区域：[/support](/support)。不要在 docs 下加 `support` 文件夹。

## 7. 新分区检查清单

1. 在 [`Tiger-Studio-WAB/docs`](https://github.com/Tiger-Studio-WAB/docs) 创建文件夹
2. 添加带 `#` 标题的 `index.md`
3. 按需再加 `.md` 页面
4. 可选：用 `_category.json` 设标签和顺序
5. 部署后打开 `/docs`，检查侧栏

排版规则就是这些。
