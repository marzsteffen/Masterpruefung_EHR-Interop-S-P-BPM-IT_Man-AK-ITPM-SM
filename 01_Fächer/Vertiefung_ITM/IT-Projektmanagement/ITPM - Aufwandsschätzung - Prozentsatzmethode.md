---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Aufwandsschätzung - Prozentsatzmethode

> [!info] Kurzdefinition
> Die Prozentsatzmethode ermittelt den Aufwand für übrige Phasen als Anteil am Gesamtaufwand, basierend auf erfahrungsbasierten Verhältniszahlen aus vergleichbaren Projekten. Eine Phase wird detailliert geschätzt; die übrigen werden hochgerechnet. Sie ist keine vollständig eigenständige Methode.

## Beschreibung

Aus Folie 36 und 43:

- **Keine vollständig eigenständige Schätzmethode** – Detailschätzung einer Phase erfolgt mit anderen Methoden.
- Aufwand für übrige Phasen entspricht einem **Anteil am Gesamtaufwand** (abhängig von der Art des Projekts).

**Vorgehensweise (Folie 43):**

1. **Ermittlung der prozentualen Aufwandsverteilung** für die einzelnen Projektphasen aus **abgelaufenen vergleichbaren Projekten**.
2. **Detaillierte Schätzung einer Phase** und Hochrechnung über die ermittelten Prozentsätze.
3. Alternative: Durchführung einer Phase und anschließend Hochrechnung.

## Bestandteile / Aufbau

### Beispiel: Prozentsatzmethode nach Hewlett-Packard (Folie 36)

| Phase | Anteil |
|---|---|
| **Analyse** | 18 % |
| **Entwurf** | 19 % |
| **Implementierung** | 34 % |
| **Test** | 29 % |

### Vorteile (Folie 43)

- **Zeitsparende** Methode.
- Oft **überraschend genau**.

### Nachteile (Folie 43)

- Bei kleinen Abweichungen der Detailschätzung: **Multiplikation des Fehlers** in der Hochrechnung.

## Beispiel

Hewlett-Packard-Verteilung (siehe oben). Wenn die Implementierung mit 34 PT geschätzt wird, ergibt das 100 PT Gesamtaufwand.

## Abgrenzung

- **Prozentsatzmethode** ≠ **Drei-Punkt-Schätzung** (siehe [[ITPM - Aufwandsschätzung - Drei-Punkt]]): Drei-Punkt schätzt eine Aktivität direkt; Prozentsatz hochrechnet die Verteilung.
- **Prozentsatzmethode** ≠ **Analogiemethode**: Analogie vergleicht **das ganze Projekt** mit Vorprojekten; Prozentsatz vergleicht nur die **Verteilung über Phasen**.
- **Aufwandsverteilung in mittelgroßen Projekten** (¼ je Phase, 10 % PM, siehe [[ITPM - RE - Aufwand und Kostenschätzung]]) ist eine Variante der Prozentsatzmethode.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie funktioniert die Prozentsatzmethode? Warum ist sie keine eigenständige Schätzmethode?

**Anwendungsfrage:** Sie haben den Implementierungsaufwand für ein Patientenportal mit 800 PT geschätzt. Wie hoch ist der Gesamtaufwand nach HP-Verteilung?

**Diskussionsfrage:** Wann ist die Prozentsatzmethode robust, wann gefährlich? Welche Projektarten sollten sie meiden?

**Mögliche Anschlussfragen:**
- Wo bekommt man die Prozentwerte her (Cost Data Base, Erfahrungsdatenbank)?
- Wie verhält sich die Methode zur Analogie?
- Welche Rolle spielt der „Multiplikationsfehler"?

## Verwandt

- [[ITPM - Aufwandsschätzung - Schätzverfahren Übersicht]]
- [[ITPM - Aufwandsschätzung - Analogiemethode]]
- [[ITPM - Aufwandsschätzung - Drei-Punkt]]
- [[ITPM - RE - Aufwand und Kostenschätzung]]

## Quelle

- Vorlesung: [[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]
- Folien/Seitenangabe: 36, 43
