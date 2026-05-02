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

# ASP - Asymmetrische Verschlüsselung - Faktorisierungsproblem

> [!info] Kurzdefinition
> Mathematische Grundlage von RSA: das Produkt zweier sehr großer Primzahlen lässt sich (klassisch) leicht berechnen, aber aus dem Produkt die Primzahlen zurückzugewinnen, ist mit klassischen Algorithmen praktisch nicht in vertretbarer Zeit machbar.

## Beschreibung

Folie 42 erläutert das Faktorisierungsproblem als Sicherheitsfundament von RSA.

**Kernpunkte:**
- **Beispiel:** Faktor 1: 317 × Faktor 2: 443 = Produkt: 140 431. Gegeben das Produkt, beide Primzahlen zu finden, wird mit wachsender Größe extrem teuer.
- **Primfaktorzerlegung einer 600–1200-stelligen Zahl** ist in überschaubarer Zeit kaum zu schaffen.
- **Allerdings durch Quantencomputer gefährdet!** (laut Folie, in Rot).
- **Menge der Primzahlen als Faktoren entscheidend** – je größer der Pool möglicher Primzahlen, desto sicherer.
- **Unsichere Algorithmen liefern vorhersagbare Primzahlen.** Folie 42 illustriert das mit zwei Pools: 100 000 Primzahlen (sicher) vs. 100 Primzahlen (unsicher).

Damit ergibt sich eine doppelte Sicherheitsanforderung an RSA-Schlüsselerzeugung:
1. **Schlüssellänge muss groß genug sein** (Empfehlung 2048 Bit, siehe [[ASP - Asymmetrische Verschluesselung - RSA]]).
2. **Primzahlen müssen aus einem ausreichend großen, nicht vorhersagbaren Pool stammen** (Zufalls-Generator-Qualität).

## Bestandteile / Aufbau

| Element | Bedeutung |
|---|---|
| Primzahlen p, q | Geheime Faktoren |
| N = p · q | Öffentlicher Modulus |
| Schwierigkeit | Aus N die Primfaktoren p, q zu bestimmen |
| Klassische Komplexität | Subexponentiell – praktisch nicht durchführbar bei genügend großem N |
| Quanten-Komplexität | Polynomial (Shor's Algorithmus, im PDF nur als „durch Quantencomputer gefährdet" angedeutet) |

## Beispiel

Aus Folie 42:
```
Faktor 1: 317  ×  Faktor 2: 443  =  Produkt: 140 431
Aufgabe an die Studierenden: gegeben 140 431, finde Faktor 1 und Faktor 2.
```
Bei dieser Größe noch von Hand machbar, ab einigen hundert Dezimalstellen aber praktisch unlösbar.

## Abgrenzung

- Das Faktorisierungsproblem ist die Sicherheitsbasis von RSA. Andere asymmetrische Verfahren basieren auf anderen Hardness-Annahmen:
  - [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]: Diskreter Logarithmus modulo p.
  - [[ASP - Asymmetrische Verschluesselung - ECC]]: Diskreter Logarithmus auf elliptischen Kurven.
- Alle drei sind durch Quantencomputer (Shor's Algorithmus) gefährdet. Die Suche nach „Post-Quantum"-tauglichen asymmetrischen Verfahren ist ein aktives Forschungsfeld – *im PDF dieser Vorlesung nicht behandelt*.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worauf basiert die Sicherheit von RSA mathematisch?

**Anwendungsfrage:** Skizziere am kleinen Beispiel (z. B. p=317, q=443), wo das „leichte" Multiplizieren und das „harte" Faktorisieren liegen.

**Diskussionsfrage:** Warum ist RSA durch Quantencomputer gefährdet, und welche Konsequenzen hat das für langlebige verschlüsselte Daten? (Stichwort „Harvest now, decrypt later" – im PDF nicht ausgeführt.) Welche Rolle spielt die Qualität des Primzahlen-Generators?

**Mögliche Anschlussfragen:**
- Welche Mindest-Schlüssellänge wird heute für RSA empfohlen? (laut Folie 41: 2048 Bit.)
- Was ist Shor's Algorithmus? (*Im PDF nicht definiert.*)
- Wie hängt die Sicherheit von DH und RSA mathematisch zusammen? (Beide auf zahlentheoretischen Hardness-Annahmen.)

## Verwandt

- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]
- [[ASP - Angriff - Aufzeichnung und Entschluesselung]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folie 42
- Wiederholung in Kapitel 03, Folie 17 – inhaltlich deckungsgleich; der explizite Quantencomputer-Hinweis aus Kapitel 02 fehlt allerdings auf Folie 17.

## Ergänzung außerhalb der Vorlesung

Klassisch: bester bekannter Algorithmus für Faktorisierung großer Zahlen ist das *General Number Field Sieve* (GNFS) mit subexponentieller Laufzeit. Quantum: *Shor's Algorithmus* faktorisiert in polynomieller Zeit – ein hinreichend großer Quantencomputer würde RSA-2048 binnen Stunden brechen. Deshalb arbeiten NIST und andere an Post-Quantum-Krypto-Standardisierung (z. B. Kyber, Dilithium, Falcon).
