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

# ASP - Symmetrische Verschlüsselung - Prinzip

> [!info] Kurzdefinition
> Bei der symmetrischen Verschlüsselung verwenden Sender und Empfänger denselben geheimen Schlüssel sowohl für Ver- als auch Entschlüsselung.

## Beschreibung

Folie 5 stellt das symmetrische Verschlüsselungs-Prinzip dar:

- **Derselbe Schlüssel** wird für Ver- und Entschlüsselung verwendet (Secret Key / Geheimer Schlüssel).
- **Voraussetzung:** Beide Parteien müssen den geheimen Schlüssel kennen → Schlüssel muss vorab über einen sicheren Kanal ausgetauscht werden („Austausch des geheimen Schlüssels" in der Vorlesung).
- **Unterscheidung** in zwei grundlegende Bauarten: **Stromchiffren** und **Blockchiffren** (siehe Folie 6/7).

Ablauf laut Folie 5:
1. Alice und Bob einigen sich auf einen geheimen Schlüssel.
2. Alice verschlüsselt die Nachricht mit dem Schlüssel.
3. Verschlüsselte Nachricht geht über das Internet zum Empfänger.
4. Bob entschlüsselt mit demselben Schlüssel.

## Bestandteile / Aufbau

| Komponente | Rolle |
|---|---|
| Klartext (Plaintext) | Eingabe vor Verschlüsselung |
| Schlüssel (Secret Key) | Identisch bei Sender und Empfänger |
| Verschlüsselungs-Algorithmus | DES, 3DES, AES, … |
| Ciphertext | Ausgabe der Verschlüsselung |
| Sicherer Kanal für Schlüsselübertragung | Vorausgesetzt – ist das größte praktische Problem |

## Beispiel

Aus Folie 5 visualisiert: Alice → schlüsselt mit Secret Key → Ciphertext über Internet → Bob entschlüsselt mit demselben Secret Key.

## Abgrenzung

- Im Unterschied zur [[ASP - Asymmetrische Verschluesselung - Prinzip]] gibt es nur **einen** Schlüssel (statt eines Schlüsselpaars).
- Im Unterschied zu [[ASP - Hash - HMAC]] schützt symmetrische Verschlüsselung primär die *Vertraulichkeit*, nicht die Integrität.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist das zentrale Charakteristikum symmetrischer Verschlüsselung?

**Anwendungsfrage:** Skizziere den Datenfluss zwischen Alice und Bob bei symmetrischer Verschlüsselung – wo liegt das praktisch schwierige Problem? (Antwort: sicherer Schlüsselaustausch.)

**Diskussionsfrage:** Warum ist symmetrische Verschlüsselung in modernen Protokollen (TLS, etc.) trotzdem die Arbeitspferd-Komponente, obwohl sie das Schlüsselaustauschproblem hat? (Antwort: hybride Konstruktion löst das Problem; symmetrisch bleibt wegen Performance-Vorteil unverzichtbar.)

**Mögliche Anschlussfragen:**
- Welche zwei Untertypen unterscheidet man? (Strom- und Blockchiffre.)
- Welche typischen Algorithmen kommen zum Einsatz?
- Wie wächst die Anzahl Schlüssel mit der Anzahl Teilnehmer? (n·(n-1)/2 paarweise.)

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Stromchiffre]]
- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]
- [[ASP - Symmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Schluesselaustausch - Problem]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe: Folie 5
