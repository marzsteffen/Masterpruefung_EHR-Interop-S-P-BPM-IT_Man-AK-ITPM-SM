---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Gruener Pass]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Grüner Pass - EU Digital COVID Certificate (Verordnung)

> [!info] Kurzdefinition
> Mit der EU-Verordnung 2021/953 vom 1. Juli 2021 eingeführter pan-europäischer digitaler Statusnachweis. Drei Zertifikatstypen (Impf-, Test-, Genesungszertifikat), enthält QR-Code und digitale Signatur, ausgestellt durch nationale Behörden.

## Beschreibung

Folie 6 stellt den rechtlichen Rahmen vor.

**Verordnung über die EU Digital COVID Certificates (1. Juli 2021):**
- Für die Ausstellung der Zertifikate sind die nationalen Behörden zuständig.
- Enthält einen **QR-Code** und eine **digitale Signatur** von einem **EU Gateway**.

**Aus Gründen der Datenminimierung sollten Zertifikate nur unbedingt erforderliche personenbezogene Daten enthalten.**

**Drei Zertifikatstypen (Folie 6 visualisiert):**
1. **Impfzertifikat (Vaccination Certificate)**
2. **Testzertifikat (Test Certificate)**
3. **Genesungszertifikat (Certificate of Recovery)**

Jedes Zertifikat besteht aus:
- Einer für den Menschen lesbaren Darstellung (Name, Datum, Land etc.).
- Einem **QR-Code** mit den signierten Rohdaten.
- Einer **digitalen Signatur**, die mit dem Document Signer Certificate des ausstellenden Landes erzeugt wurde.

## Bestandteile / Aufbau

| Komponente | Funktion |
|---|---|
| QR-Code | Maschinenlesbare, signierte Repräsentation der Zertifikatsdaten |
| Digitale Signatur | Authentizitäts- und Integritätsschutz |
| Aussteller | Nationale Behörde (z. B. Gesundheitsministerium) |
| Rechtsgrundlage | EU-Verordnung 2021/953 |
| Datenminimierung | nur unbedingt erforderliche personenbezogene Daten |

## Beispiel

Ein österreichisches Impfzertifikat: Republik-Österreich-Logo, Vor-/Nachname „Musterfrau-Gößfinger", Geburtsdatum, Impfstoff-Code (z. B. EU/1/20/1528 = Comirnaty), Datum, signiert vom österreichischen Gesundheitsministerium über sein Document Signer Certificate.

## Abgrenzung

- **DCC ist NICHT verschlüsselt.** Es ist *signiert*. Inhalte sind technisch öffentlich lesbar; Schutz der Privatsphäre erfolgt über Datenminimierung und die Beschränkung in Validator-Apps.
- **DCC ist NICHT zentralisiert gespeichert.** Es liegt nur beim Bürger (Smartphone, Papier-Ausdruck). Zentral ist nur die Trust List der Aussteller-Zertifikate.
- **EU Gateway signiert nicht direkt das Zertifikat** (Folie 6 sagt das missverständlich: „digitale Signatur von einem EU Gateway"). In Wirklichkeit signiert die nationale CSCA bzw. DSC; das EU Gateway verteilt nur die Trust List. Siehe [[ASP - Gruener Pass - Vertrauensmodell]].

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wann und auf welcher Rechtsgrundlage wurde das EU Digital COVID Certificate eingeführt? Welche drei Zertifikatstypen gibt es?

**Anwendungsfrage:** Beschreiben Sie die zwei Bestandteile eines DCC-Dokuments. Welche dient welchem Zweck?

**Diskussionsfrage:** Warum ist Datenminimierung im DCC-Design wichtig? Welche personenbezogenen Daten würden Sie als „unbedingt erforderlich" bezeichnen, welche nicht? (Vorname, Nachname, Geburtsdatum vs. Adresse, SVNR, Telefonnummer.)

**Mögliche Anschlussfragen:**
- Welche Schutzziele werden durch Signatur erfüllt? (Authentizität, Integrität, Non-repudiation – siehe [[ASP - Digitale Signatur - Grundlagen]].)
- Wie funktioniert die Vertrauenskette der DCC-Signatur? (Siehe [[ASP - Gruener Pass - Vertrauensmodell]].)
- Welche DSGVO-Grundsätze adressiert die Verordnung? (Datenminimierung, Zweckbindung.)

## Verwandt

- [[ASP - Gruener Pass - Ausgangssituation]]
- [[ASP - Gruener Pass - Vertrauensmodell]]
- [[ASP - Gruener Pass - DCC-Schema]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - DSGVO - Grundsaetze]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folie 6
- Rechtsgrundlage: Verordnung (EU) 2021/953, https://eur-lex.europa.eu/legal-content/DE/TXT/PDF/?uri=CELEX:32021R0953
