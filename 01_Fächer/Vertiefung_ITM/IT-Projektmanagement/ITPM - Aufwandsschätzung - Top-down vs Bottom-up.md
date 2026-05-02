---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Aufwandsschätzung - Top-down vs Bottom-up

> [!info] Kurzdefinition
> Top-down schätzt den Gesamtaufwand aus der allgemeinen Funktionalität und teilt diesen auf Teilfunktionen auf. Bottom-up schätzt den Aufwand jeder Komponente einzeln und summiert. Beide Strategien haben gegensätzliche Schwächen.

## Beschreibung

Aus Folie 32:

### Top-down Schätzung

- Aufwand für das **gesamte Projekt** schätzen aus allgemeiner Funktionalität und dessen Aufteilung auf Teilfunktionen.
- Basis: **logische Funktionen** statt Komponenten, welche die Funktionalität implementieren.
- **Gefahr:** Schätzung geht **nicht genug auf wichtige Details** ein.

### Bottom-up Schätzung

- Aufwand für **jede Komponente** bestimmen.
- Gesamtaufwand = **Summe aller Teilaufwände**.
- **Gefahr:** **Projektübergreifende Aktivitäten** werden vergessen.

## Bestandteile / Aufbau

| Aspekt | Top-down | Bottom-up |
|---|---|---|
| **Richtung** | vom Ganzen ins Detail | von Teilen zum Ganzen |
| **Basis** | logische Funktionen | Komponenten |
| **Vorteil** | schneller, ganzheitlich | präzise pro Komponente |
| **Risiko** | Detail wird vernachlässigt | Querschnittsaufgaben werden übersehen |
| **Geeignet für** | frühe Phase, grobe Schätzung | spätere Phase, Detailplanung |

## Beispiel

*Im PDF nicht durch konkretes Beispiel illustriert.*

## Abgrenzung

- Beide Strategien können (und sollten in der Praxis) **kombiniert** werden – top-down für die Gesamtschätzung, bottom-up zur Validierung.
- Beziehung zur PSP-Erstellung: Top-down vs. Bottom-up gibt es auch dort als Strukturierungsrichtung (siehe [[ITPM - Projektstrukturplan]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich Top-down- und Bottom-up-Schätzung, und welche Risiken hat jede?

**Anwendungsfrage:** Sie haben ein Pflichtenheft mit detaillierten Komponenten. Welche Strategie wählen Sie? Und ohne Pflichtenheft?

**Diskussionsfrage:** Wann sollten beide Strategien kombiniert werden, und was tun, wenn sie zu sehr unterschiedlichen Ergebnissen führen?

**Mögliche Anschlussfragen:**
- Wie verhält sich diese Strategie zur Wahl des Schätzverfahrens (Delphi, FP, CoCoMo)?
- Wie passt agile Schätzung (Story Points) hier rein?

## Verwandt

- [[ITPM - Aufwandsschätzung - Grundlagen]]
- [[ITPM - Aufwandsschätzung - Schätzverfahren Übersicht]]
- [[ITPM - Projektstrukturplan]]
- [[ITPM - Agile - Story Points]]

## Quelle

- Vorlesung: [[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]
- Folien/Seitenangabe: 32
