---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Macro-Level Interoperabilität]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - eHealth Capabilities - Information Flows

> [!info] Kurzdefinition
> Liste typischer eHealth-Capabilities (Informationsflüsse), die ein modernes nationales Gesundheits-Informationssystem unterstützen sollte – von klinischer Dokumentation bis zu Video-Konsultation und digitalen Interventions-Apps.

## Beschreibung

Die Folie „Information flows / ehealth capabilities" listet die Capabilities, die in einem reifen eHealth-System adressiert sein sollten. Sie wirken zunächst wie eine Aufzählung, sind aber als Bewertungs-Checkliste für nationale Architektur-Pläne gedacht.

## Bestandteile / Aufbau

Capabilities laut Folie:
- Clinical documentation sharing
- Diagnostic image sharing
- Laboratory orders and reports
- Insurance claims reimbursement
- Public health reporting
- Prescription to drug-drug-interaction decision support
- Appointment booking
- Rescue service to ambulance to ER
- Clinical trials hires/reports/monitoring
- Professionals registration
- Healthcare providers registration
- Home monitoring
- Self-triage to referral
- Video consultation
- Digital intervention apps

## Beispiel

Anwendung als Checkliste für ELGA: welche dieser Capabilities sind in ELGA realisiert (z. B. e-Befunde = Clinical documentation sharing, e-Medikation = Prescription to drug-drug-interaction), welche fehlen oder liegen außerhalb (Video Consultation, Digital intervention apps).

## Abgrenzung

- Diese Liste ist **deskriptiv**, nicht normativ – kein offizielles Reifegradmodell.
- Capabilities ≠ Use Cases: Ein Use Case ist ein konkreter Workflow; eine Capability ist die generische Fähigkeit.
- Stark verwandt mit der MITRE Maturity-Matrix, die diese Capabilities um Bewertungs-Dimensionen ergänzt ([[EHR - Maturity Model - MITRE HISCF]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Nenne 5–7 typische eHealth-Capabilities, die ein nationales System unterstützen sollte.

**Anwendungsfrage:** Welche Capabilities sind in Österreich im ELGA-Kern verankert, welche werden außerhalb (z. B. von Krankenkassen, Apps) bereitgestellt?

**Diskussionsfrage:** Welche Capabilities verlangen am stärksten nach Standards (z. B. FHIR, IHE), welche eher nach Governance-Lösungen (z. B. Identity Management)?

**Mögliche Anschlussfragen:**
- Was ist „self-triage to referral" und wo wird es heute schon umgesetzt?
- Welche Capability hat den größten Reifegrad-Sprung in den letzten 5 Jahren gemacht?
- Welche Capability fehlt in der Liste deiner Meinung nach? (z. B. Genomics, AI-basierte CDS, Patient-generated Data)

## Verwandt

- [[EHR - Maturity Model - MITRE HISCF]]
- [[EHR - Datensharing - Logic Modes]]
- [[EHR - HL7 FHIR - 5 Levels]]
- [[EHR - Funktionen - Basisfunktionen]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folie „Information flows / ehealth capabilities"
