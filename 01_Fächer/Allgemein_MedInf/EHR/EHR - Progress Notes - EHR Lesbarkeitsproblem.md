---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - Paper - Lin 2013 SOAP vs APSO Provider Satisfaction]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Progress Notes - EHR Lesbarkeitsproblem

> [!info] Kurzdefinition
> Strukturelles Problem moderner EHR-Progress-Notes: Sie können bis zu 17 elektronische Seiten umfassen, weil Billing-Anforderungen, regulatorische Statements und automatisch eingebettete Test-Ergebnisse die klinisch relevante Information überdecken. Das **Auffinden des Clinical Reasoning** wird dadurch extrem erschwert.

## Beschreibung

Aus dem Paper Lin et al. (2013) als Motivation für die APSO-Studie:

> „A health care provider's EHR progress notes are essential for effective communication. However, these notes may increase errors when they are difficult to read. Billing requirements, regulatory statements, and extensive inclusion of test results detract from progress note brevity and clarity. In our experience, EHR progress notes that include such elements can span 17 electronic pages, rendering actual clinical reasoning extraordinarily difficult to locate. Missing data can lead to lost productivity and increased cost. Health care providers' frustration with EHR progress notes may interfere with EHR adoption and deployment."

## Bestandteile / Aufbau

Drei Hauptursachen für die Aufblähung von EHR-Progress-Notes:

| Ursache | Inhalt | Wirkung |
|---|---|---|
| **Billing requirements** | Verpflichtende Dokumentation für Abrechnung (US: CMS E/M Levels) | künstlich erweiterte Inhalte zur Erfüllung von Reimbursement-Levels |
| **Regulatory statements** | Pflicht­textbausteine aus regulatorischen Vorgaben | Boilerplate-Text ohne klinischen Wert |
| **Auto-inclusion of test results** | Automatisch eingefügte Lab-/Imaging-Ergebnisse | Datenmenge ohne klinische Filterung |

## Beispiel

Folgen laut Paper:
- Notes von **bis zu 17 elektronischen Seiten**
- Clinical Reasoning ist „extraordinarily difficult to locate"
- **Missing data** durch Übersehen → Produktivitätsverlust und höhere Kosten
- **Provider-Frustration** behindert EHR-Adoption und -Deployment

Konkretes Szenario: Ein Arzt sucht in einer 17-seitigen EHR-Note nach der Assessment-Sektion eines Kollegen → muss durch automatisch eingefügte Labordaten, regulatorische Boilerplates und Vital-Signs-Verläufe scrollen → übersieht möglicherweise die Diagnose oder den geänderten Behandlungsplan.

## Abgrenzung

- Das Lesbarkeitsproblem ist **strukturell**, nicht autoren-spezifisch – auch sorgfältige Autoren erzeugen aufgeblähte Notes, weil das EMR es technisch begünstigt.
- Es ist **abgrenzbar** vom rein orthographischen Lesbarkeits­problem handgeschriebener Notes (das EHRs ja eigentlich lösen sollten).
- Es ist auch **abgrenzbar** vom Daten-Quality-Problem (Datenmenge ≠ Datenqualität).
- StatPearls greift dasselbe Problem auf (siehe [[EHR - SOAP - Schwächen und Kritik]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was beschreibt das „EHR-Lesbarkeitsproblem" und welche drei Hauptursachen werden im Paper Lin et al. genannt?

**Anwendungsfrage:** Wie würde ein modernes EHR-System dieses Problem strukturell adressieren? Nenne 3 konkrete Maßnahmen.

**Diskussionsfrage:** Das Paper benennt das Problem 2013. Hat sich die Lage seither verbessert oder verschlechtert (Stichwort: KI-/LLM-Integration, FHIR-API-Apps, Note-Bloat)? Argumente in beide Richtungen.

**Mögliche Anschlussfragen:**
- Was sind „CMS Evaluation/Management Levels" und wie führen sie zu Note-Bloat?
- Welche Rolle spielt Note-Cloning („Copy-Forward") für das Problem?
- Wie kann Reformatierung (APSO statt SOAP) das Symptom lindern, ohne die Ursache zu beseitigen?
- Welche Lösungsansätze gibt es: Note-Templates, Smart-Phrases, Macros, KI-Zusammenfassungen?

## Verwandt

- [[EHR - SOAP - Schwächen und Kritik]]
- [[EHR - SOAP - APSO Variante]]
- [[EHR - Studie - APSO Adoption Lin 2013]]
- [[EHR - SOAP - Templates]]
- [[EHR - SOAP - Progress Notes]]

## Quelle

- Vorlesung: [[EHR - Paper - Lin 2013 SOAP vs APSO Provider Satisfaction]]
- Folien/Seitenangabe: Einleitung des Letters (Absatz 1, S. 160)
