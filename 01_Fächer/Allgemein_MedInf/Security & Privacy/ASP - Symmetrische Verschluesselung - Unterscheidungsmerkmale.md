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

# ASP - Symmetrische Verschlüsselung - Unterscheidungsmerkmale der Algorithmen

> [!info] Kurzdefinition
> Vier Achsen, anhand derer sich symmetrische Verschlüsselungs-Algorithmen unterscheiden: Schlüssellänge, mathematische Funktion, Performance, Verschlüsselungsmodus.

## Beschreibung

Folie 8 listet die Achsen auf, an denen sich symmetrische Algorithmen unterscheiden:

1. **Länge des Schlüssels** – Anzahl Bits des Symmetric Key. Direkt sicherheitsrelevant: Brute-Force-Aufwand wächst mit 2^n. Beispiele aus den Folien: DES 56 Bit, 3DES 168 Bit, AES 128 (oder mehr) Bit.
2. **Mathematische Funktion** – konkrete Konstruktion des Algorithmus (z. B. Feistel-Netzwerk bei DES, Substitutions-Permutations-Netzwerk bei AES).
3. **Performance** – Geschwindigkeit der Ver- und Entschlüsselung; ergibt sich aus Algorithmus-Aufbau und Implementation.
4. **Verschlüsselungsmodus** – Betriebsmodus für Blockchiffren (z. B. ECB, CBC, CTR – **im PDF nicht detailliert**).

## Bestandteile / Aufbau

| Achse | Bedeutung | Beispiel |
|---|---|---|
| Schlüssellänge | Anzahl Bits → Brute-Force-Resistenz | DES 56, AES 128/192/256 |
| Mathematische Funktion | interne Algorithmik | Feistel (DES), SP-Netzwerk (AES) |
| Performance | Durchsatz | AES auf modernen CPUs sehr schnell |
| Modus | Betriebsmodus für Blockchiffren | ECB, CBC, CTR, GCM (PDF nicht spez.) |

## Beispiel

Vergleich aus späteren Folien dieser Vorlesung:
- DES: 56-Bit-Schlüssel, Feistel, abgelöst.
- 3DES: 168-Bit-Schlüssel, dreimal DES.
- AES: 128–256 Bit, SP-Netzwerk, NIST-Standard, sehr performant.

## Abgrenzung

- Diese Achsen gelten für *symmetrische* Algorithmen. Asymmetrische Algorithmen werden anders charakterisiert (Public-/Private-Key-Verfahren basierend auf mathematischen Hardness-Annahmen wie Faktorisierung oder elliptische Kurven).

## Prüfungsrelevanz

**Typische Definitionsfrage:** An welchen Merkmalen unterscheiden sich symmetrische Verschlüsselungs-Algorithmen?

**Anwendungsfrage:** Vergleiche DES, 3DES und AES anhand dieser vier Merkmale.

**Diskussionsfrage:** Welches Merkmal hat den größten Einfluss auf die Sicherheit, welches auf die Praxis-Tauglichkeit? Welche Trade-offs ergeben sich (z. B. längere Schlüssel ↔ langsamere Performance bei naiver Implementation)?

**Mögliche Anschlussfragen:**
- Wann ist „Schlüssellänge × 2" wirklich „Sicherheit × 2"? (Brute-Force-Aufwand verdoppelt sich pro zusätzlichem Bit – vereinfacht.)
- Welche Modi gibt es bei Blockchiffren? (*Im PDF nicht behandelt.*)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - Triple-DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folie 8
