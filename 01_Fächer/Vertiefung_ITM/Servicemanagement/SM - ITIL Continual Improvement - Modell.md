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

# SM - ITIL Continual Improvement - Modell

> [!info] Kurzdefinition
> Das CSI-Modell (Continual Service Improvement) ist ein iterativer Sechs-Schritte-Zyklus zur kontinuierlichen Service-Verbesserung: 1. Was ist unsere Vision? → 2. Wo stehen wir gerade? → 3. Wo wollen wir hin? → 4. Wie kommen wir dort hin? → 5. Aktiv werden → 6. Sind wir angekommen? → (Klammer: Wie halten wir unsere Services in Schwung?)

## Beschreibung

Folien 107–122 widmen sich Continual Service Improvement.

**Warum CSI?** (Folie 107)
- Geschäftsumfeld und Kundenanforderungen ändern sich ständig — der Serviceprovider muss sich ständig anpassen.
- Technologie ändert sich ständig; ohne Anpassung sind Services schnell veraltet.
- Angebotene Services müssen kontinuierlich auf Verbesserungsmöglichkeiten geprüft und aktualisiert werden, sonst verlieren sie an Wert.

**Methoden und Techniken** (Folie 109): Balanced Scorecard, Lean-Management (zur Reduzierung von Verschwendung), Multi-Phasen-Projekte, Reifegrad-Assessments (siehe [[SM - CMMI - Reifegradmodell]]), DevOps, SWOT (siehe [[SM - SWOT-Analyse]]), Continual Service Improvement Modell, Inkrementelle agile Verbesserung.

**Das CSI-Modell** (Folie 110) hat 6 Hauptschritte plus eine Klammer-Frage:

| Schritt | Frage | Aktivität |
|---|---|---|
| 1 | Was ist unsere Vision? | Business Vision, Mission, Ziele |
| 2 | Wo stehen wir gerade? | Grundlegende Assessments durchführen |
| 3 | Wo wollen wir hin? | Messbare Ziele definieren |
| 4 | Wie kommen wir dort hin? | Verbesserungsplan definieren |
| 5 | Aktiv werden | Verbesserungsaktionen ausführen |
| 6 | Sind wir angekommen? | Metriken und KPIs evaluieren |
| (Klammer) | Wie halten wir unsere Services in Schwung? | Kontinuität sichern |

**Detail je Schritt:**

- **Schritt 1: Was ist unsere Vision?** (Folie 111) — Vision für die Verbesserungsinitiative erstellen. Vision und Ziele der Organisation müssen den Geschäftseinheiten, Abteilungen, Teams und Einzelpersonen bekannt sein. Auf Managementebene muss eine eigene Vision für die geplanten Verbesserungsbedürfnisse entwickelt werden.

- **Schritt 2: Wo stehen wir gerade?** (Folie 112) — Assessment zum aktuellen Stand (Current State Assessment): Bewertung existierender Services, Verstehen der Organisationskultur. Wichtig: Ohne diesen Schritt fehlt die grundlegende Messlinie zur Zielerreichung — *„Startpunkt muss bekannt sein!"*.

- **Schritt 3: Wo wollen wir hin?** (Folien 113–117)
  - Skizzieren des Zielstatus.
  - Verbesserungsmöglichkeiten auf Basis von **GAP-Analyse** identifizieren und priorisieren (Folien 114–115).
  - Verbesserungsziele werden mit kritischen Erfolgsfaktoren (CSFs) und Key Performance Indicators (KPIs) festgelegt.
  - **GAP-Analyse-Beispiel** (Folie 115): Verbesserungspotenzial „Erhöhung Kundenzufriedenheit". Tabelle: Desired State (99 % Zufriedenheit, 3-Tage-Lösungszeit) vs. Current State (Zufriedenheit unbekannt, 6-Tage-Lösungszeit) vs. Action Steps (aktuelle Zufriedenheit erheben, Eskalationsprozess adaptieren, Helpdesk-MA einschulen).
  - **SWOT** wird als Hilfsmethode in Schritt 3 mit Tesla-Beispiel illustriert (Folien 116–117) — siehe [[SM - SWOT-Analyse]].
  - **KPIs:** Auf www.kpilibrary.com findet man eine Fülle praxisgenutzter KPIs (Folie 118).

