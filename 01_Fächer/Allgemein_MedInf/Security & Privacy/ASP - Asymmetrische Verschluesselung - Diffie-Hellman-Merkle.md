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

# ASP - Asymmetrische Verschlüsselung - Diffie-Hellman-Merkle Schlüsselaustausch

> [!info] Kurzdefinition
> Schlüsselaustausch-Protokoll, bei dem zwei Parteien aus öffentlich übertragenen Zwischenwerten und einer privaten Zufallszahl je einen identischen gemeinsamen Schlüssel berechnen, ohne den Schlüssel selbst je zu übertragen.

## Beschreibung

Folien 37–39 stellen das Verfahren vor:

**Eckpunkte (Folie 37 in Kapitel 02; Folie 7 in Kapitel 03):**
- 1976 veröffentlicht durch Diffie, Hellman und Merkle.
- Kryptografisches Verfahren zur **Berechnung eines gemeinsamen Schlüssels**.
- **Keine Übertragung eines symmetrischen Schlüssels.**
- **Nur Ergebnisse von Rechenoperationen werden übertragen.**
- Mit den Ergebnissen wird der gemeinsame Schlüssel berechnet.
- **Eignet sich nicht zur Erstellung von digitalen Signaturen.**
- **Mathematische Grundlage (laut Kapitel 03, Folie 7):** „Methode basiert auf einer mathematischen Funktion, bei der es leicht ist, eine Richtung zu berechnen (Multiplikation), aber extrem schwierig, sie umzukehren (**diskreter Logarithmus**)."

**Ablauf (Folie 38, am numerischen Beispiel):**

| Schritt | Alice | Bob |
|---|---|---|
| 1 | bestimmt eine Primzahl p und natürliche Zahl g (z. B. p=11, g=6) | erhält p, g |
| 2 | wählt geheime Zufallszahl a (1…p-1), z. B. a=3 | wählt geheime Zufallszahl b (1…p-1), z. B. b=6 |
| 3 | berechnet A = gᵃ mod p = 6³ mod 11 = 7 | berechnet B = gᵇ mod p = 6⁶ mod 11 = 5 |
| 4 | sendet A=7 an Bob | sendet B=5 an Alice |
| 5 | berechnet K1 = Bᵃ mod p = 5³ mod 11 = 4 | berechnet K2 = Aᵇ mod p = 7⁶ mod 11 = 4 |
| 6 | **Schlüssel K1 = K2 = 4** ist auf beiden Seiten identisch | |

**Anschauungsmodell (Folie 39):** Die „Farben"-Analogie zeigt, dass beide Parteien dieselbe gemeinsame Farbe erzeugen, ohne dass ein Lauscher die einzelnen Bestandteile rekonstruieren kann (Annahme: Umkehren des Mischens ist sehr aufwändig).

**Was öffentlich übertragen wird:** p, g, A, B. **Was geheim bleibt:** a, b und der berechnete Schlüssel.

## Bestandteile / Aufbau

| Variable | Bedeutung | Sichtbarkeit |
|---|---|---|
| p | Primzahl | öffentlich |
| g | natürliche Zahl (Generator) | öffentlich |
| a | Alice' geheime Zufallszahl | privat |
| b | Bobs geheime Zufallszahl | privat |
| A = gᵃ mod p | Alice' öffentlicher Wert | öffentlich |
| B = gᵇ mod p | Bobs öffentlicher Wert | öffentlich |
| K = Bᵃ mod p = Aᵇ mod p | gemeinsamer Schlüssel | privat |

## Beispiel

Numerisches Beispiel aus Folie 38:
- p = 11, g = 6
- a = 3 → A = 6³ mod 11 = 216 mod 11 = 7
- b = 6 → B = 6⁶ mod 11 = 46656 mod 11 = 5
- K1 = 5³ mod 11 = 125 mod 11 = 4
- K2 = 7⁶ mod 11 = 117649 mod 11 = 4
- Gemeinsamer Schlüssel: 4

## Abgrenzung

- **Diffie-Hellman vs. [[ASP - Asymmetrische Verschluesselung - RSA]]:** RSA verschlüsselt Daten direkt mit Public/Private Key und kann auch signieren. DH macht ausschließlich Schlüsselaustausch und kann nicht signieren.
- **Diffie-Hellman vs. asymmetrischer Schlüsseltransport:** Beim Schlüsseltransport (z. B. mit RSA) wird ein symmetrischer Schlüssel mit dem Public Key des Empfängers verschlüsselt übertragen. Bei DH wird gar kein Schlüssel übertragen, sondern beidseitig berechnet. DH ermöglicht (mit ephemeren Werten) Perfect Forward Secrecy, RSA-Schlüsseltransport nicht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Diffie-Hellman-Merkle, und wozu dient es?

**Anwendungsfrage:** Rechne ein einfaches Beispiel mit kleinen Zahlen durch (p, g, a, b → A, B → K). Welche Werte sind öffentlich, welche privat?

**Diskussionsfrage:** Warum ist DH nicht für digitale Signaturen geeignet? (Antwort: DH ist konstruiert für Schlüsselvereinbarung, nicht für Authentifizierung; es liefert kein zur Identität gehörendes Beweismittel über Daten.) Wie hängt DH mit Perfect Forward Secrecy zusammen?

**Mögliche Anschlussfragen:**
- Auf welchem mathematischen Problem basiert die Sicherheit von DH? (Diskreter Logarithmus modulo p – *im PDF nicht ausdrücklich genannt*; siehe Ergänzung.)
- Welche Schwäche hat DH gegen Man-in-the-Middle-Angriffe? (DH allein authentifiziert die Gegenseite nicht; deshalb braucht es zusätzlich Signaturen / Zertifikate.)

## Verwandt

- [[ASP - Schluesselaustausch - Problem]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Kryptografie - Perfect Forward Secrecy]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folien 37, 38, 39
- Wiederholung in Kapitel 03 (`IVL_ADSP_Asymmetrische_Verschlüsselung…pdf`, 28.10.2024), Folien 7–9 – inhaltlich deckungsgleich, mit zusätzlich der expliziten Nennung des diskreten Logarithmus auf Folie 7.

## Ergänzung außerhalb der Vorlesung

Praxis-Details zum diskreten Logarithmus (über die Folien hinaus): heute mind. 2048 Bit für klassisches DH, deutlich kleiner für ECDH. Reines DH bietet keinen Schutz gegen Man-in-the-Middle-Angriffe, weil keine der beiden Seiten die Identität der Gegenseite verifiziert – produktive Protokolle wie TLS kombinieren DH deshalb mit signierten Zertifikaten. Werden in jeder Sitzung *frische* a und b verwendet (ephemerales DH, „DHE" / „ECDHE"), erhält man Perfect Forward Secrecy.
