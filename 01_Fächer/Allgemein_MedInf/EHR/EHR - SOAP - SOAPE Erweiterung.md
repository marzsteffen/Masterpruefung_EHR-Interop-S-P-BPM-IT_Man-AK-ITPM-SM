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

# EHR - SOAP - SOAPE Erweiterung

> [!info] Kurzdefinition
> **SOAPE** ist eine Erweiterung des SOAP-Schemas um einen fünften Buchstaben: **E** für **Evaluate** – die explizite Bewertung, wie gut der vorherige Plan gewirkt hat. Adressiert die zentrale Schwäche von SOAP: die fehlende Zeitdimension.

## Beschreibung

Aus StatPearls (Sektion „Issues of Concern"):

> „A weakness of the SOAP note is the inability to document changes over time. In many clinical situations, evidence changes over time, requiring providers to reconsider diagnoses and treatments. An important gap in the SOAP model is that it does not explicitly integrate time into its cognitive framework. Extensions to the SOAP model to include this gap are acronyms such as SOAPE, with the letter E as an explicit reminder to assess how well the plan has worked."

## Bestandteile / Aufbau

| Buchstabe | Inhalt |
|---|---|
| **S** | Subjective |
| **O** | Objective |
| **A** | Assessment |
| **P** | Plan |
| **E** | **Evaluate** – Bewertung der Wirksamkeit des Plans |

Die E-Sektion fragt explizit:
- Hat der Plan die gewünschte Wirkung erzielt?
- Wo bleibt der Patient hinter den Erwartungen zurück?
- Welche Konsequenzen ergeben sich für den nächsten SOAP-Zyklus?

## Beispiel

SOAPE bei einer Diabetes-Folgevisite (3 Monate nach Therapie­beginn):
- **S:** Patient berichtet weniger Müdigkeit
- **O:** HbA1c 6,8 % (Vorwert 7,8 %), Gewicht -3 kg
- **A:** Diabetes Typ 2 unter Therapie verbessert
- **P:** Metformin fortsetzen, BZ-Selbstkontrolle weiter führen, Wiedervorstellung in 3 Monaten
- **E:** Ziel HbA1c < 7,0 % erreicht (Ausgangsziel definiert in voriger Visite). Patient compliant mit Therapie. Metformin-Dosis ausreichend, keine Anpassung nötig. Nächste Evaluation des Lebensstil-Zielgewichts (-5 kg) bei Folgevisite.

## Abgrenzung

- SOAPE ≠ Progress Notes: Progress Notes ([[EHR - SOAP - Progress Notes]]) bilden den Verlauf über mehrere SOAP-Notes ab, indem die Inhalte aufeinander Bezug nehmen. SOAPE integriert die Verlaufs­bewertung **innerhalb einer einzelnen Note** als eigenen Block.
- SOAPE ist eine Erweiterung – kein Ersatz. SOAP-Inhalte bleiben gleich, nur die Plan-Bewertung wird explizit.
- SOAPE hat sich praktisch **nicht durchgesetzt** – SOAP bleibt der dominante Standard.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist SOAPE und welche Schwäche von SOAP adressiert es?

**Anwendungsfrage:** Erstelle eine SOAPE-Note für einen Folgepatienten mit Hypertonie – wie unterscheidet sich der E-Block von einer reinen SOAP-Note?

**Diskussionsfrage:** Warum hat sich SOAPE in der Praxis nicht etabliert, obwohl es die identifizierte Schwäche von SOAP adressiert? Welche Hindernisse stehen im Weg (Gewohnheit, fehlender EMR-Support, Aufwand)?

**Mögliche Anschlussfragen:**
- Welche FHIR-Resource könnte den E-Block abbilden? (Antwort: `Goal` mit Ziel-Achievement; `CarePlan.activity.outcome`; `Procedure.outcome`)
- Welche Alternativen zu SOAPE gibt es, die Verlauf integrieren? (Stichwort: APSO + Verlaufsdiagramm; PIE; DAR)
- Wie würde ein modernes EMR die E-Bewertung automatisieren können?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Plan]]
- [[EHR - SOAP - Progress Notes]]
- [[EHR - SOAP - Schwächen und Kritik]]

## Quelle

- Vorlesung: [[EHR - Paper - SOAP Notes StatPearls]]
- Folien/Seitenangabe: Sektion „Issues of Concern" (letzter Absatz, SOAPE-Erweiterung)
