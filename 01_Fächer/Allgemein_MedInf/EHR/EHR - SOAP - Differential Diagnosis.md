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

# EHR - SOAP - Differential Diagnosis

> [!info] Kurzdefinition
> **Differential Diagnosis (DD)** ist eine Substruktur des Assessment-Blocks: Eine geordnete Liste möglicher Diagnosen, von der wahrscheinlichsten zur unwahrscheinlichsten, mit dem dahinterstehenden Reasoning. Sie macht klinisches Denken explizit.

## Beschreibung

Aus StatPearls (Sektion „Assessment"):

> „This is a list of the different possible diagnosis, from most to least likely, and the thought process behind this list. This is where the decision-making process is explained in depth. Included should be the possibility of other diagnoses that may harm the patient, but are less likely."

Wichtiger Punkt: **„don't miss"-Diagnosen** (potenziell gefährliche Diagnosen, die unbedingt ausgeschlossen werden müssen) sollen mit aufgenommen werden, **auch wenn sie unwahrscheinlich sind**.

## Bestandteile / Aufbau

Strukturierter Aufbau nach StatPearls:

```
Problem 1
  Differential Diagnoses (most → least likely):
    1. Diagnose A (Begründung warum wahrscheinlich)
    2. Diagnose B (Begründung)
    3. Diagnose C (don't miss – warum trotzdem prüfen)
  Discussion (Reasoning, was unterscheidet A/B/C)
  Plan for Problem 1 (Tests, Therapie, → siehe Plan-Block)

Problem 2
  ... (gleiche Struktur)
```

## Beispiel

Bei einem Patienten mit Brustschmerz:

```
Problem 1: Brustschmerz
  Differential Diagnoses:
    1. Akutes Koronarsyndrom (don't miss; Risikofaktoren: Hypertonie, Raucher)
    2. Lungenembolie (don't miss; Reisedauer 6 h vor Beginn)
    3. Muskuloskeletaler Schmerz (lokaler Druckschmerz, atemabhängig)
    4. Reflux (Postprandiales Auftreten)
  Discussion: EKG ohne ST-Hebung, Troponin ausstehend; Wells-Score 3 → 
              D-Dimer indiziert.
  Plan: EKG, Troponin, D-Dimer, ggf. CT-Angio.
```

## Abgrenzung

- **DD ist Teil von Assessment** – nicht von Plan. Plan adressiert die diagnostischen/therapeutischen Konsequenzen, DD ist die Liste der Hypothesen.
- **DD ≠ Working Diagnosis:** Working Diagnosis ist die aktuell wahrscheinlichste; DD ist die Liste mit Alternativen.
- DD ist die expliziteste Form von Clinical Reasoning – fehlt sie, kann das Assessment intransparent werden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Differential Diagnosis und welche Aufgabe erfüllt sie im SOAP-Schema?

**Anwendungsfrage:** Erstelle eine Differential Diagnosis für einen Patienten mit akuten Bauchschmerzen rechts unten – inklusive einer „don't miss"-Diagnose.

**Diskussionsfrage:** Eine ausführliche DD ist klinisch wertvoll, aber zeit­aufwändig. In welchen Settings (z. B. Notaufnahme, Routine-Sprechstunde, Stations­arbeit) muss man Aufwand und Tiefe der DD anpassen?

**Mögliche Anschlussfragen:**
- Wie würde man DD in FHIR abbilden? (Antwort: mehrere `Condition`-Resourcen mit verschiedenem `verificationStatus` – z. B. provisional, differential, refuted)
- Welche Bayes'sche Logik steckt hinter „most likely" → „least likely"?
- Wie unterstützen CDS-Systeme eine DD?
- Was ist der Unterschied zwischen DD und Provisional Diagnosis?

## Verwandt

- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Plan]]
- [[EHR - SOAP - Symptoms vs Signs]]

## Quelle

- Vorlesung: [[EHR - Paper - SOAP Notes StatPearls]]
- Folien/Seitenangabe: Sektion „Assessment → Differential Diagnosis"
