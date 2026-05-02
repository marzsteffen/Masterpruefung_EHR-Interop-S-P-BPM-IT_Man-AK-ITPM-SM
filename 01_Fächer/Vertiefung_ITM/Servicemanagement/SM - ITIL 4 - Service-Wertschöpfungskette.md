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

# SM - ITIL 4 - Service-Wertschöpfungskette

> [!info] Kurzdefinition
> Die Service-Wertschöpfungskette (Service Value Chain, SVC) ist das zentrale Element des ITIL Service Value System. Sie ist ein Betriebsmodell, das die zentralen Aktivitäten beschreibt, die erforderlich sind, um auf Nachfrage zu reagieren und die Realisierung von Wert durch die Schaffung und das Management von Produkten und Services zu unterstützen. Sie umfasst sechs Aktivitäten: Planung, Verbesserung, Engagement, Design und Transition, Erhalten/Erstellen, Bereitstellung und Support.

## Beschreibung

Folien 70–78 widmen sich der Service-Wertschöpfungskette. Folie 70 stellt sie als zentrales Element des SVS dar; Folie 71 zeigt das Diagramm mit den sechs Aktivitäten und dem Demand → Engage → [Design+Transition / Obtain+Build / Deliver+Support] → Products+Services → Value-Fluss, eingerahmt von **Plan** (oben) und **Improve** (unten).

**Die sechs Aktivitäten** und ihre Zwecke (Folien 73–78):

1. **Planung (Plan)** — Folie 73:
   > „Ein gemeinsames Verständnis der Vision, des aktuellen Stands und der Verbesserungsmöglichkeiten für alle vier Dimensionen und in allen Produkten und Dienstleistungen (Services) der Organisation sicherstellen."

2. **Verbesserung (Improve)** — Folie 74:
   > „Eine ‚kontinuierliche Verbesserung' von Produkten, Services und Practices über alle Aktivitäten der Wertschöpfungskette und die vier Dimensionen des Service Managements hinweg sicherstellen."

3. **Engagement (Engage)** — Folie 75:
   > „Ein gutes Verständnis für die Bedürfnisse der Stakeholder, Transparenz, kontinuierliches Engagement und gute Beziehungen zu allen Stakeholdern fördern. Alle eingehenden und ausgehenden Interaktionen mit Parteien außerhalb der Wertschöpfungskette werden über Engagement durchgeführt."

4. **Design und Transition (Design and Transition)** — Folie 76:
   > „Sicherstellen, dass Produkte und Services die Erwartungen der Stakeholder an Qualität, Kosten und Zeit bis zur Markteinführung kontinuierlich erfüllen."

5. **Erhalten und Erstellen (Obtain/Build)** — Folie 77:
   > „Sicherstellen, dass Servicekomponenten verfügbar sind, wann und wo sie benötigt werden, und dass sie den vereinbarten Spezifikationen entsprechen."

6. **Bereitstellung und Support (Deliver and Support)** — Folie 78:
   > „Sicherstellen, dass die Services gemäß den vereinbarten Spezifikationen und Erwartungen der Stakeholder bereitgestellt und supported werden."

Folie 72 ergänzt das Konzept der **Servicewertströme** (siehe [[SM - ITIL 4 - Wertstrom Definition]]):
> „Servicewertströme sind spezifische Kombinationen von Aktivitäten und Practices. Jede ist für ein bestimmtes Szenario konzipiert. Einmal entworfen, sollten die Wertströme der kontinuierlichen Verbesserung unterliegen. Beispiele für generische Practices, die in vielen verschiedenen Szenarien als Unterstützung verwendet werden können: Geschäftsanalyse, Entwicklung, Testen, Release und Rollout, Unterstützung."

## Bestandteile / Aufbau

| # | Aktivität | Zweck |
|---|---|---|
| 1 | Planung | Gemeinsames Verständnis von Vision, Ist-Stand, Verbesserung über alle 4 Dimensionen |
| 2 | Verbesserung | Kontinuierliche Verbesserung über alle Aktivitäten und 4 Dimensionen |
| 3 | Engagement | Stakeholder-Bedürfnisse verstehen; Verbindung zu allen externen Parteien |
| 4 | Design und Transition | Produkte/Services mit Stakeholder-erwartungs-konformer Qualität, Kosten, Time-to-Market |
| 5 | Erhalten und Erstellen | Servicekomponenten verfügbar, wo/wann nötig, gemäß Spezifikation |
| 6 | Bereitstellung und Support | Services gemäß Vereinbarung bereitstellen und unterstützen |

Im Diagramm (Folie 71): Demand → Engage → [Design+Transition / Obtain+Build / Deliver+Support] → Products+Services → Value, alles eingerahmt von Plan (oben) und Improve (unten).

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Krankenhaus-Service „mobiler KIS-Zugang":

- **Plan:** Vision „mobile Pflegekraft 2027" mit allen Dimensionen abstimmen.
- **Improve:** Lessons-Learned aus früheren Tablet-Pilotprojekten einbeziehen.
- **Engage:** Pflegeleitung, Datenschutz, Betriebsrat, Cloud-Anbieter einbinden.
- **Design and Transition:** Lösung entwerfen, Pilot, Schulung.
- **Obtain/Build:** Tablets beschaffen, App ausrollen.
- **Deliver and Support:** Anwender-Support, Garantie-Management, Updates.

## Abgrenzung

- **Service-Wertschöpfungskette vs. Servicewertstrom**: Die SVC ist die generische Vorlage; ein Wertstrom ist eine konkrete Kombination aus SVC-Aktivitäten + Practices für ein spezifisches Szenario.
- **SVC vs. ITIL-V3-Lifecycle**: V3 hat 5 Phasen (Strategy/Design/Transition/Operation/CSI), die sequenziell-zyklisch ablaufen. SVC hat 6 Aktivitäten, die nicht-linear in beliebigen Wertströmen kombiniert werden — flexibler, agil-kompatibel.
- **SVC vs. Practices**: Practices sind konkrete Organisationsressourcen; SVC-Aktivitäten sind generische Wertschöpfungs-Schritte. Practices unterstützen die Aktivitäten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche sechs Aktivitäten umfasst die Service-Wertschöpfungskette? — Planung, Verbesserung, Engagement, Design und Transition, Erhalten/Erstellen, Bereitstellung und Support.

**Anwendungsfrage:** Skizzieren Sie für einen konkreten Service einen Wertstrom — welche Aktivitäten der SVC werden in welcher Reihenfolge mit welchen Practices kombiniert?

**Diskussionsfrage:** Wie unterscheidet sich die SVC vom V3-Lifecycle? — V3 ist sequenziell-zyklisch und phasenorientiert; SVC ist nicht-linear und kombinierbar — entspricht der ITIL-4-Philosophie der Wertströme.

**Mögliche Anschlussfragen:**
- Was ist die Rolle von „Engagement" in der SVC? — Brücke zu allen externen Parteien (Stakeholder).
- Warum sind Plan und Improve als Außenring dargestellt? — Beide wirken über alle anderen Aktivitäten hinweg (Querschnittsfunktionen).
- Wie hängt die SVC mit den 34 Practices zusammen?
- Welche Practices sind in der Service-Wertschöpfungskette generische Unterstützer (Folie 72)? — Geschäftsanalyse, Entwicklung, Testen, Release und Rollout, Unterstützung.

## Verwandt

- [[SM - ITIL 4 - Service Value System]]
- [[SM - ITIL 4 - Wertstrom Definition]]
- [[SM - ITIL 4 - Management Practices Übersicht]]
- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - ITIL 4 - Sieben Grundprinzipien]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 70–78; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
