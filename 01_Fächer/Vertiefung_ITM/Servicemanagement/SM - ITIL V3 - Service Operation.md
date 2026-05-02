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

# SM - ITIL V3 - Service Operation

> [!info] Kurzdefinition
> Service Operation ist die Phase im ITIL-V3-Lebenszyklus, in der IT-Services im laufenden Betrieb erbracht werden. Sie umfasst fünf zentrale Prozesse: Request Fulfillment, Access Management, Incident Management, Event Management, Problem Management — die untereinander vernetzt sind.

## Beschreibung

Im V3-Lifecycle ist Service Operation die obere Phase des Diagramms (siehe [[SM - ITIL V3 - Servicelebenszyklus]]). Sie ist das operative Herz des ITSM — hier werden die Services tatsächlich erbracht und Störungen behoben. Folien 40–44 zeigen die Detail-Diagramme der Teilprozesse mit ihren Beziehungen.

Das wiederkehrende Diagramm in Folien 40–44 zeigt fünf Boxen mit Pfeilen:

```
Request                Access
Fulfillment  ────────► Management
                         │
                         ▼
Event           Incident
Management ──► Management
                  │
                  ▼
                Problem
                Management
```

Die Pfeile zeigen typische Auslöser und Eskalationen:
- **Event Management** triggert **Incident Management**, wenn ein Event als Störung erkannt wird.
- **Request Fulfillment** kann **Access Management** anstoßen, wenn der Request einen Zugriff betrifft.
- **Incident Management** kann an **Problem Management** weiterleiten, wenn die Ursache eines wiederkehrenden Incidents gesucht werden muss.
- **Access Management** wird bei Bedarf bei Incidents oder Requests aktiviert.

Quelle der Detail-Folien: *Service Operation: Eine Management Guide; Zaltbommel: Van Haren Publishing, 2008.*

## Bestandteile / Aufbau

| Prozess | Auslöser | Outcome | Detail-Note |
|---|---|---|---|
| Request Fulfillment | Anfrage Standardservice | Service-Bereitstellung | [[SM - ITIL V3 Practice - Request Fulfillment]] |
| Access Management | Zugriffsanfrage | Berechtigung gesetzt | [[SM - ITIL V3 Practice - Access Management]] |
| Event Management | technisches Ereignis | Bewertung, ggf. Incident | [[SM - ITIL V3 Practice - Event Management]] |
| Incident Management | Service-Ausfall / -Störung | Wiederherstellung | [[SM - ITIL V3 Practice - Incident Management]] |
| Problem Management | wiederkehrende Incidents / Major Incident | Ursachenanalyse, Workaround, Known Error, dauerhafte Lösung | [[SM - ITIL V3 Practice - Problem Management]] |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Beispielablauf in einer Krankenhaus-IT:

1. **Event Management:** Monitoring meldet Lastpeak im KIS-Server.
2. **Incident Management:** Pflegekraft meldet, dass das KIS „extrem langsam" ist — Ticket eröffnet.
3. **Access Management:** Während Diagnose stellt sich heraus, dass eine Berechtigung versehentlich entzogen wurde — Access Management korrigiert.
4. **Problem Management:** Selber Effekt zum dritten Mal in einem Monat — Problem Management identifiziert die Ursache (fehlerhafter Berechtigungs-Sync) und liefert Workaround + dauerhaften Fix als Known Error.
5. **Request Fulfillment:** Pflegekraft beantragt regulär einen zusätzlichen User-Account (Standard-Service).

## Abgrenzung

- **Service Operation V3 vs. Service Operation in ITIL 4**: ITIL 4 ersetzt die Lifecycle-Phasen durch das SVS und die Service-Wertschöpfungskette (siehe [[SM - ITIL 4 - Service-Wertschöpfungskette]]). Die V3-Service-Operation-Prozesse leben in ITIL 4 aber weitgehend als Practices weiter (Incident Management, Problem Management, Service Request Management, Service Desk).
- **Service Operation vs. Service Transition**: Operation ist Tagesgeschäft; Transition ist Überführung neuer/geänderter Services in den Betrieb (Change Management).
- **Service Operation vs. CSI**: Operation ist Status quo; CSI ist Verbesserung über die Zeit.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche fünf Prozesse umfasst Service Operation laut V3? — Request Fulfillment, Access Management, Incident Management, Event Management, Problem Management.

**Anwendungsfrage:** Skizzieren Sie das Zusammenspiel der Service-Operation-Prozesse anhand eines konkreten Vorfalls (z. B. „KIS ist im OP-Bereich abgestürzt"). Welche Prozesse werden in welcher Reihenfolge aktiv?

**Diskussionsfrage:** Wie unterscheiden sich Incident Management und Problem Management? — Incident: Wiederherstellung des Services (so schnell wie möglich, ggf. mit Workaround); Problem: Ursachenanalyse und dauerhafte Lösung. Beide sind in ITIL 4 weiterhin separate Practices.

**Mögliche Anschlussfragen:**
- Welche dieser V3-Prozesse haben in ITIL 4 ein direktes Pendant? — Alle, in den ITIL-4-Practices: Incident Management, Problem Management, Service Request Management (Request Fulfillment), Monitoring and Event Management (Event Management). Access Management ist in ITIL 4 als Information Security Management gelistet (überlappend, aber nicht 1:1).
- Welche Rolle spielt der Service Desk in Service Operation? — Single Point of Contact (SPOC); in V3 oft als „Function" und nicht eigener Prozess geführt.
- Wo enden die Verantwortlichkeiten von Service Operation, wo beginnen die von Service Transition?

## Verwandt

- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - ITIL V3 Practice - Request Fulfillment]]
- [[SM - ITIL V3 Practice - Access Management]]
- [[SM - ITIL V3 Practice - Incident Management]]
- [[SM - ITIL V3 Practice - Event Management]]
- [[SM - ITIL V3 Practice - Problem Management]]
- [[SM - ITIL Practice - Incident Management]] *(ITIL 4 Pendant)*

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 38–44; Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing, 2008)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
