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

# SM - ITIL Practice - Incident Management

> [!info] Kurzdefinition
> ITIL-4-Practice (Service Management) zum Minimieren der negativen Auswirkungen von Incidents durch schnellstmögliche Wiederherstellung des normalen Servicebetriebs. Ein Incident ist eine nicht geplante Unterbrechung eines Services oder eine Qualitätsminderung eines Services.

## Beschreibung

Folien 89–92 beschreiben die Practice. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

**Zweck (Folie 89):**
> „Das Minimieren der negativen Auswirkung von Incidents, indem der normale Servicebetrieb schnellstmöglich wiederhergestellt wird."

**Definition Incident:**
> „Eine nicht geplante Unterbrechung eines Services oder eine Qualitätsminderung eines Service."

**Incident Management Prozess (Folie 90):**
- Es sollte einen formellen Prozess zum Protokollieren und Verwalten von Incidents geben.
- Dieser Prozess enthält in der Regel keine detaillierten Verfahrensanweisungen zur Diagnose, Untersuchung und Behebung von Incidents, kann jedoch Techniken bereitstellen, um Untersuchungen und Diagnosen effizienter zu gestalten.
- Während des Erstkontakts können Skripts zum Sammeln von Informationen von Benutzern vorhanden sein, die direkt zur Diagnose und Lösung einfacher Incidents führen können.
- Die Untersuchung komplizierterer Incidents erfordert häufig Wissen und Sachverstand und keine Verfahrensschritte.
- In der Regel gibt es separate Prozesse zum Managen von Major Incidents und von Incidents im Bereich der Informationssicherheit.

**Wer kann Incidents lösen? (Folie 91):**
- Manche Incidents werden von den Anwendern selbst unter Verwendung der Selbsthilfe gelöst — die Verwendung bestimmter Selbsthilfe-Records sollte erfasst werden, um sie bei Mess- und Verbesserungsaktivitäten zu nutzen.
- Service Desk gelöst.
- Komplexere Incidents werden in der Regel zur Lösung an ein Support-Team eskaliert. Normalerweise basiert die Weiterleitung auf der Incident-Kategorie, die es erleichtern sollte, das richtige Team zu ermitteln.
- Incidents können an Lieferanten oder Partner eskaliert werden, die Support für die von ihnen gelieferten Produkte und Services bieten.
- Besonders komplexe Incidents und alle Major Incidents erfordern es oft, dass ein temporäres Team gemeinsam an der Ermittlung der Lösung arbeitet. Dieses Team kann Vertreter vieler Stakeholder umfassen, z. B. den Service Provider, Lieferanten, Anwender usw.
- In gravierenden Fällen können zur Lösung eines Incidents Notfallwiederherstellungspläne eingeleitet werden.

**Auswirkungen auf das Business (Folie 92):**
- Das Incident Management kann erhebliche Auswirkungen auf die Kunden- und Anwenderzufriedenheit haben und darauf, wie Kunden und Anwender den Service Provider wahrnehmen.
- Jeder Incident sollte erfasst und gemanagt werden, um sicherzustellen, dass er innerhalb eines Zeitfensters gelöst wird, und dass die Erwartungen des Kunden und Anwenders erfüllt werden.
- Ziellösungszeiten werden vereinbart, dokumentiert und kommuniziert, um sicherzustellen, dass die Erwartungen realistisch sind.
- Incidents werden auf Basis einer vereinbarten Klassifizierung priorisiert, um sicherzustellen, dass Incidents mit den höchsten geschäftlichen Auswirkungen zuerst gelöst werden.

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Zweck | Negative Auswirkung minimieren, Wiederherstellung |
| Definition Incident | Nicht geplante Unterbrechung oder Qualitätsminderung |
| Prozess-Charakter | Formaler Prozess für Protokollierung/Verwaltung; keine starren Diagnose-Anweisungen |
| Lösungs-Hierarchie | Selbsthilfe → Service Desk → Support-Team → Lieferanten/Partner → temporäres Team |
| Major Incidents | Eigener Prozess, ggf. temporäres Team mit allen Stakeholdern |
| Informationssicherheits-Incidents | Eigener Prozess |
| Priorisierung | Basierend auf vereinbarter Klassifizierung; höchste geschäftliche Auswirkung zuerst |
| Ziellösungszeit | Vereinbart, dokumentiert, kommuniziert |

## Beispiel

KIS-Lock im OP-Bereich (kritisch):
- Anwender meldet via Service Desk → Klassifikation „KIS – Performance" → Priorität „kritisch".
- 1st Level: Service Desk versucht, anhand Skript zu klären — keine schnelle Lösung.
- Eskalation an DB-Spezialisten (2nd Level), basierend auf Kategorie.
- Bei Major Incident: temporäres Team (DB-Spezialist, Pflegeleitung als User-Vertreter, Hersteller-Support).
- Lösung, Wiederherstellung, Abschluss.

## Abgrenzung

- **Incident Management vs. Problem Management** ([[SM - ITIL Practice - Problem Management]]): Incident = aktueller Vorfall, Wiederherstellung; Problem = Ursache, Analyse + dauerhafte Lösung.
- **Incident vs. Service Request** ([[SM - ITIL Practice - Service Request Management]]): Incident = nicht geplante Unterbrechung; Service Request = vereinbarter Standard-Service.
- **Incident vs. Major Incident**: Major Incident hat besonders hohe Auswirkung — eigener Prozess.
- **vs. Informationssicherheits-Incident**: Eigener Prozess, mit zusätzlichen Compliance- und Forensik-Anforderungen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Zweck der Incident Management Practice? — Negative Auswirkung minimieren, normalen Servicebetrieb schnellstmöglich wiederherstellen.

**Definition Incident:** Nicht geplante Unterbrechung oder Qualitätsminderung eines Services.

**Diskussionsfrage:** Warum gibt es separate Prozesse für Major Incidents und Informationssicherheits-Incidents? — Major Incident: höhere Eskalationsstufe, mehr Stakeholder, mehr Kommunikation. Informationssicherheits-Incidents: Compliance (Meldepflichten), Forensik, Vertraulichkeit.

**Mögliche Anschlussfragen:**
- Wer kann Incidents lösen? — Anwender (Selbsthilfe), Service Desk, Support-Team, Lieferanten/Partner, temporäres Team.
- Welche Rolle hat Klassifizierung in der Priorisierung?
- Wie kann KI Incident Management verbessern? — Siehe [[SM - Fallstudie - KI Incident Management]].
- Welche Auswirkungen hat Incident Management auf die Kundenwahrnehmung?

## Verwandt

- [[SM - ITIL Practice - Problem Management]]
- [[SM - ITIL Practice - Service Desk]]
- [[SM - ITIL Practice - Service Request Management]]
- [[SM - ITIL Practice - Monitoring and Event Management]]
- [[SM - ITIL V3 Practice - Incident Management]]
- [[SM - Fallstudie - KI Incident Management]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 89–92; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
