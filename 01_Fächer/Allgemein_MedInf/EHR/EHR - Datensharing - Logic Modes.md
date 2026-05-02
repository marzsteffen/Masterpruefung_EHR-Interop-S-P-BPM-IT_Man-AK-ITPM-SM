---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Macro-Level Interoperabilität]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Datensharing - Logic Modes

> [!info] Kurzdefinition
> Drei Modi des Datenteilens nach Reifegrad: **transactional** (bilateral, ad hoc), **shared registries** (zentrale Sammlung in starren Strukturen) und **informational** (vielfältige, dynamische Mehrfachnutzung). Letzteres ist das vom Vortrag intendierte Zielmodell.

## Beschreibung

Folie „Logic of Data Sharing" stellt die drei Modi entlang von vier Bewertungsachsen gegenüber: Governance, Ecosystem agility, Data use for multipurpose, Data Standards.

## Bestandteile / Aufbau

| Modus | Governance | Ecosystem agility | Data use for multipurpose | Data Standards |
|---|---|---|---|---|
| **Informational** (vision/expectation – intendiertes Modell) | Diverse (confederate, matrix) | High | Fundamental | Dynamic |
| **Shared registries** (state-of-art) | Monopoly, Fragmented, Federative | Low | Static | Central |
| **Transactional** (common) | Bilateral, Multilateral | Moderate | Secondary | Contractual |

## Beispiel

- **Transactional:** Krankenhaus A schickt Befund per HL7 v2 an Krankenhaus B, basierend auf bilateralem Vertrag.
- **Shared registries:** Eine nationale Impfregistrierung, die alle Versorger einheitlich befüllen müssen, mit zentraler Festlegung von Format und Inhalt.
- **Informational:** EHDS-ähnliches Ökosystem, in dem Daten für klinische Entscheidung, Research, Policy und Funding aus denselben Quellen flexibel und unter dynamischen Standards nutzbar sind.

Das PDF betont, dass die Realität meistens beim Modus **transactional** verharrt – mit dem Kommentar „common" (gängig, nicht angestrebt).

## Abgrenzung

- Kein technisches Modell, sondern eine **Governance-Typologie**.
- Verbunden mit Tolks LCIM ([[EHR - Interoperabilität - LCIM nach Tolk]]): Process Composability ist nur im informational mode wirklich erreichbar.
- Verwandt mit der „Findings"-Folie aus dem PDF: „Still lots of point-to-point data exchange" – das ist transactional mode.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Modi des Datenteilens unterscheidet die Vorlesung, und welche Bewertungsachsen werden angelegt?

**Anwendungsfrage:** In welchem Modus operiert ELGA aktuell – und welcher Modus wäre der Zielzustand?

**Diskussionsfrage:** Warum ist „dynamic standards" Voraussetzung für „fundamental multipurpose"? Was bedeutet „dynamic" hier konkret?

**Mögliche Anschlussfragen:**
- Was ist „secondary use" von Daten? (Antwort: Nutzung über den ursprünglichen Erfassungs­zweck hinaus, z. B. Forschung, Policy)
- Welche Governance-Strukturen ermöglichen den informational mode?
- Wie verhält sich „shared registries" zu Repository vs. Registry ([[EHR - Architektur - Registry vs Repository]])?

## Verwandt

- [[EHR - Interoperabilität - LCIM nach Tolk]]
- [[EHR - Governance - Data Sharing Rollen]]
- [[EHR - eHealth Capabilities - Information Flows]]
- [[EHR - Architektur - Registry vs Repository]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folien „Logic of Data Sharing", „Findings: Still lots of point-to-point data exchange"
