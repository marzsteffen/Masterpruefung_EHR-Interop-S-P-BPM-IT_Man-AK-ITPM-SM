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

# EHR - Datenmodelle - Klassische Record Typen

> [!info] Kurzdefinition
> Drei klassische Strukturierungen medizinischer Records: zeit-orientiert, quellen-orientiert und problem-orientiert. Sie unterscheiden sich darin, welche Dimension primär als Anker dient. Der problem-orientierte Record führt SOAP als dritte Dimension ein.

## Beschreibung

Vorlesung Folie 88 („Types of (classic) medical records"). Die Klassifikation strukturiert, wie Daten innerhalb einer Akte primär organisiert werden – nicht *was* enthalten ist.

## Bestandteile / Aufbau

| Typ | 1. Dimension | 2. Dimension | 3. Dimension |
|---|---|---|---|
| **Time oriented medical record** | Zeit | Physical examinations, tests | – |
| **Source oriented medical record** | Physical examinations, tests | Zeit | – |
| **Problem oriented medical record** | Medizinische Probleme, Diagnosen, Symptome | Zeit | **SOAP**: Subjective, Objective, Assessment, Plan |

## Beispiel

Folie 89 listet Sichten auf medizinische Records:
- Verlauf einer Krankheit über die Zeit
- Alle Urin-Labortests als Funktion der Zeit
- Alle Besuche im Krankenhaus XYZ in 2015
- Medikation der letzten 6 Monate

Diese Sichten sind je nach Record-Typ unterschiedlich performant abrufbar.

## Abgrenzung

- Es geht um die **Strukturierung** der Akte, nicht um Speichertechnologie (Datenbankmodell) oder Datenformat (HL7, FHIR).
- Der problem-orientierte Record ist der Einstieg in das Thema **SOAP-Notes** (eigene Vorlesung [[EHR - VL - SOAP Notes]]).
- Diese drei klassischen Typen sind historisch – moderne EHRs kombinieren sie typischerweise und liefern verschiedene Sichten je nach Anwendungsfall.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei klassischen Typen medizinischer Records gibt es und wie unterscheiden sie sich in den Dimensionen?

**Anwendungsfrage:** Welcher Record-Typ ist günstig für die Frage „Welche Medikation hat der Patient seit 2020 erhalten?"

**Diskussionsfrage:** Moderne EHRs müssen alle drei Sichten gleichzeitig liefern können. Welche Konsequenz hat das für das interne Datenmodell?

**Mögliche Anschlussfragen:**
- Was ist SOAP konkret und wo kommt es zum Einsatz? (siehe [[EHR - VL - SOAP Notes]])
- Welcher Typ war historisch am verbreitetsten in Papierakten?
- Wie repräsentiert FHIR diese verschiedenen Sichten?

## Verwandt

- [[EHR - VL - SOAP Notes]]
- [[EHR - SOAP - Komponenten]]
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 88–89 (Types of (classic) medical records, Views on medical records)
