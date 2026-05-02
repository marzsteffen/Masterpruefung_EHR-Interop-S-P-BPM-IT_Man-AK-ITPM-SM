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

# EHR - Funktionen - Basisfunktionen

> [!info] Kurzdefinition
> Die Vorlesung leitet aus der EHR-Definition (Margareth & Steven, 2005) sieben funktionale Kernbereiche ab, die ein EHR-System abdecken muss: Datenhaltung & Integration, Workflow-Replikation, Effizienz, Clinical Decision Support, Patient Support, Messaging/Datenverarbeitung, administrative Werkzeuge.

## Beschreibung

Ausgangspunkt ist die Definition von Margareth & Steven (2005, Folie 29):

> "System of hardware, software, people, policy, process, working together to collect data from multiple resources, providing information and decision support to multiple healthcare providers, irrespective of time and place."

Vier Eigenschaften werden hervorgehoben: **Information** (nicht nur Daten), **multiple resources**, **multiple healthcare providers**, **irrespective of time and place**.

Daraus entwickelt die Vorlesung die folgenden funktionalen Bereiche.

## Bestandteile / Aufbau

| Funktion | Inhalte laut PDF |
|---|---|
| **Health Information & Data** | Patientenanamnese, Allergien, Laborbefunde, Diagnosen, aktuelle/frühere Medikation, Integration aus verschiedenen Quellen |
| **Workflow-Replikation** | EHR muss synchron mit dem originalen Workflow der Versorgungs­organisation arbeiten, ihn nicht ersetzen |
| **Effiziente Interaktion** | Muss effektiv arbeiten, Zeit für Versorger und Patienten sparen – kritische Diskussion: tut es das wirklich? Mehr Doku, mehr Eingabezeit? |
| **Clinical Decision Support** | Reminder, Prompts, Alerts – unterstützt Versorger bei Entscheidungen |
| **Patient Support** | Patient soll informiert werden und auf eigene Gesundheitsdaten zugreifen können (Beispiel: OpenNotes – Beth Israel Deaconess Medical Center) |
| **Patient- und Familien-Support** | Patient organisiert sich auch mit Familie – Beispiel: patientslikeme.com, e-patients.net, krankheitserfahrungen.de |
| **Messaging & Datenverarbeitung** | Datenaustausch in Standardformaten, Interoperabilität, Verarbeitung eingehender Daten |
| **Administrative Tools** | Scheduling, Termine, Reminder |

## Beispiel

OpenNotes-Experiment (Folie 33): Patienten lesen die Notizen ihres Arztes online. Studien zeigten erhöhtes Engagement und besseres Selbstmanagement.

## Abgrenzung

- Diese **funktionale** Sicht ist abzugrenzen von den **formalen Anforderungs-Frameworks** ([[EHR - Anforderungen - HIMSS High-Level Requirements]] und [[EHR - Anforderungen - IOM 8 Core Requirements]]), die dieselben Bereiche systematisch und prüfbar formulieren.
- Funktionen ≠ Architektur: Die Funktionen sagen nichts darüber aus, ob das System zentral oder dezentral, Repository oder Registry ist (siehe [[EHR - Architektur - Zentral vs Dezentral]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche grundlegenden Funktionen muss ein EHR erfüllen?

**Anwendungsfrage:** Welche dieser Funktionen sind in ELGA realisiert, welche fehlen aktuell? (z. B. CDS in ELGA – im PDF nicht eindeutig beantwortet)

**Diskussionsfrage:** „Replicate the workflow" – ist es wünschenswert, einen ineffizienten Papier-Workflow 1:1 zu digitalisieren, oder muss Digitalisierung den Prozess transformieren? Vortragender benennt das als Spannungsfeld.

**Mögliche Anschlussfragen:**
- Wie steht „efficient interaction" im Verhältnis zu Studien, die mehr Doku-Zeit durch EHR zeigen?
- Was unterscheidet Clinical Decision Support von einer simplen Alarmierung?
- Welche Rolle spielt Patient Support in der DSGVO-Perspektive auf Datenzugang?

## Verwandt

- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[EHR - Standards - Unterstützte Coding Standards]]
- [[EHR - Portal - Patientenportal]]
- [[EHR - Definition - HIMSS]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 29–38 (Basic functions of EHRs, mehrteilig)
