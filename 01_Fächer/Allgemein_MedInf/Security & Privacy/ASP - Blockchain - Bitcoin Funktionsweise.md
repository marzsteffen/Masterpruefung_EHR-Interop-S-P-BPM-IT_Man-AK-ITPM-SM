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

# ASP - Blockchain - Bitcoin Funktionsweise (Transaktionsablauf)

> [!info] Kurzdefinition
> Benutzer signieren Transaktionen mit ihrem Wallet-Schlüssel und schicken sie ans Netzwerk. Miner sammeln offene Transaktionen aus einem gemeinsamen Pool, fassen sie zu einem Block zusammen und konkurrieren via Proof-of-Work darum, den nächsten Block hinzuzufügen.

## Beschreibung

Folie 17 zeigt den dreischrittigen Ablauf:

1. **Benutzer (Kunden, die mit Bitcoin bezahlen) senden Transaktionen** an das Bitcoin-Netzwerk. Jede Transaktion wird mit dem **Private Key** des Senders aus seiner Bitcoin-Wallet signiert.
2. **Diese Transaktionen werden in einem Pool / einer Warteschlange** zusammengefasst (Mempool).
3. **Miner sammeln eine Gruppe von Transaktionen aus dem Pool** und erstellen daraus einen neuen Block.

**Wallet (Folie 17):** Software/Hardware, die das asymmetrische Schlüsselpaar des Benutzers verwaltet. Der **Public Key** dient als Adresse, der **Private Key** zum Signieren.

Anschließend versucht der Miner, das Proof-of-Work-Rätsel zu lösen (siehe [[ASP - Blockchain - Proof-of-Work]]). Sobald er erfolgreich ist, sendet er den Block ans Netzwerk; die anderen Nodes verifizieren in Sekunden, indem sie den gefundenen Nonce-Wert in die Hash-Berechnung einsetzen und prüfen, ob das Ergebnis die Kriterien erfüllt.

## Bestandteile / Aufbau

| Akteur | Rolle |
|---|---|
| Benutzer / Wallet | erstellt und signiert Transaktion |
| Mempool / Transaktions-Pool | zentrale Warteschlange offener Transaktionen |
| Miner | wählen Transaktionen aus, bilden einen Block, lösen PoW-Rätsel |
| Übrige Nodes | verifizieren den Block und übernehmen ihn |

## Beispiel

Aus Folie 17: Bob möchte Alice 0,5 BTC schicken. Bobs Wallet erstellt eine Transaktion, signiert sie mit Bobs Private Key, schickt sie ans Netzwerk. Der Bitcoin-Miner sammelt diese und andere Transaktionen aus dem Pool und beginnt einen neuen Block n zu bauen.

## Abgrenzung

- **Transaktion ≠ Block:** Eine Transaktion ist eine einzelne Wertübertragung. Ein Block fasst typisch hunderte bis tausende Transaktionen zusammen.
- **Pool ≠ Distributed Ledger:** Der Pool enthält *unbestätigte* Transaktionen; das Ledger enthält *bestätigte* Transaktionen in geordneten Blöcken.
- **Miner ≠ alle Nodes:** Jeder Miner ist eine Node, aber nicht jede Node mined. Manche Nodes verifizieren nur.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie läuft eine Bitcoin-Transaktion vom Benutzer bis zur Eintragung in die Blockchain ab?

**Anwendungsfrage:** Welche Krypto-Bausteine kommen zum Einsatz, und wofür? (Asymmetrische Krypto: Wallet-Schlüsselpaar, Signatur. Hash: PoW-Rätsel und Block-Verkettung.)

**Diskussionsfrage:** Was passiert, wenn zwei Miner gleichzeitig einen gültigen Block finden? (Fork – im PDF nicht ausgeführt; in der Praxis setzt sich die Kette mit der größten kumulierten Arbeitsleistung durch.)

**Mögliche Anschlussfragen:**
- Was ist eine Wallet?
- Wie schützt die Signatur die Transaktion gegen Manipulation und Impersonation?
- Welche Anreize gibt es für Miner, ehrlich zu rechnen? ([[ASP - Blockchain - Proof-of-Work]] – Reward.)

## Verwandt

- [[ASP - Blockchain - Bitcoin Grundlagen]]
- [[ASP - Blockchain - Distributed Ledger]]
- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Block und Verkettung]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 17
