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

# SM - ITIL V3 Practice - Problem Management

> [!info] Kurzdefinition
> Problem Management analysiert und löst die Ursachen von Incidents und entwickelt proaktive Aktivitäten zur Verhinderung künftiger Incidents. Es gibt einen „Known-Error-Unterprozess", in dem analysierte, aber noch nicht behobene Probleme dokumentiert werden.

## Beschreibung

Folie 44 zeigt Ziele und Ablauf:

**Ziele:**
- Analyse und Auflösung von Ursachen von Incidents
- Entwickelt proaktive Aktivitäten zur Verhinderung von künftigen Incidents
- Dazu gibt es einen „Known-Error-Unterprozess"

**Ablauf (10 Schritte):**
1. Erkennung
2. Dokumentation
3. Klassifizierung
4. Priorisierung
5. Untersuchung/Diagnose
6. Festlegung von Workarounds
7. Identifikation eines Known-Errors
8. Lösung & Abschluss
9. Review von Major Problems
10. Fehlerkorrektur in Entwicklungsumgebung

Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008).

In ITIL 4 läuft Problem Management ähnlich (siehe [[SM - ITIL Practice - Problem Management]]) mit drei klar getrennten Phasen: Problemidentifizierung, Problemsteuerung, Fehlersteuerung — und expliziten Definitionen von Problem, Workaround, Known Error.

## Bestandteile / Aufbau

| Schritt | Inhalt |
|---|---|
| Erkennung | Aus Incident-Trends, Event-Korrelationen, Beobachtungen |
| Dokumentation | Problem-Record anlegen |
| Klassifizierung | Kategorie zuordnen |
| Priorisierung | Risiko/Auswirkung bewerten |
| Untersuchung/Diagnose | Ursachenanalyse |
| Festlegung von Workarounds | Provisorische Lösung dokumentieren |
| Identifikation eines Known-Errors | Bekannter, dokumentierter Fehler ohne dauerhafte Lösung |
| Lösung & Abschluss | Wenn dauerhaft gelöst |
| Review von Major Problems | Lessons Learned bei größeren Problemen |
| Fehlerkorrektur in Entwicklungsumgebung | Korrekturen werden zurück in den Lifecycle gespeist |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Krankenhaus-Beispiel:
- Pflegekräfte berichten in einem Monat dreimal vom KIS-Lock im OP-Bereich (wiederkehrender Incident).
- Problem-Record angelegt, klassifiziert (DB-Locking), priorisiert (hoch wegen OP-Bezug).
- Diagnose: spezifische Abfrage triggert Lock.
- Workaround: Abfrage wird zeitlich begrenzt; Pflegekraft erhält Hinweis.
- Known Error dokumentiert.
- Lösung: DB-Index-Änderung im nächsten Release.
- Lösung dauerhaft, Abschluss.

## Abgrenzung

- **Problem vs. Incident** (siehe [[SM - ITIL V3 Practice - Incident Management]]): Incident = aktueller Vorfall (Wiederherstellung); Problem = Ursache (Analyse + dauerhafte Lösung). Beide sind separate Records.
- **Workaround vs. Lösung**: Workaround = provisorisch (vermindert Auswirkung); Lösung = dauerhaft.
- **Known Error**: Problem mit bekannter Ursache und Workaround, aber noch ohne dauerhafte Lösung.
- **V3 Problem Management vs. ITIL 4 Problem Management** (siehe [[SM - ITIL Practice - Problem Management]]): ITIL 4 strukturiert in drei Phasen (Identifizierung, Steuerung, Fehlersteuerung) und definiert Begriffe expliziter.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist das Ziel von Problem Management? — Ursachen von Incidents analysieren und lösen, künftige Incidents verhindern.

**Anwendungsfrage:** Wann wird ein Incident zum Problem? — Wenn er wiederkehrt oder ein Major Incident Trends zeigt — Problem Management dann als zugeordnete Untersuchung.

**Diskussionsfrage:** Warum braucht es einen Known-Error-Unterprozess? — Damit Workarounds dokumentiert und Service Desk und Anwender bei wiederkehrenden Symptomen schneller reagieren können — auch wenn die dauerhafte Lösung noch fehlt.

**Mögliche Anschlussfragen:**
- Was unterscheidet einen Workaround von einer dauerhaften Lösung?
- Welche Trigger lösen Problem Management aus?
- Welche Schnittstellen hat Problem Management zu Risk Management, Change Enablement, Knowledge Management, Continual Improvement (siehe [[SM - ITIL Practice - Problem Management]])?
- Was ist ein Major Problem?

## Verwandt

- [[SM - ITIL V3 - Service Operation]]
- [[SM - ITIL V3 Practice - Incident Management]]
- [[SM - ITIL Practice - Problem Management]] *(ITIL 4 Pendant)*

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 44; Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
