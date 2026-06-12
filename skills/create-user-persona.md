---
name: create-user-persona
description: Erstellt einmalig eine persönliche Persona-Datei für die Person die das Projekt umsetzt. Diese Datei wird von allen anderen Skills automatisch gelesen. Claude weiß danach genau: wer ist diese Person, was kann sie beantworten, wie kommuniziert sie, was ist ihr Fachgebiet. Nur einmal pro Projekt ausführen.
---

# create-user-persona — Dein persönliches Profil erstellen

## Zweck

Bevor wir anfangen zu bauen, lerne ich dich kennen. Nicht technisch — sondern als Mensch mit einem Fachgebiet, einer Idee und einer bestimmten Art zu denken. Diese Informationen speichere ich einmalig in einer Datei. Alle weiteren Schritte (PRD schreiben, Ideen schärfen, Bausteine planen) passe ich dann automatisch auf dich an — du bekommst immer nur die Fragen, die du auch wirklich beantworten kannst.

## Prozess

### Schritt 1: Interview (eine Frage nach der anderen)

Stelle die folgenden Fragen **einzeln** — immer eine warten, dann die nächste. Nicht alle auf einmal.

**Pflichtfragen (immer stellen):**

1. "Wie heißt du, und was machst du beruflich oder womit beschäftigst du dich hauptsächlich?"

2. "Was möchtest du bauen oder umsetzen? Beschreib es so, wie du es einem Freund erklären würdest — ganz ohne Fachbegriffe."

3. "Für wen soll das sein? Beschreib die Person, die das später nutzen wird."

4. "Was passiert heute, wenn diese Person das Problem hat? Wie löst sie das gerade — oder löst sie es gar nicht?"

5. "Woran würdest du in 3 Monaten erkennen, dass das funktioniert hat?"

**Optionale Folgefragen (nur wenn Antworten unklar sind):**

6. "In welchem Bereich kennst du dich besonders gut aus — wo würdest du sagen bist du Experte?"

7. "Gibt es etwas, das du bei diesem Vorhaben auf keinen Fall willst — ein klares Nein?"

### Schritt 2: Archetype bestimmen

Ordne die Person einem der vier Archetypen zu (intern, nicht laut aussprechen):

- **Gründerin**: Baut erstes eigenes Produkt, kennt Zielgruppe gut, will schnell starten
- **Fachexperte**: Hat tiefes Domänenwissen, will es digitalisieren/skalieren
- **Prozess-Optimiererin**: Will wiederkehrende manuelle Arbeit automatisieren
- **Kreativer**: Denkt in Ästhetik und Erlebnis, baut rund um kreative Arbeit

Wenn keiner passt: beschreibe den Archetyp in eigenen Worten.

### Schritt 3: Persona-Datei erstellen

Erstelle die Datei `claude-vault/user-persona.md` mit folgendem Inhalt:

```markdown
# User Persona: [Vorname oder Rolle]

> "[Satz aus dem Interview der zeigt wie diese Person denkt]"

---

## Wer ich bin

**Name / Rolle:** [Name oder "anonym"] — [Beruf/Tätigkeit]
**Fachgebiet:** [Domäne — z.B. "Steuerberatung für Selbstständige", "Hochzeitsfotografie", "HR in Mittelstand"]
**Archetype:** [Gründerin / Fachexperte / Prozess-Optimiererin / Kreativer]

---

## Was ich bauen möchte

[2-3 Sätze in den eigenen Worten der Person — aus dem Interview übernommen]

**Für wen:** [Beschreibung der Zielnutzer]
**Warum jetzt:** [Motivation / Auslöser]

---

## Was ich fachlich beurteilen kann

Claude darf mich zu diesen Themen befragen — ich kenne mich aus:

- [Domäne 1: z.B. "Steuerrechtliche Anforderungen und Fristen"]
- [Domäne 2: z.B. "Meine Kunden und ihre typischen Fragen"]
- [Domäne 3: z.B. "Was in meinem Arbeitsalltag nervt und Zeit kostet"]
- [Domäne 4: z.B. "Was ein gutes Ergebnis für meine Kunden aussieht"]

---

## Was ich NICHT beantworten kann

Claude entscheidet diese Dinge selbst — ich frage nicht danach:

- Technologie, Programmiersprachen, Frameworks
- Datenbankstruktur oder Datenspeicherung
- Server, Hosting, Deployment
- Sicherheit, Performance, Skalierung
- Code-Qualität oder Architektur

---

## Wie ich kommuniziere

**Stil:** [formal / informell / direkt / ausführlich]
**Ich beschreibe Dinge in:** [Beispielen / Schritt-für-Schritt / Bildern / Zahlen / Geschichten]
**Typische Formulierungen:** ["[Zitat aus Interview]", "[weiteres Zitat]"]

---

## Meine Antwortkapazität

| Thema | Kann ich beurteilen? |
|---|---|
| Fachliche Inhalte meiner Branche | Ja |
| Nutzerbedürfnisse meiner Zielgruppe | Ja |
| Was Erfolg für mein Vorhaben bedeutet | Ja |
| Prioritäten und Reihenfolge von Funktionen | Ja |
| Ob etwas sich richtig anfühlt | Ja |
| Technische Umsetzung | Nein — Claude entscheidet |
| Datenbankdesign | Nein — Claude entscheidet |
| Code-Architektur | Nein — Claude entscheidet |
| Hosting und Deployment | Nein — Claude entscheidet |

---

## Eskalationsprofil

**Wann externer Tech-Rat sinnvoll sein könnte:**
[Nur ausfüllen wenn aus dem Interview erkennbar: z.B. "Regulatorische Anforderungen im Gesundheitsbereich erfordern ggf. DSGVO-Expertise", "Sehr hohe Nutzerzahlen erfordern ggf. Skalierungsberatung"]

**Standard:** Claude trifft alle technischen Entscheidungen nach Best Practices. Externer Rat wird nur signalisiert wenn eine Entscheidung fundamentale Auswirkungen hat die Claude nicht alleine tragen kann.

---

## Einstellungen

**mockup-oeffnen:** fragen
*(Optionen: `automatisch` — Browser öffnet immer ohne Nachfrage / `fragen` — Claude fragt vorher)*

*Zum Ändern einfach sagen: "Öffne Mockups immer automatisch" oder "Frag mich immer bevor du etwas öffnest"*
```

### Schritt 4: Bestätigung

Zeige der Person eine kurze Zusammenfassung:

> "Ich habe dein Profil angelegt. Hier ist eine Kurzversion:
>
> Du bist [Beschreibung in 1 Satz]. Du baust [Was] für [Wen].
> Ich werde dich nur nach [Fachgebiet]-Fragen fragen — alles Technische entscheide ich selbst.
>
> Stimmt das so?"

Wenn ja: Prozess kann beginnen.

---

## Hinweis für alle nachfolgenden Skills

Jeder Skill der nach `/create-user-persona` ausgeführt wird, liest zuerst `claude-vault/user-persona.md`.
Wenn die Datei nicht existiert, weist Claude darauf hin: "Bitte führe zuerst `/create-user-persona` aus."
