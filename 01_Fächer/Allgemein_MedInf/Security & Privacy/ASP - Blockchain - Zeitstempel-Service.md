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

# ASP - Blockchain - Zeitstempel-Service (Vorgeschichte der Blockchain)

> [!info] Kurzdefinition
> 1989/91 entwickelten Haber und Stornetta die Urform der Blockchain: signierte digitale Zeitstempel, die zu Blöcken zusammengefasst und über Hash-Werte kryptografisch verkettet werden. Der finale Block-Hash wird öffentlich (z. B. in der NYT) veröffentlicht.

## Beschreibung

Folien 3–10 beschreiben das Ausgangsproblem 1989: Mit dem Beginn des Internets sollten digitale Dokumente bald online gestellt werden. Um die **Originalität** zu schützen, sollte erkennbar sein, wer ein Dokument erstellt hat (**Authentizität**) und ob es unverändert vorliegt (**Integrität**). Stuart Haber und W. Scott Stornetta entwickelten dafür die Urform der Blockchain mit digitalen Zeitstempeln.

**Digitaler Zeitstempel (Folie 4):**
- Bescheinigung, dass ein elektronisches Dokument zu einer angegebenen Zeit dem (unparteilichen) Aussteller des Zeitstempels vorgelegen hat.
- Erstellung über ein Zeitstempel-Service zur Verhinderung von Manipulation.

**Erstellung eines digitalen Zeitstempels (Folie 4):**
1. Antragsteller schickt Dokument an den Aussteller.
2. Aussteller berechnet den Hash-Wert des Dokuments (Hash-Funktion).
3. Aussteller signiert den Hash-Wert plus die aktuelle Zeit mit seinem Private Key → digitaler Zeitstempel.

**Zeitstempel-Service (Folien 6, 10):**
- Mehrere signierte Zeitstempel werden zu Blöcken zusammengefasst.
- Pro Block wird ein **Block-Hash** über alle enthaltenen Zeitstempel berechnet.
- Die Block-Hashes werden iterativ über die Hash-Funktion zu einem **finalen Hash-Wert** verdichtet (kryptografische Verkettung).
- Alle Daten werden zentral in einer Datenbank gespeichert.
- Eine zentrale Partei (Trusted Timestamping Authority) führt die Überprüfung durch.

**Kryptografische Verkettung (Folien 7, 8):**
- Eine Änderung eines Dokuments verändert den Hash dieses Zeitstempels und damit den Block-Hash.
- Da Block-Hashes wiederum als Input weiterer Hash-Berechnungen dienen, ändern sich auch alle nachfolgenden Block-Hashes – die Manipulation wird auf jeder Stufe sichtbar.

**Veröffentlichung (Folie 9):** Um den finalen Hash-Wert öffentlich verifizierbar zu machen, wurde er von 1995 bis heute jede Woche in der **New York Times** in der „Notices & Lost and Found"-Anzeigenrubrik abgebildet (Surety, Inc.).

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Digitaler Zeitstempel | signierter (Hash + Zeit) durch Aussteller |
| Block | Zusammenfassung mehrerer Zeitstempel mit Block-Hash |
| Kette | Block-Hashes als Input für Hash der nächsten Stufe → finaler Hash |
| Vertrauensbasis | Zentrale Trusted Timestamping Authority |
| Öffentliche Verifikation | Veröffentlichung des finalen Hashes (z. B. NYT) |

## Beispiel

Aus Folie 4: Antragsteller reicht „Hallo Alice" ein → Hash `487a09209f657a0…` → Aussteller signiert (Hash + Zeit `2023-11-11T12:34:56`) mit seinem Private Key → digitaler Zeitstempel.

## Abgrenzung

- **Zeitstempel-Service ist die Urform der Blockchain**, aber NICHT dezentral – es braucht eine vertrauenswürdige zentrale Partei. Genau das löst Bitcoin später (siehe [[ASP - Blockchain - Bitcoin Grundlagen]]).
- **NYT-Veröffentlichung** ist eine clevere „öffentliche Quelle der Wahrheit" – sie ersetzt die zentrale Speicherung durch ein massenhaft archiviertes Beweisstück.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was war das Ursprungsproblem von Haber/Stornetta, und wie wurde es gelöst?

**Anwendungsfrage:** Skizzieren Sie die Erstellung eines digitalen Zeitstempels und die Verkettung mehrerer Zeitstempel zu einem finalen Hash.

**Diskussionsfrage:** Welche Schwachstelle hat das System, und wie behebt Bitcoin sie? (Antwort: zentrale Trusted Authority – Bitcoin ersetzt sie durch ein Distributed Ledger plus Konsens.) Welche Rolle spielt die NYT-Veröffentlichung?

**Mögliche Anschlussfragen:**
- Welche Krypto-Bausteine kommen zum Einsatz? (Hash, digitale Signatur.)
- Was passiert, wenn ein Zeitstempel manipuliert wird?
- Warum wird die kryptografische Verkettung als Vorform der Blockchain bezeichnet?

## Verwandt

- [[ASP - Hash - Funktion]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Blockchain - Bitcoin Grundlagen]]
- [[ASP - Blockchain - Block und Verkettung]]
- [[ASP - Blockchain - Distributed Ledger]]

## Quelle

- Vorlesung: [[ASP - VL - Blockchain]]
- Folien/Seitenangabe: Folien 3–10
- Externe Referenz: Haber & Stornetta, „How to time-stamp a digital document" (Springer, 1991)
