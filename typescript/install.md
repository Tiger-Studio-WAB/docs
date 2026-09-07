---
title: Install Node.js and TypeScript
description: Install Node.js so npm, Next.js, and TypeScript work on the website repo.
order: 2
---

# Install Node.js and TypeScript

The hub uses **Node.js** to install packages and run Next.js. TypeScript ships **inside** the website repo (`devDependencies`). Install Node; then `npm install` pulls TypeScript.

## 1. Install Node.js

Use current **LTS** from [nodejs.org](https://nodejs.org/). Vercel’s default Node for new projects is **24 LTS**; a recent LTS on your machine is fine for local work.

Check:

```bash
node -v
npm -v
```

Both should print versions.

## 2. Install the website packages

```bash
gh repo clone Tiger-Studio-WAB/Tiger-Studio-Website
cd Tiger-Studio-Website
npm install
```

That installs `typescript`, `next`, React, and the rest from `package.json`.

## 3. You rarely run `tsc` yourself

Local loop:

```bash
npm run dev
```

Production typecheck happens during `npm run build` (what Vercel runs). If the editor shows type errors, fix them before you push.

## Related

- [TypeScript on the website](/docs/typescript/website)
- [Run the website locally](/docs/website/local)
