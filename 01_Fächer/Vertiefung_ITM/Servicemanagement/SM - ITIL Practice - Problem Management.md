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

# SM - ITIL Practice - Problem Management

> [!info] Kurzdefinition
> ITIL-4-Practice (Service Management) zum Reduzieren der Eintrittswahrscheinlichkeit und der Auswirkungen von Incidents durch Identifizierung tatsächlicher und potenzieller Ursachen und Management von Workarounds und Known Errors. Drei Phasen: Problemidentifizierung, Problemsteuerung, Fehlersteuerung.

## Beschreibung

Folien 93–99 vertiefen die Practice. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

**Zweck (Folie 93):**
> „Das Reduzieren der Eintrittswahrscheinlichkeit und der Auswirkungen von Incidents durch die Identifizierung tatsächlicher und potenzieller Ursachen von Incidents und das Management von Workarounds und Known Errors."

**Definitionen (Folie 93):**

- **Problem:** „Eine Ursache oder mögliche Ursache eines oder mehrerer Incidents."
- **Workaround:** „Eine Lösung, die die Auswirkungen von Incidents oder Problemen reduziert oder beseitigt, für die noch keine vollständige Lösung verfügbar ist. Einige Workarounds verringern die Wahrscheinlichkeit des Auftretens von Incidents."
- **Known Error:** „Ein Problem, das analysiert, aber noch nicht gelöst wurde."

**Problem vs. Incident (Folie 94):**
- Incidents wirken sich auf Anwender oder Geschäftsprozesse aus und müssen behoben werden, damit der normale Geschäftsbetrieb laufen kann.
- Probleme sind die Ursachen von Incidents. Sie erfordern eine Untersuchung und Analyse, um die Ursachen zu ermitteln, Workarounds zu entwickeln und eine längerfristige Lösung zu empfehlen. Dies reduziert die Anzahl und die Auswirkungen künftiger Incidents.

**Drei Phasen des Problem Managements (Folien 95–98):**

### Phase 1: Problemidentifizierung (Folie 96)
- Durchführen einer Trendanalyse von Incident Records
- Erkennung doppelter und wiederkehrender Schwierigkeiten durch Anwender, Service Desk und Mitarbeiter des technischen Supports
- Während eines Major Incidents: Risiken entdecken, die dazu führen, dass ein Incident erneut auftreten könnte
- Analyse der von Lieferanten und Partnern erhaltenen Informationen
- Analyse der von internen Softwareentwicklern, Test- und Projektteams erhaltenen Informationen
- Andere Informationsquellen können auch zur Identifizierung von Problems führen

### Phase 2: Problemsteuerung – Aktivitäten „Problem Control" (Folie 97)
- **Problemanalyse**
  - Probleme werden für die Analyse auf Basis des Risikos priorisiert, das sie darstellen, und werden auf Basis der möglichen Auswirkungen und Wahrscheinlichkeit als Risiken gemanagt
  - Es ist nicht erforderlich, jedes Problem zu analysieren; es kann sinnvoller sein, Probleme mit höchster Priorität zunächst zu klären
- Dokumentieren von Workarounds
- Dokumentieren von Known Errors

### Phase 3: Fehlersteuerung – Aktivitäten „Error Control" (Folie 98)
- Im Rahmen der Fehlersteuerung werden Known Errors gemanagt — Probleme, bei denen die anfängliche Analyse abgeschlossen wurde und fehlerhafte Komponenten bereits identifiziert wurden.
- Fehlersteuerung umfasst auch die Identifizierung möglicher dauerhafter Lösungen, die zu einem Change Request für die Implementierung einer Lösung führen können — aber nur, wenn dieser im Hinblick auf Kosten, Risiken und Nutzen gerechtfertigt ist.
- Fehlersteuerung bewertet den Status von Known Errors, die nicht behoben wurden, regelmäßig neu. Dazu zählen die allgemeinen Auswirkungen auf Kunden, Verfügbarkeit und Kosten dauerhafter Lösungen sowie die Effektivität von Workarounds. Die Effektivität von Workarounds sollte jedes Mal bewertet werden, wenn ein Workaround verwendet wird, da der Workaround basierend auf der Bewertung möglicherweise verbessert werden kann.

**Schnittstellen mit anderen Practices (Folie 99):**

Beispiele für Schnittstellen zwischen:
- Problem Management
- Risk Management
- Change Enablement
- Knowledge Management
- Continual Improvement

> „Problemmanagementaktivitäten können als konkreter Fall von Risk Management organisiert werden. Die Implementierung der Problemlösung erfolgt oft außerhalb des Bereichs des Problem Managements. Der Output der Problem Management Practice umfasst Informationen und Dokumentationen zu Workarounds und Known Errors. Aktivitäten des Problem Managements können Verbesserungsmöglichkeiten in allen vier Dimensionen des Service Managements identifizieren."

## Bestandteile / Aufbau

| Phase | Aktivitäten |
|---|---|
| Problemidentifizierung | Trendanalysen, Erkennung Wiederholungsmuster, Major-Incident-Risiken, Lieferanten-/Partner-/Entwicklungs-Inputs |
| Problemsteuerung (Problem Control) | Problemanalyse (priorisiert), Workarounds dokumentieren, Known Errors dokumentieren |
| Fehlersteuerung (Error Control) | Known Errors managen, dauerhafte Lösungen identifizieren (ggf. Change Request), Status regelmäßig neu bewerten |

## Beispiel

Krankenhaus: Wiederkehrende KIS-Locks (3× im Monat im OP-Bereich) → Problem-Identifizierung über Trendanalyse → Analyse: spezifischer DB-Index fehlt → Workaround dokumentiert (Abfrage-Limit) → Known Error angelegt → Fehlersteuerung: Change Request für DB-Index → Lösung im nächsten Release.

## Abgrenzung

- **Problem vs. Incident** (siehe [[SM - ITIL Practice - Incident Management]]): Incident = Vorfall, Wiederherstellung; Problem = Ursache, Analyse.
- **Workaround vs. dauerhafte Lösung**: Workaround = provisorisch; Lösung = endgültig.
- **Known Error vs. Problem**: Known Error = Problem mit abgeschlossener Erstanalyse, fehlerhafte Komponenten identifiziert.
- **Problem Management vs. Risk Management**: Problemmanagement-Aktivitäten können als konkreter Fall von Risk Management organisiert werden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Zweck von Problem Management? — Eintrittswahrscheinlichkeit und Auswirkungen von Incidents reduzieren, Ursachen identifizieren, Workarounds und Known Errors managen.

**Definitionen:** Problem (Ursache von Incidents), Workaround (Auswirkungs-Reduzierung ohne Lösung), Known Error (analysiert, nicht gelöst).

**Welche 3 Phasen?** Problemidentifizierung, Problemsteuerung (Problem Control), Fehlersteuerung (Error Control).

**Diskussionsfrage:** Warum muss nicht jedes Problem analysiert werden? — Priorisierung nach Risiko/Auswirkung; ressourcenökonomisch.

**Mögliche Anschlussfragen:**
- Welche Schnittstellen hat Problem Management zu anderen Practices? — Risk, Change Enablement, Knowledge, CSI.
- Wie unterscheidet sich „Workaround verbessern" von „dauerhaft lösen"?
- Wie hängt Problem Management mit den Vier Dimensionen zusammen? — Aktivitäten können Verbesserungsmöglichkeiten in allen vier Dimensionen identifizieren.

## Verwandt

- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL Practice - Change Enablement]]
- [[SM - ITIL V3 Practice - Problem Management]]
- [[SM - ITIL Continual Improvement - Modell]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 93–99; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
