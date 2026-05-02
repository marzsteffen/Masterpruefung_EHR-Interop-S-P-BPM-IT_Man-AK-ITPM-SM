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

# EHR - SOAP - APSO Variante

> [!info] Kurzdefinition
> **APSO** ist eine alternative Reihenfolge der SOAP-Inhalte: **Assessment, Plan, Subjective, Objective**. Inhalt identisch mit SOAP, aber Diagnose und Behandlungsplan stehen vorne – viele Ärzte bevorzugen das beim **Lesen** von Progress Notes.

## Beschreibung

Folie 20:

> „For reading progress notes, (many) physicians prefer the APSO format (Assessment, Plan, Subjective, Objective)."

Verwiesene Artikel:
- „Physicians rethinking the progress note" – healthcareitnews.com
- „Clinical Leaders Discuss SOAP vs. APSO" – healthcare-informatics.com

Die Vorlesung wirft die offene Diskussionsfrage auf: „Discussion: how would you resolve this issue?"

## Bestandteile / Aufbau

Vergleich der Reihenfolgen:

| Reihenfolge | Anwendung |
|---|---|
| **SOAP** | Subjective → Objective → Assessment → Plan – folgt dem Ablauf der Visite (chronologisch beim Schreiben) |
| **APSO** | Assessment → Plan → Subjective → Objective – stellt Diagnose und Plan voran (für schnelles Lesen) |

## Beispiel

Lesesituation in der Praxis:
- **SOAP-Lesefluss:** Arzt scrollt durch lange Subjective-Texte, bevor er die Diagnose findet → ineffizient bei Verlaufs­visiten.
- **APSO-Lesefluss:** Arzt sieht zuerst „Diagnose: Diabetes mellitus, gut eingestellt; Plan: Metformin fortsetzen, HbA1c in 3 Mo." → schnelle Orientierung, Details bei Bedarf darunter.

## Abgrenzung

- **APSO ≠ alternativer Inhalt:** Beide Formate enthalten dieselben vier Komponenten – nur die Reihenfolge ist anders.
- **APSO ist eine Lese-Optimierung**, kein Dokumentations­standard. Die Erfassung folgt häufig weiterhin SOAP, das EMR rendert dann APSO.
- Diskussion: Manche EMRs erlauben das **dynamische Umsortieren** der Anzeige – die Daten sind strukturiert dieselben.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet APSO und wie unterscheidet es sich von SOAP?

**Anwendungsfrage:** In welcher Situation ist APSO praktisch besser als SOAP? In welcher Situation ist SOAP überlegen?

**Diskussionsfrage:** „How would you resolve this issue?" (Folie 20). Mögliche Antwort: Dokumentation entkoppelt von Anzeige – das EMR speichert strukturiert (FHIR-Resourcen wie Condition, CarePlan, Encounter, Observation), die Anzeige rendert dann auf Wunsch SOAP oder APSO.

**Mögliche Anschlussfragen:**
- Welche EMR-Hersteller bieten dynamisches Umsortieren?
- Warum wurde APSO erst nach Einführung elektronischer Records relevant? (Antwort: Auf Papier ist die Reihenfolge fix, im EMR kann die Anzeige rekonfiguriert werden)
- Welche Auswirkungen hat APSO auf NLP-/AI-Auswertungen von Free-Text-Notes?

## Verwandt

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Progress Notes]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folie 20 (APSO versus SOAP, mit Diskussionsfrage)
