# Deine Idee wird ein Produkt — so einfach wie möglich

> Du brauchst kein technisches Wissen. Du brauchst nur deine Idee und Claude Code.

---

## So startest du

Öffne Claude Code und schreib:

```
/no-tech
```

Das war's. Claude führt dich ab hier durch alles — du tippst nie wieder einen Befehl.

---

## Was danach passiert

### Neues Projekt — 3 Phasen

#### Phase 1: Erzählen
Claude stellt dir Fragen zu deiner Idee — **eine nach der anderen**, nicht alle auf einmal. Wer soll es nutzen? Was soll es tun? Was nervt heute? Du antwortest in deinen eigenen Worten — keine Fachbegriffe nötig.

Claude stellt so viele Fragen wie nötig — keine künstliche Begrenzung. Wenn Claude genug weiß, zeigt es dir eine kurze Zusammenfassung: *"Habe ich das richtig verstanden?"* Du sagst ja oder korrigierst.

**Dauer:** 20–40 Minuten Gespräch

---

#### Phase 2: Anschauen
Claude baut dir ein klickbares Mockup — eine HTML-Datei. Es sieht aus wie eine echte App, aber dahinter ist noch kein Code. Claude öffnet es direkt im Browser für dich — je nach deiner Einstellung automatisch oder nach Rückfrage.

Du klickst durch und sagst: *"Genau so"* oder *"Da fehlt noch X."*

Dieser Schritt ist wichtig: Dinge die im Text klar klangen, sehen manchmal im Mockup ganz anders aus.

**Dauer:** Claude baut 30–60 Minuten, du brauchst 10–15 Minuten zum Durchklicken

---

#### Phase 3: Bauen
Claude baut das Produkt Stück für Stück. Nach jedem Baustein startet Claude die App für dich und öffnet sie im Browser — du kannst sofort testen. Du gibst grünes Licht, dann das nächste Stück.

**Dauer:** Variiert je nach Größe des Produkts

---

### Bestehendes Projekt — Weitermachen

Wenn du `/no-tech` bei einem laufenden Projekt eintippst, zeigt Claude dir zuerst den aktuellen Stand:

```
Hier ist wo wir stehen:

✓ Login (Fertig)
✓ Nutzerverwaltung (Fertig)
⟳ Terminbuchung (In Arbeit)
○ E-Mail-Bestätigung (Geplant)

Wie möchtest du weitermachen?
```

Du kannst dann sagen:
- *"Weiter mit Terminbuchung"* → Phase 3 fortsetzen
- *"Teste mal die Buchung"* → Claude startet und testet
- *"Da ist ein Bug"* → Bug-Fix-Fluss (siehe unten)
- *"Ich brauche noch eine neue Funktion"* → Neue Funktion (siehe unten)
- *"Wir sind fertig"* → Abschluss

---

## Was du tust — und was Claude tut

| Du | Claude |
|---|---|
| Deine Idee beschreiben | Alle technischen Entscheidungen treffen |
| Fachliche Fragen beantworten | Das Produkt entwerfen und strukturieren |
| Das Mockup durchklicken | Das Mockup bauen und im Browser öffnen |
| Prüfen ob etwas stimmt | Den Code schreiben |
| "Weiter" oder "Da ist ein Problem" sagen | Probleme selbst lösen und testen |
| Dein Fachgebiet beschreiben | Technologie, Hosting, Sicherheit entscheiden |

**Du wirst nie gefragt:**
- Welche Technologie verwendet werden soll
- Wie Daten gespeichert werden
- Wo die App läuft
- Wie der Code aufgebaut ist

---

## Was wenn ein Bug auftritt?

Beschreib was du siehst:

- *"Der Button tut nichts wenn ich draufklicke"*
- *"Das sieht auf dem Handy komisch aus"*
- *"Wenn ich X mache passiert Y, aber ich erwarte Z"*

**Was Claude dann tut:**

1. Liest den betroffenen Code selbst durch
2. Versteht was falsch läuft — ohne dich zu fragen
3. Behebt den Fehler
4. Testet ob es jetzt funktioniert
5. Meldet: *"Behoben — hier was ich geändert habe: [einfache Erklärung]"*

**Wenn der Bug tiefer sitzt:**
In seltenen Fällen liegt ein Problem so tief in der Struktur, dass ein normaler Fix nicht reicht. Dann kommt kein stiller Fix — sondern ein ehrlicher Hinweis:

