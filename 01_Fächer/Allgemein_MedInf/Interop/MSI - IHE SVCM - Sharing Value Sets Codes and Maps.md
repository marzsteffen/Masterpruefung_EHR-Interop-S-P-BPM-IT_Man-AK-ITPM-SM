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

# MSI - IHE SVCM - Sharing Value Sets Codes and Maps

> [!info] Kurzdefinition
> IHE SVCM (*Sharing Valuesets, Codes and Maps*) ist das aktuelle, **FHIR-basierte** IHE-Profil zum Austausch von Terminologien zwischen einem **Terminology Repository** und einem **Terminology Consumer**. Sieben Transaktionen ITI-95 bis ITI-101 mappen direkt auf FHIR-Operationen.

## Beschreibung

Folie 51 zeigt die Akteure und Transaktionen:

| ITI-Nummer | Transaktion | Inhalt | FHIR-Pendant |
|---|---|---|---|
| ITI-95 | Query Value Set | ValueSet-Suche/Read | FHIR ValueSet read/search |
| ITI-96 | Query Code System | CodeSystem-Suche/Read | FHIR CodeSystem read/search |
| ITI-97 | Expand Value Set | Konzepte eines ValueSets auflisten | `ValueSet/$expand` |
| ITI-98 | Lookup Code | Details zu einem Code | `CodeSystem/$lookup` |
| ITI-99 | Validate Code | Code in ValueSet prüfen | `ValueSet/$validate-code` |
| ITI-100 | Query Concept Map | ConceptMap-Suche/Read | FHIR ConceptMap read/search |
| ITI-101 | Translate Code | Code via ConceptMap übersetzen | `ConceptMap/$translate` |

Akteure:
- **Terminology Repository** (server-seitig)
- **Terminology Consumer** (client-seitig)

Quelle laut Folie: `https://profiles.ihe.net/ITI/SVCM/index.html`.

## Bestandteile / Aufbau

| Komponente | Funktion |
|---|---|
| Profil-Familie | IHE ITI (IT Infrastructure) |
| Basis-Standard | HL7 FHIR |
| Akteure | Terminology Repository + Terminology Consumer |
| Drei Resource-Typen | Value Set, Code System, Concept Map |
| Sieben Transaktionen | ITI-95 bis ITI-101 |

## Beispiel

Ein FHIR-Terminology-Server (z. B. Ontoserver, tx.fhir.org) implementiert SVCM-konform ITI-95 bis ITI-101 als REST-Operationen. Ein KIS als Consumer kann z. B. via `GET ValueSet/$expand?url=...` ein ValueSet auflisten – das entspricht ITI-97.

## Abgrenzung

- **SVCM ≠ SVS**: SVCM ist FHIR-basiert (REST/JSON, XML); SVS ist SOAP/XML-basiert. SVCM hat mehr Operationen (Code Systems, Concept Maps zusätzlich zu Value Sets).
- **SVCM ≠ FHIR Terminology Service**: SVCM ist die *IHE-Profilierung* des FHIR Terminology Service – es legt zusätzlich Konformitäts­anforderungen auf das FHIR-Verhalten.
- **ITI-Nummern aus SVCM ≠ ITI-Nummern aus XDS**: ITI-95 bis ITI-101 sind SVCM-spezifisch; XDS hat eigene ITI-Nummern (ITI-8/41/42/43/44/18/61).

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Was ist IHE SVCM? Welche Akteure und Transaktionen kennt es?

**Anwendungsfrage:** Welche ITI-Transaktion verwenden Sie für (a) Code-Validierung, (b) ValueSet-Expansion, (c) Code-Übersetzung?

**Diskussionsfrage:** Welchen Vorteil hat IHE SVCM gegenüber dem reinen FHIR Terminology Service?

**Mögliche Anschlussfragen:**
- Welche FHIR-Operationen entsprechen welchen ITI-Transaktionen?
- Wie unterscheidet sich SVCM von SVS? → [[MSI - IHE SVS - Sharing Value Sets]]
- Welche FHIR-Resources sind beteiligt? → [[MSI - HL7 FHIR - CodeSystem Resource]], [[MSI - HL7 FHIR - ValueSet Resource]], [[MSI - HL7 FHIR - ConceptMap Resource]]

## Verwandt

- [[MSI - Terminologieserver - Austauschstandards]]
- [[MSI - IHE SVS - Sharing Value Sets]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 51
- Externe: `https://profiles.ihe.net/ITI/SVCM/index.html`
