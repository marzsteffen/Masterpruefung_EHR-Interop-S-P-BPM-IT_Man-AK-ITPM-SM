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

# MSI - HL7 FHIR - Datentyp Coding

> [!info] Kurzdefinition
> `Coding` repräsentiert ein definiertes Konzept als Symbol aus einem definierten Codesystem. Felder: **system (URI)**, **version (string)**, **code (code)**, **display (string)**, **userSelected (boolean)**. Wird selten direkt verwendet – meist innerhalb eines `CodeableConcept`.

## Beschreibung

Wörtlich aus Folie 34:

> „enthält einen Code sowie
> dessen CodeSystem-URI und ggf. Version
> einen Display-Value und das User-Selected-Flag (bei mehreren alternativen Codings in einem CodableConcept)
> selten direkt verwendet (meist im CodableConcept)"

Tabelle aus Folie 34:

| Name | Flags | Card. | Type | Description |
|---|---|---|---|---|
| Coding | Σ N | – | Element | Reference to a code defined by a terminology system |
| system | Σ | 0..1 | uri | Identity of the terminology system |
| version | Σ | 0..1 | string | Version of the system – if relevant |
| code | Σ | 0..1 | code | Symbol in syntax defined by the system |
| display | Σ | 0..1 | string | Representation defined by the system |
| userSelected | Σ | 0..1 | boolean | If this coding was chosen directly by the user |

## Bestandteile / Aufbau

| Feld | Datentyp | Bedeutung |
|---|---|---|
| `system` | uri | Identifiziert das Codesystem (z. B. `http://loinc.org`) |
| `version` | string | Version des Codesystems, falls relevant |
| `code` | code | Der Code-Wert |
| `display` | string | Lesbarer Anzeigename |
| `userSelected` | boolean | Wurde dieser Coding-Eintrag vom Anwender ausgewählt? |

## Beispiel

Aus Folie 31 (LOINC-Coding):
```json
{
  "system" : "http://loinc.org",
  "version" : "2.62",
  "code" : "55423-8",
  "display" : "Number of steps in unspecified time Pedometer"
}
```

## Abgrenzung

- **Coding ≠ code**: Coding ist ein komplexer Datentyp; `code` ein primitiver String.
- **Coding ≠ CodeableConcept**: CodeableConcept enthält 0..n Codings + optionalen text. Reine `Coding`-Elemente kommen direkt selten vor.
- **userSelected unterscheidet alternative Codings**: in einem CodeableConcept mit mehreren Codings sagt `userSelected: true` an *einem* Coding, dass dieser gewählt wurde – die anderen sind alternativ/translation.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Welche Felder hat ein FHIR-Coding-Element?

**Anwendungsfrage:** Erklären Sie das `userSelected`-Flag.

**Diskussionsfrage:** Warum wird Coding selten direkt, sondern meist im CodeableConcept verwendet? (Antwort: Mehrfach-Codierung + Freitext sind im klinischen Alltag häufig.)

**Mögliche Anschlussfragen:**
- Wie wird das Codesystem identifiziert? (URI, in FHIR Standard)
- Wie verhält sich Coding zu CDA's `<code>`-Element? → [[MSI - HL7 CDA - Codierte Werte]]
- Was bedeutet der Σ-Flag? (Summary – Element ist Teil der Element-Summary einer Resource.)

## Verwandt

- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]
- [[MSI - HL7 CDA - Codierte Werte]]

## Ergänzung aus Anna-Lin-Gastvortrag

**XML-Beispiel für Coding-Datentyp** (Seite 40):

- Coding-Element mit explizitem System-Attribut (ICD-10) und Code:

```xml
<code>
  <system value="http://hl7.org/fhir/sid/icd-10" />
  <code value="G44.1" />
</code>
```

Vergleich zum primitiven `code`: hier ist das Codesystem explizit im Element angegeben, nicht implizit durch das Profil.

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 31, 34 (06er-VL); Seite 40 (Anna Lin Starter)
