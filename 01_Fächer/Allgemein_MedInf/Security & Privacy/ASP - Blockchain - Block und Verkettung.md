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

# ASP - Blockchain - Block und kryptografische Verkettung

> [!info] Kurzdefinition
> Eine Blockchain ist eine kryptografisch verkettete Liste von Blöcken. Jeder Block enthält Hash dieses Blocks, Hash des Vorgänger-Blocks, Nonce und Transaktionen (mit Signaturen + Public Keys). Die Verkettung über die Hashes macht die Kette manipulationssicher.

## Beschreibung

Folie 25 zeigt den **Block-Aufbau**:

| Feld | Beispielwert (Folie 25) |
|---|---|
| Hash-Wert Block n | `00000aacf2d35b5` |
| Hash-Wert Block n-1 | `00000b14db12fd1` |
| Nonce | `5975ftghfd` |
| Transaktionen | Transaktion 1–n |
| Digitale Signaturen | Signatur 1–n |
| Public Keys | Public Key 1–n |

**Eigenschaften (Folie 25):**
- Transaktionen werden in Blöcken zusammengefasst (z. B. alle 10 Minuten).
- Blöcke fungieren als **Container**, die folgendes beinhalten:
  - Hash-Wert, der den Block eindeutig repräsentiert
  - Hash-Wert des vorhergehenden Blocks
  - Gefundene Nonce und Transaktionen
  - Digitale Signaturen und öffentliche Schlüssel zur Prüfung der Signaturen der Transaktionen

**Prinzip der Blockchain (Folie 26):** Kryptografische Verkettung von Blöcken mittels Hash-Funktion:

```
Hash(Hash-Wert Block n-1 + Nonce + Transaktionen + Block-Header-Metadaten) = Hash-Wert Block n
```

Damit zeigt jeder Block über das Feld „Hash-Wert Block n-1" auf seinen Vorgänger. Eine Manipulation an einem alten Block würde dessen Hash ändern und die gesamte nachfolgende Kette ungültig machen – jeder einzelne nachfolgende PoW-Wert müsste neu berechnet werden, was praktisch unmöglich ist.

## Bestandteile / Aufbau

| Block-Feld | Funktion |
|---|---|
| Hash-Wert Block n | Identifikator dieses Blocks; das, was der nächste Block als „Vorgänger-Hash" speichert |
| Hash-Wert Block n-1 | Verkettung zur vorhergehenden Block, macht Tampering teuer |
| Nonce | Lösung des PoW-Rätsels |
| Transaktionen | Inhaltliche Nutzdaten |
| Signaturen + Public Keys | ermöglichen Verifizierung der Transaktionen |

## Beispiel

Block n hat Hash `00000aacf2d35b5`. Block n+1 trägt im Feld „Hash-Wert Block n" eben diesen Wert (Folie 26 zeigt das explizit). Wer Block n manipuliert, ändert dessen Hash und müsste Block n+1, n+2, … alle neu rechnen.

## Abgrenzung

- **Block-Hash ≠ Hash der Transaktionen:** Der Block-Hash bezieht den Vorgänger-Hash, die Nonce und alle Transaktionen ein.
- **Verkettung ≠ verteilte Speicherung:** Die kryptografische Verkettung schützt vor Manipulation, die verteilte Speicherung schützt vor Single Point of Failure. Beides ist orthogonal nötig.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Felder enthält ein Block, und wie sind Blöcke verkettet?

**Anwendungsfrage:** Skizzieren Sie die Hash-Verkettung an einem Beispiel mit zwei Blöcken. Was passiert, wenn jemand Block n-1 manipuliert?

**Diskussionsfrage:** Warum macht die Kombination aus Hash-Verkettung und PoW eine Manipulation praktisch unmöglich? (Antwort: Manipulation an Block X erfordert das Neu-Rechnen aller PoW-Rätsel von X, X+1, …, was bei einer aktiven Kette eine Mehrheit der globalen Hash-Rate voraussetzt – siehe 51-%-Attack.)

**Mögliche Anschlussfragen:**
- Welche Hash-Funktion verwendet Bitcoin? (SHA-256, doppelt – im PDF nicht spezifiziert.)
- Wozu sind die Public Keys im Block gespeichert? (Zur Signatur-Prüfung der enthaltenen Transaktionen.)
- Wie groß ist ein typischer Bitcoin-Block? (1 MB oder mehr – im PDF nicht ausgewiesen.)

## Verwandt

- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Distributed Ledger]]
- [[ASP - Blockchain - Eigenschaften und Vorteile]]
- [[ASP - Blockchain - Zeitstempel-Service]]
- [[ASP - Hash - Funktion]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folien 25, 26
