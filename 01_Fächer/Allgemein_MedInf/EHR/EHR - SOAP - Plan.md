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

# EHR - SOAP - Plan

> [!info] Kurzdefinition
> **Plan** ist die vierte Komponente einer SOAP-Note. Sie beschreibt, was der Versorger als nächstes tun wird – Diagnostik, Therapie, Überweisungen, Patientenaufklärung, Disposition. Plan ist **nicht** auf Therapie reduziert.

## Beschreibung

Inhalt laut Folien:

> „This describes what the health care provider will do to treat the patient – ordering labs, referrals, ... procedures to be performed, medications prescribed, therapies started."

Plan unterteilt sich in mehrere **Sub-Komponenten**, die gemeinsam den nächsten Schritt der Versorgung dokumentieren.

## Bestandteile / Aufbau

Plan-Sub-Komponenten laut PDF-Beispiel (Patient nach Appendektomie):

| Sub-Komponente | Inhalt |
|---|---|
| **Diagnostic component** | Weitere Diagnostik, Monitoring – z. B. „continue to monitor labs" |
| **Therapeutic component** | Therapeutische Maßnahmen – z. B. „advance diet" |
| **Referrals** | Überweisungen – z. B. „follow up with Cardiology within three days of discharge for stress testing as an out-patient" |
| **Patient education component** | Aufklärung, Information – z. B. „progress is good" |
| **Disposition component** | Entlass-Disposition – z. B. „discharge to home in the morning" |

## Beispiel

Plan-Eintrag bei einem Patienten mit neu diagnostiziertem Diabetes Typ 2:
- **Diagnostic:** Re-Check HbA1c in 3 Monaten, Augenarzt-Screening
- **Therapeutic:** Metformin 500 mg 1-0-1, Diätberatung
- **Referrals:** Diabetologie zur Strukturierten Schulung
- **Patient education:** Aufklärung Hypoglykämie, BZ-Selbstkontrolle
- **Disposition:** Wiedervorstellung in 2 Wochen zur Therapieanpassung

## Abgrenzung

- Plan ≠ nur Therapie: Häufiger Fehler ist, Plan auf Medikation/Therapie zu reduzieren. Diagnostik (z. B. Lab-Orders) und Patient Education sind ebenso Bestandteil.
- Plan ≠ Care Plan: Im klinischen Sprachgebrauch ist „Care Plan" oft umfassender (langfristig, multidisziplinär), während die Plan-Komponente einer SOAP-Note die nächsten Schritte bis zur nächsten Visite umfasst.
- **Disposition** ist der einzige Sub-Bereich, der bei ambulanten Visiten oft entfällt – bei stationären Aufenthalten zentral.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Sub-Komponenten umfasst der Plan-Block einer SOAP-Note?

**Anwendungsfrage:** Erstelle einen Plan-Eintrag für einen Patienten mit neu diagnostiziertem Hochdruck.

**Diskussionsfrage:** Patient Education ist im PDF als Sub-Komponente von Plan gelistet. Welche Konsequenz hat das für Health-Literacy-Strategien? Wird Patient Education in der Praxis ausreichend dokumentiert?

**Mögliche Anschlussfragen:**
- Wie verhält sich Plan zu FHIR (Stichwort: ServiceRequest, MedicationRequest, CarePlan, ReferralRequest)?
- Wo wird Plan in einem CCD-Dokument abgebildet?
- Was unterscheidet Plan in einer SOAP-Note von einem CarePlan?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Progress Notes]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folien 14–15 (SOAP: Plan + Beispiel Appendektomie)
