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

# EHR - CCR - Continuity of Care Record

> [!info] Kurzdefinition
> **CCR** (Continuity of Care Record) ist ein US-Standard (**ASTM E2369-12**) für eine kompakte Versorgungs-Zusammenfassung. **Keine vollständige Akte**, sondern eine Summary mit 6 vorgegebenen Sektionen. Eingeführt im Rahmen von Meaningful Use als Mindest-Anforderung für EHR-Exchange.

## Beschreibung

Aus den Folien:

> „CCR = Continuity of Care Record. Developed for the USA, but also used in other countries. Somewhat like 'ELGA Entlassungsbrief', but … more. A summary, not a full health record. Predefined content and sections."

## Bestandteile / Aufbau

### Die 6 CCR-Sektionen (Mandated Core Elements)

| # | Sektion | Inhalt |
|---|---|---|
| 1 | **Provider Info** | Wer hat das CCR erstellt? (Optional Extension) |
| 2 | **Patient Identifying Info** | Demographic and Administrative Information (Optional Extension) |
| 3 | **Insurance and Financial Info** | Eligibility, Co-payment etc. (Extension möglich) |
| 4 | **Patient's Health Status** | Problems/Diagnoses/Conditions, Adverse Reactions, Current Medications, Immunizations, Vital Signs, Lab Results, Procedures & Assessments |
| 5 | **Care Documentation** | Med. Specialty-spezifische Info, Disease-Management-Info, Institution-spezifische Info, Care Documentation für Payers (Attachments), Personal Health Record Info (vom Patienten dokumentiert) |
| 6 | **Care Plan Recommendation** | Empfehlungen zum weiteren Plan (Text) |

### Section 4 – Patient's Health Status (Folie 18)

- Problems / Diagnoses / Conditions
- Adverse reactions & alerts
- Current medications
- Immunizations
- Vital signs
- Lab results
- Procedures & assessments

### Section 5 – Case Documentation (Folie 19)

- Med. Specialty-spezifische Information
- Disease-Management-spezifische Information
- Institution-spezifische Information
- Information über vorherige Encounters (Datum + Zeit, …)
- Care Documentation for Payers (über Attachments)
- Personal Health Record Information (vom Patienten dokumentiert)

### Document Identifying Information

- From / To / Reason for Referral oder Transfer

## Beispiel

CCR ist im PDF mit dem ELGA-Entlassungsbrief verglichen, aber „mehr": Es fasst Health Status + Versorgungsdokumentation + Care Plan zusammen, **nicht** die gesamte Patientenakte.

Use-Case: Patient wechselt vom Krankenhaus in die Reha → CCR wird übergeben mit aktuellem Status, Plan und allen relevanten Informationen für den nächsten Versorger.

## Abgrenzung

- CCR ist eine **Spezifikation für Inhalt und Struktur**, nicht für Format. Implementiert wird CCR per ASTM-XML oder per HL7-CDA (= [[EHR - CCD - Continuity of Care Document]]).
- CCR ≠ vollständiges EHR: Es ist eine **Summary** für die Versorgungs-Übergabe (Care Transition).
- CCR ist **fading out** (laut Folie) – CCD/C-CDA hat die ASTM-XML-Variante praktisch ersetzt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein CCR? Welche 6 Sektionen umfasst er?

**Anwendungsfrage:** Welche Inhalte würdest du in einem CCR für eine Versorgungs-Übergabe vom Hausarzt zum Krankenhaus erwarten?

**Diskussionsfrage:** Eine kompakte Summary vs. ein voller Datenexport – welche Vor- und Nachteile haben beide Modelle? Wann reicht eine Summary, wann ist sie unzureichend?

**Mögliche Anschlussfragen:**
- Was sind die „Mandated Core Elements" und welche sind „Optional Extensions"?
- Was ist der Unterschied zwischen Section 4 (Health Status) und Section 5 (Case Documentation)?
- Welche Implementierung ist heute Standard – ASTM-XML oder CDA?
- Wie verhält sich CCR zur „Patient Summary" im EHDS-Kontext?

## Verwandt

- [[EHR - CCD - Continuity of Care Document]]
- [[EHR - C-CDA - Consolidated CDA]]
- [[EHR - CCR - Patient Identification]]
- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - VL - Meaningful Use]]
- [[EHR - SOAP - Plan]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folien 14–20 (CCR Definition, Sections, Conceptual Model)
