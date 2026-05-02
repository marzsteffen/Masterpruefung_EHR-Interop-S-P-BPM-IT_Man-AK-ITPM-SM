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

# ASP - Symmetrische Verschlüsselung - Bewertung gegen das Angriffsmodell

> [!info] Kurzdefinition
> Bewertung der acht Angriffe aus dem Einführungs-Angriffsmodell unter symmetrischer Verschlüsselung: Sie verhindert „Nachricht lesen" und „Modifikation Plaintext" zuverlässig, andere Angriffe bleiben offen oder sind szenarioabhängig.

## Beschreibung

Folie 27 listet alle acht Angriffe aus dem Modell der Einführungs-Vorlesung und bewertet, ob symmetrische Verschlüsselung sie verhindern kann. Voraussetzung sind die Annahmen auf Folie 26:

**Annahmen (Folie 26):**
- Geheime Schlüssel (privater/symmetrischer Schlüssel) werden nicht kompromittiert.
- Kryptografische Primitive sind sicher (richtig implementiert).
- Der Angreifer befindet sich in der Kommunikationsverbindung und kann Nachrichten ändern, unterdrücken oder einschleusen.

**Bewertung (Folie 27):**

| Angriff | Bewertung | Begründung laut Folie |
|---|---|---|
| Nachricht lesen | ✅ verhindert | Daten werden verschlüsselt. |
| Indirektes Ableiten von Informationen (Traffic Analysis) | ⚠️ szenarioabhängig | Nicht direkt, aber Zweck der Nachricht und andere Meta-Informationen könnten extrahiert werden. |
| Aufzeichnung + Entschlüsselung mit gestohlenem Schlüssel | ❌ erfolgreich | Kommunikation kann aufgezeichnet und mit gestohlenem Schlüssel entschlüsselt werden. |
| Replay | ❌ erfolgreich | Verschlüsselung allein verhindert keinen Replay-Angriff. |
| Modifikation Plaintext | ✅ verhindert | Keine Modifizierung möglich, da die Daten verschlüsselt sind. |
| Modifikation Ciphertext | ❌ erfolgreich | Ein Angreifer kann einen Ciphertext hinzufügen. |
| Impersonation | ⚠️ szenarioabhängig | Sym. Verschlüsselung allein gewährleistet keine Authentizität. |
| Nachricht unterdrücken (DoS) | ❌ erfolgreich | Möglich. |

**Farbschema laut Vorlesung:** Grün = Angriff unter den genannten Annahmen nicht möglich; Gelb = Auswirkung des Angriffs hängt vom Szenario ab; Rot = Angriff ist erfolgreich.

## Bestandteile / Aufbau

Acht-Punkte-Bewertung wie oben. Daraus ergeben sich offene Schwächen, die in den weiteren Verschlüsselungs- und Authentizitäts-Vorlesungen adressiert werden:
- Schlüsselaustausch (Folge: asymmetrisch / hybrid).
- Replay (Folge: Frische-Mechanismen, Identitätsmanagement-Vorlesung).
- Modifikation Ciphertext (Folge: HMAC, digitale Signatur).
- Impersonation (Folge: Signatur, PKI).

## Beispiel

Beispielhafte Verkettung: Symmetrische Verschlüsselung allein in einem eHealth-Messaging schützt zwar den Inhalt vor Eve, aber Eve kann einen Replay einer alten verschlüsselten Bestellung auslösen oder einen Ciphertext-Block manipulieren – ohne dass die Empfängerseite das ohne weitere Mechanismen erkennen würde.

## Abgrenzung

- Diese Tabelle bewertet nur **symmetrische** Verschlüsselung. Eine identisch strukturierte Bewertung für asymmetrische Verschlüsselung folgt auf Folie 51 ([[ASP - Asymmetrische Verschluesselung - Angriffsmodell]]) – mit ähnlichen, aber nicht gleichen Ergebnissen.
- Die Bewertung gilt unter den expliziten Annahmen von Folie 26. Wird z. B. die Annahme „Schlüssel wird nicht kompromittiert" verletzt, ändert sich die Bewertung von „Aufzeichnung + Entschlüsselung" entsprechend (rot, sofern keine PFS).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Angriffe aus dem Angriffsmodell verhindert symmetrische Verschlüsselung – und welche nicht?

**Anwendungsfrage:** Erkläre für jeden der acht Angriffe, ob symmetrische Verschlüsselung schützt, und falls nicht, warum nicht.

**Diskussionsfrage:** Welche Schutzziele bleiben bei reiner symmetrischer Verschlüsselung offen? Mit welchen Bausteinen werden sie geschlossen? (Authentizität → HMAC/Signatur; Frische → Nonce/Zeitstempel; Schlüsselaustausch → asymmetrisch.)

**Mögliche Anschlussfragen:**
- Wie ändert sich die Bewertung, wenn die Annahme „Schlüssel sicher" gelockert wird?
- Wie wirkt sich der Übergang zur hybriden Verschlüsselung auf das Tabellenbild aus?

## Verwandt

- [[ASP - Asymmetrische Verschluesselung - Angriffsmodell]]
- [[ASP - Angriff - Nachricht lesen]]
- [[ASP - Angriff - Traffic Analysis]]
- [[ASP - Angriff - Aufzeichnung und Entschluesselung]]
- [[ASP - Angriff - Replay]]
- [[ASP - Angriff - Modifikation Plaintext]]
- [[ASP - Angriff - Modifikation Ciphertext]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Angriff - Denial-of-Service]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folien 25–27 (Annahmen + Tabelle)
