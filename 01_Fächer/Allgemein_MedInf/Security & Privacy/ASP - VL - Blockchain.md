---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/06 Blockchain/IVL_ADSP IT-Basisschutzmethoden in der Praxis (Blockchain).pdf
datum_vorlesung: 2024-11-12
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Blockchain (IT-Basisschutzmethoden in der Praxis)

## Überblick

Sechster Vorlesungsblock und zugleich erstes der zwei Praxiskapitel („IT-Security Basis-Schutzmethoden in der Praxis"). Die Vorlesung zeigt am Beispiel **Blockchain**, wie die zuvor eingeführten Bausteine (Hash, digitale Signatur, asymmetrische Krypto) in einem konkreten verteilten System zusammenspielen. Aufbau gemäß Agenda (Folie 2): Zeitstempel-Problem, Funktionsweise des Bitcoins, Anwendung der Blockchain, Konsensus-Protokolle, Anwendungsgebiete.

## Lernziele (laut Vorlesung)

*Im PDF nicht als eigene Liste ausgewiesen.* Aus dem Aufbau ergeben sich: digitale Zeitstempel und kryptografische Verkettung verstehen; Bitcoin-Funktionsweise erklären können; Distributed Ledger und Konsens-Notwendigkeit motivieren; Proof-of-Work und Proof-of-Stake gegeneinander abgrenzen; Anwendungsgebiete der Blockchain jenseits Kryptowährung kennen.

## Behandelte Konzepte

### Vorgeschichte: Zeitstempel
- [[ASP - Blockchain - Zeitstempel-Service]]

### Bitcoin und Blockchain
- [[ASP - Blockchain - Bitcoin Grundlagen]]
- [[ASP - Blockchain - Distributed Ledger]]
- [[ASP - Blockchain - Bitcoin Funktionsweise]]
- [[ASP - Blockchain - Mining Pools]]
- [[ASP - Blockchain - Halving]]
- [[ASP - Blockchain - Block und Verkettung]]
- [[ASP - Blockchain - Eigenschaften und Vorteile]]

### Konsensus-Protokolle
- [[ASP - Blockchain - Proof-of-Work]]
- [[ASP - Blockchain - Proof-of-Stake]]
- [[ASP - Blockchain - Weitere Konsensus-Protokolle]]
- [[ASP - Blockchain - Kritik PoW]]

### Anwendungsgebiete
- [[ASP - Blockchain - Anwendungen]]

## Roter Faden

Ausgangsproblem (1989, Folie 3): Mit dem Aufkommen des Internets sollte die **Originalität** digitaler Dokumente erkennbar bleiben – wer hat sie erstellt (Authentizität) und ob sie unverändert vorliegen (Integrität). Stuart Haber und W. Scott Stornetta entwickelten dafür die **Urform der Blockchain** mithilfe digitaler Zeitstempel: Hash der Dokumente + Zeit, signiert von einer vertrauenswürdigen Stelle. Mehrere Zeitstempel werden zu Blöcken zusammengefasst und über Hashes kryptografisch verkettet (Folie 6). Eine Manipulation an einem Dokument ändert den Block-Hash und – durch die Verkettung – auch alle nachfolgenden. Der finale Hash wurde wöchentlich in der **New York Times** veröffentlicht (seit 1995, Folie 9), um öffentlich verifizierbar zu bleiben. Zwei Schwachpunkte blieben: zentrale Datenbank und vertrauenswürdige Authority.

**Bitcoin (2008, Satoshi Nakamoto)** adaptiert diese Idee und löst die zentrale Schwachstelle: keine Trusted Authority mehr, dafür ein **Distributed Ledger** auf vielen Nodes plus ein **Konsens-Mechanismus**. Benutzer signieren Transaktionen und schicken sie ans Netzwerk; **Miner** sammeln sie aus einem Pool, fassen sie zu einem Block zusammen und versuchen, ein **mathematisches Rätsel** zu lösen (Hash mit ausreichend vielen führenden Nullen; gesuchter Wert ist eine **Nonce**). Der erste Miner, der eine gültige Nonce findet, sendet seinen Block an das Netzwerk; alle anderen Nodes verifizieren in Sekunden. Der erfolgreiche Miner erhält einen **Reward** in Bitcoin – Anreiz, ehrlich zu rechnen. Die **Belohnung halbiert sich** alle 210 000 Blöcke (≈ 4 Jahre, „Halving"), Gesamtmenge konvergiert gegen 21 Mio.

Die so entstehende Datenstruktur ist die **Blockchain**: Jeder Block enthält Transaktionen, Nonce, eigenen Hash und Hash des Vorgängers; die ganze Kette ist append-only und manipulationssicher dank kryptografischer Verkettung. **Eigenschaften:** verteilt, unveränderbar, append-only. **Vorteile:** Transparenz, Authentizität/Verifizierbarkeit, kein Single Point of Failure, keine zentrale Trust Authority.

Hauptkritik an Bitcoin / Proof-of-Work: enormer **Energieverbrauch** (137 TWh/Jahr ≈ Stromverbrauch der Ukraine; 411 kg CO₂ pro Transaktion). Daraus motivieren sich Alternative Konsens-Protokolle: **Proof-of-Stake** (Validators hinterlegen Kaution / „Steak"), **Delegated Proof-of-Stake**, **Proof-of-Authority**, **Proof-of-Identity**, **Proof-of-Elapsed-Time**.

**Anwendungsgebiete jenseits Kryptowährungen:** Ethereum mit Smart Contracts, **Grundbuch** (Estland, Kanada), **Lieferketten** (Bauer → Industrie → Transport → Markt → Kunde, alles in der Blockchain).

## Zentrale Aussagen / Take-aways

- **Vorgeschichte:** Haber/Stornetta 1989 – Hash + Zeitstempel, in Blöcken verkettet, Veröffentlichung in der NYT.
- **Bitcoin (2008, Nakamoto):** dezentral, kein Trusted Third Party, Konsens über Mining.
- **Proof-of-Work:** Hash-Rätsel mit Nonce; erste Lösung gewinnt Reward; alle anderen verifizieren.
- **Block-Felder:** Hash dieses Blocks, Hash des Vorgängers, Nonce, Transaktionen (+ Signaturen + Public Keys der Sender).
- **Reward-Halving alle 210 000 Blöcke**, Maximum 21 Mio. Bitcoins.
- **Eigenschaften:** verteilt, unveränderbar, append-only.
- **PoW ist energieintensiv:** 137 TWh/Jahr, 411 kg CO₂ pro Transaktion.
- **PoS** als Alternative: Validators statt Miner, „Steak" als Kaution, ehrliches Verhalten wird belohnt, Manipulation kostet den Steak.
- **Weitere Protokolle:** DPoS, PoA, PoI, PoET.
- **Anwendungen:** Bitcoin, Ethereum (Smart Contracts), Grundbuch, Lieferketten.

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (Krypto-Bausteine, die Blockchain nutzt)
- [[ASP - VL - Verschluesselungsmethoden]] (asymmetrische Schlüssel für Bitcoin-Wallets)
- [[ASP - VL - Gruener Pass]] (folgt – zweites Praxis-Kapitel mit signierten QR-Codes)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/06 Blockchain/IVL_ADSP IT-Basisschutzmethoden in der Praxis (Blockchain).pdf`
- Folienanzahl: 37
- Vortragender: Dr. Kevin Theuermann
- Datum laut Folien: 12.11.2024
- Externe Referenz auf Folie 3: Haber/Stornetta, „How to time-stamp a digital document", https://link.springer.com/content/pdf/10.1007/BF00196791.pdf
