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

# ASP - Identitätsmanagement - Definition (IdM)

> [!info] Kurzdefinition
> Identitätsmanagement (IdM) bündelt Prozesse, Technologien und Richtlinien zur Verwaltung digitaler Identitäten und ihrer Zugriffe auf Ressourcen.

## Beschreibung

Folie 18 zitiert die Microsoft-Definition:

> *„Identity and access management combines processes, technologies, and policies to manage digital identities and specify how they are used to access resources." [Microsoft]*

**Eckpunkte:**
- Management des **Lebenszyklus** einer digitalen Identität – siehe [[ASP - Identitaetsmanagement - Lebenszyklus]].
- Management von **Zugriffsrechten auf Ressourcen** – siehe [[ASP - Berechtigungsmodelle - Uebersicht]].
- **Verschiedene Dimensionen** je nach Geltungsbereich:
  - Innerhalb einer Anwendung / App
  - Innerhalb eines Systems (z. B. eines Unternehmens)
  - Innerhalb eines Netzwerks oder eines Landes (z. B. nationale ID-Systeme)

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Prozesse | Registrierung, Authentifizierung, Autorisierung, Wartung, Löschung |
| Technologien | IdP-Systeme, Verzeichnisdienste, Protokolle (SAML, OIDC), Tokens |
| Richtlinien (Policies) | Regeln zu Identitätserstellung, Authentifizierung, Zugriff, Audit |
| Geltungsbereich | App / System / Netzwerk-Land |

## Beispiel

Die ELGA-Plattform ist ein länderweites IdM-System für das österreichische Gesundheitswesen: ID Austria als Identity Provider, ELGA-Portal als Service Provider, Zugriffsrichtlinien (Patient kann Akteure sperren), Audit-Logging.

## Abgrenzung

- **IdM ist breiter als reine Authentifizierung.** Es umfasst auch Lifecycle, Governance, Audit.
- **IdM ist nicht dasselbe wie ein Berechtigungsmodell.** Das Berechtigungsmodell ist *ein Baustein* innerhalb eines IdM-Systems.
- **Identity Management vs. Access Management:** Microsoft fasst beides zu IAM zusammen; einige Frameworks trennen Identitätsverwaltung (Wer?) und Zugriffsverwaltung (Was darf wer?).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Identitätsmanagement, und welche Aspekte fasst es zusammen?

**Anwendungsfrage:** Beschreiben Sie ein konkretes IdM-System (z. B. ELGA, ID Austria, Microsoft 365) und ordnen Sie seine Komponenten den Aspekten Prozesse / Technologien / Richtlinien zu.

**Diskussionsfrage:** Welche Dimension (App / System / Netzwerk-Land) bringt welche zusätzlichen Herausforderungen? (Stichwort: Cross-Border-Identitäten in eIDAS, IHE XUA für Cross-Domain Healthcare.)

**Mögliche Anschlussfragen:**
- Welche Phasen hat der IdM-Lebenszyklus?
- Welche Akteure spielen in einem IdM-System eine Rolle?
- Welche Rolle spielt Governance?

## Verwandt

- [[ASP - Identitaetsmanagement - Lebenszyklus]]
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Modelle]]
- [[ASP - Berechtigungsmodelle - Uebersicht]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folie 18
