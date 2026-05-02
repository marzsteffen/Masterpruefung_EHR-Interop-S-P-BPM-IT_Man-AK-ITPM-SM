---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 CDA - Aufbau

> [!info] Kurzdefinition
> Ein CDA-Dokument besteht aus zwei Hauptteilen: **Header** (administrative Metadaten – Patient, GDA, Erstellungsdatum, Custodian, Authenticator …) und **Body** (medizinische Inhalte). Der Body kann strukturiert sein und enthält **Sections** mit lesbarem **Narrative Block** (`<text>`) und maschinenlesbaren **Entries** (Clinical Statements wie Observation, Procedure, Encounter, Medication).

## Beschreibung

Folie 4 zeigt den schematischen Aufbau:

- **Header**: Administrative Metadaten – Patient, GDA, Erstellungsdatum, … Verlinkt auf Patient-Entity, Autor (Arzt), Body Structures.
- **Body**: Strukturierter Body mit Body Entries (Clinical Statements).
- **Body Entries**: Observation, Procedure, Encounter, Medication, …
- **External References**: External Observation, External Procedure, External Document.

Folie 5 zeigt die XML-Sicht:
```
<ClinicalDocument>
  ...                                  <!-- Header -->
  <structuredBody>
    <section>                          <!-- Section -->
      <text>...</text>                 <!-- Narrative Block -->
      <observation>                    <!-- Clinical Statement (Entry) -->
        ...
      </observation>
      <observation>
        ...
      </observation>
    </section>
    <section>
      <section>                        <!-- verschachtelte Sections möglich -->
        ...
      </section>
    </section>
  </structuredBody>
</ClinicalDocument>
```

Drei wesentliche Ebenen: **Document** → **Body** → **Section** → **Entry** (Clinical Statement). Sections können verschachtelt sein. Jede Section hat einen Narrative Block (`<text>`, lesbar) und optional Entries (codiert/strukturiert).

## Bestandteile / Aufbau

| Element | Inhalt | Beispielsweise |
|---|---|---|
| `<ClinicalDocument>` | Wurzel | – |
| Header (im Wurzelelement) | Patient, Autor, Custodian, Authenticator, recordTarget, encompassingEncounter, … | siehe [[MSI - HL7 CDA - Header]] |
| `<structuredBody>` | Wrapper für Sections | – |
| `<section>` | Abschnitt mit definierter Bedeutung | „Aufnahmegrund", „Diagnose bei Entlassung" |
| `<text>` | Narrative Block (lesbar) | menschenlesbarer Befundtext |
| `<observation>`, `<procedure>`, `<encounter>`, `<medication>` | Clinical Statements | codierte Befunde |

## Beispiel

Aus Folie 15 (Beispiel ELGA-Body):
```
<component>
  <section>
    <templateId root="1.2.40.0.34.11.3.2.15" assigningAuthorityName="ELGA"/>
    <code code="PFMED" displayName="Medikamentenverabreichung"
          codeSystem="1.2.40.0.34.5.40" codeSystemName="ELGA_Sections"/>
    <title>Medikamentenverabreichung</title>
    <text>Klient nimmt Medikamente selbstständig ein. Er führt auch die Inhalationen selbst durch.</text>
  </section>
</component>
```

## Abgrenzung

- **Header ≠ Body**: Header trägt Metadaten (wer, wann, wofür), Body trägt klinische Inhalte (was wurde dokumentiert).
- **Section ≠ Entry**: Section ist ein lesbarer Abschnitt mit Titel und Narrativ; Entries sind die maschinenlesbaren Einzeldatenelemente innerhalb einer Section.
- **`<structuredBody>` ≠ `<nonXMLBody>`**: structuredBody enthält Sections; nonXMLBody enthält nur ein eingebettetes PDF/Bild → CDA-Level 1.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Skizzieren Sie den Aufbau eines CDA-Dokuments.

**Anwendungsfrage:** Erklären Sie an einem Section-Snippet, welche Teile Header, Body, Section, Narrative Block, Entry sind.

**Diskussionsfrage:** Warum hat eine Section sowohl Narrative Block (`<text>`) als auch Entries? Welche Rolle spielen sie für Lesbarkeit vs. Maschinenverarbeitung?

**Mögliche Anschlussfragen:**
- Wie hängen Body Entries und External References zusammen?
- Welche Clinical-Statement-Klassen kennen Sie?
- Wie verhält sich der Narrative Block zur Authentisierung des Dokuments? → [[MSI - HL7 CDA - Eigenschaften]] („wholeness" und „human readability")

## Verwandt

- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Header]]
- [[MSI - HL7 CDA - Body und Sections]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - HL7 RIM - Reference Information Model]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 4, 5, 15
