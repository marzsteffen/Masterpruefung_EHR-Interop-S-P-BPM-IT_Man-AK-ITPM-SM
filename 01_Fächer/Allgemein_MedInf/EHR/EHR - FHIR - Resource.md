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

# EHR - FHIR - Resource

> [!info] Kurzdefinition
> Eine **Resource** ist die kleinste atomare Einheit des FHIR-Datenmodells – eine in sich geschlossene Beschreibung eines „Things" wie Patient, Observation, MedicationRequest, Practitioner. „Resources sind die Atome des Health-Information-Exchange."

## Beschreibung

Aus den Folien:

> „In FHIR, almost everything is a 'resource' – Term from the semantic web world.
> A basic unit, describing a 'thing' – 'Patient', 'Prescription', 'Device'.
> FHIR tries to keep the number of 'resources' limited – Differentiation through attributes / coding."

> „FHIR Resources can be thought of as the 'atoms' of health information exchange. Smallest unit of exchange."

Die offizielle Resource-Liste ist unter https://www.hl7.org/fhir/resourcelist.html.

## Bestandteile / Aufbau

Eine Resource hat:
- **`resourceType`-Feld** (immer Pflicht; identifiziert den Resource-Typ, z. B. „Patient")
- **Data Elements** (Felder mit Cardinality, Data Type, Definition)
- Optional: **id**, **meta** (Versions-Info, Profile-Referenzen, Tags)

Beispiel-Datenelemente einer Patient-Resource: `identifier`, `active`, `name`, `gender`, `birthDate`, `address`, `telecom`.

## Beispiel

Eine minimale FHIR Patient Resource (JSON):

```json
{
  "resourceType": "Patient",
  "id": "example-1",
  "active": true,
  "name": [
    {
      "family": "Mustermann",
      "given": ["Max"]
    }
  ],
  "gender": "male",
  "birthDate": "1980-05-15"
}
```

Diese Resource ist eine **vollständige, in sich geschlossene Repräsentation** dieses Patienten und kann via REST-API abgerufen, erstellt, aktualisiert und gelöscht werden.

## Abgrenzung

- **Resource ≠ Bundle:** Eine Bundle ist ein Container für mehrere Resources.
- **Resource ≠ Document:** Ein Document ist eine spezielle Bundle mit Composition als Root-Resource.
- **Resource ≠ Profile:** Eine Resource ist die Basis-Definition; Profile schränken/erweitern eine Resource für lokale Use-Cases.
- FHIR hält die Anzahl der Resource-Typen **bewusst begrenzt** (~150) – Variation läuft über Attribute und Coding.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine FHIR-Resource? Nenne 5 Beispiele.

**Anwendungsfrage:** Wie würdest du einen Patienten mit Diabetes-Diagnose und Metformin-Verschreibung in FHIR-Resources zerlegen? (Antwort: Patient + Condition + MedicationRequest)

**Diskussionsfrage:** „Almost everything is a resource" – wo liegt die Grenze? Was ist explizit **kein** Resource (Antwort: Datatypes, Profiles, Extensions, Search Parameters – sie sind Bestandteile, aber keine Resources im Sinne der REST-API)?

**Mögliche Anschlussfragen:**
- Wo findet man die Resource-Liste? (hl7.org/fhir/resourcelist.html)
- Warum heißt die Resource für Krankheiten **nicht** „Disease", sondern „Condition"?
- Welche Felder hat ein Patient mindestens?
- Wie unterscheidet sich „Resource" in FHIR vom Resource-Begriff im Semantic Web?

## Verwandt

- [[EHR - FHIR - Resource Kategorien]]
- [[EHR - FHIR - Data Types und Cardinality]]
- [[EHR - FHIR - Resource Granularität]]
- [[EHR - FHIR - References]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[MSI - HL7 FHIR - Resource]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 7–13 (Resources, Beispiel Patient, Resource-Liste)
