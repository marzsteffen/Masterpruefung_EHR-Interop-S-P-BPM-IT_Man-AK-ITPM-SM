---
fach: bpm
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/bpm
---

# BPM - PF - Prozessanalyse und Methoden

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile
> - Niveau-Konvention: `definition` · `anwendung` · `diskussion`

> [!warning] BPMN 2.0 Materialhinweis
> Das Vorlesungsmaterial erwähnt BPMN 2.0 nur als Bildbeispiel (Folien 102–103), erklärt aber keine Elemente. Die Vorlesung verwendet eine **eigene, reduzierte Flussdiagramm-Notation (4 Symbole + DEMI)**. Karten zu BPMN-Detailinhalten basieren auf der [Ergänzung]-Sektion der Konzept-Note.

## Kontext

Dieser Kartensatz deckt die Prozessmodellierungs- und Analysemethoden aus PzM-Kompakt ab: die eigene Flussdiagramm-Notation der Vorlesung (inkl. DEMI-Verantwortlichkeitsspalten), Brown-Paper-Methode für die IST-Aufnahme, Prozessabgrenzung, Prozessbeschreibung und Kennzahlen (Schritt 1–3 der 4-Schritte-Methode), sowie alle sechs Analysemethoden aus Schritt 2B: Wertschöpfungsanalyse, FMEA, Schnittstellenanalyse, Ishikawa/7M, 5-Warum und Low-Hanging-Fruits.

## Verlinkte Konzepte

- [[BPM - Modellierung - Flussdiagramm Notation]]
- [[BPM - Methode - Brown Paper]]
- [[BPM - Phase 2 - Prozessidentifikation und Abgrenzung]]
- [[BPM - Prozessbeschreibung - Mindestinhalte]]
- [[BPM - Prozess-Kennzahlen]]
- [[BPM - Methode - Wertschoepfungsanalyse]]
- [[BPM - Methode - FMEA]]
- [[BPM - Methode - Schnittstellenanalyse]]
- [[BPM - Methode - Ishikawa 7M]]
- [[BPM - Methode - 5-Warum]]
- [[BPM - Methode - Low-Hanging-Fruits]]

---

## Karten

### Definition

Welche vier Symbole und welche vier Verantwortlichkeitsspalten verwendet die Flussdiagramm-Notation der Vorlesung (kein BPMN)?
?
**Vier Symbole:**
1. **Auslöser / Ergebnis** – Trigger oder Outcome; beschriftet im Passiv.
2. **Prozessschritt** – einzelne Aktivität; Hauptwort + Zeitwort.
3. **Entscheidung** – Verzweigung; Frageform, Ja = in Flussrichtung.
4. **Eigener Prozess** – Verweis auf einen anderen Prozess; Hauptwort + Zeitwort.
**Vier DEMI-Verantwortlichkeitsspalten:**
- **D** – Durchführungsverantwortlich (wer führt aus)
- **E** – Ergebnis- & Entscheidungsverantwortlich (wer entscheidet – pro Schritt genau eine Rolle!)
- **M** – Mitwirkend (wird konsultiert)
- **I** – Informiert (Kenntnisnahme)
Merkhilfe DEMI ≈ RACI (Responsible / Accountable / Consulted / Informed).
(Quelle: Folie 99)

---

Welche drei Kennzahlen liefert eine Wertschöpfungsanalyse, und wie sind sie definiert? Nennen Sie die drei Schritt-Kategorien.
?
**Drei Schritt-Kategorien:**
- **WS** – wertschöpfend: direkter Mehrwert für den Kunden.
- **U** – unterstützend: notwendig, aber kein direkter Wert.
- **V** – verschwendend: nicht notwendig und kein Wert → eliminieren.
**Drei Kennzahlen:**
| Kennzahl | Formel |
|---|---|
| **Wertschöpfungsgrad (WS%)** | Σ WS-Bearbeitungszeit ÷ Σ alle Bearbeitungszeiten |
| **Fluss-Rate (FR%)** | Σ alle Bearbeitungszeiten ÷ Σ Durchlaufzeiten |
| **Wertschöpfungsquotient (WSQ%)** | Σ WS-Bearbeitungszeit ÷ Σ Durchlaufzeiten |
Durchlaufzeit = Liegezeit + Bearbeitungszeit. Folie-Beispiel (Sirup): WS% ≈ 74 %, FR% ≈ 10 %, WSQ% ≈ 7,4 % – die Liegezeit dominiert.
(Quelle: Folien 106–113)

