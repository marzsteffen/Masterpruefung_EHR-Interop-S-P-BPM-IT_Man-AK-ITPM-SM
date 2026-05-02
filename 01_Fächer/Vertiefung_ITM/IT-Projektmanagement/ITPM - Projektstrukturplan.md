---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Initiierung Strukturierung Requirements]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Projektstrukturplan

> [!info] Kurzdefinition
> Der Projektstrukturplan (PSP) stellt in einer Übersicht alle für das Projekt zu leistenden Arbeiten hierarchisch dar. Er ist ein zentrales Steuerungs-Dokument: Grundlage für Ablauf-, Termin-, Ressourcen- und Kostenpläne, für die Risikoanalyse und für die ersten Budgetierungen. **Im PSP werden keine Reihenfolgen dargestellt.**

## Beschreibung

**Funktionen des PSP (Folie 39):**

- Stellt **alle zu leistenden Arbeiten** in einer Übersicht dar.
- Strukturiert und ordnet sämtliche Arbeiten, sodass Ablauf-, Termin-, Ressourcen- und Kostenpläne darauf aufbauen können.
- Wird auch als Grundlage für die **Risikoanalyse** verwendet.
- Hilft bei den ersten **Budgetierungen**.
- Ist ein **zentrales Dokument für die Projektsteuerung**.
- Hilft, die Projektorganisation bedarfsgerecht weiterzuentwickeln.
- Beschreibt **was** zu tun ist (nicht wann/wie).

## Bestandteile / Aufbau

### Drei Arten von Projektstrukturplänen (Folie 40)

| Art | Beschreibung |
|---|---|
| **Objektorientierter PSP** | Projekt wird in Objekte zerlegt (oft in Softwareentwicklung). |
| **Funktionsorientierter PSP** | Unterteilung in unterschiedliche, auszuführende Tätigkeiten. |
| **Gemischtorientierter PSP** | Kombination: höhere Ebenen objekt-, niedrigere funktionsorientiert. |

### Strukturierungsrichtungen (Folie 41)

- **Top-down:** über mehrere Ebenen vom Ganzen heruntergebrochen.
- **Bottom-up:** alle anfallenden Arbeiten werden gesammelt, geordnet und unter Oberpunkten zusammengefasst.

### Ergebnis: Arbeitspakete

Die unterste Ebene, die nicht mehr aufgeteilt werden kann, sind **Arbeitspakete (AP)** – siehe [[ITPM - Arbeitspaket]].

### Wichtige Regeln (Folie 42)

- **Im PSP werden keine Reihenfolgen dargestellt.**
- Die **Verantwortung** für ein Arbeitspaket muss einer **Person eindeutig** zugeordnet werden können.
- Die Beschreibung jedes Arbeitspakets enthält eine **klare Ergebniserwartung**.
- Ein **PSP-Code** wird zur Identifizierung verwendet.

PSPs sind projektspezifisch, abhängig von:
- Größe und Komplexität des Projekts
- Struktur der Organisationseinheit, die Arbeitspakete übernimmt
- Unsicherheiten zum Erstellungszeitpunkt

## Beispiel

Beispiel-PSP aus der Vorlesung (Folie 43, KIS/SAP IS-H-Projekt) – sechs Hauptbereiche:

1. Projektmanagement (1.1 Projekt beauftragt, 1.2 Start, 1.3 Koordination, 1.4 Controlling, 1.5 Marketing, 1.6 Abschluss, 1.7 abgeschlossen)
2. Konzeptionsphase (2.1–2.6: Stammdatenabzug, SOLL-Prozessdefinition, Bereinigung, Rollen, Migrationsplanung)
3. Realisierungsphase (3.1–3.5: Customizing, Programmanpassungen, Formulare/Statistiken)
4. Testphase (4.1–4.3: ISH-Connector, Geschäftsprozesse mit Berechtigungen, Abnahme)
5. Schulungsphase (5.1–5.4: Vorbereitung, Key-User, restliche Schulungen, geschult)
6. Inbetriebnahmephase (6.1–6.6: Initial-Load, GO-Live-Planung, Vorbereitung, Inbetriebnahme, Nacharbeiten, Abnahme)

Legende: weiß = 0 %, gelb = 50 %, grün = 100 % Fertigstellung; blaue Umrandung mit Kursivschrift = Meilenstein.

## Abgrenzung

- **PSP** zeigt **was**, **Ablaufplan** zeigt **wann/Reihenfolge** (siehe [[ITPM - Ablauf- und Terminplan]]).
- PSP ≠ Gantt: Gantt ist eine Darstellungsform für den Ablauf-/Terminplan.
- PSP ist ein **klassisches** Werkzeug; agile Projekte arbeiten mit dem Product Backlog statt PSP.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein PSP, welche drei Arten gibt es, und welche zwei Vorgehensweisen zur Erstellung?

**Anwendungsfrage:** Erstellen Sie für ein Patientenportal-Projekt einen groben PSP (Hauptbereiche und 1–2 AP je Bereich).

**Diskussionsfrage:** Warum dürfen im PSP **keine Reihenfolgen** dargestellt werden? Welche Funktion hat dann der Ablaufplan?

**Mögliche Anschlussfragen:**
- Was ist ein PSP-Code?
- Wer pflegt den PSP über die Projektlaufzeit?
- Verhältnis PSP zu Risikomanagement?

## Verwandt

- [[ITPM - Arbeitspaket]]
- [[ITPM - Ablauf- und Terminplan]]
- [[ITPM - Phasenmodelle]]
- [[ITPM - Aufwandsschätzung - Drei-Punkt]]
- [[ITPM - Meilenstein]]
- [[ITPM - Risikomanagement - Grundlagen]]

## Quelle

- Vorlesung: [[ITPM - VL - Initiierung Strukturierung Requirements]]
- Folien/Seitenangabe: 39–43
