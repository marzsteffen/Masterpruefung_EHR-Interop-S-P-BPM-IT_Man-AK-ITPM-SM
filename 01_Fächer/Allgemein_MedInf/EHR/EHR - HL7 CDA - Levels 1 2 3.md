---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - CCR und CCD]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - HL7 CDA - Levels 1 2 3

> [!info] Kurzdefinition
> CDA-Dokumente lassen sich in drei **Strukturierungs-Levels** einordnen: **Level 1** (rein narrativ), **Level 2** (mit kodierten Sektionen), **Level 3** (mit strukturierten Entries). Höhere Levels = mehr Strukturierung = mehr maschinelle Verarbeitbarkeit.

## Beschreibung

CDA (Clinical Document Architecture) erlaubt eine schrittweise Steigerung des Strukturierungsgrads. Die Levels sind kumulativ – Level 3 enthält automatisch Level 1 und Level 2.

In der Vorlesung [[EHR - VL - CCR und CCD]] wurde CDA und sein RIM-Bezug eingeführt, die Level-Stufung selbst aber nicht behandelt. Diese Note ergänzt die Levels aus dem CDA-Standard.

## Bestandteile / Aufbau

| Level | Was wird strukturiert? | Charakter | Maschinelle Verarbeitbarkeit |
|---|---|---|---|
| **Level 1** | Nur Header (Patient, Author, Custodian, Encounter) + Body als unstrukturiertes Narrative oder PDF-Attachment | menschen-lesbar, „CDA als Dokumenten-Hülle" | gering – nur Metadaten |
| **Level 2** | Body in **Sections** unterteilt; jede Section trägt einen LOINC-Section-Code + Narrative-Block | strukturierte Inhaltsverzeichnis-Logik | mittel – Sections können maschinell adressiert werden, Inhalt aber nicht |
| **Level 3** | Innerhalb der Sections existieren **strukturierte Entries** (Observations, Substance Administrations, Procedures) mit kodierten Werten | voll strukturiert, RIM-konform | hoch – jeder einzelne Datenpunkt ist auswertbar |

## Beispiel

Diagnose „Hypertonie" auf den verschiedenen Levels:

**Level 1:**
> „Der Patient leidet seit 2018 an arterieller Hypertonie." (nur Fließtext)

**Level 2:**
> Section: „Active Problems" (LOINC 11450-4)
> Narrative: „Der Patient leidet seit 2018 an arterieller Hypertonie."
> → Section ist klassifiziert, Inhalt aber unstrukturiert.

**Level 3:**
> Section: „Active Problems" (LOINC 11450-4)
> Narrative: „Der Patient leidet seit 2018 an arterieller Hypertonie."
> Entry: `<observation classCode="OBS" moodCode="EVN">`
>   `<code code="38341003" codeSystem="2.16.840.1.113883.6.96"/>` (SNOMED-CT „Hypertensive disorder")
>   `<effectiveTime value="2018"/>`
>   `<value xsi:type="CD" code="..."/>`
> → kodiert, automatisiert auswertbar.

## Verbindung zur Interoperabilität

Die CDA-Levels bilden direkt die Schichten von **struktureller und semantischer Interoperabilität** ab (siehe [[EHR - Interoperabilität - Strukturell vs Semantisch]]):

| CDA-Level | LCIM-Schicht ([[EHR - Interoperabilität - LCIM nach Tolk]]) | Strukturell/Semantisch |
|---|---|---|
| Level 1 | Technical Integration | strukturell minimal, keine Semantik |
| Level 2 | Technical Integration + Section-Semantik | strukturell + Teil-Semantik |
| Level 3 | Syntax & Semantics | voll strukturell + voll semantisch |

→ Erst auf Level 3 wird CDA zu einem Backbone für Process Composability nutzbar.

## Abgrenzung

- **CDA-Level ≠ Document Type:** Ein CCD (siehe [[EHR - CCD - Continuity of Care Document]]) muss Level-3-strukturiert sein, wenn er CMS-MU-Anforderungen erfüllen soll. Ein Discharge Summary kann theoretisch Level 1 sein, ist im US-MU-Kontext aber zunehmend Level 3.
- **CDA-Level ≠ FHIR-Maturity-Levels:** FHIR hat eigene Maturity-Levels für Resource-Stabilität – das ist eine andere Dimension.
- **CDA-Level kumulativ:** Level 3 enthält Level 1 + Level 2. Ein Dokument auf Level 3 ist immer auch menschen-lesbar (Narrative bleibt Pflicht).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Levels unterscheidet CDA, und was charakterisiert jedes?

**Anwendungsfrage:** Auf welchem Level müsste ein CCD im Rahmen von Meaningful Use mindestens sein, damit Lab-Ergebnisse maschinell ausgewertet werden können?

**Diskussionsfrage:** Level 1 ist „nur PDF im XML-Mantel" – warum ist das überhaupt als CDA spezifiziert? Welcher pragmatische Wert steckt darin?

**Mögliche Anschlussfragen:**
- Wie verhält sich CDA Level 1/2/3 zu LCIM (Tolk)?
- Welche LOINC-Codes klassifizieren typische CDA-Sections? (z. B. 11450-4 Problems, 10160-0 Medications, 30954-2 Lab Results, 8716-3 Vital Signs, 18776-5 Treatment Plan)
- Wie unterscheidet sich der Mehraufwand für Level-3-Implementierung gegenüber Level 1?
- Welche Konsequenzen für Migrations­strategien zu FHIR ergeben sich aus dem Level eines existierenden CDA-Bestands?

## Ergänzung außerhalb der Vorlesung

Die Level-Stufung ist nicht im PDF SS24_CCR-CCD.pdf ausgeführt – sie ist Bestandteil der HL7 CDA Release 2 Spezifikation. Sie wird in praktisch jedem CDA-Lehrwerk und auch in den ELGA-Implementation Guides referenziert. Die Stufung ist **klassisch und prüfungsrelevant**, weil sie den Übergang von rein narrativer zu voll maschinen-verarbeitbarer Dokumentation greifbar macht.

## Verwandt

- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - CCD - Continuity of Care Document]]
- [[EHR - C-CDA - Consolidated CDA]]
- [[EHR - Interoperabilität - Strukturell vs Semantisch]]
- [[EHR - Interoperabilität - LCIM nach Tolk]]
- [[EHR - ELGA - Technologie-Architektur]]
- [[MSI - HL7 CDA]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]] (CDA wird dort eingeführt; die Level-Stufung ist Ergänzung außerhalb der Vorlesung)
- Externe Referenz: HL7 CDA Release 2 Specification
