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

# ASP - Blockchain - Bitcoin Grundlagen

> [!info] Kurzdefinition
> 2008 von Satoshi Nakamoto vorgestellte dezentrale digitale Währung auf Blockchain-Basis. Erster und bis heute populärster Anwendungsfall der Blockchain. Kein zentraler Validierer.

## Beschreibung

Folie 12 stellt Bitcoin vor:

- Die Idee einer **kryptografischen Verkettung** wurde 2008 von **Satoshi Nakamoto** adaptiert.
- Der Bitcoin war der erste – und ist bis heute der populärste – Anwendungsfall der Blockchain.
- **Dezentralisierte digitale Währung**, die auf einer Blockchain-Technologie basiert.
- Im Bitcoin-Netzwerk gibt es **keine zentrale Stelle**, die die Überprüfung der Transaktionen vornimmt.

Damit löst Bitcoin den letzten verbleibenden Schwachpunkt der Haber/Stornetta-Vorform: die zentrale Trusted Authority. Ersetzt wird sie durch das **Distributed Ledger** ([[ASP - Blockchain - Distributed Ledger]]) und ein **Konsens-Protokoll** ([[ASP - Blockchain - Proof-of-Work]]).

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Erfinder/Pseudonym | Satoshi Nakamoto |
| Jahr | 2008 (Whitepaper „Bitcoin: A Peer-to-Peer Electronic Cash System") |
| Charakter | dezentrale digitale Währung |
| Technologie | Blockchain |
| Zentrale Stelle | keine |

## Beispiel

Praktisch: Alice will Bob 0,5 BTC schicken. Sie signiert die Transaktion mit ihrem Private Key, schickt sie ans Netzwerk, Miner sammeln die Transaktion, packen sie in einen Block, lösen das PoW-Rätsel, und nach Konsens ist die Transaktion bestätigt. Kein Zwischeninstitut, keine Bank.

## Abgrenzung

- **Bitcoin ≠ Blockchain:** Bitcoin ist ein konkreter Anwendungsfall der Blockchain. Die Blockchain ist die zugrunde liegende Technik.
- **Bitcoin vs. Ethereum:** Ethereum ist eine andere Blockchain mit Smart-Contract-Funktionalität (siehe [[ASP - Blockchain - Anwendungen]]).
- **Bitcoin vs. klassische Währung:** Klassisch: Banken/Zentralbanken als vertrauenswürdige Dritte. Bitcoin: keine.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Bitcoin, wer hat es erfunden, und wann?

**Anwendungsfrage:** Welche Probleme der zentralen Zeitstempel-Lösung löst Bitcoin? Welche Krypto-Bausteine sind notwendig?

**Diskussionsfrage:** „Bitcoin ist nicht dezentral, sondern es gibt heute Mining-Pool-Konzentration." Diskutieren Sie diese Behauptung. (Stichwort: Mehrheit der Hash-Rate liegt bei wenigen Pools – realer Risikoaspekt, *im PDF nur in der Mining-Pool-Folie angedeutet*.)

**Mögliche Anschlussfragen:**
- Was ist ein Distributed Ledger?
- Was ist Proof-of-Work?
- Wie viele Bitcoins gibt es maximal? (21 Mio. – siehe [[ASP - Blockchain - Halving]].)

## Verwandt

- [[ASP - Blockchain - Zeitstempel-Service]]
- [[ASP - Blockchain - Distributed Ledger]]
- [[ASP - Blockchain - Bitcoin Funktionsweise]]
- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Halving]]
- [[ASP - Blockchain - Anwendungen]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 12
