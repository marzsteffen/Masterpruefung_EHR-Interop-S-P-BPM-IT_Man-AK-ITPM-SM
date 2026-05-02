---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Evidenzbasierte Medizin]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - Validität - Interne vs. Externe

> [!info] Kurzdefinition
> **Interne Validität** beschreibt, wie frei eine Studie von systematischen Fehlern (Bias) ist – also wie verlässlich die Innen-Aussage ist. **Externe Validität** beschreibt die Generalisierbarkeit/Übertragbarkeit der Ergebnisse auf andere Personen, Situationen oder Zeitpunkte.

## Beschreibung

Folien 21 (Interne Validität / Bias) und 31 (Externe Validität).

### Interne Validität (Folie 21)

Interne Validität ist die Frage: **Stimmt das Ergebnis innerhalb der Studie?** Hauptbedrohung: Bias. Eine biasarme Studie hat hohe interne Validität.

Quelle in den Folien: Cochrane Deutschland & AWMF, *Risk-of-Bias-Manual* 2016.

In dem zitierten Manual werden u. a. Selection-, Performance-, Detection-, Attrition- und Reporting-Bias als Bedrohungen der internen Validität identifiziert (im Foliensatz nur als Bild auf Folie 21, nicht textuell ausgeführt).

### Externe Validität (Folie 31, wörtlich)

> Die externe Validität hingegen bezeichnet die Generalisierbarkeit oder Übertragbarkeit der Untersuchungs­ergebnisse und hängt damit von der Fragestellung, den Ein- und Ausschluss­kriterien und dem Setting der Studie ab. Sie gibt an, ob Studienresultate auf andere Personen, Situationen und/oder Zeitpunkte übertragen werden können.

### Trade-off

| Maßnahme | Interne Validität | Externe Validität |
|---|---|---|
| Restriktion der Studienpopulation (z. B. nur Nichtraucher < 60 J.) | ↑ (weniger Confounder) | ↓ (Ergebnisse gelten nur für Nichtraucher < 60 J.) |
| Heterogene Population mit großer Fallzahl | ↓ (mehr Störfaktoren) | ↑ (breit übertragbar) |
| Strikt protokollierte RCT-Bedingungen | ↑ | ↓ („efficacy") |
| Pragmatische Studie unter Alltagsbedingungen | ↓ | ↑ („effectiveness") |

→ Hohe interne Validität ist nicht automatisch hohe externe Validität, und umgekehrt.

### Bezug zu klinischen Pfaden

Klinische Pfade implementieren in der Regel Evidenz aus Studien mit hoher *interner* Validität (RCT-basierte Leitlinien). Die Übertragbarkeit auf das eigene Patientengut hängt von der *externen* Validität ab – ein Pfad funktioniert in einem österreichischen Allgemein­krankenhaus möglicherweise anders als in dem amerikanischen Universitäts­zentrum, in dem die Originalstudie lief.

## Bestandteile / Aufbau

```
Studie/Daten
   ├── Interne Validität → bias-arm? → vertraue ich der Aussage IN der Studie?
   └── Externe Validität → übertragbar? → vertraue ich der Aussage AUF mein Setting?
```

## Beispiel

Eine Studie zur Wirksamkeit eines neuen Hernien-Verfahrens schließt nur ASA-1-Patient:innen unter 50 Jahren ein. Ergebnis: Komplikationsrate 1 %. Interne Validität: hoch (homogene Gruppe, wenig Confounding). Externe Validität: gering (kein Hinweis, was passiert bei multimorbiden 75-Jährigen). Wenn man auf Basis dieser Studie einen Pfad für die Allgemein­chirurgie aufsetzt, bekommt man schnell ein Realitätsproblem.

## Abgrenzung

- **Interne Validität ≠ Reliabilität.** Reliabilität = Wiederhol­genauigkeit; interne Validität = Bias-Freiheit.
- **Externe Validität ≠ Repräsentativität.** Repräsentativität ist *eine Voraussetzung* für externe Validität, aber nicht das gleiche.
- **Beide sind nicht durch Stichprobengröße allein gewährleistet.** Eine sehr große Studie mit demselben Bias bleibt verzerrt; eine sehr große Studie mit Restriktion auf eine enge Gruppe bleibt schlecht generalisierbar.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was unterscheidet interne von externer Validität?"

**Anwendungsfrage:** „Sie planen eine Pfad-Implementierung auf Basis einer RCT. Welche Validitäts-Frage müssen Sie sich vor der Implementierung stellen?" – externe Validität / Übertragbarkeit.

**Diskussionsfrage:** Warum ist die Spannung zwischen interner und externer Validität fundamental? – Methodisch sauberere Studien sind oft enger im Einschluss → weniger Generalisierbarkeit. Pragmatische Studien sind breiter, aber durch Confounding bedrohter. Beide Studienformen sind komplementär.

**Mögliche Anschlussfragen:**
- Welche Bias-Typen bedrohen die interne Validität?
- Welche Faktoren bestimmen die externe Validität?
- Gibt es einen Trade-off zwischen beiden?

## Verwandt

- [[BPM - Bias - Definition]]
- [[BPM - Confounder - Definition]]
- [[BPM - Confounder-Kontrolle - Methoden]]
- [[BPM - Studiendesign - RCT Goldstandard]]
- [[BPM - VL - Erstellung von Leitlinien]]

## Quelle

- Vorlesung: [[BPM - VL - Evidenzbasierte Medizin]]
- Folien/Seitenangabe: Folien 21 (Interne Validität), 31 (Externe Validität)
- Externe Quelle laut Folien: Cochrane Deutschland & AWMF, *Risk-of-Bias-Manual* 2016.
