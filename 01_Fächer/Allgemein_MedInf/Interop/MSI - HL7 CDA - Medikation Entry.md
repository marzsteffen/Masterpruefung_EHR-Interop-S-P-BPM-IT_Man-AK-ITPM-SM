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

# MSI - HL7 CDA - Medikation Entry

> [!info] Kurzdefinition
> Beispiel für maschinenlesbare Medikations-Daten in einem ELGA-Entlassungsbrief: `<substanceAdministration>` mit Template-ID `1.2.40.0.34.11.8.1.3.1` (ELGA Medikation_Verordnung), MedikationTherapieArt-Code (Einzelverordnung vs. Dauermedikation), Einnahmedauer (IVL_TS), Einnahme-Frequenz (PIVL_TS), repeatNumber, doseQuantity, manufacturedProduct mit PZN-Code.

## Beschreibung

Folie 54 betont den Zweck:
- Empfohlene Medikation im Entlassungsbrief → Übernahme zur Rezeptschreibung möglich.
- Erstellung eines Einnahmeplans aus Abgaben und Verordnungen.

Folie 55 zeigt einen vereinfachten Medikation-Verordnungs-Entry:

```xml
<entry typeCode="DRIV">
  <substanceAdministration classCode="SBADM" moodCode="INT">
    <templateId root="1.2.40.0.34.11.8.1.3.1" assigningAuthorityName="ELGA"/>
                                            <!-- Template-ID für ELGA Medikation_Verordnung -->
    [...]
    <id root="1.2.40.0.10.1.4.3.4.2.2" extension="2b4x6qA2p4OLa53i4dyt_4733"/>
    <code code="EINZEL" displayName="Einzelverordnung"
          codeSystem="1.2.40.0.10.1.4.3.4.3.6"
          codeSystemName="MedikationTherapieArt"/>
                                            <!-- Einzelverordnung vs. Dauermedikation -->
    <text> <reference value="#vpos-3"/> </text>
    <statusCode code="completed"/>
    <effectiveTime xsi:type="IVL_TS">
      <low value="20130327000000+0200"/>
      <high value="20130330235959+0200"/>
    </effectiveTime>                        <!-- Einnahmedauer -->
    <effectiveTime xsi:type="PIVL_TS" operator="A" institutionSpecified="true">
      <period value="1" unit="d"/>
    </effectiveTime>                        <!-- Einnahme: 1x täglich -->
    <repeatNumber value="0"/>
    <doseQuantity value="1"/>               <!-- Einnahme: 1 Stück -->
    <consumable>
      <manufacturedProduct xmlns:pharm="urn:ihe:pharm:medication" classCode="MANU">
        [...]
        <manufacturedMaterial classCode="MMAT" determinerCode="KIND">
          <templateId root="1.2.40.0.34.11.2.3.4" assigningAuthorityName="ELGA"/>
          [...]
          <code code="889900" displayName="Novalgin"
                codeSystem="1.2.40.0.34.4.16" codeSystemName="Pharmazentralnummer">
            <originalText> <reference value="#prodcode-3"/> </originalText>
          </code>                           <!-- Arzneispezialität -->
          <name>Novalgin Tropfen</name>
        </manufacturedMaterial>
      </manufacturedProduct>
    </consumable>
  </substanceAdministration>
</entry>
```

Beachten: zwei `<effectiveTime>`-Elemente. Erstes ist `IVL_TS` (Zeitintervall low/high) für die Einnahmedauer. Zweites ist `PIVL_TS` (Periodic Interval of Time) mit `period value="1" unit="d"` für „1 Mal täglich".

## Bestandteile / Aufbau

| Element | Bedeutung |
|---|---|
| `substanceAdministration` (classCode SBADM, moodCode INT = Intent) | Verordnung (Intent) |
| `templateId` | ELGA Medikation_Verordnung |
| `code` (MedikationTherapieArt) | EINZEL vs. DAUER |
| `effectiveTime IVL_TS` | Einnahmedauer (low/high) |
| `effectiveTime PIVL_TS` | Frequenz (z. B. `period value="1" unit="d"`) |
| `repeatNumber` | Anzahl Wiederholungen |
| `doseQuantity` | Stückzahl pro Einnahme |
| `manufacturedProduct/manufacturedMaterial/code` | PZN-Code des Arzneimittels |

## Beispiel

Aus Folie 55: Novalgin Tropfen, PZN `889900`, 1 Stück, 1× täglich, Einnahme 27.–30.03.2013, Einzelverordnung.

## Abgrenzung

- **`moodCode="INT"` ≠ `moodCode="EVN"`**: INT (Intent) = geplante Verordnung; EVN (Event) = tatsächlich verabreichte Medikation. Verordnung vs. Abgabe sind unterschiedliche Acts mit unterschiedlichen moodCodes und Templates (ELGA Medikation_Verordnung vs. ELGA Medikation_Abgabe).
- **PIVL_TS ≠ IVL_TS**: PIVL_TS modelliert periodische Wiederholung, IVL_TS einen Zeitraum.
- **manufacturedProduct vs. manufacturedMaterial**: Product wrappt Material; classCode MMAT, determinerCode KIND zeigt, dass es ein „Kind"-Material ist (Klasse, nicht spezifische Charge).

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Wie ist ein ELGA-Medikations-Verordnungs-Entry strukturiert? Welche Template-ID, welche Pflichtelemente?

**Anwendungsfrage:** Erklären Sie die zwei `effectiveTime`-Elemente in einem Medikation-Entry.

**Diskussionsfrage:** Welcher Unterschied liegt zwischen einer Verordnung (Intent) und einer Abgabe (Event)? Welche Konsequenzen hat das für den Einnahmeplan?

**Mögliche Anschlussfragen:**
- Was ist eine PZN? → [[MSI - Identifikator - Übersicht eHealth]]
- Wie passen Verordnung und Abgabe zur eMedikation? (eMedikation umfasst Rezept, Abgabe, Medikationsliste, Pharmazeutische Empfehlung – siehe Folie 40)
- Wie wird die Frequenz codiert?

## Verwandt

- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - Datentypen]] (PIVL_TS, IVL_TS)
- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - Identifikator - Übersicht eHealth]] (PZN)
- [[MSI - HL7 RIM - Reference Information Model]] (substanceAdministration als Act-Klasse)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 54, 55
