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

# EHR - SOAP - OLDCARTS

> [!info] Kurzdefinition
> **OLDCARTS** ist ein Mnemonic zur strukturierten Erfassung der **History of Present Illness (HPI)** im Subjective-Block einer SOAP-Note. Acht Aspekte: Onset, Location, Duration, Characterization, Alleviating/Aggravating factors, Radiation, Temporal factor, Severity.

## Beschreibung

StatPearls beschreibt OLDCARTS als das im US-Diskurs etablierte Mnemonic, mit dem die History of Present Illness systematisch erhoben wird. Die HPI beginnt mit einem one-line opening: „47-year old female presenting with abdominal pain", danach folgt die Detail-Erfassung entlang der acht Buchstaben.

## Bestandteile / Aufbau

| Buchstabe | Aspekt | Frage an den Patienten |
|---|---|---|
| **O** | Onset | Wann hat das Chief Complaint begonnen? |
| **L** | Location | Wo ist es lokalisiert? |
| **D** | Duration | Wie lange dauert es schon an? |
| **C** | Characterization | Wie beschreibt der Patient das Symptom? |
| **A** | Alleviating and Aggravating factors | Was lindert es? Was verschlimmert es? |
| **R** | Radiation | Strahlt es aus oder bleibt es lokal? |
| **T** | Temporal factor | Ist es zu bestimmten Tageszeiten schlimmer/besser? |
| **S** | Severity | Auf einer Skala 1–10: wie stark? (1 = am wenigsten, 10 = am schlimmsten) |

## Beispiel

OLDCARTS für einen Patienten mit Bauchschmerzen:
- **O:** Begann gestern Abend nach dem Essen
- **L:** Rechter Unterbauch
- **D:** ca. 18 Stunden andauernd
- **C:** Drückend, kolikartig, bewegungsabhängig schlimmer
- **A:** Linderung durch Liegen, Verschlimmerung durch Husten
- **R:** Strahlt nicht aus
- **T:** Konstant, nachts geringfügig schlimmer
- **S:** 7/10

## Abgrenzung

- OLDCARTS ist eine **Substruktur des Subjective-Blocks**, speziell für die HPI – nicht für die gesamte Subjective-Sektion.
- Es gibt verwandte Mnemonics: **OPQRST** (Onset, Provocation/Palliation, Quality, Region/Radiation, Severity, Time) – ähnliche Aspekte, andere Reihenfolge.
- OLDCARTS ist **nicht zwingend** – manche Lehrbücher empfehlen freie HPI-Erfassung. Der Vorteil ist Vollständigkeit und Vergleichbarkeit.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist OLDCARTS und wofür wird es verwendet?

**Anwendungsfrage:** Wende OLDCARTS auf einen Patienten mit Kopfschmerz an und nenne pro Buchstabe ein Beispielitem.

**Diskussionsfrage:** OLDCARTS ist ein Lehrmittel der ärztlichen Ausbildung – wie verträgt sich das mit der Forderung in StatPearls, „auf Qualität und Klarheit zu achten, statt Details zu überhäufen"? Wo liegt die Grenze zwischen Vollständigkeit und Verschlankung?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zu OPQRST?
- Welche Aspekte sind bei akuten Schmerzen am wichtigsten? Welche bei chronischen Beschwerden?
- Wie würde man OLDCARTS in einem strukturierten EMR-Formular abbilden? (Stichwort: 8 Felder pro HPI-Eintrag)
- Welche FHIR-Resourcen können einzelne OLDCARTS-Items aufnehmen? (Antwort: Observation, Condition, Encounter mit reasonReference)

## Verwandt

- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - HEADSS]]
- [[EHR - SOAP - Review of Systems]]
- [[EHR - SOAP - Prinzip]]

## Quelle

- Vorlesung: [[EHR - Paper - SOAP Notes StatPearls]]
- Folien/Seitenangabe: Sektion „History of Present Illness (HPI)"
