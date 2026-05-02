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

# ASP - Hybride Verschlüsselung - Grundlagen

> [!info] Kurzdefinition
> Kombination aus symmetrischer und asymmetrischer Verschlüsselung: Ein zufällig erzeugter symmetrischer Sitzungsschlüssel wird mit dem Public Key des Empfängers asymmetrisch verschlüsselt; die eigentliche Nachricht wird symmetrisch mit diesem Sitzungsschlüssel verschlüsselt.

## Beschreibung

Folien 53–55 stellen das Verfahren vor.

**Eckpunkte (Folie 54):**
- Kombination aus symmetrischer und asymmetrischer Verschlüsselung.
- **Löst das Schlüsselaustausch-Problem** der symmetrischen Verschlüsselung.
- **Löst das Performance-Problem** der asymmetrischen Verschlüsselung.

**Ablauf (Folie 54):**
1. Alice erzeugt zufällig einen symmetrischen Schlüssel.
2. Alice verschlüsselt die Nachricht symmetrisch mit diesem Schlüssel → Ciphertext.
3. Alice verschlüsselt den symmetrischen Schlüssel asymmetrisch mit Bobs Public Key.
4. Alice sendet beides (verschlüsselte Nachricht + verschlüsselter Sitzungsschlüssel) an Bob.
5. Bob entschlüsselt den symmetrischen Schlüssel asymmetrisch mit seinem Private Key.
6. Bob entschlüsselt die Nachricht symmetrisch mit dem so gewonnenen Sitzungsschlüssel.

**Offenes Problem (Folie 55):**
- **Keine Authentizität!** Der hybride Aufbau wie oben sagt nichts darüber aus, *von wem* die Nachricht kommt.
- **Lösung:** Einsatz von digitalen Signaturen oder MACs. Folie 55 zeigt eine erweiterte Konstruktion: Alice signiert die Nachricht zusätzlich mit ihrem Private Key. Bob verifiziert die Signatur mit Alice' Public Key. Mit der Signatur wird gleichzeitig auch der Public Key von Alice mitübertragen, damit Bob verifizieren kann.

## Bestandteile / Aufbau

| Teilkomponente | Schlüsselart | Zweck |
|---|---|---|
| Symmetrischer Sitzungsschlüssel | symmetrisch (z. B. AES) | verschlüsselt die Nachricht effizient |
| Asymmetrische Verschlüsselung des Sitzungsschlüssels | Public Key des Empfängers | sicherer Transport des Sitzungsschlüssels |
| Optional: Signatur über die Nachricht | Private Key des Senders | Authentizität, Integrität, Non-repudiation |

## Beispiel

Konkret in der Praxis: TLS-Handshake. Der Client einigt sich mit dem Server auf einen Sitzungsschlüssel (typisch via ECDHE oder verschlüsselt per RSA), ab dann läuft alle Kommunikation symmetrisch (typisch AES-GCM). *Konkrete TLS-Erwähnung im PDF nicht ausgeführt, aber die Grundidee genau dieser Vorlesung entspricht TLS-Aufbau.*

## Abgrenzung

- **Hybrid vs. nur symmetrisch:** Hybrid hat das Schlüsselaustausch-Problem gelöst.
- **Hybrid vs. nur asymmetrisch:** Hybrid skaliert performant (Inhalt wird symmetrisch verschlüsselt).
- **Hybrid ohne Signatur vs. mit Signatur:** Ohne Signatur fehlt Authentizität – die zusätzliche Signatur (Folie 55) schließt diese Lücke.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist hybride Verschlüsselung, und welche zwei Probleme löst sie gegenüber rein symmetrischer und rein asymmetrischer Verschlüsselung?

**Anwendungsfrage:** Skizziere den Datenfluss zwischen Alice und Bob bei hybrider Verschlüsselung. Welcher Schlüssel wird wann erzeugt, übertragen und verwendet?

**Diskussionsfrage:** Welche Schwäche bleibt auch bei hybrider Verschlüsselung ohne zusätzliche Maßnahme? (Authentizität.) Wie wird sie geschlossen, und welcher Schlüssel kommt dafür zum Einsatz? (Signatur mit Private Key des Senders.) Diskutieren Sie die Reihenfolge: erst signieren, dann verschlüsseln vs. erst verschlüsseln, dann signieren – welche Vor-/Nachteile? (*Diese feinere Reihenfolge ist im PDF nicht behandelt.*)

**Mögliche Anschlussfragen:**
- Wie wird der symmetrische Sitzungsschlüssel typischerweise generiert?
- Wie hängt das mit Perfect Forward Secrecy zusammen? (Wird der Sitzungsschlüssel pro Sitzung neu und nicht aus dem Public Key direkt abgeleitet, ist eine Form von PFS möglich.)
- Welche Angriffe verhindert die hybride Konstruktion plus Signatur, die einzeln nicht abgedeckt sind?

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Schluesselaustausch - Problem]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Symmetrische Verschluesselung - AES]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Hash - HMAC]]
- [[ASP - Kryptografie - Perfect Forward Secrecy]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folien 53, 54, 55
- Wiederholung in Kapitel 03, Folien 27–29 – inhaltlich deckungsgleich.
