---
name: to-prd
description: Erstellt ein PRD aus einem Problem Statement oder einer Idee — ohne technische Rückfragen. Liest zuerst die User Persona. Der Kunde beschreibt nur was er will und für wen. Claude entscheidet alles Technische nach Best Practices. Output hat zwei klar getrennte Zonen: Kunden-Zone (fachlich) und AI-Zone (technisch, nicht für Kunden).
---

# to-prd — Produktanforderungen ohne Technik

## Schritt 0: User Persona laden (immer zuerst)

Lies `claude-vault/user-persona.md` bevor du irgendetwas tust.

- Wenn die Datei **existiert**: Lade Fachgebiet, Kommunikationsstil, Antwortkapazität und Archetype. Alle Fragen und die gesamte Kommunikation richtet sich ab jetzt nach dieser Persona.
- Wenn die Datei **nicht existiert**: Stoppe und antworte:
  > "Bevor wir das PRD erstellen, sollten wir kurz dein Profil anlegen — das dauert 5 Minuten und sorgt dafür, dass ich dir nur die richtigen Fragen stelle. Starte dafür `/create-user-persona`."

---

## Grundregeln (niemals brechen)

1. **Keine technischen Fragen an den Kunden** — nie. Nicht nach Datenbanken, APIs, Frameworks, Architektur, Testing, Deployment fragen.
2. **Persona-Profil beachten** — Fragen immer im Fachgebiet der Person halten. Was laut `user-persona.md` unter "Kann ich beurteilen: Nein" steht, wird niemals gefragt.
3. **Einfachster Weg zuerst** — AI-Zone: immer die technisch einfachste, bewährteste Lösung. Kein Over-Engineering. Orientierung an etablierten Best Practices (Convention over Configuration, YAGNI, KISS).
4. **Langfristige Wartbarkeit** — Entscheidungen so treffen, dass das Produkt in 2 Jahren ohne Entwickler weiterentwickelt werden kann.
5. **Zwei Zonen, sauber getrennt** — Kunden-Zone liest die Person. AI-Zone liest nur Claude.

---

## Eskalations-Protokoll

Nur im äußersten Notfall — wenn eine Entscheidung fundamentale Konsequenzen hat, die Claude nicht alleine tragen kann:

```
⚠️ HINWEIS: Diese Entscheidung geht über Standardfälle hinaus.
Hier wäre Know-how einer Person mit [spezifisches Wissen, z.B. "DSGVO-Expertise" /
"Zahlungsanbieter-Erfahrung" / "Skalierungs-Architektur"] hilfreich.

Optionen:
A) Claude trifft die Standardentscheidung (empfohlen für den Anfang)
B) Du holst Rat von jemandem mit [Wissen X] bevor wir weitermachen

Was möchtest du tun?
```

Dieser Hinweis erscheint **maximal einmal pro PRD-Erstellung** und nur wenn wirklich unvermeidbar.

---

## Prozess

### Schritt 1: Input + Persona verstehen

- Persona aus `user-persona.md` geladen? ✓
- Ist ein Problem Statement vorhanden? → direkt zu Schritt 3
- Wenn nicht: Fragen stellen (Schritt 2)

### Schritt 2: Fachliche Rückfragen (eine nach der anderen, gefiltert durch Persona)

**Dialogprinzip:** Eine Frage stellen — Antwort abwarten — nächste Frage. Niemals mehrere Fragen auf einmal. So viele Fragen wie nötig, bis alles klar ist.

Erlaubte Fragen — immer in der Sprache und im Fachgebiet der Persona:

| Frage | Für wen geeignet |
|---|---|
| "Wer genau soll das nutzen? Beschreib eine typische Person aus deiner Welt." | Alle |
| "Was soll jemand damit tun können? Beschreib den wichtigsten Moment." | Alle |
| "Was passiert heute stattdessen?" | Alle |
| "Woran merkst du, dass das funktioniert hat?" | Alle |
| "Gibt es in deinem Fachbereich Regeln oder Ausnahmen die wir beachten müssen?" | Fachexperte |
| "Wie soll das aussehen und sich anfühlen?" | Kreativer |
| "Welche Schritte hat der Prozess heute — und welcher nervt am meisten?" | Prozess-Optimiererin |
| "Was hat dein erster Kunde gesagt, der das braucht?" | Gründerin |

**Niemals fragen:**
- Alles was in `user-persona.md` unter "Kann ich beurteilen: Nein" steht
- Technologien, Frameworks, Datenbankstruktur, Architektur, Testing, Deployment

### Schritt 3: PRD erstellen

---

## PRD Template

```markdown
# PRD: [Produktname / Arbeitstitel]
*Erstellt für: [Vorname / Rolle aus user-persona.md]*

---

## KUNDEN-ZONE
*Dieser Teil ist für dich. Hier steht, was wir gemeinsam erarbeitet haben.*

### Was ist das Ziel?
[1-2 Sätze: Was soll dieses Produkt für den Nutzer tun? In Alltagssprache.]

### Wer nutzt es?
[Kurze Beschreibung der Hauptnutzer — echte Menschen, keine technischen Rollen]

### Was kann man damit tun?
[Nummerierte Liste aus Nutzerperspektive — in der Sprache der Persona]

1. Als [Nutzertyp] kann ich [Aktion], damit [Ziel/Nutzen].
2. Als [Nutzertyp] kann ich [Aktion], damit [Ziel/Nutzen].
3. ...

### Was ist NICHT dabei?
[Bewusste Abgrenzung — schützt vor Scope Creep]

- Nicht dabei: ...
- Nicht dabei: ...

### Wie sieht Erfolg aus?
[Messbar, in der Sprache des Fachgebiets der Persona]

- [Konkrete, beobachtbare Aussage]
- ...

---

## AI-ZONE 🤖
*Dieser Bereich ist ausschließlich für Claude — nicht für den Kunden.*
*Er enthält technische Entscheidungen die nach Best Practices getroffen wurden.*
*Der Kunde muss diesen Teil weder lesen noch verstehen.*

### Technologie-Stack
[Gewählte Technologien + Begründung: einfachste bewährte Lösung, wartbar, community-supported]

### Datenmodell
[Einfachstmögliche Struktur — keine Überabstraktion]

### Authentifizierung
[Standardlösung — z.B. Supabase Auth, Clerk, NextAuth]

### Start-Befehl (lokal)
[Befehl zum Starten der App während der Entwicklung — z.B. `npm run dev`, `python app.py`]

### Hosting & Deployment
[Einfachste Option mit automatischem Deployment — z.B. Vercel, Railway, Render]

### Architektur-Entscheidungen
[Wichtige Entscheidungen mit Begründung — nach KISS, YAGNI, Convention over Configuration]

### Bekannte Risiken
[Was könnte beim Bauen zu einer Eskalation führen — intern für Claude]

### Offene technische Fragen
[Was beim Bauen noch intern geklärt werden muss]
```

---

## Qualitätsprüfung vor Ausgabe

- [ ] Persona aus `user-persona.md` korrekt angewendet
- [ ] Kein technisches Wort in der Kunden-Zone
- [ ] Alle Fragen waren im Fachgebiet der Persona
- [ ] AI-Zone vollständig ausgefüllt mit konkreten Entscheidungen
- [ ] Einfachste technische Lösung gewählt
- [ ] Eskalations-Protokoll wurde höchstens einmal ausgelöst (oder gar nicht)
