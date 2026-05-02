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

# MSI - HL7 FHIR - Terminology Binding Strength

> [!info] Kurzdefinition
> Vier Stufen der Bindungsstärke (Binding Strength) zwischen einem FHIR-Element und einem Value Set: **required**, **extensible**, **preferred**, **example**. Sie definieren, wie verbindlich der Code aus dem Value Set gewählt werden muss.

## Beschreibung

Folie 36 fasst die vier Stufen zusammen:

| Strength | Bedeutung |
|---|---|
| **required** | „To be conformant, the concept in this element SHALL be from the specified value set." |
| **extensible** | „To be conformant, the concept in this element SHALL be from the specified value set if any of the codes within the value set can apply to the concept being communicated. If the value set does not cover the concept (based on human review), alternate codings (or, data type allowing, text) may be included instead." |
| **preferred** | „Instances are encouraged to draw from the specified codes for interoperability purposes but are not required to do so to be considered conformant." |
| **example** | „Instances are not expected or even encouraged to draw from the specified value set. The value set merely provides examples of the types of concepts intended to be included." |
| **Nichts** | Kein Value Set angegeben – Frei verwendbar (kein Binding). |

Die Vorlesung zitiert Benson & Grieve:

> „It is amazing how often everyone agrees that a coded element is essential for exchange, but there is no prospect of agreeing to a value set for said exchange."

→ „Sehr häufig nur Empfehlungen bzw. Beispiele". Daher: „Muss für den Use Case spezifiziert werden (z. B. nationale Ebene, FHIR-Profil oder IHE-Profil)."

Aus Folie 35 (Patient-Beispiele):
- `Patient.gender` / `Patient.contact.gender` → AdministrativeGender, **Required**.
- `Patient.maritalStatus` → MaritalStatus, **Extensible**.
- `Patient.contact.relationship` → PatientContactRelationship, **Extensible**.
- `Patient.communication.language` → AllLanguages, **Preferred** (limited to AllLanguages).
- `Patient.link.type` → LinkType, **Required**.
- Observation:
  - `status` → ObservationStatus, **Required**.
  - `category` → Observation Category Codes, **Preferred**.
  - `code` → LOINC Codes, **Example**.

## Bestandteile / Aufbau

| Strength | Hierarchie | Konformität | Praxis |
|---|---|---|---|
| required | strikt | SHALL aus Value Set | Pflicht-Bindings für globale Vokabulare (z. B. gender) |
| extensible | mittel | SHALL aus Value Set, wenn passend; sonst alternate codings/text | Standard für „normalerweise reicht das Value Set" |
| preferred | schwach | empfohlen, kein Konformitäts-Pflicht | Wenn das Value Set hilfreich ist, aber lokale Variation erwartet |
| example | informativ | nicht verpflichtend, nur Hinweis | Wenn jede Lokalimplementierung eigene Value Sets braucht |
| (nichts) | keines | vollständig frei | Kein Value Set spezifiziert – Implementierung wählt selbst |

## Beispiel

Aus Folie 35:
- `Observation.code` ist mit **Example**-Bindung an LOINC gebunden – heißt: in der Praxis muss jede Implementierung ein eigenes Value Set definieren (z. B. ELGA_Laborparameter).
- `Observation.status` ist **Required** an ObservationStatus – muss strikt eingehalten werden.

## Abgrenzung

- **Required ≠ Extensible**: required ist auch dann verpflichtend, wenn der Code unpassend ist; extensible erlaubt den Wechsel auf alternate codings.
- **Preferred ≠ Example**: preferred ist eine Empfehlung; example ist nur ein „so-könnte-es-aussehen".
- **Strength ≠ Cardinality**: Strength sagt, *wie* der Code zu wählen ist; Cardinality, *wie viele* Codes erlaubt sind.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche Binding Strengths kennt FHIR (inkl. „kein Binding")? Was sagt jede aus?

**Anwendungsfrage:** Welche Binding Strength erwarten Sie für (a) Patient.gender, (b) Observation.code für Lab, (c) Patient.maritalStatus?

**Diskussionsfrage:** Warum sind Bindings im FHIR-Standard oft nur Beispiele/Empfehlungen?

**Mögliche Anschlussfragen:**
- Was bedeutet das Benson-&-Grieve-Zitat im Kontext realer Implementierungen?
- Wie verhält sich „required" zum CDA-„DYNAMIC"-Binding? → [[MSI - HL7 CDA - Terminology Binding]]
- Welche Stufe wird typischerweise in IHE-Profilen oder nationalen Implementierungs­leitfäden verschärft?

## Verwandt

- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 CDA - Terminology Binding]] (CDA-Pendant DYNAMIC/STATIC)
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 35, 36 (06er-VL, inkl. Zitat Benson & Grieve); Seite 54 (Anna Lin Starter, 5. Option „Nichts")