- **Schritt 4: Wie kommen wir dort hin?** (Folie 119) — Erstellung eines Plans zur Bewältigung der CSI-Herausforderungen. Die einfachste Route ist zu Beginn oft nicht klar; sobald sie klar ist, ist eine iterative Vorgehensweise notwendig. Jede Iteration trägt zu einer ständigen Verbesserung bei. Der CSI-Ansatz muss reevaluiert werden.

- **Schritt 5: Aktiv werden** (Folie 120) — Folgende ITIL-Praktiken sollten für diesen Schritt verstanden und eingesetzt werden: **Change Management, Measurement und Reporting, Risk Management, Continual Improvement.**

- **Schritt 6: Sind wir angekommen?** (Folie 121)
  - Wurden die Ziele erreicht (KPIs)?
  - Sind diese Ziele noch relevant?
  - Change Management.

**Beziehungen zwischen CSI und Grundprinzipien** (Folie 122) — siehe Tabelle in [[SM - ITIL 4 - Sieben Grundprinzipien]].

## Bestandteile / Aufbau

| # | Frage | Aktivität | Hilfsmethoden |
|---|---|---|---|
| 1 | Vision? | Business Vision, Mission, Ziele | — |
| 2 | Ist-Zustand? | Assessments | CMMI, ggf. SWOT |
| 3 | Soll-Zustand? | Messbare Ziele | GAP-Analyse, SWOT, KPIs (kpilibrary.com) |
| 4 | Wie hin? | Plan, iterativ | — |
| 5 | Aktiv werden | Umsetzung | Change Mgmt, Measurement, Risk Mgmt, Continual Improvement |
| 6 | Angekommen? | Evaluierung | KPIs, Change Management |
| Klammer | Schwung halten | Kontinuität | — |

## Beispiel

Krankenhaus-IT, Initiative „Pflegekraft-Zufriedenheit erhöhen" (analog Folie 115):
1. Vision: „Pflegekraft als zufriedener IT-Service-Konsument."
2. Ist: Zufriedenheit unbekannt, Ø Lösungszeit 6 Tage.
3. Soll: 99 % Zufriedenheit, Lösungszeit ≤ 3 Tage.
4. Plan: Eskalationsprozess optimieren, Helpdesk-Schulung, Zufriedenheitsumfrage einführen.
5. Aktion: Maßnahmen umsetzen, Schulungen durchführen, Umfragen starten.
6. Evaluation: KPIs nach 6 Monaten messen.

## Abgrenzung

- **CSI-Modell vs. PDCA / Deming-Zyklus**: Beide sind iterative Verbesserungsmodelle; CSI ist ITIL-spezifisch und expliziter (6+1 Schritte mit klaren Fragen).
- **CSI-Modell vs. Continual Improvement Practice**: Continual Improvement ist eine General Management Practice in ITIL 4; CSI-Modell ist die methodische Vorlage, mit der die Practice umgesetzt werden kann. CSI ist auch eine Phase im V3-Lifecycle.
- **CSI-Modell vs. CMMI** (siehe [[SM - CMMI - Reifegradmodell]]): CMMI bewertet Prozessreife; CSI verbessert sie. CMMI ist eine Hilfsmethode in CSI Schritt 2.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche 6+1 Schritte umfasst das CSI-Modell? — Vision → Ist → Soll → Plan → Aktion → Evaluation → (Schwung halten).

**Anwendungsfrage:** Wenden Sie das CSI-Modell auf eine konkrete Verbesserungsinitiative an (z. B. „mobile KIS-Nutzung beschleunigen").

**Diskussionsfrage:** Warum ist Schritt 2 („Wo stehen wir?") so kritisch? — Ohne Startpunkt keine Messung der Zielerreichung; CSI ohne Ist-Analyse arbeitet im Blindflug.

**Mögliche Anschlussfragen:**
- Welche Methoden unterstützen CSI? — Balanced Scorecard, Lean, Reifegrad-Assessments, DevOps, SWOT, GAP-Analyse, agile Verbesserung.
- Welche Beziehung haben die Grundprinzipien zu den CSI-Schritten (siehe Tabelle Folie 122)?
- Welche ITIL-Practices werden in Schritt 5 explizit genannt? — Change Management, Measurement and Reporting, Risk Management, Continual Improvement.
- Was ist eine GAP-Analyse?

## Verwandt

- [[SM - ITIL 4 - Service Value System]]
- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - SWOT-Analyse]]
- [[SM - CMMI - Reifegradmodell]]
- [[SM - 5 Phasen - serviceorientierte IT-Organisation]]
- [[SM - ITIL V3 - Servicelebenszyklus]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 107–122

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
