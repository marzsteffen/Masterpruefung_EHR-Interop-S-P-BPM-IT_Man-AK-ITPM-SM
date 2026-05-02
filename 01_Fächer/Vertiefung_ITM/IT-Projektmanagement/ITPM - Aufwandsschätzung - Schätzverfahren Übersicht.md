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

# ITPM - Aufwandsschätzung - Schätzverfahren Übersicht

> [!info] Kurzdefinition
> Es gibt vier grundsätzliche Verfahren der Aufwandsschätzung: **Expertenbefragung** (Delphi), **Kennzahlverfahren** (Prozentsatz), **Vergleichsmethoden** (Analogie) und **algorithmische Schätzverfahren** (Function Points, CoCoMo). Zusätzlich gibt es politische Methoden (Pricing-to-win, Max-Budget).

## Beschreibung

Die Vorlesung systematisiert die Schätzverfahren auf Folien 32–37.

## Bestandteile / Aufbau

### Drei Teilbereiche der Schätzung (Folien 30–31)

| Teilbereich | Inhalt |
|---|---|
| **Größenschätzung** | Wie lange braucht ein Projektmitglied in Zeiteinheiten für ein Arbeitspaket? |
| **Aufwandsschätzung** | Im einfachsten Fall proportional zur Größe; in der Realität nicht trivial. Hier werden unklare Anforderungen häufig erkannt. |
| **Kostenschätzung** | Aus Aufwand + Personalstundensätzen + weitere Kostenarten (Reisen, Fortbildung, Werkzeuge). |

### Vier grundsätzliche Verfahren (Folie 37)

| Verfahren | Beispiel | Detail-Note |
|---|---|---|
| **Expertenbefragung** | Delphi-Methode | [[ITPM - Aufwandsschätzung - Delphi-Methode]] |
| **Kennzahlverfahren** | Prozentsatzmethode | [[ITPM - Aufwandsschätzung - Prozentsatzmethode]] |
| **Vergleichsmethoden** | Analogiemethode | [[ITPM - Aufwandsschätzung - Analogiemethode]] |
| **Algorithmische Schätzverfahren** | Function-Points, CoCoMo | [[ITPM - Aufwandsschätzung - Function Point]], [[ITPM - Aufwandsschätzung - CoCoMo]] |

**Zusätzlich:** Politische Methoden (Pricing-to-win, Max-Budget) – siehe [[ITPM - Aufwandsschätzung - Politische Methoden]].

### Methodencharakter (Folien 33–36)

- **Formale Methoden:** Aufwand = f(Mengengerüst, Einflussgrößen).
- **Vergleichs-/Analogiemethoden:** Daten abgeschlossener / ähnlicher Projekte → Kennzahlen → geplantes Projekt; **Erfahrungsdatenbank** ist zentrale Voraussetzung.
- **Prozentsatzmethoden:** keine vollständig eigenständige Schätzmethode → Detailschätzung einer Phase mit anderer Methode + Hochrechnung.

### Strategien (Folie 32)

- **Top-down:** allgemeine Funktionalität → Auf-Teilung auf Teilfunktionen → Schätzung. *Gefahr:* zu wenig Detail.
- **Bottom-up:** Komponentenaufwand → Summe der Teilaufwände. *Gefahr:* projektübergreifende Aktivitäten vergessen.

Detail in eigener Note: [[ITPM - Aufwandsschätzung - Top-down vs Bottom-up]].

## Beispiel

Prozentsatzmethode nach Hewlett-Packard (Folie 36): Analyse 18 % – Entwurf 19 % – Implementierung 34 % – Test 29 %.

## Abgrenzung

- Mehrere Verfahren werden in der Praxis **kombiniert** – Best Practice der Vorlesung empfiehlt mehrere Schätzer und mehrere Verfahren.
- Politische Methoden sind **keine Schätzverfahren im engeren Sinne**, sondern Verhandlungsstrategien.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Hauptverfahren der Aufwandsschätzung kennt die Vorlesung? Welche zusätzlichen Methoden?

**Anwendungsfrage:** Welches Verfahren passt zu welcher Projektsituation – frühe Phase, ähnliche Vorprojekte, klar definiertes Pflichtenheft, politische Vorgabe?

**Diskussionsfrage:** Warum sollten mehrere Verfahren kombiniert werden? Welche Gefahren bei Einzelmethoden?

**Mögliche Anschlussfragen:**
- Welche drei Teilbereiche umfasst eine Schätzung?
- Wann ist Bottom-up, wann Top-down sinnvoll?
- Was sind „Mengengerüst" und „Einflussgrößen"?

## Verwandt

- [[ITPM - Aufwandsschätzung - Grundlagen]]
- [[ITPM - Aufwandsschätzung - Top-down vs Bottom-up]]
- [[ITPM - Aufwandsschätzung - Delphi-Methode]]
- [[ITPM - Aufwandsschätzung - Prozentsatzmethode]]
- [[ITPM - Aufwandsschätzung - Analogiemethode]]
- [[ITPM - Aufwandsschätzung - Function Point]]
- [[ITPM - Aufwandsschätzung - CoCoMo]]
- [[ITPM - Aufwandsschätzung - Politische Methoden]]
- [[ITPM - Agile - Planning Poker]]

## Quelle

- Vorlesung: [[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]
- Folien/Seitenangabe: 30–37
