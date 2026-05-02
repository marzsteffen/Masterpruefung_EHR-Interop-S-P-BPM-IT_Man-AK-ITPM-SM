---
fach: asp
typ: pruefungsfrage
status: offen
niveau: vertiefung
tags:
  - fach/allgemein/asp
  - typ/pruefungsfrage
  - status/offen
---

# ASP - PF - Blockchain Detail

## Kontext

Prüfungskarten für die mündliche Masterprüfung ASP. Thema: Blockchain – historische Entwicklung (Zeitstempel-Service), Distributed Ledger, Block-Aufbau und Verkettung, Proof-of-Work, Proof-of-Stake, Bitcoin (Halving), Energie-Kritik, Eigenschaften/Vorteile, Anwendungen.

**Achtung Honeypot:** Die Verwendung von SHA-256 für Bitcoin PoW ist im PDF **nicht spezifiziert** (nur als Anmerkung in der Konzept-Note vermerkt). Karten, die das erwähnen, sind als `[Ergänzung]` markiert.

## Verlinkte Konzepte

- [[ASP - Blockchain - Zeitstempel-Service]]
- [[ASP - Blockchain - Bitcoin Grundlagen]]
- [[ASP - Blockchain - Distributed Ledger]]
- [[ASP - Blockchain - Bitcoin Funktionsweise]]
- [[ASP - Blockchain - Block und Verkettung]]
- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Proof-of-Stake]]
- [[ASP - Blockchain - Halving]]
- [[ASP - Blockchain - Kritik PoW]]
- [[ASP - Blockchain - Mining Pools]]
- [[ASP - Blockchain - Eigenschaften und Vorteile]]
- [[ASP - Blockchain - Weitere Konsensus-Protokolle]]
- [[ASP - Blockchain - Anwendungen]]

---

## Karten

### Definition

Was war das Ursprungsproblem (1989) von Haber/Stornetta, und wie funktioniert ein digitaler Zeitstempel?

?

**Ausgangsproblem (Folie 3):** Mit dem Aufkommen digitaler Dokumente sollte erkennbar sein, ob ein Dokument **authentisch** (vom richtigen Ersteller) und **integer** (unverändert) ist. 1989/91 entwickelten Stuart Haber und W. Scott Stornetta einen Zeitstempel-Service.

**Erstellung eines digitalen Zeitstempels (Folie 4) – 3 Schritte:**
1. Antragsteller schickt Dokument an den Aussteller (Trusted Timestamping Authority).
2. Aussteller berechnet den **Hash-Wert** des Dokuments.
3. Aussteller signiert **(Hash-Wert + aktuelle Zeit)** mit seinem Private Key → digitaler Zeitstempel.