---

Was ist FMEA? Erklären Sie RPZ, die drei Faktoren, ihre Skalen und die Handlungsschwellen laut Vorlesung.
?
**FMEA** (Failure Mode and Effects Analysis) = präventive Risikoanalyse zur Identifikation und Priorisierung potenzieller Fehler *vor* ihrem Auftreten.
**RPZ = B × A × E** (Risikoprioritätszahl):
| Faktor | Bedeutung | Skala |
|---|---|---|
| **B** Bedeutung | Auswirkung des Fehlers | 1 (unbedeutend) → 10 (katastrophal) |
| **A** Auftreten | Häufigkeit | 1 (sehr selten) → 10 (sehr häufig) |
| **E** Entdeckung | Wahrscheinlichkeit, dass Fehler *nicht* entdeckt wird | 1 (sehr wahrscheinlich entdeckt) → 10 (kaum entdeckt) |
**Achtung:** E-Skala ist invers – hoher E-Wert = schlecht.
**Handlungsschwellen (Folie 118):**
- > 150–250: dringender Handlungsbedarf
- 50–150: Maßnahmen erforderlich
- < 50: Maßnahmen empfohlen
**Vier Schritte FMEA:** Prozessablauf analysieren → Schwachstellen bestimmen → RPZ berechnen → Maßnahmen ableiten.
(Quelle: Folien 115–119)

---

Nennen und erklären Sie die 7M-Kategorien des Ishikawa-Diagramms.
?
Das **Ishikawa-Diagramm** (Fischgräten-Diagramm) visualisiert Ursachen eines Problems entlang sieben Kategorien:
| M | Kategorie | Verbesserungs-Hebel |
|---|---|---|
| **Management** | Führung/Planung | Verbesserung der Planung, Prozessführung |
| **Maschine** | Technik/IT | Bestmögliche Nutzung von EDV-Systemen |
| **Methode** | Vorgehensweise | Verbesserung der effektiven Ressourcennutzung |
| **Mitwelt** | Arbeitsumgebung | Verbesserung der physischen Arbeitsumgebung |
| **Mensch** | Personal | Verbesserung der Mitarbeiterausbildung |
| **Material** | Materialien/Unterlagen | Vereinfachung und Kombination von Arbeit und Material |
| **Messung** | Kennzahlen | Verbesserte Messung und Darstellung der Leistung |
Die 7M sind eine Erweiterung der klassischen 4M (ohne Management, Mitwelt, Messung).
Eingebettet in Schritt 3 eines 6-stufigen Problemlösungsansatzes: Problembeschreibung → Sofortmaßnahme → Ursachenanalyse (Brainstorming + Ishikawa + 5-Warum) → Korrekturmaßnahme → Umsetzen → Wirksamkeitsprüfung.
(Quelle: Folien 124–126)

---

### Anwendung

Brown-Paper-Methode: Was genau passiert in einem Brown-Paper-Workshop, und welche vier Aktivitäten umfasst er?
?
Der **Brown-Paper-Workshop** ist ein partizipatives Format zur Erfassung des **IST-Prozesses**: alle Beteiligten visualisieren gemeinsam auf einem großformatigen Papier die realen Abläufe – inklusive informeller Workarounds, die in keiner Doku stehen.
**Vier Aktivitäten (Folie 98):**
1. **Prozessabgrenzung** – Trigger, Outcome und Schnittstellen klären.
2. **IST-Prozess erfassen** – gegenwärtig vorherrschende Arbeitsabläufe festhalten.
3. **IST-Prozess dokumentieren** – Ergebnis des Workshops als Flussdiagramm.
4. **IST-Prozessanalyse** – Schwächen, Risiken und Verbesserungspotenziale identifizieren.
Klinisch: Workshop mit Chirurgen, Pflegekräften, Anästhesie, OP-Personal → Hernien-IST-Pfad inkl. aller tatsächlich gelebten Abweichungen vom Papierpfad.
(Quelle: Folie 98)

---

