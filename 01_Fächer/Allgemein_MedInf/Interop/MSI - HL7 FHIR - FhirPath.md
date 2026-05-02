---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - FhirPath

> [!info] Kurzdefinition
> FhirPath ist eine Navigations- und Abfragesprache für FHIR-Ressourcen, spezifiziert unter `https://hl7.org/fhir/fhirpath.html`. Sie ermöglicht den programmatischen Zugriff auf einzelne Elemente innerhalb einer FHIR-Ressource.

## Beschreibung

Aus Seite 2:

- Specification: `https://hl7.org/fhir/fhirpath.html`
- Playground: `https://fhirpath-lab.com/FhirPath`

Weitere Inhalte (Definition, Syntax, Beispiele) wurden im PDF nicht ausgeführt – die Vorlesung verweist auf die externe Spezifikation und die Übungsaufgabe (HAPI-Übung, Aufgabe 7: „Evaluierung von FHIR Paths anhand einer Beispiel-Ressource").

## Bestandteile / Aufbau

Im PDF nicht definiert. Siehe externe Spezifikation: `https://hl7.org/fhir/fhirpath.html`

## Beispiel

Im PDF kein Beispiel angegeben. Für praktische Erprobung: Playground unter `https://fhirpath-lab.com/FhirPath`.

## Abgrenzung

- **FhirPath ≠ FHIR Search**: FHIR Search ist eine HTTP-GET-Syntax für Serverabfragen; FhirPath navigiert innerhalb einer einzelnen Ressource (client-seitig).
- **FhirPath ≠ SQL/XPath**: FhirPath ist speziell auf das FHIR-Datenmodell zugeschnitten (analog zu XPath für XML).

## Prüfungsrelevanz

**Hoch** (Konzept wird in der Vorlesung eingeführt, aber inhaltlich nicht vertieft).

**Typische Definitionsfrage:** Was ist FhirPath und wofür wird es verwendet?

**Anwendungsfrage:** Wie würde man mit FhirPath auf die erste Telefonnummer eines Patienten zugreifen?

**Diskussionsfrage:** Wo wird FhirPath außerhalb der Client-Navigation noch eingesetzt? (→ in StructureDefinitions als Constraints, in CQL, in SMART/CDS-Hooks-Kontexten)

**Mögliche Anschlussfragen:**
- Wie verhält sich FhirPath zu FHIR Search Parametern?
- Welche Rolle spielt FhirPath in StructureDefinitions? (→ als Invarianten-Ausdruck)

## Verwandt

- [[MSI - HL7 FHIR - Search]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - CQL]]

## Quelle

- Vorlesung: [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]
- Folien/Seitenangabe: Seite 2
