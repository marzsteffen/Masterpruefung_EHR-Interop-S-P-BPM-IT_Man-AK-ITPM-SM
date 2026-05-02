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

# MSI - HL7 FHIR - Datentyp CodeableConcept

> [!info] Kurzdefinition
> `CodeableConcept` beinhaltet ein oder mehrere `Coding`-Elemente für ein Konzept und/oder eine Freitext-Beschreibung des Konzepts. Standard-Datentyp für medizinische Codierungen in FHIR (Diagnose, Allergie, Medikament etc.).

## Beschreibung

Wörtlich aus Folie 33:

> „beinhaltet ein oder mehrere Codings für ein Konzept
> und/oder eine Freitext-Beschreibung des Konzeptes"

Struktur (Folie 33):

| Name | Flags | Card. | Type | Description |
|---|---|---|---|---|
| CodeableConcept | Σ N | – | Element | Concept – reference to a terminology or just text |
| coding | Σ | 0..* | Coding | Code defined by a terminology system |
| text | Σ | 0..1 | string | Plain text representation of the concept |

Beispiele für CodeableConcept-Verwendung in der Patient-Resource (Folie 33):
- `Patient.maritalStatus` (CodeableConcept, Binding: MaritalStatus, Extensible)
- `Patient.contact.relationship` (CodeableConcept, Binding: PatientContactRelationship, Extensible)

## Bestandteile / Aufbau

- **`coding` (0..\*)**: mehrere Codings für dasselbe Konzept (z. B. ICD-10 + SNOMED CT). Reihenfolge bedeutet keine Priorität – `userSelected` markiert die Wahl.
- **`text` (0..1)**: Freitext, der das Konzept beschreibt. Sinnvoll, wenn keine Codings möglich sind oder die Codings den eigentlich gemeinten Kontext nicht 100 % treffen.

## Beispiel

```json
"maritalStatus": {
  "coding": [
    {
      "system": "http://terminology.hl7.org/CodeSystem/v3-MaritalStatus",
      "code": "M",
      "display": "Married"
    }
  ],
  "text": "verheiratet seit 2010"
}
```

Mehrfach-Codierung (Diagnose ICD-10 + SNOMED):
```json
"code": {
  "coding": [
    { "system": "http://hl7.org/fhir/sid/icd-10",
      "code": "M54.9", "display": "Rückenschmerzen, nicht näher bezeichnet" },
    { "system": "http://snomed.info/sct",
      "code": "161891005", "display": "Backache" }
  ],
  "text": "unspezifische Rückenschmerzen LWS"
}
```

## Abgrenzung

- **CodeableConcept ≠ Coding**: CodeableConcept enthält Codings + Text; Coding ist ein einzelner Code-Eintrag.
- **CodeableConcept-`text` ≠ Coding-`display`**: `display` ist die Anzeige aus dem Codesystem, `text` ist der freie Anwender-Text.
- **Mehrere Codings ≠ Mehrere Bedeutungen**: Mehrere Codings sollen *dasselbe* Konzept aus verschiedenen Codesystemen ausdrücken (Translation/Cross-Mapping). Sie dürfen nicht für unterschiedliche Bedeutungen genutzt werden.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Was enthält ein FHIR-CodeableConcept?

**Anwendungsfrage:** Wie codieren Sie eine Diagnose, die sowohl ICD-10 als auch SNOMED CT verwendet? (Mehrfach-Codings im selben CodeableConcept.)

**Diskussionsfrage:** Wann ist `text` allein sinnvoll, ohne Coding?

**Mögliche Anschlussfragen:**
- Welcher CDA-Mechanismus entspricht der Mehrfach-Codierung? → [[MSI - HL7 CDA - Translation]]
- Was bedeutet `userSelected: true` in einem von mehreren Codings? → [[MSI - HL7 FHIR - Datentyp Coding]]
- Welche Binding Strength ist für CodeableConcept typisch? → [[MSI - HL7 FHIR - Terminology Binding Strength]]

## Verwandt

- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 CDA - Translation]] (CDA-Pendant)

## Ergänzung aus Anna-Lin-Gastvortrag

**XML-Beispiel für CodeableConcept mit zwei Codings** (Seite 41):

```xml
<concept>
  <coding>
    <system value="http://hl7.org/fhir/sid/icd-10" />
    <code value="R51"/>
  </coding>
  <coding>
    <system value="http://snomed.info/sct"/>
    <code value="25064002"/>
    <display value="Headache"/>
    <userSelected value="true"/>
  </coding>
  <text value="general headache"/>
</concept>
```

Das Beispiel zeigt gleichzeitig: ICD-10 ohne Display, SNOMED CT mit Display und `userSelected`, plus Freitext.

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 33 (06er-VL); Seite 41 (Anna Lin Starter)