```
⚠️ Umbau notwendig

Was nicht stimmt:
Die Buchungslogik ist so aufgebaut, dass mehrere Nutzer sich
gegenseitig überschreiben können. Das ist kein einzelner Bug —
das ist ein strukturelles Problem.

Aufwand: Ca. 3 Bausteine (Login-System, Buchung, Tests)

Risiken:
- Bestehende Buchungen müssen migriert werden
- 2–3 Tage Arbeit

Empfehlung:
A) Jetzt umbauen — sauber und zukunftssicher (empfohlen)
B) Workaround einbauen — schnell, aber hält nicht ewig
C) Erst weiterentwickeln, Umbau später planen

Was möchtest du tun?
```

Du entscheidest. Claude setzt um.

---

## Neue Funktion hinzufügen

Wenn dein Produkt schon läuft und du etwas Neues brauchst, sag es einfach:

*"Ich brauche noch eine Möglichkeit, Termine zu stornieren."*

**Was Claude dann tut:**

1. Liest zuerst den bestehenden Code — versteht wie alles zusammenhängt
2. Stellt nur die Fragen, die wirklich unklar sind (oft nur 2–3)
3. Baut die neue Funktion passend zum bestehenden Produkt
4. Optional: zeigt ein kleines Mockup nur für den neuen Teil

Claude fragt nicht nochmal alles von vorne — der Kontext aus dem bestehenden Produkt fließt automatisch ein.

---

## Einstellungen anpassen

### Mockup und App — Browser-Verhalten

Standardmäßig fragt Claude bevor es den Browser öffnet. Du kannst das ändern:

- *"Öffne Mockups immer automatisch"* → Claude öffnet ab sofort ohne Rückfrage
- *"Frag mich immer bevor du etwas öffnest"* → Claude fragt immer nach

Claude merkt sich deine Einstellung — du musst es nur einmal sagen.

---

## Ein echtes Beispiel: Lena, Life Coach

**Start:** `/no-tech Ich will ein Buchungstool für meine Klientinnen bauen`

**Phase Erzählen:**
Claude fragt: *"Wer soll Termine buchen — nur bestehende Klientinnen oder auch neue?"* → Lena antwortet.
Claude fragt: *"Sollen Klientinnen sich erinnern lassen?"* → Lena antwortet.
Claude fragt: *"Was passiert wenn ein Termin doppelt gebucht wird?"* → Lena antwortet.
Claude zeigt Zusammenfassung → Lena bestätigt.

**Phase Anschauen:**
Claude baut ein Mockup mit Buchungsseite, Terminauswahl, Bestätigungsseite — und öffnet es direkt im Browser.
Lena: *"Die Seite sieht gut aus, aber ich will oben mein Foto haben."* → Claude passt an.

**Phase Bauen:**
- Baustein 1: Seite mit Lenas Namen und Foto, Beispieltermine sichtbar → Claude öffnet App im Browser
- Baustein 2: Klientin kann echten Termin buchen, Bestätigungs-E-Mail kommt → Claude öffnet App im Browser
- Baustein 3: Lena sieht alle Buchungen in einer Übersicht → Claude öffnet App im Browser
- Baustein 4: Automatische Erinnerungs-E-Mail einen Tag vorher → Claude öffnet App im Browser

Nach jedem Baustein: Lena testet, sagt "passt" oder beschreibt was fehlt.

**6 Wochen später:**
Lena: *"Ich brauche noch eine Warteliste für ausgebuchte Termine."*
Claude liest den Code — stellt 2 Fragen — baut die Funktion.

**Ergebnis:** Ein echtes Buchungstool mit Warteliste — ohne eine Zeile Code zu kennen.

---

## Was Claude im Hintergrund tut

Du siehst nur das Gespräch. Hinter den Kulissen arbeitet Claude strukturiert — mit klaren internen Werkzeugen und Dateien. Hier ist was wirklich passiert:

---

### Beim Start: Kontext laden

**Was Claude tut:** Lädt den gesamten Projektstand aus deinen Dateien.

- **Neues Projekt** → startet bei Phase 1 (Erzählen)
- **Bestehendes Projekt** → liest alle Feature-Status, zeigt dir wo ihr steht, wartet auf deine Eingabe

---

### Beim Start: Dein Profil

**Was Claude tut:** Prüft ob bereits ein Profil von dir existiert.

