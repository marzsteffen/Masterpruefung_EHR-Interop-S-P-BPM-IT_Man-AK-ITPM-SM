---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Einführung und Definitionen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Standards - Unterstützte Coding Standards

> [!info] Kurzdefinition
> Liste der Standards, deren Unterstützung die Vorlesung als funktionale Anforderung an ein EHR-System nennt: DICOM (Bilddaten), LOINC (klinische Beobachtungen, Vitalwerte, Labor), ICD-9/-10 (Diagnosen), SNOMED CT (klinische Terminologie), nationale Medikamenten-Terminologien.

## Beschreibung

Aus Folie 60 („More functional requirements – Standards"). Die Vorlesung listet die Standards als Mindestanforderungen, ohne sie tiefgehend zu erklären – „SNOMED-CT (see later)" verweist auf eine spätere Vertiefung.

## Bestandteile / Aufbau

| Standard | Zweck (laut PDF) | Versionsangabe |
|---|---|---|
| **DICOM** | Bilddaten – jeder Beteiligter (inkl. Patient) soll Bilder ohne Zusatzsoftware sehen können | im PDF nicht spezifiziert |
| **LOINC** | Coding für medizinische Terminologie (z. B. Anamnese, frühere Medikation), Vitalwerte, Laboruntersuchungen | im PDF nicht spezifiziert |
| **ICD-9** | Diagnosecodes (US, älter) | Version 9 |
| **ICD-10** | Diagnosecodes | Version 10 |
| **SNOMED CT** | Klinische Terminologie (im PDF Verweis „see later") | im PDF nicht spezifiziert |
| **RxNorm** (USA) | Lokale Medikamenten-Terminologie | im PDF nicht spezifiziert |
| **PZN** (Austria) | Pharmazentralnummer für Medikamente | im PDF nicht spezifiziert |

Begriffe **DICOM**, **LOINC**, **SNOMED CT**, **ICD** werden im PDF nur erwähnt, aber nicht definiert (siehe [[MSI - MOC]]).

## Beispiel

Konkretes Beispiel im PDF: „LOINC for coding (medical terminology, e.g. „anamnesis", „prior medications", vital signs, laboratory tests)."

## Abgrenzung

- Diese Liste ist **nicht erschöpfend**; HL7 (Messaging) und IHE (Profile) tauchen an dieser Stelle des PDFs nicht explizit als Coding-Standards auf, werden aber in anderen Vorlesungen behandelt.
- **Coding Standards** ≠ **Messaging Standards** ≠ **Document Standards**: LOINC/SNOMED/ICD sind Coding (was), HL7 v2/FHIR ist Messaging (wie), CDA ist Document (Container) – die Vorlesung trennt das hier nicht streng, das ist aber prüfungsrelevant.
- Lokale Terminologien (RxNorm, PZN) sind regional und nicht international interoperabel.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Coding-Standards muss ein EHR-System typischerweise unterstützen?

**Anwendungsfrage:** Warum reicht ICD-10 nicht aus, wenn man auch SNOMED CT nutzt? Wo liegt die Aufgabenteilung?

**Diskussionsfrage:** RxNorm in den USA, PZN in Österreich – warum gibt es keinen weltweit einheitlichen Medikamenten-Code, und welche Konsequenzen hat das für grenzüberschreitende Versorgung?

**Mögliche Anschlussfragen:**
- Welcher Standard kodiert was? (ICD: Diagnosen; LOINC: Laboruntersuchungen + Beobachtungen; SNOMED: alles klinische)
- Wie verhält sich SNOMED CT zu ICD-10?
- Wie nutzt FHIR diese Coding-Standards (Stichwort: CodeableConcept)?
- Welche Versionen sind aktuell? (im PDF nicht angegeben → siehe Quellen-Vertiefung)

## Verwandt

- [[MSI - MOC]]
- [[MSI - SNOMED CT]]
- [[MSI - LOINC]]
- [[MSI - ICD-10]]
- [[MSI - DICOM]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folie 60 (More functional requirements – Standards)
