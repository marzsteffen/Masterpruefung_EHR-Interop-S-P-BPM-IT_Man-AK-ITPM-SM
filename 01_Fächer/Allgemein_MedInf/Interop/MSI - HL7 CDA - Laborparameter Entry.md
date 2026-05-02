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

# MSI - HL7 CDA - Laborparameter Entry

> [!info] Kurzdefinition
> Beispiel für maschinenlesbare Lab-Daten in einem ELGA-CDA-Befund: Hierarchie­ebene Bereich (Hämatologie) → Hierarchie­ebene Gruppe (Blutbild) → Observation mit Template-ID, LOINC-Code, PQ-Wert + UCUM-Einheit, Interpretation, Referenz­bereich. Mögliche Lab-Parameter sind im Value Set `ELGA_Laborparameter` fixiert.

## Beschreibung

Folie 49 zeigt einen vereinfachten Laborparameter-Entry mit kommentierten Bereichen:

```xml
<entry typeCode="DRIV">
  <act classCode="ACT" moodCode="EVN">
    <code code="300" codeSystem="1.2.40.0.34.5.11"
          codeSystemName="ELGA_LaborparameterErgaenzung"
          displayName="Hämatologie"/>      <!-- Hierarchieebene Bereich -->
    <statusCode code="completed"/>
    <entryRelationship typeCode="COMP">
      <organizer classCode="BATTERY" moodCode="EVN">
        <code code="03010" codeSystem="1.2.40.0.34.5.11"
              codeSystemName="ELGA_LaborparameterErgaenzung"
              displayName="Blutbild"/>      <!-- Hierarchieebene Gruppe -->
        <statusCode code="completed"/>
        <component typeCode="COMP">
          <observation classCode="OBS" moodCode="EVN">
            <templateId root="1.3.6.1.4.1.19376.1.3.1.6"/>
                                            <!-- Template-ID Lab Observation -->
            <id extension="OBS-1-1" root="2.16.840.1.113883.2.16.1.99.3.1"/>
            <code code="26464-8" codeSystem="2.16.840.1.113883.6.1"
                  codeSystemName="LOINC" displayName="Leukozyten"/>
                                            <!-- Laborparameter: LOINC 26464-8 -->
            <text><reference value="#OBS-1-1"/></text>
            <statusCode code="completed"/>
            <effectiveTime value="20121201073406+0100"/>
            <value unit="G/L" value="26" xsi:type="PQ"/>
                                            <!-- Laborwert: 26 UCUM-Einheit: G/l -->
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
                                            <!-- Referenzbereich: 4-10 G/l -->
                <interpretationCode>[...]</interpretationCode>
              </observationRange>
            </referenceRange>
          </observation>
        </component>
      </organizer>
    </entryRelationship>
  </act>
</entry>
```

Folie 51 ergänzt zur Übernahme der Laborwerte:
- Laborwerte in das Anwendungssystem übernehmen für Werte-Kurven, Kumulativbefunde, Vergleiche, Berechnungen.
- ELGA bietet mit dem Value Set ELGA_Laborparameter eine **österreichweit einheitliche Mappingtabelle** für Laboranalysen.
- Standardisierte Angaben von Einheiten durch UCUM. Achtung: Bei Übernahme auf idente Einheiten achten – Einheiten können leicht umgerechnet werden. Hilfe bei Umrechnung: `http://xml4pharmaserver.com/WebServices/UCUM_webservices.html`.

## Bestandteile / Aufbau

| Element | Funktion |
|---|---|
| Outer act | Hierarchie­ebene Bereich (z. B. Hämatologie) |
| organizer (BATTERY) | Hierarchie­ebene Gruppe (z. B. Blutbild) |
| observation | Einzelner Laborwert |
| templateId | identifiziert Template (`1.3.6.1.4.1.19376.1.3.1.6` = IHE PCC Lab Observation) |
| code | LOINC-Code des Laborparameters |
| value (PQ) | Wert + UCUM-Einheit |
| interpretationCode | HL7-Interpretation (U=increased, N=normal, L=low, …) |
| referenceRange (IVL_PQ) | Normalbereich mit low/high |

## Beispiel

Direkt aus Folie 49: Leukozyten 26 G/L (erhöht), Referenzbereich 4–10 G/L.

## Abgrenzung

- **Laborparameter Entry ≠ Laborbefund-Section**: Section gruppiert Entries; jeder Entry ist eine Einzelbeobachtung.
- **`code` ≠ `value`**: code identifiziert die Frage (LOINC), value das Ergebnis (PQ).
- **`interpretationCode` ≠ `referenceRange`**: Interpretation fasst zusammen, Referenzbereich gibt die Normwerte an.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Erklären Sie an einem Lab-Snippet die wichtigsten Elemente und welche Codes sie tragen.

**Anwendungsfrage:** Identifizieren Sie in einem Lab-Entry: LOINC-Code, UCUM-Einheit, Interpretation, Referenzbereich, Template-ID.

**Diskussionsfrage:** Was bedeutet die Hierarchie Bereich → Gruppe → Observation? Welche Konsequenzen hat sie für die Anzeige?

**Mögliche Anschlussfragen:**
- Was, wenn der lokale Lab-Code nicht im ELGA_Laborparameter-Value-Set ist? → [[MSI - HL7 CDA - Translation]]
- Welche UCUM-Einheiten sind hier erlaubt?
- Wie wird der Bewertungscode standardisiert? → [[MSI - Terminologie - Mapping in CDA]]

## Verwandt

- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - UCUM - Definition]]
- [[MSI - HL7 CDA - Translation]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - Terminologie - Mapping in CDA]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 49, 51
