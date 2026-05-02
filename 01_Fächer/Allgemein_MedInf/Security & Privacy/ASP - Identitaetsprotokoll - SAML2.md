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

# ASP - Identitätsprotokoll - SAML2 (Security Assertion Markup Language 2.0)

> [!info] Kurzdefinition
> XML-basiertes Identitätsprotokoll, das Authentifizierungsergebnisse und Benutzerattribute in Form signierter SAML-Assertions zwischen Identity Provider und Service Provider transportiert.

## Beschreibung

Folie 29 stellt SAML2 vor:

- Identitätsprotokoll mit **XML-basierter Authentifizierung**.
- **SAML-Assertions** (XML-Dokumente) transportieren Authentifizierungsergebnisse und Benutzerattribute.
- Häufige Verwendung für Authentifizierung **älterer Webanwendungen und interner Unternehmensdienste**.

**SAML2-Flow am ELGA-Beispiel (Folie 30):**

1. **Service Request:** Benutzer will auf seine elektronische Gesundheitsakte zugreifen.
2. **Authentication Redirect:** ELGA fordert eine Authentifizierung und leitet den Benutzer zum IdP weiter.
3. **Authentication:** Der IdP führt die Authentifizierung mit dem Benutzer durch.
4. **Authentication Response:** Der IdP sendet eine Antwort an den Benutzer, die eine SAML-Assertion enthält. (*Hinweis: Folie listet Schritte 5 und 6 nicht explizit, springt direkt zu 7.*)
7. Nach einer **erfolgreichen Validierung der SAML2-Assertion** gewährt ELGA dem Benutzer Zugriff auf seine Daten.

**Datenfluss in der Folien-Grafik:**
- Benutzer → Service-Request → SP (ELGA)
- SP → Authentication-Redirect → Benutzer → IdP
- IdP ↔ Benutzer (Authentifizierung)
- IdP → Authentication Response (mit SAML-Assertion) → Benutzer → SP
- SP → Zugriff auf Informationen → Benutzer

Die transportierte SAML-Assertion siehe [[ASP - Identitaetsprotokoll - SAML Assertion]].

## Bestandteile / Aufbau

| Komponente | Rolle |
|---|---|
| Service Provider (SP) | hostet die Anwendung (z. B. ELGA) |
| Identity Provider (IdP) | authentifiziert den Benutzer (z. B. A-Trust) |
| User Agent (Browser) | leitet zwischen SP und IdP um, transportiert Assertion |
| SAML Assertion | XML-Dokument mit Authentifizierungs- und Attribut-Aussagen |

## Beispiel

ELGA-Login (Folie 30): Patient möchte Akte einsehen → ELGA leitet zu A-Trust um → A-Trust authentifiziert per Handy-Signatur → schickt Assertion mit Identitätsdaten zurück → ELGA validiert Assertion und gewährt Zugriff.

## Abgrenzung

- **SAML2 vs. [[ASP - Identitaetsprotokoll - OpenID Connect]]:** SAML ist XML-basiert und schwergewichtig, ideal für klassische Web-Apps und Enterprise-Setups. OIDC nutzt JSON Web Tokens und ist leichtgewichtiger, ideal für Web/Mobile.
- **SAML vs. OAuth2:** OAuth2 ist ein Autorisierungs-Protokoll (Stichwort „Access Token"), nicht primär ein Authentifizierungs-Protokoll. OIDC setzt auf OAuth2 auf und macht daraus ein Authentifizierungs-Protokoll. *Im PDF nicht ausgeführt.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist SAML2, und wo wird es typischerweise eingesetzt?

**Anwendungsfrage:** Skizzieren Sie den SAML2-Flow am Beispiel eines ELGA-Logins. Welche Akteure sind beteiligt, welche Nachrichten werden in welcher Reihenfolge ausgetauscht?

**Diskussionsfrage:** Wann wird SAML2 gegenüber OIDC bevorzugt – und umgekehrt? Welche Trade-offs zwischen XML/JSON, Web/Mobile, Enterprise/Cloud spielen eine Rolle?

**Mögliche Anschlussfragen:**
- Welche Felder enthält eine SAML-Assertion? (siehe [[ASP - Identitaetsprotokoll - SAML Assertion]])
- Wie wird die Assertion vor Manipulation geschützt? (Digitale Signatur durch IdP – im PDF nicht ausgeführt.)
- Wo wird SAML in eHealth-Standards verwendet? (IHE XUA – Cross-Enterprise User Assertion.)

## Verwandt

- [[ASP - Identitaetsprotokoll - SAML Assertion]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Modelle]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[MSI - IHE - XUA]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folien 29, 30
- Standard: SAML 2.0 (OASIS, 2005)
