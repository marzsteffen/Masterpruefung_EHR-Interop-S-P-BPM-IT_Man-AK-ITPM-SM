---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Terminologien Anwendung]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Identifikator - OID

> [!info] Kurzdefinition
> OID (*Object Identifier*) ist eine global eindeutige, hierarchisch aufgebaute Zeichenkette zur Identifikation von Code Systemen, Value Sets, Templates, Standards-Artefakten u. v. m. In CDA wird jedes verwendete Code System über eine OID referenziert; bei Sinnänderungen muss eine neue OID vergeben werden.

## Beschreibung

OID werden in der Vorlesung 03 an mehreren Stellen verwendet. Folie 6 listet sie unter „Systeme zur eindeutigen Identifizierung" auf, Folie 10 erklärt ihre Rolle für Code Systeme:

> „Codesysteme … werden durch eine ID (bei CDA: OID) eindeutig identifiziert; bei Löschungen oder Sinnänderungen von Codes muss dem Codesystem eine neue OID gegeben werden."

Folie 10 ergänzt für Value Sets:

> „werden durch einen Namen identifiziert (zusätzlich auch OID und/oder URL)"

OID werden im CDA-Beispiel (Folie 25) als `codeSystem`-Attribut verwendet (`2.16.840.1.113883.6.1` für LOINC).

> Hinweis Quelltreue: Die Vorlesung 03 enthält keine eigene Definition des OID-Aufbaus (Punkt-getrennte Hierarchie ISO/IEC 9834). Die Folien zeigen OIDs nur als Beispiele.

## Bestandteile / Aufbau

| OID-Beispiel aus den Folien | Identifiziert |
|---|---|
| `2.16.840.1.113883.6.1` | LOINC (Code System) |
| `2.16.840.1.113883.6.8` | UCUM |
| `2.16.840.1.113883.5.83` | HL7 ObservationInterpretation |
| `1.2.40.0.34.5.38` | APPC |
| `1.2.40.0.34.10.4` | Value Set ELGA_AdministrativeGender |
| `1.2.40.0.34.10.11` | Value Set ELGA_MaritalStatus |
| `1.2.40.0.34.10.180` | Value Set ELGA_AllergyOrIntoleranceAgent |
| `1.2.40.0.34.10.44` | Value Set ELGA_Laborparameter (Parent-OID) |
| `1.3.6.1.4.1.19376.1.3.1.6` | Template-ID Lab Observation (IHE PCC) |
| `2.16.1.4.1.99.3.1` | Lab-Observation-Identifier-Root |

Die Hierarchie ist hier sichtbar: `1.2.40.0.34.*` ist österreich-spezifisch (ELGA, APPC); `2.16.840.1.113883.*` ist HL7-international; `1.3.6.1.4.1.19376.*` ist IHE.

## Beispiel

Aus Folie 25 (CDA-Beispiel):
```
<code code="26464-8" codeSystem="2.16.840.1.113883.6.1"
      codeSystemName="LOINC" displayName="Leukozyten"/>
```
Die OID `2.16.840.1.113883.6.1` ist der eindeutige Identifier für LOINC – nur damit kann der Empfänger sicher sein, dass `26464-8` aus LOINC kommt und nicht aus einem anderen System mit demselben Code-Wert.

## Abgrenzung

- **OID ≠ URL**: In FHIR werden Code Systems typischerweise per URL identifiziert (z. B. `http://loinc.org`); CDA verwendet OIDs. Die Folie 10 zeigt: Value Sets können *zusätzlich* eine URL haben.
- **OID ≠ UUID**: UUIDs sind 128-Bit-Zufalls­identifikatoren, OIDs sind hierarchische ISO-Zeichenketten. Beide können eindeutig sein, sind aber unterschiedliche Standards.
- **OID ≠ Versions­nummer**: Eine OID identifiziert das Code System dauerhaft; bei Sinnänderungen wird eine *neue* OID vergeben (siehe Cimino's Concept Permanence → [[MSI - Terminologie - Cimino Desiderata]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine OID, und wozu wird sie in CDA verwendet?

**Anwendungsfrage:** Erklären Sie die Bedeutung der OID `2.16.840.1.113883.6.1` in einem CDA-`<code>`-Element.

**Diskussionsfrage:** Warum bekommt ein Code System bei Sinnänderungen eine neue OID? Welches Cimino-Desideratum steht dahinter?

**Mögliche Anschlussfragen:**
- Wie unterscheiden sich OID-Bereiche für HL7-international, IHE, ELGA?
- Wie verwendet FHIR Identifikatoren? (URL statt OID, im PDF nicht detailliert)
- Welche Rolle hat termgit.elga.gv.at für österreichische OIDs?

## Verwandt

- [[MSI - Identifikator - Übersicht eHealth]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - LOINC - Verwendung in CDA]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 6, 10, 11, 12, 25