**Zeitstempel-Service (Folien 6, 10):** Mehrere Zeitstempel werden zu **Blöcken** zusammengefasst; ein Block-Hash über alle Zeitstempel wird berechnet; Block-Hashes werden kryptografisch verkettet zu einem **finalen Hash**. Dieser wird öffentlich veröffentlicht (z. B. seit 1995 wöchentlich in der **New York Times**, Rubrik „Notices & Lost and Found").

**Schwäche:** Es braucht noch eine **zentrale Trusted Authority** – das löst Bitcoin erst später.

---

Was ist ein Distributed Ledger, und warum ist ein Konsens-Protokoll zwingend notwendig?

?

**Distributed Ledger (Folie 14):** Verteilte Datenbank, die auf mehreren **Knotenpunkten (Nodes)** im Netzwerk gespeichert ist. Jeder Node hat eine identische Kopie der Transaktionshistorie.

- Bei Bitcoin: Aufzeichnung aller Transaktionen auf dezentralen Nodes.
- Damit hängt Sicherheit nicht von einer einzigen zentralen Stelle ab → **kein Single Point of Failure**.

**Warum Konsens nötig ist:** Die Datenbanken müssen synchronisiert sein (identische Daten!). Ohne zentralen Schiedsrichter muss ein **mathematischer Mechanismus** sicherstellen, dass alle Nodes denselben nächsten Block akzeptieren. Ohne Konsens könnte ein bösartiger Node falsche Daten verbreiten.

**Bitcoin löst damit das letzte Problem des Zeitstempel-Service:** Statt einer zentralen Trusted Authority übernehmen alle Nodes gemeinsam via Konsens die Vertrauensfunktion.

---

Welche Felder enthält ein Blockchain-Block, und wie ergibt sich die kryptografische Verkettung?

?

**Block-Aufbau (Folie 25):**

| Feld | Funktion |
|---|---|
| Hash-Wert Block n | Identifikator dieses Blocks |
| Hash-Wert Block n-1 | Verkettung mit dem Vorgänger-Block |
| Nonce | Lösung des PoW-Rätsels |
| Transaktionen | Inhaltliche Nutzdaten |
| Digitale Signaturen | Verifizierung der Transaktionen |
| Public Keys | zur Signatur-Prüfung |

**Verkettungsformel (Folie 26):**
```
Hash(Hash-Wert Block n-1 + Nonce + Transaktionen + Block-Header-Metadaten) = Hash-Wert Block n
```

**Konsequenz:** Wer Block n manipuliert, ändert dessen Hash. Damit wird Block n+1 ungültig (weil er Hash von Block n referenziert). Alle nachfolgenden PoW-Rätsel müssten neu berechnet werden → praktisch unmöglich.

---

Was ist Proof-of-Work (PoW), wie funktioniert das mathematische Rätsel, und wer erhält die Belohnung?

?

**Prinzip (Folie 18):** Miner müssen eine **Nonce** finden, sodass:
```
Hash(Block-Daten + Nonce) → Kriterium erfüllt
```

**Kriterien (Folie 18):**
- **Leading Zero Target:** Hash muss mit einer bestimmten Anzahl „0" beginnen (z. B. `0000000EZ793BDJAK…`)
- Nonce-Wert muss im gültigen Zielbereich liegen

**Ablauf (Folie 19):**
1. Miner sucht per Brute-Force die passende Nonce.
2. Miner sendet Block + Nonce ans Netzwerk.
3. Andere Nodes **verifizieren**: Eine Hash-Berechnung reicht (trivial schnell).
4. Nodes übernehmen den Block in ihre Kopie der Kette.

**Asymmetrie:** Lösung finden = rechenintensiv. Lösung verifizieren = trivial (eine Hash-Berechnung).

**Belohnung (Folie 20):** Erfolgreicher Miner erhält neue **Bitcoin** als Anreiz, Rechenleistung bereitzustellen. Miner stehen im Wettbewerb: Wer findet als Erster die richtige Nonce?

---

### Anwendung

Was sind die Bitcoin-Grunddaten, und wie funktioniert das Halving?

?

**Bitcoin-Grunddaten (Folie 12):**
- Erfunden von **Satoshi Nakamoto** (Pseudonym), 2008
- Erste dezentralisierte digitale Währung auf Blockchain-Basis
- Kein zentrales Prüfinstitut für Transaktionen
- Maximum: **21 Millionen Bitcoins**

**Halving (Folie 22):** Alle **210 000 Blöcke** (≈ 4 Jahre) halbiert sich die Block-Belohnung:

| Jahr | Block-Belohnung |
|---|---|
| 2008 | 50 BTC |
| 2012 | 25 BTC |
| 2016 | 12,5 BTC |
| 2020 | 6,25 BTC |
| 2024 | 3,125 BTC |
| 20.. | ~ 0 BTC |

Durch die Halbierungen nähert sich die Gesamtmenge **asymptotisch** dem Höchstwert von 21 Mio. an (geometrische Reihe).

---

Wie funktioniert Proof-of-Stake (PoS) – und welcher wirtschaftliche Anreiz ersetzt die Rechenarbeit?

?

**Proof-of-Stake (Folie 28):**
- Statt Miner gibt es **Validators**, die zufällig ausgewählt werden.
- Validators hinterlegen eine **Kaution (Stake = Deposit)** in Kryptowährung.
- Höherer Stake → höhere Auswahlwahrscheinlichkeit.

**Anreizstruktur:**
| Verhalten | Konsequenz |
|---|---|
| Ehrliche Validierung | Belohnung |
| Manipulation / schädliches Verhalten | **Verlust des Stakes (Slashing)** |

**Kerngedanke:** Statt Energie wird **Kapital** eingesetzt. Wer manipuliert, verliert sein Geld. Damit entsteht wirtschaftlicher Anreiz für Ehrlichkeit, ohne Hash-Rätsel rechnen zu müssen.

---

Wie konkret sieht die Energie-Kritik an Proof-of-Work aus? Gib die Zahlen aus der Vorlesung an.

?

**Bitcoin Energieverbrauch (Folien 24–25, Quelle: digiconomist.net):**

**Pro Bitcoin-Transaktion:**
| Metrik | Wert | Vergleich |
|---|---|---|
| Elektrische Energie | 737,58 kWh | US-Haushalt über **25,28 Tage** |
| CO₂-Fußabdruck | **411,39 kg CO₂** | entspricht **911 789 VISA-Transaktionen** oder 68 565 h YouTube |
| Elektrogeräte-Müll | 381,30 g | Gewicht von 2,33 iPhones 12 |

**Pro Jahr (Bitcoin gesamt):**
| Metrik | Wert | Vergleich |
|---|---|---|
| Elektrische Energie | **137,68 TWh** | Stromverbrauch der **Ukraine** |
| CO₂-Fußabdruck | 76,79 Mt CO₂ | CO₂ von Oman |
| Elektrogeräte-Müll | 71,18 kt | IT-Abfall der Niederlande |

**Ursache:** Brute-Force-Hashing aller Miner im Wettbewerb → je teurer Bitcoin, desto mehr Hash-Rate, desto mehr Energie.

---

Welche drei Anwendungsfelder der Blockchain nennt die Vorlesung, und wer sind jeweils die Akteure?

?

**1. Kryptowährungen (Folie 31):**
- **Bitcoin:** Transaktionen in Blocks gebündelt, Blöcke durch Mining erzeugt.
- **Ethereum:** Ähnlich Bitcoin, zusätzlich Plattform für **verteilte Berechnungen** und **Smart Contracts**.

**2. Grundbuch (Folie 32):**
- Proof-of-Concepts in Kanada, Estland u. a.
- Nodes werden von der **Regierung** betrieben.
- Transaktionen beschreiben **Eigentumsübergänge** (transparent nachvollziehbar).

**3. Lieferkette (Folie 33):**
- Akteurskette: **Bauer → Industrie → Transport → Lebensmittelmarkt → Kunde**
- Jeder Übergang = eine Transaktion in der Blockchain.
- Endkunde kann den gesamten Weg nachvollziehen (z. B. „Ist mein Steak wirklich von dieser Region?").

---

### Diskussion

Welche drei strukturellen Eigenschaften hat eine Blockchain, und welche Konsequenzen haben sie – positiv wie negativ?

?

**Drei Eigenschaften (Folie 26):**
1. **Verteilt (dezentral):** Daten auf vielen Nodes repliziert.
2. **Unveränderbar:** Bestehende Blöcke können nachträglich nicht geändert werden, ohne die gesamte Kette zu invalidieren.
3. **Append-Only:** Neue Daten kommen nur am Ende hinzu; Löschen ist nicht vorgesehen.

**Daraus abgeleitete Vorteile:**
- Erhöhte Transparenz (alle Transaktionen nachvollziehbar)
- Authentizität und Überprüfbarkeit (Signaturen + Hash-Verkettung)
- Kein Single Point of Failure (Dezentralisierung)
- Keine zentrale vertrauenswürdige Partei nötig

**Kritische Konsequenzen:**
| Eigenschaft | Negativkonsequenz |
|---|---|
| Append-Only | DSGVO-Konflikt: Recht auf Vergessenwerden nicht erfüllbar |
| Transparent (öffentliche Blockchain) | Personenbezogene Daten dürfen nicht direkt gespeichert werden |
| Unveränderbar | Fehler können nicht korrigiert werden |

---

Warum kollidiert die Blockchain-Architektur mit der DSGVO – und wie könnte man den Konflikt lösen?

?

**Hauptkonflikt: Append-Only vs. Recht auf Vergessenwerden (Art. 17 DSGVO):**
- Eine Blockchain kann Einträge nicht löschen (Append-Only + Unveränderbarkeit).
- Die DSGVO fordert das Recht auf Löschung personenbezogener Daten.

**Weiterer Konflikt: Transparenz vs. Datenschutz:**
- Öffentliche Blockchains sind für alle einsehbar.
- Patientendaten dürfen nicht öffentlich zugänglich sein.

**Konflikt: Speicherbegrenzung (Art. 5 DSGVO) vs. Unveränderbarkeit:**
- Daten dürfen nur so lange gespeichert werden wie notwendig.
- In der Blockchain bleiben sie dauerhaft.

**Lösungsansätze** (im PDF nicht behandelt, da eHealth-Blockchain in der Vorlesung nicht direkt besprochen):
- **Off-Chain-Speicherung:** Nur Hashes on-chain, Daten selbst off-chain → on-chain-Datensatz bleibt, enthält aber keine personenbezogenen Daten.
- **Private/Permissioned Blockchains:** Zugang kontrolliert, nicht öffentlich transparent.

---

Warum war die Zeitstempel-Lösung von Haber/Stornetta der Urform von Bitcoin ähnlich – und was fehlte noch?

?

**Gemeinsamkeiten:**
| Element | Zeitstempel-Service (1989/91) | Bitcoin (2008) |
|---|---|---|
| Krypto-Bausteine | Hash + digitale Signatur | Hash + digitale Signatur |
| Datenstruktur | Zeitstempel in Blöcken verkettet | Transaktionen in Blöcken verkettet |
| Manipulationsschutz | kryptografische Verkettung | kryptografische Verkettung + PoW |
| Öffentliche Verifikation | Hash-Veröffentlichung in NYT | Distributed Ledger auf Tausenden Nodes |

**Was fehlte im Zeitstempel-Service:**
- **Zentrale Trusted Authority** (Trusted Timestamping Authority) als Schwachstelle.
- Bitcoin **ersetzt** diese Authority durch: Distributed Ledger + Konsens-Protokoll (PoW).
- Statt einer vertrauenswürdigen Stelle: **Mathematik und wirtschaftliche Anreize** schaffen Vertrauen.

---

### Vergleich

Vergleiche Proof-of-Work und Proof-of-Stake hinsichtlich Konsens-Mechanismus, Energiebedarf und Schwächen.

?

| Aspekt | Proof-of-Work (PoW) | Proof-of-Stake (PoS) |
|---|---|---|
| Konsens durch | Rechenarbeit (Brute-Force-Hashing) | Kapitaleinsatz (Stake) |
| Rollen | Miner | Validators |
| Auswahl | Wettbewerb (wer löst zuerst?) | Zufällig, gewichtet nach Stake |
| Anreiz für Ehrlichkeit | Belohnung (BTC) | Belohnung + Stakeerhalt |
| Strafe für Manipulation | kein direkter, aber neues PoW nötig | **Verlust des Stakes (Slashing)** |
| Energiebedarf | **sehr hoch** (137 TWh/Jahr Bitcoin) | drastisch geringer |
| Schwäche | 51-%-Angriff; Energieverbrauch | Kapitalkonzentration bei wenigen Validatoren |
| Beispiel | Bitcoin | Ethereum (seit PoS-Wechsel) |

---

Vergleiche Bitcoin und Ethereum als Blockchain-Implementierungen.

?

| Aspekt | Bitcoin | Ethereum |
|---|---|---|
| Erfunden | 2008 (Satoshi Nakamoto) | 2015 (Vitalik Buterin) |
| Primärzweck | Dezentrale digitale Währung | Plattform für verteilte Berechnungen |
| Besonderheit | Transaktionen (Werttransfer) | **Smart Contracts** (programmierbare Verträge) |
| Konsens (laut Vorlesung) | PoW | ähnlich Bitcoin (Folie 31 – ohne Detailangabe) |
| Höchstwert | 21 Mio. Bitcoins | kein fester Cap |
| eHealth-Relevanz | Audit-Trail, Zahlungen | Smart Contracts für automatisierte Prozesse |

*(Ethereum-PoS-Wechsel 2022 „The Merge" – im PDF nicht erwähnt)*

---

Vergleiche die drei Blockchain-Anwendungen hinsichtlich Konsens, Akteure und Öffentlichkeit.

?

| Aspekt | Kryptowährung | Grundbuch | Lieferkette |
|---|---|---|---|
| Konsens | öffentlich (PoW/PoS) | staatlich kontrolliert (Regierung = Nodes) | konsortial (Lieferketten-Partner) |
| Akteure | beliebige Miner/Nodes weltweit | staatliche Behörden | Bauer, Industrie, Transport, Markt, Kunde |
| Sichtbarkeit | öffentlich | transparent (kontrolliert) | für alle Kettenakteure einsehbar |
| Transaktion | Geldtransfer | Eigentumsübergang | Übergabe entlang der Kette |
| Kernvorteil | Dezentralisierung, kein Intermediär | Manipulationssichere Eigentumsnachweise | Herkunfts- und Weg-Transparenz |

---

## Mögliche Anschlussfragen

- Was ist ein Smart Contract, und welche Blockchain unterstützt ihn? (Ethereum – im PDF nur genannt, nicht definiert)
- Warum veröffentlichte Surety Inc. den Block-Hash wöchentlich in der NYT? (Öffentliche, massenhaft archivierte Wahrheitsquelle)
- Was passiert beim Halving mit der Wirtschaftlichkeit von Mining, wenn der Reward gegen Null geht?
- Wie hängen Distributed Ledger und kryptografische Verkettung zusammen – und welches Problem löst jedes?
- Was ist eine 51-%-Attacke, und warum ist sie bei Mining-Pool-Konzentration relevant?
- [Ergänzung] Welche Hash-Funktion nutzt Bitcoin für PoW? (SHA-256, doppelt – im PDF nicht spezifiziert)

## Eigene Notizen

<!-- Platz für persönliche Ergänzungen, Eselsbrücken, etc. -->
