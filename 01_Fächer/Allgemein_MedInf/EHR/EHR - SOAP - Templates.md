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

# EHR - SOAP - Templates

> [!info] Kurzdefinition
> **Customized SOAP Templates** sind in EMR-Systemen anlegbare, fachspezifische SOAP-Vorlagen. Sie standardisieren wiederkehrende Patiententypen (z. B. Verletzungen, Diabetes-Routine) und steigern Effizienz und Vollständigkeit der Dokumentation.

## Beschreibung

Folie 18:

> „Some EMR systems allow to build customized SOAP templates. For example, a department specialized in injuries may want to build an 'injury SOAP template'."

Vorteile laut PDF:
- Less typing, more (automated) coding
- Standardized questions
- Completeness
- Standardized therapies

## Bestandteile / Aufbau

Ein SOAP-Template enthält typischerweise:
- **Vordefinierte Subjective-Fragen**: bei einem Injury-Template z. B. „Mechanism of Injury", „Time of Injury", „First Aid Performed".
- **Vordefinierte Objective-Felder**: Wundgröße, Lokalisation, Pulsstatus, Sensibilität.
- **Assessment-Vorlagen**: vorab kodierte Diagnose-Vorschläge (z. B. ICD-10 für typische Verletzungs-Codes).
- **Plan-Bausteine**: Wundversorgung, Tetanus-Schutz, Tetanus-Booster, Wiedervorstellung.

## Beispiel

Beispiel-Templates aus dem PDF-Kontext:
- **Injury Template** (Verletzungen)
- **Diabetes-Routine-Template** (Folge-Visiten Diabetes mellitus)
- **Wellness-Visit-Template** (Vorsorge)

PDF verweist auf ein YouTube-Video „Building a SOAP template for injuries" (Folie 19) als praktisches Beispiel.

## Abgrenzung

- SOAP-Templates ≠ PowerForms o. ä. spezielle EMR-Module: Templates sind Vorlagen für eine SOAP-Note; PowerForms ist eine Cerner-spezifische Form-Engine ([[EHR - Beispiel - Cerner PowerChart Office]]).
- Templates ≠ Pathways: Templates sind Dokumentations-Hilfen; Pathways sind klinische Versorgungs­prozesse mit Entscheidungslogik.
- Customized Templates standardisieren Inhalt – sie sind aber nicht dasselbe wie strukturierte Coding-Vorgaben (LOINC, SNOMED-Bindings).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind SOAP-Templates und welchen Zweck erfüllen sie in EMR-Systemen?

**Anwendungsfrage:** Wie würdest du ein SOAP-Template für „Hypertonie-Folgevisite" entwerfen? Welche Felder wären in S/O/A/P jeweils sinnvoll vordefiniert?

**Diskussionsfrage:** Templates erhöhen Effizienz, aber kritisieren manche Ärzte sie als „cookie-cutter medicine". Wo verläuft die Grenze zwischen sinnvoller Standardisierung und problematischer Verflachung der ärztlichen Dokumentation?

**Mögliche Anschlussfragen:**
- Wie verhalten sich Templates zu Custom-Care-Designs in modernen EMR-Systemen?
- Welche Vorteile bringen Templates für Sekundärnutzung (Forschung, Quality Assurance)?
- Welche Rolle könnten LLMs künftig bei dynamischen, kontextuellen Templates spielen?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Progress Notes]]
- [[EHR - Beispiel - Cerner PowerChart Office]]
- [[EHR - EMR - 24 Funktionsbereiche]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folien 18–19 (Customized SOAP Templates + YouTube-Verweis)
