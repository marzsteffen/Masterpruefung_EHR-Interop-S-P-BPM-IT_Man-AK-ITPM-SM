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

# ASP - Blockchain - Anwendungen (Krypto, Grundbuch, Lieferkette)

> [!info] Kurzdefinition
> Drei Anwendungsfelder der Blockchain laut Vorlesung: Kryptowährungen (Bitcoin, Ethereum), staatliches Grundbuch (Estland, Kanada), Lieferketten-Tracking.

## Beschreibung

Folien 31–33 stellen drei Anwendungsfelder vor.

### Kryptowährungen (Folie 31)

**Bitcoin:**
- Transaktionen werden in Blocks gebündelt.
- Blocks entstehen durch Mining.
- Konkurrierende Miner versuchen, die Belohnung zu erhalten.

**Ethereum:**
- Ähnlich zu Bitcoin.
- Bietet eine Plattform für **verteilte Berechnungen**.
- Hat **Smart Contracts** eingeführt.

### Grundbuch (Folie 32)

- **Proof-of-Concepts in vielen Ländern** wie Kanada, Estland, etc.
- Die Nodes eines Netzwerkes werden von der **Regierung betrieben**.
- Transaktion beschreibt den **Eigentumsübergang**.
- Transparenz bei allen Transaktionen.

### Lieferkette (Folie 33)

- Akteure entlang der Kette: **Bauer → Industrie → Transport → Lebensmittelmarkt → Kunde**.
- Jeder Übergang wird als Transaktion in der Blockchain dokumentiert.
- Endkunde kann den gesamten Weg nachvollziehen (z. B. „Ist mein Steak wirklich von dieser Region?").

## Bestandteile / Aufbau

| Anwendungsfeld | Akteure / Konsens | Kerngedanke |
|---|---|---|
| Bitcoin | öffentlich, PoW | dezentrale Währung |
| Ethereum | öffentlich, früher PoW, jetzt PoS | Plattform + Smart Contracts |
| Grundbuch | staatlich, PoA-artig | manipulationssichere Eigentumsübergänge |
| Lieferkette | konsortial, oft PoA | Herkunfts-/Wegnachweis |

## Beispiel

Aus Folie 33: Bauer schickt Milch an Industrie → Industrie an Transport → Transport an Lebensmittelmarkt → Markt an Kunde. Jede Übergabe wird als Transaktion in der Blockchain festgehalten; der Kunde kann mit einem QR-Code die gesamte Kette einsehen.

## Abgrenzung

- **Kryptowährungen** sind der originäre Anwendungsfall, aber bei Weitem nicht der einzige.
- **Smart Contracts (Ethereum)** erweitern Blockchains zu programmierbaren Plattformen – nicht alle Blockchains unterstützen das.
- **Anwendungen außerhalb Krypto** brauchen meist andere Konsens-Protokolle (PoA, DPoS), weil Anonymität nicht das Ziel ist und Energieverbrauch ein Problem darstellt.
- **eHealth-Anwendungen sind im PDF nicht erwähnt.** In der Praxis gibt es Initiativen (Verschreibungen, Patientenakten), aber die DSGVO-Konflikte mit Append-Only sind ein offenes Problem.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Anwendungsfelder der Blockchain nennt die Vorlesung?

**Anwendungsfrage:** Beschreiben Sie konkret den Lieferketten-Use-Case. Welche Transaktionen werden geschrieben, welche Akteure sind Nodes?

**Diskussionsfrage:** Wäre Blockchain für ein eHealth-Szenario wie Patientenakten sinnvoll? Diskutieren Sie Pro/Contra mit Bezug auf die [[ASP - Blockchain - Eigenschaften und Vorteile]] und die DSGVO. (Stichworte: Append-Only widerspricht Recht auf Vergessenwerden; öffentliche Lesbarkeit problematisch; vermutlich besser: Hashes on-chain, Daten off-chain.) Was sind Smart Contracts, und welche Risiken bringen sie?

**Mögliche Anschlussfragen:**
- Welcher Konsens-Mechanismus passt zu welchem Anwendungsfeld? (Krypto: PoW/PoS; Grundbuch/Lieferkette: PoA.)
- Was ist ein Smart Contract konkret? (*Im PDF nicht definiert.*)
- Welche eHealth-Anwendungen wären realistisch? (Verschreibungen, Audit-Trails, Einwilligungs-Tracking.)

## Verwandt

- [[ASP - Blockchain - Bitcoin Grundlagen]]
- [[ASP - Blockchain - Eigenschaften und Vorteile]]
- [[ASP - Blockchain - Weitere Konsensus-Protokolle]]
- [[ASP - DSGVO - Grundsaetze]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folien 31, 32, 33
