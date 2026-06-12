# Agentic Engineering — No-Tech Edition

Dieser Ordner ist der Arbeitsbereich für dein Produkt. Claude liest ihn bei jeder Session automatisch.

Du brauchst hier nichts manuell ändern — Claude pflegt alle Dateien selbst.

---

## Einstieg

```
/no-tech
```

Das ist der einzige Befehl den du je eingeben musst. Claude übernimmt danach alles.

---

## Was hier passiert

```
[A] Profil laden oder erstellen (einmalig)
  ↓
[B] Idee verstehen → Problem + PRD pro Feature
  ↓
[C] Lücken prüfen → Schärfen durch Fragen
  ↓
[D] Mockup → klickbares HTML, Browser öffnet sich
  ↓
[E] Bauen → Baustein für Baustein, App startet automatisch
```

Für bestehende Produkte:
```
[F] Neue Funktion → Code lesen, dann bauen
[G] Bug-Fix → selbst analysieren, beheben, testen
```

---

## Ordnerstruktur (von Claude verwaltet)

```
claude-vault/
  user-persona.md        ← Dein Profil (einmalig angelegt)
  mockup.html            ← Klickbares Mockup (nach Phase 2)
  claude-data/
    index.md             ← Produktübersicht + alle Features
    features/
      [feature-name]/
        README.md        ← Was das Feature tut (für dich)
        tech.md          ← Technische Details (für Claude)
    _templates/          ← Vorlagen für neue Features
```

---

## Personas

Vier Archetypen — Claude erkennt automatisch welcher passt:

| Typ | Baut | Spricht über |
|---|---|---|
| [Gründerin](personas/die-gruenderin.md) | Erstes Produkt | Nutzer, Outcomes |
| [Fachexperte](personas/der-fachexperte.md) | Wissen als Tool | Prozesse, Fachlogik |
| [Prozess-Optimiererin](personas/die-prozess-optimiererin.md) | Interne Tools | Workflows, Zeit |
| [Kreativer](personas/der-kreative.md) | Branded Erlebnis | Gefühl, Ästhetik |

---

## Grundprinzip

**Du entscheidest:** Was gebaut wird, für wen, ob es sich richtig anfühlt.  
**Claude entscheidet:** Wie es gebaut wird — Technologie, Struktur, Code.

Du wirst nie nach Technik gefragt.
