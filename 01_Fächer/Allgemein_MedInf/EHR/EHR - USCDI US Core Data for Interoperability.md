---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Meaningful Use]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - USCDI US Core Data for Interoperability

> [!info] Kurzdefinition
> **USCDI** (United States Core Data for Interoperability) ist ein vom **ONC** definiertes, **standardisiertes Mindest-Datenset** für Gesundheits­datenaustausch in den USA. Das Set wird jährlich erweitert (V1, V2, V3+) und ist die technische Grundlage moderner US-EHR-Interoperabilität – als Erbe von Meaningful Use.

## Beschreibung

Aus Folie 45:

> „United States Core Data for Interoperability (USCDI) – 'US Core'.
> Version 1 versus Version 2 and Draft Version 3."

USCDI ist eine Liste von **Datenklassen und Datenelementen**, die zertifizierte EHRs unterstützen müssen. Die Liste wächst jährlich; Hersteller müssen die jeweils aktuellen Versionen unterstützen. Verlinkt mit HL7 FHIR via das Profil-Set **„US Core"**.

## Bestandteile / Aufbau

USCDI gliedert sich in **Datenklassen** mit einzelnen **Datenelementen**. Beispiele für Datenklassen (im PDF nicht enumeriert; ergänzt aus dem ONC-Standard):

- Patient Demographics (Name, Birth Date, Sex)
- Allergies and Intolerances
- Assessment and Plan of Treatment
- Care Team Members
- Clinical Notes
- Goals
- Health Concerns
- Immunizations
- Laboratory
- Medications
- Patient Demographics
- Problems
- Procedures
- Provenance
- Smoking Status
- Unique Device Identifiers (UDI) for Implantable Devices
- Vital Signs

Jede Klasse verweist auf konkrete Coding-Standards:
- LOINC – für Lab und Beobachtungen
- SNOMED CT – für klinische Konzepte
- RxNorm – für Medikamente
- ICD-10-CM – für Diagnosen
- UCUM – für Maßeinheiten

## Beispiel

Übungsaufgabe aus dem PDF:

> „Which standard(s) is (or are) required for coding of:
> - lab tests and results?
> - medications?
> - diagnoses?
> - units of measure?"

**Antworten** (eigene Erschließung aus USCDI-Mappings):
- Lab tests/results → **LOINC** (für Test-Identität), **SNOMED CT** oder **UCUM** (Werte/Einheiten)
- Medications → **RxNorm** (für Medikamenten-Identität), **NDC** (für Produkte)
- Diagnoses → **ICD-10-CM** (Coding) und/oder **SNOMED CT** (klinisch)
- Units of measure → **UCUM** (Unified Code for Units of Measure)

## Abgrenzung

- USCDI ≠ FHIR: USCDI definiert Inhalte, FHIR ist das Austausch-Format. „US Core" Profile sind die FHIR-Bindings für USCDI.
- USCDI ≠ HL7 CCDA: CCDA ist ein älteres Dokumenten­format; USCDI ist daten-element-orientiert.
- USCDI ist **nicht** statisch – jede Version (V1, V2, V3, ...) erweitert das Set. Hersteller müssen mitziehen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist USCDI, und welche Rolle spielt es in der US-Interoperabilität?

**Anwendungsfrage:** Welche Coding-Standards sind für Lab, Medikamente, Diagnosen und Maßeinheiten in USCDI vorgeschrieben?

**Diskussionsfrage:** Jährliche Erweiterung von USCDI – wie verhält sich das zu langfristig planenden EHR-Roadmaps der Hersteller? Welche Belastung für Interoperabilität entsteht durch ständige Versions­wechsel?

**Mögliche Anschlussfragen:**
- Wer ist ONC, und welche Rolle spielt diese Behörde? (Office of the National Coordinator for Health Information Technology, US Department of Health and Human Services)
- Was ist das HL7 FHIR „US Core"-Profil-Set?
- Wie verhält sich USCDI zum europäischen EHDS und seinen Datenkategorien?
- Welche neuen Datenklassen kamen zwischen V1 und V3 hinzu? (im PDF nicht ausgeführt)

## Verwandt

- [[EHR - VL - Meaningful Use]]
- [[EHR - HL7 FHIR - 5 Levels]]
- [[EHR - Standards - Unterstützte Coding Standards]]
- [[EHR - EHDS - European Health Data Space]]

## Quelle

- Vorlesung: [[EHR - VL - Meaningful Use]]
- Folien/Seitenangabe: Folie 45 („United States Core Data for Interoperability (USCDI)") + Übungsaufgabe
