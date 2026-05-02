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

# ASP - Asymmetrische Verschlüsselung - ECC (Elliptische-Kurven-Verfahren)

> [!info] Kurzdefinition
> ECC (Elliptic Curve Cryptography) ist ein asymmetrisches Verfahren auf Basis elliptischer Kurven über endlichen Körpern. Es liefert vergleichbare Sicherheit wie RSA bei deutlich kürzeren Schlüsseln (typisch 128–256 Bit).

## Beschreibung

Folien 46–47 stellen ECC vor:

**Eckpunkte (Folie 46):**
- Mitte 1980 veröffentlicht.
- **Seit 1999 NIST-Standard** (National Institute of Standards and Technology).
- Für Schlüsselaustausch und Signaturverfahren.
- Komplexer mathematischer Hintergrund.
- Basieren auf Punkte-Paare auf elliptischen Kurven.
- **Viel kleinere Schlüssellänge als RSA (128, 192, 256 Bits).**

**Funktionsprinzip (Folie 47):**
- Eine elliptische Kurve ist eine Menge von Punkten (x, y).
- **Wichtige Eigenschaft:** Eine Gerade (Tangente) schneidet die Kurve in 3 Punkten.
- Aus 2 Zahlen (Punkten) wird eine 3. Zahl berechnet (Punkt-Addition R = P + Q, siehe Diagramm).
- Wenn ein Punkt P(x, y) mit einer Zahl n multipliziert wird (skalare Multiplikation), erhält man einen anderen Punkt auf der Kurve.
- **Zahl n, die dabei verwendet wurde, ist praktisch unmöglich rückzuberechnen.** → Das ist die Hardness-Annahme.

**Showcase (Folie 48):** Verweis auf Online-Tools https://8gwifi.org/ecfunctions.jsp und https://8gwifi.org/ecsignverify.jsp.

## Bestandteile / Aufbau

| Element | Bedeutung |
|---|---|
| Elliptische Kurve | Menge von (x, y)-Punkten, mathematisch durch eine Gleichung definiert |
| Punkt-Addition | P + Q = R (geometrisch über Gerade durch P und Q) |
| Skalare Multiplikation | n·P = ein anderer Punkt auf der Kurve |
| Sicherheit | Schwierigkeit, n aus P und n·P zu bestimmen (diskreter Log auf elliptischer Kurve) |
| Schlüssellängen | 128, 192, 256 Bit (laut Folie) |

## Beispiel

Aus Folie 46/47: Diagramm mit elliptischer Kurve, zwei Punkten P und Q, Gerade durch beide schneidet die Kurve in einem dritten Punkt -R; R = P + Q ergibt sich durch Spiegelung an der x-Achse.

## Abgrenzung

- **ECC vs. [[ASP - Asymmetrische Verschluesselung - RSA]]:** Bei vergleichbarer Sicherheit hat ECC drastisch kürzere Schlüssel (z. B. ECC 256 Bit ≈ RSA 3072 Bit). Operationen sind dadurch schneller, Speicherbedarf geringer. Wichtig für Smartcards, mobile Geräte, IoT.
- **ECC vs. [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]:** Klassisches DH operiert in der multiplikativen Gruppe modulo p. ECC führt analoge Operationen auf einer elliptischen Kurve durch (Stichwort ECDH).
- ECC ist genau wie RSA durch Quantencomputer gefährdet (Shor's Algorithmus bricht beide Hardness-Annahmen). *Im PDF dieser Vorlesung nicht explizit erwähnt für ECC, aber für RSA auf Folie 42.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ECC, und auf welchem mathematischen Problem basiert seine Sicherheit?

**Anwendungsfrage:** Vergleiche RSA und ECC hinsichtlich Schlüssellänge, Performance und Anwendungsgebiet. Wann würden Sie ECC bevorzugen? (Mobile Geräte, IoT, Smartcards, schnellere TLS-Handshakes.)

**Diskussionsfrage:** Warum kommt ECC mit so viel kürzeren Schlüsseln aus? (Antwort: Best-known Angriff auf elliptische-Kurven-Diskreter-Log läuft in voller Wurzel der Gruppenordnung; auf RSA-Faktorisierung gibt es subexponentielle Algorithmen, die effektiv kürzere RSA-Schlüssel knacken können – also bei gleichem Sicherheitsniveau braucht RSA längere Schlüssel.)

**Mögliche Anschlussfragen:**
- Was ist eine elliptische Kurve mathematisch? (*Im PDF nicht formal definiert.*)
- Was ist ECDH und ECDSA? (*Im PDF nur indirekt über „Schlüsselaustausch und Signaturverfahren" angedeutet.*)
- Welche Schwächen hat ECC gegen Quantencomputer?

## Verwandt

- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Asymmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folien 46, 47, 48
- Wiederholung in Kapitel 03, Folien 20–23 – nahezu deckungsgleich; in Kap 03 fehlt der Punkt „Für Schlüsselaustausch und Signaturverfahren".

## Ergänzung außerhalb der Vorlesung

Übliche Schlüssellängen-Äquivalenzen (Faustformel, NIST):
- RSA 1024 ≈ ECC 160 Bit (heute beides zu schwach)
- RSA 2048 ≈ ECC 224 Bit
- RSA 3072 ≈ ECC 256 Bit
- RSA 7680 ≈ ECC 384 Bit

Praktisch verbreitete Kurven: NIST P-256 (auch secp256r1, prime256v1), Curve25519 (für ECDH/X25519), Ed25519 (für Signaturen). ECC wird in TLS 1.3, Signal-Protokoll, JWT/JOSE und vielen aktuellen Protokollen bevorzugt eingesetzt. Wie RSA ist ECC durch Quantencomputer (Shor) gefährdet; daher die Forschung an Post-Quantum-Krypto.
