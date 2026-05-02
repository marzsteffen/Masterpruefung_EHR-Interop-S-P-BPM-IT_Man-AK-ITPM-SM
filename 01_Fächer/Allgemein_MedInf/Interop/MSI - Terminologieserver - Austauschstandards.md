---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR und Terminologieserver]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologieserver - Austauschstandards

> [!info] Kurzdefinition
> Standards für den Austausch von Terminologien zwischen Server und Consumer (Folie 9): **FHIR Terminology Resources und Operationen**, **ClaML** (Classification Markup Language, CEN/TS 14463:2003 / EN 14463:2007), **CTS2** (Object Management Group, veraltet), **IHE-Profile** (SVCM auf FHIR-Basis, SVS auf XML-Basis).

## Beschreibung

Wörtlich aus Folie 9:

> „**FHIR Terminology Ressourcen und Operationen** – siehe eigene Folien dazu
>
> **ClaML: Classification Markup Language**
> – CEN/TS 14463:2003 / EN 14463:2007
> – XML-Datenformat-Spezifikation für den Austausch von (hierarchischen) medizinischen Klassifikationen
>
> **CTS2 (veraltet)**
> – Object Management Group Common Terminology Services 2 …
> – Standard für die Pflege, Abfrage und für die Weitergabe von Terminologien und Value Sets.
>
> **IHE Profile**
> – IHE SVCM (Sharing Valuesets, Codes and Maps, siehe eigene Folien dazu)
>   – Austausch von Terminologien auf Basis von FHIR
> – IHE SVS (Sharing Value Sets)
>   – IHE Sharing Value Sets Profil (XML) zum Austausch von Value Sets"

## Bestandteile / Aufbau

| Standard | Format | Status | Anwendung |
|---|---|---|---|
| **FHIR Terminology** | FHIR Resources + REST Operationen | aktuell | CodeSystem, ValueSet, ConceptMap + `$expand`, `$lookup`, `$validate-code`, `$translate` |
| **ClaML** | XML | aktiv | Hierarchische Klassifikationen wie ICD-10 |
| **CTS2** | OMG / Webservices | **veraltet** | Datenmodell + Webservice-Schnittstellen für Terminologieserver |
| **IHE SVCM** | FHIR | aktuell | Sharing Valuesets, Codes and Maps – Profil über IHE ITI |
| **IHE SVS** | XML / SOAP | älter | Sharing Value Sets – ITI-48 (Retrieve Value Set), ITI-60 (Retrieve Multiple Value Sets) |

## Beispiel

- **CTS2 Umsetzungsbeispiel** (Folie 10): Terminologieserver der FH Dortmund (Haas, Mützner). Methoden u. a. `GetTermserverVersion`, `ListCodeSystems`, `ListCodeSystemConcepts`, `ListConceptAssociationTypes`, `ListDomains`, `ListDomainValues`, `ListGloballySearchedConcepts`, `ListMetadataParameter`, `ListValueSets`, `ListValueSetContents`, `ListValueSetContentsByTermOrCode`, `ReturnCodeSystemDetails`.
- **IHE SVS Beispiel** (Folie 11): SOAP-/XML-basierte Abfrage gegen Value Set Repository über ITI-48 (Retrieve Value Set) und ITI-60 (Retrieve Multiple Value Sets). Beispiel-Snippet zeigt ELGA_AddressUse-ValueSet mit OID `1.2.40.0.34.10.16`.
- **FHIR Terminology** (Folie 37 ff.): siehe [[MSI - HL7 FHIR - Terminology Service]].

## Abgrenzung

- **CTS2 ≠ FHIR Terminology**: CTS2 ist OMG-basiert und veraltet; FHIR ist HL7-basiert und der aktuelle Standard.
- **IHE SVCM ≠ IHE SVS**: SVCM ist FHIR-basiert (modern); SVS ist XML-/SOAP-basiert (älter).
- **ClaML ≠ FHIR CodeSystem**: ClaML codiert Klassifikationen wie ICD-10 in einem eigenen XML-Format; FHIR CodeSystem ist die FHIR-Resource. Beide können dieselben Daten enthalten.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Welche Standards für den Austausch von Terminologien gibt es? Welcher ist veraltet?

**Anwendungsfrage:** Welche Standards würden Sie heute für einen neuen Terminologieserver wählen, und warum?

**Diskussionsfrage:** Wie ist das Verhältnis zwischen IHE SVCM und FHIR Terminology Service?

**Mögliche Anschlussfragen:**
- Was ist ClaML konkret? → [[MSI - ClaML - Classification Markup Language]]
- Was leisten IHE SVS und IHE SVCM? → [[MSI - IHE SVS - Sharing Value Sets]], [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]
- Welche FHIR-Operationen gibt es? → [[MSI - HL7 FHIR - Terminology Service]]

## Verwandt

- [[MSI - ClaML - Classification Markup Language]]
- [[MSI - IHE SVS - Sharing Value Sets]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 9, 10, 11
