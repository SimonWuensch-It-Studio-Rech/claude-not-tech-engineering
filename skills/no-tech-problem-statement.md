---
name: problem-statement
description: Erstellt ein strukturiertes Problem Statement aus einer kurzen Idee oder Beobachtung. Liest zuerst die User Persona — wenn vorhanden, werden alle Fragen auf das Fachgebiet der Person zugeschnitten. Stellt so viele Rückfragen wie nötig. Output folgt exakt dem Template. Sprache: Deutsch, klar, testbar.
---

# problem-statement — Idee in ein scharfes Problem verwandeln

## Schritt 0: User Persona laden (immer zuerst)

Lies `claude-vault/user-persona.md` bevor du Fragen stellst.

- Wenn die Datei **existiert**: Lade Fachgebiet und Kommunikationsstil. Alle Rückfragen bleiben im Fachgebiet der Person.
- Wenn die Datei **nicht existiert**: Fortfahren ohne Persona, aber am Ende empfehlen:
  > "Tipp: Mit `/create-user-persona` kann ich alle weiteren Schritte noch besser auf dich zuschneiden."

---

## Grundregeln

1. **Nur fachliche Rückfragen** — niemals nach Technik fragen
2. **Konkrete Rollen aus dem Fachgebiet der Persona** — keine vagen "User"
3. **Messbare Erfolgskriterien** — in Zahlen, Zeit, Häufigkeit, Qualität
4. **Annahmen klar markieren** — was nicht bestätigt ist, wird als Annahme gekennzeichnet
5. **Eine Frage nach der anderen** — eine Frage stellen, Antwort abwarten, nächste Frage. Niemals mehrere Fragen auf einmal. So viele Fragen wie nötig.

---

## Eskalations-Protokoll

Nur wenn das Problem Statement einen Bereich berührt der externes Know-how erfordert:

```
⚠️ HINWEIS: Dieses Problem berührt einen Bereich der spezifisches Know-how erfordert.
Bereich: [z.B. "Regulierung im Gesundheitsbereich" / "Steuerrechtliche Anforderungen"]
Know-how das helfen würde: [spezifisch]

Das Problem Statement kann trotzdem vollständig erstellt werden.
Dieser Hinweis dient nur als Merkposten für später.
```

---

## Rückfragen (eine nach der anderen, gefiltert durch Persona)

Immer in der Sprache und im Fachgebiet der Person:

1. "Wer genau hat dieses Problem — beschreib eine konkrete Person aus deiner Welt."
2. "Was passiert heute stattdessen? Wie lösen sie das gerade?"
3. "Woran würdest du in 3 Monaten erkennen, dass das besser ist?"
4. "Was ist der größte Schaden durch das Problem — Zeit, Geld, Frust, verpasste Chancen?"
5. "Gibt es Unterlagen, Notizen oder Beispiele die du teilen kannst?"

---

## Output Template

```markdown
## Stakeholder

| Rolle | Person / Team |
|---|---|
| Driver | [Wer verantwortet die Exploration] |
| Contributors | [Wer liefert Input aus dem Fachgebiet] |
| Informed | [Wer braucht Updates] |

## Strategic Alignment

[Wie passt dieses Problem zur Gesamtstrategie — in der Sprache der Persona]

## Problem Definition

**Wir haben das Problem, dass** [konkrete Zielgruppe aus dem Fachgebiet der Persona]
derzeit nicht in der Lage sind, [gewünschte Handlung] effizient durchzuführen,
**weil** [Hindernis].

**Das führt dazu, dass** [Impact — in der Sprache des Fachgebiets].

**Wir wissen, dass das Problem gelöst ist, wenn** [messbares Ergebnis].

### Wie lösen sie das Problem heute?

[2-5 Workarounds aus dem Fachgebiet der Persona — konkret und erkennbar]

## Validation

### Wie haben wir das validiert?

[Belege oder: "Noch nicht validiert" + was als nächstes geprüft werden sollte]

### Annahmen

1. Wenn ..., dann ...
2. Wenn ..., dann ...
3. Wenn ..., dann ...

### Offene Fragen

1. ...?
2. ...?
3. ...?

## Ressourcen

[Liste oder: "Keine Ressourcen — bitte ergänze wenn verfügbar"]
```
