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

# ASP - Angriff - Impersonation (Identitätsfälschung)

> [!info] Kurzdefinition
> Eve injiziert oder verändert Nachrichten so, dass sie scheinbar von Bob oder Alice stammen. Schutzziel: Integrität (Authentizität). Schutz: HMACs, Signaturen.

## Beschreibung

Folie 25 beschreibt den Angriff:

- **Angriff:** Eve injiziert oder verändert Nachrichten so, dass sie von Bob/Alice (Identitätswechsel) zu stammen scheinen.
- **Auswirkung:** Integrität (Authentizität)
- **Typische Sicherheitsfunktion:** HMACs, Signaturen.

Damit ist Impersonation der direkteste Angriff auf das Schutzziel Authentizität: Eve gibt sich als jemand anderes aus, um den Empfänger zu täuschen.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Angreifer-Aktion | Nachrichten injizieren oder verändern, scheinbar von einer anderen Identität |
| Verletztes Schutzziel | Integrität (Authentizität) |
| Schutzmechanismus | HMAC, digitale Signatur |

## Beispiel

*Im PDF nicht weiter ausgeführt.* Klassisch: gespoofte E-Mail mit gefälschtem Absender; ohne S/MIME-Signatur ist der Empfänger auf andere Indizien angewiesen.

## Abgrenzung

- **Impersonation vs. [[ASP - Angriff - Modifikation Plaintext]]:** Modifikation verändert eine bestehende echte Nachricht; Impersonation **erfindet** Nachrichten unter falscher Identität (oder gibt sich beim Empfangen als jemand anderes aus).
- **Impersonation vs. [[ASP - Angriff - Replay]]:** Replay verwendet eine echte alte Nachricht erneut. Impersonation erzeugt eine neue Nachricht, die so aussieht, als käme sie von jemand anderem.
- Schutz erfordert nicht nur kryptografische Bausteine (HMAC, Signatur), sondern auch eine vertrauenswürdige Bindung zwischen Identität und Schlüssel – d. h. Identitätsmanagement und PKI (siehe folgende Vorlesungen).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Impersonation, welches Schutzziel ist primär betroffen?

**Anwendungsfrage:** Mit welchen Krypto-Bausteinen schützen Sie sich? Welche Voraussetzung muss in der Schlüssel-Infrastruktur erfüllt sein, damit eine Signatur auch tatsächlich gegen Impersonation hilft? (Antwort: vertrauenswürdige Bindung Schlüssel–Identität, z. B. Zertifikate.)

**Diskussionsfrage:** Warum ist Impersonation in eHealth besonders kritisch? (Verschriebene Medikamente unter falscher Arzt-Identität, Patienten-Verwechslung.) Wie wirkt SMART on FHIR / OAuth2 dem entgegen? (*Im PDF nicht behandelt – Vorlesung 05.*)

**Mögliche Anschlussfragen:**
- Wie unterscheiden sich Impersonation auf Nachrichtenebene und auf Sitzungsebene?
- Welche Rolle spielt eine PKI bei der Verhinderung von Impersonation?
- Welcher Zusammenhang besteht zu Phishing? (*Phishing im PDF nicht behandelt.*)

## Verwandt

- [[ASP - Angriff - Replay]]
- [[ASP - Angriff - Modifikation Plaintext]]
- [[ASP - Angriff - Modifikation Ciphertext]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Identitaetsmanagement - Grundlagen]]
- [[ASP - Zertifikate - X.509]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 25; Übersicht auf Folie 27
