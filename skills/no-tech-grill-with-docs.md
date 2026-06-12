---
name: grill-with-docs
description: Schärft und stress-testet ein PRD durch gezielte Fragen — ausschließlich aus Nutzerperspektive und im Fachgebiet der User Persona. Liest zuerst die User Persona. Keine technischen Fragen. Claude hinterfragt Annahmen, Lücken und Edge Cases im Nutzerverhalten. Output: Liste offener Fragen die der Kunde beantworten soll, plus direkte PRD-Updates.
---

# grill-with-docs — PRD schärfen ohne Technik

## Schritt 0: User Persona laden (immer zuerst)

Lies `claude-vault/user-persona.md` bevor du irgendeine Frage stellst.

- Wenn die Datei **existiert**: Lade Fachgebiet, Kommunikationsstil und Antwortkapazität. Alle Fragen bleiben innerhalb des Fachgebiets dieser Person.
- Wenn die Datei **nicht existiert**: Stoppe und antworte:
  > "Bitte führe zuerst `/create-user-persona` aus, damit ich weiß welche Fragen ich dir stellen darf."

---

## Grundregeln

1. **Nur Fragen im Fachgebiet der Persona** — was laut `user-persona.md` nicht beantwortet werden kann, wird nicht gefragt
2. **Nutzerperspektive** — alle Fragen beziehen sich auf Nutzerverhalten, nicht auf Technik
3. **Eine Frage nach der anderen** — eine Frage stellen, Antwort abwarten, dann nächste Frage. Niemals mehrere Fragen auf einmal.
4. **So viele Fragen wie nötig** — kein künstliches Limit. Alle offenen Punkte müssen geklärt werden.
5. **PRD direkt aktualisieren** — Antworten sofort ins PRD integrieren
6. **Abbruch wenn scharf** — keine neuen offenen Fragen mehr = fertig

---

## Eskalations-Protokoll

Nur wenn eine Lücke im PRD entdeckt wird, die **nicht durch fachliche Fragen** geschlossen werden kann:

```
⚠️ HINWEIS: Hier gibt es eine offene Frage die technisches Know-how erfordert.
Bereich: [z.B. "Datenschutz bei sensiblen Gesundheitsdaten" / "Zahlungsabwicklung"]
Know-how das helfen würde: [spezifisch, z.B. "DSGVO-Berater" / "Payment-Spezialist"]

Ich empfehle Option A: Wir gehen mit einer Standardlösung weiter.
Option B: Du holst vorab Rat zu diesem Thema.

Was möchtest du?
```

---

## Fragekategorien (gefiltert durch Persona)

### Für alle Personas: Fehlende Szenarien
- "Was passiert, wenn jemand das zum ersten Mal benutzt — ohne Anleitung?"
- "Was macht ein Nutzer der einen Fehler macht? Kann er das rückgängig machen?"
- "Was passiert wenn jemand den Prozess mittendrin abbricht?"

### Für alle Personas: Annahmen prüfen
- "Du sagst Nutzer werden X tun — passiert das heute schon so, oder ist das eine Annahme?"
- "Hast du jemanden aus deiner Zielgruppe gefragt ob sie das so nutzen würden?"

### Für alle Personas: Abgrenzung schärfen
- "Was ist der einfachste Weg das falsch zu benutzen?"
- "Gibt es Nutzer die das für einen anderen Zweck nutzen könnten?"

### Zusatz für Gründerin
- "Was hat dein erster Testkunde gesagt als du ihm das erklärt hast?"
- "Was würde dein Wettbewerber an diesem PRD kritisieren?"

### Zusatz für Fachexperte
- "Gibt es Ausnahmen oder Sonderfälle in deinem Fachbereich die wir noch nicht abgedeckt haben?"
- "Was passiert wenn jemand eine ungewöhnliche Kombination von Eingaben macht?"
- "Welche Fehler machen Nutzer in deiner Branche am häufigsten?"

### Zusatz für Prozess-Optimiererin
- "Wer außer dir ist von diesem Prozess betroffen — und was brauchen die?"
- "Was passiert wenn die Person krank ist — funktioniert das Tool auch ohne sie?"
- "Was ändert sich am Prozess wenn es plötzlich 10x so viele Einträge gibt?"

### Zusatz für Kreativen
- "Wie soll sich das anfühlen wenn jemand es zum ersten Mal benutzt?"
- "Gibt es eine Seite oder ein Tool das sich so anfühlt wie du dir das vorstellst?"
- "Was darf auf keinen Fall billig oder unprofessionell wirken?"

---

## Prozess

### Start: PRD lesen, Persona berücksichtigen, wichtigste Frage stellen — dann warten
### Weiter: Antwort ins PRD einarbeiten, nächste Frage stellen — dann warten
### Wiederholen bis keine neuen Fragen mehr entstehen
### Abschluss:

```
✓ PRD ist scharf.
Offene Punkte: [keine / Liste]
Nächster Schritt: Mockup bauen
```
