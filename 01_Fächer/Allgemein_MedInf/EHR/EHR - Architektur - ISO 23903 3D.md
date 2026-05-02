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

# EHR - Architektur - ISO 23903 3D

> [!info] Kurzdefinition
> ISO 23903 ist eine **Interoperability and Integration Reference Architecture** für Health Informatics. Sie strukturiert Systeme entlang dreier Dimensionen: **Viewpoint**, **Components / Composition**, **Domains**.

## Beschreibung

Folie „Making Sense of eHealth 3D – ISO 23903":

> „ISO 23903 – Health informatics. Interoperability and integration reference architecture. Model and framework."

Die drei Dimensionen werden in der Folie als Cluster mit Inhalten benannt.

## Bestandteile / Aufbau

| Dimension | Inhalt laut Folie |
|---|---|
| **Viewpoint** | Requirements, organization, tools, technology |
| **Components / Composition** | Concepts, relations, details |
| **Domains** | Capability, purpose, provision, custody, consumption |

## Beispiel

Die fünf Domains korrespondieren auffällig mit Metsalliks Datensharing-Rollen-Modell (Capability/Purpose/Provision/Custody/Consumption ↔ Capabilities, Demands/Needs, Provider/Capture, Custodian, Consumer aus [[EHR - Governance - Data Sharing Rollen]]).

## Abgrenzung

- ISO 23903 ist eine **Referenzarchitektur**, kein Datenformat. Sie ist dafür da, andere Standards einzuordnen.
- Komplementär zu ContSys (ISO 13940): ContSys liefert die Konzepte, ISO 23903 liefert das Strukturraster zur Einordnung.
- ISO 23903 ≠ ISO 18308: 18308 ist Anforderungs­spezifikation, 23903 ist Architektur-Framework.
- **Versionsangabe:** Im PDF nicht angegeben. ISO 23903:2021 ist die international gültige Erst­publikation (Ergänzung außerhalb der Vorlesung).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Dimensionen unterscheidet ISO 23903?

**Anwendungsfrage:** Wie ordnet ISO 23903 das Verhältnis zwischen FHIR (Components), Clinical-Pathway-Tools (Viewpoint Tools) und Custody (Domain) ein?

**Diskussionsfrage:** Wozu braucht man eine Referenzarchitektur, wenn schon Standards wie HL7 FHIR und IHE existieren?

**Mögliche Anschlussfragen:**
- Wie verhält sich ISO 23903 zu Zachman? (Zachman ist Klassifikations-Framework, ISO 23903 ist Reference Architecture für Health speziell)
- Was sind die fünf Domains konkret in einem ELGA-Kontext?
- Was ist der Unterschied zwischen Capability und Purpose in dieser Architektur?

## Ergänzung außerhalb der Vorlesung

ISO 23903:2021 trägt den vollständigen Titel „Health informatics – Interoperability and integration reference architecture – Model and framework". Sie zielt darauf, die zahlreichen einzelnen Health-Informatics-Standards (HL7, IHE, openEHR, ContSys etc.) in einer übergeordneten Architektur einzuordnen, statt sie zu ersetzen.

## Verwandt

- [[EHR - ContSys - ISO 13940]]
- [[EHR - ISO 18308 - Anforderungsspezifikation]]
- [[EHR - Governance - Data Sharing Rollen]]
- [[EHR - Methodik - Zachman Framework]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folie „Making Sense of eHealth 3D – ISO 23903"