- **Profil vorhanden** → Claude lädt es still und passt ab sofort Sprache, Fragen und Fachgebiet automatisch an
- **Kein Profil** → Claude stellt dir 5–7 einfache Fragen und speichert deine Antworten als Profil — einmalig, fühlt sich wie normales Gespräch an

**Warum:** Damit Claude immer weiß welche Fragen du beantworten kannst — und welche es selbst entscheiden soll.

---

### Phase 1 — Erzählen: Was intern passiert

```
Du erzählst deine Idee
        │
        ▼
Claude analysiert: Wer hat das Problem? Was kostet es heute?
Woran erkennt man dass es gelöst ist?
        │
        ▼
Claude erstellt intern ein strukturiertes Problem Statement
(du siehst das nicht — Claude nutzt es als Grundlage)
        │
        ▼
Claude erstellt intern ein vollständiges PRD pro Feature:
  ┌─────────────────────────────────┐
  │ KUNDEN-ZONE → du liest das      │
  │ Was es tun soll, für wen, Ziel  │
  └─────────────────────────────────┘
  ┌─────────────────────────────────┐
  │ AI-ZONE → nur für Claude        │
  │ Technologie, Datenstruktur,     │
  │ Hosting — du siehst das nie     │
  └─────────────────────────────────┘
        │
        ▼
Claude zeigt dir nur die Kunden-Zone zur Bestätigung
```

**Was gespeichert wird:** Pro Feature eine README (Kunden-Zone) und eine tech.md (AI-Zone). Kein globales Dokument — jede Funktion hat ihre eigenen Dateien.

---

### Phase 1 — Erzählen: Die Verbesserungsschleife

Nachdem du die Zusammenfassung bestätigt hast, prüft Claude das PRD kritisch:

```
Claude liest das PRD wie ein kritischer Produktmanager
        │
        ▼
Findet Lücken: "Was passiert wenn Nutzer X macht?"
              "Ist diese Annahme wirklich wahr?"
              "Welcher Fall fehlt noch?"
        │
        ▼
Stellt dir eine Frage — wartet auf deine Antwort — stellt die nächste
(So viele wie nötig, keine künstliche Begrenzung)
        │
        ▼
Deine Antworten → PRD wird intern aktualisiert
        │
        ▼
Schleife läuft bis keine neuen Fragen mehr entstehen
        │
        ▼
"Ich denke wir haben alles geklärt — ich baue jetzt das Mockup."
```

---

### Phase 2 — Anschauen: Was intern passiert

```
Claude liest die Kunden-Zone des PRD
        │
        ▼
Identifiziert alle Hauptscreens und Nutzerabläufe
        │
        ▼
Baut eine einzelne HTML-Datei:
  - Alle Hauptseiten der App
  - Klickbare Navigation zwischen Seiten
  - Echter Content aus dem PRD (kein Platzhalter-Text)
  - Design passend zum Fachgebiet
        │
        ▼
Speichert als: claude-vault/mockup.html
        │
        ▼
Öffnet es direkt im Browser (automatisch oder nach Rückfrage — je nach deiner Einstellung)
        │
        ▼
Du klickst durch → gibst Feedback
        │
        ▼
Kleines Feedback → Mockup-Update
Großes Feedback → zurück zur Verbesserungsschleife
Bestätigung → weiter zu Phase 3
```

---

### Phase 3 — Bauen: Was intern passiert

```
Claude liest finales PRD (Kunden-Zone + AI-Zone)
        │
        ▼
Zerlegt alles in kleine Bausteine:
  Reihenfolge: Was bringt dir am schnellsten echten Nutzen?
  Größe: Jeder Baustein = ein sichtbares Ergebnis
  Sprache: Alles in deinen Worten, kein Tech-Jargon
        │
        ▼
Zeigt dir die Baustein-Liste zur Bestätigung
"Stimmt die Reihenfolge? Willst du etwas tauschen?"
        │
        ▼
Baut Baustein 1:
  - Technologie-Entscheidungen: selbst, nach bewährten Standards
  - Code: selbst, mit Fokus auf Einfachheit und Wartbarkeit
  - Probleme: selbst lösen, nicht fragen
        │
        ▼
Startet die App, öffnet Browser (automatisch oder nach Rückfrage)
"Baustein 1 ist fertig. Schau mal rein."
        │
        ▼
Du: "Passt"  →  Baustein 2
Du: "Problem: [Beschreibung]"  →  Claude behebt, testet, meldet zurück
        │
        ▼
Wiederholen bis alle Bausteine fertig
Status jedes Bausteins wird in den Feature-Dateien gespeichert
```

