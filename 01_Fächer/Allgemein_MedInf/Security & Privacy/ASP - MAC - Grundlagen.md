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

# ASP - MAC - Grundlagen (Message Authentication Codes)

> [!info] Kurzdefinition
> Message Authentication Code: Sammelbegriff für Verfahren, die Integrität und Authentizität einer Nachricht über einen geheimen symmetrischen Schlüssel sicherstellen. Wichtige Vertreter: HMAC (Hash-basiert) und CMAC (Block-Cipher-basiert).

## Beschreibung

Folie 9 stellt MACs als „Obergruppe verschiedener Funktionen" vor. Zwei Vertreter werden konkret behandelt:

**HMAC – Hash-based Message Authentication Code:**
- Berechnung mit Hash + geheimer symmetrischer Schlüssel (z. B. AES).
- Ablauf laut Folie: Input → Hash-Funktion → Hash Value → Verschlüsselung mit symmetrischem Schlüssel → HMAC.
- Funktioniert auf beliebigen Hash-Funktionen (z. B. SHA-256).

**CMAC – Cipher-based Message Authentication Code:**
- Berechnet als „letzter verschlüsselter Block der Nachricht bei Blockverschlüsselung".
- Ablauf laut Folie: Input → Verschlüsselung (Block-Verschlüsselung) → letzter verschlüsselter Block (CMAC).

**Kerneigenschaft (Folie 9, rechte Anmerkung):** „Integrität kann nur durch einen bestimmten Empfänger (der im Besitz des symmetrischen Schlüssels ist) geprüft werden."

Daraus folgt die zentrale Schwäche von MACs: **Keine Non-repudiation.** Da beide Seiten den geheimen Schlüssel kennen, kann der Empfänger nicht beweisen, dass die Nachricht vom Sender und nicht von ihm selbst stammt.

## Bestandteile / Aufbau

| MAC-Variante | Baut auf | Schlüsselart | Typischer Einsatz |
|---|---|---|---|
| HMAC | Hash-Funktion (z. B. SHA-256) | symmetrisch | TLS, JWT-Signatur (HS256), API-Authentifizierung |
| CMAC | Blockchiffre (z. B. AES) | symmetrisch | gerätenahe Sicherheit, AES-CCM-Modus |

## Beispiel

Aus Folie 9: HMAC-Beispiel `C887F75DD…` als Tag, das mit der Nachricht „Nachricht" mitgesendet wird. Empfänger kann den HMAC mit demselben Schlüssel verifizieren. Bei CMAC wird die Nachricht im Block-Modus verschlüsselt; der letzte Ciphertext-Block ist der MAC.

## Abgrenzung

- **MAC vs. [[ASP - Hash - Funktion]] (reiner Hash):** Reiner Hash hat keinen Schlüssel und schützt nur, wenn der Hash separat gesichert wird. MAC bindet einen geheimen Schlüssel ein – Eve kann den MAC ohne Schlüssel nicht selbst berechnen.
- **MAC vs. [[ASP - Digitale Signatur - Grundlagen]]:** Signatur nutzt asymmetrische Schlüssel und liefert zusätzlich Non-repudiation. MAC liefert nur Integrität + Authentizität gegenüber dem Schlüsselbesitzer-Paar.
- **HMAC vs. CMAC:** HMAC braucht eine Hash-Funktion, CMAC eine Blockchiffre. Wahl meist abhängig davon, was die Plattform schon hardwarebeschleunigt unterstützt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein MAC, und welche zwei konkreten Varianten kennen Sie? Was ist der Unterschied zwischen HMAC und CMAC?

**Anwendungsfrage:** Skizzieren Sie den Aufbau eines HMAC. Was wird wann mit welchem Schlüssel gemacht?

**Diskussionsfrage:** Welche Schutzziele liefert ein MAC – und welches Schutzziel liefert er nicht, das eine digitale Signatur leisten würde? Diskutieren Sie die Konsequenzen für Anwendungsfälle, in denen ein Beweis gegenüber Dritten erforderlich ist (z. B. signierte ärztliche Verordnung).

**Mögliche Anschlussfragen:**
- Warum erfüllt MAC keine Non-repudiation?
- Wie hängt HMAC mit der zugrunde liegenden Hash-Funktion zusammen? Wenn die Hash-Funktion gebrochen ist, ist HMAC dann automatisch unsicher? (Nicht direkt – HMAC hat zusätzliche Sicherheits-Garantien gegen Hash-Schwächen.)
- In welchem Modus liefert AES gleichzeitig Verschlüsselung und MAC? (AEAD-Modi wie AES-GCM – im PDF nicht behandelt.)

## Verwandt

- [[ASP - Hash - Funktion]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Symmetrische Verschluesselung - AES]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Security Eigenschaften - Non-repudiation]]
- [[ASP - Schutzmethoden - Uebersicht]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folie 9

## Ergänzung außerhalb der Vorlesung

Die HMAC-Konstruktion ist standardisiert in RFC 2104; sie ist robuster als naive „Hash(Schlüssel ‖ Nachricht)"-Konstruktionen, die für Length-Extension-Angriffe anfällig sind. CMAC (NIST SP 800-38B) ersetzt das ältere CBC-MAC. AEAD-Modi wie AES-GCM oder AES-CCM kombinieren Verschlüsselung und MAC in einer Operation und sind heute die bevorzugte Wahl, wenn Vertraulichkeit *und* Integrität gleichzeitig gefordert sind.
