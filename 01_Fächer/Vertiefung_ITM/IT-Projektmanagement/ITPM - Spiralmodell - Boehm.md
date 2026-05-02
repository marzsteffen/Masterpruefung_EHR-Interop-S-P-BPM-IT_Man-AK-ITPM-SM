---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Werkzeuge 01]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Spiralmodell - Boehm

> [!info] Kurzdefinition
> Das Spiralmodell (Boehm Spiral Model) ist eines der ersten Vorgehensmodelle, das einen **iterativ-inkrementellen** Entwicklungsprozess von Software beschreibt. Jeder Spiraldurchlauf entspricht einem vollständigen Wasserfall-Zyklus; charakteristisch ist die starke Betonung der **Risikoanalyse**.

## Beschreibung

Das Spiralmodell beschreibt als eines der ersten Vorgehensmodelle den **iterativ-inkrementellen Entwicklungsprozess** von Software. Es wird visualisiert durch eine Spirale, die ausgehend vom Ursprung eines rechtwinkligen Koordinatensystems im Uhrzeigersinn eine immer größer werdende Fläche umschließt. **Jeder Umlauf** entspricht dem **Durchlaufen eines Entwicklungszyklus** in den Phasen des Wasserfallmodells.

**Ursprung:**
Geht auf zwei Publikationen von **Barry Boehm** zurück:
- *Boehm, Barry: A Spiral Model of Software Development and Enhancement.* ACM SIGSOFT Software Engineering Notes, August 1986.
- *Boehm, Barry: A Spiral Model of Software Development and Enhancement.* IEEE Computer, Vol. 21, Ausg. 5, Mai 1988, S. 61–72.

**Charakteristisch:** Die starke Betonung der **Risikoanalyse**, die einem Scheitern des Projekts frühzeitig vorbeugen bzw. ein aussichtsloses Projekt möglichst schnell beenden soll.

## Bestandteile / Aufbau

Jeder Spiraldurchlauf gliedert sich in **vier Quadranten / Phasen**:

| Quadrant | Phase |
|---|---|
| 1 | Klärung der Ziele, Erhebung von Anforderungen, Bestimmung der Randbedingungen |
| 2 | **Risikoanalyse**, Entwurf und Erstellung eines Prototypen |
| 3 | Implementierung und Anwendertest |
| 4 | Auswertung der Iteration und Planung der nächsten Iteration bzw. **Stopp des Projekts** |

## Beispiel

Vertiefendes Video laut Vorlesung: `https://youtu.be/QqEhGXfGN8A`. Konkrete Anwendungsbeispiele werden im PDF nicht gegeben.

## Abgrenzung

- **Wasserfallmodell:** linear, nicht iterativ.
- **V-Modell-Vorgehensmodell:** linear mit gegenüberliegenden Testphasen.
- **Agile Modelle (Scrum):** ebenfalls iterativ-inkrementell, aber mit kürzeren, fest getakteten Iterationen und ohne den expliziten Risikoanalyse-Quadranten.

Das Spiralmodell ist ein **iteratives klassisches Modell** und damit konzeptionell **zwischen** strikt klassisch (Wasserfall) und agil zu verorten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind die vier Quadranten/Phasen eines Spiraldurchlaufs?

**Anwendungsfrage:** Welche Projektsituation passt besonders zum Spiralmodell? (hohe Unsicherheit, Risikofokus, Prototyping-Bedarf)

**Diskussionsfrage:** Inwieweit ist das Spiralmodell ein „Vorläufer" agiler Methoden? Was ist gleich, was unterschiedlich?

**Mögliche Anschlussfragen:**
- Wie viele Iterationen sind „typisch" – wann ist man fertig?
- Wie wird in der Praxis der „Stopp des Projekts" entschieden?
- Vergleich mit Scrum: Welche Rolle spielt Prototyping in beiden Ansätzen?

## Verwandt

- [[ITPM - Wasserfallmodell]]
- [[ITPM - V-Modell - Vorgehensmodell]]
- [[ITPM - Klassisches PM - Definition]]
- [[ITPM - Risikomanagement - Grundlagen]]
- [[ITPM - Vorgehensmodelle - Klassisch vs Agile]]
- [[ITPM - Scrum - Grundlagen]]

## Quelle

- Vorlesung: [[ITPM - VL - Werkzeuge 01]]
- Folien/Seitenangabe: 33–34
