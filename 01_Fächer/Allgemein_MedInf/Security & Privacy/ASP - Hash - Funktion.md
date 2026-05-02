---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Hash - Funktion

> [!info] Kurzdefinition
> Mathematische Einwegfunktion, die eine beliebig lange Eingabe auf einen Wert fester Länge abbildet, dabei nicht invertierbar und kollisionsfrei ist. Wird zur Integritätsprüfung von Nachrichten verwendet.

## Beschreibung

Eigenschaften einer Hash-Funktion (Folie 5):

- **Mathematische Einwegfunktion.**
- **Nicht invertierbar** (vom Hash-Wert kann nicht auf die Eingabe geschlossen werden).
- **Kollisionsfrei** (zwei unterschiedliche Eingaben sollen praktisch nie denselben Hash-Wert produzieren).
- **Beispiele aus der Vorlesung:** MD2, SHA-256 („uvm.").

Visualisierung in der Vorlesung: „Hallo Alice" → Hash-Funktion → `487a09209f657a02416b692d2fb1b7e6`. Die Schoko-Muffin-Metapher veranschaulicht die Einweg-Eigenschaft: aus den Zutaten (Schokolade, Eier, Mehl) lässt sich leicht ein Muffin backen, aber aus dem fertigen Muffin nicht mehr die einzelnen Zutaten zurückgewinnen.

**Verwendung zur Integritätsprüfung (Folie 7):**
1. Sender berechnet Hash-Wert der Nachricht.
2. Sender übermittelt Nachricht und Hash-Wert an Empfänger.
3. Empfänger berechnet Hash-Wert der empfangenen Nachricht (mit demselben Algorithmus).
4. Empfänger vergleicht errechneten und empfangenen Hash-Wert.
5. Bei Übereinstimmung: Nachricht unverändert.

**Schwäche reines Hash:** Wenn der Angreifer nicht nur die Nachricht, sondern auch den mitgesendeten Hash-Wert manipulieren kann, fällt die Prüfung positiv aus. Reine Hashes schützen nur, wenn der Hash-Wert über einen separaten, sicheren Kanal kommt – sonst braucht es einen [[ASP - MAC - Grundlagen]] oder eine [[ASP - Digitale Signatur - Grundlagen]].

## Bestandteile / Aufbau

| Eigenschaft | Bedeutung |
|---|---|
| Beliebige Eingabelänge | Funktioniert auf Nachrichten jeder Länge |
| Feste Ausgabelänge | z. B. 256 Bit bei SHA-256 |
| Einwegfunktion | Aus Hash kann Eingabe nicht rekonstruiert werden |
| Kollisionsfreiheit | Zwei verschiedene Eingaben → praktisch nie gleicher Hash |
| Determinismus | Gleiche Eingabe → immer gleicher Hash |

## Beispiel

Aus Folie 5: Eingabe „Hallo Alice" → Hash-Wert `487a09209f657a02416b692d2fb1b7e6` (32 hexadezimale Stellen, also 128 Bit – passt zu MD5/MD-Familie; SHA-256 hätte 64 hex Stellen).

## Abgrenzung

- **Hash vs. Verschlüsselung:** Verschlüsselung ist umkehrbar (mit Schlüssel), Hash ist es definitionsgemäß nicht.
- **Hash vs. [[ASP - MAC - Grundlagen]]:** Reiner Hash hat keinen Schlüssel und schützt nur dann gegen Manipulation, wenn der Hash-Wert separat gesichert wird. MAC bindet einen Schlüssel ein.
- **Hash vs. [[ASP - Digitale Signatur - Grundlagen]]:** Signatur = Hash plus asymmetrische Verschlüsselung mit Private Key. Liefert zusätzlich Authentizität und Non-repudiation.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Hash-Funktion und welche Eigenschaften muss sie für kryptografische Anwendungen erfüllen?

**Anwendungsfrage:** Skizziere den Workflow zur Integritätsprüfung mit Hash. Wo liegt die Schwachstelle, wenn der Hash zusammen mit der Nachricht über denselben unsicheren Kanal übertragen wird?

**Diskussionsfrage:** MD2 ist im PDF als Algorithmus-Beispiel genannt, gilt aber heute als unsicher (ähnlich MD5, SHA-1). Welche Eigenschaft eines Hash-Algorithmus muss verletzt sein, damit er praktisch unsicher wird? (Antwort: Kollisionsfreiheit – wenn man zwei Eingaben mit gleichem Hash konstruieren kann, lässt sich eine Signatur einer Nachricht für eine andere Nachricht „wiederverwenden".)

**Mögliche Anschlussfragen:**
- Welche Hash-Algorithmen gelten heute als sicher? (SHA-256, SHA-3 – im PDF nicht ausgewiesen.)
- Was ist der Unterschied zwischen Kollisions- und Pre-image-Resistance? (*Im PDF nicht behandelt.*)
- Wie viele Bits sollten ein moderner Hash-Wert haben? (Mindestens 256 – im PDF nicht beziffert.)

## Verwandt

- [[ASP - MAC - Grundlagen]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Angriff - Modifikation Plaintext]]
- [[ASP - Angriff - Modifikation Ciphertext]]
- [[ASP - Schutzmethoden - Uebersicht]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folien 4–7

## Ergänzung außerhalb der Vorlesung

MD2 (1989) und MD5 (1991) sind heute unsicher und werden für sicherheitsrelevante Zwecke nicht mehr eingesetzt; SHA-1 (1995) gilt seit 2017 als praktisch gebrochen (Google SHAttered-Angriff). Aktuelle Empfehlungen sind die SHA-2-Familie (insbesondere SHA-256, SHA-384, SHA-512) oder SHA-3 (Keccak, NIST-Standard 2015). Drei kryptografische Eigenschaften werden formal unterschieden: Pre-image-Resistance (aus Hash → Eingabe), Second-Pre-image-Resistance (zu gegebener Eingabe eine zweite mit gleichem Hash) und Collision-Resistance (zwei beliebige Eingaben mit gleichem Hash).
