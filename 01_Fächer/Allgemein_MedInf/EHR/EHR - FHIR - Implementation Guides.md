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

# EHR - FHIR - Implementation Guides

> [!info] Kurzdefinition
> Ein **Implementation Guide (IG)** ist ein praxisnahes Dokumentations-Bundle, das mehrere FHIR-Komponenten (Profiles, Extensions, Beispiele, Exchange-Paradigm, ValueSets, Coding-Bindings, Workflows) für einen **konkreten Use-Case** kombiniert. Ohne IG ist FHIR nicht produktiv einsetzbar.

## Beschreibung

Aus Folien 77–79:

> „IGs are comprehensive documents that combine multiple FHIR components to create a practical, real-world implementation for specific use cases."

> „'FHIR IGs = FHIR Profiles + Examples + Exchange Paradigm + LOTS of Documentation'
> IGs serve as a blueprint for implementing FHIR in specific contexts, providing detailed guidance on how to use FHIR resources, profiles, and exchange paradigms to achieve particular healthcare interoperability goals."

## Bestandteile / Aufbau

### Inhalte eines IG (Folie 79)

1. **Profiles und Extensions** – tailored an den Use-Case
2. **Examples** – konkrete Resource-Beispiele
3. **Exchange Paradigms** – welche Methoden (REST/Documents/Messaging) genutzt werden, und wie
4. **Detailed Documentation** – technische Details, Workflows, Best Practices

### Bekannte IGs (Folie 80)

| IG | Land/Org | URL |
|---|---|---|
| **US Core** | USA | build.fhir.org/ig/HL7/US-Core/index.html |
| **ADBM / NDHM** | Indien | nrces.in/ndhm/fhir/r4/index.html |
| **Nphies** | Saudi-Arabien | scribd.com/document/719877031/NPHIES-Implementation-Guide-v2-0 |
| **AT Core (HL7-AT-FHIR-Core-R5)** | Österreich | fhir.hl7.at/HL7-AT-FHIR-Core-R5/index.html |

### Tooling

- **FHIR Registry** (fhir.org/guides/registry/) – zentrale Auffindbarkeit
- **Simplifier.net** – Hosting/Editing-Plattform für IGs

## Beispiel

**US Core IG** definiert:
- US Core Patient Profile (mit Race/Ethnicity-Extensions, Identifier 1..*)
- US Core Condition Profile
- US Core Observation Profile (Vital Signs, Lab Results)
- ValueSet-Bindings auf LOINC, SNOMED CT, ICD-10-CM, RxNorm
- Exchange-Paradigm: REST mit OAuth2 / SMART on FHIR
- Dokumentation für die ONC-Zertifizierung

→ Ein US-EHR, das ONC-zertifiziert sein will, muss US Core implementieren.

**AT Core IG** ist das österreichische Pendant – es definiert SVNR-spezifische Identifier-Strukturen, ELGA-kompatible Codes etc.

## Abgrenzung

- **IG ≠ Profile:** Profile ist ein Bestandteil eines IG. Ein IG enthält typischerweise viele Profiles + ergänzende Komponenten.
- **IG ≠ Standard:** Der FHIR-Standard ist das Fundament; IGs sind die konkreten Anwendungs-Pakete darauf.
- IGs können sich überlappen oder konfligieren – ein nationales IG kann zusätzliche Anforderungen über ein internationales (z. B. IPS) legen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein FHIR Implementation Guide, und welche Bestandteile hat er typischerweise?

**Anwendungsfrage:** Welches IG würdest du für ein österreichisches EHR-Projekt nutzen? Welches für ein US-Projekt?

**Diskussionsfrage:** Internationale IGs (z. B. IPS – International Patient Summary) vs. nationale IGs (US Core, AT Core) – wie verhalten sich die zueinander? Wie kombiniert man sie?

**Mögliche Anschlussfragen:**
- Was ist Simplifier.net und welche Rolle spielt es?
- Wie funktioniert IG-Versionierung?
- Was ist der Unterschied zwischen einem Trial-Use IG und einem Normative IG?
- Welche IGs gibt es international für Patient Summary, Care Plan, Patient Access?

## Verwandt

- [[EHR - FHIR - Profiles und Must Support]]
- [[EHR - FHIR - Extensions und 80 20 Regel]]
- [[EHR - FHIR - 6 Exchange Paradigms]]
- [[EHR - USCDI US Core Data for Interoperability]]
- [[EHR - ELGA - Technologie-Architektur]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 77–80 (Implementation Guides, IG-Definition, Liste konkreter IGs)
