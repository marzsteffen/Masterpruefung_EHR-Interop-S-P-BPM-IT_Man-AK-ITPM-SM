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

# ASP - Symmetrische Verschlüsselung - Triple-DES (3DES)

> [!info] Kurzdefinition
> Triple-DES (auch TDES oder 3DES) ist eine Verstärkung von DES durch dreifache Anwendung mit drei voneinander unabhängigen 56-Bit-Schlüsseln. Effektive Schlüssellänge: 168 Bit.

## Beschreibung

Folie 20 erläutert Triple-DES:

- **Motivation:** Zu geringe Schlüssellänge bei DES (56 Bit).
- **Funktionsweise:** Mehrfache Ausführung von DES mit verschiedenen Schlüsseln.
- **Schlüssellänge insgesamt 168 Bits statt 56 Bits** (3 × 56 = 168).
- **Drei voneinander unabhängige Schlüssel.**

**Verschlüsselung (laut Folie):**
```
3DES(k1, k2, k3) = Encrypt_k1( Decrypt_k2( Encrypt_k3( Plaintext ) ) )
```
Die Reihenfolge ist also **Encrypt – Decrypt – Encrypt** (EDE), wobei die mittlere Operation eine *Entschlüsselung* mit k2 ist. Bei Wahl k1 = k2 = k3 reduziert sich 3DES dadurch auf einfaches DES (Abwärtskompatibilität – *im PDF nicht erläutert*).

**Entschlüsselung (laut Folie):**
```
3DES(k1, k2, k3) = Decrypt_k3( Encrypt_k2( Decrypt_k1( Ciphertext ) ) )
```
Also Decrypt – Encrypt – Decrypt mit umgekehrter Schlüsselreihenfolge.

## Bestandteile / Aufbau

| Element | Wert |
|---|---|
| Schlüssellänge | 168 Bit (3 × 56) |
| Blockgröße | 64 Bit (wie DES) |
| Anzahl DES-Anwendungen | 3 |
| Schema | EDE (Encrypt–Decrypt–Encrypt) |
| Anzahl unabhängiger Schlüssel | 3 (k1, k2, k3) |

## Beispiel

*Im PDF nicht ausgeführt.* Aus dem Schema lässt sich ableiten: Klartext m → Encrypt mit k3 → Decrypt mit k2 → Encrypt mit k1 → Ciphertext c.

## Abgrenzung

- **3DES vs. [[ASP - Symmetrische Verschluesselung - DES]]:** identische Block-Operation, aber dreimal angewendet → höhere Brute-Force-Resistenz.
- **3DES vs. [[ASP - Symmetrische Verschluesselung - AES]]:** AES ist neuer (NIST 2000), schneller und kryptografisch deutlich robuster gestaltet. 3DES war eine Übergangslösung; heute wird AES bevorzugt.
- **Effektive Sicherheit von 3DES** ist trotz 168-Bit-Schlüssellänge nur ca. 112 Bit, da Meet-in-the-Middle-Angriffe die Brute-Force-Komplexität halbieren. *Diese Bewertung ist im PDF nicht enthalten*, ist aber prüfungsrelevant (siehe Ergänzung).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist 3DES, wie ist es aufgebaut, und was war die Motivation für seine Entwicklung?

**Anwendungsfrage:** Schreibe die Verschlüsselungs- und Entschlüsselungsformel von 3DES auf. Warum lautet das Schema EDE und nicht EEE?

**Diskussionsfrage:** Warum ist 3DES heute zugunsten von AES weitgehend abgelöst? Welche Schwächen hat es trotz langer Schlüssellänge? (Performance: dreifache DES-Ausführung; effektive Sicherheit nur ca. 112 Bit; kleine Blockgröße 64 Bit – Birthday-Bound-Probleme bei großen Datenmengen.)

**Mögliche Anschlussfragen:**
- Warum verwendet 3DES das Schema EDE statt EEE? (Antwort: Bei k1=k2=k3 wird daraus einfaches DES → Rückwärtskompatibilität.)
- Welche Schlüssellänge gilt als „effektiv" und warum?

## Verwandt

- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]
- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folie 20

## Ergänzung außerhalb der Vorlesung

Das EDE-Schema ist kein Performance-Trick, sondern dient der Abwärtskompatibilität: Setzt man k1 = k2 = k3, wird aus 3DES einfaches DES. Effektive Sicherheit beträgt aufgrund von Meet-in-the-Middle-Angriffen ca. 112 Bit (statt der naiven 168 Bit). Außerdem ist die Block-Größe von 64 Bit nach heutigen Maßstäben zu klein – nach ca. 32 GB verschlüsselter Daten unter dem gleichen Schlüssel werden Birthday-Kollisionen statistisch wahrscheinlich (Sweet32-Angriff). NIST hat 3DES für neue Anwendungen 2017 als veraltet markiert.
