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

# MSI - LOINC - Verwendung in CDA

> [!info] Kurzdefinition
> In ELGA-CDA wird LOINC für (1) Laborparameter (Value Set ELGA-Laborparameter), (2) Codierung von Dokumenten­klassen (z. B. Discharge Summary) und (3) Codierung von Sektionen (z. B. „Reason for Referral") verwendet. Das Code-Element trägt Code, codeSystem-OID, codeSystemName und displayName.

## Beschreibung

Folie 25 zeigt drei konkrete Anwendungs­fälle:

**1) Laborbefund (Observation in einer Lab-Section)**

Aus dem Folien-XML:
```
<observation classCode="OBS" moodCode="EVN">
  <templateId root="1.3.6.1.4.1.19376.1.3.1.6"/>
  <id extension="OBS-1-1" root="2.16.1.4.1.99.3.1"/>
  <code code="26464-8" codeSystem="2.16.840.1.113883.6.1"
        codeSystemName="LOINC" displayName="Leukozyten"/>
  <text><reference value="#OBS-1-1"/></text>
  <statusCode code="completed"/>
  <effectiveTime value="20121201073406+0100"/>
  <value unit="G/L" value="26" xsi:type="PQ"/>
  <interpretationCode code="U" displayName="increased"
        codeSystemName="HL7:ObservationInterpretation"
        codeSystem="2.16.840.1.113883.5.83"/>
  <referenceRange typeCode="REFV">
    <observationRange classCode="OBS" moodCode="EVN.CRT">
      <text><reference value="#OBSREF-1-1"/></text>
      <value xsi:type="IVL_PQ">
        <low value="4.0" unit="G/L"/>
        <high value="10.0" unit="G/L"/>
      </value>
      ...
```

Beachten: `code` (LOINC-Code), `codeSystem` (LOINC-OID `2.16.840.1.113883.6.1`), `codeSystemName` (`LOINC`), `displayName` (`Leukozyten`); Wert mit UCUM-Einheit (`G/L`); InterpretationCode (`U` = increased) aus HL7-Code-System; Referenzbereich als IVL_PQ-Intervall.

**2) Dokumentenklasse**

Aus dem Folien-XML:
```
<!-- Dokumentenklasse (siehe Allgemeiner Leitfaden, Kapitel 6.2.7) -->
<code code="11490-0" displayName="Physician Discharge summary"
      codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>
```

**3) Section-Codierung**

Aus dem Folien-XML:
```
<section>
  <templateId root="1.2.40.0.34.11.2.2.1" assigningAuthorityName="ELGA"/>
  <templateId root="1.3.6.1.4.1.19376.1.5.3.1.3.1"
              assigningAuthorityName="IHE PCC"/>
  <code code="42349-1" displayName="Reason for Referral"
        codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>
  <title>Aufnahmegrund</title>
```

## Bestandteile / Aufbau

In jedem CDA-`<code>`-Element:
- `code` – der eigentliche LOINC-Code (z. B. `26464-8`).
- `codeSystem` – LOINC-OID `2.16.840.1.113883.6.1`.
- `codeSystemName` – `LOINC`.
- `displayName` – sprechende Bezeichnung (im ELGA häufig deutsch).

Daneben werden Lab-Werte typisiert als `value xsi:type="PQ"` mit UCUM-Einheit (`unit="G/L"`).

## Beispiel

Drei Beispiele direkt aus der Folie (siehe oben). Die zugehörigen Value Sets sind ELGA-spezifisch, z. B. das Value Set `ELGA_Laborparameter` (Parent-OID `1.2.40.0.34.10.44`, Folie 12).

## Abgrenzung

- **LOINC in CDA ≠ LOINC in HL7 v2.** HL7 v2 codiert mit LOINC im OBX-3 (`OBX|1|NM|10839-9^Troponin-I^LN|...`, Folie 15) – syntaktisch anders, semantisch gleicher Code.
- **LOINC ≠ ELGA-Laborparameter-Value-Set.** Das Value Set ist die *Auswahl* aus LOINC, die in ELGA tatsächlich verwendet werden darf.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Anwendungs­fälle für LOINC kennt CDA?

**Anwendungsfrage:** Welche Attribute trägt ein CDA-`<code>`-Element bei LOINC-Codierung? Geben Sie die OID an.

**Diskussionsfrage:** Warum wird in ELGA *nicht* der gesamte LOINC verwendet, sondern ein Value Set?

**Mögliche Anschlussfragen:**
- Welche zusätzlichen Codes treten in einer Lab-Observation auf? (interpretationCode aus HL7, UCUM-Einheit)
- Wie wird der Referenzbereich strukturiert (`IVL_PQ`)?
- Wie sieht dieselbe Lab-Observation in FHIR aus? → [[MSI - HL7 FHIR - Resource]] (Querverweis VL 06)

## Verwandt

- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Sechs-Achsen-Struktur]]
- [[MSI - UCUM - Definition]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Identifikator - OID]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 25
