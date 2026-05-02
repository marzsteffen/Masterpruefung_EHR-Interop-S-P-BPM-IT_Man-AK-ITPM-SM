---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Prozessmanagement Grundlagen (PzM-Kompakt)]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - Modellierung - Flussdiagramm Notation

> [!info] Kurzdefinition
> Die **Flussdiagramm-Notation** der Vorlesung beschreibt vier Symbol-Typen (Auslöser/Ergebnis, Prozessschritt, Entscheidung, eigener Prozess) und eine vierspaltige **DEMI-Verantwortlichkeits­spalte** (Durchführung, Ergebnis-/Entscheidung, Mitwirkend, Informiert).

## Beschreibung

Folie 99. Die Vorlesung definiert eine eigene, einfache Flussdiagramm-Legende:

### Symbole

| Symbol | Bedeutung | Beschriftung (Form) |
|---|---|---|
| Auslöser / Ergebnis | Trigger / Outcome | im Passiv |
| Prozessschritt | einzelne Aktivität | Hauptwort + Zeitwort |
| Entscheidung | Verzweigung | Frageform; Ja = in Flussrichtung |
| Eigener Prozess | Verweis auf anderen Prozess | Hauptwort + Zeitwort |

### Verantwortlichkeitsspalten (DEMI)

Pro Prozessschritt werden vier Spalten geführt:

| Kürzel | Bedeutung (laut Folie 99) |
|---|---|
| **D** | Durchführungs­verantwortlich |
| **E** | Ergebnis- & Entscheidungs­verantwortlich |
| **M** | Mitwirkend |
| **I** | Informiert |

Im PDF wird der Begriff **DEMI** nicht ausgeschrieben, nur die vier Buchstaben werden verwendet.

#### Verhältnis DEMI ↔ RACI (Ergänzung)

Das DEMI-Schema ist eine deutsche Variante des in der BPM-Praxis verbreiteten **RACI** (Responsibility-Assignment-Matrix). Die Buchstaben stehen für unterschiedliche Konzepte, die Logik ist aber gleich.

| DEMI (Folien) | RACI (englische Praxis) | Bedeutung |
|---|---|---|
| **D** Durchführungsverantwortlich | **R** Responsible | Wer führt die Tätigkeit aus? Mehrere R/D pro Schritt erlaubt. |
| **E** Ergebnis-/Entscheidungs­verantwortlich | **A** Accountable | Wer hat die letzte Entscheidung und trägt die Verantwortung für das Ergebnis? Pro Schritt **genau eine** Person/Rolle – Eindeutigkeit ist Pflicht. |
| **M** Mitwirkend | **C** Consulted | Wer wird zwei-Wege-konsultiert (gibt Input, kann widersprechen)? |
| **I** Informiert | **I** Informed | Wer wird ein-Wege-informiert (nur Kenntnisnahme)? |

Diese 1:1-Abbildung ist eindeutig. In manchen Quellen wird zusätzlich **RASCI** (mit "Supportive") oder **RACI-VS** (mit "Verifies", "Signs") erweitert; das geht über DEMI hinaus und ist nicht Inhalt der Vorlesung.

**Zentrale praktische Regel beider Schemata:** pro Prozessschritt darf es nur *eine* A/E-Rolle geben – sonst ist die Verantwortung diffus und der Schritt nicht steuerbar. Mehrere R/D, mehrere C/M und mehrere I/I sind erlaubt.

### Swim-Lane-Darstellung / BPMN 2.0

Folie 102 zeigt ein „Swim-Lane-Diagramm (Modellierung mittels BPMN 2.0)" und Folie 103 ein „BPMN 2.0 Poster" als Beispielbild. **Im PDF wird BPMN 2.0 nicht erklärt** – die Vorlesung verwendet es nur als Beispielbild für die Swim-Lane-Modellierung. Die folgende Erläuterung ist eine externe Ergänzung, weil BPMN 2.0 ein expliziter Themenbereich des MOC ist und die Vorlesung den Begriff einführt, ohne ihn auszuführen.

## Ergänzung außerhalb der Vorlesung

### BPMN 2.0 – Grundelemente

**Business Process Model and Notation 2.0** (OMG-Standard, Version 2.0 finalisiert 2011, Version 2.0.2 von 2014) ist die Industrie-Standardnotation für Prozessmodelle. Sie definiert ca. 100 Symbole, die in vier Kategorien gegliedert sind:

#### 1. Flow Objects (Flussobjekte)

| Symbol | Form | Bedeutung |
|---|---|---|
| **Activity** | Abgerundetes Rechteck | Eine Tätigkeit / ein Prozessschritt. Untertypen: Task (atomar), Sub-Process (zusammenklappbar), Call Activity, Transaction. |
| **Event** | Kreis | Ein Ereignis. Drei Lebenslagen über die Linienstärke kodiert: **Start** (dünn), **Intermediate** (doppelt), **End** (dick). Untertypen über Symbol im Kreis: Message, Timer, Error, Signal, Conditional, Compensation, Cancel, Terminate. |
| **Gateway** | Raute | Eine Verzweigung oder Zusammenführung. Typen: **XOR** (exklusiv, „entweder/oder", leere Raute oder mit X), **AND** (parallel, „und", mit +), **OR** (inklusiv, mit O), **Event-based** (entscheidet sich am ersten eintretenden Event), **Complex**. |

