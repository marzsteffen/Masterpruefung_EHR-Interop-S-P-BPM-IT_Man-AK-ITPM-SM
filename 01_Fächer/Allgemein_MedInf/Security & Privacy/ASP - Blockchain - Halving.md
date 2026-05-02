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

# ASP - Blockchain - Halving und begrenzte Bitcoin-Anzahl

> [!info] Kurzdefinition
> Im Bitcoin-Protokoll halbiert sich die Block-Belohnung alle 210 000 Blöcke (≈ 4 Jahre). Dadurch konvergiert die Gesamtzahl jemals erzeugter Bitcoins asymptotisch gegen den Höchstwert von 21 Millionen.

## Beschreibung

Folie 22:

- **Bitcoin-Protokoll:** Alle 210 000 Blöcke wird die Belohnung halbiert (**Halving**), also ca. alle 4 Jahre.
- Durch die Halbierung der Belohnung wird die Anzahl der neu geschaffenen Bitcoins pro Block kontinuierlich reduziert.
- Mit jeder Halbierung nähert sich die Gesamtmenge an geschaffenen Bitcoins asymptotisch dem **Höchstwert von 21 Millionen** an.

**Halving-Tabelle (Folie 22):**

| Jahr | Belohnung pro Block |
|---|---|
| 2008 | 50 Bitcoins |
| 2012 | 25 Bitcoins |
| 2016 | 12,5 Bitcoins |
| 2020 | 6,25 Bitcoins |
| 2024 | 3,125 Bitcoins |
| 20.. | ~ 0 Bitcoins |

## Bestandteile / Aufbau

| Element | Wert |
|---|---|
| Halving-Zyklus | alle 210 000 Blöcke (≈ 4 Jahre) |
| Initial-Reward | 50 BTC pro Block |
| Asymptote | 21 Mio. Bitcoins (geometrische Reihe) |

## Beispiel

Direkt aus der Tabelle Folie 22.

## Abgrenzung

- **Halving regelt nur den Block-Reward**, nicht die Transaktionsgebühren. Sobald der Reward gegen Null geht, finanzieren sich Miner ausschließlich aus Transaktionsgebühren. *Im PDF nicht ausgeführt.*
- **Andere Kryptowährungen** haben andere Belohnungs-/Inflationsmodelle (z. B. Ethereum hat keinen festen Cap, *im PDF nicht detailliert*).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Halving, und was ist der Höchstwert an Bitcoins?

**Anwendungsfrage:** Erklären Sie, wie aus dem Halving-Mechanismus der Höchstwert von 21 Millionen Bitcoins folgt. (Geometrische Reihe: 50 + 25 + 12,5 + … pro 210 000 Blöcken.)

**Diskussionsfrage:** Welche Auswirkungen hat das Halving auf die Wirtschaftlichkeit von Mining? Was passiert, wenn der Block-Reward gegen Null geht? (Miner werden auf Transaktionsgebühren angewiesen sein – wirtschaftlich kritisch.)

**Mögliche Anschlussfragen:**
- Wann findet das nächste Halving statt? (Etwa 2028.)
- Warum wurde der Cap von 21 Millionen gewählt? (Designentscheidung Nakamotos – im PDF nicht weiter diskutiert.)
- Was sind die wirtschaftlichen Implikationen einer deflationären Währung?

## Verwandt

- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Bitcoin Grundlagen]]
- [[ASP - Blockchain - Mining Pools]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 22
