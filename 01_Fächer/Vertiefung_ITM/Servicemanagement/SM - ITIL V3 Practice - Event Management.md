---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - ITIL V3 Practice - Event Management

> [!info] Kurzdefinition
> Event Management überwacht alle Ereignisse, die in der IT-Infrastruktur geschehen. Ein Event ist ein Ereignis, welches die IT-Infrastruktur beeinflusst. Events werden von Security-Werkzeugen aufgezeichnet, ausgewertet, gefiltert und ggf. eskaliert.

## Beschreibung

Folie 43 zeigt Ziele und Ablauf:

**Ziele:**
- Ein Event ist ein Ereignis, welches die IT-Infrastruktur beeinflusst.
- Events werden von einem Security-Werkzeug aufgezeichnet.
- Überwachung aller Events, die in der IT-Infrastruktur geschehen.

**Ablauf (10 Schritte):**
1. Auftreten eines Events
2. Event-Bericht
3. Event-Erkennung
4. Event-Filterung
5. Event-Klassifizierung
6. Event-Zusammenhänge
7. Auslöser
8. Reaktionsmöglichkeiten
9. Maßnahmen
10. Abschluss des Events

Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008).

In ITIL 4 wird der Prozess als **Monitoring and Event Management Practice** geführt, mit aktualisierter Definition für Event (siehe [[SM - ITIL Practice - Monitoring and Event Management]]).

## Bestandteile / Aufbau

| Schritt | Inhalt |
|---|---|
| Auftreten | Tatsächliches Ereignis in der Infrastruktur |
| Bericht | System gibt Event-Meldung aus |
| Erkennung | System (oder Mensch) erkennt das Event |
| Filterung | Relevante von irrelevanten Events trennen |
| Klassifizierung | Information / Warnung / Ausnahme |
| Zusammenhänge | Korrelation mit anderen Events |
| Auslöser | Was hat das Event verursacht? |
| Reaktionsmöglichkeiten | Welche Optionen gibt es? |
| Maßnahmen | Konkrete Aktion (Incident anlegen, Alarmierung, automatisierte Behebung) |
| Abschluss | Event geschlossen, ggf. dokumentiert |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Krankenhaus-Beispiel:
- Monitoring-Tool meldet hohe CPU-Last am KIS-Server (Event-Auftreten).
- Event-Bericht ans Monitoring-Dashboard.
- Erkennung durch automatisierten Schwellwert.
- Filterung: temporärer Peak vs. anhaltend hohe Last → anhaltend → Klassifizierung „Warnung".
- Zusammenhang: gleichzeitig Backup-Job aktiv → Auslöser identifiziert.
- Reaktion: keine sofortige Aktion nötig (Backup endet bald) → Abschluss.

## Abgrenzung

- **Event vs. Incident** (siehe [[SM - ITIL V3 Practice - Incident Management]]): Event = Ereignis (auch unkritisch); Incident = ungeplante Unterbrechung. Nicht jedes Event wird zum Incident.
- **Event Management vs. Monitoring**: Monitoring ist die kontinuierliche Überwachung; Event Management bewertet die Events und entscheidet über Reaktionen.
- **V3 Event Management vs. ITIL 4 Monitoring and Event Management** (siehe [[SM - ITIL Practice - Monitoring and Event Management]]): Inhaltlich ähnlich, in ITIL 4 mit präziserer Event-Definition: „Jede Statusänderung, die für das Management eines Service oder eines anderen Configuration Items (CI) von Bedeutung ist."

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Event? — Ein Ereignis, welches die IT-Infrastruktur beeinflusst. (V3-Definition; ITIL 4 präzisiert auf „Statusänderung mit Bedeutung für CI-Management".)

**Anwendungsfrage:** Wie verhält sich Event Management zu Incident und Problem Management? — Events können Incidents auslösen; aus mehreren ähnlichen Incidents entsteht ein Problem.

**Diskussionsfrage:** Welche Filtertechniken sind sinnvoll, um „Event Storms" zu vermeiden? — Schwellwerte, Korrelation, Deduplizierung, KI-basierte Anomalie-Erkennung.

**Mögliche Anschlussfragen:**
- Welche Event-Klassifikationen sind üblich? — Information, Warnung, Ausnahme/Exception.
- Wie unterscheidet sich Event Management von Security-Information-and-Event-Management (SIEM)? *(im PDF nicht thematisiert)*
- Wie kann Event Management zu Continual Improvement beitragen? — Auswertung wiederkehrender Events liefert Verbesserungspotenzial.

## Verwandt

- [[SM - ITIL V3 - Service Operation]]
- [[SM - ITIL V3 Practice - Incident Management]]
- [[SM - ITIL V3 Practice - Problem Management]]
- [[SM - ITIL Practice - Monitoring and Event Management]] *(ITIL 4 Pendant)*

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 43; Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
