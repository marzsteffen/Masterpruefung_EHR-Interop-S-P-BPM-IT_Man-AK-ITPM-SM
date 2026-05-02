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

# ITM-AK - Costing Myth - Charges als Cost Surrogate

> [!info] Kurzdefinition
> Mythos #1 laut Kaplan/Porter: Charges (Abrechnungsbeträge) seien ein guter Stellvertreter für tatsächliche Anbieterkosten. Falsch – Charges spiegeln Reimbursement-Logik wider, nicht Ressourcenverbrauch, und führen Costing-Systeme systematisch in die Irre.

## Beschreibung

Healthcare-Anbieter haben ihre Kostensysteme historisch auf das Reimbursement-System aufgebaut – in den USA insbesondere durch den Medicare Cost Report (MCR), der eine Aufschlüsselung von Kosten und Charges nach Department verlangt. Das Ergebnis: Was abgerechnet wird, gilt operativ als „Kost". Statt eigene, akkurate Costing-Systeme zu pflegen, leiten Anbieter Kosten aus Reimbursement-Daten ab.

Das Paper kritisiert diesen Ansatz aus mehreren Gründen:
- **Aggregation:** Reimbursement-Daten sind hoch aggregiert, basieren auf groben Schätzungen.
- **Profit-Margen-Annahme:** Reimbursement-basiertes Costing unterstellt fälschlich, dass jeder abrechenbare Vorgang dieselbe Profit-Marge hat.
- **Nicht-abrechenbare Aktivitäten** (z. B. Patientenkonsultationen): Werden in große Overhead-Pools verschoben und willkürlich ungenau auf abrechenbare Vorgänge umgelegt.
- **RVUs (Relative Value Units)** für Arztleistungen: Geschätzt aus Befragungen von Spezialisten – die selbst Anreiz haben, Zeit und Komplexität zu überschätzen. Niemand misst diese RVUs systematisch.
- **Reimbursement → Cost-Allocation:** Wenn Reimbursement-Raten zur Allokation von Arztkosten *auf Patienten* verwendet werden, werden inakkurate Schätzungen zu „Kostenwahrheiten" – ein Zweck, für den sie nie gedacht waren.

Kernkritik: Die tatsächlichen Kosten einer Ressource sind unabhängig davon, ob sie für eine schlecht oder gut bezahlte Leistung eingesetzt wird, und unabhängig davon, ob die Leistung überhaupt erstattet wird.

## Bestandteile / Aufbau

| Quelle der Verzerrung | Wirkung |
|---|---|
| Aggregation auf Department-Ebene | Patientenebene unsichtbar |
| Reimbursement = Kosten | Cross-Subsidies zwischen Services nicht aufdeckbar |
| RVU-Schätzungen | Systematische Überschätzung von Zeit/Komplexität |
| Allokation via Reimbursement-Raten | Inakkurate Daten werden im Costing kanonisiert |
| Nicht-abrechenbare Events in Overhead | Wertvolle, aber nicht-abrechenbare Aktivitäten werden unsichtbar |

## Beispiel

Im Paper nicht ausgearbeitet als einzelnes Fallbeispiel, aber als systemische Kritik formuliert. Implizit aus dem Knee-Replacement-Beispiel ablesbar: Der gleiche Eingriff kostet in den USA das 3-fache wie in DE/SE – die genauen Treiber bleiben in einem Charges-basierten System unsichtbar.

## Abgrenzung

- **Charges ≠ Reimbursement:** Charges sind die in Rechnung gestellten Beträge; Reimbursement ist das, was tatsächlich gezahlt wird (oft niedriger). Beide sind nicht Kosten.
- **Charges ≠ Direct Costs:** Direct Costs lassen sich aus Buchhaltung extrahieren (Personal, Material), Charges sind ein verhandeltes Preisniveau.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Warum sind Charges kein guter Surrogate für Kosten?"

**Anwendungsfrage:** „Was passiert, wenn ein Krankenhaus seine Kosten allein aus Reimbursement-Daten ableitet?" Erwartet: Cross-Subsidies werden nicht erkannt; hochbezahlte Services erscheinen profitabel, niedrig-bezahlte unprofitabel; Anreiz, hochbezahlte Services auszuweiten ohne Rücksicht auf Wert.

**Diskussionsfrage:** Warum hat sich diese Praxis trotz Kritik so lange gehalten? Diskussion:
- Pfadabhängigkeit (Medicare Cost Report ist verpflichtend → kein doppelter Aufwand für separates Costing).
- Technologische Hürde (Patientenebene-Tracking war historisch unmöglich).
- Politische Hürde (Anbieter, deren Margen aus Cross-Subsidies leben, haben kein Interesse an Transparenz).

**Mögliche Anschlussfragen:**
- Wie löst TDABC genau dieses Problem (Capacity Cost Rate × Time)?
- Welche Implikationen hat dieser Mythos für DRG-basierte Erstattungssysteme?
- Wie würden RVUs aussehen, wenn sie auf TDABC-Daten basierten?

## Verwandt

- [[ITM-AK - TDABC - Time Driven Activity Based Costing]]
- [[ITM-AK - Costing Myth - Hospital Overhead too complex]]
- [[ITM-AK - Costing Myth - Healthcare Costs are fixed]]
- [[ITM-AK - Bundled Payments und Value-Based Reimbursement]]

## Quelle

- Vorlesung: [[ITM-AK - Paper - Porter-Kaplan 2011 - TDABC]]
- Folien/Seitenangabe: HBR-Paginierung 50 (Sidebar „Myth #1: Charges are a good surrogate for provider costs").
