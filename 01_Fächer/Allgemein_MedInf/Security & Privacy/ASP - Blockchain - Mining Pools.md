---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Blockchain]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Blockchain - Mining Pools

> [!info] Kurzdefinition
> Zusammenschluss mehrerer Miner, die ihre Rechenleistung bündeln, um die Chance auf einen Block-Reward zu erhöhen. Die Belohnung wird unter den Teilnehmenden anteilig aufgeteilt.

## Beschreibung

Folie 21:

- Mining ist für Privatpersonen, insbesondere mit einem einzelnen Server, oft aufgrund der hohen Gesamt-Rechenleistung des Netzwerks **nicht mehr wirtschaftlich**.
- In vielen Fällen schließen sich Miner in **Mining-Pools** zusammen, um ihre Chancen auf Belohnungen zu erhöhen.
- Belohnungen werden dann unter den teilnehmenden Minern aufgeteilt.

**Implizite Schwäche, im PDF nicht explizit ausgeführt:** Mining-Pools führen zu einer **Konzentration der Hash-Rate**. Wenn wenige Pools gemeinsam mehr als 51 % der Hash-Rate halten, wird die Annahme der Dezentralität untergraben.

## Bestandteile / Aufbau

| Element | Funktion |
|---|---|
| Pool-Operator | koordiniert die Arbeitsverteilung |
| Pool-Miner | bringen Rechenleistung ein |
| Reward-Verteilung | typischerweise proportional zur eingebrachten Hash-Rate |

## Beispiel

Aus Folie 21: Fünf Miner mit jeweils eigenen Server-Farmen schließen sich zu einem Mining-Pool zusammen. Sie versuchen gemeinsam, die richtige Nonce zu finden. Wenn ein Mitglied erfolgreich ist, geht der Reward an den Pool-Operator und wird dann anteilig verteilt.

## Abgrenzung

- **Solo-Mining vs. Pool-Mining:** Solo bekommt jeder Block-Reward zu 100 %, aber selten (für Kleinst-Miner praktisch nie). Pool-Mining bekommt regelmäßig Anteile.
- **Mining-Pool ≠ Bitcoin-Pool/Mempool:** Der Mining-Pool ist eine Allianz von Minern. Der Mempool ist die Warteschlange unbestätigter Transaktionen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Mining-Pool und warum gibt es ihn?

**Anwendungsfrage:** Wie wird die Belohnung im Mining-Pool aufgeteilt?

**Diskussionsfrage:** Welche Risiken birgt die Existenz großer Mining-Pools für die Dezentralität von Bitcoin? (Stichwort: 51-%-Attack möglich, wenn ein einzelner Pool / eine Allianz mehr als 50 % der Hash-Rate kontrolliert.)

**Mögliche Anschlussfragen:**
- Welche Konsequenzen hätte ein Mining-Pool mit dauerhaft mehr als 51 % Hash-Rate?
- Wie haben sich die größten Pools historisch entwickelt? (*Im PDF nicht behandelt.*)

## Verwandt

- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Bitcoin Funktionsweise]]
- [[ASP - Blockchain - Halving]]
- [[ASP - Blockchain - Kritik PoW]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 21
