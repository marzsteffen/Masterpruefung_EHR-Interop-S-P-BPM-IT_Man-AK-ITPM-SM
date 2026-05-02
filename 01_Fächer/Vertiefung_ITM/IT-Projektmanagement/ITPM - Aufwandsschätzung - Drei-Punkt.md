---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Initiierung Strukturierung Requirements]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Aufwandsschätzung - Drei-Punkt

> [!info] Kurzdefinition
> Die Drei-Punkt-Schätzung ist eine klassische Methode zur Schätzung der Zeitdauer einer Aktivität. Jeder Schätzer gibt drei Werte ab: optimistisch, wahrscheinlich, pessimistisch. Der erwartete Wert berechnet sich als gewichtetes Mittel: **t = (tO + 4·tW + tP) / 6**.

## Beschreibung

Die Vorlesung führt die Drei-Punkt-Schätzung als Methode zur Aufwandsschätzung im Ablauf-/Terminplan ein (Folie 48). Sie soll die Unsicherheit bei Schätzungen explizit machen.

## Bestandteile / Aufbau

| Wert | Bedeutung |
|---|---|
| **tO** | optimistische Zeit – Schätzung des minimalsten Zeitbedarfs |
| **tW** | wahrscheinliche Zeit – was wird normalerweise benötigt |
| **tP** | pessimistische Zeit – Schätzung der längsten Zeit, die man brauchen könnte |

**Berechnungsformel:**

```
t = (tO + 4·tW + tP) / 6
```

## Beispiel

*Im PDF nicht durch konkretes Zahlenbeispiel illustriert.*

> *Rechenbeispiel zur Lernunterstützung (Standardlehrbuch, nicht aus Vorlesung):* tO = 4 Tage, tW = 7 Tage, tP = 12 Tage → t = (4 + 28 + 12) / 6 = 44 / 6 ≈ 7,33 Tage.

## Abgrenzung

- **Drei-Punkt-Schätzung** ist eine **klassische** Methode (PERT-/Beta-Verteilung im Hintergrund). Standardlehrbuch unterscheidet zusätzlich zwischen Beta- und Triangular-Mittel; im PDF nur die Beta-Variante mit Faktor 4.
- **Agile Pendants:** Story Points + Planning Poker / Magic Estimation (siehe [[ITPM - Agile - Story Points]], [[ITPM - Agile - Planning Poker]]).
- **Function-Point-Methode** (siehe [[ITPM - Aufwandsschätzung - Function Point]] – kommt in Vorlesung 6).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie lautet die Formel der Drei-Punkt-Schätzung, und wozu dienen die drei Werte?

**Anwendungsfrage:** Schätzen Sie für ein AP „Schulungsunterlagen erstellen" tO/tW/tP und berechnen Sie t.

**Diskussionsfrage:** Welche Vorteile hat die Drei-Punkt-Schätzung gegenüber einer einfachen Mittelwert-Schätzung (tO + tP)/2?

**Mögliche Anschlussfragen:**
- Warum wird tW vierfach gewichtet?
- Wie verhält sich Drei-Punkt zu PERT-Berechnungen?
- Wann sollte man Story Points statt Drei-Punkt verwenden?

## Verwandt

- [[ITPM - Ablauf- und Terminplan]]
- [[ITPM - Pufferzeiten]]
- [[ITPM - Kritischer Weg]]
- [[ITPM - Aufwandsschätzung - Function Point]]
- [[ITPM - Agile - Story Points]]
- [[ITPM - Agile - Planning Poker]]

## Quelle

- Vorlesung: [[ITPM - VL - Initiierung Strukturierung Requirements]]
- Folien/Seitenangabe: 48
