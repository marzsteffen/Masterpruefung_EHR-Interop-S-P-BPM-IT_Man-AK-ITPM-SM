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

# SM - ITIL V3 Practice - Request Fulfillment

> [!info] Kurzdefinition
> Request Fulfillment ist der ITIL-V3-Prozess, der die Anforderung von Standard-Services bearbeitet und Kunden mit Informationen über die Verfügbarkeit von Services und das Verfahren zu deren Erhalt versorgt.

## Beschreibung

Folie 40 zeigt Ziele und Ablauf:

**Ziele:**
- Anforderung von Standard-Services
- Kunden mit Informationen über die Verfügbarkeit von Services und dem Verfahren, wie diese zu erhalten sind, versorgen

**Ablauf (4 Schritte):**
1. Menüauswahl
2. Finanzielle Genehmigung
3. Erfüllung
4. Abschluss

Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008).

In ITIL 4 wird dieser Prozess als **Service Request Management** geführt (siehe [[SM - ITIL Practice - Service Request Management]]), inhaltlich ähnlich aber prinzipieller im SVS verankert.

## Bestandteile / Aufbau

| Schritt | Inhalt |
|---|---|
| Menüauswahl | Anwender wählt aus Service-Katalog/Self-Service-Portal aus |
| Finanzielle Genehmigung | Falls nötig, Genehmigung durch Vorgesetzten/Budget-Verantwortlichen |
| Erfüllung | Service wird bereitgestellt (z. B. Account angelegt, Hardware geliefert) |
| Abschluss | Bestätigung an Anwender, Ticket geschlossen |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Krankenhaus-Beispiele:
- Antrag auf KIS-Zugriff für neuen Mitarbeiter (Menüauswahl im Self-Service-Portal → Genehmigung Stationsleitung → Account-Anlage durch IT → E-Mail-Bestätigung).
- Bestellung eines neuen Laptops für eine Pflegekraft.
- Anforderung eines neuen Drucker-Toners für die Station.

## Abgrenzung

- **Request Fulfillment vs. Incident Management** (siehe [[SM - ITIL V3 Practice - Incident Management]]): Request = vereinbarter Standard-Service, kein Defekt; Incident = ungeplante Unterbrechung oder Qualitätsminderung.
- **Request Fulfillment vs. Change Management**: Standard-Changes laufen über Request Fulfillment; größere Changes über Change Management.
- **V3 Request Fulfillment vs. ITIL 4 Service Request Management** (siehe [[SM - ITIL Practice - Service Request Management]]): Inhaltlich nahezu identisch, in ITIL 4 in das SVS eingebettet.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Request Fulfillment? — V3-Prozess zur Bearbeitung von Standard-Service-Anfragen.

**Anwendungsfrage:** Welche Schritte durchläuft ein Standard-Service-Request (z. B. Account-Anlage)? — Menüauswahl → finanzielle Genehmigung → Erfüllung → Abschluss.

**Diskussionsfrage:** Welche Standardisierung muss vorausgehen, damit Request Fulfillment effizient ist? — Servicekatalog mit klar definierten, atomaren Standard-Services und automatisierten Workflows. Ohne Katalog wird jeder Request individuell bearbeitet — ineffizient.

**Mögliche Anschlussfragen:**
- Wie hängt Request Fulfillment mit dem Servicekatalog zusammen?
- Welche Beispiele für Service Requests nennt ITIL 4 (siehe [[SM - ITIL Practice - Service Request Management]])? — Servicebereitstellung, Information, Ressourcen-Anfrage, Zugriff, Feedback.
- Warum trennt ITIL Standard-Requests von Incidents?

## Verwandt

- [[SM - ITIL V3 - Service Operation]]
- [[SM - ITIL Practice - Service Request Management]] *(ITIL 4 Pendant)*
- [[SM - ITIL V3 Practice - Access Management]]
- [[SM - IT-Service-Katalog - Sichten und Strukturierung]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 40; Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
