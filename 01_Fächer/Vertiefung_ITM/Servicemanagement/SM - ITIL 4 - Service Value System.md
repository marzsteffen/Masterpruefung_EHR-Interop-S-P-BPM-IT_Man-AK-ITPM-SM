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

# SM - ITIL 4 - Service Value System

> [!info] Kurzdefinition
> Das ITIL Service Value System (SVS) beschreibt, wie alle Komponenten und Aktivitäten einer Organisation systematisch zusammenwirken, um Wertschöpfung zu ermöglichen. Es nimmt Inputs (Opportunity/Demand) auf und liefert Outputs (Ziele und Wert) — gesteuert durch fünf zentrale Komponenten: Grundprinzipien, Governance, Service-Wertschöpfungskette, Practices und Continual Improvement.

## Beschreibung

Das SVS ist der zentrale Strukturrahmen von ITIL 4 und ersetzt den linearen V3-Lebenszyklus. Folien 52–56 zeigen das SVS-Diagramm mit Inputs, Komponenten und Outputs.

**Inputs:**
- **Opportunity** (Möglichkeit): Optionen, die das Unternehmen zur Wertschöpfung nutzen kann
- **Demand** (Nachfrage): konkrete Anforderungen aus dem Geschäft

**Komponenten** (innerhalb des Systems):
- Grundprinzipien (siehe [[SM - ITIL 4 - Sieben Grundprinzipien]])
- Governance (siehe [[SM - Governance - Definition]])
- Service-Wertschöpfungskette (siehe [[SM - ITIL 4 - Service-Wertschöpfungskette]])
- Practices (siehe [[SM - ITIL 4 - Management Practices Übersicht]])
- Continual Improvement (kontinuierliche Verbesserung — siehe [[SM - ITIL Continual Improvement - Modell]])

**Outputs:**
- Ziele und Wert erreichen

Folie 53 ergänzt den Zweck des SVS:
- Sicherstellen, dass die Organisation gemeinsam mit allen Stakeholdern durch die Verwendung und das Management von Produkten und Services fortlaufend gemeinsamen Wert schafft.
- Das ITIL-SVS beschreibt, wie alle Komponenten und Aktivitäten der Organisation systematisch zusammenwirken, um Wertschöpfung zu ermöglichen.

Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Bestandteile / Aufbau

| Komponente | Beschreibung (laut Folie 54–56) |
|---|---|
| **Grundprinzipien** | Empfehlungen, die eine Organisation unter allen Umständen leiten können, ungeachtet von Änderungen in ihren Zielen, Strategien, Arbeitsweisen oder Führungsstrukturen. |
| **Governance** | Die Mittel, mit denen eine Organisation geführt und gesteuert wird. |
| **Service-Wertschöpfungskette** | Eine Reihe miteinander verbundener Aktivitäten, die ein Unternehmen ausführt, um seinen Kunden ein Produkt oder ein Service von Wert zu liefern und die Wertrealisierung zu erleichtern. |
| **Practices** | Eine Reihe von Organisationsressourcen, die zur Durchführung von Aufgaben oder zur Erreichung eines Ziels bestimmt sind. |
| **Continual Improvement** | Eine wiederkehrende organisatorische Aktivität, die auf allen Ebenen durchgeführt wird, um sicherzustellen, dass die Leistung einer Organisation stets den Erwartungen der Stakeholder entspricht. |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Aus Krankenhaus-IT-Sicht: Ein Pflegekraft-Bedarf nach mobilem KIS-Zugang (Demand) trifft auf die Möglichkeit (Opportunity), Tablets einzuführen. Im SVS wird dies durch Governance gerahmt (Datenschutz, Sicherheitsrichtlinien), durch die Wertschöpfungskette (Engagement → Design+Transition → Erhalten/Erstellen → Bereitstellung+Support) realisiert, durch Practices (Service Configuration Management, Information Security, Incident Management) operational unterstützt und im CSI iterativ verbessert. Output: produktive Tablet-Lösung mit messbarem Mehrwert.

## Abgrenzung

- **SVS vs. ITIL-V3-Lifecycle** (siehe [[SM - ITIL V3 - Servicelebenszyklus]]): V3 ist sequenziell-zyklisch (5 Phasen); SVS ist nicht-linear, mit der Service-Wertschöpfungskette als zentralem Element. SVS ist flexibler und besser kompatibel mit Agil/DevOps.
- **SVS vs. Vier Dimensionen** (siehe [[SM - ITIL 4 - Four Dimensions]]): SVS beschreibt die Funktionsweise; die Vier Dimensionen sind die Designperspektiven, aus denen alle Komponenten betrachtet werden müssen.
- **SVS vs. Service Value Chain**: Die Service-Wertschöpfungskette ist das *zentrale Element* des SVS, aber nur eine seiner fünf Komponenten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist das ITIL Service Value System? — System, das Inputs (Opportunity/Demand) systematisch in Outputs (Ziele und Wert) umwandelt — durch Grundprinzipien, Governance, Wertschöpfungskette, Practices und Continual Improvement.

**Anwendungsfrage:** Skizzieren Sie das SVS und ordnen Sie konkrete Aktivitäten der Krankenhaus-IT den fünf Komponenten zu.

**Diskussionsfrage:** Warum ersetzt ITIL 4 den V3-Lifecycle durch das SVS? — V3 wurde als zu starr kritisiert; SVS erlaubt nicht-lineare Wertströme, ist agil-kompatibel und betont Zusammenwirken statt Sequenzierung.

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen Grundprinzipien und Practices?
- Welche Rolle hat Governance im SVS?
- Wie ist Continual Improvement im SVS verankert? — Als eigene Komponente *und* als organisatorische Aktivität auf allen Ebenen.
- Was sind Inputs und Outputs des SVS?
- Welche Verbindung gibt es zur Service-Wertschöpfungskette ([[SM - ITIL 4 - Service-Wertschöpfungskette]])?

## Verwandt

- [[SM - ITIL 4 - Wertstrom Definition]]
- [[SM - ITIL 4 - Organisatorische Agilität und Resilienz]]
- [[SM - ITIL 4 - Four Dimensions]]
- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 - Service-Wertschöpfungskette]]
- [[SM - ITIL 4 - Management Practices Übersicht]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - Governance - Definition]]
- [[SM - ITIL - Überblick]]
- [[SM - ITIL V3 - Servicelebenszyklus]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 50, 52–56; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
