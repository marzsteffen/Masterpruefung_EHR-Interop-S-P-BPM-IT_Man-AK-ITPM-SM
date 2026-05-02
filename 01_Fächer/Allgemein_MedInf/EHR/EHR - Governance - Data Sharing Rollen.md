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

# EHR - Governance - Data Sharing Rollen

> [!info] Kurzdefinition
> Rollenmodell für Datensharing nach Metsallik: getrennte Verantwortlichkeiten für **Erfassung** (Capture/Provider), **Verwahrung** (Custodian), **Lieferung** (Delivery), **Konsum** (Consumer) sowie übergreifende Steuerungsrollen (Data Steward, Policy Owner, Policy Controller).

## Beschreibung

Folie „Governance concepts of data sharing" zeigt eine Architektur mit explizit getrennten Rollen entlang des Datenlebenszyklus. Damit ist Daten-Mehrfachnutzung möglich, weil Erfassung und Nutzung entkoppelt sind.

## Bestandteile / Aufbau

| Rolle | Verantwortlichkeit |
|---|---|
| **Data Policy Owner** | Setzt die Datenpolitik fest (oberste Steuerungsebene) |
| **Data Steward** | Verwaltet die Bedeutung und Qualität der Daten – die VL fragt explizit, ob es treffender „Knowledge Steward" wäre |
| **Data Demands** ↔ **Information Needs** | Linke und rechte Seite des Bedarfs – Data Demand vom Provider aus, Information Need vom Consumer aus |
| **Data Provider** | Stellt Daten zur Verfügung |
| **Data Capture** | Erfasst Daten |
| **Data Custodian** | Verwaltet Daten dauerhaft (Custody = Verwahrung) |
| **Data Delivery** | Liefert Daten an Konsumenten aus |
| **Data Consumer** | Nutzt Daten |
| **Data Usability** | Querschnittsfunktion, die für die Nutzbarkeit (Qualität, Format, Interpretierbarkeit) sorgt |
| **Data Policy Controller** | Überwacht die Einhaltung der Datenpolitik (oberste Kontrollebene) |

## Beispiel

Aus dem PDF-Beispiel „Vaccination":
- **Data Capture:** Computer Log, Paper Log, Patient Summary, Vaccination Passport, Vaccination Certificate, Patient Consent, Eligibility Request, Reimbursement Claim, Monthly Report, Quarterly Report, Vaccination Registry, Service Quality Report, Case Report Form
- **Data Custody:** EMR, Paper Records, EHR, Personal Records, Insurance, Public Health, Vaccination Reg, Accreditation Reg, Research Records
- **Information Use:** Clinical, Personal, Funding, Policy, Management, Scientific

Die Folien-Notiz zu diesem Beispiel: „don't do like this!" – das gezeigte Modell hat zu viele unterschiedliche Capture-Pfade für eigentlich gleiche Information.

## Abgrenzung

- Data Steward ≠ Data Custodian: Steward kümmert sich um Bedeutung/Qualität, Custodian um Speicherung/Verwahrung.
- Data Provider ≠ Data Capture: Provider ist die Organisation, Capture ist der Akt der Erfassung.
- Data Consumer ≠ Data Subject (= Patient, Person, deren Daten erfasst werden – nicht in dieser Folie thematisiert).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Rollen unterscheidet das Datensharing-Governance-Modell, und warum die Trennung?

**Anwendungsfrage:** Wer ist im ELGA-Kontext Data Custodian, wer Data Steward?

**Diskussionsfrage:** Warum ist die Trennung zwischen Erfassung und Verwahrung kritisch für Daten-Mehrfachnutzung? Was passiert ohne sie?

**Mögliche Anschlussfragen:**
- Wer übernimmt die Rolle des Data Stewards in einem Krankenhaus-HIS?
- Wie verhält sich diese Governance zu DSGVO-Rollen (Verantwortlicher, Auftragsverarbeiter)?
- Was bedeutet „Knowledge Steward" gegenüber Data Steward?
- Wie verbindet sich diese Rollenarchitektur mit den Logic Modes des Datenteilens?

## Verwandt

- [[EHR - Datensharing - Logic Modes]]
- [[EHR - ContSys - ISO 13940]]
- [[EHR - Maturity Model - MITRE HISCF]]
- [[ASP - DSGVO Rollen]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folien „Governance concepts of data sharing", „An example of health data sharing implementation (don't do like this!)"

## Ergänzung außerhalb der Vorlesung

**Data Steward vs. Knowledge Steward** – die rhetorische Frage in der Folie löst Metsallik bewusst nicht auf, weil sie auf einen unterschiedlichen Verantwortungs­bereich zielt:

- **Data Steward:** operative Verantwortung für **Daten als Asset** – Datenqualität, Datenstandards, Metadaten-Pflege, Datendefinitionen, Lineage, Master-Data-Konsistenz. Fokus liegt auf einzelnen Datenfeldern und -strukturen (z. B. „ist `body_weight` in kg oder lb? wer darf den Wert ändern?").
- **Knowledge Steward:** konzeptuelle Verantwortung für **Wissen als Asset** – inhaltliche Bedeutung, Zusammenhang zu klinischen Pathways, Guidelines, Decision-Support-Logik, Ontologie-Pflege (z. B. ContSys, SNOMED-Subsets). Fokus liegt darauf, wie Daten in Versorgungs- und Entscheidungs­prozessen interpretiert werden („was bedeutet das Body-Weight-Trend für den CarePlan eines Adipositas-Patienten?").

**Warum die Frage relevant ist:** Reine Data Stewardship reicht im Gesundheitswesen oft nicht, weil Daten ohne klinischen Kontext nicht entscheidungs­fähig sind. Wer dafür sorgt, dass `Observation.code = LOINC 29463-7` korrekt befüllt ist, ist Data Steward. Wer dafür sorgt, dass dieses Datenfeld richtig in einem Adipositas-Pathway nach ISO 13940 verstanden wird, ist Knowledge Steward.

**Praktische Einordnung:** In den meisten realen Organisationen werden beide Rollen nicht getrennt besetzt – die Folie macht den Mangel sichtbar. In reifen Architekturen (informational mode, ISO 13940 als ontologisches Backbone) wird die Knowledge-Stewardship-Funktion explizit zugewiesen, oft an klinisch-fachliche Stellen, nicht an die IT.
