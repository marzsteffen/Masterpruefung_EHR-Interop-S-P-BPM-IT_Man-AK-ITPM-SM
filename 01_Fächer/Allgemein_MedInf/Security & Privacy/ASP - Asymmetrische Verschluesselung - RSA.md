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

# ASP - Asymmetrische Verschlüsselung - RSA

> [!info] Kurzdefinition
> RSA ist ein 1977 von Rivest, Shamir und Adleman veröffentlichtes asymmetrisches Verschlüsselungs- und Signaturverfahren. Seine Sicherheit basiert auf dem Faktorisierungsproblem großer Primzahlprodukte. Empfehlung: mindestens 2048 Bit Schlüssellänge.

## Beschreibung

Eckdaten laut Folien 41, 44.

**Eckpunkte (Folie 41):**
- 1977 veröffentlicht durch Rivest, Shamir und Adleman.
- Am weitesten eingesetztes asymmetrisches Verfahren.
- Eignet sich für: **Signaturverfahren** und **Verschlüsselungsverfahren**.
- Relativ einfach zu implementieren.
- Im Vergleich zu sym. TripleDES oder AES ca. um Faktor 100 (und mehr) langsamer.
- **Große Schlüssellänge (Empfehlung mind. 2048 Bit).**
- **Basiert auf Faktorisierungsproblem** (siehe [[ASP - Asymmetrische Verschluesselung - Faktorisierungsproblem]]).

**Funktionsweise (Folie 44):**

Variablen:
- **N**: öffentliche Zahl (Produkt 2er Primzahlen p, q)
- **e**: Teil des öffentlichen Schlüssels
- **p, q**: Primzahlen
- **φ(N)**: Anzahl teilerfremder Zahlen zu N
- **d**: privater Schlüssel
- **m**: Klartext / Plaintext
- **c**: Geheimtext / Ciphertext

**Verschlüsseln (mit öffentlichem Schlüssel (e, N)):**
```
c = mᵉ mod N
```
Beispiel: m = 9, c = 9⁴⁷ mod 77 (mit beispielhaften e=47, N=77).

**Entschlüsseln (mit privatem Schlüssel (d, N)):**
```
m = cᵈ mod N
```

**Schlüsselgenerierung (im PDF nicht detailliert ausgeführt):** Wahl zweier großer Primzahlen p, q; N = p·q; φ(N) = (p-1)(q-1); Wahl von e mit ggT(e, φ(N)) = 1; d ist das modulare Inverse von e modulo φ(N). *Diese Schritte sind im PDF dieser Vorlesung nicht explizit ausgeführt – die Folie zeigt nur die Tabelle mit den Variablen.*

**Showcase (Folie 43):** Verweis auf Online-Tool [https://tools.justus-d.de/rsa/](https://tools.justus-d.de/rsa/) für Schlüsselgenerierung, Ver- und Entschlüsselung.

## Bestandteile / Aufbau

| Element | Wert |
|---|---|
| Veröffentlicht | 1977 |
| Erfinder | Rivest, Shamir, Adleman |
| Schlüssellänge (Empfehlung) | mind. 2048 Bit |
| Sicherheits-Annahme | Faktorisierung großer Zahlen ist hart |
| Verwendung | Verschlüsselung + Signatur |
| Public Key | (e, N) |
| Private Key | (d, N) |
| Verschlüsseln | c = mᵉ mod N |
| Entschlüsseln | m = cᵈ mod N |

## Beispiel

Folie 44 zeigt: m = 9, e = 47, N = 77. Berechnung c = 9⁴⁷ mod 77 → eine konkrete Zahl modulo 77. Die Entschlüsselung c²³ mod 77 (d = 23 ist passendes modulares Inverses zu e=47 mod φ(77)=60) liefert wieder 9.

## Abgrenzung

- **RSA vs. [[ASP - Asymmetrische Verschluesselung - ECC]]:** RSA basiert auf Faktorisierung, ECC auf elliptischen Kurven. ECC braucht viel kleinere Schlüssel bei vergleichbarer Sicherheit (128–256 Bit ECC ≈ 2048+ Bit RSA).
- **RSA vs. [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]:** RSA macht direkte Verschlüsselung und Signatur. DH macht nur Schlüsselaustausch.
- RSA ist **durch Quantencomputer gefährdet** (Shor's Algorithmus bricht das Faktorisierungsproblem effizient – siehe Hinweis auf Folie 42).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist RSA, wer hat es entwickelt, und auf welchem mathematischen Problem basiert seine Sicherheit?

**Anwendungsfrage:** Schreibe die RSA-Verschlüsselungs- und Entschlüsselungsformel auf. Wer hat welchen Schlüssel? Welche Schlüssellänge wird empfohlen?

**Diskussionsfrage:** Warum ist RSA durch Quantencomputer gefährdet? Welche Alternativen gibt es? (Post-Quantum-Krypto – im PDF dieser Vorlesung nicht behandelt.) Welcher Trade-off besteht zwischen RSA und ECC?

**Mögliche Anschlussfragen:**
- Wie hängen e und d mathematisch zusammen? (d ist modulares Inverses von e modulo φ(N).)
- Warum ist die Wahl der Primzahlen entscheidend?
- Wie schnell ist RSA im Vergleich zu AES? (Faktor 100 oder mehr langsamer laut Folie 41; Größenordnung 10 000–100 000× laut Folien 34/52.)

## Verwandt

- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - Faktorisierungsproblem]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folien 40, 41, 43, 44
- Wiederholung in Kapitel 03, Folien 15, 16, 18, 19 – inhaltlich deckungsgleich.

## Ergänzung außerhalb der Vorlesung

RSA-Schlüsselgenerierung in Kurzform:
1. Zwei große Primzahlen p, q wählen → N = p · q.
2. φ(N) = (p-1)(q-1).
3. e wählen mit ggT(e, φ(N)) = 1 (oft e = 65537).
4. d = modulares Inverses von e mod φ(N).
5. Public Key (e, N), Private Key (d, N).

In der Praxis wird RSA nie direkt auf den Klartext angewandt, sondern mit Padding (OAEP für Verschlüsselung, PSS für Signatur) und meist nur für einen symmetrischen Sitzungsschlüssel (hybride Verschlüsselung) bzw. einen Hashwert (Signatur).
