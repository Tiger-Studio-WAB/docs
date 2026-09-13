---
title: Docs formatieren
description: Ordner- und Markdown-Regeln, damit jede Person einen Abschnitt hinzufügen kann, ohne den Website-Code anzufassen.
order: 90
sidebar_label: Docs formatieren
review_status: draft-for-mingli29
---

# Docs formatieren

<!-- Deutscher Entwurf zur Prüfung durch Mingli29 -->

Kopiere diese Datei ins öffentliche [`docs`](https://github.com/Tiger-Studio-WAB/docs)-Repository, falls sie dort noch fehlt. Die Website liest zuerst dieses Repo und füllt fehlende Seiten aus demselben Baum, der mit dem Hub ausgeliefert wird.

Das ist der einzige Schreibleitfaden, den du brauchst. Du bearbeitest keine Next.js-Dateien, um einen Abschnitt hinzuzufügen.

## 1. Einen Abschnitt hinzufügen (einen Ordner)

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

Lege den Ordner auf GitHub an, füge `index.md` hinzu und committe. Nach der nächsten Aktualisierung (etwa zwei Minuten) erscheint er in der Seitenleiste.

## 2. Dateien so benennen, dass URLs sauber bleiben

| Datei | URL |
| --- | --- |
| `README.md` im Stamm | `/docs` |
| `how-to-format.md` | `/docs/how-to-format` |
| `getting-started/index.md` | `/docs/getting-started` |
| `getting-started/join.md` | `/docs/getting-started/join` |
| `01-overview.md` | `/docs/overview` (das `01-` sortiert nur) |

Die englische Datei ist die Quelle. Übersetzungen liegen daneben: `join.md`, `join.zh.md`, `join.de.md`; im Stamm `README.md`, `README.zh.md`, `README.de.md`. Keine Locale-Suffixe an `_category.json`.

Kleinbuchstaben, Bindestriche, kurze Namen. Keine Leerzeichen.

## 3. Jede Seite mit einem Titel beginnen

```md
# Getting started
```

Optionales Front Matter steht über dieser Überschrift. Nutze es, wenn das Seitenleisten-Label von der Überschrift abweichen soll oder dir die Reihenfolge wichtig ist.

```md
---
title: Getting started
description: What Tiger Studio is and how to join.
order: 1
sidebar_label: Start here
---

# Getting started
```

`order` ist eine Zahl. Kleinere Zahlen erscheinen zuerst. Die Ordnerreihenfolge kann auch in `_category.json` stehen.

## 4. Optionale Abschnittsdatei

Lege das als `_category.json` in den Ordner:

```json
{
  "label": "Getting started",
  "order": 1
}
```

Wenn du sie weglässt, wird der Ordnername zum Label (`getting-started` → „Getting started“).

## 5. Schreiben wie andere Entwicklerdocs

Seiten kurz halten. Eine Aufgabe pro Seite.

- **Überblick / Index** — worum es geht, dann Links nach unten
- **Erste Schritte** — Schritte, die jemand zu Ende bringen kann
- **How-to** — eine Aufgabe
- **Referenz** — Fakten, keine Geschichte

Verwende:

- Überschriften (`##`, `###`) statt fetter Absätze
- Nummerierte Listen für Schritte
- Aufzählungen für Optionen
- Code-Zäune für Befehle, JSON und Markdown-Beispiele
- Tabellen für Zuordnungen (Datei → URL, Feld → Bedeutung)
- Links zu anderen Seiten mit Site-Pfaden: `[Join](/docs/getting-started/join)`

Relative Links funktionieren ebenfalls: `[Join](./join.md)`.

## 6. Was hier nicht hingehört

| Gehört in Docs | Gehört in Support |
| --- | --- |
| Wie ein Produkt funktioniert | „Ich kann mich nicht anmelden“ |
| Wie man eine Seite hinzufügt | „Diese Seite ist falsch / down“ |
| Club-Prozess zum Ausliefern | „Ich brauche einen Menschen“ |

Support ist ein eigener Site-Bereich: [/support](/support). Lege keinen `support`-Ordner unter docs an.

## 7. Checkliste für einen neuen Abschnitt

1. Einen Ordner in [`Tiger-Studio-WAB/docs`](https://github.com/Tiger-Studio-WAB/docs) anlegen
2. `index.md` mit einer `#`-Überschrift hinzufügen
3. Weitere `.md`-Seiten nach Bedarf
4. Optional: `_category.json` für Label und Reihenfolge
5. Nach dem Deploy `/docs` öffnen und die Seitenleiste prüfen

Das ist das gesamte Format.
