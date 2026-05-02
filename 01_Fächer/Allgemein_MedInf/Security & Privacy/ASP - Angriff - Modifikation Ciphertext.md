---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Einfuehrung und Motivation]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Angriff - Verändern der verschlüsselten Nachricht

> [!info] Kurzdefinition
> Eve fängt eine verschlüsselte Nachricht ab und modifiziert den Ciphertext, ohne den Klartext zu kennen. Schutzziel: Integrität. Schutz: zusätzliche HMAC oder digitale Signatur.

## Beschreibung

Folie 24 beschreibt den Angriff:

- **Angriff:** Eve fängt geschützte (verschlüsselte) Nachrichten ab und modifiziert sie nach ihren Bedürfnissen.
- **Auswirkung:** Integrität
- **Typische Sicherheitsfunktion:** Verschlüsselung allein schützt die Nachricht nicht vor Veränderung; zusätzlich HMAC oder digitale Signatur notwendig.

Die Vorlesungsaussage ist die zentrale Lehre: **Verschlüsselung ≠ Integritätsschutz.** Eve kann einen Ciphertext „kaputt" machen, ohne ihn entschlüsseln zu müssen. Bei manchen Modi (z. B. Stromchiffren oder unauthenticated CTR-Mode) hat Bit-Flipping im Ciphertext direkte vorhersagbare Auswirkungen im Klartext.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Angreifer-Aktion | Modifikation des Ciphertexts |
| Klartext-Zugriff | Nicht erforderlich |
| Verletztes Schutzziel | Integrität |
| Schutzmechanismus | HMAC oder digitale Signatur **zusätzlich** zur Verschlüsselung |

## Beispiel

*Im PDF nicht ausgeführt.* In der Praxis: ein TLS-Cipher wie AES-CBC ohne MAC (theoretisch) wäre angreifbar; deshalb nutzen moderne Modi (AEAD wie AES-GCM) Authentication eingebaut. *AEAD im PDF nicht erwähnt.*

## Abgrenzung

- **Modifikation Ciphertext vs. [[ASP - Angriff - Modifikation Plaintext]]:** Beim Ciphertext-Angriff weiß Eve nicht, was sie verändert – Modifikationen können trotzdem Schaden anrichten (siehe Bit-Flipping).
- Klärt die häufige Fehlannahme: „Wenn die Daten verschlüsselt sind, sind sie auch fälschungssicher". Das stimmt nicht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Angriff „Verändern der verschlüsselten Nachricht"? Welches Schutzziel ist betroffen?

**Anwendungsfrage:** Welche zwei Krypto-Bausteine kombinieren Sie, um sowohl Vertraulichkeit als auch Integrität sicherzustellen? Welche Reihenfolge ist üblich (Encrypt-then-MAC vs. MAC-then-Encrypt)? (*Im PDF dieser Vorlesung nicht erläutert.*)

**Diskussionsfrage:** Warum ist der Mythos „Verschlüsselung schützt automatisch vor Manipulation" weit verbreitet, und welche reale Folge hat er in unsicher gebauten Systemen? Welche Rolle spielt AEAD (Authenticated Encryption with Associated Data) heute? (*AEAD im PDF nicht behandelt.*)

**Mögliche Anschlussfragen:**
- Was passiert beim sogenannten Bit-Flipping-Angriff? (*Im PDF nicht behandelt.*)
- Wie schützt TLS sich gegen Ciphertext-Manipulation? (*Im PDF nicht erklärt.*)
- Gibt es Verschlüsselungsverfahren, die Integrität implizit garantieren? (*Im PDF nicht behandelt.*)

## Verwandt

- [[ASP - Angriff - Modifikation Plaintext]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Hash - HMAC]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Symmetrische Verschluesselung - Modi]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 24; Übersicht auf Folie 27
