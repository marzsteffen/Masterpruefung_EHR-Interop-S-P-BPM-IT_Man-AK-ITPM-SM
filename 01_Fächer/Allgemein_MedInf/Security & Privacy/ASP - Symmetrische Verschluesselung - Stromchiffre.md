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

# ASP - Symmetrische Verschlüsselung - Stromchiffre

> [!info] Kurzdefinition
> Bauart symmetrischer Verschlüsselung, die Daten **bitweise** verschlüsselt (typischerweise per XOR mit einem Schlüsselstrom) und ohne Mindestanzahl an Zeichen auskommt – ideal für Echtzeitverarbeitung.

## Beschreibung

Eigenschaften der Stromchiffre laut Folie 6:

- **Bitweise Verschlüsselung:** braucht keine Mindestanzahl an Zeichen.
- **Echtzeitverschlüsselung:** eignet sich für Echtzeitübertragung (z. B. bei telemedizinischen Anwendungen).
- **Effiziente Leistung.**
- **Beispiel-Operation:** XOR-Funktion (Exklusiv-Oder-Gatter). Die Folie zeigt XOR auf zwei Bitströmen:
  - 0 ⊕ 1 = 1
  - 1 ⊕ 1 = 0
  - 0 ⊕ 0 = 0

Konzeptuell wird ein Klartext-Bitstrom mit einem Schlüssel-Bitstrom XOR-verknüpft; das Ergebnis ist der Ciphertext-Bitstrom. Entschlüsselung funktioniert symmetrisch: nochmals mit dem gleichen Schlüsselstrom XOR ergibt wieder den Klartext.

## Bestandteile / Aufbau

| Element | Rolle |
|---|---|
| Klartext-Bitstrom | Zu verschlüsselnde Daten |
| Schlüssel-Bitstrom (Keystream) | Aus dem Schlüssel deterministisch generiert |
| XOR-Operation | Verknüpft Klartext und Keystream bitweise |
| Ciphertext-Bitstrom | Ausgabe |

## Beispiel

Aus Folie 6:
```
Bitstream 1: 0,1,0,0,0,1,0
Bitstream 2: 0,1,0,1,0,1,1
XOR:         0,0,0,1,0,0,1
```

## Abgrenzung

- **Stromchiffre vs. [[ASP - Symmetrische Verschluesselung - Blockchiffre]]:** Strom verschlüsselt bitweise und kontinuierlich, Block verschlüsselt feste Bit-Blöcke unabhängig voneinander. Block ist parallelisierbar und bietet laut Vorlesung höhere Sicherheit gegen Datenmanipulation.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Stromchiffre, und worin unterscheidet sie sich von einer Blockchiffre?

**Anwendungsfrage:** Wann wäre eine Stromchiffre einer Blockchiffre vorzuziehen? (Echtzeitverarbeitung, kontinuierliche Datenströme, kleine Datenmengen ohne Padding.)

**Diskussionsfrage:** Welches praktische Risiko birgt die Wiederverwendung des Keystreams in einer XOR-Stromchiffre? (Two-Time-Pad-Problem – nicht im PDF, aber sehr prüfungsnah, siehe Ergänzung.)

**Mögliche Anschlussfragen:**
- Wie hängt die Sicherheit einer Stromchiffre vom Keystream-Generator ab?
- Welche bekannten Stromchiffren gibt es? (Im PDF dieser Vorlesung nicht behandelt.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]
- [[ASP - Symmetrische Verschluesselung - Prinzip]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folie 6

## Ergänzung außerhalb der Vorlesung

XOR mit einem Schlüsselstrom ist nur dann sicher, wenn der Schlüsselstrom *nicht* wiederverwendet wird. Werden zwei Klartexte mit demselben Keystream verschlüsselt, lässt sich durch XOR der beiden Ciphertexte der Keystream herausrechnen. Dieses sogenannte „Two-Time-Pad"-Problem ist ein klassischer Implementationsfehler bei Stromchiffren. Bekannte Stromchiffren in der Praxis: ChaCha20, RC4 (heute unsicher und abgekündigt).
