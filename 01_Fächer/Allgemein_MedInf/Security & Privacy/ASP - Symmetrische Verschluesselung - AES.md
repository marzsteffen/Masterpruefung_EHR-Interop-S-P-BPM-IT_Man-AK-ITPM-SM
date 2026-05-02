---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Verschluesselungsmethoden]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Symmetrische Verschlüsselung - AES (Advanced Encryption Standard)

> [!info] Kurzdefinition
> AES ist seit 2000 der NIST-Standard für symmetrische Verschlüsselung und Nachfolger von DES. Es ist eine Blockchiffre mit 128-Bit-Block, beliebigem Schlüssel ab 128 Bit und einem mehrrundigen Substitutions-Permutations-Netzwerk (SubBytes, ShiftRows, MixColumns, AddRoundKey).

## Beschreibung

Eckdaten laut Folien 22–24:

- **Seit 2000 offizieller NIST Standard und Nachfolger von DES.**
- **Meistgenutztes und sicherstes Verschlüsselungsverfahren** (laut Vorlesung).
- **Schlüssel mit 128 Bit zu knacken dauert länger als das angenommene Alter des Universums.**
- **Blockverschlüsselung (16 Byte = 128 Bit).**
- **Verwendete Operationen:** Byteersetzung (Substitution), Verwürfelung (Permutation), Verschiebungen.

**Algorithmus-Aufbau (Folie 23):**

1. **Schlüsselexpansion** durch einen Sub-Key-Generator: Aus dem Master-Key werden Rundenschlüssel abgeleitet.
2. **Vorrunde:** AddRoundKey mit dem 1. Rundenschlüssel auf den 128-Bit-Klartext.
3. **9 Verschlüsselungsrunden** (für AES-128) – jede Runde besteht aus:
   - **Sub-Byte-Step** (Substitution per S-Box)
   - **ShiftRows** (Verschiebung)
   - **MixColumns** (Spaltenmischung)
   - **AddRoundKey** (XOR mit Rundenschlüssel)
4. **Abschlussrunde** (10. Runde) – wie eine normale Runde, aber **ohne MixColumns**:
   - Sub-Byte-Step
   - ShiftRows
   - AddRoundKey (mit dem 10. Rundenschlüssel)
5. **Ausgabe:** 128-Bit-Ciphertext.

**Anwendungsgebiete (Folie 24):**
- Wireless LAN (WPA-2 Sicherheitsstandard)
- IP-Telefonie
- Real-Time-Systeme wie Skype
- Verschlüsselung von Dateiarchiven (7-Zip, RAR, …)

## Bestandteile / Aufbau

| Element | Wert |
|---|---|
| Standardisiert | 2000 (NIST) |
| Blockgröße | 128 Bit (16 Byte) |
| Schlüssellänge | 128 Bit (im PDF gezeigt). Standard kennt drei Varianten: AES-128, AES-192, AES-256 (Ergänzung) |
| Konstruktion | Substitutions-Permutations-Netzwerk (kein Feistel) |
| Runden | AES-128: 10 · AES-192: 12 · AES-256: 14 (Ergänzung); im PDF nur AES-128 gezeigt |
| Einzeloperationen | SubBytes, ShiftRows, MixColumns, AddRoundKey |

## Beispiel

Aus Folie 23: Klartext (128 Bit) durchläuft Vorrunde (AddRoundKey mit 1. Rundenschlüssel), dann 9 Runden mit allen vier Operationen, dann Abschlussrunde ohne MixColumns mit dem 10. Rundenschlüssel. Ergebnis: 128 Bit Ciphertext.

## Abgrenzung

- **AES vs. [[ASP - Symmetrische Verschluesselung - DES]]:** AES nutzt kein Feistel-Netzwerk. Blockgröße 128 statt 64 Bit. Schlüssel ab 128 Bit statt 56 Bit. Anders im Aufbau (alle Bytes pro Runde modifiziert, nicht nur eine Hälfte).
- **AES vs. [[ASP - Symmetrische Verschluesselung - Triple-DES]]:** Schneller, sicherer, modernerer Standard. 3DES war eine Übergangslösung; AES ist die saubere Neuentwicklung.
- AES-128, AES-192 und AES-256 unterscheiden sich in Schlüssellänge und Rundenanzahl (10/12/14 Runden). **Im PDF wird nur AES-128 mit 10 Runden gezeigt; AES-192/256 sind nicht erwähnt.**

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist AES, welche Schlüssel- und Blockgröße verwendet es, und welche vier Operationen pro Runde sind charakteristisch?

**Anwendungsfrage:** Skizziere den AES-Verschlüsselungsablauf (Schlüsselexpansion, Vorrunde, n Hauptrunden, Abschlussrunde). Welcher Schritt fehlt in der Abschlussrunde, und warum?

**Diskussionsfrage:** Warum hat AES 3DES abgelöst? Welche Trade-offs zwischen DES, 3DES und AES gibt es bei Schlüssellänge, Performance und Blockgröße?

**Mögliche Anschlussfragen:**
- Warum braucht AES eine Schlüsselexpansion?
- Welche Eigenschaft hat MixColumns, und warum entfällt der Schritt in der Abschlussrunde? (*Im PDF nicht beantwortet.*)
- Wie hängt die Aussage „128 Bit knacken dauert länger als das Universumsalter" mit der Brute-Force-Komplexität 2^128 zusammen?

## Verwandt

- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - Triple-DES]]
- [[ASP - Symmetrische Verschluesselung - S-Box]]
- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folien 22–24

## Ergänzung außerhalb der Vorlesung

- **Drei Varianten:** AES-128 (10 Runden), AES-192 (12 Runden), AES-256 (14 Runden). Block bleibt immer 128 Bit.
- **Abschlussrunde ohne MixColumns:** der Schritt würde die Sicherheit ohne nachfolgendes SubBytes nicht weiter erhöhen, kostet aber Rechenzeit.
- **AES-NI** auf modernen CPUs macht AES hardwarebeschleunigt; oft schneller als ein Hash über die gleichen Daten.
- Original-Algorithmus: **Rijndael** von Joan Daemen und Vincent Rijmen, NIST-Wettbewerb 2000.
