---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - Paper - SOAP Notes StatPearls]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - SOAP - Symptoms vs Signs

> [!info] Kurzdefinition
> Ein **Symptom** ist die subjektive Beschreibung des Patienten und gehört in Subjective; ein **Sign** ist ein objektiver Befund eines Untersuchers und gehört in Objective. Diese Unterscheidung ist die häufigste Fehlerquelle bei SOAP-Dokumentation.

## Beschreibung

Aus StatPearls (Sektion „Objective"):

> „A common mistake is distinguishing between symptoms and signs. Symptoms are the patient's subjective description and should be documented under the subjective heading, while a sign is an objective finding related to the associated symptom reported by the patient. An example of this is a patient stating he has 'stomach pain,' which is a symptom, documented under the subjective heading. Versus 'abdominal tenderness to palpation,' an objective sign documented under the objective heading."

## Bestandteile / Aufbau

| Aspekt | Symptom | Sign |
|---|---|---|
| Quelle | Patient | Untersucher |
| SOAP-Block | Subjective | Objective |
| Reproduzierbarkeit | nur durch Patient erneut | objektiv reproduzierbar |
| Beispiel: Schmerz | „I have stomach pain" | „abdominal tenderness to palpation" |
| Beispiel: Erkältung | „I feel feverish" | „T 38,7 °C, axillär" |
| Beispiel: Atemnot | „shortness of breath" | „RR 28/min, SpO2 89 %" |

## Beispiel

Praktisches Vor-/Nachher:

**Falsch (vermischt):**
> „Patient hat Bauchschmerzen mit Druckschmerz im rechten Unterbauch."

**Richtig (getrennt):**
> Subjective: „Patient berichtet Bauchschmerzen, kolikartig, im rechten Unterbauch lokalisiert."
> Objective: „Druckschmerz rechter Unterbauch, McBurney-Punkt positiv, kein Loslassschmerz."

## Abgrenzung

- Symptom-Sign-Trennung ist Voraussetzung für valide klinische Logik: Aus Symptom + Sign + Test-Ergebnis → Assessment (Differential Diagnosis).
- Nicht zu verwechseln mit „chief complaint" (immer ein Symptom) und „presenting problem" (kann beides sein).
- Wichtige Konsequenz für Coding: SNOMED-CT trennt Concepts in „Clinical finding" mit Sub-Hierarchien für Symptom und Sign.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen einem Symptom und einem Sign? Wo werden sie in SOAP dokumentiert?

**Anwendungsfrage:** Klassifiziere bei einem Patienten mit Pneumonie-Verdacht: „Husten" – „Rhonchi bei Auskultation" – „Patient fühlt sich krank" – „Temperatur 39,2 °C". Was ist Symptom, was Sign?

**Diskussionsfrage:** Bei einem Patienten mit chronischen Schmerzen ohne Korrelat im Befund (kein Sign) – wie geht man methodisch sauber vor? Welche diagnostische Falle droht?

**Mögliche Anschlussfragen:**
- Welche FHIR-Resource bildet ein Sign ab? (Antwort: typischerweise `Observation`, manchmal `Condition` mit clinicalStatus)
- Wie kodiert SNOMED-CT diese Unterscheidung? (Antwort: über Sub-Hierarchien des Concepts „Clinical finding")
- Warum ist die Trennung im EMR-Kontext besonders wichtig (Stichwort: NLP, Auswertbarkeit)?

## Verwandt

- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - OLDCARTS]]

## Quelle

- Vorlesung: [[EHR - Paper - SOAP Notes StatPearls]]
- Folien/Seitenangabe: Sektion „Objective" (Hinweis auf häufigen Fehler)
