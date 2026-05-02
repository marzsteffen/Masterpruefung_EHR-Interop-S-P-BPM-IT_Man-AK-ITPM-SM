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

# ASP - Identitätsprotokoll - SAML Assertion

> [!info] Kurzdefinition
> Vom Identity Provider signiertes XML-Dokument, das die Authentifizierungs-Aussage und Attribute eines Benutzers an einen Service Provider transportiert.

## Beschreibung

Folie 31 zeigt eine vereinfachte SAML 2.0 Assertion mit ihren wichtigsten Feldern (Pfeile auf Folie):

- **Identity Provider (Issuer):** Wer hat die Assertion ausgestellt? (z. B. `http://idp.example.org`)
- **Benutzer (Subject / NameID):** Wer ist authentifiziert? (z. B. `j.doe@example.com`)
- **Gültigkeitszeitraum (Conditions):** Ab wann und bis wann ist die Assertion gültig? (NotBefore, NotOnOrAfter)
- **Zeitpunkt der Authentifizierung (AuthnInstant):** Wann wurde authentifiziert?
- **Authentifizierungsmethode (AuthnContextClassRef):** Welche Methode wurde verwendet? (z. B. `PasswordProtectedTransport`)

**XML-Auszug aus Folie 31:**

```xml
<saml:Assertion xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion"
                Version="2.0"
                IssueInstant="2005-01-31T12:00:00Z">
  <saml:Issuer Format="urn:oasis:names:SAML:2.0:nameid-format:entity">
    http://idp.example.org
  </saml:Issuer>
  <saml:Subject>
    <saml:NameID Format="urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress">
      j.doe@example.com
    </saml:NameID>
  </saml:Subject>
  <saml:Conditions
    NotBefore="2005-01-31T12:00:00Z"
    NotOnOrAfter="2005-01-31T12:10:00Z">
  </saml:Conditions>
  <saml:AuthnStatement
    AuthnInstant="2005-01-31T12:00:00Z" SessionIndex="67775277772">
    <saml:AuthnContext>
      <saml:AuthnContextClassRef>
        urn:oasis:names:tc:SAML:2.0:ac:classes:PasswordProtectedTransport
      </saml:AuthnContextClassRef>
    </saml:AuthnContext>
  </saml:AuthnStatement>
</saml:Assertion>
```

**Wichtige Eigenschaften (Folien-Hinweis nicht explizit, aber inhaltlich impliziert):** Die Assertion wird typischerweise vom IdP **digital signiert**, sodass der SP die Echtheit verifizieren kann (siehe [[ASP - Digitale Signatur - Grundlagen]]). Die kurze Gültigkeit (im Beispiel: 10 Minuten) ist ein impliziter Replay-Schutz.

## Bestandteile / Aufbau

| Feld | Bedeutung |
|---|---|
| Issuer | Identity Provider (URL) |
| Subject / NameID | identifizierter Benutzer (z. B. E-Mail) |
| Conditions / NotBefore, NotOnOrAfter | Gültigkeitszeitraum |
| AuthnStatement / AuthnInstant | Zeitpunkt der Authentifizierung |
| AuthnContextClassRef | Authentifizierungsmethode |
| (Signatur) | digitale Signatur des IdP |

## Beispiel

Aus Folie 31: Eine Assertion von `idp.example.org` für den Benutzer `j.doe@example.com`, ausgestellt am 31.01.2005 um 12:00 UTC, gültig 10 Minuten, Authentifizierung per Passwort über sicheren Transportkanal.

## Abgrenzung

- **SAML Assertion vs. [[ASP - Identitaetsprotokoll - JWT ID-Token]]:** Beide transportieren Identitätsinformationen. Assertion ist XML, ID-Token ist JSON. Beide sind digital signiert.
- **Assertion vs. SAML-Protokoll:** Die Assertion ist nur ein Dokument; das SAML2-Protokoll definiert, wie sie ausgetauscht wird (z. B. POST-Binding, Redirect-Binding).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Felder enthält eine SAML-Assertion, und welche Funktion hat jedes?

**Anwendungsfrage:** Lesen Sie eine vorgegebene Assertion und beantworten Sie: Wer hat sie ausgestellt, für wen, wann, mit welcher Authentifizierungsmethode, wie lange ist sie gültig?

**Diskussionsfrage:** Warum ist eine kurze Gültigkeitsdauer wichtig? Welcher Schutz wäre ohne digitale Signatur des IdP nicht gegeben? (Antwort: Manipulation der Assertion durch Eve – Authentizität des IdP wäre nicht prüfbar.)

**Mögliche Anschlussfragen:**
- Wo wird die digitale Signatur in der Assertion eingefügt? (Im XML-Element `<ds:Signature>` – im PDF nicht gezeigt.)
- Welche Rolle spielt der `SessionIndex`?
- Wie unterscheidet sich eine SAML-Assertion in IHE XUA von einer Standard-SAML-Assertion?

## Verwandt

- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsprotokoll - JWT ID-Token]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[MSI - IHE - XUA]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folie 31
- Standard: SAML 2.0 (OASIS, 2005)
