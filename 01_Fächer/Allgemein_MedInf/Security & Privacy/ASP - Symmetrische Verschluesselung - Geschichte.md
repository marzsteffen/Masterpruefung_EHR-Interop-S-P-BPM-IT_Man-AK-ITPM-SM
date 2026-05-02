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

# ASP - Symmetrische Verschlüsselung - Geschichte

> [!info] Kurzdefinition
> Symmetrische Verschlüsselung ist die älteste Verschlüsselungsform – mit historischen Vertretern wie der Cäsar-Verschiebungschiffre und der Enigma-Maschine im Zweiten Weltkrieg.

## Beschreibung

Die Vorlesung verortet symmetrische Verschlüsselung historisch (Folie 4):

- **Älteste Verschlüsselungsform** – seit dem 1. Jahrhundert v. Chr.
- **Cäsar-Verschlüsselung / Verschiebungschiffre:** jedes Zeichen im Klartext wird um eine feste Zahl von Stellen im Alphabet verschoben. Vorlesungs-Beispiel mit Verschiebung um 3 Stellen: „Geheimer Text" → „Jhkhlphu WhAw".
- **Enigma:** erste symmetrische Verschlüsselungs-*Maschine* im Zweiten Weltkrieg. Wurde durch Alan Turing und sein Team entschlüsselt. (Schreibweise im PDF: „Alan Turin" – wohl ein Schreibfehler.)

## Bestandteile / Aufbau

| Vertreter | Zeit | Mechanismus |
|---|---|---|
| Cäsar-Chiffre | 1. Jh. v. Chr. | Buchstabenverschiebung um festen Wert |
| Enigma | 2. Weltkrieg | Elektromechanische Rotor-Maschine |

## Beispiel

Cäsar-Beispiel laut Folie 4:
```
Klartext:  Geheimer Text
Schlüssel: Verschiebung um 3 Stellen
Ciphertext: Jhkhlphu WhAw
```

## Abgrenzung

- Klassische Cäsar-Chiffre und Enigma sind heute kryptografisch wertlos. Sie sind nicht für ihren Sicherheitswert relevant, sondern als historische Einordnung.
- Beide sind „symmetrisch" im weiten Sinn (Sender und Empfänger nutzen denselben Schlüssel/dieselbe Maschineneinstellung), aber keine Stromchiffre und keine Blockchiffre im modernen Sinn.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Beispiele für historische symmetrische Verschlüsselungen kennt man, und seit wann gibt es symmetrische Verschlüsselung?

**Anwendungsfrage:** Verschiebe einen kurzen Klartext mit Cäsar-Chiffre und Schlüssel 3.

**Diskussionsfrage:** Was lehrt der Bruch der Enigma über die Sicherheit damaliger und moderner Verschlüsselung? (Stichworte: Schwächen in der Schlüsselverteilung und in operativen Mustern, nicht in der reinen Mathematik – relevant auch heute.)

**Mögliche Anschlussfragen:**
- Welche Eigenschaft macht Cäsar-Chiffre per se unsicher? (Geringer Schlüsselraum: 25 Verschiebungen.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Symmetrische Verschluesselung - Stromchiffre]]
- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folie 4

## Ergänzung außerhalb der Vorlesung

Die Cäsar-Chiffre hat einen Schlüsselraum von nur 25 möglichen Verschiebungen (modulo 26 Buchstaben), ist also durch reines Durchprobieren in Sekunden zu brechen. Enigma hatte trotz komplexer Rotorkombinatorik strukturelle Schwächen (z. B. dass kein Buchstabe auf sich selbst verschlüsselt wurde), die zusammen mit operativen Fehlern (wiederverwendete Tagesschlüssel, vorhersagbare Wettermeldungen) den Bruch durch Bletchley Park ermöglichten.
