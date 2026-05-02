---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - CMMI - Reifegradmodell

> [!info] Kurzdefinition
> CMMI (Capability Maturity Model Integration) ist ein Reifegradmodell mit fünf Stufen, das den Reifegrad von Prozessen einer Organisation beschreibt: Initial → Gemanagt → Definiert → Quantitativ gemanagt → Optimierend. Höhere Stufen bedeuten standardisiertere, messbarere und kontinuierlich verbesserte Prozesse.

## Beschreibung

Folie 33 zeigt das Modell als ansteigende Treppe. Quelle: „Eine Management Guide. Service Transition basierend auf ITIL V3" (Folie 33).

Die fünf Stufen mit den Folientexten:

1. **Initial** — Prozesse sind ad-hoc und chaotisch.
2. **Gemanagt** — Organisation gewährleistet, dass die Prozesse gemäß den Grundsätzen geplant und durchgeführt werden.
3. **Definiert** — Prozesse sind charakterisiert und verstanden und werden in Standards, Verfahren, Werkzeugen und Methoden beschrieben.
4. **Quantitativ gemanagt** — Die Organisation und die Projekte etablieren quantitative Ziele für Qualitäts- und Prozessleistung und nutzen diese als Kriterien im Rahmen des Prozessmanagements.
5. **Optimierend** — Fokussiert auf kontinuierlicher Verbesserung der Prozessleistung durch inkrementelle und innovative Prozess- und Technologieverbesserungen.

CMMI ist im Foliensatz innerhalb der Servicelebenszyklus-Sektion eingeordnet — als Werkzeug, mit dem man den Reifegrad eines ITSM-Prozesses (etwa Incident Management, Change Management) bewerten kann.

## Bestandteile / Aufbau

| Stufe | Bezeichnung | Charakter |
|---|---|---|
| 1 | Initial | Ad-hoc, chaotisch, personenabhängig |
| 2 | Gemanagt | Geplant und gemäß Grundsätzen durchgeführt |
| 3 | Definiert | Standardisiert, dokumentiert in Verfahren/Werkzeugen/Methoden |
| 4 | Quantitativ gemanagt | Mit messbaren Qualitäts- und Leistungszielen |
| 5 | Optimierend | Kontinuierliche, inkrementelle und innovative Verbesserung |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Beispiel Incident Management:

- **Initial:** Tickets werden per E-Mail entgegengenommen, jeder Mitarbeiter arbeitet anders.
- **Gemanagt:** Es gibt einen Incident-Prozess, der eingehalten wird.
- **Definiert:** Incident-Management-Prozess ist im Tool abgebildet, Klassifikation und Priorisierung stehen in einem Handbuch.
- **Quantitativ gemanagt:** SLAs mit Lösungszeiten, monatliche Reports, KPIs (z. B. Ø Lösungszeit, First-Call-Resolution-Rate) werden verfolgt.
- **Optimierend:** Trendanalysen, KI-Unterstützung bei Klassifikation (siehe [[SM - Fallstudie - KI Incident Management]]), kontinuierliche Prozessverbesserung.

## Abgrenzung

- **CMMI vs. ITIL CSI** (siehe [[SM - ITIL Continual Improvement - Modell]]): CMMI ist eine *Bewertungsmethode* für den Ist-Zustand; CSI ist ein *Verbesserungsmodell*. Beide ergänzen sich: CMMI sagt „Wo stehen wir?", CSI sagt „Wie kommen wir weiter?".
- **CMMI vs. ISO 20000:** CMMI ist ein Reifegradmodell; ISO 20000 ein Standard mit Anforderungen. Reifegrade können auch nach ISO 20000 Auditkriterien bewertet werden — *im PDF nicht ausgearbeitet*.
- **CMMI vs. KPI-Framework:** CMMI bewertet Prozessreife; KPIs messen einzelne Service-Levels. Erst Stufe 4 (Quantitativ gemanagt) verlangt KPIs.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche fünf CMMI-Reifegrade gibt es? — Initial, Gemanagt, Definiert, Quantitativ gemanagt, Optimierend.

**Anwendungsfrage:** Ordnen Sie eine konkrete IT-Organisation einer CMMI-Stufe zu — z. B. „Die IT hat einen Incident-Prozess, dieser wird per Tool abgebildet, KPIs werden monatlich gemessen." → Stufe 4 Quantitativ gemanagt.

**Diskussionsfrage:** Welche Stufe ist realistisch erreichbar für eine durchschnittliche Krankenhaus-IT? Was hindert Organisationen daran, höhere Stufen zu erreichen? — Typischerweise scheitert es nicht an Tools, sondern an konsequenter Datenerhebung (Stufe 4) und Kultur der kontinuierlichen Verbesserung (Stufe 5).

**Mögliche Anschlussfragen:**
- Wie unterscheidet sich CMMI von der CMMI-Variante CMMI-SVC (für Services)? *(im Foliensatz nicht thematisiert)*
- Welche Beziehung besteht zwischen CMMI und ITIL? — Beide sind Best-Practice-Ansätze; CMMI bewertet Prozessreife, ITIL definiert Praktiken.
- Warum wird Reifegradmodell als Methode in ITIL CSI genannt (siehe [[SM - ITIL Continual Improvement - Modell]])?

## Verwandt

- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - SWOT-Analyse]]
- [[SM - ITIL 4 - Service Value System]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 33; Quelle: „Eine Management Guide. Service Transition basierend auf ITIL V3"

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
