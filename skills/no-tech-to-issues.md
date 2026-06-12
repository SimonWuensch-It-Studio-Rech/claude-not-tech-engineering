---
name: to-issues
description: Zerlegt ein fertiges PRD in kleine, umsetzbare Bausteine — in der Sprache der User Persona, ohne Technik. Liest zuerst die User Persona. Jeder Baustein beschreibt ein Ergebnis das nach der Umsetzung sichtbar und prüfbar ist. Der Kunde versteht jeden Baustein und kann die Reihenfolge beurteilen.
---

# to-issues — PRD in Bausteine zerlegen

## Schritt 0: User Persona laden (immer zuerst)

Lies `claude-vault/user-persona.md` bevor du loslegst.

- Wenn die Datei **existiert**: Lade Fachgebiet, Kommunikationsstil und Archetype. Bausteine werden in der Sprache und mit den Beispielen des Fachgebiets formuliert.
- Wenn die Datei **nicht existiert**: Stoppe und antworte:
  > "Bitte führe zuerst `/create-user-persona` aus."

---

## Grundregeln

1. **Ergebnis-Sprache der Persona** — "Danach kann [Name/Rolle aus Persona] [Aktion tun]"
2. **Klein genug für eine Session** — ein Baustein, eine Umsetzungseinheit
3. **Sichtbar und prüfbar** — die Person kann nach jedem Baustein etwas erleben
4. **Reihenfolge nach Wert** — was bringt dem Nutzer am meisten, kommt zuerst
5. **Fachgebiet der Persona** — Bezeichnungen und Beispiele aus der Welt der Person

---

## Eskalations-Protokoll

Nur wenn ein Baustein eine technische Entscheidung erfordert die fundamentale Konsequenzen hat:

```
⚠️ HINWEIS: Dieser Baustein berührt einen Bereich der spezifisches Know-how erfordert.
Thema: [z.B. "Zahlungsabwicklung mit echtem Geld" / "Medizinische Daten und DSGVO"]
Know-how das helfen würde: [z.B. "Erfahrung mit Zahlungsanbietern" / "Datenschutzrecht"]

Ich empfehle: Baustein mit Standardlösung umsetzen, bei Bedarf später anpassen.
Oder: Vor Umsetzung dieses Bausteins Beratung einholen.

Was möchtest du?
```

---

## Baustein-Format

```
📦 BAUSTEIN [Nr.]: [Titel in der Sprache der Persona]

Was danach möglich ist:
[Nutzer aus Persona-Fachgebiet] kann [konkrete Aktion], [Nutzen/Ergebnis].

Was dazu gehört:
- [Sichtbares Element oder Funktion — in Alltagssprache]
- [Sichtbares Element]
- [Sichtbares Element]

Braucht vorher: [Baustein X] — oder: nichts, kann sofort starten

Wie du prüfen kannst ob es funktioniert:
[Konkrete Anweisung — was macht die Person, um zu testen?]
```

---

## Reihenfolge-Logik je Persona

**Gründerin**: Zuerst der Baustein, den sie einem echten Kunden zeigen kann. "Was kann ich nächste Woche vorführen?"

**Fachexperte**: Zuerst der Kern-Fachprozess. Erst wenn die Logik stimmt, kommt der Rest.

**Prozess-Optimiererin**: Zuerst der größte Zeitfresser. Was spart sofort die meiste Zeit?

**Kreativer**: Zuerst wie es aussieht. Das Erlebnis muss stimmen, bevor Funktionen dazukommen.

---

## Prozess

### Schritt 1: PRD lesen (Kunden-Zone + AI-Zone)
### Schritt 2: Bausteine entwerfen und vorschlagen

> "Ich schlage vor, wir starten mit Baustein 1, weil [Persona] danach schon [Ergebnis] kann.
> Macht die Reihenfolge für dich Sinn?"

### Schritt 3: Feedback einarbeiten, Reihenfolge anpassen
### Schritt 4: Übergabe

```
✓ [Anzahl] Bausteine definiert und bestätigt.

Reihenfolge:
1. [Baustein 1 Titel]
2. [Baustein 2 Titel]
...

Claude beginnt mit Baustein 1.
Nach jedem Baustein: kurze Überprüfung, dann weiter.
```
