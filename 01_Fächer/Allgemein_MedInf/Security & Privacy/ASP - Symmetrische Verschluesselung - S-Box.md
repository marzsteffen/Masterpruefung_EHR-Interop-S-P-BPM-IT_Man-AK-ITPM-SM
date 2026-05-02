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

# ASP - Symmetrische Verschlüsselung - S-Box (Substitutionsbox)

> [!info] Kurzdefinition
> Substitutionstabelle als Grundkomponente kryptografischer Algorithmen: Eine S-Box vom Typ m×n ersetzt eine m-stellige Binärzahl durch eine n-stellige Binärzahl gemäß einer festen Tabelle.

## Beschreibung

Folie 15 definiert S-Boxen als „Grundkomponente kryptographischer Systeme". Eine **m×n-Box** bildet einen Eingabe-Bitvektor der Länge m auf einen Ausgabe-Bitvektor der Länge n ab.

**Adressierung der Tabelle (Folie 15, am Beispiel von DES-S-Boxen):**
- Die **äußeren Bits** (das erste und letzte Bit der 6-Bit-Eingabe) bilden den **Zeilenindex** der Substitutionstabelle.
- Die **inneren 4 Bits** bilden den **Spaltenindex**.
- Der Tabelleneintrag an Position (Zeile, Spalte) ist der 4-Bit-Ausgabewert.

**Statisch vs. dynamisch (Folie 16):**
- **Statische S-Boxen:** fester Eintragsinhalt (DES, AES).
- **Dynamische S-Boxen:** schlüsselabhängig generiert (Twofish).

## Bestandteile / Aufbau

| Element | Erklärung |
|---|---|
| Eingabe | m Bits (z. B. 6 Bit bei DES) |
| Ausgabe | n Bits (z. B. 4 Bit bei DES) |
| Tabelle | 2^außere × 2^innere Einträge |
| Adressierung | Äußere Bits = Zeile, innere Bits = Spalte |
| Typ | Statisch oder dynamisch |

## Beispiel

Aus Folie 15 (DES-Beispiel):
```
Eingabe: 100101
Äußere Bits: 1 _ _ _ _ 1 → 11 (Zeile 3)
Innere 4 Bits: 0010 (Spalte 2)
Ausgabe: tabelleneintrag (Zeile 3, Spalte 2)
```

Folie 16 zeigt die DES-S-Box S₅. Aufgabe an die Studierenden: Wert für 101011 ermitteln.
- Zeile aus äußeren Bits 1_____1 → 11 = Zeile 3 (00, 01, 10, 11 → 4 Zeilen).
- Spalte aus inneren 4 Bits: 0101 → Spalte 5.
- Wert: laut Tabelle in S₅ Zeile „11", Spalte „0101" → 1110.

## Abgrenzung

- S-Boxen liefern die **Nichtlinearität** im Algorithmus – ohne sie wäre die gesamte Konstruktion eine lineare Funktion und damit kryptografisch wertlos. *Diese Aussage ist im PDF nicht enthalten*; Folie 15 nennt nur „Grundkomponente kryptographischer Systeme".
- DES und AES haben statische S-Boxen, Twofish dynamische.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine S-Box, und welche Rolle spielt sie in einem Block-Verschlüsselungsverfahren?

**Anwendungsfrage:** Bestimme den Ausgabewert einer S-Box für eine gegebene 6-Bit-Eingabe (Adressierungsschema: äußere Bits → Zeile, innere → Spalte).

**Diskussionsfrage:** Warum sind S-Boxen kryptografisch entscheidend? (Stichwort: Nichtlinearität, Konfusion im Sinn von Shannon.) Welcher Unterschied besteht zwischen statischen und dynamischen S-Boxen, und welche Vor-/Nachteile haben sie?

**Mögliche Anschlussfragen:**
- Welche Konstruktionsprinzipien stehen hinter den DES-S-Boxen? (*Im PDF nicht behandelt – S-Boxen wurden seinerzeit von der NSA designt; gegen differenzielle Kryptoanalyse besonders robust.*)
- Wie viele Eingänge/Ausgänge haben die DES- bzw. AES-S-Boxen? (DES: 6→4 Bit; AES: 8→8 Bit – AES-Größe *im PDF nicht angegeben*.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Feistel-Funktion]]
- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folien 15, 16

## Ergänzung außerhalb der Vorlesung

S-Boxen liefern die in der Kryptografie unverzichtbare **Konfusion** (im Sinn von Shannons Designprinzipien); ohne sie wäre die Verschlüsselung eine lineare Abbildung und durch Algebra brechbar. AES verwendet eine 8-zu-8-Bit-S-Box, die mathematisch über die multiplikative Inverse im Galois-Feld GF(2⁸) konstruiert ist – also nicht willkürlich, sondern mit nachweisbar guten Eigenschaften gegen lineare und differenzielle Kryptoanalyse.
