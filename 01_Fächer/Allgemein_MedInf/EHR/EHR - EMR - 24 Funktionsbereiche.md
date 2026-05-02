---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - Spec - BPHC EMR Functional Specs Cerner]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - EMR - 24 Funktionsbereiche

> [!info] Kurzdefinition
> Die 24 Sektionen des BPHC Functional Requirements Document bilden eine strukturierte Übersicht über die typischen Funktionsbereiche eines klinischen EMR – brauchbar als Bewertungsraster für jede Beschaffungs- oder Reife­bewertung eines EMR-Systems.

## Beschreibung

Das BPHC-Dokument gliedert die EMR-Anforderungen in 24 nummerierte Funktionsbereiche (Sektion 22 bleibt leer; im Original-Index als „No Section" markiert). Sie bilden ein robustes generisches Bewertungsraster, das auch über das konkrete Cerner-Angebot hinaus Geltung hat.

## Bestandteile / Aufbau

### Klinische Funktionen (Sektionen 1–18)

| # | Sektion | Kerninhalt laut PDF |
|---|---|---|
| 1 | **General** | Coding-Standards, HIPAA, Vocabularies, Datums-Stempel, integrierte Standard-Nomenklatur, Speicher- und Performance-Dimensionierung |
| 2 | **Demographics** | HL7-Import von Stammdaten, permanente und temporäre Adressen |
| 3 | **Medical History** | Anamnese (rapid capture), Risk Factors (Tobacco, Alcohol, Drugs, Occupation), Sozialanamnese, Hospitalisierungs-Daten, Allergien, Immunisierungen, Familienanamnese, Genogramme |
| 4 | **Current Health Data, Encounters, Health Risk Appraisal** | HL7-basierter Lab-/Imaging-Import, Health Risk Factors, Problem-orientierte Encounter-Sicht, SF-36-Survey, Vital Signs (Height, Weight, Pulse, Respiratory Rate, BP), Functional Level, freier Text |
| 5 | **Encounter – Progress Notes** | Strukturierte Progress Notes, dynamische Dokumentation entlang Coding-Regeln |
| 6 | **Problem Lists** | Aktive und historische Probleme, Verknüpfung zu Encounters |
| 7 | **Clinical Practice Guidelines (CPG)** | Integration und Anwendung von Leitlinien |
| 8 | **Care Plan** | Versorgungspläne |
| 9 | **Prevention** | Präventionsempfehlungen, Health Maintenance |
| 10 | **Patient Education** | Patientenaufklärung |
| 11 | **Alerts** | Warnungen, Reminder, Notifikationen |
| 12 | **Orders** | Order Management |
| 13 | **Results** | Befund-Management |
| 14 | **Medications** | Medikationsmanagement, Drug-Drug-Interaction |
| 15 | **Confidentiality and Security** | Biosensor-Logon, elektronische Signaturen, RBAC, Audit Trails, Audit-Analyse |
| 16 | **Decision Support** | Clinical Decision Support, Triggers, Alerts an Behörden (z. B. CDC) |
| 17 | **Cost Measuring/Quality Assurance** | Kostenmessung, Qualitätssicherung |
| 18 | **Disease Management/Clinical Registries** | Registries, populationsbezogene Versorgung |

### Technische Funktionen (Sektionen 19–21)

| # | Sektion | Kerninhalt |
|---|---|---|
| 19 | **Technical** | Skalierbarkeit, einheitliche UI, Input-Modalitäten, 99,5 % Verfügbarkeit, < 2 s Antwortzeit zu 90 %, sub-second zu 80 %, Remote-Monitoring, Locking, Redundanz/Fault-Tolerance, Transaction-Logs |
| 20 | **Clinical IT Data Dictionary** | Datenmodell-Attribute, statische/dynamische Beziehungen |
| 21 | **Input Mechanisms** | Voice Recognition, Touch Screen, Light Pen, Maus, Tastatur, freier Text + diskrete Daten |

### Ergonomie & Implementierung (Sektionen 23–24)

| # | Sektion | Kerninhalt |
|---|---|---|
| 23 | **Ergonomic Presentation** | User-Friendliness, konsistente Präsentation, Visual Cues |
| 24 | **Implementation and Support** | Implementierungs­plan, Skills Assessment, Training, Wartung, Netzwerk-Support |

## Beispiel

Die Sektion **15 Confidentiality and Security** illustriert, wie konkret die Anforderungen formuliert sind:
- Biosensor-Technologie für Logon (Opt)
- Elektronische Signaturen (Min)
- Multi-Level-Access-Control mit RBAC (Min)
- Patient/Physician-Daten-Vertraulichkeit (Opt)
- Lokationsunabhängiger Zugriff (Min)
- Audit Trails pro Daten-Zugriff (Min)
- Automatische Audit-Trail-Analyse (Min)
- B2-zertifiziertes OS (Min)

## Abgrenzung

- Diese 24 Sektionen sind **systemzentriert** (was muss das System können). Sie sind nicht das Gleiche wie die [[EHR - Anforderungen - IOM 8 Core Requirements]], die **versorgungs­zentriert** strukturiert sind, oder die [[EHR - Anforderungen - HIMSS High-Level Requirements]], die in 4 Themen­blöcken zusammenfassen.
- Es gibt deutliche **Überlappungen**: IOM-Result Management ↔ Sektion 13 Results; IOM-Decision Support ↔ Sektion 16; HIMSS Data Protection ↔ Sektion 15.
- 2003-Stand: einige moderne Themen fehlen (FHIR-API, Cloud, Mobile, KI-CDS, Patient-generated Data, Telemedizin).

## Prüfungsrelevanz

**Typische Definitionsfrage:** In welche groben Funktionsblöcke gliedert sich ein typisches RFP für ein EMR? Nenne 8–10 Sektionen.

**Anwendungsfrage:** Welche der 24 Sektionen ist in modernen EMRs durch FHIR-Standardisierung am stärksten transformiert worden?

**Diskussionsfrage:** Ist eine Bewertung über 24 Funktionsbereiche überhaupt zeitgemäß, oder müsste 2025 Plattformfähigkeit (FHIR-API, App-Ökosystem, AI-Integration) den Vorrang haben?

**Mögliche Anschlussfragen:**
- Welche Sektion enthält die meisten Min-Anforderungen?
- Wie verteilen sich die IOM 8 Core Requirements auf diese 24 Sektionen?
- Welche Sektion ist am US-spezifischsten (Hinweis: 1, 17 mit Cost/Quality, 16 wegen CDC-Reporting, 24 mit Implementations-Vorgaben)?
- Welcher Funktionsbereich fehlt deutlich? (Antwort: Patient-Portal/Engagement, Telemedizin, KI-CDS, Genomics)

## Verwandt

- [[EHR - Beschaffung - Functional Requirements Document]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - Beispiel - Cerner PowerChart Office]]

## Quelle

- Vorlesung: [[EHR - Spec - BPHC EMR Functional Specs Cerner]]
- Folien/Seitenangabe: Seite 8 (Inhaltsverzeichnis), Seiten 9–37 (alle Sektionen)