---

### Neue Funktion: Was intern passiert

```
Du beschreibst die neue Funktion
        │
        ▼
Claude liest zuerst den bestehenden Code:
  - Wie ist das Produkt aufgebaut?
  - Was gibt es schon?
  - Was muss die neue Funktion beachten?
        │
        ▼
Stellt nur die Fragen die wirklich unklar sind
(Oft 0–3 Fragen — vieles ergibt sich aus dem Code)
        │
        ▼
Optional: kleines Mockup nur für den neuen Teil
        │
        ▼
Baut die neue Funktion — passend zum Bestand
Legt neue Feature-Dateien (README + tech.md) an
```

---

### Bug-Fix: Was intern passiert

```
Du beschreibst das Problem
        │
        ▼
Claude liest den betroffenen Code selbst
        │
        ▼
Normaler Bug → behebt es, testet, meldet zurück
        │
        ▼
Strukturelles Problem →
  Gibt ehrlichen Hinweis:
  - Was genau nicht stimmt (in einfachen Worten)
  - Wie viel Aufwand ein Umbau wäre
  - Welche Risiken es gibt
  - Empfehlung mit 3 Optionen
  → Wartet auf deine Entscheidung
```

---

### Wann Claude dich warnt (selten)

In sehr seltenen Fällen kommt ein Hinweis:

```
⚠️ Kurzer Hinweis: Für [Thema] wäre Know-how von jemandem
mit [z.B. "Erfahrung mit Zahlungsanbietern"] hilfreich.

Empfehlung: Wir gehen mit der Standardlösung weiter.
Oder möchtest du das vorher klären?
```

Das passiert bei Themen wie Zahlungsabwicklung, Gesundheitsdaten oder sehr großen Nutzerzahlen. In 95% der Projekte nie.

---

### Alle internen Werkzeuge auf einen Blick

| Was Claude intern tut | Wann |
|---|---|
| Projektstand laden (alle Features + Status) | Beim Start jeder Session |
| Profil erstellen / laden | Beim Start, einmalig |
| Problem strukturieren | Während des Gesprächs in Phase 1 |
| PRD pro Feature erstellen (Kunden-Zone + AI-Zone) | Nach dem Gespräch in Phase 1 |
| PRD kritisch prüfen & Lücken finden | Verbesserungsschleife nach Phase 1 |
| Klickbares HTML-Mockup bauen + Browser öffnen | Phase 2 |
| Bausteine planen (Reihenfolge nach Wert) | Beginn von Phase 3 |
| Baustein für Baustein bauen + App starten | Phase 3 |
| Bestehenden Code lesen vor neuer Funktion | Bei Neue-Funktion-Anfragen |
| Bug selbst analysieren und beheben | Bei Bug-Meldungen |
| Alle technischen Entscheidungen treffen | Durchgehend |
| Einstellungen (z.B. Mockup-Verhalten) merken | Sofort wenn du etwas sagst |

---

## Häufige Fragen

**"Muss ich Claude Code installieren?"**
Ja — Claude Code ist das Programm in dem du tippst. Es läuft in deinem Terminal oder als Desktop-App. Die Installation dauert ein paar Minuten und ist einmalig.

**"Was passiert wenn ich eine Pause mache?"**
Claude merkt sich den Stand in deinen Dateien. Du kannst jederzeit aufhören und später weitermachen. Beim nächsten `/no-tech` zeigt Claude dir wo ihr steht.

**"Was wenn mein Produkt danach wächst?"**
Sag einfach was dazukommen soll. Claude liest erst was schon da ist, stellt nur die nötigsten Fragen, und baut die neue Funktion passend rein.

**"Was wenn etwas schiefläuft?"**
Beschreib was du siehst. Claude analysiert den Code selbst, behebt den Fehler und meldet zurück. Wenn ein Problem struktureller Natur ist, bekommst du einen ehrlichen Hinweis mit drei Optionen — du entscheidest.

**"Was bedeuten die Status-Anzeigen?"**

| Status | Bedeutung |
|---|---|
| Geplant | Noch nicht begonnen |
| In Arbeit | Gerade im Bau |
| In Review | Fertig, wartet auf dein Feedback |
| Fertig | Abgenommen und läuft |
| Problem | Etwas stimmt nicht — Claude schaut rein |
