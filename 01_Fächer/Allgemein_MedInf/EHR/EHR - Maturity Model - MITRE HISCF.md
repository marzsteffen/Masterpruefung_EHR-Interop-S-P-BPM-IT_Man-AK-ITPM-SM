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

# EHR - Maturity Model - MITRE HISCF

> [!info] Kurzdefinition
> **Health Information Sharing Capability Framework** der MITRE Health: Reifegrad-Modell für nationale eHealth-Architekturen mit **11 Capabilities × 6 Stakeholder-Purposes**. Bewertet Datenqualität, Transport, Security, Interoperabilität, Usability, Alignment, Participation, Consent, Data Governance, Stakeholder Governance und Sustainability.

## Beschreibung

Quelle laut Folie: „Health Information Sharing Maturity Model. MITRE Health. https://health.mitre.org/blog/health-information-sharing-maturity-model-2/".

Das Modell strukturiert sich in drei Cluster (Governance Alignment, Process Alignment, Technical Alignment) und bewertet jede der 11 Capabilities pro Stakeholder-Purpose auf einer Maturity-Skala (1–5: Projects, Experts, Standards, Performance, Optimizing).

## Bestandteile / Aufbau

**Drei Alignment-Cluster:**
- **Governance Alignment** – Stakeholder Governance, Sustainability Governance, Data Governance
- **Process Alignment** – „composability of information and action": Usability/Workflow, Activity Alignment, Participation, Consent & Privacy
- **Technical Alignment** – „interoperability and integration of data": Data Quality, Data Security, Data Transport, Data Interoperability

**11 Capabilities × 6 Stakeholder-Purposes (Maturity-Matrix laut PDF):**

| | 1 Empowering | 2 Clinical | 3 Management | 4 Research | 5 Policy | 6 Funding |
|---|---|---|---|---|---|---|
| 01 Data quality | 2 | 2 | 2 | 3 | 2 | 3 |
| 02 Data transport | 2 | 3 | 2 | 2 | 2 | 3 |
| 03 Data security | 4 | 4 | 4 | 4 | 4 | 4 |
| 04 Interoperability | 3 | 3 | 3 | 2 | 2 | 3 |
| 05 Usability | 3 | 3 | 3 | 3 | 2 | 3 |
| 06 Alignment | 2 | 3 | 3 | 3 | 2 | 2 |
| 07 Participation | 4 | 3 | 4 | 3 | 3 | 2 |
| 08 Consent | 3 | 3 | 3 | 3 | 2 | 2 |
| 09 Data governance | 3 | 3 | 2 | 2 | 2 | 2 |
| 10 Stakeholder governance | 2 | 3 | 3 | 2 | 2 | 2 |
| 11 Sustainability | 4 | 2 | 2 | 4 | 3 | 4 |

**Maturity-Stufen** (Folie „Improvement of the maturity"): Projects → Experts → Standards → Performance → Optimizing.

## Beispiel

Aus der Folie ablesbar:
- **Data Security** ist quer über alle Purposes auf Stufe 4 (gleichmäßig hoch).
- **Data Quality** verharrt fast überall auf Stufe 2.
- **Sustainability** ist sehr unterschiedlich (Funding 4, Clinical/Management 2).
- Insgesamt zeigt die Matrix: Sicherheit ist oft gut ausgebaut, aber Qualität, Governance und Stakeholder-Alignment hinken hinterher.

Die Matrix wurde 2020 erhoben, vermutlich für ein konkretes Land (vermutlich Estland, basierend auf Metsalliks Beispiel-Anchor – im PDF nicht eindeutig benannt).

## Abgrenzung

- HISCF ≠ HIMSS EMRAM (HIMSS-eigenes Reifegradmodell für Krankenhäuser). HISCF ist auf nationale Sharing-Capabilities ausgerichtet.
- HISCF ≠ MITRE Healthcare Maturity Model im Allgemeinen – ist ein konkretes Sub-Framework dieser Organisation.
- 6 Purposes ≠ 6 Akteure: Es geht um *Zwecke* der Datennutzung, nicht um Akteure.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche 11 Capabilities und welche 6 Stakeholder-Purposes unterscheidet das MITRE-Maturity-Modell?

**Anwendungsfrage:** Wo würdest du Österreich auf dieser Matrix einordnen? Welche Capabilities sind stark, welche schwach? (Antwort offen)

**Diskussionsfrage:** Warum ist Data Security oft auf hoher Reife, Data Quality oft niedrig? Welche Anreizstruktur ist verantwortlich?

**Mögliche Anschlussfragen:**
- Was bedeutet „Empowering" als Purpose – Empowerment wessen?
- Wie verhält sich diese Matrix zu den Logic Modes des Datenteilens?
- Welche Capability ist für CDS (Clinical Decision Support) am wichtigsten?
- Wie passt MITRE HISCF zu DSGVO, EHDS und anderen Regulierungen?

## Verwandt

- [[EHR - Datensharing - Logic Modes]]
- [[EHR - Governance - Data Sharing Rollen]]
- [[EHR - eHealth Capabilities - Information Flows]]
- [[EHR - EHDS - European Health Data Space]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folien „Health Information Sharing Capability FW", „Health Information Sharing Maturity Assessment 2020", „Improvement of the maturity"
