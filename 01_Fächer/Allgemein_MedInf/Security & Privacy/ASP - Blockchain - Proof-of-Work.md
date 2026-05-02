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

# ASP - Blockchain - Proof-of-Work (PoW)

> [!info] Kurzdefinition
> Konsens-Mechanismus, bei dem Miner ein mathematisches Hash-Rätsel lösen, indem sie eine Nonce so lange variieren, bis der Hash über Block + Nonce vorgegebene Kriterien (Leading Zeros) erfüllt. Der erste erfolgreiche Miner darf den Block hinzufügen und erhält eine Belohnung.

## Beschreibung

Folien 16, 18, 19, 20 erläutern PoW.

**Mathematisches Rätsel (Folie 18):**
- Der Miner muss einen Wert namens **Nonce** finden, der zusammen mit den Transaktionsdaten einen Hashwert ergibt, der bestimmte Kriterien erfüllt.
- **Kriterien:**
  - **Leading Zero Target:** Der Hashwert muss mit einer bestimmten Anzahl an „0" starten (z. B. `0000000EZ793BDJAK896…`).
  - **Nonce-Wert im Zielbereich:** Der Hashwert muss in einem bestimmten Bereich liegen, der durch den Nonce-Wert bestimmt wird.

**Konsens-Protokoll (Folie 19):**
- Sobald ein Miner einen gültigen Hashwert gefunden hat, sendet er den neuen Block mit dem gefundenen Nonce an das Netzwerk.
- **Andere Knoten (Nodes) überprüfen**, indem sie den Ziel-Hash-Wert mit der gefundenen Nonce selbst berechnen und sicherstellen, dass der Hashwert die festgelegten Kriterien erfüllt.
- Auch die Transaktionen selbst werden von den Nodes überprüft.

**Asymmetrie:** Eine Lösung zu **finden** ist rechenintensiv (probabilistisches Brute-Force). Eine Lösung zu **verifizieren** ist trivial (eine Hash-Berechnung).

**Belohnung / Reward (Folie 20):**
- Der erfolgreiche Miner erhält neue Kryptowährungseinheiten (Bitcoin) als Belohnung.
- Diese Belohnung dient als **Anreiz**, Rechenleistung bereitzustellen.
- Miner stehen also in einem **Wettbewerb**: Wer findet als Erster die richtige Nonce?

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Eingabe | Block-Header (Hash des Vorgängers, Transaktionen, Metadaten) + Nonce |
| Hash-Funktion | (Bitcoin: SHA-256, doppelt) |
| Kriterium | Leading Zeros / Zielwert |
| Suche | Brute-Force über Nonce |
| Verifikation | einmalige Hash-Berechnung |
| Belohnung | Bitcoin-Reward (siehe [[ASP - Blockchain - Halving]]) |

## Beispiel

Folie 16/18 zeigt einen Block mit `Hash-Wert Block n: 00000aacf2d35b5` – die führenden Nullen sind das Resultat einer erfolgreichen PoW-Suche. Der Vergleich der gefundenen Nonce mit den Block-Daten muss bei allen Nodes denselben Hash ergeben.

## Abgrenzung

- **PoW vs. [[ASP - Blockchain - Proof-of-Stake]]:** PoW löst Konsens durch *Rechenarbeit*, PoS durch *Kapitaleinsatz*. PoW ist energieintensiv ([[ASP - Blockchain - Kritik PoW]]).
- **PoW-Rätsel löst zwei Probleme gleichzeitig:** Konsens (wer darf den nächsten Block schreiben?) und Manipulationsschutz (eine Manipulation bedeutet, alle nachfolgenden PoW-Rätsel neu zu lösen, was praktisch unmöglich ist).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Proof-of-Work, und wie funktioniert das mathematische Rätsel?

**Anwendungsfrage:** Skizzieren Sie den Ablauf: Wer berechnet was, wer verifiziert was, wer bekommt die Belohnung?

**Diskussionsfrage:** Warum ist PoW gleichzeitig Konsens-Mechanismus und Manipulationsschutz? Welche Schwäche zeigt sich bei einer 51-%-Attack? (Wer mehr als 51 % der Hash-Rate kontrolliert, kann die Kette neu schreiben – im PDF nicht direkt erwähnt.)

**Mögliche Anschlussfragen:**
- Wie unterscheidet sich „Lösung finden" von „Lösung verifizieren"?
- Was ist der Reward, und wie ändert er sich über die Zeit?
- Welche Hash-Funktion verwendet Bitcoin? (SHA-256 doppelt – im PDF nicht spezifiziert.)
- Welche Kritik gibt es an PoW? ([[ASP - Blockchain - Kritik PoW]])

## Verwandt

- [[ASP - Blockchain - Bitcoin Funktionsweise]]
- [[ASP - Blockchain - Mining Pools]]
- [[ASP - Blockchain - Halving]]
- [[ASP - Blockchain - Proof-of-Stake]]
- [[ASP - Blockchain - Kritik PoW]]
- [[ASP - Hash - Funktion]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folien 16, 18, 19, 20
