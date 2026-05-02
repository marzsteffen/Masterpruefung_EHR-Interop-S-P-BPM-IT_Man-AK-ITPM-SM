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

# ASP - Symmetrische Verschlüsselung - Blockchiffre

> [!info] Kurzdefinition
> Bauart symmetrischer Verschlüsselung, die Daten in festen Blöcken (z. B. 64 oder 128 Bit) verschlüsselt; jeder Block wird unabhängig, aber mit demselben Schlüssel chiffriert.

## Beschreibung

Eigenschaften der Blockchiffre laut Folie 7:

- **Blockbasierte Datenverschlüsselung:** eine bestimmte Anzahl von Bits (Blöcke) wird verschlüsselt.
- **Unabhängige Blockverschlüsselung:** Jeder Block wird unabhängig, aber mit demselben Schlüssel verschlüsselt.
- **Anwendungsfeld:** Verschlüsselung von Daten auf Festplatten und anderen Speichermedien.
- **Parallelisierbar:** Gleichzeitige Verschlüsselung mehrerer Blöcke parallel möglich.
- **Höhere Sicherheit gegen Datenmanipulation** (laut Folie).

## Bestandteile / Aufbau

| Element | Rolle |
|---|---|
| Klartext-Block fester Länge | z. B. 64 Bit (DES) oder 128 Bit (AES) |
| Schlüssel | identisch für alle Blöcke |
| Block-Algorithmus | Anwendung von Substitution, Permutation, XOR pro Block |
| Ciphertext-Block | Ausgabe gleicher Länge wie Eingabe |

## Beispiel

Aus dem Vorlesungs-Kontext: DES verschlüsselt 64-Bit-Blöcke (Folie 11), AES 128-Bit-Blöcke (16 Byte; Folie 22). Die konkreten Round-Funktionen werden in den Algorithmus-Notes behandelt.

## Abgrenzung

- **Blockchiffre vs. [[ASP - Symmetrische Verschluesselung - Stromchiffre]]:** Strom kommt mit beliebig wenigen Bits aus, Block braucht volle Blocklänge (Padding nötig, falls Klartext nicht passt). Strom ist sequentiell, Block parallelisierbar.
- Die Aussage „jeder Block wird unabhängig verschlüsselt" beschreibt im Strengen den ECB-Modus (Electronic Codebook). **Der Modus-Begriff (z. B. CBC, CTR, GCM) wird im PDF nicht definiert** – moderne Praxis nutzt fast immer einen Modus mit Verkettung oder Authentication, weil reines ECB Muster im Klartext erhält.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Blockchiffre, und wie unterscheidet sie sich von einer Stromchiffre?

**Anwendungsfrage:** In welchem Anwendungsfall ist eine Blockchiffre die richtige Wahl? (Datenträgerverschlüsselung, große Datenmengen.) Welche Algorithmen sind klassische Blockchiffren? (DES, 3DES, AES.)

**Diskussionsfrage:** Welche Probleme entstehen, wenn alle Blöcke wirklich „unabhängig" verschlüsselt werden (ECB-Modus)? Welche Modi adressieren das? (*Modi nicht im PDF*, siehe Ergänzung.)

**Mögliche Anschlussfragen:**
- Welche Blocklänge hat DES, welche AES?
- Warum ist Blockchiffre laut PDF „sicherer gegen Datenmanipulation"?
- Welcher Bauart unterliegt DES intern? (Feistel-Funktion.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Stromchiffre]]
- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]
- [[ASP - Symmetrische Verschluesselung - Triple-DES]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folie 7

## Ergänzung außerhalb der Vorlesung

In der Praxis wird eine Blockchiffre fast nie im reinen ECB-Modus eingesetzt, weil identische Klartext-Blöcke identische Ciphertext-Blöcke erzeugen und so Muster im Klartext sichtbar bleiben (klassisches „Pinguin-Bild"-Beispiel). Stattdessen verwendet man Betriebsmodi wie CBC (Cipher Block Chaining – verkettet Blöcke per XOR), CTR (Counter – aus Blockchiffre wird quasi eine Stromchiffre) oder AEAD-Modi wie GCM (Galois/Counter Mode), die zusätzlich Authentizität liefern.
