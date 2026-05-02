---
fach: asp
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/asp
---

# ASP - PF - Symmetrische Verschluesselung Detail

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Symmetrische Verschlüsselung aus ASP (VL Verschlüsselungsmethoden). Umfasst das Grundprinzip (ein gemeinsamer Schlüssel), die zwei Bauarten Strom- und Blockchiffre mit ihren Eigenschaften, die Algorithmenklassifikation (Schlüssellänge, Funktion, Performance, Modus), historische Einordnung (Cäsar, Enigma), konkrete Algorithmen DES/3DES/AES mit internen Konstruktionen (Feistel-Netzwerk, S-Box, SP-Netzwerk), sowie die Bewertung gegen das Angriffsmodell (Folie 27). ⚠️ Honeypot: AES-Schlüssellängen – im PDF explizit nur AES-128 mit 128-Bit-Schlüssel und 10 Runden gezeigt; AES-192/256 und deren Rundenanzahl sind nur in der Ergänzungs-Sektion dokumentiert.

## Verlinkte Konzepte

- [[ASP - Symmetrische Verschluesselung - Geschichte]]
- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Symmetrische Verschluesselung - Stromchiffre]]
- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]
- [[ASP - Symmetrische Verschluesselung - Unterscheidungsmerkmale]]
- [[ASP - Symmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - Feistel-Funktion]]
- [[ASP - Symmetrische Verschluesselung - S-Box]]
- [[ASP - Symmetrische Verschluesselung - Triple-DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]
- [[ASP - Symmetrische Verschluesselung - Angriffsmodell]]

---

## Karten

### Definition

Frage: Was sind die wesentlichen Eigenschaften von Stromchiffre und Blockchiffre? Für welchen Anwendungsfall eignet sich welche?

?

Antwort: Laut Folien 6–7 (VL Verschlüsselungsmethoden):

| Aspekt | Stromchiffre | Blockchiffre |
|---|---|---|
| **Granularität** | Bitweise | Feste Blöcke (z. B. 64 oder 128 Bit) |
| **Mindestdatenmenge** | Keine – braucht keine Mindestanzahl Zeichen | Blockgröße; Padding nötig falls Klartext nicht passt |
| **Echtzeitfähigkeit** | Ja – eignet sich für Echtzeitübertragung | Nein – wartet auf vollständigen Block |
| **Parallelisierbarkeit** | Nein (sequenziell) | Ja |
| **Sicherheit gegen Datenmanipulation** | Geringer | Höher (laut Folie 7) |
| **Kernoperation** | XOR mit Schlüssel-Bitstrom | Substitution, Permutation, XOR pro Block |
| **Anwendungsfeld** | Echtzeitübertragung (z. B. Telemedizin) | Daten auf Festplatten und Speichermedien |
| **Beispiel-Algorithmen** | *(im PDF nicht genannt)* | DES, 3DES, AES |

**XOR-Beispiel aus Folie 6:** Bitstream 0,1,0,0,0,1,0 ⊕ 0,1,0,1,0,1,1 = 0,0,0,1,0,0,1.

---

Frage: Was ist DES? Nenne seine wesentlichen Eckdaten und den internen Aufbau.

?

Antwort: Laut Folien 10–18 (VL Verschlüsselungsmethoden):

| Merkmal | Wert |
|---|---|
| Voller Name | Data Encryption Standard |
| Standardisiert | 1977 |
| Schlüssellänge | **56 Bit** |
| Blockgröße | **64 Bit** |
| Anzahl Runden | **16** |
| Rundenfunktion | **Feistel-Netzwerk** (Expansion → XOR mit Rundenschlüssel → S-Box → XOR mit linker Hälfte) |
| Rundenschlüssellänge | 48 Bit (aus Hauptschlüssel K abgeleitet) |
| Status | **Abgelöst durch AES** |

**Grundstruktur:** Initiale Permutation IP → Block in zwei 32-Bit-Hälften L₀ / R₀ → 16 Feistel-Runden → Inverse Permutation IP⁻¹ → Ciphertext (64 Bit).

**Entschlüsselung (Folie 18):** Identischer Algorithmus, aber Rundenschlüssel in **umgekehrter Reihenfolge** (16 → 1).

---

Frage: Was ist AES? Nenne Eckdaten, Konstruktionsprinzip und die vier Operationen pro Runde.

?

Antwort: Laut Folien 22–24 (VL Verschlüsselungsmethoden):

| Merkmal | Wert |
|---|---|
| Voller Name | Advanced Encryption Standard |
| Standardisiert | 2000 (NIST), Nachfolger von DES |
| Schlüssellänge | **128 Bit** (im PDF gezeigt) |
| Blockgröße | **128 Bit (16 Byte)** |
| Anzahl Runden | **10** (für AES-128; im PDF gezeigt) |
| Konstruktion | **Substitutions-Permutations-Netzwerk** (kein Feistel) |
| Status | Meistgenutztes und sicherstes Verschlüsselungsverfahren (laut Vorlesung); 128-Bit-Schlüssel dauert länger zu knacken als das angenommene Alter des Universums |

**Vier Operationen pro Runde (Folie 23):**
1. **SubBytes** – Byteersetzung per S-Box
2. **ShiftRows** – Zeilenverschiebung
3. **MixColumns** – Spaltenoperationen
4. **AddRoundKey** – XOR mit Rundenschlüssel

**Abschlussrunde:** wie Hauptrunde, aber **ohne MixColumns**.

**Anwendungen (Folie 24):** WPA-2, IP-Telefonie, Skype, 7-Zip/RAR-Archive.

---

Frage: Was ist eine S-Box, und wie wird sie in DES adressiert?

?

Antwort: Laut Folien 15–16 (VL Verschlüsselungsmethoden):

**Definition:** Eine S-Box (Substitutionsbox) ist eine Grundkomponente kryptografischer Systeme. Eine **m×n-S-Box** ersetzt einen Eingangs-Bitvektor der Länge m durch einen Ausgangs-Bitvektor der Länge n gemäß einer festen Tabelle.

**Adressierungsschema bei DES (Folie 15, 6-Bit-Eingang, 4-Bit-Ausgang):**
- **Äußere Bits** (Bit 1 und Bit 6) → Zeilenindex der Tabelle.
- **Innere 4 Bits** (Bit 2–5) → Spaltenindex der Tabelle.
- Tabelleneintrag an dieser Position = 4-Bit-Ausgabe.

**Beispiel aus Folie 15:** Eingabe 100101 → äußere Bits 1…1 = 11 → Zeile 3; innere Bits 0010 → Spalte 2 → Ausgabewert.

**Statisch vs. dynamisch (Folie 16):**
- **Statisch:** fester Tabelleninhalt, unabhängig vom Schlüssel (DES, AES).
- **Dynamisch:** schlüsselabhängig generiert (Twofish – *im PDF nur als Hinweis*).

---

### Anwendung

Frage: Skizziere die fünf Schritte einer Feistel-Runde in DES. Was passiert bei der Entschlüsselung anders?

?

Antwort: Laut Folien 13–14, 17–18 (VL Verschlüsselungsmethoden):

**Eingabe:** zwei 32-Bit-Hälften L_(n-1) und R_(n-1), sowie Rundenschlüssel k_n (48 Bit).

| Schritt | Eingang | Operation | Ausgang |
|---|---|---|---|
| 1 | R_(n-1) (32 Bit) | **Expansionsfunktion** → bestimmte Bits werden doppelt übernommen | 48 Bit |
| 2 | 48 Bit + k_n (48 Bit) | **XOR** mit Rundenschlüssel | 48 Bit |
| 3 | 48 Bit | **S-Box-Substitution** | 32 Bit |
| 4 | 32 Bit + L_(n-1) | **XOR** | R_n (32 Bit) |
| 5 | R_(n-1) unverändert | direkt weiterreichen | L_n = R_(n-1) |

**Entschlüsselung:** Gleicher Algorithmus, aber Rundenschlüssel in **umgekehrter Reihenfolge** (k_16, k_15, … k_1). Die Feistel-Konstruktion erlaubt das, ohne eine eigene Umkehrfunktion zu benötigen.

---

Frage: Skizziere den vollständigen AES-Verschlüsselungsablauf (AES-128). Welcher Schritt fehlt in der Abschlussrunde?

?

Antwort: Laut Folie 23 (VL Verschlüsselungsmethoden):

1. **Schlüsselexpansion:** Sub-Key-Generator leitet aus dem 128-Bit-Master-Key zehn Rundenschlüssel ab.
2. **Vorrunde:** AddRoundKey – XOR des 128-Bit-Klartexts mit dem 1. Rundenschlüssel.
3. **9 Hauptrunden**, jede besteht aus:
   - SubBytes (Byteersetzung per S-Box)
   - ShiftRows (Zeilenverschiebung)
   - MixColumns (Spaltenoperationen)
   - AddRoundKey (XOR mit Rundenschlüssel)
4. **Abschlussrunde (10. Runde):**
   - SubBytes
   - ShiftRows
   - ~~MixColumns~~ → **entfällt**
   - AddRoundKey (mit dem 10. Rundenschlüssel)
5. **Ausgabe:** 128-Bit-Ciphertext.

**Fehlender Schritt:** MixColumns fällt in der letzten Runde weg. *(Im PDF wird der Grund nicht erklärt.)*

---

Frage: Wie funktioniert Triple-DES? Gib die Verschlüsselungs- und Entschlüsselungsformel an, und was war die Motivation?

?

Antwort: Laut Folie 20 (VL Verschlüsselungsmethoden):

**Motivation:** Die Schlüssellänge von DES (56 Bit) ist zu gering.

**Schema (EDE – Encrypt–Decrypt–Encrypt):**
```
Verschlüsselung: c = Encrypt_k1( Decrypt_k2( Encrypt_k3( m ) ) )
Entschlüsselung: m = Decrypt_k3( Encrypt_k2( Decrypt_k1( c ) ) )
```

| Merkmal | Wert |
|---|---|
| Schlüssellänge | **168 Bit** (3 × 56) |
| Blockgröße | 64 Bit (wie DES) |
| Anzahl unabhängiger Schlüssel | 3 (k1, k2, k3) |
| Schema | EDE (Encrypt–Decrypt–Encrypt) |

**Warum EDE statt EEE?** [Ergänzung] Bei k1 = k2 = k3 reduziert sich EDE auf einfaches DES → Abwärtskompatibilität.

---

Frage: Welche der acht Angriffe aus dem Vorlesungs-Angriffsmodell verhindert symmetrische Verschlüsselung – und welche nicht? (Angriffsmodell-Tabelle aus Folie 27)

?

Antwort: Laut Folie 27 (VL Verschlüsselungsmethoden, unter den Annahmen: Schlüssel nicht kompromittiert, Primitive sicher):

| Angriff | Bewertung | Begründung (Folie 27) |
|---|---|---|
| Nachricht lesen | ✅ verhindert | Daten werden verschlüsselt |
| Traffic Analysis | ⚠️ szenarioabhängig | Meta-Informationen und Nachrichtenzweck können evtl. extrahiert werden |
| Aufzeichnung + nachträgliche Entschlüsselung | ❌ erfolgreich | Kommunikation kann aufgezeichnet und mit gestohlenem Schlüssel entschlüsselt werden |
| Replay | ❌ erfolgreich | Verschlüsselung allein verhindert keinen Replay |
| Modifikation Plaintext | ✅ verhindert | Keine Modifizierung möglich, da Daten verschlüsselt sind |
| Modifikation Ciphertext | ❌ erfolgreich | Angreifer kann Ciphertext hinzufügen/verändern |
| Impersonation | ⚠️ szenarioabhängig | Sym. Verschlüsselung allein gewährleistet keine Authentizität |
| Denial-of-Service | ❌ erfolgreich | Möglich |

**Offene Lücken → Baustein-Antworten:** Replay → Nonces/Zeitstempel; Ciphertext-Manipulation → HMAC/Signatur; Impersonation → Signatur + PKI; Schlüssel-Diebstahl → PFS.

---

### Diskussion

Frage: Warum gilt DES heute als unsicher – und was waren die zwei Wege, mit dieser Schwäche umzugehen?

?

Antwort: Aus den Notes zu DES und 3DES (Folien 10–20, VL Verschlüsselungsmethoden):

**Schwäche:** DES hat nur eine Schlüssellänge von **56 Bit**. Der Schlüsselraum von 2⁵⁶ ≈ 72 Billiarden Möglichkeiten ist mit moderner Hardware durch Brute-Force durchsuchbar. *(Im PDF wird die genaue Zeitdauer nicht beziffert.)*

**Zwei Reaktionen:**

1. **Übergangslösung: Triple-DES (3DES)** – dreifache DES-Anwendung mit drei unabhängigen 56-Bit-Schlüsseln → 168-Bit-Schlüssellänge.
   - Vorteil: bestehende DES-Hardware wiederverwendbar.
   - Nachteil: dreifacher Rechenaufwand, gleiche 64-Bit-Blockgröße, komplexeres Schema.

2. **Neuentwurf: AES** – vollständig neuer Algorithmus, 128-Bit-Blockgröße, mindestens 128-Bit-Schlüssel, SP-Netzwerk. 2000 als NIST-Standard eingeführt.

**Fazit:** 3DES war ein Pragmatismus-Kompromiss für Systeme, die DES bereits implementiert hatten. AES ist der saubere Nachfolger.

---

Frage: Warum hat AES 3DES weitgehend abgelöst? Welche strukturellen Schwächen hat 3DES trotz 168-Bit-Schlüssel?

?

Antwort: Aus den Notes zu DES, 3DES und AES (Folien 20–24, VL Verschlüsselungsmethoden):

**3DES-Schwächen gegenüber AES:**
- **Performance:** dreifacher DES-Aufwand je Block; AES ist auf modernen CPUs deutlich schneller.
- **Blockgröße:** 64 Bit wie DES – nach modernem Standard zu klein. [Ergänzung] Bei großen Datenmengen (≥32 GB unter gleichem Schlüssel) können Birthday-Angriffe (Sweet32) greifen.
- **Effektive Sicherheit** [Ergänzung]: trotz 168-Bit-Schlüssel nur ca. 112 Bit, da Meet-in-the-Middle-Angriffe den Aufwand halbieren. *Diese Bewertung ist im PDF nicht enthalten.*

**AES-Vorteile (laut Folie 22/23):**
- SP-Netzwerk transformiert in jeder Runde alle Bytes (nicht nur eine Hälfte wie beim Feistel).
- 128-Bit-Blockgröße.
- Schlüssel ab 128 Bit; laut Folie: knacken dauert länger als das Alter des Universums.
- Modernes Design (NIST-Wettbewerb 2000), speziell gegen lineare und differenzielle Kryptoanalyse ausgelegt.

---

Frage: Welche Vor- und Nachteile hat symmetrische Verschlüsselung insgesamt? Warum kommt sie trotz ihrer Nachteile in modernen Protokollen weiter zum Einsatz?

?

Antwort: Laut Folie 9 (VL Verschlüsselungsmethoden):

**Vorteile:**
- **Einfaches Schlüsselmanagement lokal** – nur ein Schlüssel für Ver- und Entschlüsselung.
- **Hohe Geschwindigkeit** – Algorithmen basieren auf effizienten Operationen.

**Nachteile:**
- **Schlüsselaustausch-Problem** – Schlüssel muss vorab über einen sicheren Kanal übermittelt werden.
- **Schlüssel darf nicht in unbefugte Hände gelangen.**
- **Skalierungsproblem** – Anzahl paarweiser Schlüssel wächst mit n·(n-1)/2. Bei 10 Teilnehmern = 45 Schlüssel; bei 100 Teilnehmern = 4.950 Schlüssel.

**Warum trotzdem unverzichtbar?** Symmetrische Verschlüsselung bleibt wegen der Geschwindigkeit die Arbeitspferd-Komponente in Protokollen. Das Schlüsselaustausch-Problem wird durch **hybride Verschlüsselung** gelöst: Asymmetrisches Verfahren tauscht den symmetrischen Sitzungsschlüssel sicher aus; danach übernimmt Symmetrisch für die Bulk-Datenverschlüsselung.

---

### Vergleich

Frage: Vergleiche DES, Triple-DES und AES anhand der vier Algorithmen-Unterscheidungsmerkmale (Schlüssellänge, Konstruktion, Blockgröße, Status).

?

Antwort: Laut Folien 8, 10–24 (VL Verschlüsselungsmethoden):

| Merkmal | DES | Triple-DES (3DES) | AES |
|---|---|---|---|
| **Schlüssellänge** | 56 Bit | 168 Bit (3×56) | 128 Bit (im PDF; [Ergänzung]: auch 192/256) |
| **Blockgröße** | 64 Bit | 64 Bit | **128 Bit** |
| **Konstruktion** | Feistel-Netzwerk (16 Runden) | 3× DES – EDE-Schema | SP-Netzwerk (10 Runden bei AES-128) |
| **Rundenschlüssellänge** | 48 Bit | wie DES | aus Master-Key abgeleitet |
| **Status** | Abgelöst (56-Bit zu kurz) | Übergangslösung; weitgehend abgelöst | Aktueller Standard (NIST 2000) |

*(AES-192/256 mit 12/14 Runden: nur in Ergänzung, im PDF nicht gezeigt.)*

---

Frage: Worin unterscheiden sich Feistel-Netzwerk (DES) und Substitutions-Permutations-Netzwerk (AES) strukturell – und was ist der praktische Vor- bzw. Nachteil jedes Ansatzes?

?

Antwort: Aus den Notes zu Feistel-Funktion und AES (VL Verschlüsselungsmethoden):

| Aspekt | Feistel-Netzwerk (DES) | SP-Netzwerk (AES) |
|---|---|---|
| **Transformierte Datenmenge pro Runde** | Nur **eine Hälfte** (32 von 64 Bit) | **Alle Bytes** (128 Bit) |
| **Symmetrie** | Ver- und Entschlüsselung nutzen **denselben Algorithmus** (nur Schlüsselreihenfolge umkehren) | Entschlüsselung erfordert separate Inverse-Operationen |
| **Rundenanzahl** | 16 (mehr nötig, weil nur Hälfte transformiert) | 10 (für AES-128) |
| **Hardware-Vorteil** | Gleiche Schaltung für Ver- und Entschlüsselung nutzbar | Größere Parallelisierbarkeit pro Runde |
| **Vertreter** | DES, Triple-DES | AES |

**Fazit:** Feistel ist elegant durch seine Symmetrie; SP-Netzwerk transformiert in jeder Runde mehr Daten und gilt heute als moderner.

*(Diese explizite Gegenüberstellung ist im PDF nicht ausgeführt – ergibt sich aus den Beschreibungen der beiden Algorithmen.)*

---

## Mögliche Anschlussfragen des Prüfers

- Welche Eigenschaft macht die Cäsar-Chiffre per se unsicher? (Schlüsselraum: nur 25 Verschiebungen.)
- Welches praktische Risiko hat die Wiederverwendung eines XOR-Keystreams? [Ergänzung: Two-Time-Pad-Problem]
- Warum braucht AES eine Schlüsselexpansion?
- Warum entfällt MixColumns in der AES-Abschlussrunde? (Im PDF nicht erklärt.)
- Welche S-Box hat DES, welche Eingabe-/Ausgabelänge? (6 Bit → 4 Bit.)
- Was bedeutet „statische" vs. „dynamische" S-Box? Welches Verfahren hat dynamische? (Twofish.)
- Warum ist das EDE-Schema rückwärtskompatibel mit DES? (k1=k2=k3 → reduziert auf einfaches DES.)
- Welche Schutzziele bleiben bei symmetrischer Verschlüsselung allein offen – und womit werden sie geschlossen?
- Wie viele symmetrische Schlüssel braucht ein Netz aus 100 Teilnehmern paarweise? (100·99/2 = 4.950.)

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
