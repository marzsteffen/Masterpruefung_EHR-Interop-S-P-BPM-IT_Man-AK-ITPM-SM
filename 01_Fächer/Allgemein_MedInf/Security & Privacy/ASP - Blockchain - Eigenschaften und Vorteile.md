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

# ASP - Blockchain - Eigenschaften und Vorteile

> [!info] Kurzdefinition
> Drei strukturelle Eigenschaften (verteilt, unveränderbar, append-only) und mehrere daraus abgeleitete Vorteile (Transparenz, Authentizität, kein Single Point of Failure, keine zentrale Trust-Authority).

## Beschreibung

Folie 26 (zweite Block-Verkettungs-Folie) listet die strukturellen Eigenschaften und Vorteile.

**Eigenschaften:**
- **Verteilt (dezentral):** Daten liegen replizert auf vielen Nodes.
- **Unveränderbar:** Bestehende Blöcke können nachträglich nicht geändert werden, ohne die Kette zu invalidieren.
- **Nur ein „Anhängen" von Einträgen (Append-Only):** Neue Daten kommen nur am Ende der Kette dazu.

**Vorteile:**
- **Erhöhte Transparenz:** Alle Transaktionen sind in der Kette nachvollziehbar.
- **Authentizität und Überprüfbarkeit:** Über Signaturen und Hash-Verkettung jederzeit verifizierbar.
- **Kein Single Point of Failure (SPOF) durch Dezentralisierung.**
- **Keine zentrale vertrauenswürdige Partei mehr notwendig:**
  - Keine Konzentration der Macht.
  - Keine Vertrauensprobleme.

## Bestandteile / Aufbau

| Eigenschaft | Was bedeutet das praktisch? |
|---|---|
| Verteilt | viele Nodes mit identischer Kopie |
| Unveränderbar | Hash-Verkettung + PoW machen Manipulation extrem teuer |
| Append-Only | nur neue Blöcke werden angehängt |
| Transparent | jeder kann die Kette einsehen (in öffentlichen Blockchains) |
| Authentizität | Transaktionen sind signiert |
| Kein SPOF | Ausfall einzelner Nodes hat keine Folgen |
| Keine Trust Authority | Vertrauen wird durch Krypto + Konsens ersetzt |

## Beispiel

Der Bitcoin-Ledger ist seit 2009 öffentlich einsehbar. Jede Transaktion seit dem Genesis-Block kann verifiziert werden – ohne dass irgendeine zentrale Stelle befragt werden muss. Wer Bitcoin signiert hat, lässt sich kryptografisch beweisen.

## Abgrenzung

- **Vorteile gelten primär für öffentliche Blockchains.** Private/permissioned Blockchains (z. B. Hyperledger) haben eingeschränktere Transparenz und nutzen meist andere Konsens-Protokolle. *Im PDF nicht ausgeführt.*
- **„Unveränderbar" ist nicht absolut**, sondern an die Annahme gebunden, dass keine Mehrheit der Hash-Rate / des Stakes bösartig agiert.
- **„Keine Trust Authority"** stimmt für das Protokoll, aber nicht zwangsläufig für Sekundär-Infrastrukturen wie Wallets, Exchanges oder Wallet-Software.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche strukturellen Eigenschaften und welche Vorteile hat eine Blockchain?

**Anwendungsfrage:** Welche dieser Eigenschaften sind für Ihren konkreten eHealth-Use-Case relevant – und welche eher nicht? (Beispiel: Audit-Trails profitieren von Append-Only und Unveränderbarkeit; aber Patientendaten direkt in einer öffentlichen Blockchain wäre DSGVO-problematisch wegen Transparenz.)

**Diskussionsfrage:** „Blockchain ist nicht für jedes Problem die Lösung." Diskutieren Sie diese Aussage mit Bezug auf die Eigenschaften. Welche Probleme entstehen, wenn personenbezogene Daten in einer öffentlichen Blockchain liegen? (DSGVO-Speicherbegrenzung kollidiert mit Append-Only / Unveränderbarkeit.)

**Mögliche Anschlussfragen:**
- Wie hängt „kein SPOF" mit dem Distributed Ledger zusammen?
- Welche Vorteile bringt eine Blockchain gegenüber einer klassischen verteilten Datenbank konkret?
- Wie löst man das DSGVO-„Recht auf Vergessenwerden" in einer unveränderbaren Kette? (Off-chain speichern, On-chain nur Hashes – im PDF nicht behandelt.)

## Verwandt

- [[ASP - Blockchain - Distributed Ledger]]
- [[ASP - Blockchain - Block und Verkettung]]
- [[ASP - Blockchain - Anwendungen]]
- [[ASP - DSGVO - Grundsaetze]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 26
