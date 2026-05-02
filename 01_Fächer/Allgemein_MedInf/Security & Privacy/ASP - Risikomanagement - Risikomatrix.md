---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Informationssicherheits-Risikomanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Risikomanagement - Risikomatrix

> [!info] Kurzdefinition
> Visuelle Bewertungsmatrix mit Eintrittswahrscheinlichkeit auf der einen und Auswirkung im Schadensfall auf der anderen Achse. Zellen werden mit Risikoklassen (rot/gelb/grün) markiert. Granularität (3×3 vs. 4×4 vs. größer) bestimmt Differenzierungs-Schärfe.

## Beschreibung

Folie 12 zeigt eine 4×4-Risikomatrix.

**Achsen:**
- y-Achse: Eintrittswahrscheinlichkeit (1 gering bis 4 sehr hoch).
- x-Achse: Auswirkung im Schadensfall (1 gering bis 4 sehr hoch).

**Risikoklassen (Beispiel-Färbung):**
- **Rot = hohes Risiko:** rechts oben (hohe Wahrscheinlichkeit + hohe Auswirkung).
- **Gelb = mittleres Risiko:** Diagonale.
- **Grün = geringes Risiko:** links unten.

**Granularität (Folie 13):**
- Angemessene Anzahl an Klassen für Eintrittswahrscheinlichkeit und Schadenshöhe wählen.
- Größere Anzahl an Klassen führt zu höherer Granularität und damit zu besserer Unterscheidbarkeit von Risiken.
- 3×3 Matrix: zwei Risiken landen schnell in derselben Zelle („kein erkennbarer Unterschied").
- 4×4 Matrix: feinere Differenzierung möglich.

**Berechnung:** Risiko = Eintrittswahrscheinlichkeit × Auswirkung. Position in der Matrix bestimmt die Klasse (Farbe).

## Bestandteile / Aufbau

| Element | Bedeutung |
|---|---|
| y-Achse | Eintrittswahrscheinlichkeit |
| x-Achse | Auswirkung im Schadensfall |
| Zelle | konkrete Bewertung eines Risikos |
| Farbe | Risikoklasse (rot/gelb/grün) |
| Granularität | Anzahl Stufen pro Achse (3, 4, 5, …) |

## Beispiel

Aus Folie 13: 3×3-Matrix mit zwei Risiken in derselben grünen Zelle – Risiko 1 und Risiko 2 sind nicht unterscheidbar. Bei 4×4-Matrix mit feinerer Skalierung würden sie in unterschiedliche Zellen fallen.

## Abgrenzung

- **Risikomatrix ≠ Risikoliste:** Matrix ist die visuell-quantitative Darstellung; die Liste enthält die qualitativ-textuellen Beschreibungen (Wer + tut was + gegen wen + Auswirkung – siehe [[ASP - Risikomanagement - Asset-basierte Identifikation]]).
- **3×3 vs. 4×4:** Trade-off zwischen Übersichtlichkeit (weniger Klassen) und Differenzierungs-Schärfe (mehr Klassen).
- **Im PDF (Folie 13)** wird ausdrücklich vor der 3×3-Matrix gewarnt – sie kann zwei sehr unterschiedliche Risiken gleich aussehen lassen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was zeigt eine Risikomatrix, und welche Achsen hat sie?

**Anwendungsfrage:** Trage drei konkrete Risiken in eine 4×4-Matrix ein. Welcher Klasse gehören sie an?

**Diskussionsfrage:** Welche Vor- und Nachteile hat eine größere Granularität (z. B. 5×5)? Wann ist eine kleinere Matrix angemessener? (Kleine Organisationen mit wenig Daten; Erstaufsetzen des Prozesses.)

**Mögliche Anschlussfragen:**
- Welche Schwächen kann die Risikomatrix systematisch haben? (Die Folie nennt das implizit über das 3×3-Problem; in der Praxis: subjektive Skalen, Anchoring-Effekte – im PDF nicht ausgeführt.)
- Wie verbindet die Matrix die Kontextbestimmung mit der Risikoanalyse?
- Wie ändert sich die Klasse, wenn man Maßnahmen umsetzt? (Verschiebung in der Matrix.)

## Verwandt

- [[ASP - Risikomanagement - Kontextbestimmung]]
- [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]
- [[ASP - Risikomanagement - Risikobewertung]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 12, 13
