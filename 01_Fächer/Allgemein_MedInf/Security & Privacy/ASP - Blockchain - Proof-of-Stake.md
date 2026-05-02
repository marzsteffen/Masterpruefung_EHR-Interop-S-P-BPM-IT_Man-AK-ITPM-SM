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

# ASP - Blockchain - Proof-of-Stake (PoS)

> [!info] Kurzdefinition
> Konsens-Mechanismus, bei dem Validatoren (statt Miner) zufällig ausgewählt werden. Zur Teilnahme hinterlegen sie eine Kaution (Stake); ehrliches Verhalten wird belohnt, Manipulation kostet die Kaution.

## Beschreibung

Folie 28 erläutert PoS:

- **Validators (Überprüfende Parteien)** werden anstatt Miner eingesetzt und **zufällig ausgewählt**.
- Validators hinterlegen eine **Kaution (Deposit)**.
- Diese Kaution wird als **Stake** bezeichnet.
- **Erhöhung der Chance, ausgewählt zu werden, durch Hinterlegung höherer Stakes.**
- **Ehrliches Verhalten** einer Partei (richtige Berechnung) wird belohnt.
- **Schädliches Verhalten** (z. B. Manipulation) führt zu einem **Verlust des Stakes**.

**Kerngedanke:** Statt Energie (PoW) wird Kapital eingesetzt. Wer manipuliert, verliert sein Geld. Damit entsteht ein wirtschaftlicher Anreiz für Ehrlichkeit, ohne Hash-Rätsel rechnen zu müssen.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Validator | übernimmt die Rolle des Miners |
| Stake | hinterlegte Kaution in Kryptowährung |
| Auswahl | zufällig, gewichtet mit der Stake-Höhe |
| Belohnung | für ehrliche Validierung |
| Slashing | Verlust des Stakes bei Manipulation |

## Beispiel

Aus Folie 28: Validator hinterlegt einen Stake. Wird er vom Protokoll ausgewählt, führt er die Validierung durch und erhält eine Belohnung. Manipuliert er, verliert er seinen Stake.

## Abgrenzung

- **PoS vs. [[ASP - Blockchain - Proof-of-Work]]:** PoW kostet Energie, PoS kostet eingesetztes Kapital. PoS ist deutlich energieeffizienter.
- **PoS hat eigene Schwächen** (im PDF nicht behandelt): „Nothing-at-Stake"-Problem, „Long-Range-Attacks", potenzielle Konzentration bei wenigen großen Stake-Haltern (Ethereum-Foundation-Kritik).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Proof-of-Stake, und wie unterscheidet es sich von Proof-of-Work?

**Anwendungsfrage:** Welche Anreize lenken einen Validator zu ehrlichem Verhalten? Was passiert bei Manipulation?

**Diskussionsfrage:** Welche Vor- und Nachteile hat PoS gegenüber PoW – und welche neuen Schwächen ergeben sich aus der Kapitalbindung? (Energieeffizienz vs. Kapitalkonzentration.) Warum ist PoS heute der bevorzugte Ansatz für neue Blockchains? (Stichwort: Ethereum-Wechsel von PoW zu PoS, „The Merge" 2022 – im PDF nicht behandelt.)

**Mögliche Anschlussfragen:**
- Was ist „Slashing"? (Verlust des Stakes bei Manipulation – im PDF nur indirekt erwähnt.)
- Welche Variante davon ist „Delegated Proof-of-Stake"? ([[ASP - Blockchain - Weitere Konsensus-Protokolle]])
- Welche aktuelle Blockchain nutzt PoS? (Ethereum seit 2022; Cardano, Solana etc. – im PDF nicht erwähnt.)

## Verwandt

- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Weitere Konsensus-Protokolle]]
- [[ASP - Blockchain - Kritik PoW]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 28