#### 2. Connecting Objects (Verbindungen)

- **Sequence Flow** (durchgezogener Pfeil): Reihenfolge der Aktivitäten innerhalb eines Pools.
- **Message Flow** (gestrichelter Pfeil mit offenem Pfeilkopf): Nachrichtenaustausch zwischen Pools.
- **Association** (gepunktete Linie): Verknüpfung von Annotationen / Daten zu Flussobjekten.

#### 3. Swimlanes (Pools und Lanes)

- **Pool**: ein Beteiligter (z. B. „Krankenhaus", „Hausarzt", „Patient"). Pools kommunizieren ausschließlich über Message Flows.
- **Lane**: eine Rolle/Abteilung *innerhalb* eines Pools (z. B. „Anästhesie", „OP", „Recovery" innerhalb von „Krankenhaus"). Lanes innerhalb eines Pools sind über Sequence Flows verbunden.

#### 4. Artefakte

- **Data Object**: Datenobjekt, das im Prozess verwendet wird.
- **Group**: visuelle Gruppierung ohne Bedeutung für den Ablauf.
- **Text Annotation**: Kommentar.

### Zentrale Modellierungsregeln

- Sequence Flow überschreitet keine Pool-Grenzen.
- Jeder Prozess startet mit (mindestens) einem Start Event und endet mit (mindestens) einem End Event.
- Gateways verzweigen / synchronisieren – sie führen *keine* Tätigkeiten aus.

### BPMN 2.0 vs. die Vorlesungs-Notation

| Aspekt | Vorlesungs-Flussdiagramm | BPMN 2.0 |
|---|---|---|
| Symbole | 4 (+ DEMI-Spalten) | ~100 |
| Pools/Lanes | nicht vorgesehen | zentral |
| Event-Differenzierung | keine | Start/Intermediate/End mit Subtypen |
| Standardisierung | hauseigen (scc-score) | OMG-Standard, Werkzeugübergreifend (Camunda, Signavio, Bizagi, …) |
| Lernkurve | flach | mittel bis steil |

### Quelle der Ergänzung

OMG, *Business Process Model and Notation (BPMN) Version 2.0.2*, Object Management Group, Januar 2014. Die hier zitierten Element-Definitionen entsprechen dem OMG-Standard und sind in jedem aktuellen BPMN-Lehrbuch enthalten (z. B. Allweyer, *BPMN 2.0*, 2016; Freund/Rücker, *Praxishandbuch BPMN 2.0*, 6. Aufl. 2019).

## Bestandteile / Aufbau

- Vier Symbol-Typen
- DEMI-Spalten für Verantwortlichkeit
- Beschriftungs-Regeln (Passiv für Trigger/Outcome, Hauptwort+Zeitwort für Aktivitäten, Frageform für Entscheidungen, Ja = Flussrichtung)

## Beispiel

Folie 100 zeigt ein einfaches Flussdiagramm „Personal anfordern":
- Trigger (passiv): „Personal ist angefordert"
- Aktivität: „Anforderungsprofil erstellen"
- Entscheidung: „Personal genehmigt?" – nein → Ende; ja → „Stelle ausschreiben" → ...

## Abgrenzung

- **Flussdiagramm ≠ BPMN 2.0.** BPMN 2.0 ist ein deutlich umfangreicherer Standard; das Flussdiagramm der Vorlesung ist eine reduzierte Variante.
- **Flussdiagramm ≠ Swim-Lane.** Swim-Lane fügt Bahnen für unterschiedliche Akteure hinzu; das einfache Flussdiagramm hat nur eine Bahn.
- **DEMI ≠ RACI** in der Bezeichnung, aber inhaltlich nahezu identisch. **Im PDF nicht als RACI bezeichnet.**

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche Symbole und welche Verantwortlichkeitsspalten verwendet die Flussdiagramm-Legende der Vorlesung?"

**Anwendungsfrage:** „Modellieren Sie den Prozess ‚Patient aufnehmen‘ mit der Notation der Vorlesung." – Trigger (Patient steht in Aufnahme), Schritte mit DEMI, Entscheidungen mit Frageform.

**Diskussionsfrage:** Warum verwendet die Vorlesung die einfache Notation und nicht direkt BPMN 2.0? – Pragmatische Einstiegshürde; BPMN 2.0 hat ~50 Elemente, das Flussdiagramm fünf. Trade-off: BPMN ist standardisiert und ausdrucksstärker, aber lernintensiver.

**Mögliche Anschlussfragen:**
- Was bedeuten die vier DEMI-Buchstaben?
- Wie modelliert man eine Entscheidung?
- In welchem Verhältnis steht das Flussdiagramm zu BPMN 2.0?

## Verwandt

- [[BPM - Methode - Brown Paper]]
- [[BPM - Phase 2 - 4-Schritte-Methode]]
- [[BPM - BPMN]]
- [[BPM - Methode - Schnittstellenanalyse]]

## Quelle

- Vorlesung: [[BPM - VL - Prozessmanagement Grundlagen (PzM-Kompakt)]]
- Folien/Seitenangabe: Folie 99 (Legende), Folie 100 (Beispiel), Folien 102–103 (Swim-Lane / BPMN 2.0 als visuelles Beispiel ohne Detailerklärung)