Ordnen Sie folgende klinische Probleme der jeweils passenden Analysemethode zu und begründen Sie kurz: (a) „Wir wissen nicht, wo im OP-Prozess Zeit verloren geht." (b) „Postoperative Infektionsrate ist plötzlich gestiegen – warum?" (c) „Welche Verbesserungsideen sollen wir zuerst umsetzen?" (d) „Welche Schritte in der Aufnahme sind Zeitverschwendung?"
?
(a) **Zeit verloren im OP-Prozess** → **Schnittstellenanalyse** (Übergaben identifizieren, Formen erfassen, Verzögerungen lokalisieren) + ggf. Wertschöpfungsanalyse für Liegezeiten.
(b) **Infektionsrate gestiegen – warum?** → **Ishikawa (7M)** für strukturiertes Brainstorming aller Ursachenkategorien; dann **5-Warum** zum Tieferbohren auf dem relevantesten Ast bis zur Wurzelursache.
(c) **Welche Ideen zuerst?** → **Low-Hanging-Fruits-Diagramm** (Bedeutung × Aufwand 1–4): Maßnahmen mit hoher Bedeutung bei niedrigem Aufwand zuerst.
(d) **Welche Schritte sind Zeitverschwendung?** → **Wertschöpfungsanalyse**: jeden Schritt als WS / U / V klassifizieren, Liegezeiten erfassen, WS%, FR%, WSQ% berechnen.
(Quelle: Folien 106–129)

---

### Diskussion

FMEA vs. Ishikawa: Wann setze ich welche Methode ein, und welche methodische Schwäche hat die RPZ-Multiplikation?
?
**Einsatz:**
- **FMEA** = *prospektiv* (vor dem Fehler): „Was könnte schiefgehen?" – ideal bei der Einführung neuer Prozesse/Pfade, um Risiken vorab zu priorisieren.
- **Ishikawa** = *retrospektiv* (nach dem Fehler): „Warum ist es schiefgegangen?" – ideal zur Ursachenanalyse eines bereits eingetretenen Problems.
**Schwäche der RPZ-Multiplikation:**
- Verschiedene Kombinationen ergeben denselben RPZ-Wert, obwohl die Risikoprofile sehr unterschiedlich sind: 1×10×10 = 100 (seltener, katastrophaler, unsichtbarer Fehler) ist gleichwertig wie 10×10×1 = 100 (häufiger, katastrophaler, immer erkannter Fehler).
- Ein hoher B-Wert (katastrophale Folge) kann durch niedrige A und E „herausgemittelt" werden – obwohl ein Fehler mit katastrophaler Folge Maßnahmen verdient, egal wie selten.
- [Ergänzung] AIAG-VDA 2019 hat die RPZ-Multiplikation daher durch eine Action-Priority-Matrix abgelöst.
(Quelle: Folien 115–119)

---

Wie kombiniert man Ishikawa und 5-Warum sinnvoll, und warum endet 5-Warum oft fälschlicherweise bei einer Person?
?
**Sinnvolle Kombination:**
1. **Ishikawa** zuerst: Brainstorming entlang der 7M → breite, strukturierte Ursachenlandschaft. Welche Kategorie hat die meisten/relevantesten Einträge?
2. **5-Warum** danach: Pro relevantem Ursachen-Ast gezielt in die Tiefe bohren, bis zur systemischen Wurzelursache.
Ishikawa ist horizontal-breit, 5-Warum ist vertikal-tief.
**Warum endet es fälschlicherweise bei einer Person?**
Kognitive Verzerrung: Wenn gefragt wird „warum ist X nicht gemacht worden?", landet man schnell bei „weil Person Y es vergessen hat". Das ist keine Wurzelursache, sondern ein Symptom – die eigentliche Frage ist: „Welcher Prozess hat es nicht strukturell abgesichert?" Verbindung zur gesunden Fehlerkultur (Deming, Punkt 8: „Schaffe die Angst ab") und zum Systemansatz von „To Err Is Human".
(Quelle: Folien 124–127)

---

Welche neun Möglichkeiten zur Prozessneugestaltung nennt die Vorlesung (Folie 136)? Nennen Sie alle neun mit ihrer primären Wirkungsrichtung.
?
Laut Folie 136 (Quelle: Wagner/Patzak, Performance Excellence):
| # | Maßnahme | Primäre Wirkung |
|---|---|---|
| 1 | **Weglassen / Auslassen** | Aufwand reduzieren |
| 2 | **Zusammenlegen** | Schnittstellen reduzieren |
| 3 | **Parallelisieren** | Zeit reduzieren |
| 4 | **Selektieren** | Effektivität erhöhen (nicht jeden Schritt für jeden Fall) |
| 5 | **Überlappen** | Zeit reduzieren (Schritte zeitlich überlappend starten) |
| 6 | **Auslagern** | Ressourcen optimieren (intern/extern) |
| 7 | **Ergänzen** | Qualität erhöhen (fehlende Schritte hinzufügen) |
| 8 | **Reihenfolge ändern** | Effizienz und Risikofruherkennung |
| 9 | **Automatisieren** | Skalierbarkeit, Qualität, Geschwindigkeit |
Klinisch: Parallelisieren = präoperative Diagnostik-Schritte gleichzeitig anfordern statt sequenziell; Automatisieren = KIS-gestützte Pfad-Orderset.
(Quelle: Folie 136)

