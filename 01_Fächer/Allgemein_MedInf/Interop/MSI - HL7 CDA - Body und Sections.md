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

# MSI - HL7 CDA - Body und Sections

> [!info] Kurzdefinition
> Der CDA-Body trägt die medizinischen Inhalte. Er ist in **Sections** gegliedert (Abschnitte mit fester Bedeutung wie „Aufnahmegrund", „Diagnose bei Entlassung"). Jede Section hat einen **Narrative Block** (`<text>` für Lesbarkeit) und optional **Entries** (codierte Clinical Statements). ELGA legt für jeden Dokumenttyp die zulässigen Sections und ihre Optionalität (M/R/O/R2) fest.

## Beschreibung

Folie 13 zeigt am Beispiel ELGA Entlassungsbrief Ärztlich, welche Sections vorgeschrieben sind:

**Epikrise** (Pflicht-Bereich):
- [O] Brieftext
- [M] Aufnahmegrund
- [M] Diagnose bei Entlassung
- [O] Rehabilitationsziele
- [O] Outcome Measurement
- [O] Durchgeführte Maßnahmen
- [M]⁵ Letzte Medikation
- [M]⁶ Empfohlene Medikation
- [M] Weitere empfohlene Maßnahmen mit Subsections [R2]: Termine/Kontrollen/Wiederbestellung, Entlassungszustand, Empfohlene Anordnungen an die weitere Pflege
- [O] Zusammenfassung des Aufenthalts
- [O] Abschließende Bemerkungen

**Sekundäre Sektionen** (zusätzlich):
- [R2] Allergien, Unverträglichkeiten und Risiken
- [O] Erhobene Befunde mit Subsections [R2]: Ausstehende Befunde, Auszüge aus erhobenen Befunden, Operationsbericht, Beigelegte erhobene Befunde, Vitalparameter
- [O] Anamnese
- [O] Frühere Erkrankungen mit Subsection [O] „Bisherige Maßnahmen"
- [O] Medikation bei Einweisung
- [O] Verabreichte Medikation während des Aufenthalts
- [O] Patientenverfügungen und andere juridische Dokumente
- [O] Beilagen

**Optionalitäts-Codes:**
- M = Mandatory (Pflicht)
- R2 = Required if (bedingt erforderlich)
- O = Optional

Sections sind verschachtelbar (`<section>` innerhalb `<section>`).

## Bestandteile / Aufbau

```xml
<structuredBody>
  <component>
    <section>
      <templateId .../>
      <code .../>          <!-- Section-Klassifikation, oft LOINC -->
      <title>...</title>   <!-- menschenlesbarer Sectiontitel -->
      <text>...</text>     <!-- Narrative Block, lesbar -->
      <entry>              <!-- maschinenlesbar -->
        <observation .../>
      </entry>
    </section>
  </component>
</structuredBody>
```

## Beispiel

Aus Folie 25 (Section-Beispiel mit doppeltem templateId für ELGA + IHE PCC):
```xml
<section>
  <templateId root="1.2.40.0.34.11.2.2.1" assigningAuthorityName="ELGA"/>
  <templateId root="1.3.6.1.4.1.19376.1.5.3.1.3.1"
              assigningAuthorityName="IHE PCC"/>
  <code code="42349-1" displayName="Reason for Referral"
        codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>
  <title>Aufnahmegrund</title>
```

## Abgrenzung

- **Section ≠ Entry**: Section ist die Abschnitts-Struktur, Entry ist der einzelne maschinenlesbare Datensatz innerhalb der Section.
- **Section-`<text>` ≠ Section-`<entry>`**: text ist menschenlesbarer Narrative; entry ist codiertes Clinical Statement. Beide können nebeneinander stehen und beschreiben dieselbe klinische Aussage.
- **`<component>` vs. `<section>`**: `<component>` ist der RIM-strukturelle Wrapper, `<section>` der inhaltliche Block. Im XML-Stack: structuredBody > component > section.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Wie ist der Body eines ELGA-Entlassungsbriefs aufgebaut? Welche Sections sind verpflichtend?

**Anwendungsfrage:** Erklären Sie an einem Section-Snippet die Rolle von templateId, code, title, text und entry.

**Diskussionsfrage:** Warum hat eine Section sowohl Narrative Block als auch Entry? Welche Risiken bestehen, wenn die beiden voneinander abweichen?

**Mögliche Anschlussfragen:**
- Welche Optionalitäts-Codes verwendet ELGA?
- Wie verhalten sich Sections und Templates zueinander? → [[MSI - HL7 CDA - Templates]]
- Welche LOINC-Codes werden für Section-Klassifikation verwendet?

## Verwandt

- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - LOINC - Verwendung in CDA]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 13, 25
