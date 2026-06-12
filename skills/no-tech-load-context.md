---
name: no-tech-load-context
description: Lädt beim Session-Start den vollständigen Projektkontext aus claude-data/. Liest index.md und alle aktiven Features. Prüft Sync-Status. Wird vom no-tech Orchestrator automatisch ausgeführt — nie direkt aufrufen.
---

# no-tech-load-context — Projektkontext laden

Wird vom no-tech Orchestrator beim Start jeder Session ausgeführt.
Gibt einen strukturierten Überblick über den Projektstand zurück.

---

## Schritt 1: index.md lesen

Lies `claude-vault/claude-data/index.md`.

**Wenn die Datei nicht existiert:**
→ Neues Projekt. Erstelle `claude-vault/claude-data/index.md` — verwende den Inhalt aus `claude-vault/claude-data/_templates/index.md` als Vorlage, ersetze alle Platzhalter mit dem aktuellen Datum und "In Planung" als Status.
→ Weiter mit Schritt 2.

**Wenn die Datei existiert:**
Extrahiere:
- Projektname + Status
- Features: Name, Status, Version, Sync-Status
- Offene Punkte

---

## Schritt 2: Produktvision aus index.md lesen

Die Produktvision steht direkt in `index.md` — kein separates prd.md.

Extrahiere aus dem Abschnitt "Produkt-Übersicht":
- Was (Ziel)
- Für wen (Zielgruppe)
- Erfolg (Messkriterium)
- Nicht dabei (Abgrenzung)
- Tech-Stack global + Start-Befehl

Diese Information braucht Claude um Fragen im richtigen Fachkontext zu stellen und Features korrekt zu bauen.

---

## Schritt 3: Sync-Check für alle Features

Für jedes Feature das in index.md aufgeführt ist:

1. Lies `claude-vault/claude-data/features/[name]/README.md` → lese Frontmatter-Feld `sync-version`
2. Lies `claude-vault/claude-data/features/[name]/tech.md` → lese Frontmatter-Feld `sync-version`
3. Vergleiche beide Werte

**Wenn sync-version unterschiedlich:**
> "⚠️ Feature [Name] ist nicht synchron (README: v[X], tech: v[Y]). Ich gleiche das ab bevor wir weitermachen."

Angleichen:
1. Inhaltlich prüfen welche Datei aktueller ist
2. Andere Datei auf denselben Stand bringen
3. sync-version in BEIDEN auf den höheren Wert setzen
4. zuletzt-geaendert in BEIDEN auf heute setzen
5. index.md aktualisieren (Sync: OK)

---

## Schritt 4: Kontext-Summary erstellen (intern — Person sieht das nicht)

```
PROJEKT: [Name] | STATUS: [In Planung / In Entwicklung / Fertig]
FEATURES: [N gesamt] | Fertig: [N] | In Arbeit: [N] | Geplant: [N] | Problem: [N]
SYNC: [alle OK] oder [Problem bei: Feature X — bereits behoben]
NÄCHSTER SCHRITT: [was logisch folgt]
```

Der Orchestrator entscheidet basierend auf dieser Summary:
- Kein index.md → Neues Projekt, starte bei Phase 1
- index.md vorhanden, keine Features → Starte bei Phase 2 oder 3
- Features vorhanden, einige in Arbeit → Setze bei Phase 3 fort