---

Warum hat die Vorlesung eine eigene, vereinfachte Flussdiagramm-Notation statt direkt BPMN 2.0? Welche Grenzen hat die Vorlesungsnotation?
?
**Warum eigene Notation:**
Die Vorlesung verwendet vier Symbole + DEMI statt der ~100 BPMN-Elemente. Pragmatischer Grund: BPMN 2.0 hat eine steile Lernkurve; die Zielgruppe sind Prozessverantwortliche im Krankenhaus, keine BPMN-Modellierungsspezialisten. Einstiegshürde bewusst niedrig gehalten.
**Grenzen der Vorlesungsnotation:**
- Keine standardisierte Maschinierbarkeit (BPMN kann direkt in Workflow-Engines ausgeführt werden).
- Keine Event-Differenzierung (Start/Intermediate/End Events mit Subtypen).
- Keine Pools/Lanes für mehrere Organisationseinheiten in einem Modell.
- Nicht werkzeugübergreifend interpretierbar (Camunda, Signavio, ADONIS sprechen BPMN, nicht die Vorlesungsnotation).
**BPMN 2.0** (OMG-Standard, Version 2.0.2, 2014) ist der Industriestandard – vier Elementkategorien: Flow Objects (Activity, Event, Gateway), Connecting Objects (Sequence Flow, Message Flow, Association), Swimlanes (Pool, Lane), Artefakte. [Ergänzung aus Konzept-Note]
(Quelle: Folien 99, 102–103; BPMN-Ergänzung laut Konzept-Note)

---

Low-Hanging-Fruits: Was ist das Diagramm, wie funktioniert die Priorisierung, und warum sind Low-Hanging-Fruits langfristig ein zweischneidiges Schwert?
?
**Diagramm:** 2D-Koordinatensystem, Aufwand (x, niedrig→hoch) × Bedeutung (y, niedrig→hoch), Skala je 1–4.
**Vier Quadranten:**
- Hohe Bedeutung + niedriger Aufwand → **Low-Hanging Fruits** (zuerst!)
- Hohe Bedeutung + hoher Aufwand → Hauptvorhaben (planen)
- Niedrige Bedeutung + niedriger Aufwand → Quick Wins / nice-to-have
- Niedrige Bedeutung + hoher Aufwand → vermeiden
Die Liste wird im **Prozess-Jour-Fixe (PzJF)** vom Prozessverantwortlichen eingefordert. Übergang zum Maßnahmenplan (Verantwortlich + Termin + PDCA-Mapping).
**Zweischneidiges Schwert:** Konsequente Konzentration auf Low-Hanging-Fruits erntet irgendwann alle leichten Früchte. Schwierige, aber strategisch wichtige Maßnahmen (hohe Bedeutung + hoher Aufwand) bleiben dann dauerhaft liegen → Stagnation auf mittlerem Niveau. Trade-off: Quick-Win-Motivation vs. strategische Langfristentwicklung.
(Quelle: Folien 128–129)

---

## Mögliche Anschlussfragen des Prüfers

- Was ist der Unterschied zwischen Brown-Paper-Methode und Process Mining – wann setzen Sie welches ein?
- Wie viel Prozent der Information geht laut Vorlesung an Schnittstellen verloren, und welche drei Arten von Schnittstellen gibt es?
- Welche fünf Typen nicht-wertschöpfender Tätigkeiten nennt die Vorlesung bei der Wertschöpfungsanalyse?
- Was ist der Unterschied zwischen Fluss-Rate und Wertschöpfungsgrad – welche ist in der Regel niedriger und warum?
- Welche Spalten hat eine Prozessbeschreibung mindestens?
- Warum darf es pro Prozessschritt nur eine E-Rolle (Entscheidungsverantwortung) geben?
- Wer fordert die Liste für Verbesserungspotenziale im laufenden Betrieb ein?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
