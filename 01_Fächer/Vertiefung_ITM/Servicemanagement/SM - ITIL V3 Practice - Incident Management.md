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

# SM - ITIL V3 Practice - Incident Management

> [!info] Kurzdefinition
> Incident Management stellt nach einem Service-Ausfall den normalen Betrieb so schnell wie möglich wieder her. Incidents können Ausfälle, Fragen oder Erkundigungen sein. Der Ablauf gliedert sich in neun Schritte von der Identifizierung bis zum Abschluss.

## Beschreibung

Folie 42 zeigt Ziele und Ablauf:

**Ziele:**
- Wiederherstellung der Services bei Ausfällen
- Incidents können Ausfälle, Fragen oder Erkundigungen sein

**Ablauf (9 Schritte):**
1. Identifizierung
2. Aufzeichnung/Dokumentation
3. Klassifizierung
4. Priorisierung
5. Erste Diagnose
6. Eskalation
7. Untersuchung und endgültige Diagnose
8. Lösung und Wiederherstellung
9. Abschluss

Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008).

In ITIL 4 läuft Incident Management ähnlich ab — siehe [[SM - ITIL Practice - Incident Management]] mit den ITIL-4-Definitionen.

## Bestandteile / Aufbau

| Schritt | Inhalt |
|---|---|
| Identifizierung | Erkennen, dass ein Incident vorliegt (Anwendermeldung, Monitoring) |
| Aufzeichnung/Dokumentation | Ticket eröffnen, Daten erfassen |
| Klassifizierung | Kategorie zuordnen (z. B. Hardware/Software/Network) |
| Priorisierung | Geschäftliche Auswirkung × Dringlichkeit |
| Erste Diagnose | Erste Hypothese, ggf. Lösung am 1st Level |
| Eskalation | Funktional (an Specialist) oder hierarchisch (an Management) |
| Untersuchung und endgültige Diagnose | Tiefer-Analyse |
| Lösung und Wiederherstellung | Service wieder verfügbar machen |
| Abschluss | Ticket schließen, Lessons Learned |

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Krankenhaus-Beispiel:
- Pflegekraft meldet KIS-Ausfall am OP-Bereich.
- Ticket-Erfassung im IT-Tool, Kategorie „KIS – Performance"; Priorität „kritisch" (OP-Bereich, Patient ggf. gefährdet).
- 1st-Level-Diagnose: Server reagiert langsam.
- Eskalation an 2nd Level (DB-Spezialist).
- Diagnose: DB-Lock; Lösung: DB-Neustart.
- Service wiederhergestellt, Pflegekraft bestätigt, Ticket geschlossen.

## Abgrenzung

- **Incident vs. Problem** (siehe [[SM - ITIL V3 Practice - Problem Management]]): Incident = aktueller Vorfall, Wiederherstellung steht im Vordergrund; Problem = Ursache mehrerer Incidents, Ursachenanalyse steht im Vordergrund.
- **Incident vs. Service Request** (siehe [[SM - ITIL V3 Practice - Request Fulfillment]]): Incident = ungeplante Unterbrechung; Request = vereinbarter Standard-Service.
- **Incident vs. Event** (siehe [[SM - ITIL V3 Practice - Event Management]]): Event = Ereignis (auch unkritisch); Incident = ungeplante Unterbrechung. Events können Incidents auslösen.
- **V3 Incident Management vs. ITIL 4 Incident Management** (siehe [[SM - ITIL Practice - Incident Management]]): ITIL 4 hat ähnliche Logik, aber in ITIL 4 wird der Prozess weniger streng vorgegeben; mehr Flexibilität in der Praxis-Umsetzung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist das Ziel von Incident Management? — Wiederherstellung des normalen Servicebetriebs nach einem Ausfall, möglichst schnell.

**Anwendungsfrage:** Skizzieren Sie den Incident-Management-Ablauf für einen konkreten Vorfall. Wo sind die kritischen Übergänge? — Übergang 1st → 2nd Level (Eskalation), Übergang Lösung → Abschluss (Bestätigung durch Anwender).

**Diskussionsfrage:** Wie unterscheiden sich Klassifizierung und Priorisierung? — Klassifizierung = welche Kategorie (was)?; Priorisierung = wie dringend (wann lösen)? — beide sind unabhängig.

**Mögliche Anschlussfragen:**
- Wie hängt Incident Management mit Problem Management zusammen?
- Was ist ein Major Incident? *(im V3-Foliensatz nicht detailliert; in ITIL 4 explizit als Sonderfall)*
- Welche Rolle hat Eskalation in der Wiederherstellungsstrategie?
- Wie wird KI im Incident Management eingesetzt? — Siehe [[SM - Fallstudie - KI Incident Management]].

## Verwandt

- [[SM - ITIL V3 - Service Operation]]
- [[SM - ITIL V3 Practice - Problem Management]]
- [[SM - ITIL V3 Practice - Event Management]]
- [[SM - ITIL Practice - Incident Management]] *(ITIL 4 Pendant)*
- [[SM - Fallstudie - KI Incident Management]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 42; Quelle: *Service Operation: Eine Management Guide* (Van Haren Publishing 2008)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
