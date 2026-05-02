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

# EHR - HL7 FHIR - 5 Levels

> [!info] Kurzdefinition
> Schichtmodell der HL7-FHIR-Spezifikation (laut hl7.org/fhir): **Level 1 Foundation → Level 2 Conformance → Level 3 Master Data → Level 4 Operational Data → Level 5 Knowledge**. Macht sichtbar, dass FHIR mehr ist als ein Austauschformat – es deckt von Encoding bis Wissens-Sharing alles ab.

## Beschreibung

Die Vorlesung übernimmt das offizielle 5-Level-Modell von hl7.org/fhir.

## Bestandteile / Aufbau

| Level | Inhalt laut Folie |
|---|---|
| **Level 1 – Foundation** | Technologien zum Encoding von Daten in digitale Formate; Datentypen und Basisstrukturen für die Nutzung in Computernetzen |
| **Level 2 – Conformance** | Regeln und Strukturen für Metadaten; Daten zu Security, Conformance, Terminologie und Exchange-Features eines Health Data Space |
| **Level 3 – Master Data** | Regeln und Strukturen für Stammdaten-Management; Verlinkung von Records zu Personen, Organisationen, Geräten, Locations, Services |
| **Level 4 – Operational Data** | Regeln und Strukturen für operative Daten: klinische Events, Diagnostik, Medikation, Workflow, Finanz-Events |
| **Level 5 – Knowledge** | Regeln und Strukturen für Wissens-Daten; digitales Knowledge Sharing erlaubt schnelles Update klinischer Algorithmen und Medikations-Guidance |

## Beispiel

- **Level 1:** Wie wird ein Patient als JSON oder XML codiert?
- **Level 2:** CapabilityStatement (welche Operationen unterstützt ein FHIR-Server?), SecurityLabels, ValueSet-Bindings.
- **Level 3:** Patient, Practitioner, Organization, Device, Location – die „Wer-Wo-Was"-Stammdaten.
- **Level 4:** Observation, Condition, MedicationRequest, Encounter – die operativen Versorgungs-Events.
- **Level 5:** ClinicalReasoning-Module wie PlanDefinition, ActivityDefinition, Library – mit denen sich CDS-Regeln und Pathways teilen lassen.

## Abgrenzung

- Die 5 FHIR-Level adressieren **inhaltliche Schichten der Spezifikation**, nicht Versorgungsebenen wie Macro/Meso/Micro ([[EHR - Integrated Care - Macro Meso Micro Level]]).
- Auch nicht zu verwechseln mit den [[EHR - Interoperabilität - LCIM nach Tolk]]-Schichten – LCIM beschreibt allgemeine Interoperabilität, FHIR-Level beschreiben den Aufbau eines konkreten Standards.
- Höhere Level setzen niedrigere voraus: ohne Level 1 Foundation keine Level 5 Knowledge-Daten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche fünf Levels unterscheidet HL7 FHIR, und welcher Level adressiert was?

**Anwendungsfrage:** Auf welchem Level liegen typische FHIR-Resourcen wie Patient, Observation, MedicationRequest, PlanDefinition?

**Diskussionsfrage:** Welche Levels werden in produktiven österreichischen FHIR-Implementierungen heute genutzt – und welche bleiben oft brach (Hinweis: Level 5 / Knowledge ist in der Praxis selten produktiv im Einsatz)?

**Mögliche Anschlussfragen:**
- Was bedeutet „Conformance" konkret in FHIR (Stichwort: CapabilityStatement, StructureDefinition, Profile)?
- Was sind typische Level-5-Resourcen?
- Wie verhält sich das 5-Level-Modell zu den FHIR Maturity Levels einzelner Resourcen?

## Verwandt

- [[EHR - Interoperabilität - LCIM nach Tolk]]
- [[EHR - VL - FHIR Grundlagen]]
- [[MSI - HL7 FHIR]]
- [[MSI - HL7 FHIR - Resource]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folie „HL7 FHIR Levels" (mit Verweis auf hl7.org/fhir)
