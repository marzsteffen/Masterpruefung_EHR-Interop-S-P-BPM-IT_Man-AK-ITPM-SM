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

# EHR - FHIR - Extensions und 80 20 Regel

> [!info] Kurzdefinition
> **Extensions** fügen einer FHIR-Resource neue Datenelemente hinzu, ohne ihre Core-Definition zu ändern. Sie folgen der **80/20-Regel**: FHIR beschreibt 80 % der Versorgungsrealität in Base-Resources; die übrigen 20 % – kulturell, regional oder spezialisiert – werden über Extensions abgebildet.

## Beschreibung

### Extensions

Aus Folien 25–26:

> „Extensions are a way to add new elements to a resource without changing its core definition.
> They allow for flexibility and customization of FHIR resources to meet specific needs or requirements that aren't covered by the standard elements.
>
> 1. They have a defined URL that identifies the extension.
> 2. They can contain any datatype allowed in FHIR.
> 3. They can be simple or complex, containing multiple sub-extensions."

### 80/20-Regel

Aus Folie 27:

> „Do not try to describe the whole medical world ... But only 80% of it ...
> Do not try to describe concepts that are cultural dependent – Race, Religion, …
> The 20 other % can be described using extensions – Can be local in scope."

Folie 28 illustriert das mit dem **Race-Beispiel** (US Census Bureau):
- White
- Black or African American
- American Indian and Alaska Native
- Asian
- Native Hawaiian and Other Pacific Islander – Hispanic or Latino

Wichtig: „**self-reported**". Race ist ein typisches Beispiel für ein kulturell variantes Konzept – in den USA Pflicht-Erfassung, in vielen anderen Ländern unzulässig. Daher Extension, nicht Core.

## Bestandteile / Aufbau

### Eigenschaften einer Extension

| Eigenschaft | Inhalt |
|---|---|
| **URL** (canonical) | eindeutige globale ID der Extension-Definition |
| **Value[x]** oder Sub-Extensions | trägt die eigentlichen Daten in beliebigem FHIR-Datatype |
| **Optional** oder **Modifier** | Modifier-Extensions ändern die Bedeutung der Resource und müssen verstanden werden, sonst Verarbeitung verweigern |

### Beispiel-Struktur

```json
{
  "extension": [
    {
      "url": "http://hl7.org/fhir/us/core/StructureDefinition/us-core-race",
      "extension": [
        {
          "url": "ombCategory",
          "valueCoding": {
            "system": "urn:oid:2.16.840.1.113883.6.238",
            "code": "2106-3",
            "display": "White"
          }
        }
      ]
    }
  ]
}
```

## Beispiel

US-Spezifika, die als Extensions implementiert sind:
- **Race** (US Census Categories)
- **Ethnicity** (Hispanic or Latino vs. Not Hispanic or Latino)
- **Birth Sex** (separate Erfassung von Sex assigned at birth)

Österreich-spezifische Extensions (in AT-Core-IG):
- SVNR als spezifische Identifier-Extension
- Adressen-Erweiterungen für Bundesland-Codes

## Abgrenzung

- **Extension ≠ Profile:** Profile schränkt vorhandene Felder ein; Extension fügt neue Felder hinzu.
- **Extension ≠ Modifier Extension:** Eine Modifier Extension verändert die Bedeutung der Resource. Wenn der Empfänger sie nicht versteht, **muss er die Resource ablehnen** – das ist eine wichtige Sicherheits­regel.
- **80/20 ≠ 50/50:** FHIR ist bewusst ungleich verteilt – Pareto-Logik. Das ist Designentscheidung, nicht Compromise.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine FHIR-Extension? Was bedeutet die 80/20-Regel?

**Anwendungsfrage:** Wie würdest du Religion eines Patienten in FHIR abbilden? (Antwort: Extension, weil kulturell variabel)

**Diskussionsfrage:** Race in den USA ist Pflicht (US Core), in Deutschland gesetzlich unzulässig zu erfassen. Wie geht FHIR damit um? Welche Trade-offs entstehen?

**Mögliche Anschlussfragen:**
- Was ist eine Modifier Extension und wie unterscheidet sie sich von einer Standard-Extension?
- Wo werden Extensions registriert? (Antwort: HL7 FHIR Registry, Simplifier.net, lokale IG-Repositories)
- Welche Risiken haben „wilde" Extensions ohne kanonische URL?
- Was ist „self-reported" im Race-Kontext und warum ist das wichtig?

## Verwandt

- [[EHR - FHIR - Profiles und Must Support]]
- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Data Types und Cardinality]]
- [[EHR - FHIR - Implementation Guides]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 25–28 (Extensions, 80/20-Regel, Race-Beispiel)
