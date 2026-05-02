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

# MSI - HL7 FHIR - CodeSystem Resource

> [!info] Kurzdefinition
> Eine FHIR-Resource zur **Definition** eines Codesystems: Konzepte mit Code und Bedeutung, Namensraum (URI), optional Hierarchien, Display-Values, Properties/Attribute. **CodeSystem-Supplements** erweitern bestehende Codesysteme um zusätzliche Codes, Display-Values (z. B. Übersetzungen) oder Properties (lokale Annotationen).

## Beschreibung

Folie 38:

> „Codesysteme definieren Konzepte mit Code und Bedeutung
> definieren den Namensraum (URI) dieser Codes
> definieren ggf. die Relationen zwischen den Codes (Hierarchien)
> definieren Display-Values
> Konzepte können Eigenschaften/Attribute beinhalten
>
> CodeSystem-Supplements können enthalten
> – zusätzliche (lokale) Codes, wie nationale Erweiterungen zu einem internationalen CodeSystem
> – zusätzliche Display-Values wie Übersetzungen eines internationalen CodeSystems
> – zusätzliche Properties wie lokale Annotationen"

Folie 39 zeigt die UML-Struktur der CodeSystem-Resource:

| Attribut | Typ | Card. | Bedeutung |
|---|---|---|---|
| `url` | uri | 0..1 | Canonical URL |
| `identifier` | Identifier | 0..* | OIDs etc. |
| `version` | string | 0..1 | Version |
| `name`, `title` | string | 0..1 | Bezeichner |
| `status` | code | 1..1 | PublicationStatus |
| `experimental` | boolean | 0..1 | – |
| `date`, `publisher`, `contact`, `description`, `useContext`, `jurisdiction`, `purpose`, `copyright` | – | – | Metadaten |
| `caseSensitive` | boolean | 0..1 | – |
| `valueSet` | canonical(ValueSet) | 0..1 | Implizit-ValueSet, das alle Konzepte enthält |
| `hierarchyMeaning` | code | 0..1 | – |
| `compositional` | boolean | 0..1 | unterstützt Postkoordination |
| `versionNeeded` | boolean | 0..1 | – |
| `content` | code | 1..1 | CodeSystemContentMode (z. B. complete, fragment, supplement) |
| `supplements` | canonical(CodeSystem) | 0..1 | wenn das CodeSystem ein Supplement ist, hier das Original |
| `count` | unsignedInt | 0..1 | – |
| `filter` | Filter[0..\*] | – | Suchfilter |
| `property` | Property[0..\*] | – | Eigenschaften der Konzepte |
| `concept` | ConceptDefinition[0..\*] | – | Die Konzepte selbst |

ConceptDefinition enthält: `code`, `display`, `definition`, optional `concept` (rekursiv für Hierarchie), `designation` (Sprachvarianten), `property` (Werte der Properties).

## Bestandteile / Aufbau

| Bestandteil | Inhalt |
|---|---|
| Metadata | url, identifier, version, name, status, publisher, copyright … |
| Inhalt | `concept`-Liste mit code/display/definition |
| Hierarchie | `concept` rekursiv verschachtelt + `hierarchyMeaning` |
| Designations | Sprachvarianten/Synonyme |
| Properties | typisierte Eigenschaften pro Konzept (boolean/integer/Coding/dateTime/decimal) |
| Filter | Suchfilter für `$expand` etc. |
| Supplements | Erweiterung eines anderen CodeSystems |

## Beispiel

Aus dem Folien-Beispiel (Folie 47, lookup-Antwort):
```json
{
  "resourceType" : "Parameters",
  "parameter" : [
    {"name" : "name", "valueString" : "v3.MaritalStatus"},
    {"name" : "version", "valueString" : "2018-08-12"},
    {"name" : "display", "valueString" : "Married"}
  ]
}
```

Eine CodeSystem-Resource für HL7 v3 MaritalStatus liefert auf Lookup für Code `M` Name, Version, Display.

## Abgrenzung

- **CodeSystem ≠ ValueSet**: CodeSystem definiert Codes; ValueSet wählt Codes für einen Use Case aus.
- **CodeSystem-Supplement ≠ neues CodeSystem**: ein Supplement erweitert ein bestehendes; ein neues CodeSystem ist eigenständig.
- **`identifier` (OID) ≠ `url` (canonical)**: in FHIR ist `url` primär; `identifier` mit OID ist optional für Mapping zu CDA/v3.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Was leistet die FHIR-CodeSystem-Resource? Welche Bestandteile hat sie?

**Anwendungsfrage:** Welche FHIR-Operation liefert Details zu einem Code? (`$lookup` auf CodeSystem.)

**Diskussionsfrage:** Wann verwenden Sie ein CodeSystem-Supplement statt eines neuen CodeSystems?

**Mögliche Anschlussfragen:**
- Was bedeutet `compositional: true`? (Codesystem unterstützt Postkoordination.)
- Wie wird die Hierarchie ausgedrückt? (`concept` rekursiv + `hierarchyMeaning`.)
- Wie wird das CodeSystem über `$lookup` abgefragt? → [[MSI - HL7 FHIR - Terminology Service]]

## Verwandt

- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - Terminology Framework]]
- [[MSI - Terminologie - Code System]]

## Ergänzung aus Anna-Lin-Gastvortrag

**Historische Einordnung: CodeSystem als eigene Ressource** (Seite 43):

In FHIR **STU2** war CodeSystem keine eigenständige Ressource — das Codesystem war immer einem ValueSet zugeordnet, das Codes gruppieren musste. Der Starter-PDF beschreibt diese ältere Sicht:

> „Code System: Ein System welches Codes definiert (Bsp.: LOINC) – Muss ValueSets enthalten, um die Codes zu gruppieren. In STU3 ist Code System als eigene Ressource geplant."

Ab **STU3** (heute R4/R5) ist CodeSystem eine vollständig eigenständige DomainResource mit eigener URL, eigenem Lifecycle und eigener `$lookup`-Operation. Die enge Koppelung an ValueSet besteht nur noch über den `valueSet`-Parameter (implizites ValueSet, das alle Konzepte des CodeSystems enthält).

**Abgrenzung für die Prüfung:** Falls nach der historischen Entwicklung gefragt wird — CodeSystem wurde in STU3 von ValueSet entkoppelt.

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 38, 39, 47 (06er-VL); Seite 43 (Anna Lin Starter, historische Einordnung)
