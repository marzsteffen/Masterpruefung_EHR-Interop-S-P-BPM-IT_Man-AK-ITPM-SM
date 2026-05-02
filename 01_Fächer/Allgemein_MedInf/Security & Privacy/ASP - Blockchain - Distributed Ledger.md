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

# ASP - Blockchain - Distributed Ledger

> [!info] Kurzdefinition
> Verteilte Datenbank, die auf mehreren Knoten (Nodes) im Netzwerk gespeichert ist. Statt einer einzigen zentralen Authority wird die Datensicherheit durch Replikation auf vielen Knoten gewährleistet, die per Konsens synchron gehalten werden.

## Beschreibung

Folie 14 erläutert das Konzept:

- **Verteilte Datenbank**, die auf mehreren Knotenpunkten (Nodes) gespeichert ist.
- Bei Bitcoin: Aufzeichnung von Daten einer **Transaktionshistorie** auf dezentralen Nodes.
- **Node** bezieht sich auf einen Computer im Netzwerk, der Transaktionen validiert und aufzeichnet.
- Damit wird sichergestellt, dass die Sicherheit nicht von einer einzigen zentralen Stelle abhängt.
- **Aber:** Es braucht einen **gemeinsamen Konsens** mehrerer Nodes bei Updates der Transaktionshistorie.

**Hinweis aus der Folie:** „Die Datenbanken müssen synchronisiert sein bzw. die gleichen Daten enthalten!"

Das motiviert die Notwendigkeit eines Konsens-Protokolls (siehe [[ASP - Blockchain - Proof-of-Work]] und [[ASP - Blockchain - Proof-of-Stake]]) – ohne zentralen Schiedsrichter braucht es einen mathematischen Mechanismus, der sicherstellt, dass alle Nodes denselben nächsten Block akzeptieren.

## Bestandteile / Aufbau

| Element | Funktion |
|---|---|
| Node | Computer im Netzwerk, validiert und speichert Transaktionen |
| Replizierte Datenbank | jede Node hat dieselbe Kopie der Transaktionshistorie |
| Synchronisation | Nodes tauschen Updates aus, müssen denselben Stand haben |
| Konsens-Protokoll | Einigt Nodes auf den nächsten gültigen Block |

## Beispiel

Bitcoin: Tausende Nodes weltweit, jeder mit einer vollständigen Kopie der Blockchain. Eine neue Transaktion wird allen Nodes bekanntgegeben; ein Miner schafft den nächsten Block und schickt ihn ans Netzwerk; alle Nodes verifizieren ihn unabhängig und übernehmen ihn in ihre Kopie.

## Abgrenzung

- **Distributed Ledger ≠ Blockchain:** Blockchain ist eine spezifische Form von DLT mit kryptografisch verketteten Blöcken. Es gibt auch andere DLTs (z. B. Hashgraph, IOTA Tangle), die *im PDF nicht behandelt werden*.
- **Replikation ohne Konsens** (klassische DB-Cluster) reicht nicht, weil Angreifer in einer feindlichen Umgebung gezielt manipulieren könnten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Distributed Ledger, und warum braucht es einen Konsens-Mechanismus?

**Anwendungsfrage:** Beschreiben Sie an Bitcoin, wie ein Distributed Ledger den Single Point of Failure einer zentralen Datenbank ersetzt.

**Diskussionsfrage:** Welche Skalierungs- und Konsistenz-Probleme entstehen aus einer verteilten Datenbank? (Stichwort: CAP-Theorem – im PDF nicht erwähnt; Synchronisations-Latenz, Partition-Risiken.)

**Mögliche Anschlussfragen:**
- Welche Konsens-Protokolle gibt es?
- Wie wird verhindert, dass ein bösartiger Node falsche Daten verbreitet? (Konsens, kryptografische Verkettung.)
- Was passiert bei einem temporären Netzwerk-Split (Fork)?

## Verwandt

- [[ASP - Blockchain - Bitcoin Grundlagen]]
- [[ASP - Blockchain - Block und Verkettung]]
- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Proof-of-Stake]]
- [[ASP - Blockchain - Eigenschaften und Vorteile]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folie 14
