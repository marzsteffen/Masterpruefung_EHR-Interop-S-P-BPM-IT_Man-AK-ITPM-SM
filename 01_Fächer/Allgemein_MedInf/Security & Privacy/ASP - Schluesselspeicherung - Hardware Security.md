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

# ASP - Schlüsselspeicherung - Hardware Security (HSM, Secure Element, Secure Enclave)

> [!info] Kurzdefinition
> Sichere Speicherung und Erzeugung kryptografischer Schlüssel erfordert dedizierte Hardware (HSM, Secure Element, Secure Enclave), weil Software-Keystores grundsätzlich angreifbar sind. Die Hardware-Sicherheit bestimmt die Qualität der Authentifizierung.

## Beschreibung

Folie 32 listet die offenen Probleme der Schlüsselsicherheit auch nach PFS:

- **Risiko: Unsichere Software Keystores.**
- **Sichere Schlüsselerstellung erfordert spezielle Hardware:**
  - **Secure Elements (Android) / Secure Enclave (iOS)** für mobile Geräte.
  - **Key Attestation auf Smartphones** – Beweis, dass der Schlüssel wirklich in einem Hardware-Sicherheitsmodul erzeugt wurde.
  - **Hardware Security Modules (HSM)** – dedizierte Hardware-Boxen für Server-Umgebungen.
- **Beeinflusst die Qualität einer Authentifizierung: Level of Assurance (LoA)** – siehe [[ASP - Authentifizierung - Level of Assurance]].

**Kerngedanke:** Auch der beste kryptografische Algorithmus ist nutzlos, wenn der Private Key oder der ephemerale Schlüssel auf einem unsicheren Speicher liegt, von dem ihn ein Angreifer abgreifen kann. Hardware-Module erzeugen den Private Key intern und geben ihn nie heraus – kryptografische Operationen werden innerhalb des Moduls ausgeführt.

## Bestandteile / Aufbau

| Mechanismus | Plattform | Hauptzweck |
|---|---|---|
| Secure Element (SE) | Android-Geräte, Smartcards | abgeschotteter Chip für Schlüsselspeicherung und Krypto-Operationen |
| Secure Enclave | iOS-Geräte (Apple) | dedizierter Sicherheitskern in Apple-Prozessoren |
| Key Attestation | Smartphones | Beweis, dass ein Schlüssel im SE/Enclave erzeugt wurde |
| Hardware Security Module (HSM) | Server, Banken, CAs | dedizierte Sicherheitsappliance für kryptografische Operationen |

## Beispiel

Aus Folie 32 visualisiert: orangener Kasten mit Schlüssel-Sammlung steht symbolisch für Hardware-Schlüsselspeicher. Folientext nennt explizit Secure Element, Secure Enclave, Key Attestation und HSM.

## Abgrenzung

- **Software-Keystore vs. Hardware-Keystore:** Software-Keystores liegen in normalen Betriebssystem-Speicherbereichen, sind durch Malware oder Speicher-Auslesefehler angreifbar. Hardware-Keystores haben physische und kryptografische Trennungen.
- **Secure Element vs. HSM:** SE ist klein, eingebettet, für Endgeräte. HSM ist groß, eigenständig, für Server. Beide haben dieselbe Idee.
- **Key Attestation:** Liefert den Empfänger der Authentifizierung den Beweis, dass die Gegenseite tatsächlich Hardware-Sicherheit nutzt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Warum sind Software-Keystores unsicher und welche Alternativen gibt es?

**Anwendungsfrage:** Welche Hardware-Sicherheitsmechanismen werden in mobilen Geräten verwendet, welche auf Servern? Wozu dient Key Attestation?

**Diskussionsfrage:** Welche Konsequenz hat ein unsicherer Schlüsselspeicher für PFS-Eigenschaften? (Antwort: Wird ein ephemeraler Schlüssel aus einem unsicheren Software-Speicher abgegriffen, kann die zugehörige Sitzung entschlüsselt werden – PFS bricht zusammen für diese Sitzung. Der retrospektive Schutz für *andere* Sitzungen bleibt aber erhalten, weil deren Schlüssel bereits gelöscht sind.) Wie hängt das mit dem Level of Assurance der eIDAS-Verordnung zusammen?

**Mögliche Anschlussfragen:**
- Was ist genau Key Attestation und welcher Trust-Anchor steht dahinter? (Hersteller-Wurzelzertifikat – im PDF nicht ausgeführt.)
- Wann reicht ein Software-Keystore aus? (Niedrige LoA-Anforderungen, kurzlebige Schlüssel mit niedrigem Schadenpotenzial.)
- Wie unterscheiden sich SE auf Smartcards und SE im Smartphone-Chip technisch?

## Verwandt

- [[ASP - Kryptografie - Perfect Forward Secrecy]]
- [[ASP - Authentifizierung - Level of Assurance]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Zertifikate - X.509]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folie 32

## Ergänzung außerhalb der Vorlesung

Standardisiert sind HSMs nach **FIPS 140-2/3** (US-Bundesstandard, Stufen Level 1–4) und nach **Common Criteria**. Eine **Sichere Signaturerstellungseinheit (SSEE)** im eIDAS-Sinne ist typischerweise eine zertifizierte Smartcard oder ein zertifiziertes HSM, das in einer kontrollierten Umgebung betrieben wird. Apple Secure Enclave ist ein co-prozessor-basiertes Konzept; Android Secure Element kann in Hardware (eSE) oder als Trusted Execution Environment (TEE) realisiert sein.
