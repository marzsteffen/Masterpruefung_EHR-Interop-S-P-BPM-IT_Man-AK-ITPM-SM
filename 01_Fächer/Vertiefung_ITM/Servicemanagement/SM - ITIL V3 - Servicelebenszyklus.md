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

# SM - ITIL V3 - Servicelebenszyklus

> [!info] Kurzdefinition
> Der ITIL-V3-Servicelebenszyklus besteht aus fünf Phasen, die kreisförmig angeordnet sind: Service Strategy (im Zentrum), Service Design, Service Transition, Service Operation, Continual Service Improvement (CSI, als Außenring). Jeder Phase sind spezifische Prozesse zugeordnet.

## Beschreibung

Folie 32 (und 39, 148) zeigt das ITIL-V3-Lebenszyklusdiagramm. Die Darstellung ist „nicht vollständig" (Hinweis auf der Folie) — sie listet ausgewählte Prozesse pro Phase. Im Zentrum steht **Service Strategy**, daran angedockt sind **Service Design** (links), **Service Transition** (rechts) und **Service Operation** (oben). Den Außenring bildet **Continual Service Improvement** mit dem **Seven-Step Improvement Process** als Hauptmethode.

Im Foliensatz dargestellte Prozesse pro Phase (laut Folie 32, ausgewählte):

- **Service Strategy:** Strategy Management for IT-Services, Service Portfolio Management, Financial Management, Demand Management, Business Relationship Management
- **Service Design:** Service Level Management, Supplier Management, Service Catalogue Management, Availability Management, Information Security Management, Capacity Management
- **Service Transition:** Change Management, Release and Deployment Management, Service Validation and Testing, Access Management, Knowledge Management
- **Service Operation:** Event Management, Incident Management, Request Fulfillment, Problem Management, Access Management
- **Continual Service Improvement:** Seven-Step Improvement Process

Die Auflistung ist nicht vollständig — ITIL V3 enthält insgesamt deutlich mehr Prozesse pro Phase. Die Folie ist als Übersicht zu verstehen, nicht als Referenz.

## Bestandteile / Aufbau

| Phase | Position im Diagramm | Auswahl der Prozesse |
|---|---|---|
| Service Strategy | Zentrum | Strategy Management, Service Portfolio Management, Financial Management, Demand Management, Business Relationship Management |
| Service Design | Links | Service Level Management, Supplier Management, Service Catalogue Management, Availability Management, Information Security Management, Capacity Management |
| Service Transition | Rechts | Change Management, Release and Deployment Management, Service Validation and Testing, Access Management, Knowledge Management |
| Service Operation | Oben | Event Management, Incident Management, Request Fulfillment, Problem Management, Access Management |
| Continual Service Improvement | Außenring | Seven-Step Improvement Process |

**Hinweis:** Access Management taucht doppelt auf (Service Transition und Service Operation) — *im Foliensatz nicht weiter erläutert*. In der Praxis ist Access Management organisatorisch oft an beiden Phasen beteiligt: Setup während Transition, Tagesgeschäft während Operation.

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Aus Service-Sicht: Ein neuer KIS-Modul-Service durchläuft den Lebenszyklus — Strategy klärt Zielsetzung, Design legt SLAs fest, Transition rollt aus, Operation betreibt, CSI verbessert kontinuierlich.

## Abgrenzung

- **ITIL V3 Lifecycle vs. ITIL 4 SVS** (siehe [[SM - ITIL 4 - Service Value System]]): V3-Lifecycle ist starr, prozessorientiert, sequenziell-zyklisch. ITIL 4 ersetzt das durch das Service Value System mit Service-Wertschöpfungskette, die nicht-lineare Wertströme erlaubt.
- **Service Operation vs. Service Transition**: Operation ist der laufende Betrieb (täglich); Transition ist die Überführung neuer/geänderter Services in den Betrieb (projektförmig). Schnittstelle: Change Management (Transition) → Incident Management (Operation), wenn ein Change Probleme verursacht.
- **CSI als Phase oder Klammer?** — Im V3-Diagramm ist CSI der Außenring, also eine *Klammer* um alle anderen Phasen. ITIL 4 baut diesen Gedanken aus zur Continual-Improvement-Komponente des SVS (siehe [[SM - ITIL Continual Improvement - Modell]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche fünf Phasen umfasst der ITIL-V3-Servicelebenszyklus? — Service Strategy, Service Design, Service Transition, Service Operation, Continual Service Improvement.

**Anwendungsfrage:** Ordnen Sie folgende Aktivitäten den V3-Phasen zu: SLA-Verhandlung, Incident-Bearbeitung, Service-Idee-Bewertung, Change-Genehmigung, Verbesserungsmaßnahme. — SLA-Verhandlung: Service Design (SLM); Incident: Service Operation; Service-Idee: Service Strategy (Service Portfolio); Change-Genehmigung: Service Transition (Change Management); Verbesserung: CSI (Seven-Step).

**Diskussionsfrage:** Warum hat ITIL 4 den V3-Lifecycle ersetzt? — V3 wurde als zu starr, prozessorientiert und unverträglich mit Agil/DevOps kritisiert (siehe [[SM - ITIL - Überblick]]). ITIL 4 ersetzt sequenzielle Phasen durch flexible Wertströme.

**Mögliche Anschlussfragen:**
- Wie verhält sich V3 zu V4? Welche Konzepte aus V3 leben in V4 weiter?
- Was ist der „Seven-Step Improvement Process"? *(im Foliensatz nicht weiter ausgeführt — Hinweis: 7-stufiger Prozess zur Verbesserung)*
- Warum kommt Access Management in zwei Phasen vor?
- Welche V3-Prozesse haben in ITIL 4 ein direktes Pendant unter den 34 Practices?

## Verwandt

- [[SM - ITIL - Überblick]]
- [[SM - ITIL V3 - Service Operation]]
- [[SM - ITIL 4 - Service Value System]]
- [[SM - CMMI - Reifegradmodell]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - ITIL 4 - Management Practices Übersicht]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 32, 39, 148; „Eigendarstellung nach ITIL Foundation. Darstellung nicht vollständig!"

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
