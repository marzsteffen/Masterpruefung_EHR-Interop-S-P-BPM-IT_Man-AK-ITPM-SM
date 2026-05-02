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

# SM - ITIL Practice - Monitoring and Event Management

> [!info] Kurzdefinition
> ITIL-4-Practice (Service Management) zum systematischen Beobachten von Services und Servicekomponenten sowie zum Aufzeichnen und Erstellen von Berichten zu ausgewählten Statusänderungen, die als Events identifiziert wurden.

## Beschreibung

Folie 80 definiert Zweck und Begriff:

**Zweck:**
> „Das systematische Beobachten von Services und Servicekomponenten sowie das Aufzeichnen und Erstellen von Berichten zu ausgewählten Statusänderungen, die als Events identifiziert wurden."

> „Diese Practice identifiziert und priorisiert Infrastruktur, Services, Geschäftsprozesse und Informationssicherheits-Events; ebenfalls reagiert sie angemessen auf diese Events und auf Gegebenheiten, die auf potenzielle Fehler oder Incidents hinweisen."

**Definition Event** (ITIL 4):
> „Jede Statusänderung, die für das Management eines Service oder eines anderen Configuration Items (CI) von Bedeutung ist. Events werden normalerweise durch Benachrichtigungen erkannt, die von einem IT Service, CI oder Monitoring-Tool erstellt werden."

Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Zweck | Systematisches Beobachten, Aufzeichnen, Berichten |
| Identifikations-Scope | Infrastruktur, Services, Geschäftsprozesse, Informationssicherheit |
| Definition Event | Statusänderung mit Bedeutung für CI-Management |
| Typische Quellen | Service, CI, Monitoring-Tool |

## Beispiel

CPU-Auslastung des KIS-Servers überschreitet definierten Schwellwert → Monitoring-Tool erkennt Status-Änderung → Event-Eintrag → Reaktion (Information / Warnung / Auslösen Incident).

## Abgrenzung

- **Monitoring and Event Management vs. ITIL V3 Event Management** (siehe [[SM - ITIL V3 Practice - Event Management]]): ITIL 4 hat eine präzisere Event-Definition (Statusänderung mit Bedeutung für CI-Management) und integriert Informationssicherheits-Events explizit.
- **vs. Incident Management** ([[SM - ITIL Practice - Incident Management]]): Events können Incidents auslösen — Monitoring identifiziert, Incident bearbeitet.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Zweck der Monitoring and Event Management Practice? — Systematische Beobachtung von Services/Komponenten, Aufzeichnung und Berichterstattung zu identifizierten Events.

**Definition Event:** Statusänderung, die für das Management eines Service oder CIs von Bedeutung ist.

**Diskussionsfrage:** Welche Events sind relevant, welche bedeuten nur „Rauschen"? Wie filtert man? — Schwellwerte, Korrelation, KI-Anomalie-Erkennung.

**Mögliche Anschlussfragen:**
- Wie hängt Monitoring and Event Management mit Incident und Problem zusammen?
- Wie verändert Cloud Computing diese Practice ([[SM - ITIL 4 - Cloud Computing Auswirkungen]])?

## Verwandt

- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL Practice - Problem Management]]
- [[SM - ITIL Practice - Service Configuration Management]]
- [[SM - ITIL V3 Practice - Event Management]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 80; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
