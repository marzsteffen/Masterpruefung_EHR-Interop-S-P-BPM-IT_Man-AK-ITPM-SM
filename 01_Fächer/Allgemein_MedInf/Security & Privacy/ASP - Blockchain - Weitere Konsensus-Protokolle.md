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

# ASP - Blockchain - Weitere Konsensus-Protokolle (DPoS, PoA, PoI, PoET)

> [!info] Kurzdefinition
> Vier weitere Konsens-Protokolle jenseits von Proof-of-Work und Proof-of-Stake: Delegated Proof-of-Stake (gewählte Validatoren), Proof-of-Authority (autorisierte Authorities), Proof-of-Identity (autorisierte Identitäten) und Proof-of-Elapsed-Time (zufällige Wartezeit).

## Beschreibung

Folie 29 listet vier weitere Protokolle.

### Delegated Proof-of-Stake (DPoS)
- **Keine zufällige, sondern explizite Auswahl von Validatoren (Nodes).**
- Stake-Halter wählen die Validatoren – ähnlich wie repräsentative Demokratie.

### Proof-of-Authority (PoA)
- **Autorisierte Nodes werden als Authority bezeichnet.**
- **Authorities müssen einen Konsens erreichen.**
- Vertrauen wird auf eine kleine Gruppe vorab autorisierter Knoten konzentriert.

### Proof-of-Identity (PoI)
- **Autorisierte Identitäten haben zusätzliche Befugnisse.**
- **Die Auswahl dieser Identitäten stellt ein Problem dar (Vertrauen).**

### Proof-of-Elapsed-Time (PoET)
- **Jeder Node muss eine zufällig bestimmte Zeitspanne warten.**
- **Nach Ablauf dieser Zeit erhält der erste Node mit der richtigen Berechnung die Belohnung (Reward).**
- Idee: Energie-Sparen durch faire Wartezeit-Verteilung statt Hash-Rennen.

## Bestandteile / Aufbau

| Protokoll | Auswahl-Mechanismus | Vertrauensbasis |
|---|---|---|
| DPoS | gewählt durch Stake-Halter | Reputation der gewählten Validatoren |
| PoA | feste Liste autorisierter Authorities | externe Autorisierung |
| PoI | feste Liste autorisierter Identitäten | externe Autorisierung |
| PoET | zufällige Wartezeit | sichere Hardware (Trusted Execution Environment) |

## Beispiel

*Im PDF nicht ausgeführt.* Praxis: PoA wird in privaten Konsortium-Blockchains eingesetzt (z. B. Hyperledger Besu); PoET ist Teil von Hyperledger Sawtooth und nutzt Intel SGX.

## Abgrenzung

- **DPoS, PoA, PoI** geben Dezentralität teilweise auf zugunsten von Effizienz und Skalierbarkeit.
- **PoET** kombiniert PoW-ähnliche Lotterie mit Energie-Effizienz.
- **Im PDF wenig Tiefe** – die Folie nennt jedes Protokoll mit ein bis zwei Sätzen, ohne Vor- und Nachteile zu vergleichen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Konsens-Protokolle gibt es jenseits PoW und PoS, und wie funktionieren sie kurz?

**Anwendungsfrage:** In welchen Anwendungsfällen wäre PoA gegenüber PoW oder PoS sinnvoll? (Konsortium-Blockchain mit bekannten Teilnehmern, z. B. ein Verbund von Krankenhäusern.)

**Diskussionsfrage:** Welche dieser Protokolle bewahren Dezentralität, welche opfern sie zugunsten von Effizienz? (DPoS/PoA/PoI sind weniger dezentral; PoET ist es eher.) Welcher Trade-off besteht jeweils?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen PoA und PoI?
- Welche Hardware-Voraussetzung hat PoET? (Trusted Execution Environment / SGX – im PDF nicht behandelt.)
- Welches Protokoll passt zu einer öffentlichen Anwendung mit unbekannten Teilnehmern? (PoW oder PoS.)

## Verwandt

- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Proof-of-Stake]]
- [[ASP - Blockchain - Distributed Ledger]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 29
