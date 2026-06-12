---
name: prototype
description: Validiert Annahmen aus einem PRD durch einen geschriebenen Nutzer-Walkthrough — kein Code, keine Technik. Liest zuerst die User Persona. Claude beschreibt Schritt für Schritt was ein Nutzer erlebt, in der Sprache und mit den Beispielen die zur Persona passen. Output: Szenarien die der Kunde lesen und bestätigen kann.
---

# prototype — Annahmen prüfen ohne Code

## Schritt 0: User Persona laden (immer zuerst)

Lies `claude-vault/user-persona.md` bevor du loslegst.

- Wenn die Datei **existiert**: Lade Fachgebiet, Kommunikationsstil und Beispiele. Nutze den Namen, die Branche und die Sprache der Persona für alle Szenarien.
- Wenn die Datei **nicht existiert**: Stoppe und antworte:
  > "Bitte führe zuerst `/create-user-persona` aus."

---

## Grundregeln

1. **Kein Code** — reines Deutsch, keine Programmierung
2. **Persona-spezifische Szenarien** — benutze konkrete Namen und Kontexte aus dem Fachgebiet der Person
3. **Was der Nutzer sieht und tut** — nie was das System intern macht
4. **Lücken sichtbar machen** — offene Fragen immer markieren
5. **Bestätigung vor dem nächsten Szenario** — erst bestätigen lassen, dann weitermachen

---

## Eskalations-Protokoll

Nur wenn beim Durchdenken eines Szenarios eine technische Entscheidung auftaucht die fundamentale Auswirkungen hat:

```
⚠️ HINWEIS: Dieses Szenario berührt einen Bereich der spezifisches Know-how erfordert.
Thema: [z.B. "Echtzeit-Updates zwischen mehreren Nutzern gleichzeitig"]
Warum relevant: [kurze Erklärung ohne Technik]
Know-how das helfen würde: [z.B. "Erfahrung mit kollaborativen Tools"]

Standard-Entscheidung: [was Claude wählen würde]
Möchtest du damit weitermachen?
```

---

## Szenario-Typen (je nach Persona)

### Für Gründerin: Erster-Nutzer-Szenario
Zeige wie ein völlig fremder Mensch das Produkt zum ersten Mal findet und nutzt — ohne Erklärung, ohne Hilfe.

### Für Fachexperte: Fachprozess-Szenario
Zeige wie das Tool einen konkreten Fall aus dem Fachgebiet durcharbeitet — mit realistischen Eingaben und dem erwarteten Ergebnis.

### Für Prozess-Optimiererin: Vor/Nach-Szenario
Zeige erst wie der Prozess heute läuft (manuell, umständlich), dann wie er mit dem Tool läuft. Zeitersparnis sichtbar machen.

### Für Kreativen: Erlebnis-Szenario
Beschreibe nicht nur was passiert, sondern wie es sich anfühlt. Was sieht die Person, was fühlt sie, was denkt sie?

---

## Walkthrough-Format

```
🚶 SZENARIO: [Titel — konkret und aus Nutzerperspektive]
Person: [Konkreter Name aus dem Fachgebiet der Persona — z.B. "Maria, 38, Steuerberaterin"]
Situation: [Wo ist sie? Was will sie gerade tun? Kontext aus dem Fachgebiet]

---

Schritt 1: [Name] [Aktion].
           Sie sieht: [Beschreibung in einfachen Worten — was ist auf dem Bildschirm?]

Schritt 2: Sie [Aktion — klickt, tippt, wählt, liest...].
           Daraufhin: [Was passiert? Was sieht sie?]

[Fortsetzung bis Ziel erreicht]

Ergebnis: [Name] hat [Ziel erreicht]. Sie [Reaktion / nächste Aktion].

---

❓ OFFENE FRAGEN aus diesem Szenario:
1. [Frage im Fachgebiet der Persona]
2. [Frage]
```

---

## Abschluss

```
✓ Szenarien bestätigt.
Erkenntnisse: [Was ändert sich am PRD?]
Nächster Schritt: PRD aktualisieren → Mockup bauen
```
