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

# ASP - Identitätsprotokoll - JWT ID-Token

> [!info] Kurzdefinition
> Vom Identity Provider digital signiertes JSON Web Token, das in OpenID Connect die Identität des authentifizierten Benutzers in kompakter Form transportiert.

## Beschreibung

Folie 34 zeigt ein konkretes ID-Token-Beispiel über das Online-Tool jwt.ms. Ein JWT besteht aus drei Teilen, durch Punkte getrennt:

```
HEADER.PAYLOAD.SIGNATURE
```

In der Folie ist das Token am Anfang als langer Base64-String zu sehen; der Decoded-Teil zeigt die Inhalte:

**Header:**
```json
{
  "alg": "HS256",
  "typ": "JWT"
}
```

**Payload (mit den von der Folie hervorgehobenen Pfeilen):**
```json
{
  "sub": "1234567890",                ← Benutzer
  "name": "John Doe",
  "email": "john.doe@example.com",
  "aud": "https://api.example.com",
  "iss": "https://idps.example.com",  ← Identity Provider
  "exp": 1625128644,                  ← Gültigkeitszeitraum (Ende)
  "iat": 1625128644,
  "jti": "1434385471"
}
```

**Signature:** kryptografisch berechneter Wert, mit dem der IdP das Token signiert. Bei `alg: HS256` wird HMAC-SHA-256 verwendet (in Produktion werden meist asymmetrische Algorithmen wie RS256 oder ES256 bevorzugt – *im PDF nicht hervorgehoben*).

**Standard-Felder (Claims), die in der Folie gezeigt werden:**
- `sub` (Subject): eindeutige ID des Benutzers
- `iss` (Issuer): URL des IdP
- `aud` (Audience): für welchen Empfänger das Token bestimmt ist
- `exp` (Expiration): Ablaufzeit (Unix-Timestamp)
- `iat` (Issued At): Ausstellungszeit
- `jti` (JWT ID): eindeutige Token-ID (gegen Replay)

## Bestandteile / Aufbau

| Teil | Inhalt | Zweck |
|---|---|---|
| Header | `alg`, `typ` | Signaturalgorithmus, Token-Typ |
| Payload | Claims (sub, iss, aud, exp, iat, jti, …) | Identitätsdaten, Gültigkeit |
| Signature | HMAC oder asymmetrische Signatur | Manipulationsschutz, Authentizität des IdP |

## Beispiel

Das Folien-Beispiel: ein ID-Token für „John Doe" (sub = 1234567890), ausgestellt vom IdP `idps.example.com`, gültig bis Unix-Zeit 1625128644 (= 2021-07-01), für den API-Empfänger `api.example.com`.

## Abgrenzung

- **JWT ID-Token vs. [[ASP - Identitaetsprotokoll - SAML Assertion]]:** Beide tragen Identitätsinformationen und sind digital signiert. JWT ist JSON, kompakt, URL-safe. SAML Assertion ist XML, schwergewichtig.
- **ID-Token vs. Access Token:** Im OIDC-/OAuth-Modell trägt das ID-Token die Identität, das Access Token den Zugriff auf APIs. Beide sind oft JWTs, haben aber unterschiedliche Audiences und Inhalte.
- **HS256 vs. RS256/ES256:** HS256 ist symmetrisch (geteiltes Secret), RS256/ES256 sind asymmetrisch (Signatur mit Private Key, Verifizierung mit Public Key). Für föderierte Setups asymmetrisch nötig.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein JWT, und welche drei Teile hat es?

**Anwendungsfrage:** Lesen Sie ein gegebenes JWT-Token und beantworten Sie: Wer ist der Benutzer, wer ist der Issuer, wann läuft es ab, mit welchem Algorithmus signiert?

**Diskussionsfrage:** Warum ist es kritisch, das `aud`-Feld bei der Verifikation zu prüfen? (Antwort: Sonst kann ein Token, das für API X ausgestellt wurde, missbräuchlich an API Y geschickt werden.) Welche Folgen hat es, wenn ein langlebiges JWT gestohlen wird?

**Mögliche Anschlussfragen:**
- Wie hängt JWT mit der zugrunde liegenden Hash- und Signatur-Technik zusammen?
- Was ist eine JWK (JSON Web Key) und ein JWKS-Endpoint? (*Im PDF nicht behandelt.*)
- Welche Rolle spielt das `jti`-Feld für Replay-Schutz?

## Verwandt

- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Identitaetsprotokoll - SAML Assertion]]
- [[ASP - Hash - Funktion]]
- [[ASP - MAC - Grundlagen]]
- [[ASP - Digitale Signatur - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folie 34
- Standards: JWT (RFC 7519), JWS (RFC 7515)
