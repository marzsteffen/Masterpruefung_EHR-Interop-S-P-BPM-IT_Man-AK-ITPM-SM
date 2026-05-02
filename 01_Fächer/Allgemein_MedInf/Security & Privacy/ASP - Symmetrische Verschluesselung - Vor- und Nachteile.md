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

# ASP - Symmetrische Verschlüsselung - Vor- und Nachteile

> [!info] Kurzdefinition
> Symmetrische Verschlüsselung ist schnell und einfach im Schlüsselmanagement (nur ein Schlüssel pro Paar), hat aber das Schlüsselaustausch-Problem und skaliert in der Anzahl Schlüssel quadratisch mit der Anzahl Teilnehmer.

## Beschreibung

Bilanz laut Folie 9.

**Vorteile:**
- **Einfaches Schlüsselmanagement**, da nur ein Schlüssel für Ent- und Verschlüsselung benötigt wird.
- **Hohe Geschwindigkeit** für Ent- und Verschlüsselung, da Verfahren auf effizienten Operationen aufbauen.

**Nachteile:**
- **Schlüssel darf nicht in unbefugte Hände gelangen.**
- **Schlüsselaustausch:** Schlüssel muss über einen sicheren Weg übermittelt werden. → Eigene Note: [[ASP - Schluesselaustausch - Problem]]
- **Anzahl der Schlüssel** bezogen auf die Anzahl der Teilnehmer wächst.

## Bestandteile / Aufbau

| Aspekt | Bewertung |
|---|---|
| Schlüsselmanagement (lokal) | Einfach |
| Performance | Sehr hoch |
| Schlüsselaustausch | Aufwendig, sicherer Kanal nötig |
| Skalierbarkeit | Schlecht – n·(n-1)/2 paarweise Schlüssel |
| Authentizität | Nicht gegeben (siehe Angriffsmodell-Note) |

## Beispiel

Bei 10 Teilnehmern, die paarweise sicher kommunizieren wollen, sind 10·9/2 = 45 separate symmetrische Schlüssel nötig (Skalierungsproblem). *Im PDF nicht explizit gerechnet, ergibt sich aber aus der Aussage.*

## Abgrenzung

- Vor- und Nachteile beziehen sich speziell auf die *symmetrische* Familie. Asymmetrische und hybride Verfahren adressieren genau die genannten Nachteile (Schlüsselaustausch, Skalierung) – siehe [[ASP - Asymmetrische Verschluesselung - Vor- und Nachteile]] und [[ASP - Hybride Verschluesselung - Grundlagen]].

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Vor- und Nachteile hat symmetrische Verschlüsselung?

**Anwendungsfrage:** Warum kommt in TLS-ähnlichen Protokollen trotzdem symmetrische Verschlüsselung zum Einsatz – wenn Sie das Schlüsselaustausch-Problem hat? (Antwort: Hybride Verschlüsselung; symmetrisch bleibt wegen Performance erhalten, asymmetrisch löst nur den Austausch.)

**Diskussionsfrage:** Wie skaliert die Anzahl Schlüssel mit der Anzahl Teilnehmer? Wann wird das in der Praxis problematisch?

**Mögliche Anschlussfragen:**
- Wie viele Schlüssel braucht ein Netz aus 100 Teilnehmern, wenn jeder mit jedem sicher kommunizieren können soll?
- Gibt es eine Möglichkeit, das Schlüsselaustausch-Problem mit ausschließlich symmetrischer Krypto zu lösen? (Stichwort: Out-of-Band-Übergabe, Key Distribution Center – im PDF dieser Vorlesung nicht behandelt.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Schluesselaustausch - Problem]]
- [[ASP - Asymmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folie 9
