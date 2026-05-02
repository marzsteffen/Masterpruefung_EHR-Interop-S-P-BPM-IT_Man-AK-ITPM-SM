---
fach: itm-ak
typ: konzept
status: offen
quelle: "[[ITM-AK - Paper - Porter-Kaplan 2011 - TDABC]]"
tags:
  - fach/vertiefung/itm-ak
  - typ/konzept
  - status/offen
---

# ITM-AK - TDABC - Sieben Schritte der Kostenmessung

> [!info] Kurzdefinition
> Die TDABC-Implementierung im Healthcare folgt einem siebenstufigen Prozess: von der Wahl der medical condition über die Care Delivery Value Chain, Process Maps und Zeit-Schätzungen bis zur Berechnung von Capacity Cost Rates und der Gesamtkosten über den vollen Care Cycle.

## Beschreibung

Im Sidebar-Block „Creating a Cost Measurement System" listen Kaplan und Porter die sieben Schritte explizit auf. Der Prozess setzt voraus, dass die Anbieter ihre Versorgung als zusammenhängenden Care Cycle für eine medical condition denken – nicht als Folge isolierter Abrechnungseinheiten.

## Bestandteile / Aufbau

| # | Schritt | Inhalt laut Paper |
|---|---|---|
| 1 | **Select the medical condition** | Wahl der medical condition oder Patient Population, die kostiert werden soll. Definition von Anfang und Ende des Care Cycle. Bei chronischen Erkrankungen typischerweise ein Jahr. |
| 2 | **Define the care delivery value chain (CDVC)** | Mapping aller Hauptaktivitäten im Care Cycle samt Lokationen. Fokussiert Anbieter auf den vollen Care Cycle statt einzelner Prozesse. |
| 3 | **Develop process maps of each activity in patient care delivery** | Pro Aktivität: Identifikation aller eingesetzten Capacity-Supplying-Resources (Personen, Räume, Equipment) plus direkt benutzte Verbrauchsmaterialien. |
| 4 | **Obtain time estimates for each process step** | Zeit-Schätzungen für jede Ressource und jeden Patientenkontakt. Standardzeiten genügen für kurze, wenig variierende Prozesse; komplexe Prozesse benötigen Messung. |
| 5 | **Estimate the cost of supplying each patient care resource** | Direkte Kosten je Ressource: Personalkosten, Equipment-Abschreibung/Leasing, Supplies, Operating Expenses. Unterstützungs-Funktionen werden den primären Ressourcen zugewiesen. |
| 6 | **Estimate the practical capacity of each resource provider, and calculate the capacity cost rate** | Praktische Kapazität (HR-Daten: tatsächliche Arbeitstage, abzüglich Pausen, Schulung, Verwaltung). Capacity Cost Rate = Schritt 5 / Schritt 6. |
| 7 | **Compute the total costs over each patient's cycle of care** | Multiplikation Capacity Cost Rate × Zeit pro Schritt; Summe über alle Schritte und alle Ressourcen. |

## Beispiel

**Patient Jones** (Paper) und **MD Anderson Head & Neck Center** (CDVC + Process Map). Die CDVC für Severe Knee Osteoarthritis Requiring Replacement (Brigham & Women's Pilot, S. 56) zeigt sechs Stages: Monitoring/Preventing, Diagnosing, Preparing, Intervening, Recovering/Rehabbing, Monitoring/Managing. Jede Stage erhält eine eigene Process Map (Schritt 3).

## Abgrenzung

- **Schritt 1 ≠ Wahl einer Abteilung:** Die Wahl ist immer auf medical condition-Ebene, nicht auf Department-Ebene. Das ist der entscheidende Unterschied zu klassischer Kostenträgerrechnung.
- **Schritt 2 (CDVC) ≠ Prozesslandkarte:** CDVC ist die Stage-Übersicht über den vollen Care Cycle; Process Maps in Schritt 3 sind detaillierte Ablaufdiagramme innerhalb jeder Stage.
- **Schritt 6 (Capacity Cost Rate) ≠ Stundensatz:** Stundensatz wird oft auf Basis Vollzeit-Arbeitsstunden berechnet; Capacity Cost Rate basiert auf *praktischer* Kapazität (nach Abzug von Urlaub, Schulung, Pausen, Meetings).

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche Schritte umfasst die TDABC-Implementierung im Healthcare?"

**Anwendungsfrage:** „Beschreiben Sie, wie Sie eine TDABC-Analyse für die medical condition ‚Hüft-TEP' aufsetzen würden." Antwort entlang der sieben Schritte.

**Diskussionsfrage:** Welcher der sieben Schritte ist in der Praxis der schwierigste? Diskussion:
- Schritt 3+4 (Process Maps und Time Estimates): personalintensiv, klinisch dichter Aufwand. Pilot-Sites berichten 40 h pro Care-Cycle-Segment am MD Anderson.
- Schritt 6 (Practical Capacity): HR-Daten oft lückenhaft, Definitionen variieren (was zählt als „nicht verfügbar"?).
- Schritt 1 (Medical Condition wählen): organisatorisch heikel, weil Care Cycle oft über mehrere Abteilungen/Anbieter spannt – wer verantwortet?

**Mögliche Anschlussfragen:**
- Wie verhält sich Schritt 2 (CDVC) zu Wertstromanalyse / Lean?
- Welche IT-Systeme erleichtern Schritt 4 (Time Estimates) – RFID, Bar-Code, EHR-Time-Stamps?
- Was, wenn der Care Cycle einen Anbieter verlässt (Reha extern)? Wie endet die TDABC-Analyse?

## Verwandt

- [[ITM-AK - TDABC - Time Driven Activity Based Costing]]
- [[ITM-AK - Care Delivery Value Chain]]
- [[ITM-AK - Capacity Cost Rate]]
- [[ITM-AK - Value in Healthcare]]
- [[BPM - Process Mapping]]

## Quelle

- Vorlesung: [[ITM-AK - Paper - Porter-Kaplan 2011 - TDABC]]
- Folien/Seitenangabe: HBR-Paginierung 54 (Sidebar „Creating a Cost Measurement System"), 52–58 (ausführliche Erläuterung).
