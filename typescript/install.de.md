---
title: Node.js und TypeScript installieren
description: Node.js installieren, damit npm, Next.js und TypeScript im Website-Repo funktionieren.
order: 2
review_status: draft-for-mingli29
---

# Node.js und TypeScript installieren

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Der Hub nutzt **Node.js**, um Pakete zu installieren und Next.js auszuführen. TypeScript liegt **im** Website-Repo (`devDependencies`). Installiere Node; danach holt `npm install` TypeScript.

## 1. Node.js installieren

Nutze das aktuelle **LTS** von [nodejs.org](https://nodejs.org/). Vercels Standard-Node für neue Projekte ist **24 LTS**; ein aktuelles LTS auf deinem Rechner reicht für lokale Arbeit.

Prüfen:

```bash
node -v
npm -v
```

Beide sollen Versionen ausgeben.

## 2. Die Website-Pakete installieren

```bash
gh repo clone Tiger-Studio-WAB/Tiger-Studio-Website
cd Tiger-Studio-Website
npm install
```

Das installiert `typescript`, `next`, React und den Rest aus `package.json`.

## 3. Du führst `tsc` selten selbst aus

Lokale Schleife:

```bash
npm run dev
```

Der Produktions-Typecheck passiert während `npm run build` (was Vercel ausführt). Wenn der Editor Typfehler zeigt, behebe sie, bevor du pushst.

## Verwandt

- [TypeScript auf der Website](/docs/typescript/website)
- [Die Website lokal ausführen](/docs/website/local)
