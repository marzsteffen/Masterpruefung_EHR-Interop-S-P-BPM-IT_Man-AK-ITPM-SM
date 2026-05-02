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

# ASP - Asymmetrische Verschlüsselung - Bewertung gegen das Angriffsmodell

> [!info] Kurzdefinition
> Bewertung der acht Angriffe aus dem Einführungs-Angriffsmodell unter asymmetrischer Verschlüsselung: ähnliches Bild wie bei symmetrischer Verschlüsselung – Vertraulichkeit gut, Authentizität ungelöst, Replay und DoS offen.

## Beschreibung

Folie 51 listet die Angriffe und ihre Bewertung unter asymmetrischer Verschlüsselung – mit denselben Annahmen wie bei symmetrischer (Folie 50, identisch zu Folie 26):

**Annahmen (Folie 50):**
- Geheime Schlüssel (privater/symmetrischer Schlüssel) werden nicht kompromittiert.
- Kryptografische Primitive sind sicher (richtig implementiert).
- Der Angreifer befindet sich in der Kommunikationsverbindung und kann Nachrichten ändern, unterdrücken oder einschleusen.

**Bewertung (Folie 51):**

| Angriff | Bewertung | Begründung laut Folie |
|---|---|---|
| Nachricht lesen | ✅ verhindert | Nicht möglich, Daten werden verschlüsselt. |
| Indirektes Ableiten von Informationen (Traffic Analysis) | ⚠️ szenarioabhängig | Meta-Informationen könnten extrahiert werden (Bsp: Datenmenge bei RSA größer als bei ECC). |
| Aufzeichnung + Entschlüsselung mit gestohlenem Schlüssel | ❌ erfolgreich | Kommunikation kann aufgezeichnet und mit gestohlenen Schlüssel entschlüsselt werden. |
| Replay | ❌ erfolgreich | Möglich. Verschlüsselung allein verhindert keinen Replay-Angriff. |
| Modifikation Plaintext | ✅ verhindert | Keine Modifizierung möglich, da die Daten verschlüsselt sind. |
| Modifikation Ciphertext | ❌ erfolgreich | Ein Angreifer kann einen Ciphertext hinzufügen. |
| Impersonation | ⚠️ szenarioabhängig | Asym. Verschlüsselung allein gewährleistet keine Authentizität. |
| Nachricht unterdrücken (DoS) | ❌ erfolgreich | Möglich. |

**Farbschema:** Grün = nicht möglich; Gelb = szenarioabhängig; Rot = erfolgreich.

## Bestandteile / Aufbau

Die Bewertung ist *nahezu identisch* mit der von symmetrischer Verschlüsselung. Unterschiede liegen primär in den Begründungen, nicht im Ergebnis:
- Bei Traffic Analysis nennt die Folie als zusätzliches Beispiel die unterschiedliche Datenmenge bei RSA vs. ECC – das selbst kann eine Information leaken (welcher Algorithmus genutzt wird).
- Bei Aufzeichnung + Entschlüsselung steht das Risiko bei einem kompromittierten Privaten Schlüssel; ohne Perfect Forward Secrecy (z. B. mit ECDHE) ist alle aufgezeichnete Kommunikation lesbar.

Konsequenz: Auch asymmetrische Verschlüsselung allein reicht nicht aus. Authentizität, Replay-Schutz und Modifikations-Erkennung brauchen zusätzliche Bausteine (Signatur, Frische-Mechanismen).

## Beispiel

Beispielhafte Verkettung: Alice schickt eine signierte und mit Bobs Public Key verschlüsselte Nachricht. Eve fängt sie ab. Sie kann den Inhalt nicht lesen (Vertraulichkeit OK). Sie könnte aber die Nachricht später erneut einspielen (Replay) – außer das Protokoll enthält Frische-Mechanismen (Nonce, Zeitstempel).

## Abgrenzung

- Diese Tabelle bewertet asymmetrische Verschlüsselung *isoliert*. In der Praxis wird sie kombiniert mit Signaturen, hybride Verschlüsselung etc., wodurch sich das Bild deutlich verbessert.
- Vergleich: [[ASP - Symmetrische Verschluesselung - Angriffsmodell]] – sehr ähnliches Ergebnis, aber andere Begründungen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Angriffe verhindert asymmetrische Verschlüsselung allein?

**Anwendungsfrage:** Vergleiche die Bewertung gegen das Angriffsmodell zwischen symmetrischer und asymmetrischer Verschlüsselung. Wo unterscheiden sich die Begründungen, auch wenn das Ergebnis ähnlich aussieht?

**Diskussionsfrage:** Warum bringt der Wechsel von symmetrisch zu asymmetrisch *für sich allein* keinen großen Sicherheitsgewinn? (Antwort: Beide adressieren primär Vertraulichkeit. Der echte Mehrwert asymmetrischer Verfahren liegt im *Schlüsselaustausch* und in der Möglichkeit zur *Signatur* – nicht in den abgewehrten Angriffen.)

**Mögliche Anschlussfragen:**
- Welche Bausteine ergänzen asymmetrische Verschlüsselung, um Authentizität sicherzustellen? (Signatur, ggf. PKI.)
- Wie hilft Perfect Forward Secrecy in dieser Tabelle? (Mit PFS wird „Aufzeichnung + Entschlüsselung" auch nach Schlüsselkompromittierung verhindert.)
- Warum bleibt DoS unter beiden Verfahren ungelöst?

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Angriffsmodell]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
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
- Folien/Seitenangabe Kapitel 02: Folien 49, 50, 51
- Wiederholung in Kapitel 03, Folien 24, 25 – Tabelle deckungsgleich; Annahmen-Folie aus Kapitel 02 (Folie 50) ist in Kap 03 nicht wiederholt.
