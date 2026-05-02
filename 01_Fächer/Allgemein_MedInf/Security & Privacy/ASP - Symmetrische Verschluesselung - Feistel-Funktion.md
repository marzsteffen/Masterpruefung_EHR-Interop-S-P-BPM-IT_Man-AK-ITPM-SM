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

# ASP - Symmetrische Verschlüsselung - Feistel-Funktion

> [!info] Kurzdefinition
> Konstruktionsprinzip einer Block-Verschlüsselungs-Runde, bei dem der Datenblock in zwei Hälften geteilt wird; eine Hälfte wird durch eine Rundenfunktion mit dem Rundenschlüssel verarbeitet und mit der anderen Hälfte XOR-verknüpft, dann werden die Hälften vertauscht.

## Beschreibung

Die Vorlesung benennt die Feistel-Funktion als „Runden-Funktion" innerhalb von DES (Folien 13, 17).

**Aufbau einer Feistel-Runde laut Folien 14 und 17:**
1. Eingabe: zwei 32-Bit-Hälften L₀ und R₀.
2. R₀ wird durch eine **Expansionsfunktion** auf 48 Bit erweitert (genaue Bit-Mapping-Regel auf Folie 14: jede 4-Bit-Gruppe wird auf 6 Bit ausgedehnt durch Mitübernahme benachbarter Bits).
3. Die expandierten 48 Bits werden mit dem 48-Bit-Rundenschlüssel kₙ **XOR-verknüpft**.
4. Das Ergebnis geht in eine **S-Box** (Substitutionsbox – siehe [[ASP - Symmetrische Verschluesselung - S-Box]]); Output sind wieder 32 Bit.
5. Diese 32 Bit werden mit L₀ per XOR verknüpft → **R₁**.
6. **L₁ = R₀** (die rechte Hälfte wandert unverändert nach links).

**Wichtige strukturelle Eigenschaft (im PDF nicht ausdrücklich erklärt, ergibt sich aus der Konstruktion):** Ent- und Verschlüsselung verwenden denselben Algorithmus; nur die Reihenfolge der Rundenschlüssel wird umgekehrt (Folie 18 macht das für DES explizit).

## Bestandteile / Aufbau

| Schritt | Eingang | Operation | Ausgang |
|---|---|---|---|
| 1 | R₀ (32 Bit) | Expansionsfunktion | 48 Bit |
| 2 | 48 Bit + kₙ (48 Bit) | XOR | 48 Bit |
| 3 | 48 Bit | S-Box-Substitution | 32 Bit |
| 4 | 32 Bit + L₀ (32 Bit) | XOR | R₁ (32 Bit) |
| 5 | R₀ | unverändert weiterreichen | L₁ (32 Bit) |

## Beispiel

Folie 14 zeigt die Expansionsregel als Bit-Tabelle: Eingabe 32 Bits werden auf 48 Bits expandiert, indem bestimmte Bits doppelt übernommen werden, z. B. Bits „1 2 3 4" werden zu „32 1 2 3 4 5".

## Abgrenzung

- **Feistel-Netzwerk vs. SP-Netzwerk:** AES verwendet kein Feistel-Netzwerk, sondern ein Substitutions-Permutations-Netzwerk (alle Bits werden in jeder Runde transformiert, nicht nur eine Hälfte). Diese Abgrenzung wird *im PDF nicht explizit gezogen*, ist aber prüfungsrelevant.
- Der praktische Vorteil von Feistel: Ver- und Entschlüsselung können dieselbe Hardware/Implementation nutzen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Feistel-Funktion, und in welchem Algorithmus kommt sie zum Einsatz?

**Anwendungsfrage:** Skizziere eine Feistel-Runde inklusive Expansion, XOR mit Rundenschlüssel, S-Box und Hälften-Vertauschung. Was passiert bei der Entschlüsselung anders?

**Diskussionsfrage:** Welcher strukturelle Vorteil ergibt sich aus dem Feistel-Prinzip im Vergleich zu einem SP-Netzwerk – und welcher Nachteil? (Vorteil: Symmetrie zwischen Ver- und Entschlüsselung. Nachteil: pro Runde wird nur die halbe Datenbreite kryptografisch transformiert, daher mehr Runden nötig.)

**Mögliche Anschlussfragen:**
- Was ist eine S-Box?
- Wie wird der Rundenschlüssel aus dem Hauptschlüssel abgeleitet? (*Im PDF auf Folie 13 nur als „werden von Schlüssel K abgeleitet" angerissen, nicht im Detail erklärt.*)
- Welche Algorithmen außer DES verwenden Feistel-Netzwerke? (Triple-DES, Blowfish, Twofish – *im PDF nicht behandelt*.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - S-Box]]
- [[ASP - Symmetrische Verschluesselung - Triple-DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folien 13, 14, 17, 18

## Ergänzung außerhalb der Vorlesung

Die Feistel-Konstruktion stammt von Horst Feistel (IBM, 1970er) und ist die Grundlage von DES, Triple-DES, Blowfish und Twofish. Strukturelle Eigenschaft: Wenn die Rundenfunktion F sicher genug ist, ist nach genügend Runden auch ohne Umkehrbarkeit von F selbst eine sichere Verschlüsselung möglich – ein in der theoretischen Kryptologie bewiesenes Ergebnis (Luby-Rackoff-Theorem).
