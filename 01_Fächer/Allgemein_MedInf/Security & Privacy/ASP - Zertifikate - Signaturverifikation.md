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

# ASP - Zertifikate - Signaturverifikation (kryptografisch + Zertifikat)

> [!info] Kurzdefinition
> Die vollständige Verifikation einer signierten Nachricht besteht aus zwei Schritten: kryptografische Verifikation (Hash + Signatur) UND Zertifikatsvalidierung (Gültigkeit, Sperrstatus, Schlüsselverwendung, Authentizitätsqualität).

## Beschreibung

Folie 19 betont in roter Schrift: **„Bei der Signaturverifizierung muss neben der kryptografischen Verifikation auch eine Validierung des Zertifikats vorgenommen werden!"**

**1. Kryptografische Verifikation (Signatur + Hashwert):**
- Empfänger berechnet den Hash der erhaltenen Nachricht.
- Empfänger entschlüsselt die Signatur mit dem Public Key des Senders.
- Beide Hash-Werte werden verglichen – sind sie identisch, ist die Signatur kryptografisch gültig.

**2. Zertifikatsvalidierung (Folie 20, 21):**
- **Gültigkeitsperiode:** Liegt der aktuelle Zeitpunkt zwischen „gültig ab" und „gültig bis"?
- **Schlüsselverwendung:** Ist das Zertifikat überhaupt für „Digitale Signatur" zugelassen (oder nur für Verschlüsselung)?
- **Überprüfung der Revozierung:** Steht das Zertifikat auf einer CRL oder sagt OCSP „revoked"?
- **Qualität der Authentizität:** Ist die ausstellende Certification Authority vertrauenswürdig? Ist es ein qualifiziertes Zertifikat?
- **Personenbindung:** Ist ein eindeutiger Identifier der Person im Zertifikat enthalten (Folie 21).

Beide Schritte müssen erfolgreich sein. Eine kryptografisch gültige Signatur mit einem widerrufenen oder abgelaufenen Zertifikat ist nicht akzeptabel.

## Bestandteile / Aufbau

| Schritt | Inhalt |
|---|---|
| Krypto-Verifikation | Hash der Nachricht neu berechnen → Signatur mit Public Key entschlüsseln → vergleichen |
| Zertifikats-Validierung – Gültigkeit | Datum prüfen |
| Zertifikats-Validierung – Schlüsselverwendung | „Digitale Signatur" erlaubt? |
| Zertifikats-Validierung – Revozierung | CRL oder OCSP befragen |
| Zertifikats-Validierung – Vertrauen | Wurzel-CA bekannt und vertrauenswürdig? |
| Zertifikats-Validierung – Personenbindung | eindeutiger Identifier vorhanden? |

## Beispiel

Aus Folie 20 abgeleitet: Eine Signatur mit Klaus Stranachers Zertifikat (Gültigkeit 13.08.2013–13.08.2018) wird heute (2026) **nicht** mehr akzeptiert, weil das Zertifikat abgelaufen ist – auch wenn die kryptografische Verifikation noch funktioniert. (*Im PDF nicht explizit ausgeführt; logische Folge der Felder.*)

## Abgrenzung

- **Krypto-Verifikation allein** ist unzureichend, weil sie nichts über die Bindung Public Key ↔ Person aussagt.
- **Zertifikats-Validierung allein** ist unzureichend, weil sie nichts über die Echtheit der konkreten Signatur aussagt.
- Erst beide Schritte zusammen liefern den vollen Beweis: „Die Nachricht stammt unverändert von der Person, deren Identität die CA zum Zeitpunkt X bestätigt hat, und das Zertifikat ist heute weiterhin gültig."

## Prüfungsrelevanz

**Typische Definitionsfrage:** Aus welchen zwei Teilen besteht eine vollständige Signatur-Verifikation? Wofür ist jeder Teil zuständig?

**Anwendungsfrage:** Sie erhalten eine elektronisch signierte Nachricht. Beschreiben Sie schrittweise, welche Prüfungen Sie vornehmen müssen, bevor Sie der Signatur trauen können.

**Diskussionsfrage:** Was passiert, wenn die Krypto-Verifikation gelingt, das Zertifikat aber widerrufen ist? (Antwort: Signatur ist nicht akzeptabel; meistens Hinweis auf Schlüsselkompromittierung.) Was passiert, wenn das Zertifikat gültig ist, aber die Krypto-Verifikation fehlschlägt? (Antwort: Nachricht wurde manipuliert oder die Signatur stammt nicht vom angegebenen Schlüsselbesitzer.)

**Mögliche Anschlussfragen:**
- Wie funktioniert OCSP, wie eine CRL? (siehe [[ASP - Zertifikate - PKI]] – im PDF nur als Felder genannt.)
- Welche Rolle spielt die Wurzel-CA bei der Vertrauenswürdigkeit?
- Wie würden Sie eine Signatur-Verifikation in einem eHealth-System implementieren, wenn die OCSP-Quelle gerade nicht erreichbar ist?

## Verwandt

- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Zertifikate - X.509]]
- [[ASP - Zertifikate - PKI]]
- [[ASP - Zertifikate - CSR]]
- [[ASP - Hash - Funktion]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folien 19, 20, 21
