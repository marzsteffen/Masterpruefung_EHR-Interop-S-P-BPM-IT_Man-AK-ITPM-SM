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

# ASP - Identitätsprotokoll - OpenID Connect (OIDC)

> [!info] Kurzdefinition
> Modernes Identitätsprotokoll auf Basis von OAuth2, das die Identität eines Benutzers über ein signiertes JSON Web Token (ID-Token) bestätigt. Speziell für Web- und mobile Anwendungen konzipiert.

## Beschreibung

Folie 32 stellt OIDC vor:

- OIDC verwendet **JSON Web Tokens (JWT)**, insbesondere das **ID-Token**, um die Identität des Benutzers zu bestätigen.
- **Leichtgewichtige Implementierung**, was eine einfachere und schnellere Implementierung für Web- und mobile Anwendungen ermöglicht.
- OIDC ist speziell für Web- und Mobile-Anwendungen konzipiert und daher **flexibler für moderne Anwendungsszenarien als SAML2**.

**OIDC-Flow am ELGA-Beispiel (Folie 33):**

1. **Service Request:** Benutzer will auf seine elektronische Gesundheitsakte zugreifen.
2. **Authentication Redirect:** ELGA fordert eine Authentifizierung und leitet den Benutzer zum IdP weiter.
3. **Authentication:** Der IdP führt die Authentifizierung mit dem Benutzer durch.
4. **Authentication Response:** Der IdP sendet eine Antwort an den Benutzer, die einen **Berechtigungscode (Authorization Code)** enthält, welcher wiederum an das Backend der ELGA weitergeleitet wird.
5. **Token Request:** Das Backend der ELGA sendet eine Anfrage an den IdP zur Übermittlung der Identitätsdaten. Dazu wird der Berechtigungscode und ein **geheimes Kennwort (Client Secret)** an den IdP geschickt.
6. **Token Response:** Der IdP antwortet mit dem **ID-Token**, das die Identitätsdaten enthält.
7. Basierend auf den Identitätsdaten werden die jeweiligen Rechte geprüft und Zugriff gewährt oder abgelehnt.

**Unterschied zu SAML2:** Bei OIDC durchläuft der Benutzer nur einen **Authorization Code** (kurzlebiger Code), das eigentliche ID-Token wird **direkt zwischen ELGA-Backend und IdP** ausgetauscht (Server-zu-Server). Damit wandert das eigentliche Token nicht durch den Browser des Nutzers – höhere Sicherheit gegen Token-Diebstahl.

## Bestandteile / Aufbau

| Komponente | Rolle |
|---|---|
| Client / Service Provider | hostet die Anwendung (z. B. ELGA-Backend) |
| Identity Provider (OpenID Provider) | authentifiziert Benutzer, stellt Token aus |
| Resource Owner / Benutzer | der angemeldete Nutzer |
| Authorization Code | kurzlebiger Code, der über den Browser geht |
| Client Secret | geteiltes Geheimnis zwischen Client und IdP |
| ID-Token | JWT mit Identitätsdaten (siehe [[ASP - Identitaetsprotokoll - JWT ID-Token]]) |

## Beispiel

ELGA-Login mit OIDC (Folie 33): Patient öffnet ELGA → Redirect zum IdP → Authentifizierung per Handy-Signatur → IdP schickt Authorization Code zurück → ELGA-Backend tauscht Code + Client Secret gegen ID-Token → Token enthält Identitätsdaten → Zugriff wird gewährt.

## Abgrenzung

- **OIDC vs. [[ASP - Identitaetsprotokoll - SAML2]]:** OIDC nutzt JSON/JWT (kompakter, gut Web/Mobile-tauglich), SAML nutzt XML (schwergewichtig, gut Enterprise-tauglich).
- **OIDC vs. OAuth2:** OAuth2 ist reines Autorisierungsprotokoll (Access Tokens für Ressourcenzugriff). OIDC erweitert es um die Authentifizierungs-Schicht (ID-Token mit Identitätsdaten). *Im PDF nicht ausdrücklich erläutert.*
- **Authorization Code vs. ID-Token:** Der Code ist kurzlebig und nur einmal einlösbar. Das ID-Token ist das eigentliche Identitätsbeweis-Dokument.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist OpenID Connect, und wofür wird es eingesetzt?

**Anwendungsfrage:** Skizzieren Sie den OIDC-Flow am ELGA-Beispiel. Welche Rolle hat der Authorization Code, welche das ID-Token, welche das Client Secret?

**Diskussionsfrage:** Warum ist OIDC heute meist die erste Wahl für Web- und Mobile-Apps gegenüber SAML2? Warum trennt OIDC den Authorization Code von dem ID-Token? (Sicherheits-Argument: Token verlässt nie den Browser.)

**Mögliche Anschlussfragen:**
- Welche Felder enthält ein OIDC-ID-Token? (siehe [[ASP - Identitaetsprotokoll - JWT ID-Token]])
- Was ist der Unterschied zwischen Access Token, ID-Token und Refresh Token?
- Wie wird die Signatur des ID-Tokens validiert? (Über JWKs des IdP – im PDF nicht behandelt.)

## Verwandt

- [[ASP - Identitaetsprotokoll - JWT ID-Token]]
- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Modelle]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folien 32, 33
- Standard: OpenID Connect 1.0 (OpenID Foundation), basiert auf OAuth 2.0 (RFC 6749)
