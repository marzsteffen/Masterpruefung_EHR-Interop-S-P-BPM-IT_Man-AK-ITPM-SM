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

# EHR - SOAP - Objective

> [!info] Kurzdefinition
> **Objective** ist die zweite Komponente einer SOAP-Note. Sie umfasst alle **objektiven, reproduzierbaren und nachvollziehbaren** Fakten über den Status des Patienten – also alles, was gemessen oder beobachtet werden kann.

## Beschreibung

Inhalt laut Folien:

> „The second step is usually to perform measurements (objective, repeatable, and traceable facts about the patient's status)."

## Bestandteile / Aufbau

Inhalte einer Objective-Sektion laut Folie:
- **Vital signs** – Blutdruck, Temperatur, Herzfrequenz
- **Findings from physical examinations** – oft als „normal / abnormal" kodiert
- **Laboratory results**
- **Measurements** – Height, Weight, BMI
- **Other information** – Alter
- **Current medications and allergies**
- **Family history**
- **ECG**
- **Alles, was gemessen/erfasst werden kann und Einfluss haben kann**

EMR-Systeme bieten typischerweise mehrere Tabs für die Objective-Sektion: Vital Signs, Physical Examination, Laboratory Results, ECG, etc.

## Beispiel

Beispiel-Objective bei einem Patienten mit Diabetes-Verdacht:
- Blutdruck 145/90 mmHg
- Gewicht 95 kg, Größe 178 cm → BMI 30.0
- Nüchternblutzucker 142 mg/dL
- HbA1c 7.8 %
- Physical exam: Akanthose im Nacken, periphere Pulse normal

## Abgrenzung

- **Subjective vs. Objective** ist die zentrale Trennlinie: Subjective = Patient sagt es; Objective = wird gemessen oder beobachtet. Schmerz-Rating gehört zu Subjective (Patient sagt 7/10), Blutdruck zu Objective (gemessen 140/90).
- **Current medications** und **Allergies** stehen laut Folie unter Objective – das ist eine pragmatische Zuordnung, andere Quellen führen sie als eigenen Block.
- Objective ≠ Diagnose: aus Objective wird Assessment erst durch ärztliche Interpretation.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was gehört in die Objective-Komponente einer SOAP-Note?

**Anwendungsfrage:** Wie würdest du eine ECG-Aufzeichnung in SOAP einordnen – als Rohdaten oder Interpretation, in welchem Block?

**Diskussionsfrage:** Aktuelle Medikation und Allergien werden im PDF unter Objective geführt. Sind das wirklich „messbare Fakten"? Wo könnten sie alternativ stehen?

**Mögliche Anschlussfragen:**
- Was unterscheidet Objective von Subjective im Detail? (Rule of thumb: kann es ohne Patient-Aussage erhoben werden?)
- Welche FHIR-Resourcen bilden Objective ab? (Antwort: Observation, AllergyIntolerance, MedicationStatement, FamilyMemberHistory)
- Warum sind „normal/abnormal"-Codes in PE praktisch?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Plan]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folien 10–12 (SOAP: Objective + EMR-Beispiel + Tabs)
