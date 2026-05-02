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

# ASP - Angriff - Replay-Angriff

> [!info] Kurzdefinition
> Eve zeichnet eine zuvor gesendete (legitime) Nachricht auf und schickt sie zu einem späteren Zeitpunkt erneut, um beim Empfänger eine wiederholte Aktion auszulösen.

## Beschreibung

Folie 22 beschreibt den Angriff:

- **Angriff:** Eve zeichnet vorherige Nachrichten auf und schickt sie zu einem späteren Zeitpunkt erneut an einen Empfänger.
- **Auswirkung:** Integrität (Authentizität)
- **Typische Sicherheitsfunktion:** Abhängig vom Protokoll, allgemeiner Replay-Schutz: Sicherstellen, dass die Nachricht aktuell ist – über Zeitstempel oder Protokolle.

Das Schaubild auf der Folie zeigt: Alice schickt eine Bestellung an einen Server, Eve fängt sie ab und sendet sie zu einem späteren Zeitpunkt erneut – der Server würde die Bestellung doppelt verarbeiten.

Wichtig: Eve muss die Nachricht **nicht** entschlüsseln können. Der Angriff funktioniert auch gegen verschlüsselte Nachrichten, weil das einfache Wiedereinspielen keinen Klartext-Zugriff erfordert.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Angreifer-Aktion | Aufzeichnen und Wiedereinspielen einer Nachricht |
| Verletztes Schutzziel | Integrität (Authentizität) |
| Klartext-Zugriff erforderlich? | Nein |
| Schutzmechanismen | Zeitstempel, Sequenznummern, Nonces – allgemein „Frische"-Garantien |

## Beispiel

Aus der Folie: Online-Bestellung. Alice bestellt etwas. Eve zeichnet die Bestellung auf und sendet die exakt gleiche Nachricht später erneut – der Server interpretiert es als zweite Bestellung. *Im PDF nicht eHealth-spezifisch ausgeführt.*

## Abgrenzung

- **Replay vs. [[ASP - Angriff - Modifikation Plaintext]] / [[ASP - Angriff - Modifikation Ciphertext]]:** Bei Replay wird die Nachricht **nicht verändert** – nur wiederholt. Das macht den Angriff besonders einfach und gleichzeitig gefährlich.
- **Replay vs. [[ASP - Angriff - Impersonation]]:** Eve gibt sich nicht als jemand anderes aus, sie verwendet nur eine echte alte Nachricht erneut. Das verletzt aber dennoch die Authentizität, weil die wiederholte Nachricht nicht mehr „aktuell" autorisiert ist.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Replay-Angriff, welches Schutzziel verletzt er?

**Anwendungsfrage:** Welche Mechanismen schützen vor Replay? Skizzieren Sie ein Schema mit Sequenznummer und/oder Nonce.

**Diskussionsfrage:** Warum reicht Verschlüsselung allein nicht aus, um Replay zu verhindern? Welchen Trade-off bringt der Einsatz von Zeitstempeln (Uhren-Synchronisation, Drift)?

**Mögliche Anschlussfragen:**
- Wie schützt das HTTP-Replay-Schutzkonzept in OAuth2 (z. B. State-Parameter, Nonce in OIDC) vor Replay? (*Im PDF dieser Vorlesung nicht behandelt – Vorlesung 05.*)
- Wie unterscheiden sich Replay und Reflection Attack? (*Im PDF nicht behandelt.*)

## Verwandt

- [[ASP - Angriff - Modifikation Plaintext]]
- [[ASP - Angriff - Modifikation Ciphertext]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Identitaetsmanagement - Nonce]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 22; Übersicht auf Folie 27
