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

# EHR - SOAP - Subjective

> [!info] Kurzdefinition
> **Subjective** ist die erste Komponente einer SOAP-Note. Sie beschreibt den aktuellen Zustand des Patienten in narrativer Form – aus seiner eigenen Sicht. Üblicherweise enthält sie das **Chief Complaint** (Hauptbeschwerde) und den Grund des Arztbesuchs.

## Beschreibung

Inhalt laut Folien:

> „Describes the patient's current condition (usually in narrative form) as described by the patient (subjective). This section usually includes the patient's chief complaint, or reason(s) why they came to the physician."

Die Information stammt **primär vom Patienten**, der Arzt darf gezielt nachfragen („do you also feel pain in the neck?").

## Bestandteile / Aufbau

Inhalte eines Subjective-Eintrags laut Folie:
- **Onset** – wann hat es begonnen?
- **Chronology** – Verbesserung, Verschlechterung
- **Quality and severity** – z. B. „pain rating" auf einer Skala
- **Modifying factors** – Drogen, Kaffee, Stress …
- **Additional symptoms**

## Beispiel

EMR-Systeme bieten typischerweise einen eigenen Tab oder eine eigene Sektion „Subjective", in der Chief Complaint, History of Present Illness und Review of Systems strukturiert eingegeben werden können.

## Abgrenzung

- Subjective ≠ Anamnese im engeren Sinn: Die Anamnese beinhaltet auch frühere Erkrankungen, Medikamente, Familie etc. – Teile davon werden in SOAP eher dem **Objective**-Block zugeordnet (z. B. „current medications, allergies, family history").
- Subjective ist klar abgegrenzt von Objective: alles, was nicht direkt messbar ist, gehört nach Subjective.
- Im SOAP-Schema ist Subjective immer **erster Block** – im APSO-Schema steht es an dritter Stelle.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was umfasst die Subjective-Komponente einer SOAP-Note? Welche Inhalte gehören hinein?

**Anwendungsfrage:** Wie würdest du Subjective bei einem Patienten mit Kopfschmerz strukturiert dokumentieren?

**Diskussionsfrage:** Wie verträgt sich der „subjektive" Charakter mit der Forderung nach strukturierten, kodierten Daten? Welche Methoden (Vorgaben, Templates, NLP) helfen, Subjective trotzdem analysierbar zu machen?

**Mögliche Anschlussfragen:**
- Was ist das Chief Complaint?
- Welche FHIR-Resource bildet typischerweise das Chief Complaint ab? (Antwort: `Encounter.reasonCode` oder `Condition`, abhängig von der Implementierung)
- Wie unterscheidet sich Onset von Chronology?
- Warum sind „modifying factors" (Drogen, Kaffee, Stress) relevant?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Plan]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folien 7–9 (SOAP: Subjective + EMR-Beispiel)
