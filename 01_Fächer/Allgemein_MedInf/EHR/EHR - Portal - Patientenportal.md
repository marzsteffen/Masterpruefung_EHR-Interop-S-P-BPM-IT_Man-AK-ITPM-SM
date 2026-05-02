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

# EHR - Portal - Patientenportal

> [!info] Kurzdefinition
> Web-basierter Zugang, über den Patienten (oder Versorger) per Browser auf ihre Gesundheitsdaten zugreifen können. Standard-Bestandteil moderner EHR-Systeme; Ankerpunkt für Patient Empowerment.

## Beschreibung

Vorlesung Folien 68–72: „Most EHR systems have a (patient) portal. Allows patients / providers to log in using a web browser and inspect (their) data."

Konkret im PDF genannte österreichische Beispiele:
- **ELGA-Portal**: gesundheit.gv.at/gesundheitsleistungen/elga.html
- **KAGes-Portal** (zwei Portale):
  - medizin-portal.kages.at (für Versorger)
  - patienten-portal.kages.at (für Patienten)

US-Vergleichsbeispiel: **Mayo Clinics Patient Portal**.

Übungsfragen aus dem PDF:
- Was ist der Unterschied zwischen den beiden KAGes-Portalen?
- Welche Funktionalitäten sind verfügbar?
- Wie funktioniert der Login (Security)?
- Beim Patientenportal: welche weiteren Funktionen sind geplant?
- Vergleich Mayo Clinics ↔ KAGes / ELGA.

Zusätzlich verweist das PDF auf eine Reading-Übung: „Impact of Health Portal Enrollment With Email Reminders on Adherence to Clinic Appointments: A Pilot Study" – Diskussion: interventional vs. observational, Kontrollgruppe, Population, statistische Relevanz.

## Bestandteile / Aufbau

Typische Portal-Funktionen (im PDF angedeutet, nicht vollständig definiert):
- Einsicht in eigene Daten
- Login / Authentifizierung
- Termin-Adhärenz, Reminder
- Kommunikation mit Versorgern (im PDF nicht explizit, aber durch HIMSS-Definition impliziert)

## Abgrenzung

- Patient Portal ≠ PHR ([[EHR - Abgrenzung - EMR CPR EPR PHR]]): Ein Portal ist die **Zugriffs-Schnittstelle** zu einer EHR/EMR; ein PHR ist eine **patientenkontrollierte** Akte. Manche Systeme verwischen die Grenze.
- Patient Portal ≠ Versorger-Portal: KAGes hat zwei getrennte Portale.
- Funktionalität variiert massiv zwischen Systemen (Mayo Clinics vs. ELGA-Portal).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Patientenportal, und welche Funktionen erfüllt es typischerweise?

**Anwendungsfrage:** Vergleiche das ELGA-Portal mit dem KAGes-Patientenportal: Welche Funktionalitäten sind ähnlich, welche unterscheiden sich? (Diskussion offen, da im PDF als Übung formuliert)

**Diskussionsfrage:** Patientenportale steigern Patient Engagement – aber wie verträgt sich das mit Sicherheits- und Auditanforderungen aus [[EHR - Anforderungen - HIMSS High-Level Requirements]]? Welche Authentifizierungs-Anforderungen sind angemessen?

**Mögliche Anschlussfragen:**
- Wie funktioniert der Login bei ELGA (Stichwort: ID Austria, Handy-Signatur)?
- Welche Daten sind im ELGA-Portal sichtbar, welche nicht?
- Welche Rolle spielt das Portal bei der Umsetzung der IOM-Anforderung „Patient Support"?
- Zur Pilotstudie: was bedeutet „interventional" vs. „observational" – und welcher Typ ist dort gegeben?

## Verwandt

- [[EHR - Abgrenzung - EMR CPR EPR PHR]]
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[ASP - Authentifizierung]]
- [[EHR - VL - ELGA Portal]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 68–72 (Portals, Übungsfragen)
