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

# ASP - Symmetrische Verschlüsselung - DES (Data Encryption Standard)

> [!info] Kurzdefinition
> DES (Data Encryption Standard) ist eine 1977 standardisierte symmetrische Blockchiffre mit 56-Bit-Schlüssel und 64-Bit-Blockgröße, basierend auf einem 16-runden Feistel-Netzwerk. Heute durch AES abgelöst.

## Beschreibung

Eckdaten laut Folien 10–18:

- **Seit 1977 offizieller Standard.**
- **War lange Zeit der am weitesten verbreitete Standard.**
- **Schlüssellänge k = 56 Bits.**
- **Blockverschlüsselung (64 Bits).**
- **Wurde durch Advanced Encryption Standard (AES) abgelöst** (siehe [[ASP - Symmetrische Verschluesselung - AES]]).

**Aufbau (Folien 13, 17):**
1. **Initiale Permutation IP(x)** auf den 64-Bit-Eingabeblock.
2. Block wird in zwei 32-Bit-Hälften L₀ und R₀ geteilt.
3. **16 Verschlüsselungsrunden**, jede ist eine Feistel-Funktion (siehe [[ASP - Symmetrische Verschluesselung - Feistel-Funktion]]):
   - In Runde n: R_(n-1) wird durch Expansionsfunktion auf 48 Bit erweitert, mit dem Rundenschlüssel kₙ (48 Bit) XOR-verknüpft, durch S-Boxen geschickt; das Ergebnis wird mit L_(n-1) per XOR verbunden und ergibt R_n; L_n = R_(n-1).
4. Nach 16 Runden: **Inverse Ausgangs-Permutation IP⁻¹** liefert Ciphertext Y (64 Bits).

**Rundenschlüssel:** k₁, k₂, k₃ … werden vom Hauptschlüssel K abgeleitet (Folie 13).

**Entschlüsselung (Folie 18):** Gleicher Algorithmus, aber Rundenschlüssel werden in **umgekehrter Reihenfolge** angewendet (16 → 1).

## Bestandteile / Aufbau

| Element | Wert |
|---|---|
| Standardisiert | 1977 |
| Schlüssellänge | 56 Bit |
| Blockgröße | 64 Bit |
| Anzahl Runden | 16 |
| Rundenfunktion | Feistel mit Expansion, XOR mit Rundenschlüssel, S-Boxen |
| Initiale/finale Permutation | IP / IP⁻¹ |
| Rundenschlüssellänge | 48 Bit (aus 56-Bit-Hauptschlüssel abgeleitet) |
| Status | Abgelöst durch AES |

## Beispiel

Aus Folie 12: DES-Black-Box mit X (64 Bit Klartext) → DES mit Schlüssel k (56 Bit) → Y (64 Bit Ciphertext).

## Abgrenzung

- **DES vs. [[ASP - Symmetrische Verschluesselung - Triple-DES]]:** 3DES erweitert DES auf 168 Bit Schlüssellänge durch dreifache Anwendung mit unabhängigen Schlüsseln.
- **DES vs. [[ASP - Symmetrische Verschluesselung - AES]]:** AES nutzt kein Feistel-Netzwerk, sondern ein Substitutions-Permutations-Netzwerk; Blockgröße 128 Bit; mindestens 128 Bit Schlüssel; deutlich sicherer.
- DES gilt heute als unsicher gegen Brute Force (56-Bit-Schlüsselraum ist mit moderner Hardware in Stunden bis Tagen durchsuchbar). *Im PDF wird dies nicht explizit beziffert.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist DES, welche Schlüssel- und Blockgröße hat es, und welcher interner Aufbau steckt dahinter?

**Anwendungsfrage:** Skizzieren Sie eine DES-Runde. Wie wird aus dem Hauptschlüssel der Rundenschlüssel? Wie funktioniert die Entschlüsselung?

**Diskussionsfrage:** Warum gilt DES heute als unsicher? Welche zwei Wege gibt es, mit der DES-Schwäche umzugehen, und welche Trade-offs entstehen? (3DES als Übergang vs. AES als Neudesign.)

**Mögliche Anschlussfragen:**
- Was ist eine Feistel-Funktion, und welche Eigenschaft hat sie, die Ent- und Verschlüsselung mit demselben Algorithmus erlaubt?
- Was sind S-Boxen und welche Rolle spielen sie in DES?
- Warum reicht die effektive Schlüssellänge bei 3DES nicht 168 Bit, sondern eher 112 Bit? (Meet-in-the-Middle-Angriff – *im PDF nicht behandelt*.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Feistel-Funktion]]
- [[ASP - Symmetrische Verschluesselung - S-Box]]
- [[ASP - Symmetrische Verschluesselung - Triple-DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]
- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folien 10–18

## Ergänzung außerhalb der Vorlesung

DES wurde 1999 durch das Distributed.net-Projekt mit Spezialhardware (EFF DES Cracker) in unter 24 Stunden gebrochen, was die Ablösung beschleunigte. Effektive Sicherheit von 3DES liegt wegen Meet-in-the-Middle bei ca. 112 Bit, nicht 168. NIST hat 3DES für neue Anwendungen 2017 für veraltet erklärt; vollständige Abschaltung war 2023 vorgesehen.
