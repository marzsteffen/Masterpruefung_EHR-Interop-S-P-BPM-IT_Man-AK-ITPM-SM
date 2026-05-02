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

# MSI - HL7 CDA - Templates

> [!info] Kurzdefinition
> CDA-Templates sind definierte und wiederverwendbare Vorlagen, die als **Bausteine** in CDA-Dokumenten verwendet werden. Sie können Dokument-Strukturen, Dokumentabschnitte und einzelne Datenelemente beschreiben. Eine eindeutige **template-ID** ist essenziell für die Konformitäts­prüfung. Vier Typen: **Document Level, Header Level, Section Level, Entry Level**.

## Beschreibung

Wörtlich aus Folie 38:

> „CDA Templates sind definierte und wiederverwendbare Vorlagen, die wie Bausteine in CDA-Dokumenten verwendet werden können. Sie können Dokumentstrukturen, Dokumentabschnitte und einzelne Datenelemente beschreiben. Templates gewährleisten die Interoperabilität von CDA. **Templates werden wiederverwendet.**
>
> Templates tragen eine eindeutige **template-ID**: Essenziell für die Konformitätsprüfung
>
> ‚Vier Typen' von CDA-Templates:
> 1. **Document Level Templates** definieren die Gesamtstruktur von Dokumenten. Sie nutzen dazu die anderen Templates.
> 2. **Header Level Templates** beschreiben die administrativen Metadaten im CDA Header.
> 3. **Section Level Templates** etablieren die Abschnitte des Dokuments.
> 4. **Entry Level Templates** legen strukturierte bzw. kodierte Informationen fest, die CDA-Entries.
>
> Weitere Templates: z. B. wiederverwendbare ‚Compilations' wie Adresspartikel
> Beispiel einfach: Adress-Element, Organisations-Element"

## Bestandteile / Aufbau

| Template-Typ | Was wird beschrieben? | Beispiele |
|---|---|---|
| **Document Level** | Gesamtstruktur eines Dokuments | ELGA CDA Dokument eMedikation Rezept (`1.2.40.0.34.11.8.1`), Entlassungsbrief Ärztlich, Laborbefund, Pflegesituations­bericht (siehe Folie 40) |
| **Header Level** | Administrative Metadaten | Patient, Author, Custodian, LegalAuthenticator |
| **Section Level** | Abschnitte | Aufnahmegrund, Diagnose bei Entlassung, Allergien |
| **Entry Level** | Codierte Einzeleinträge | Laborparameter (`1.3.6.1.4.1.19376.1.3.1.6`), Problem/Bedenken (`1.2.40.0.34.11.1.3.5`), Medikation Verordnung (`1.2.40.0.34.11.8.1.3.1`), Medikation Abgabe (`1.2.40.0.34.11.8.2.3.1`) |
| **Compilations** | wiederverwendbare Substrukturen | Adress-Element, Organisations-Element, Person Name |

## Beispiel

Aus Folie 39 (Person Name Compilation G2):
- Frage: „Darf es mehr als einen family name geben?"
- Frage: „Wäre folgendes Snippet korrekt?"
```xml
<name>
  <given>Max Mustermann</given>
  <qualifier="BR"/>
  <suffix qualifier="AC">MSc</suffix>
</name>
```

(Antwort: das Snippet ist syntaktisch fehlerhaft – `<qualifier>` ist kein eigenständiges Element, sondern ein Attribut. Die Vorlesung nutzt das als Diskussionsbeispiel; der Allgemeine Leitfaden zeigt die korrekte Form.)

Aus Folie 48: Template-IDs für maschinenlesbare Inhalte:
- Laborwert: `<templateId root="1.3.6.1.4.1.19376.1.3.1.6"/>` (IHE PCC).
- Diagnose: `<templateId root="1.2.40.0.34.11.1.3.5"/>` (ELGA Problem/Bedenken Entry).
- Medikation Verordnung: `<templateId root="1.2.40.0.34.11.8.1.3.1"/>`.
- Medikation Abgabe: `<templateId root="1.2.40.0.34.11.8.2.3.1"/>`.

Aus Folie 15 (Entry-Level mit mehreren Templates):
```xml
<entry typeCode="DRIV">
  <organizer classCode="CLUSTER" moodCode="EVN">
    <templateId root="1.2.40.0.34.11.1.3.3" assigningAuthorityName="ELGA"/>
    <templateId root="1.3.6.1.4.1.19376.1.5.3.1.4.13.1" assigningAuthorityName="IHE PCC"/>
    <templateId root="2.16.840.1.113883.10.20.1.32" assigningAuthorityName="HL7 CCD"/>
    <templateId root="2.16.840.1.113883.10.20.1.35" assigningAuthorityName="HL7 CCD"/>
    <code code="46680005" codeSystem="2.16.840.1.113883.6.96"
          codeSystemName="SNOMED CT" displayName="Vital signs"/>
    ...
```

Hier sind vier Template-IDs gleichzeitig gesetzt – das Element ist gleichzeitig konform zu ELGA, IHE PCC und zwei HL7-CCD-Templates.

## Abgrenzung

- **Template ≠ XML-Schema**: Templates sind eine zusätzliche Konformitäts­schicht. Schema prüft Struktur, Templates prüfen Inhalt + Reihenfolge + Codes via Schematron.
- **Document Template ≠ Header/Section/Entry Templates**: Document referenziert die anderen drei.
- **Compilations ≠ Templates**: Compilations sind feinere Bausteine wie Adresse, die in mehreren Templates auftauchen.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche vier Template-Typen kennt CDA? Was beschreibt jeder?

**Anwendungsfrage:** Erkennen Sie an einem Snippet, welche Template-Typen verwendet werden.

**Diskussionsfrage:** Warum kann ein Element mehrere Template-IDs gleichzeitig tragen?

**Mögliche Anschlussfragen:**
- Wie werden Templates in ART-DECOR modelliert? → [[MSI - HL7 CDA - ART-DECOR]]
- Wie wird die Template-ID in Schematron-Regeln genutzt? → [[MSI - HL7 CDA - Stylesheet und Validierung]]
- Welche Wiederverwendung steckt hinter Compilations?

## Verwandt

- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - ART-DECOR]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Body und Sections]]
- [[MSI - HL7 CDA - Laborparameter Entry]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 38, 39, 15, 40, 48
