---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - FHIR Grundlagen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - FHIR - Resource Kategorien

> [!info] Kurzdefinition
> FHIR-Resources sind in Hauptkategorien gruppiert: **Foundation** (Infrastruktur), **Base** (Stammdaten wie Patient, Practitioner), **Clinical** (Versorgungsinhalte wie Condition, Medication), **Financial** (Abrechnung), **Specialized** (z. B. Forschung).

## Beschreibung

Aus Folie 29 („Main Categories of FHIR resources"):

| Kategorie | Beispiele |
|---|---|
| **Foundation** | ValueSet, Composition, MessageHeader |
| **Base** | Patient, Practitioner, Encounter |
| **Clinical** | Condition, Medication, Specimen |
| **Financial** | Claim, Contract |
| **Specialized** | ResearchSubject |

## Bestandteile / Aufbau

### Foundation (Infrastruktur)
Resources, die die FHIR-Mechanik selbst tragen: Conformance (CapabilityStatement, StructureDefinition), Terminologie (ValueSet, CodeSystem), Bundles und Document-Container (Composition, MessageHeader).

### Base (Stammdaten / Master Data)
Resources, die Personen, Organisationen, Geräte und Encounters identifizieren: Patient, Practitioner, PractitionerRole, Organization, Location, Device, Encounter.

### Clinical (Versorgungsinhalte)
Resources, die klinische Versorgungs-Aktivitäten und -Befunde abbilden: Condition (Diagnose), Observation (Messungen, Befunde), MedicationRequest, Procedure, AllergyIntolerance, CarePlan, Specimen.

### Financial (Abrechnung)
Resources für Claims, Coverage, Contracts.

### Specialized (Spezielle Anwendungs­domänen)
ResearchStudy, ResearchSubject (klinische Forschung), MeasureReport, EvidenceVariable.

### Bezug zu HL7 FHIR 5 Levels

Die Kategorien korrespondieren grob mit den FHIR-Inhaltsschichten ([[EHR - HL7 FHIR - 5 Levels]]):

| FHIR-Level | Kategorie |
|---|---|
| Level 1 Foundation | Foundation |
| Level 2 Conformance | Foundation |
| Level 3 Master Data | Base |
| Level 4 Operational Data | Clinical, Financial |
| Level 5 Knowledge | Specialized + Foundation (PlanDefinition etc.) |

## Beispiel

Diabetes-Patient in FHIR-Resources:
- **Base:** Patient (Steffen), Practitioner (Hausarzt), Organization (Hausarztpraxis)
- **Clinical:** Condition (Diabetes Typ 2), Observation (HbA1c-Wert), MedicationRequest (Metformin), AllergyIntolerance (Penicillin)
- **Financial:** Claim (Abrechnung der Visite)
- **Foundation:** Composition (Sammelt alles in einem Document Bundle)

## Abgrenzung

- Die Kategorien sind **konzeptuell**, nicht hierarchisch zwingend – ein Resource gehört zu einer Kategorie, hat aber eigenständige Definition.
- Manche Resources sind **Crossover** (z. B. CarePlan: Clinical, aber nutzt Knowledge-Concepts wie PlanDefinition).
- Vorsicht: Im FHIR-Standard heißt die oberste Hauptgruppe „Conformance" – das überschneidet sich mit FHIR-Level-2 ([[EHR - HL7 FHIR - 5 Levels]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Hauptkategorien von FHIR-Resources gibt es? Nenne pro Kategorie 1–2 Beispiele.

**Anwendungsfrage:** Welche Resources würdest du für eine Forschungsstudie auswählen? (Antwort: ResearchStudy, ResearchSubject + zugehörige Patient/Observation/Condition)

**Diskussionsfrage:** Warum ist die Trennung zwischen Base und Clinical sinnvoll? Welche Wartungs- und Stabilitätsfragen hängen davon ab?

**Mögliche Anschlussfragen:**
- Welche Kategorie ist am stabilsten in der FHIR-Spezifikation? (Antwort: Foundation und Base sind typischerweise am stabilsten / FMM-höchsten)
- Wie hängen Resource-Kategorien mit FHIR Maturity Levels (FMM 0-5) zusammen?
- Was ist der Unterschied zwischen Medication und MedicationRequest?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - HL7 FHIR - 5 Levels]]
- [[EHR - FHIR - Resource Granularität]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folie 29 (Main Categories of FHIR resources)
