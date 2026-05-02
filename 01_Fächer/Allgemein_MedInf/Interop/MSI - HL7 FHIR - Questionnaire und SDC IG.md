---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - Questionnaire und SDC IG

> [!info] Kurzdefinition
> FHIR Questionnaire ist eine Ressource zur Modellierung von medizinischen Formularen. Der **SDC IG** (Structured Data Capture Implementation Guide) erweitert Questionnaire um Funktionen wie Vorbefüllung und Datenextraktion aus FHIR-Ressourcen.

## Beschreibung

Aus Seite 9:

- **SDC IG:** `https://build.fhir.org/ig/HL7/sdc/` (Structured Data Capture)
- Arbeitet mit **FHIR Questionnaires**, die:
  - **Vorbefüllt** werden können (Pre-population aus FHIR-Ressourcen)
  - Aus denen **Daten extrahiert** werden können (in FHIR-Ressourcen)
- **Tool für Questionnaire-Erstellung:** `https://formbuilder.nlm.nih.gov/`

Weitere Details (Questionnaire-Struktur, SDC-Erweiterungen) wurden im PDF nicht ausgeführt.

## Bestandteile / Aufbau

Im PDF nicht ausgeführt. Erwähnte Konzepte:

| Begriff | Bedeutung laut PDF |
|---|---|
| FHIR Questionnaire | FHIR-Ressource zur Formulardefinition |
| Vorbefüllung (Pre-population) | Automatisches Befüllen von Formularfeldern aus FHIR-Daten |
| Datenextraktion | Übertragung von Formularantworten in strukturierte FHIR-Ressourcen |
| SDC IG | Implementation Guide, der Questionnaire um SDC-Fähigkeiten erweitert |

## Beispiel

NLM Form Builder (`https://formbuilder.nlm.nih.gov/`) als grafisches Werkzeug zur Erstellung von FHIR-Questionnaires.

## Abgrenzung

- **Questionnaire ≠ QuestionnaireResponse**: Questionnaire ist die Formulardefinition; QuestionnaireResponse enthält die ausgefüllten Antworten eines konkreten Patienten.
- **SDC IG ≠ Basis-Questionnaire**: Das Basis-FHIR-Questionnaire ist simpel; SDC erweitert es um Pre-population, Extraktion, adaptive Formulare und weitere Features.
- **Questionnaire ≠ HL7 CDA Formular**: CDA-Dokumente sind narrative/strukturierte Dokumente; Questionnaire ist ein interaktives Formular-Modell.

## Prüfungsrelevanz

**Mittel.**

**Typische Definitionsfrage:** Was ist der Unterschied zwischen Questionnaire und QuestionnaireResponse in FHIR?

**Anwendungsfrage:** Wie würde man ein standardisiertes Anamnese-Formular mit automatischer Vorbefüllung aus der Patientenakte umsetzen?

**Diskussionsfrage:** Welche Vorteile bietet die SDC-Extraktion gegenüber manueller Dateneingabe?

**Mögliche Anschlussfragen:**
- Was ist der SDC IG und welche Kernfunktionen fügt er hinzu?
- Wie hängt SDC mit der Semantic Interoperability zusammen? (→ strukturierte Extraktion aus Freitext-Formularen in maschinenlesbare FHIR-Ressourcen)

## Verwandt

- [[MSI - HL7 FHIR - Implementation Guide]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - CQL]]

## Quelle

- Vorlesung: [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]
- Folien/Seitenangabe: Seite 9
