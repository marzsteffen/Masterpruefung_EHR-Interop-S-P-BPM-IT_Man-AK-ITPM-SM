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

# ASP - Zertifikate - Public Key Infrastructure (PKI)

> [!info] Kurzdefinition
> System aus Rollen, Diensten und Zertifikaten, das die Identitätsbindung von Public Keys ausstellt, verwaltet, widerruft und überprüfbar macht.

## Beschreibung

Folie 18 listet die sechs Bestandteile einer PKI:

1. **Digitale Zertifikate** – die ausgestellten Bindungen zwischen Public Key und Identität ([[ASP - Zertifikate - X.509]]).
2. **Zertifizierungsstelle (CA – Certification Authority)** – stellt Zertifikate aus, signiert sie mit ihrem eigenen Private Key.
3. **Registrierungsstelle (RA – Registration Authority)** – nimmt Antragsteller-Daten entgegen, prüft die Identität und leitet Anträge an die CA weiter.
4. **Zertifikatssperrliste (CRL – Certificate Revocation List)** – Liste widerrufener Zertifikate (vor Ablauf der Gültigkeit).
5. **Verzeichnisdienst** – stellt ausgestellte Zertifikate öffentlich zum Abruf bereit.
6. **Validierungsdienst (VA – Validation Authority)** – beantwortet Anfragen zum aktuellen Status eines Zertifikats (typisch via OCSP).

**Ablauf in der Vorlesung-Grafik (Folie 18):**
- Antragsteller geht zur RA (3) und stellt Antrag.
- RA leitet an CA (2), die das Zertifikat ausstellt (1, signiert).
- Zertifikat geht an Antragsteller, der es bei einem Dienst (z. B. shop.com) verwendet.
- Sperrlisten (4) gehen von der CA an die VA (6).
- Verzeichnisdienst (5) sammelt ausgegebene Zertifikate.
- Wer ein Zertifikat verifizieren will, fragt die VA (6) nach dem aktuellen Status.

## Bestandteile / Aufbau

| Bestandteil | Rolle |
|---|---|
| Digitale Zertifikate | das ausgestellte Beweisstück |
| CA (Certification Authority) | Zertifikatsaussteller |
| RA (Registration Authority) | Identitätsprüfung der Antragsteller |
| CRL (Certificate Revocation List) | Sperrliste widerrufener Zertifikate |
| Verzeichnisdienst | Bereitstellung ausgestellter Zertifikate |
| VA (Validation Authority) | Online-Statusabfrage (z. B. OCSP) |

## Beispiel

Aus Folie 18: Beispielhafter Ablauf einer Online-Bestellung mit Browser-TLS – Browser prüft das Server-Zertifikat über die VA (OCSP-Anfrage) und kann auf eine CRL zurückgreifen, falls die VA nicht erreichbar ist.

## Abgrenzung

- **PKI vs. Web-of-Trust:** PKI ist hierarchisch mit Vertrauensanker bei einer (Wurzel-)CA. Web-of-Trust (PGP) hat keine zentrale Autorität, *im PDF nicht behandelt*.
- **CA vs. RA:** CA ist die signierende Stelle; RA übernimmt operative Identitätsprüfung. Bei kleinen Setups identisch, bei großen getrennt.
- **CRL vs. OCSP:** CRL ist eine Liste, die der Client periodisch herunterlädt; OCSP ist eine Live-Anfrage zum Einzelzertifikat. Beides gehört zur VA-Funktion. *Im PDF nur als Felder im X.509-Zertifikat genannt.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine PKI und aus welchen Bestandteilen besteht sie?

**Anwendungsfrage:** Skizziere am Beispiel einer signierten ärztlichen Verordnung, welche PKI-Bestandteile bei Ausstellung, Verwendung und Widerruf des Signatur-Zertifikats zum Einsatz kommen.

**Diskussionsfrage:** Warum gibt es die Trennung zwischen CA und RA? Welche Schwächen hat eine PKI insgesamt? (Stichworte: Wurzelzertifikat-Kompromittierung, mangelnde Sperrabfrage in der Praxis, Fehler in der Identitätsprüfung der RA.) Was passiert, wenn eine vertrauenswürdige Wurzel-CA kompromittiert wird?

**Mögliche Anschlussfragen:**
- Wie unterscheiden sich CRL und OCSP technisch und operativ?
- Was passiert, wenn die VA nicht erreichbar ist – akzeptiert man das Zertifikat oder lehnt man ab? (OCSP-Stapling, „soft-fail" vs. „hard-fail" – im PDF nicht behandelt.)
- Warum ist eine kompromittierte Wurzel-CA so kritisch? (Sie kann beliebige Identitäten bezeugen.)

## Verwandt

- [[ASP - Zertifikate - X.509]]
- [[ASP - Zertifikate - CSR]]
- [[ASP - Zertifikate - Signaturverifikation]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folie 18

## Ergänzung außerhalb der Vorlesung

In der Praxis gibt es meist eine mehrstufige PKI: eine **Root CA** (offline, hochgesichert) signiert eine oder mehrere **Intermediate CAs**, die wiederum Endteilnehmer-Zertifikate ausstellen. Diese Trennung erlaubt im Schadensfall, eine Intermediate CA zu sperren, ohne die gesamte Wurzel zu wechseln. Bekannte Browser-Trust-Stores (Mozilla, Apple, Microsoft, Google) führen Listen vertrauenswürdiger Wurzel-CAs. Das Certificate Transparency-Programm (RFC 6962) protokolliert ausgestellte Zertifikate öffentlich und macht missbräuchlich ausgestellte Zertifikate auffindbar.
