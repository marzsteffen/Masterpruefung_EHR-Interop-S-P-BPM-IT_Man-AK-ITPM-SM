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

# MSI - HL7 FHIR - Datentyp code

> [!info] Kurzdefinition
> `code` ist ein primitiver FHIR-Datentyp (String ohne Whitespace), der in der Spezifikation **required gebunden** ist. Codesystem muss nicht angegeben werden – es ist durch das Binding bekannt und es gibt keine Überlappung von Codes aus verschiedenen Systemen. Eingesetzt für international interoperable Werte (z. B. `gender: "female"`, `Bundle.type: "document"`).

## Beschreibung

Wörtlich aus Folie 32:

> „**Code**
> – primitiver Datentyp (String ohne Whitespace)
> – in der Spezifikation festgelegt (required binding)
> – Codesystem muss nicht angegeben werden (da durch Binding bekannt und keine Überlappung von Codes aus verschiedenen Systemen)
> – wird eingesetzt, wo Interoperabilität auf internationaler Ebene möglich/erforderlich ist (gender: ‚female', status: ‚active')
> – wird auch für strukturelle Belange eingesetzt (Bundle.type=‚document')"

Beispiel aus Folie 32:
| Element | Card. | Type | Description |
|---|---|---|---|
| `gender` | 0..1 | code | male \| female \| other \| unknown — AdministrativeGender (Required) |
| `birthDate` | 0..1 | date | The date of birth for the individual |

## Bestandteile / Aufbau

- **Wertebereich**: einzelner String, kein Whitespace.
- **Bindung**: immer mit Required Binding an ein FHIR-Value-Set.
- **Codesystem**: implizit über das Binding gegeben, nicht im Element angegeben.
- **Anwendung**: international invariante Vokabulare (Status-Codes, Gender, Bundle-Typ etc.).

## Beispiel

```json
"gender": "male"
"status": "active"
"type": "document"
```

## Abgrenzung

- **`code` ≠ `Coding`**: `code` ist primitiver String, `Coding` ein komplexes Element mit system + version + code + display + userSelected.
- **`code` ≠ `CodeableConcept`**: `CodeableConcept` enthält Codings + Text; `code` enthält nur den String.
- **`code` mit Required Binding ≠ `code` mit Extensible Binding**: `code` darf in der Spec nur required gebunden sein – wenn ein Element extensible/preferred/example gebunden ist, wäre der Datentyp `Coding` oder `CodeableConcept`.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Was ist der FHIR-Datentyp `code`? Welche Bindung verwendet er?

**Anwendungsfrage:** Welche FHIR-Elemente verwenden den Datentyp `code`? Welche `Coding`?

**Diskussionsfrage:** Warum braucht ein `code`-Element kein Codesystem-Attribut?

**Mögliche Anschlussfragen:**
- Was bedeutet „Required Binding"? → [[MSI - HL7 FHIR - Terminology Binding Strength]]
- Welcher Datentyp passt für Diagnose-Codes? (CodeableConcept)
- Warum ist `Bundle.type = "document"` ein `code`?

## Verwandt

- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]
- [[MSI - HL7 FHIR - Terminology Binding Strength]]

## Ergänzung aus Anna-Lin-Gastvortrag

**XML-Beispiel für code-Datentyp** (Seite 39):

- Code-Element mit ICD-10-Code als Attribut; das Codesystem ist implizit (durch das Profil fixiert, nicht explizit angegeben):

```xml
<code value="G44.1" />
```

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 32 (06er-VL); Seite 39 (Anna Lin Starter)
