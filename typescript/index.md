---
title: TypeScript
description: Typed JavaScript used on the Tiger Studio website.
order: 1
---

# TypeScript

The public hub is a **Next.js** app written in **TypeScript** (`.ts` / `.tsx`). Godot games in this studio use GDScript, not TypeScript.

You need TypeScript only when you change [Tiger-Studio-Website](https://github.com/Tiger-Studio-WAB/Tiger-Studio-Website) (or another Node project). Adding Markdown to **this** `docs` repo does not require TypeScript — see [How to format docs](/docs/how-to-format).

## Pages in this section

1. [Install Node.js and TypeScript](/docs/typescript/install)
2. [TypeScript on the website](/docs/typescript/website)

## What “TypeScript” means here

| File | Role |
| --- | --- |
| `.ts` | Logic, helpers, config |
| `.tsx` | React pages and components |
| `tsconfig.json` | Compiler options for the repo |
| `package.json` | `typescript` as a dev dependency |

The website already includes TypeScript. You do not install a global `tsc` unless you want it. `npm install` in the website repo is enough.
