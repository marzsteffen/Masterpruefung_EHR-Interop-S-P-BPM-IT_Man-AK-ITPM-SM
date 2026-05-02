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

# ASP - Schlüsselaustausch - Problem

> [!info] Kurzdefinition
> Zwei Parteien, die symmetrisch verschlüsselt kommunizieren wollen, müssen sich vorher auf einen gemeinsamen geheimen Schlüssel einigen – aber die Übertragung dieses Schlüssels selbst muss sicher erfolgen, was ohne weiteren Mechanismus ein Henne-Ei-Problem ist.

## Beschreibung

Folie 28 formuliert das Schlüsselaustausch-Problem als die zentrale offene Schwäche symmetrischer Verschlüsselung:

- Zwei Parteien müssen sich auf einen gemeinsamen Verschlüsselungsschlüssel einigen.
- Eine Partei (z. B. Alice) generiert einen symmetrischen Schlüssel.
- Dieser symmetrische Schlüssel muss an Bob gesendet werden, um Verschlüsselung/Entschlüsselung zu ermöglichen.
- **Die Übertragung des symmetrischen Schlüssels muss sicher (!) erfolgen.**

Folie 29 illustriert das Problem an Pay-TV als Beispiel-Anwendungsfall:
- Symmetrische Verschlüsselung ist hier wegen Performance geeignet.
- TV-Signal wird vom Anbieter (z. B. Sky) verschlüsselt.
- Symmetrische Schlüssel werden als **Chipkarten** ausgegeben, die in den Decoder gesteckt werden.
- **Schwäche:** Keine Authentizität – Chipkarte kann von jedem genutzt werden.

Lösung dieses Problems wird ab Folie 35 angeschnitten: asymmetrische Verschlüsselung erlaubt es, den symmetrischen Schlüssel sicher (mit dem Public Key des Empfängers verschlüsselt) zu übertragen ([[ASP - Hybride Verschluesselung - Grundlagen]]). Alternativ Schlüsselaustausch-Protokolle wie Diffie-Hellman ([[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]).

## Bestandteile / Aufbau

| Teilproblem | Beschreibung |
|---|---|
| Vereinbarung | Beide Parteien benötigen denselben Schlüssel |
| Geheimhaltung | Der Schlüssel darf nicht in falsche Hände gelangen |
| Übertragungskanal | Es existiert standardmäßig kein bereits sicherer Kanal |
| Authentizität | Wer ist der Empfänger des Schlüssels wirklich? (Pay-TV-Beispiel) |

## Beispiel

Pay-TV (Folie 29):
- Ein Anbieter verteilt Chipkarten mit den symmetrischen Schlüsseln an Abonnenten.
- Solange die Karte beim rechtmäßigen Abonnenten bleibt, funktioniert die Verschlüsselung.
- Da nur der Schlüssel die Berechtigung gibt, kann jede Person, die die Karte bekommt, die Inhalte entschlüsseln – Identität wird nicht geprüft.

## Abgrenzung

- Das Problem betrifft ausschließlich symmetrische Verfahren. Bei asymmetrischen Verfahren ([[ASP - Asymmetrische Verschluesselung - Prinzip]]) ist es lösbar, weil der Public Key offen verteilt werden darf.
- Die Lösung über asymmetrische Verschlüsselung ist die Grundidee der hybriden Verschlüsselung.
- Eine *zweite* Lösungsklasse sind kryptografische Schlüsselaustausch-Protokolle wie Diffie-Hellman, bei denen der Schlüssel überhaupt nie übertragen wird, sondern beidseitig berechnet wird.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist das Schlüsselaustausch-Problem, und warum ist es bei symmetrischer Verschlüsselung so kritisch?

**Anwendungsfrage:** Welche zwei Klassen von Lösungen kennt die Vorlesung? (Asymmetrische Verschlüsselung des symmetrischen Schlüssels; dedizierter Schlüsselaustausch mit Diffie-Hellman.)

**Diskussionsfrage:** Pay-TV als Beispiel: Welche Schwäche bleibt auch nach erfolgreichem Schlüsselaustausch? (Keine Authentizität – Chipkarten-Diebstahl/-Verleih reicht aus.)

**Mögliche Anschlussfragen:**
- Wie schließt die hybride Verschlüsselung dieses Problem?
- Worin unterscheiden sich der „asymmetrisch verschlüsselte Schlüsseltransport" und der „Diffie-Hellman-Schlüsselaustausch"?
- Welche Rolle spielen Public-Key-Infrastrukturen (PKI) bei der Authentizität des Empfänger-Public-Keys?

## Verwandt

- [[ASP - Symmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folien 28, 29
- Wiederholung in Kapitel 03, Folie 6 – nur als Übergangsfolie; das Pay-TV-Beispiel aus Kapitel 02 fehlt in Kap 03.
