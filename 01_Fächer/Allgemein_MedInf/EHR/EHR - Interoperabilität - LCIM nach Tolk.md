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

# EHR - Interoperabilität - LCIM nach Tolk

> [!info] Kurzdefinition
> Levels of Conceptual Interoperability Model (LCIM, Tolk 2003 / 2013): Schichtung von Interoperabilität in **Technical Integration → Syntax & Semantics → Process Composability**. Gibt einen Reifegrad an, in dem Systeme nicht nur Daten austauschen, sondern auch in Bedeutung und Prozess übereinstimmen.

## Beschreibung

Quellen laut Folie:
- A. Tolk, „Levels of Conceptual Interoperability", 2003 Fall Simulation Interoperability Workshop.
- A. Tolk, L. J. Bair, S. Y. Diallo, „Supporting Network Enabled Capability by extending the Levels of Conceptual Interoperability Model to an interoperability maturity model", J. of Defense Modeling & Simulation, 10(2), 2013.

Die Vorlesung präsentiert drei zentrale Schichten und konkretisiert sie an Martins Daten:

## Bestandteile / Aufbau

| Schicht | Frage | Inhalt |
|---|---|---|
| **Technical Integration** | „Where is body weight data?" | Quellen sind in Computernetzen verbunden und teilen Daten sicher → „data in the right location" |
| **Syntax and Semantics** | „What is body weight?" | Daten sind an gemeinsame Terminologien und Master Data gebunden → „data content fits the decision-algorithms" |
| **Process Composability** | „Who and when records a weight?" | Datenflüsse erfüllen die Bedürfnisse nachgelagerter Entscheidungsfindung → „data is timely and actionable" |

## Beispiel

Martins Beispiele aus der Folie:
- **Technical Integration:** Ohne Integration muss Martin selbst alle Datenquellen aufsuchen und manuell konsistent halten.
- **Syntax & Semantics:** Identifier, Body Weight, Age, Sex haben gemeinsame Bedeutung. **Family History, Lifestyle, Health Goals** sind unstrukturiert und brauchen menschliche Interpretation.
- **Process Composability:** Martin müsste seine Familienanamnese erneut erfassen; sein Smoking-Status ist für Public-Health-Forschung erneut zu erheben.

## Abgrenzung

- LCIM ist eine **konzeptuelle Schichtung**, kein konkreter Standard. Erfüllung jeder Schicht erfordert verschiedene Bausteine: HL7 v2/FHIR (Syntax), SNOMED/LOINC/ICD (Semantik), ISO 13940 ContSys (Process).
- LCIM ≠ ISO/OSI-Modell (das ist die rein technische Netzwerkschichtung).
- LCIM ist allgemein für Simulations-Interoperabilität entwickelt, im Health-Kontext adaptiert. Im Health-IT-Diskurs konkurriert LCIM mit anderen Modellen wie ReEIF (Refined eHealth European Interoperability Framework).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Schichten unterscheidet LCIM?

**Anwendungsfrage:** Auf welcher Schicht scheitert ein typischer Datenaustausch zwischen einem niedergelassenen Arzt und einem Krankenhaus heute? Beispiel diskutieren.

**Diskussionsfrage:** Process Composability ist die schwierigste Schicht – warum? Welche Standards adressieren sie überhaupt?

**Mögliche Anschlussfragen:**
- Wie verteilen sich FHIR, SNOMED, ICD, ATC, LOINC, ISO 13940 auf die drei Schichten?
- Was unterscheidet Syntax von Semantik konkret?
- Welche Schicht ist in ELGA am stärksten ausgebaut?
- Welche Verbindung sieht Tolk zwischen LCIM und Maturity Models?

## Verwandt

- [[EHR - ContSys - ISO 13940]]
- [[EHR - HL7 FHIR - 5 Levels]]
- [[EHR - Datensharing - Logic Modes]]
- [[MSI - SNOMED CT]]
- [[MSI - LOINC]]
- [[MSI - HL7 FHIR]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folien „Can Martin share his personal records with a physician?", „Interoperability of the health data", „Levels of interoperability"
