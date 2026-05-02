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

# ASP - Asymmetrische Verschlüsselung - Prinzip

> [!info] Kurzdefinition
> Verschlüsselungsverfahren, bei dem jede Partei ein **Schlüsselpaar** aus öffentlichem (Public) und privatem (Private) Schlüssel hat. Was mit dem einen verschlüsselt wird, kann nur mit dem anderen entschlüsselt werden. Der Public Key darf öffentlich verteilt werden.

## Beschreibung

Folien 31–33 stellen das Prinzip vor:

**Eckpunkte (Folie 31):**
- Erste asymmetrische Verschlüsselung 1976 (RSA).
- **Schlüsselpaar** (öffentlicher / geheimer Schlüssel).
- **Public Key kann global und ungeschützt verteilt werden.**
- **Private Key muss geheim gehalten werden** und verlässt den Besitzer in der Regel nie.
- **Anwendungsgebiete:** Digitale Signatur, viele Protokolle wie TLS, HTTPS etc.

**Funktionsprinzip (Folie 32 in Kapitel 02; Folien 11/13 in Kapitel 03 explizit als zwei Anwendungsfälle benannt):**
- **1. Anwendungsfall – Schutz der Vertraulichkeit:** Klartext wird mit dem **Public Key** des Empfängers verschlüsselt → Ciphertext kann nur mit dem zugehörigen **Private Key** entschlüsselt werden. Nur der Empfänger kann lesen.
- **2. Anwendungsfall – Schutz der Integrität / Unveränderbarkeit:** Klartext wird mit dem **Private Key** des Senders verschlüsselt → kann von jedem mit dem zugehörigen **Public Key** entschlüsselt werden. Beweist, dass die Nachricht vom Inhaber des Private Keys stammt – Grundlage für digitale Signaturen.

**Anmerkung zur Begriffswahl:** Die Vorlesung verwendet auf Folie 11 „Schutz der Integrität" und auf Folie 13 „Schutz der Unveränderbarkeit". Beide Bezeichnungen meinen dasselbe Schutzziel – „Unveränderbarkeit" ist die natursprachliche Umschreibung von „Integrität" aus der CIA-Triade. Streng genommen liefert die Konstruktion „mit Private Key verschlüsseln" gleichzeitig **Authentizität** (Identität des Senders), **Integrität** (Erkennung von Manipulation) und **Non-repudiation** (nicht abstreitbare Urheberschaft) – sie ist die Grundlage digitaler Signaturen ([[ASP - Digitale Signatur - Grundlagen]], folgt in Kapitel 04). Die Vorlesung verkürzt das hier auf „Integrität / Unveränderbarkeit"; in der mündlichen Prüfung sollte die volle Wirkungstrias genannt werden.

**Datenfluss bei Vertraulichkeit (Folie 33):**
1. Bob veröffentlicht seinen Public Key.
2. Alice verschlüsselt die Nachricht mit Bobs Public Key.
3. Verschlüsselte Nachricht geht über das Internet.
4. Bob entschlüsselt mit seinem Private Key.

Wichtig: Alice braucht für die Verschlüsselung zu Bob *keinen vorher ausgetauschten geheimen Schlüssel* – das löst das Schlüsselaustausch-Problem.

## Bestandteile / Aufbau

| Element | Rolle |
|---|---|
| Public Key | öffentlich, beliebig verteilbar |
| Private Key | bleibt beim Besitzer |
| Verschlüsselungs-Algorithmus | RSA, ECC |
| Anwendung Vertraulichkeit | Klartext mit Public Key des Empfängers verschlüsseln |
| Anwendung Signatur | Hash mit Private Key des Senders signieren |

## Beispiel

Folie 33: Bob teilt seinen Public Key mit Alice. Alice verschlüsselt eine Nachricht mit Bobs Public Key. Die verschlüsselte Nachricht geht über das Internet zu Bob, der sie mit seinem Private Key entschlüsselt.

## Abgrenzung

- Im Unterschied zur [[ASP - Symmetrische Verschluesselung - Prinzip]] gibt es zwei separate Schlüssel pro Teilnehmer (statt eines geteilten Schlüssels pro Paar).
- Asymmetrische Verfahren liefern **zusätzlich** Authentizität (über Signatur), während symmetrische allein keine Authentizität geben.
- **Trade-off Performance:** asymmetrische Operationen sind ca. 100.000-mal langsamer als symmetrische (Folie 34).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was charakterisiert asymmetrische Verschlüsselung im Vergleich zu symmetrischer?

**Anwendungsfrage:** Skizziere den Datenfluss zwischen Alice und Bob bei asymmetrischer Verschlüsselung. Wer veröffentlicht welchen Schlüssel, welcher wird wofür verwendet?

**Diskussionsfrage:** Warum kann der Public Key gefahrlos öffentlich verteilt werden? Welcher mathematische Mechanismus stellt sicher, dass der Private Key aus dem Public Key nicht praktisch ableitbar ist? (RSA: Faktorisierungsproblem; ECC: diskrete Logarithmen auf elliptischen Kurven.)

**Mögliche Anschlussfragen:**
- Welche zwei Use Cases lassen sich mit demselben Schlüsselpaar abdecken? (Verschlüsselung *zu* mir, Signatur *von* mir.)
- Wie verbindet die hybride Verschlüsselung asymmetrische und symmetrische Verfahren?
- Wie wird sichergestellt, dass ein Public Key wirklich zur richtigen Identität gehört? (PKI / X.509-Zertifikate – im PDF dieser Vorlesung nicht behandelt.)

## Verwandt

- [[ASP - Asymmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Schluesselaustausch - Problem]]

## Quelle

- Vorlesung: [[ASP - VL - Verschluesselungsmethoden]]
- Folien/Seitenangabe Kapitel 02: Folien 31, 32, 33
- Wiederholung in Kapitel 03, Folien 10–14 – mit explizit benannten zwei Anwendungsfällen.
