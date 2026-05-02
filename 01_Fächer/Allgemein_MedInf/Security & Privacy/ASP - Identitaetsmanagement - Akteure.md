---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Identitaetsmanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Identitätsmanagement - Akteure

> [!info] Kurzdefinition
> Vier Akteure in einem IdM-System: Benutzer, Identity Provider (IdP), Service Provider (SP) und Kontrollorgan.

## Beschreibung

Folie 23 stellt die vier Akteure vor.

### Benutzer
- Möchte sich an einem Service anmelden (z. B. ELGA).
- Möchte mit seiner digitalen Identität auf Daten zugreifen (z. B. Patientenakte).
- Übermittelt Authentifizierungsmittel zum Identity Provider (z. B. Name, Passwort).

### Identity Provider (IdP)
- Führt die **Überprüfung der Person** durch (z. B. A-Trust).
- Identifizierung und Authentifizierung wird durchgeführt.
- Übermittelt Attribute eines Benutzers an Service Provider.

### Service Provider (SP)
- **Bietet Service an** (z. B. ELGA).
- Bietet Services / Ressourcen für Benutzer an (z. B. Patientenakte aufrufen).
- Arbeitet mit Identitätsdaten des Identity Providers.

### Kontrollorgan
- **Überwachungsfunktion** (z. B. Staat).
- Überprüft Einhaltung von Richtlinien / Policies.
- Hat die Möglichkeit zur Durchführung von Prüfungen.

**Datenfluss laut Folien-Grafik:**
- Benutzer → Anmeldeinformationen → IdP
- IdP → Authentifizierungsergebnis + Identitätsdaten → SP
- SP → Gewährt Zugriff auf Daten → Benutzer
- Kontrollorgan überwacht die ganze Konstellation.

## Bestandteile / Aufbau

| Akteur | Rolle | Beispiel |
|---|---|---|
| Benutzer | will Zugriff auf einen Service | Patient, Arzt |
| Identity Provider (IdP) | prüft Identität, gibt Identitätsdaten weiter | A-Trust, ID Austria |
| Service Provider (SP) | bietet den Service an | ELGA |
| Kontrollorgan | überwacht Policy-Einhaltung | Staat, Aufsichtsbehörde |

## Beispiel

Patient meldet sich bei ELGA an. ELGA (SP) leitet ihn an A-Trust (IdP) weiter. A-Trust authentifiziert ihn per Handy-Signatur und schickt SAML-Assertion mit seinen Identitätsdaten zurück an ELGA. ELGA gewährt Zugriff auf die Akte. Die Datenschutzbehörde / der Staat fungiert als Kontrollorgan.

## Abgrenzung

- **Benutzer ≠ digitale Identität:** Eine Person kann mehrere digitale Identitäten besitzen.
- **IdP ≠ SP:** Im zentralen IdM-Modell fallen IdP und SP zusammen; in den anderen drei Modellen sind sie getrennt.
- **Kontrollorgan ist nicht in jedem Setup explizit vorhanden** – in privaten oder Unternehmensnetzwerken übernimmt diese Rolle oft die interne Compliance.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Akteure gibt es in einem IdM-System, und welche Rolle hat jeder?

**Anwendungsfrage:** Ordnen Sie an einem konkreten Beispiel (ELGA, ID Austria) die Akteure zu. Wer ist IdP, wer SP, wer Kontrollorgan?

**Diskussionsfrage:** Wie ändern sich die Akteurs-Rollen, wenn man vom zentralen ins föderierte Modell wechselt? Welche Vertrauensbeziehungen sind nötig?

**Mögliche Anschlussfragen:**
- Welche Identitätsdaten gibt der IdP an den SP weiter?
- Welche DSGVO-Pflichten hat der IdP als „Verantwortlicher"?
- Was passiert, wenn der IdP ausfällt? (Hängt vom Modell ab – siehe [[ASP - Identitaetsmanagement - Modelle]].)

## Verwandt

- [[ASP - Identitaetsmanagement - Modelle]]
- [[ASP - Identitaetsmanagement - Definition]]
- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Authentifizierung - Level of Assurance]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folie 23
