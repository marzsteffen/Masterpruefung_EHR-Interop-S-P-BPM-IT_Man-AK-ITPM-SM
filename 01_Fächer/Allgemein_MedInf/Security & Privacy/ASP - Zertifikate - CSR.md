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

# ASP - Zertifikate - Certificate Signing Request (CSR)

> [!info] Kurzdefinition
> Zertifikatssignierungsanforderung: Anfrage eines Antragstellers an eine vertrauenswürdige Stelle, mit der er einen selbst erzeugten Public Key zur Zertifizierung einreicht. Wird mit dem zugehörigen Private Key signiert (Beweis des Schlüsselbesitzes).

## Beschreibung

Folie 17 beschreibt den Ablauf der Zertifikatsausstellung („Public Key Registrierung"):

1. **Certificate Signing Request (CSR) = Zertifikatssignierungsanforderung.**
2. **Antragsteller erzeugt ein Schlüsselpaar und einen CSR und signiert ihn mit dem Private Key.**
3. **Antragsteller sendet CSR inkl. Public Key an vertrauenswürdige (z. B. staatlich akkreditierte) Stelle.**
4. **Vertrauensdiensteanbieter validiert CSR, erstellt ein Zertifikat und sendet es zurück an den Antragsteller.**

**Kernidee:** Der Private Key verlässt **nie** den Antragsteller. Der CSR enthält nur den Public Key plus identifizierende Daten und wird mit dem Private Key signiert – das beweist gegenüber der CA, dass der Antragsteller wirklich im Besitz des zugehörigen Private Keys ist (Proof of Possession).

**Was die CA zusätzlich leistet (nur angedeutet auf Folie 17):**
- Identitätsprüfung des Antragstellers außerhalb des CSR-Mechanismus (z. B. Vorlage eines Ausweises).
- Erstellung des Zertifikats, signiert mit dem CA-Private Key.
- Eintrag in PKI-Verzeichnisdienste.

## Bestandteile / Aufbau

| Schritt | Wer | Was |
|---|---|---|
| 1 | Antragsteller | Schlüsselpaar (Public + Private) erzeugen |
| 2 | Antragsteller | CSR mit Public Key + Antragsteller-Daten erstellen |
| 3 | Antragsteller | CSR mit eigenem Private Key signieren |
| 4 | Antragsteller | CSR an Vertrauensdiensteanbieter senden |
| 5 | CA / Vertrauensdiensteanbieter | Identität validieren |
| 6 | CA | Zertifikat erstellen, mit CA-Private-Key signieren |
| 7 | CA | Zertifikat an Antragsteller zurücksenden |

## Beispiel

Aus Folie 17 visualisiert: Antragsteller mit Public/Private-Key-Paar → signiert CSR → sendet CSR an Vertrauensdiensteanbieter → erhält Zertifikat zurück → Vertrauensdiensteanbieter publiziert in PKI.

## Abgrenzung

- **CSR vs. fertiges Zertifikat:** Der CSR ist die Anfrage; das Zertifikat ist das Ergebnis. Der CSR enthält keine CA-Signatur; das Zertifikat schon.
- **CSR-Signatur (vom Antragsteller) vs. Zertifikats-Signatur (von der CA):** Erstere beweist Schlüsselbesitz, Letztere beweist die Identitätsprüfung durch die CA.
- Wichtig: **Der Private Key wird nie übertragen.** Das ist der zentrale Unterschied zu naiven Schlüsselverteilungs-Verfahren.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein CSR und welche Rolle spielt er bei der Zertifikatsausstellung?

**Anwendungsfrage:** Skizzieren Sie den vollständigen Ablauf von der Schlüsselgenerierung bis zum fertigen Zertifikat. Welcher Schlüssel wird übertragen, welcher nicht – und warum?

**Diskussionsfrage:** Warum signiert der Antragsteller den CSR mit dem eigenen Private Key? Was würde passieren, wenn er ihn nicht signiert? (Antwort: Eve könnte einen CSR mit Alice' Public Key, aber unter Eves Identitätsdaten einreichen und so eine falsche Bindung erzeugen.) Welche Identitätsprüfung muss die CA *zusätzlich* zur CSR-Signatur durchführen?

**Mögliche Anschlussfragen:**
- Welches Format hat ein CSR typischerweise? (PKCS#10 – im PDF nicht erwähnt.)
- Was passiert, wenn der Private Key nach der Zertifikatsausstellung kompromittiert wird? (Widerruf über CRL/OCSP – siehe [[ASP - Zertifikate - PKI]].)
- Wer ist in Österreich ein qualifizierter Vertrauensdiensteanbieter? (z. B. A-Trust – im PDF nicht ausgewiesen.)

## Verwandt

- [[ASP - Zertifikate - X.509]]
- [[ASP - Zertifikate - PKI]]
- [[ASP - Zertifikate - Signaturverifikation]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folie 17

## Ergänzung außerhalb der Vorlesung

Das übliche CSR-Format ist **PKCS#10** (RFC 2986). In der Praxis enthält ein CSR den Public Key, einen Distinguished Name (z. B. CN, O, OU, C), optionale Erweiterungen (z. B. Subject Alternative Names für Webserver-Zertifikate) und die Signatur des Antragstellers. Die Antwort der CA ist meist im Format X.509 v3 (PEM- oder DER-kodiert).
