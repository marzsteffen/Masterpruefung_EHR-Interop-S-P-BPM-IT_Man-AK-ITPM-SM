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

# ITM-AK - TDABC - Time Driven Activity Based Costing

> [!info] Kurzdefinition
> TDABC ist eine Kostenrechnungsmethode, die einer einzelnen Patientenbehandlung über den vollen Care Cycle exakt diejenigen Ressourcenkosten zuordnet, die tatsächlich verbraucht wurden. Pro Prozess-Schritt werden nur zwei Parameter benötigt: der Capacity Cost Rate der Ressource und die Zeit, die der Patient diese Ressource gebunden hat.

## Beschreibung

Kaplan und Porter argumentieren, dass traditionelle Healthcare-Kostensysteme aus dem Reimbursement abgeleitet sind und damit systematisch verzerrt: sie aggregieren Kosten auf Abteilungsebene, allokieren Overhead nach „peanut butter"-Methode (gleichmäßig verschmiert) und bilden den tatsächlichen Ressourcenverbrauch eines Patienten nicht ab.

TDABC dreht diese Logik um. Die Analyseeinheit ist **patient × medical condition × full care cycle**. Für jeden Prozess-Schritt entlang des Care Cycle wird gefragt:

1. Welche Ressourcen werden benötigt (Personal, Equipment, Raum, Verbrauchsmaterial)?
2. Wie viel Zeit nutzt der Patient jede dieser Ressourcen?

Die Multiplikation der Zeit mit dem **Capacity Cost Rate** der Ressource (siehe [[ITM-AK - Capacity Cost Rate]]) ergibt die zugeordneten Kosten. Summiert über alle Prozess-Schritte ergibt das die Gesamtkosten der Patientenbehandlung.

## Bestandteile / Aufbau

Kerngleichung (für jeden Ressourceneinsatz):

```
Zugeordnete Kosten = Capacity Cost Rate (€/Stunde) × tatsächlich genutzte Zeit (Stunden)
```

Über den Care Cycle:

```
Total Patient Cost = Σ (Capacity Cost Rate_i × Time_i)  für alle Ressourcen i, für alle Process Steps
```

Die Methode setzt voraus:
- **Care Delivery Value Chain** für die medical condition (siehe [[ITM-AK - Care Delivery Value Chain]]).
- **Process Maps** je Aktivität in der CDVC, mit allen Capacity-Supplying Resources.
- **Time Estimates** pro Prozess-Schritt (Standardzeiten, gemessen oder geschätzt).
- Kostendaten je Ressource (aus Hauptbuch, Personalsystemen, IT, …).

Implementierungs-Mehrwert:
- Macht ungenutzte Kapazität sichtbar.
- Erlaubt Vergleich zwischen Anbietern, Ärzten, Standorten für dieselbe medical condition.
- Quantifiziert Effekt von Prozessänderungen (vorher/nachher).

## Beispiel

**Patient Jones** (Paper, S. 51–52): ambulanter Klinikbesuch mit drei Prozessen (Check-in, Voruntersuchung, Behandlung) und drei Ressourcen (Administrator Allen, Nurse White, Physician Green).

| Ressource | Capacity Cost Rate | Zeit | Kosten |
|---|---|---|---|
| Administrator Allen | $45/h | 0,3 h | $13,50 |
| Nurse White | $65/h | 0,4 h | $26,00 |
| Physician Green | $300/h | 0,15 h | $45,00 |
| **Total** | | | **$84,50** |

(Capacity Cost Rate der Nurse berechnet aus monatlichen Gesamtkosten $7.280 / 112 verfügbare Patientenstunden = $65/h. Siehe [[ITM-AK - Capacity Cost Rate]].)

## Abgrenzung

- **TDABC ≠ klassisches Activity-Based Costing (ABC):** Klassisches ABC erhebt Aktivitäten und Cost Drivers über Mitarbeiterbefragungen – aufwändig und subjektiv. TDABC ersetzt das durch Kapazitätskostensätze und Zeit-Schätzungen, was den Pflegeaufwand drastisch reduziert.
- **TDABC ≠ Charge-/Reimbursement-Based Costing:** Charges sind das, was abgerechnet wird; sie reflektieren historisch gewachsene Erstattungslogik, nicht den tatsächlichen Ressourcenverbrauch. Siehe [[ITM-AK - Costing Myth - Charges als Cost Surrogate]].
- **TDABC ≠ RVU-basierte Allokation:** RVUs (Relative Value Units) basieren auf Befragungs-Schätzungen von Spezialisten und werden für Reimbursement, nicht für interne Kostenmessung erhoben.
- **TDABC ≠ Departmental Costing:** TDABC orientiert sich an Patient + Care Cycle, nicht an Abteilungen. Departmental Costing aggregiert auf Cost Center, was den Verbrauch eines einzelnen Patienten nicht zeigt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was ist TDABC und wie unterscheidet es sich von traditionellen Healthcare-Kostensystemen?"

**Anwendungsfrage:** „Berechnen Sie die Kosten eines Klinikbesuchs nach TDABC, wenn der Patient 18 min Administrator (Cost Rate $45/h), 24 min Nurse ($65/h) und 9 min Arzt ($300/h) nutzt." Antwort: $84,50 (Patient-Jones-Beispiel).

**Diskussionsfrage:** Warum scheitern Healthcare-Anbieter typischerweise an akkurater Kostenmessung, obwohl sie über umfangreiche Daten verfügen? Diskussion:
- Reimbursement-Logik überlagert interne Kostensysteme.
- IT-Systeme tracken keine Patientenzeiten pro Ressource.
- Care Cycles spannen sich über mehrere Abteilungen / Anbieter, niemand hat die End-to-End-Sicht.
- Klinische und Finanz-Abteilungen sprechen unterschiedliche Sprachen.

**Mögliche Anschlussfragen:**
- Wie hängen TDABC und Process Mapping zusammen?
- Welche Rolle spielt IT für die TDABC-Implementierung (RFID, Bar-Code, EHR-Daten)?
- Inwiefern ermöglicht TDABC die Einführung von Bundled Payments?
- Warum waren die Pilot-Sites (MD Anderson, Schön Klinik, …) erfolgreich?

## Verwandt

- [[ITM-AK - TDABC - Sieben Schritte der Kostenmessung]]
- [[ITM-AK - Capacity Cost Rate]]
- [[ITM-AK - Care Delivery Value Chain]]
- [[ITM-AK - Value in Healthcare]]
- [[ITM-AK - Costing Myth - Charges als Cost Surrogate]]
- [[ITM-AK - Costing Myth - Hospital Overhead too complex]]
- [[ITM-AK - Costing Myth - Healthcare Costs are fixed]]
- [[ITM-AK - Bundled Payments und Value-Based Reimbursement]]
- [[ITM-AK - Rechnungswesen - Externes vs Internes]]
- [[BPM - MOC]]

## Quelle

- Vorlesung: [[ITM-AK - Paper - Porter-Kaplan 2011 - TDABC]]
- Folien/Seitenangabe: HBR-Paginierung 49–55, insb. 51 (Patient Jones), 51 (Capacity-Cost-Rate-Formel).
