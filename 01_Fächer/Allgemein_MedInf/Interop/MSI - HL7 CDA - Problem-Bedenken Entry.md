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

# MSI - HL7 CDA - Problem-Bedenken Entry

> [!info] Kurzdefinition
> Beispiel für maschinenlesbare Diagnose-Daten in einem ELGA-CDA-Befund. Outer Act mit Template-IDs `1.2.40.0.34.11.2.3.1` und `1.2.40.0.34.11.1.3.5` (ELGA Problem/Bedenken). Innere Observation mit SNOMED-CT-Konzept `282291009` (Diagnosis), Status, Zeitraum und ICD-10-Wert. Diagnose-Codierung in ELGA primär ICD-10, Translation in SNOMED möglich.

## Beschreibung

Folie 52 zeigt einen vereinfachten Problem-Bedenken-Entry mit kommentierten Bereichen:

```xml
<entry>
  <act classCode="ACT" moodCode="EVN">
    <templateId root="1.2.40.0.34.11.2.3.1" assigningAuthorityName="ELGA"/>
    <templateId root="1.2.40.0.34.11.1.3.5" assigningAuthorityName="ELGA"/>
                                            <!-- Template-ID für ELGA Problem/Bedenken -->
    [...]
    <id root="002D59AE-7CC4-2439-21B1-597B76C4187E"/>
    <code nullFlavor="NA"/>
    <statusCode code="active"/>             <!-- Status: aktiv -->
    <effectiveTime>
      <low value="20130111"/>
    </effectiveTime>
    <entryRelationship inversionInd="false" typeCode="SUBJ">
      <observation classCode="OBS" moodCode="EVN" negationInd="false">
        <templateId root="1.2.40.0.34.11.1.3.6" assigningAuthorityName="ELGA"/>
        [...]
        <id root="DBA414DE-6B92-4D74-30D1-46BC36770F79"/>
        <code code="282291009" displayName="Diagnosis"
              codeSystem="2.16.840.1.113883.6.96" codeSystemName="SNOMED CT"/>
                                            <!-- Codiert: das ist eine Diagnose -->
        <text> <reference value="#disdiag2"/> </text>
        <statusCode code="completed"/>
        <effectiveTime>
          <low value="20120111"/>
          <high value="20130211"/>           <!-- Zeitraum der Diagnose -->
        </effectiveTime>
        <value xsi:type="CD" code="M54.9" displayName="Rückenschmerzen, nicht näher bezeichnet"
               codeSystem="1.2.40.0.34.5.56" codeSystemName="ICD-10 BMG 2014">
                                            <!-- Diagnose: ICD M54.9 -->
          <originalText> <reference value="#disdiag2 diagnosis"/> </originalText>
          <qualifier>
            <name code="8" codeSystem="2.16.840.1.113883.3.7.1.0"/>
            <value code="V" codeSystem="2.16.840.1.113883.3.7.1.8"/>
          </qualifier>                       <!-- Diagnosesicherheit: Verdacht auf -->
        </value>
      </observation>
    </entryRelationship>
  </act>
</entry>
```

Folie 53 ergänzt:
- Für die Codierung der Diagnosen ist **ICD-10** im Leitfaden fixiert.
- **„Translation" möglich** – siehe [[MSI - HL7 CDA - Translation]].
- Wichtig: Alle Informationen in lokales System übernehmen!
  - Diagnosesicherheit: Gesichert oder nur Verdacht?
  - Seitigkeit: rechts oder links?
  - Status: noch aktiv oder schon abgeschlossen?

## Bestandteile / Aufbau

Zwei-Stufen-Struktur:

**Outer Act** (Container für Problem/Bedenken):
- `templateId` ELGA Problem/Bedenken Concern Entry.
- `id` für den Container.
- `statusCode` z. B. `active`.
- `effectiveTime` Beobachtungs­zeitraum.

**Inner Observation** (eigentliche Diagnose):
- `templateId` Diagnose-Observation.
- `code` SNOMED `282291009` (Diagnosis) – qualifiziert das Element als Diagnose.
- `statusCode` z. B. `completed`.
- `effectiveTime` low/high.
- `value xsi:type="CD"` mit ICD-10-Code.
- `qualifier` für Diagnose-Sicherheit (gesichert/Verdacht).

## Beispiel

Aus Folie 52: M54.9 „Rückenschmerzen, nicht näher bezeichnet", Verdacht auf, Beobachtungs­zeitraum 11.01.2012 – 11.02.2013.

## Abgrenzung

- **Outer Act ≠ Inner Observation**: Outer Act ist der Concern-Container, Inner Observation ist die konkrete Diagnose-Aussage.
- **`code` (Observation) ≠ `value` (Observation)**: code = „das ist eine Diagnose" (SNOMED 282291009 als Type-Codierung); value = die konkrete Diagnose (ICD-10 M54.9).
- **`statusCode` (Outer = active) ≠ `statusCode` (Inner = completed)**: outer beschreibt das Anhalten der Beobachtung, inner die Vollendung der Aussage.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Erklären Sie an einem Snippet die Struktur eines Problem-Bedenken-Entries: outer Act, Inner Observation, code vs. value, qualifier.

**Anwendungsfrage:** Welche Pflichtinformationen muss ein lokales System bei der Übernahme einer maschinenlesbaren Diagnose erfassen?

**Diskussionsfrage:** Warum wird im `<code>` der Observation `282291009 Diagnosis` und im `<value>` der eigentliche ICD-10-Code geführt? Welche Trennung erlaubt das?

**Mögliche Anschlussfragen:**
- Welche Diagnose-Sicherheits-Codes gibt es? (z. B. „V" = Verdacht, codiert über `2.16.840.1.113883.3.7.1.8`)
- Wie verhält sich Translation zu diesem Entry? → [[MSI - HL7 CDA - Translation]]
- Was bedeutet `negationInd="false"`?

## Verwandt

- [[MSI - HL7 CDA - Translation]]
- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - Datentypen]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 52, 53
