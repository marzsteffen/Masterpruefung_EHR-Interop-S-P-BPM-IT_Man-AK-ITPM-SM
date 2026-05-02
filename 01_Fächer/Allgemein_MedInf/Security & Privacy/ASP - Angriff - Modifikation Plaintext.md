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

# ASP - Angriff - Verändern der unverschlüsselten Nachricht

> [!info] Kurzdefinition
> Eve fängt eine im Klartext übertragene Nachricht ab und modifiziert sie nach ihren Bedürfnissen. Schutzziel: Integrität (Authentizität). Schutz: HMACs, Signaturen.

## Beschreibung

Folie 23 beschreibt den Angriff:

- **Angriff:** Eve fängt eine unverschlüsselte Nachricht ab und modifiziert sie nach ihren Bedürfnissen.
- **Auswirkung:** Integrität (Authentizität)
- **Typische Sicherheitsfunktion:** HMACs, Signaturen, die sicherstellen, dass Nachrichtenänderungen vom Empfänger erkannt werden.

Da die Nachricht im Klartext übertragen wird, kann Eve den Inhalt frei verstehen und so gezielt manipulieren – z. B. einen Empfänger in einer Überweisungsnachricht austauschen.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Angreifer-Aktion | Aktive Modifikation des Klartextes |
| Klartext-Zugriff | Vollständig (Nachricht ist unverschlüsselt) |
| Verletztes Schutzziel | Integrität (Authentizität) |
| Schutzmechanismen | HMAC, digitale Signatur |

## Beispiel

*Im PDF nicht weiter ausgeführt.* Klassisch: HTTP-Verkehr ohne TLS – Eve ändert eine Bestellsumme oder einen Empfänger in der Nachricht.

## Abgrenzung

- **Modifikation Plaintext vs. [[ASP - Angriff - Modifikation Ciphertext]]:** Beim Plaintext-Angriff versteht Eve den Inhalt und kann gezielt manipulieren. Beim Ciphertext-Angriff manipuliert sie blind.
- Verschlüsselung allein reicht nicht – auch verschlüsselte Nachrichten brauchen einen Integritätsschutz.
- Eine HMAC liefert Integritätsschutz, aber keine Non-repudiation. Eine Signatur liefert beides – siehe [[ASP - Security Eigenschaften - Non-repudiation]].

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Angriff „Verändern der unverschlüsselten Nachricht"? Welches Schutzziel ist betroffen?

**Anwendungsfrage:** Mit welchen Bausteinen schützen Sie eine unverschlüsselt übertragene Nachricht gegen Manipulation? Was ist der Unterschied zwischen einem HMAC- und einem Signatur-Schutz?

**Diskussionsfrage:** Wann reicht ein HMAC-Schutz, wann brauchen Sie eine digitale Signatur? Welche zusätzlichen Eigenschaften liefert eine Signatur?

**Mögliche Anschlussfragen:**
- Wie groß ist das Sicherheitsproblem, wenn nur Verschlüsselung, aber kein Integritätsschutz vorhanden ist?
- Wie verhindert TLS diesen Angriff (HMAC + Sequenznummer)? (*Im PDF dieser Vorlesung nicht behandelt.*)

## Verwandt

- [[ASP - Angriff - Modifikation Ciphertext]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Hash - HMAC]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 23; Übersicht auf Folie 27
