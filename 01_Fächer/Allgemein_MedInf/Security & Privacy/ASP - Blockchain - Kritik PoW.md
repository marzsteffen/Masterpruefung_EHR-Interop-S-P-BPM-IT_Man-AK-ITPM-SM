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

# ASP - Blockchain - Kritik Proof-of-Work (Energieverbrauch)

> [!info] Kurzdefinition
> Proof-of-Work hat einen enormen Energie- und Ressourcenverbrauch: rund 137 TWh Strom pro Jahr (vergleichbar mit dem Stromverbrauch der Ukraine), 411 kg CO₂ pro Bitcoin-Transaktion und 71 kt Elektroschrott jährlich.

## Beschreibung

Folien 24 und 25 (Kritik-Folien) zeigen die ökologische Kritik an PoW.

**Bitcoin Energy Consumption (Folie 24):** Verbrauchskurve von 2017 bis Dezember 2023 (laut digiconomist.net), Spitzenwert über 200 TWh/Jahr in 2022, stabilisiert sich um 137 TWh/Jahr.

**Daten zu einer einzelnen Bitcoin-Transaktion (Folie 25):**

| Metrik | Wert | Vergleich |
|---|---|---|
| Elektrische Energie | 737,58 kWh | Stromverbrauch eines durchschnittlichen US-Haushalts über 25,28 Tage |
| CO₂-Fußabdruck | 411,39 kg CO₂ | 911 789 VISA-Transaktionen oder 68 565 Stunden auf YouTube |
| Elektrogeräte-Müll | 381,30 g | Gewicht von 2,33 iPhones 12 oder 0,78 iPads |

**Gesamtdaten Bitcoin pro Jahr (Folie 25):**

| Metrik | Wert | Vergleich |
|---|---|---|
| Elektrische Energie | 137,68 TWh | Stromverbrauch der Ukraine |
| CO₂-Fußabdruck | 76,79 Mt CO₂ | CO₂-Fußabdruck von Oman (309 501 km²) |
| Elektrogeräte-Müll | 71,18 kt | IT-Geräteabfall der Niederlande |

**Quelle (laut Folie):** https://digiconomist.net/bitcoin-energy-consumption

## Bestandteile / Aufbau

| Aspekt | Bewertung |
|---|---|
| Energie | sehr hoch, weil Brute-Force-Hashing |
| CO₂-Bilanz | abhängig vom Strommix; oft hoch |
| Hardware-Verschleiß | spezielle ASIC-Hardware mit kurzer Lebensdauer |
| Wirtschaftlicher Anreiz | je teurer Bitcoin, desto mehr Hash-Rate, desto mehr Energie |

## Beispiel

Direkt aus Folie 25: Eine einzige Bitcoin-Transaktion verbraucht so viel Strom wie ein US-Haushalt in über 25 Tagen.

## Abgrenzung

- **Kritik gilt PoW, nicht der Blockchain als solcher.** Andere Konsens-Protokolle wie [[ASP - Blockchain - Proof-of-Stake]] und [[ASP - Blockchain - Weitere Konsensus-Protokolle]] haben einen Bruchteil des Energiebedarfs.
- **Vergleichszahlen sind aus 2023.** *Aktuelle Werte können davon abweichen; im PDF nicht ausgewiesen.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Hauptkritik gibt es an Proof-of-Work, und wie ist sie konkret beziffert?

**Anwendungsfrage:** Vergleichen Sie eine Bitcoin-Transaktion mit einer VISA-Transaktion in Bezug auf den CO₂-Fußabdruck. (Faktor ca. 1 Mio.)

**Diskussionsfrage:** Wie versucht Ethereum, dieses Problem zu lösen? (Wechsel zu PoS, „The Merge" 2022 – senkte den Energieverbrauch um ca. 99,95 %, *im PDF nicht erwähnt*.) Welche Konsequenzen hat das für die Akzeptanz von Blockchain in Anwendungen mit Nachhaltigkeitsanforderungen (eHealth, öffentliche Verwaltung)?

**Mögliche Anschlussfragen:**
- Welcher Faktor verstärkt das Problem? (Wettbewerb der Miner um die Belohnung; je höher der Bitcoin-Preis, desto mehr Hash-Rate, desto mehr Energie.)
- Welche Konsens-Protokolle adressieren das Problem direkt?
- Welche Rolle spielen ASIC-Miner und ihre Lebensdauer?

## Verwandt

- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Proof-of-Stake]]
- [[ASP - Blockchain - Weitere Konsensus-Protokolle]]
- [[ASP - Blockchain - Mining Pools]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folien 24, 25
- Externe Datenquelle: https://digiconomist.net/bitcoin-energy-consumption
