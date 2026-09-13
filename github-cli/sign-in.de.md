---
title: Anmelden
description: gh authentifizieren, damit es als dein GitHub-Benutzer handeln kann.
order: 3
review_status: draft-for-mingli29
---

# Anmelden

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Die GitHub CLI braucht ein angemeldetes Konto, bevor sie private Repos klonen, PRs öffnen oder Issues anlegen kann.

## 1. Login starten

```bash
gh auth login
```

## 2. Die Fragen beantworten

1. **GitHub.com**
2. **HTTPS** (am einfachsten auf Schulrechnern)
3. Mit **Login with a web browser** authentifizieren
4. Den Einmalcode kopieren, Enter drücken und im Browser genehmigen

SSH ist in Ordnung, wenn du bereits SSH-Schlüssel nutzt. HTTPS + Browser ist der Weg ohne extra Schlüssel-Setup.

## 3. Bestätigen

```bash
gh auth status
```

Du solltest deinen GitHub-Benutzernamen und `Logged in to github.com` sehen.

## Wenn der Login scheitert

- Den Browser-Schritt zu Ende führen; den Tab nicht früh schließen
- Schulrechner blockieren die Weiterleitung manchmal — anderen Browser oder ein privates Gerät versuchen
- Kontoprobleme sind [Support](/support), kein Docs-Bug

## Verwandt

- [Pull Requests](/docs/github-cli/pull-requests)
- [Ein Repository klonen](/docs/git/clone)
