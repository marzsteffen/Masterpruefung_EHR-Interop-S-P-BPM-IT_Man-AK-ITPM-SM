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

# MSI - HL7 FHIR - Terminology Service

> [!info] Kurzdefinition
> FHIR Terminology Service definiert vier zentrale REST-Operationen: **`$expand`** (auf ValueSet), **`$lookup`** (auf CodeSystem), **`$validate-code`** (auf ValueSet), **`$translate`** (auf ConceptMap). Damit lassen sich Value Sets auflisten, Code-Details abfragen, Codes validieren und übersetzen.

## Beschreibung

Folie 37 fasst zusammen:

> „Basis-Ressourcen
> – CodeSystem (und CodeSystemSupplement)
> – ValueSet
> – ConceptMap
>
> FHIR Terminology Operationen
> – Lookup
> – Validate
> – Expand
> – …"

Folie 45 listet die Operationen mit Aufgabe:

| Operation | Resource | Aufgabe |
|---|---|---|
| **`$expand`** | ValueSet | Anwenden der Content Logical Definition, um zur Expansion (Liste der Konzepte) zu gelangen |
| **`$lookup`** | CodeSystem | Details zu einem Code nachschlagen |
| **`$validate-code`** | ValueSet | Validieren, ob ein bestimmter Code in einem ValueSet gültig ist |
| **`$translate`** | ConceptMap | Übersetzen eines Codes von einem CodeSystem in ein anderes |

Beispiele auf den Folien 47–49:

**`$lookup`** (Folie 47):
- Parameter: `code`, `system`, `displayLanguage`.
- Beispiel:
```
GET http://tx.fhir.org/r4/CodeSystem/$lookup?
    system=http://terminology.hl7.org/CodeSystem/v3-MaritalStatus&code=M
```
- Antwort:
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

**`$translate`** (Folie 48):
- Parameter: `url:canonical` (URL der ConceptMap), `system`, `code`, `source`, `target`.

**`$validate-code`** (Folie 49):
- Parameter: `url` (Canonical URL des ValueSets), `code`, `system`.
- Beispiel:
```
GET http://tx.fhir.org/r4/ValueSet/$validate-code?
    url=http://hl7.org/fhir/ValueSet/marital-status&
    system=http://terminology.hl7.org/CodeSystem/v3-MaritalStatus&code=M
```
- Mit `code=X` würde es fehlschlagen.

## Bestandteile / Aufbau

| Operation | Eingabe | Ausgabe |
|---|---|---|
| `$expand` | ValueSet (URL + ggf. Filter) | Expansion (Liste der Konzepte) |
| `$lookup` | system + code + ggf. displayLanguage | Parameters mit name/version/display + properties |
| `$validate-code` | ValueSet-URL + system + code | Result + Message |
| `$translate` | ConceptMap-URL + system + code + source/target | Mapping-Ergebnis |

Quelle laut Folie 45: `http://hl7.org/fhir/terminology-service.html`. Beispiele: `https://ontoserver.csiro.au/tx-postman-r4`.

## Beispiel

Siehe oben (Beispiele für `$lookup` und `$validate-code`). Aus Folie 49 als zweite `$validate-code`-Anfrage:
```
GET http://tx.fhir.org/r4/ValueSet/$validate-code?
    url=http://hl7.org/fhir/ValueSet/marital-status&
    system=http://terminology.hl7.org/CodeSystem/v3-MaritalStatus&code=X
```
→ Ergebnis: Code `X` ist nicht in dem ValueSet enthalten.

## Abgrenzung

- **`$expand` ≠ `$validate-code`**: Expand listet alle Codes auf; Validate-Code prüft genau einen Code.
- **`$lookup` ≠ `$validate-code`**: Lookup gibt Details zu einem Code zurück, ohne ValueSet-Bindung; Validate-Code arbeitet im Kontext eines ValueSets.
- **`$translate` ≠ `$lookup`**: Translate übersetzt zwischen Codesystemen via ConceptMap; Lookup arbeitet innerhalb eines Codesystems.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche vier zentralen Operationen kennt der FHIR Terminology Service? Welche Aufgabe erfüllt jede?

**Anwendungsfrage:** Welche Operation verwenden Sie, um den deutschen Display-Namen von `M` (Married) aus v3-MaritalStatus zu erhalten? (`$lookup` mit `displayLanguage=de`.)

**Diskussionsfrage:** Welche Operation wird von Schematron-Validatoren in CDA implizit gebraucht? (`$validate-code`-Logik, hier per Schematron umgesetzt.)

**Mögliche Anschlussfragen:**
- Welche Operation entspricht IHE SVCM ITI-99? (`$validate-code` → ITI-99.)
- Welche IHE-ITI-Nummer entspricht `$translate`? (ITI-101.)
- Welche IHE-ITI-Nummer entspricht `$expand`? (ITI-97.)

## Verwandt

- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]
- [[MSI - HL7 FHIR - Terminology Framework]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]
- [[MSI - Terminologieserver - Aufgaben]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 37, 45, 47, 48, 49
- Externe: `http://hl7.org/fhir/terminology-service.html`, `https://ontoserver.csiro.au/tx-postman-r4`
