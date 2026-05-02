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

# ASP - Grüner Pass - Vertrauensmodell (CSCA, DSC, Trust List)

> [!info] Kurzdefinition
> Zweistufige Zertifikatskette pro Mitgliedsland: Country Signing Certificate Authority (CSCA) signiert Document Signer Certificates (DSC); mit DSCs werden die einzelnen DCCs ausgestellt. Alle CSCAs und DSCs sind in der Trust List öffentlich einsehbar.

## Beschreibung

Folie 8 stellt das Vertrauensmodell dar.

**Country Signing Certificate Authority (CSCA):**
- **Vertrauenswürdige Institution jedes teilnehmenden Landes.**
- Zuständig für das Signieren der **Dokumenten-Signaturzertifikate (DSC)**.

**Gesundheitsbehörden:**
- Stellen die EU Digital COVID Certificates aus und signieren sie mit dem **Private Key des zugehörigen Document Signer Certificates**.

**Zertifikatskette (Certificate Chain):**
- Dadurch entsteht eine Verkettung der Zertifikate, die die Vertrauenswürdigkeit der ausgestellten Zertifikate gewährleistet.
- Aufbau: **Country Signing Certificate → Document Signer Certificate → EU Digital COVID Certificate**.

**Trust List:**
- Alle Country Signing Certificates und Document Signer Certificates sind **öffentlich einsehbar und überprüfbar**.
- Die Trust List enthält vertrauenswürdige Zertifikate + Metadaten des Mitgliedsstaats.

## Bestandteile / Aufbau

| Stufe | Wer | Funktion |
|---|---|---|
| 1 | Country Signing Certificate Authority (CSCA) | Pro Land vertrauenswürdige Institution; signiert DSCs |
| 2 | Document Signer Certificate (DSC) | Mit DSC werden einzelne DCCs signiert |
| 3 | EU Digital COVID Certificate (DCC) | Konkretes Zertifikat für eine Person |
| Trust List | EU Gateway | Verteilt Liste aller CSCAs und DSCs an Mitgliedsstaaten |

## Beispiel

In Österreich: Eine staatliche Stelle (z. B. das Sozialministerium) betreibt die CSCA. Sie signiert das DSC, mit dem das Bundesrechenzentrum oder ein anderer Aussteller die einzelnen DCCs erzeugt. Wer ein österreichisches DCC verifiziert, prüft: Ist die DSC-Signatur am Zertifikat gültig? Stammt das DSC von einer in der Trust List geführten österreichischen CSCA?

## Abgrenzung

- **CSCA ↔ DSC:** Analog zur Hierarchie Wurzel-CA / Intermediate-CA in einer normalen PKI.
- **DSC ↔ DCC:** Wie End-Entity-Zertifikat zur konkreten Signatur.
- **Trust List ist nicht der DCC selbst** – sie ist nur die *Liste der vertrauenswürdigen Aussteller*. Das DCC liegt beim Bürger.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie ist das Vertrauensmodell des EU Digital COVID Certificate aufgebaut?

**Anwendungsfrage:** Skizzieren Sie die Zertifikatskette von der CSCA bis zum Zertifikat im Smartphone des Bürgers. Welche Rolle spielt die Trust List?

**Diskussionsfrage:** Welche Schwäche hat dieses Modell – und wie zeigt sich das im Hitler-Adolf-Vorfall? (Antwort: Die Vertrauenskette ist nur so stark wie das schwächste Glied; signiert ein Mitgliedsland nachlässig, sind alle resultierenden DCCs technisch gültig, aber inhaltlich falsch. Siehe [[ASP - Gruener Pass - Sicherheitsbedenken]].)

**Mögliche Anschlussfragen:**
- Wie wird die Trust List verteilt? ([[ASP - Gruener Pass - AT Architektur]] – via EU Gateway.)
- Welcher Krypto-Baustein steckt hinter der Verkettung? (Asymmetrische Signatur, X.509-artig.)
- Was passiert, wenn ein DSC kompromittiert wird? (Widerruf nötig; Trust List entsprechend aktualisieren.)

## Verwandt

- [[ASP - Gruener Pass - EU Digital COVID Certificate]]
- [[ASP - Gruener Pass - AT Architektur]]
- [[ASP - Gruener Pass - Sicherheitsbedenken]]
- [[ASP - Zertifikate - X.509]]
- [[ASP - Zertifikate - PKI]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folie 8
