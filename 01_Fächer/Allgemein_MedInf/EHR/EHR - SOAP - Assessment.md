---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - SOAP Notes]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - SOAP - Assessment

> [!info] Kurzdefinition
> **Assessment** ist die dritte Komponente einer SOAP-Note. Sie enthält die **ärztliche Diagnose** für die jeweilige Visite – narrativ und/oder kodiert. Die Kodierung dient primär der Abrechnung (Reimbursement) und Statistik.

## Beschreibung

Inhalt laut Folien:

> „The Physician's medical diagnoses for the medical visit on the given date of a note written. Narrative text and/or coded (when coded, most for reimbursement purposes)."

Genannte Coding-Standards:
- **ICD-10** (International Classification for Diseases) – primär für Reimbursement
- **SNOMED CT** – Folie verweist nach vorne („we will later learn about SNOMED-CT annotations")

## Bestandteile / Aufbau

Eine Assessment-Eintrag besteht typischerweise aus:
- Eine oder mehrere Diagnosen (Hauptdiagnose + Nebendiagnosen)
- Pro Diagnose: ICD-10-Code und/oder SNOMED-CT-Concept
- Ggf. narrative Begründung der Diagnose („Differentialdiagnose erwogen, ausgeschlossen wegen ...")
- Status der Diagnose (vermutet, gesichert, ausgeschlossen, anhaltend)

## Beispiel

Beispiel laut Diabetes-Folie (SlideShare-Referenz):
- Assessment: Diabetes mellitus Typ 2, neu diagnostiziert (ICD-10: E11.9)
- Bluthochdruck (ICD-10: I10)
- Adipositas Grad I (ICD-10: E66.0)

## Abgrenzung

- **Assessment ≠ Diagnose-History**: Assessment ist die Diagnose **für diese Visite**. Eine bestehende Diagnose aus früheren Visiten taucht im Objective auf (medical history) oder wird im neuen Assessment bestätigt/korrigiert.
- **ICD-10 vs. SNOMED-CT**: ICD-10 ist eine Klassifikation für epidemiologische und Abrechnungs­zwecke (klassifizierend, ca. 70.000 Codes). SNOMED-CT ist eine Terminologie für klinische Beschreibung (ca. 350.000 aktive Concepts, granular und mit Beziehungen).
- **Narrativ + kodiert** ist nicht entweder/oder – beide Formate ergänzen sich: Narrative trägt Kontext, Code trägt Auswertbarkeit.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was gehört in die Assessment-Komponente einer SOAP-Note? Welche Coding-Standards werden hier eingesetzt?

**Anwendungsfrage:** Wie würdest du Assessment für einen Patienten dokumentieren, dessen Diagnose noch unklar ist (Differentialdiagnose)?

**Diskussionsfrage:** ICD-10 reicht für Reimbursement, aber nicht für klinische Differenzierung. Wann ist SNOMED-CT vorzuziehen, wann ICD-10?

**Mögliche Anschlussfragen:**
- Was ist eine Differentialdiagnose und wie wird sie in SOAP dokumentiert?
- Wie verhält sich Assessment zu FHIR-Resourcen? (Antwort: typischerweise `Condition` mit Coding-Bindings auf ICD-10 oder SNOMED-CT)
- Warum gibt ICD-11 immer noch keine breite EMR-Verbreitung?
- Wozu führt eine fehlerhafte oder ungenaue Kodierung in Reimbursement-Prozessen?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Plan]]
- [[MSI - ICD-10]]
- [[MSI - SNOMED CT]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folie 13 (SOAP: Assessment)
