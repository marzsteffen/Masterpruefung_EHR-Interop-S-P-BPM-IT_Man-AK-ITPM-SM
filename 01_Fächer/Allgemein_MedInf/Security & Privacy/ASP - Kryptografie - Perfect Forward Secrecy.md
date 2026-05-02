---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Kryptografie - Perfect Forward Secrecy (PFS)

> [!info] Kurzdefinition
> Eigenschaft eines Verschlüsselungs-/Schlüsselaustausch-Protokolls, bei der eine spätere Kompromittierung von Langzeitschlüsseln zuvor aufgezeichnete Kommunikation NICHT entschlüsselbar macht. Erreicht durch ephemerale Sitzungs-Schlüsselpaare und Diffie-Hellman.

## Beschreibung

PFS wird in der Vorlesungsreihe in zwei Stufen eingeführt:

1. **Erst als Stichwort** in [[ASP - VL - Einfuehrung und Motivation]] (Folie 21), als Schutz gegen den Angriff [[ASP - Angriff - Aufzeichnung und Entschluesselung]].
2. **Vollständige Konstruktion** in [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (Folien 28–32), nachdem alle nötigen Bausteine (asym. Verschlüsselung, Signatur, Zertifikate, Diffie-Hellman) erklärt sind.

**Motivation (Folie 28):** Bei normaler hybrider Verschlüsselung kann eine dritte Partei (Eve) alle verschlüsselten Nachrichten speichern. Wird Bobs Private Key später kompromittiert (gestohlen), kann Eve den symmetrischen Sitzungsschlüssel jeder aufgezeichneten Sitzung entschlüsseln und damit die gesamte alte Kommunikation lesen.

**PFS-Konstruktion (Folie 30):**

- Sender Alice, Empfänger Bob.
- Beide verfügen über je ein **statisches asymmetrisches Schlüsselpaar** (Algorithmen: ECC oder RSA).
- **Vor jeder Kommunikation:**
  1. **Ephemeral ECC-Schlüsselpaare** werden erzeugt (eines bei Alice, eines bei Bob). – *Hinweis der Vorlesung: RSA-Algorithmus zu langsam für die Erzeugung von Ephemeral Keys; deshalb in der Praxis ECC.*
  2. **Ephemeral Public Keys** werden ausgetauscht und mit dem **statischen privaten Schlüssel** signiert (sichert Vertrauen, dass der ephemerale Schlüssel wirklich von Alice bzw. Bob stammt).
  3. **Symmetrischer Schlüssel** wird aus den Ephemeral-Public-Keys über das **Diffie-Hellman-Merkle-Protokoll** berechnet (siehe [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]).
  4. Kommunikation läuft mit diesem symmetrischen Schlüssel (hybride Verschlüsselung).
  5. **Nach der Kommunikation** werden die Ephemeral-ECC-Schlüsselpaare und der symmetrische Sitzungsschlüssel **gelöscht**.

**Warum das funktioniert:** Eve, die zu einem späteren Zeitpunkt den statischen Private Key von Alice oder Bob stiehlt, hat damit nichts gewonnen – die ephemeralen Schlüssel und der Sitzungsschlüssel existieren nicht mehr und sind aus dem statischen Schlüssel auch nicht ableitbar. Die statischen Schlüssel haben nur signiert, nicht direkt verschlüsselt.

## Bestandteile / Aufbau

| Schlüssel | Eigenschaft | Verwendung |
|---|---|---|
| Statischer Private Key | langlebig | nur zum Signieren der ephemeralen Public Keys |
| Statischer Public Key | langlebig (im Zertifikat) | zur Signaturprüfung der Gegenseite |
| Ephemeral Private Key | gilt nur für eine Sitzung | wird zur DH-Schlüsselberechnung verwendet, danach gelöscht |
| Ephemeral Public Key | gilt nur für eine Sitzung | wird ausgetauscht und vom statischen Private Key signiert |
| Symmetrischer Sitzungsschlüssel | gilt nur für eine Sitzung | verschlüsselt die Nutzdaten, danach gelöscht |

## Beispiel

Aus Folie 30 visualisiert: Alice und Bob besitzen statische Public/Private-Keys. Beide erzeugen zufällig ephemerale ECC-Schlüsselpaare; signieren ihre ephemeralen Public Keys mit dem statischen Private Key und tauschen sie aus; verifizieren die Signatur der Gegenseite mit deren statischem Public Key (aus Zertifikat). Aus den ephemeralen Schlüsseln wird per DH der gemeinsame Sitzungsschlüssel berechnet. Nach der Sitzung werden alle ephemeralen Daten gelöscht.

## Abgrenzung

- PFS schützt **nicht** vor zukünftiger Kommunikation nach Schlüsseldiebstahl – nur vor der nachträglichen Entschlüsselung *bereits abgeschlossener* Sessions.
- PFS hat nichts mit Integrität oder Authentizität zu tun – diese müssen separat sichergestellt werden (in der gezeigten Konstruktion: Signatur der ephemeralen Public Keys mit dem statischen Private Key).
- **Schwäche der einfachen hybriden Verschlüsselung:** Sitzungsschlüssel wird mit Bobs Public Key verschlüsselt übertragen → bei späterem Diebstahl von Bobs Private Key entschlüsselbar. PFS löst genau dieses Problem.
- **Bewertung gegen das Angriffsmodell (Folie 31):** Der Angriff „Aufzeichnung + Entschlüsselung mit gestohlenem Schlüssel" wird durch PFS verhindert. Replay bleibt aber weiterhin möglich (außer auf Protokollebene mit Timestamps gelöst).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Perfect Forward Secrecy, und welchen Angriff verhindert es?

**Anwendungsfrage:** Skizzieren Sie die PFS-Konstruktion mit ephemeralen Schlüsseln und Diffie-Hellman. Welche Rolle spielen die statischen Schlüssel, welche die ephemeralen?

**Diskussionsfrage:** Warum verwendet die Vorlesung explizit ECC für die ephemeralen Schlüssel und nicht RSA? Welche Trade-offs entstehen durch PFS in der Praxis (Performance, Komplexität)? Warum sind langlebige Gesundheitsdaten besonders abhängig von PFS-Eigenschaften? (Stichwort: „Harvest now, decrypt later".)

**Mögliche Anschlussfragen:**
- Wie hängt PFS mit dem Diffie-Hellman-Schlüsselaustausch zusammen?
- Schützt PFS auch dann, wenn ein Schlüssel **vor** Beginn der Session kompromittiert wurde? (Nein – nur die Vergangenheit ist geschützt.)
- Welche Schwäche bleibt auch mit PFS offen? (Ephemerale Schlüssel müssen sicher gespeichert / erzeugt werden – Folie 32.)
- Wie hängt PFS mit der Schlüssel-Speicherung in HSM/Secure Element zusammen?

## Verwandt

- [[ASP - Angriff - Aufzeichnung und Entschluesselung]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Schluesselspeicherung - Hardware Security]]
- [[ASP - Schutzmethoden - Uebersicht]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (vollständige Konstruktion)
- Folien/Seitenangabe Kapitel 04: Folien 28–31
- Erste Erwähnung als Stichwort: [[ASP - VL - Einfuehrung und Motivation]], Folie 21

## Ergänzung außerhalb der Vorlesung

In der Praxis wird PFS in TLS 1.3 standardmäßig erzwungen – jede Sitzung verwendet **ECDHE** (Elliptic Curve Diffie-Hellman Ephemeral). Statisches RSA-Schlüssel-Transport ist in TLS 1.3 entfernt. Im Signal-Protokoll (Messaging) wird PFS noch weiter getrieben durch zusätzlich rotierende Sitzungsschlüssel pro Nachricht („Double Ratchet"), was als zusätzliche Eigenschaft „Future Secrecy" gilt.
