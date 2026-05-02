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

# EHR - SOAP - Prinzip

> [!info] Kurzdefinition
> SOAP ist das international etablierte Dokumentationsschema für Patientenbegegnungen mit den vier sequentiellen Komponenten **Subjective – Objective – Assessment – Plan**. Eine Dokumentation nach SOAP wird als „SOAP Note" bezeichnet.

## Beschreibung

Das SOAP-Prinzip strukturiert die Dokumentation einer Patientenbegegnung entlang des natürlichen Visiten-Ablaufs:

> „Healthcare is event driven – we go to a physician when something is wrong. Healthcare documentation is governed by the SOAP principle."

## Bestandteile / Aufbau

| Komponente | Inhalt | Quelle der Information |
|---|---|---|
| **S – Subjective** | Aktuelle Beschwerden, narrative Schilderung | Patient (subjektiv) |
| **O – Objective** | Messbare, reproduzierbare, nachvollziehbare Fakten | Untersuchung, Messung |
| **A – Assessment** | Ärztliche Diagnose (narrativ und/oder kodiert) | Arzt |
| **P – Plan** | Geplante Behandlung, Diagnostik, Überweisungen | Arzt |

## Beispiel

Typische Visite beim Hausarzt (PCP):

```
PCP: "What's wrong?"
Patient: "I feel..."                                  → Subjective
PCP: "We will do a few measurements..."               → Objective
PCP: "I conclude you have ..." (Diagnose)             → Assessment
PCP: "Let's do the following..."                      → Plan
```

## Abgrenzung

- SOAP ≠ Patient History: SOAP ist eine **Dokumentation pro Visite**, History ist ein Verlaufs­container über mehrere Visiten.
- SOAP ist eine **3. Dimension** des problem-orientierten Records ([[EHR - Datenmodelle - Klassische Record Typen]]) – nicht zu verwechseln mit time-orientierten oder source-orientierten Records.
- SOAP ≠ APSO: APSO hat dieselben Inhalte, nur in anderer Reihenfolge ([[EHR - SOAP - APSO Variante]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wofür steht SOAP, und wozu dient es?

**Anwendungsfrage:** Beschreibe eine konkrete Patientenbegegnung in SOAP-Form.

**Diskussionsfrage:** Warum hat sich SOAP gegenüber rein narrativen Notes durchgesetzt? Welche Vorteile bringt die Strukturierung – auch für Sekundärnutzung?

**Mögliche Anschlussfragen:**
- Wer hat SOAP erfunden? (Antwort: Lawrence Weed in den 1960ern; Folie nicht explizit – Ergänzung außerhalb der Vorlesung)
- Welche FHIR-Resourcen entsprechen welcher SOAP-Komponente? (siehe [[EHR - SOAP - Subjective]] etc.)
- Warum ist die Trennung S/O so wichtig?
- Welche Alternativen zu SOAP gibt es (DAR, PIE, APSO)?

## Ergänzung außerhalb der Vorlesung

Das SOAP-Schema wurde in den 1960er-Jahren von **Lawrence L. Weed** als Teil des **Problem-Oriented Medical Record (POMR)** eingeführt – darum ist SOAP konzeptionell eng mit dem problem-orientierten Record verbunden. Es ist heute der international dominante Dokumentationsstandard in der ärztlichen Praxis.

## Verwandt

- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Plan]]
- [[EHR - SOAP - Progress Notes]]
- [[EHR - SOAP - APSO Variante]]
- [[EHR - Datenmodelle - Klassische Record Typen]]

## Quelle

- Vorlesung: [[EHR - VL - SOAP Notes]]
- Folien/Seitenangabe: Folien 1–3 (SOAP-Prinzip, typische Visite)
