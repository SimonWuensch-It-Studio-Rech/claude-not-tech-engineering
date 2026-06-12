# Projekt-Index

> Einstiegspunkt für Claude und die Person.
> Claude liest diese Datei immer zuerst — sie gibt den schnellsten Überblick.

---

## Produkt-Übersicht

**Name:** [Projektname]
**Gestartet:** [Datum]
**Zuletzt aktualisiert:** [Datum]

**Was:** [Ziel in 1-2 Sätzen — was soll dieses Produkt für den Nutzer tun?]
**Für wen:** [Zielgruppe — konkrete Person aus dem Fachgebiet, kein Tech-Jargon]
**Erfolg:** [Woran erkennt man dass es funktioniert?]
**Nicht dabei:** [Bewusste Abgrenzung — was gehört nicht dazu?]

---

## Tech-Stack (global)

[Grundlegende Technologie-Entscheidungen die alle Features teilen]

**Start-Befehl lokal:** [z.B. `npm run dev` oder `python app.py`]
**Port:** [z.B. 3000]

---

## Features

| Feature | Status | Version | Sync |
|---|---|---|---|
| [feature-name] | Geplant | 1 | OK |

**Status-Werte:**
- Geplant — noch nicht begonnen
- In Arbeit — wird gerade gebaut
- In Review — gebaut, wartet auf Test durch Person
- Fertig — Person hat bestätigt, funktioniert
- Problem — bekannter Fehler, muss behoben werden

**Sync:**
- OK — README.md und tech.md haben gleiche sync-version
- Problem — Versionen unterschiedlich, muss angeglichen werden

---

## Für Claude: Lesereihenfolge

1. **Diese Datei** — Produkt-Übersicht, Feature-Status, Sync prüfen
2. **features/[name]/tech.md** — Nur das Feature das gerade gebaut wird
3. **features/[name]/README.md** — Nur wenn Rückfrage mit Person nötig

**Sync-Regel:** README.md und tech.md eines Features immer gemeinsam aktualisieren.
sync-version in BEIDEN erhöhen. Danach diese Datei aktualisieren.

---

## Offene Punkte

_Hier trägt Claude ein was noch geklärt werden muss._

- [ ] [Offener Punkt]
