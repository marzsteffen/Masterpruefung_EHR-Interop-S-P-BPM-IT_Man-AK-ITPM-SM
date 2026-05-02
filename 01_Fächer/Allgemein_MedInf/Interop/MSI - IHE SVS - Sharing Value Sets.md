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

# MSI - IHE SVS - Sharing Value Sets

> [!info] Kurzdefinition
> IHE SVS (*Sharing Value Sets*) ist ein älteres IHE-Integrationsprofil im IT Infrastructure Technical Framework. Standardisierte Abfrage von Terminologien aus einem **Value Set Repository** durch einen **Value Set Consumer**. Auf Basis von **SOAP und XML**.

## Beschreibung

Wörtlich aus Folie 11:

> „Sharing Value Set Integrationsprofil im IT Infrastructure Technical Framework
> Standardisierte Abfrage von Terminologien aus einem Value Set Repository
> Auf Basis von SOAP und XML"

Akteure:
- **Value Set Repository**
- **Value Set Consumer**

Transaktionen:
- **Retrieve Value Set [ITI-48]** – einzelnes Value Set abrufen.
- **Retrieve Multiple Value Sets [ITI-60]** – mehrere Value Sets abrufen.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Profil-Familie | IHE ITI (IT Infrastructure) |
| Akteur 1 | Value Set Repository |
| Akteur 2 | Value Set Consumer |
| Transaktion 1 | ITI-48 Retrieve Value Set |
| Transaktion 2 | ITI-60 Retrieve Multiple Value Sets |
| Format | XML im SOAP-Envelope |

## Beispiel

Aus Folie 11 (XML-Snippet eines ELGA_AddressUse-Value-Sets):
```xml
<valueSet
  beschreibung="Beschreibt die Bedeutung und Verwendung einer Adresse..."
  description="Describes the meaning and use of addresses..."
  displayName="ELGA_AddressUse" effectiveDate="2020-08-20"
  gueltigkeitsbereich="empfohlen" id="1.2.40.0.34.10.16"
  last_change_date="2020-08-20" name="ELGA_AddressUse" statusCode="1"
  status_date="2020-08-20" verantw_Org="" version="202008"
  website="http://www.hl7.org">
  <conceptList>
    <concept code="H" codeSystem="2.16.840.1.113883.5.1119"
             conceptStatus="1" conceptStatusDate="2013-06-05"
             concept_beschreibung="zu Hause (A communication address...)"
             deutsch="Wohnort" displayName="home address"
             einheit_codiert="" einheit_print=""
             hinweise="kann für Nebenwohnsitze verwendet werden"
             level="0" orderNumber="1"
             parentCodeSystemName="HL7:AddressUse" relationships=""
             type="S"/>
    <concept code="HP" codeSystem="2.16.840.1.113883.5.1119"
             conceptStatus="1" conceptStatusDate="2013-06-05"
             ...
```
Das Snippet zeigt das hierarchische Konzept-Modell: `home address (H)` mit Kindern `primary home (HP)` und `vacation home (HV)` aus dem HL7-AddressUse-CodeSystem.

## Abgrenzung

- **IHE SVS ≠ IHE SVCM**: SVS ist XML/SOAP-basiert und älter; SVCM ist FHIR-basiert und aktueller. SVCM hat mehr Operationen (siehe [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]).
- **ITI-48 vs. ITI-60**: ITI-48 holt ein einzelnes Value Set; ITI-60 holt mehrere auf einmal.
- **IHE SVS ≠ FHIR ValueSet/$expand**: konzeptionell ähnlich, aber andere Technologie (SOAP/XML statt REST/JSON).

## Prüfungsrelevanz

**Mittel.** Wahrscheinlicher als Diskussionspunkt zur Evolution der Standards.

**Typische Definitionsfrage:** Was ist IHE SVS? Welche Akteure und Transaktionen umfasst es?

**Anwendungsfrage:** Welche Transaktion verwenden Sie, um *mehrere* Value Sets gleichzeitig abzurufen? (ITI-60.)

**Diskussionsfrage:** Warum ist IHE SVS heute weniger gebräuchlich als IHE SVCM?

**Mögliche Anschlussfragen:**
- Wie ist IHE SVCM aufgebaut, und welche zusätzlichen Operationen hat es? → [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]
- Welcher FHIR-Operation entspricht ITI-48 inhaltlich? (`$expand` auf ValueSet)
- Wie wird in einem SVS-Snippet die Hierarchie ausgedrückt? (parentCodeSystemName + level + relationships)

## Verwandt

- [[MSI - Terminologieserver - Austauschstandards]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - IHE XDS - Architektur]] (anderes IHE-Profil als Vergleich)

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 11
- Externe: `http://wiki.ihe.net/index.php/Sharing_Value_Sets`
