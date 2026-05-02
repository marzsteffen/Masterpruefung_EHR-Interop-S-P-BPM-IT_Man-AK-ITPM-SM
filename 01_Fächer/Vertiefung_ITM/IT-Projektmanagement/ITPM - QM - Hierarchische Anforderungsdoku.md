---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Qualitätsmanagement]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - QM - Hierarchische Anforderungsdoku

> [!info] Kurzdefinition
> Anforderungsdokumentation lässt sich hierarchisch strukturieren: **Business Vision → Kundenanforderungen / Stakeholder Requirements → System- und Software Requirements → Component Requirements**. Jede Ebene wird aus der darüberliegenden abgeleitet.

## Beschreibung

Aus Folie 25:

Folgende Punkte sollten in der Anforderungsdokumentation enthalten sein:

## Bestandteile / Aufbau

| Ebene | Inhalt |
|---|---|
| **Business Vision** | Was will der Kunde wie erreichen? Repräsentiert den **Kundennutzen** der Applikation. **Rechtfertigt die Investition.** |
| **Kundenanforderung / Stakeholder Requirements** | Beschreiben die **fachlichen Anforderungen** der Kunden (im Sinne der Quality in Use). |
| **System- und/oder Software Requirements** | Definieren die Anforderungen an das **Softwareprodukt**. |
| **Component Requirements** | Definieren die Anforderungen an **einzelne Komponenten** der Lösung. |

## Beispiel

*Im PDF nicht durch konkretes Anforderungs-Hierarchie-Beispiel illustriert.*

## Abgrenzung

- **Business Vision** ≠ **Stakeholder Requirements:** Vision ist abstrakt-strategisch, Stakeholder Requirements konkret-fachlich.
- **Stakeholder Requirements** = **Quality in Use** (Anwender-/Kontextsicht).
- **System/SW Requirements** = **Product Quality** (technische Sicht).
- **Component Requirements** = **technische Detail-Ebene** (Module, Microservices).

Verbindung zu agilen Pendants: Vision = **Produktvision** ([[ITPM - Scrum - Artefakte]]), Stakeholder/SW Requirements = **Product Backlog Items / User Stories**.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Ebenen umfasst die hierarchische Anforderungsdokumentation, und welche Frage beantwortet die Business Vision?

**Anwendungsfrage:** Strukturieren Sie eine Anforderung „Patient kann Befunde digital einsehen" über alle vier Ebenen.

**Diskussionsfrage:** Welche Probleme entstehen, wenn man Ebenen überspringt (z. B. direkt von Vision zu Component Requirements)?

**Mögliche Anschlussfragen:**
- Wie verhält sich diese Hierarchie zum Lastenheft/Pflichtenheft?
- Wie übersetzt man die Hierarchie in agile Strukturen (Epic, Feature, Story, Task)?
- Welche Verbindung zu Quality in Use vs. Product Quality?

## Verwandt

- [[ITPM - Qualitätsplanung]]
- [[ITPM - Critical Qualities]]
- [[ITPM - Quality in Use vs Product Quality]]
- [[ITPM - Lastenheft]]
- [[ITPM - Pflichtenheft]]
- [[ITPM - Scrum - Artefakte]]
- [[ITPM - Agile - User Story]]

## Quelle

- Vorlesung: [[ITPM - VL - Qualitätsmanagement]]
- Folien/Seitenangabe: 25
