---
fach: itm-ak
typ: konzept
status: offen
quelle: "[[ITM-AK - VL - Controlling]]"
tags:
  - fach/vertiefung/itm-ak
  - typ/konzept
  - status/offen
---

# ITM-AK - ICD-10 und MBDS

> [!info] Kurzdefinition
> ICD-10 ist die international standardisierte Klassifikation der Diagnosen; MBDS (Mindestbasisdatensatz) ist die österreichische Datenbasis, die ICD-10-Diagnosen plus Patient:innen- und Behandlungsdaten umfasst und Grundlage für die Krankenhausvergütung im LKF-System ist.

## Beschreibung

Folie 51 erklärt die Kodierung der Diagnose:
- **ICD-10-Kodierung.**
- **MBDS-Datensatz** (Mindestbasisdatensatz).
- **MBDS als Grundlage für die Krankenhausvergütung.**
- Österreich: **eine Hauptdiagnose, mehrere Nebendiagnosen.**
- Basierend auf Kodierung: Krankenhaus erhält bestimmte **Punkte (Österreich) oder Geld (z. B. Fallpauschale in Deutschland).**

## Bestandteile / Aufbau

| Element | Funktion |
|---|---|
| **ICD-10** | Internationale Klassifikation der Krankheiten, 10. Revision; standardisierte Diagnose-Codes |
| **MBDS** | Mindestbasisdatensatz; in Österreich verpflichtend pro stationärem Aufenthalt |
| **Hauptdiagnose** | Eine pro Aufenthalt; primärer Anlass der Behandlung |
| **Nebendiagnosen** | Mehrere möglich; relevante Begleiterkrankungen |
| **MEL (medizinische Einzelleistungen)** | Zusätzliche Kodierung der Leistungen, ergänzt zur Diagnose |

Die Kombination Hauptdiagnose + Nebendiagnosen + MELs ergibt das LKF-Punkteergebnis (siehe [[ITM-AK - DRG und LKF]]).

## Beispiel

Folie 54 zeigt LKF-Screenshots:
- ICD-Code „E12.8 – Diabetes mellitus in Verbindung mit Fehl- oder Mangelernährung [Malnutrition]" als Hauptdiagnose.
- MEL „EF030 R – Perkutane transluminale Angioplastie (PTA) – untere Extremität" als Leistung.

## Abgrenzung

- **ICD-10 ≠ MBDS:** ICD-10 sind nur die Diagnose-Codes; MBDS ist der gesamte Mindestdatensatz inklusive Patient:innen-Stammdaten, Aufenthaltsdaten, Diagnosen und Leistungen.
- **MBDS ≠ KDok:** KDok ist die Software des BMG zur Erfassung; MBDS ist der inhaltliche Datensatz. Folie 53 nennt zusätzlich „Xdok (Jahr)" als Erfassungssoftware.
- **ICD-10 ≠ ICD-11:** WHO hat 2022 ICD-11 eingeführt; Österreich nutzt aktuell weiter ICD-10. Versionen werden im PDF nicht im Detail behandelt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was sind ICD-10 und MBDS und wozu dienen sie?"

**Anwendungsfrage:** „Erläutern Sie DRG, MBDS und wie sie mit der Krankenhausvergütung zusammenhängen." (Frage zur Wiederholung Folie 62)

**Diskussionsfrage:** Welche Anforderungen stellt der MBDS an die IT-Architektur eines Krankenhauses?
- Strukturierte Erfassung im KIS.
- Kodierungs-Software-Integration.
- Schnittstelle zu LKF-Berechnungssystem.
- Datenqualität (Vollständigkeit, Plausibilität).
- Schnittstelle zu A-IQI für Qualitätsmessung.

**Mögliche Anschlussfragen:**
- Welche Rolle spielen ICD-10-Updates für die LKF-Punkteberechnung?
- Wer kodiert in der Praxis (Mediziner, Codier-Fachkräfte)?
- Wie hängt MBDS mit ELGA zusammen?

## Verwandt

- [[ITM-AK - DRG und LKF]]
- [[ITM-AK - Medizinisches Controlling]]
- [[ITM-AK - A-IQI - Austrian Inpatient Quality Indicators]]
- [[EHR - ELGA - Architektur]]
- [[MSI - HL7 FHIR - Resource]]

## Quelle

- Vorlesung: [[ITM-AK - VL - Controlling]]
- Folien/Seitenangabe: 51, 53–54
