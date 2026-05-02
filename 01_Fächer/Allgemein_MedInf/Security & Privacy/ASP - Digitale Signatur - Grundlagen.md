---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Digitale Signatur - Grundlagen

> [!info] Kurzdefinition
> Kryptografisches Verfahren, bei dem der Sender den Hash einer Nachricht mit seinem Private Key verschlüsselt; der Empfänger verifiziert mit dem Public Key des Senders. Liefert Integrität, Authentizität und Non-repudiation.

## Beschreibung

Folien 11–13 erläutern digitale Signaturen als Antwort auf die offene Frage „Wie schützt man Integrität *und* Authentizität gleichzeitig?"

**Signaturerstellung (Folie 12) mit Private Key des Senders:**
1. Erstellen der Nachricht / des Dokuments.
2. Berechnung des Hash-Wertes.
3. Verschlüsseln des Hash-Wertes mit dem Private Key.
4. Übermitteln der Nachricht, der digitalen Signatur und des Public Key.

**Signaturverifizierung (Folie 13) mit Public Key des Senders:**
- Empfänger berechnet selbst den Hash-Wert der erhaltenen Nachricht.
- Empfänger entschlüsselt die mitgeschickte Signatur mit dem Public Key des Senders → erhält den ursprünglichen Hash-Wert.
- Vergleich: Stimmen die zwei Hash-Werte überein, ist die Nachricht unverändert UND stammt nachweislich vom Inhaber des Private Keys.

**Schutzziele, die digitale Signaturen liefern:**
- **Integrität** (jede Änderung an der Nachricht ändert den Hash und macht die Verifikation ungültig).
- **Authentizität** (nur der Inhaber des Private Keys kann eine Signatur erzeugen, die mit dem zugehörigen Public Key verifizierbar ist).
- **Non-repudiation** (der Sender kann seine Urheberschaft im Nachhinein nicht abstreiten – im Unterschied zu HMAC).

**Voraussetzung:** Der Public Key muss zuverlässig dem Sender zugeordnet sein. Genau das leistet ein digitales Zertifikat ([[ASP - Zertifikate - X.509]]) im Rahmen einer [[ASP - Zertifikate - PKI]].

## Bestandteile / Aufbau

| Komponente | Rolle |
|---|---|
| Hash-Funktion | reduziert Nachricht beliebiger Länge auf festen Hash-Wert |
| Asymmetrisches Schlüsselpaar | Private Key zum Signieren, Public Key zum Verifizieren |
| Übertragene Bestandteile | Nachricht, Signatur (= verschlüsselter Hash), Public Key (oder Zertifikat mit Public Key) |
| Verifikation | Hash neu berechnen + Signatur entschlüsseln + vergleichen |

## Beispiel

Aus Folie 12: Alice → Nachricht → Hash-Funktion → Hash Wert → Verschlüsselung mit Private Key (Alice) → Digitale Signatur. Übertragen werden: Nachricht + Digitale Signatur + Public Key (Alice).

## Abgrenzung

- **Signatur vs. [[ASP - MAC - Grundlagen]]:** MAC nutzt symmetrischen Schlüssel und liefert keine Non-repudiation. Signatur nutzt asymmetrischen Schlüssel und liefert Non-repudiation.
- **Signatur vs. „mit Private Key verschlüsseln" (aus [[ASP - Asymmetrische Verschluesselung - Prinzip]] – 2. Anwendungsfall):** Konzeptuell dasselbe, aber in der Praxis wird *nicht* die ganze Nachricht mit dem Private Key verschlüsselt (zu langsam, große Ausgabe), sondern nur der Hash-Wert. Das ist der Effizienz-Trick der Signatur.
- **Signatur vs. Verschlüsselung:** Signatur schützt nicht die Vertraulichkeit. Wer beides will, muss kombinieren – siehe [[ASP - Digitale Signatur - Reihenfolge sign-encrypt]].

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine digitale Signatur, und welche drei Schutzziele liefert sie?

**Anwendungsfrage:** Skizziere Erstellung und Verifikation einer digitalen Signatur. Welche Schlüssel kommen wann zum Einsatz?

**Diskussionsfrage:** Warum wird der Hash der Nachricht signiert und nicht die Nachricht selbst? Welche Konsequenz hat eine Kompromittierung des Private Keys – und welche eine Kompromittierung der zugrunde liegenden Hash-Funktion?

**Mögliche Anschlussfragen:**
- Wie unterscheidet sich eine digitale Signatur von einem HMAC?
- Was muss zusätzlich passieren, damit ein Empfänger dem Public Key des Senders trauen kann? (Identitätsbindung über Zertifikat / PKI.)
- Welche Algorithmen kommen für digitale Signaturen zum Einsatz? (RSA-Signatur, ECDSA – im PDF nicht ausdrücklich genannt, aber RSA und ECC aus den Vor-Vorlesungen verfügbar.)
- Welche Schutzziele NICHT erfüllt eine Signatur? (Vertraulichkeit, Frische / Replay-Schutz.)

## Verwandt

- [[ASP - Hash - Funktion]]
- [[ASP - MAC - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]
- [[ASP - Zertifikate - X.509]]
- [[ASP - Zertifikate - Signaturverifikation]]
- [[ASP - Digitale Signatur - Reihenfolge sign-encrypt]]
- [[ASP - Security Eigenschaften - Non-repudiation]]
- [[ASP - Security Eigenschaften - Authenticity]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folien 10–13
