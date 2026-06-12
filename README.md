# claude-not-tech-engineering

> Produkte bauen ohne technisches Wissen — mit Claude Code als persönlichem Produkt-Guide.

**Website & Install:** https://simonwuensch-it-studio-rech.github.io/claude-not-tech-engineering/

---

## Was ist das?

Ein Toolkit für Claude Code das es Menschen ohne technischen Hintergrund ermöglicht, echte Software zu bauen. Du beschreibst deine Idee in normaler Sprache — Claude entscheidet alle technischen Fragen selbst und baut Schritt für Schritt.

Der einzige Befehl den du je eingeben musst: `/no-tech`

---

## Was du bekommst

### Skills (8 Dateien → `~/.claude/commands/`)
Claude Code Skills die den kompletten Prozess abdecken:

| Skill | Was er tut |
|---|---|
| `no-tech.md` | Haupt-Orchestrator — startet alles |
| `no-tech-load-context.md` | Lädt Projektstand beim Session-Start |
| `no-tech-problem-statement.md` | Idee → scharfes Problem |
| `no-tech-to-prd.md` | Problem → Produktanforderungen |
| `no-tech-grill-with-docs.md` | Lücken im PRD finden |
| `no-tech-prototype.md` | Klickbares HTML-Mockup bauen |
| `no-tech-to-issues.md` | PRD → Bausteine |
| `create-user-persona.md` | Persönliches Profil anlegen |

### Workspace (Projektordner → `claude-vault/`)
- `CLAUDE.md` — Kontext für Claude
- `no-tech-workflow.md` — Dein Leitfaden
- `personas/` — 4 Nutzertypen (Gründerin, Fachexperte, Prozess-Optimiererin, Kreativer)
- `claude-data/_templates/` — Vorlagen für Features

---

## Installation

Besuche die Website und folge den Anweisungen:
**https://simonwuensch-it-studio-rech.github.io/claude-not-tech-engineering/**

Oder gib Claude direkt diesen Prompt:

```
Installiere das claude-not-tech-engineering Toolkit.
Alle Anweisungen findest du hier:
https://simonwuensch-it-studio-rech.github.io/claude-not-tech-engineering/
```

---

## Wie es funktioniert

```
Phase 1: Erzählen
  Claude fragt — eine Frage nach der anderen
  Du antwortest in deinen eigenen Worten
  Kein Fachbegriff nötig

Phase 2: Anschauen
  Claude baut ein klickbares HTML-Mockup
  Öffnet es direkt im Browser
  Du klickst durch und gibst Feedback

Phase 3: Bauen
  Claude baut Baustein für Baustein
  Startet die App nach jedem Schritt
  Du testest, sagst ob es stimmt
```

Für bestehende Produkte:
- **Neue Funktion:** Claude liest erst den Code, stellt dann nur die nötigsten Fragen
- **Bug:** Claude analysiert selbst, behebt, testet — meldet zurück

---

## Repo-Struktur

```
claude-not-tech-engineering/
├── docs/                    ← GitHub Pages Website
├── skills/                  ← Claude Code Skills
├── workspace/               ← Projektordner-Template
└── install-manifest.json    ← Maschinenlesbare Install-Anweisungen
```

---

## Lizenz

MIT
