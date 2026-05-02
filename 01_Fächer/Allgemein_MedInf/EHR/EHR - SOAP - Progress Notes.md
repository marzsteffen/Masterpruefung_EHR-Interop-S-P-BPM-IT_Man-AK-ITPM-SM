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

# EHR - SOAP - Progress Notes

> [!info] Kurzdefinition
> **Progress Notes** sind aufeinander aufbauende SOAP-Notes über mehrere Visiten hinweg. Jede Folge-SOAP-Note baut auf der vorigen auf und dokumentiert den Verlauf eines Versorgungs­prozesses.

## Beschreibung

Folie 17:

> „One SOAP note may be the basis of the next SOAP note (subsequent visits)."

Die Struktur erlaubt, jede der vier Komponenten **als Verlauf** zu betrachten:

## Bestandteile / Aufbau

| Komponente | Frage in der Folge-SOAP-Note |
|---|---|
| **Subjective** | Status der vorherigen Beschwerden – Verbesserung, Verschlechterung? Neue Beschwerden? |
| **Objective** | Zeigen die Messergebnisse einen Verlauf zur Besserung oder Verschlechterung? |
| **Assessment** | War die vorherige Diagnose korrekt? Muss sie angepasst oder erweitert werden? |
| **Plan** | Muss der Behandlungsplan angepasst werden? |

## Beispiel

Patient mit Diabetes-Diagnose vor 3 Monaten (Folge-Visite):
- **S:** Patient berichtet weniger Müdigkeit, bessere Konzentration; gelegentlich morgendliche Hypoglykämien
- **O:** HbA1c 6.8 % (vorher 7.8 %), Gewicht -3 kg
- **A:** Diabetes Typ 2 unter Therapie verbessert; Verdacht auf zu hohe Metformin-Dosis (Hypoglykämie)
- **P:** Metformin auf 500 mg 1-0-0 reduzieren; HbA1c-Kontrolle in 3 Monaten

## Abgrenzung

- Progress Notes ≠ Discharge Summary: Discharge Summary ist ein zusammenfassendes Abschluss­dokument, Progress Notes sind die fortlaufende Dokumentation während einer Episode.
- Eine **einzelne SOAP-Note** ist keine Progress Note im engeren Sinn – Progress Notes entstehen erst durch Sequenzen aufeinander folgender SOAP-Notes.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind Progress Notes, und wie verhalten sie sich zu SOAP?

**Anwendungsfrage:** Wie würdest du eine Folge-SOAP-Note nach einer ersten Diabetes-Diagnose strukturieren?

**Diskussionsfrage:** Progress Notes erlauben Verlaufs­vergleich, sind aber dokumentations­aufwändig. Welche Trade-offs entstehen, wenn man Sub-Block S oder O reduziert oder weglässt?

**Mögliche Anschlussfragen:**
- Welche Rolle spielen Progress Notes für die mündliche Übergabe (z. B. Schichtwechsel)?
- Wie unterstützt ein EMR-System die Verlaufs­darstellung über Progress Notes?
- Welche FHIR-Resourcen bilden Progress Notes ab? (Antwort: typischerweise `DocumentReference` mit Composition)

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Plan]]
- [[EHR - SOAP - APSO Variante]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folie 17 (SOAP and progress notes)
