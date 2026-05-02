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

# ASP - Zertifikate - X.509

> [!info] Kurzdefinition
> X.509 ist der Standard-Aufbau eines digitalen Zertifikats: ein von einer Certification Authority signiertes Dokument, das einen Public Key untrennbar an die Identität seines Besitzers bindet.

## Beschreibung

Folie 16 stellt das digitale Zertifikat als Lösung für die Identitätsbindung von Schlüsseln vor:

- **Verwendung von öffentlichen digitalen Zertifikaten (optional)** – sie sind kein zwingender Bestandteil einer Signatur, aber ohne sie fehlt die Identitätsbindung.
- **Public Key ist exakt einer Person zugeteilt (Unterzeichner).**
- **Zertifikat beinhaltet Public Key und Daten des Schlüsselbesitzers.**
- **Verteilung des Zertifikats durch Akteure, die Public-Key-Infrastruktur verwenden.**
- **Ausstellung eines Zertifikats erfordert Authentifizierung des Schlüsselbesitzers.**

**Felder eines X.509-Zertifikats (Folien 16, 20, 21):**

| Feld | Beispielwert (laut Folie 20) |
|---|---|
| Public Key von X | `04EF2835ABFE81F…` |
| Seriennummer des Zertifikates | `0F69BA` |
| Gültigkeitszeitraum | gültig ab 13.08.2013 17:43:22, gültig bis 13.08.2018 15:43:22 |
| Aussteller (CN) | `CN=a-sign-Premium-Sig-02 […]` |
| Eindeutiger Name von X (Antragsteller) | `CN=Klaus Stranacher` |
| Eindeutiger Name der Zertifizierungsstelle | siehe Aussteller |
| Schlüsselverwendung | Digitale Signatur |
| Widerrufsinfo | OCSP/CRL URL |
| Qualifiziertes Zertifikat | Ja/Nein |
| Sichere Signaturerstellungseinheit | Ja/Nein |
| Digitale Unterschrift der Zertifizierungsstelle | (signiert das gesamte Zertifikat) |

**Kerngedanke:** Die CA signiert das gesamte Zertifikat mit ihrem eigenen Private Key. Wer der CA vertraut (deren Public Key/Wurzelzertifikat im Trust Store hat), kann jedem von dieser CA ausgestellten Zertifikat vertrauen.

**Wichtige Anmerkung der Vorlesung (Folie 21, in Rot):** „Eindeutiger Identifier der Person notwendig!" – nur ein eindeutiger Name reicht oft nicht (mehrere Klaus Stranacher), deshalb verlangen qualifizierte Zertifikate eine **Personenbindung** (z. B. über bPK in Österreich, *im PDF nicht ausgeführt*).

## Bestandteile / Aufbau

Siehe Felder-Tabelle oben. Die zentralen Felder, die in der Prüfung gefragt werden können, sind: Public Key, Antragsteller, Aussteller, Gültigkeitszeitraum, Schlüsselverwendung, Widerrufs-URL und CA-Signatur.

## Beispiel

Aus Folie 20: Ein qualifiziertes Signatur-Zertifikat von „a-sign-Premium" (A-Trust, Österreich) für Klaus Stranacher; gültig 5 Jahre; Schlüsselverwendung „Digitale Signatur"; Widerrufsinformation per OCSP/CRL; qualifiziertes Zertifikat nach eIDAS, mit sicherer Signaturerstellungseinheit.

## Abgrenzung

- **X.509 vs. selbst-signiertes Zertifikat:** Selbst-signierte Zertifikate enthalten keinen externen Vertrauensanker und liefern keine echte Identitätsbindung. Sie haben technisch dasselbe Format, aber eine andere Vertrauenssemantik.
- **Zertifikat vs. Public Key allein:** Reiner Public Key sagt nichts darüber aus, *wem* er gehört. Erst das Zertifikat liefert die nachprüfbare Identitätsbindung.
- **X.509 vs. PGP/OpenPGP-Zertifikate:** PGP nutzt ein Web-of-Trust statt einer hierarchischen CA; *im PDF nicht behandelt*.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein X.509-Zertifikat, welche Felder enthält es, und wer signiert es?

**Anwendungsfrage:** Erläutern Sie an einem konkreten Zertifikatsbeispiel, wie der Empfänger einer signierten Nachricht den Zusammenhang zwischen Public Key und Person prüft.

**Diskussionsfrage:** Warum sagt die Vorlesung „eindeutiger Identifier der Person notwendig"? Welche Konsequenzen hat ein unklarer Identifier (Namensgleichheit, Pseudonyme) im rechtlichen Kontext?

**Mögliche Anschlussfragen:**
- Was bedeutet „qualifiziertes Zertifikat" nach eIDAS, und welche Mehrqualität hat es gegenüber einem normalen Zertifikat? (*Im PDF nur als Feld erwähnt; Definition aus eIDAS – siehe Ergänzung.*)
- Was ist eine sichere Signaturerstellungseinheit (SSEE)?
- Wie wird ein Zertifikat zurückgezogen, und wie erfährt der Empfänger davon? (CRL, OCSP – als Felder im Zertifikat genannt.)

## Verwandt

- [[ASP - Zertifikate - PKI]]
- [[ASP - Zertifikate - CSR]]
- [[ASP - Zertifikate - Signaturverifikation]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folien 16, 20, 21
- Standard: ITU-T X.509 (im PDF nicht versionsspezifisch ausgewiesen).

## Ergänzung außerhalb der Vorlesung

Aktueller Standard ist X.509 v3 (RFC 5280 für die Internet-PKI-Profile). Ein **qualifiziertes Zertifikat** im Sinn der eIDAS-Verordnung (EU) Nr. 910/2014 wird von einem qualifizierten Vertrauensdiensteanbieter ausgestellt und erfordert eine sichere Signaturerstellungseinheit (z. B. Smartcard, HSM); eine damit erstellte qualifizierte elektronische Signatur ist juristisch der eigenhändigen Unterschrift gleichgestellt.
