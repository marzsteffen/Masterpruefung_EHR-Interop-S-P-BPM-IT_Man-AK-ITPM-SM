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

# MSI - HL7 FHIR - Codierte Elemente Übersicht

> [!info] Kurzdefinition
> Drei Datentypen für codierte Elemente in FHIR: **`code`** (primitiv, fix gebundener String aus dem FHIR-Spec), **`Coding`** (system + version + code + display + userSelected), **`CodeableConcept`** (eine oder mehrere Codings + optionaler Freitext). Externe Code Systems werden über URI identifiziert; OID gibt es nur für Mapping zu Nicht-FHIR-Welten.

## Beschreibung

Folie 31 zeigt:
- Beispiel JSON-Coding:
  ```json
  {
    "system" : "http://loinc.org",
    "version" : "2.62",
    "code" : "55423-8",
    "display" : "Number of steps in unspecified time Pedometer"
  }
  ```
- Beispiel Patient-Snippet:
  ```json
  "gender": "male",
  "birthDate": "1974-12-25"
  ```
- Tabelle „Externally Published code systems" mit URI + Source + OID:
  | URI | Source | OID (für nicht-FHIR-Systeme) |
  |---|---|---|
  | `http://snomed.info/sct` | SNOMED CT (IHTSDO) | `2.16.840.1.113883.6.96` |
  | `http://www.nlm.nih.gov/research/umls/rxnorm` | RxNorm (US NLM) | `2.16.840.1.113883.6.88` |
  | `http://loinc.org` | LOINC | `2.16.840.1.113883.6.1` |
  | `http://unitsofmeasure.org` | UCUM (Case Sensitive Codes) | `2.16.840.1.113883.6.8` |
- Coding-Datentyp-Tabelle (siehe Folie 34): system (uri), version (string), code (code), display (string), userSelected (boolean) – jeweils 0..1.

Quelle laut Folie: `https://www.hl7.org/fhir/terminologies.html`.

## Bestandteile / Aufbau

| Datentyp | Wann verwendet | Inhalt | Beispiel |
|---|---|---|---|
| **code** | für fixe, FHIR-spezifizierte Werte (required binding) | nur ein primitiver String | `gender: "male"` |
| **Coding** | wenn ein einzelner externer Code reicht | system + version + code + display + userSelected | LOINC `55423-8` |
| **CodeableConcept** | wenn mehrere Codings oder Text nötig sind | array von Coding + optional `text` | LOINC + SNOMED + Freitext |
| **Quantity** | Messwerte mit Einheit und Code (Sonderfall) | Wert + Einheit (string) + system + code | 3 Kapseln à `385049006` (SNOMED) |

## Beispiel

Aus Folie 31 (LOINC-Coding für Schritte). Aus Folie 32 (Patient-Snippet mit `gender: "male"`).

Konkrete Code Systems werden über URIs identifiziert:
- `http://snomed.info/sct` (SNOMED CT)
- `http://loinc.org` (LOINC)
- `http://unitsofmeasure.org` (UCUM)

Die zugehörigen OIDs sind im FHIR-Wiki gelistet, werden aber in FHIR selbst meist nicht verwendet (nur für Übersetzung in CDA/HL7 v3).

## Abgrenzung

- **`code` ≠ `Coding`**: `code` ist ein primitiver String mit fixer Bindung in der Spec; `Coding` ist ein komplexer Datentyp mit System/Version/Code/Display.
- **`Coding` ≠ `CodeableConcept`**: ein `CodeableConcept` *enthält* 0..n `Coding`-Elemente plus optional `text`.
- **FHIR URI ≠ CDA OID**: FHIR identifiziert Code Systems primär über URI, CDA über OID. Für Cross-Mapping gibt es Tabellen.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche drei Datentypen für codierte Elemente kennt FHIR? Wann verwenden Sie welchen?

**Anwendungsfrage:** Wie codieren Sie eine Diagnose mit ICD-10 *und* SNOMED CT in FHIR? (CodeableConcept mit zwei Coding-Einträgen.)

**Diskussionsfrage:** Warum verwendet FHIR primär URIs statt OIDs?

**Mögliche Anschlussfragen:**
- Wann verwenden Sie `code` direkt vs. `Coding` direkt? → [[MSI - HL7 FHIR - Datentyp code]]
- Wie verbindet `userSelected` ein `Coding` mit der Wahl des Anwenders? → [[MSI - HL7 FHIR - Datentyp Coding]]
- Wann wird Freitext im `CodeableConcept.text` verwendet? → [[MSI - HL7 FHIR - Datentyp CodeableConcept]]

## Verwandt

- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]
- [[MSI - HL7 FHIR - Terminology Binding Strength]]
- [[MSI - HL7 CDA - Codierte Werte]] (CDA-Pendant)

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 31, 32, 34 (06er-VL); Seiten 38–42 (Anna Lin Starter)
- Externe: `https://www.hl7.org/fhir/terminologies.html`

## Ergänzung aus Anna-Lin-Gastvortrag

**Quantity als 4. codierter Datentyp** (Seite 42):

`Quantity` ist ein **komplexer Datentyp** für Messwerte mit Einheit und Codierung – ein Sonderfall gegenüber den drei Kern-Typen:
- Repräsentiert: Wert (`value`), Maßeinheit als Text (`unit`), Codesystem (`system`), Code (`code`)
- Beispiel (Medikamentendosierung):
```xml
<dose>
  <value value="3"/>
  <unit value="capsules"/>
  <system value="http://snomed.info/sct"/>
  <code value="385049006"/>
</dose>
```
Quantity ist damit mehr als eine Codierung – sie verbindet einen numerischen Wert mit seiner coded unit.
