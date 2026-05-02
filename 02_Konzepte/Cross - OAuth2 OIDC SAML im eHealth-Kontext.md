---
typ: konzept
status: offen
faecher: [asp, msi]
quellen:
  - "[[ASP - Identitaetsprotokoll - SAML2]]"
  - "[[ASP - Identitaetsprotokoll - SAML Assertion]]"
  - "[[ASP - Identitaetsprotokoll - OpenID Connect]]"
  - "[[ASP - Identitaetsprotokoll - JWT ID-Token]]"
  - "[[ASP - Identitaetsmanagement - Autorisierung]]"
  - "[[ASP - Identitaetsmanagement - Modelle]]"
  - "[[ASP - Berechtigungsmodelle - Uebersicht]]"
  - "[[MSI - HL7 FHIR - SMART on FHIR]]"
tags:
  - typ/konzept
  - status/offen
  - cross-fach
  - fach/allgemein/asp
  - fach/allgemein/msi
---

# Cross - OAuth2 OIDC SAML im eHealth-Kontext

> [!info] Kurzdefinition
> ASP behandelt SAML2, OpenID Connect und JWT als generische Identitäts-Protokoll-Familie und nutzt ELGA-Login als wiederkehrendes Beispiel. MSI behandelt im SMART-on-FHIR-Note OAuth2 als FHIR-spezifischen Sicherheits-Standard mit Scopes, AuditEvent, Provenance und Consent. Die Brücke zeigt, wie aus ASP-Protokoll-Mechanik das eHealth-Anwendungsmuster SMART on FHIR wird — und wo MSI eine Begriffs-Unschärfe bei OAuth2 produziert, die ASP klar abgrenzt.

## Sicht aus Fach ASP

ASP behandelt die Identitäts-Protokoll-Welt als generische Sicherheits-Schicht über drei Notes plus ELGA-Beispiele.

**SAML2** (siehe [[ASP - Identitaetsprotokoll - SAML2]], Folien 29–30):

- XML-basiertes Identitätsprotokoll. SAML-Assertions transportieren Authentifizierungs- und Attribut-Aussagen zwischen IdP und SP.
- Häufig verwendet für ältere Webanwendungen und interne Unternehmensdienste.
- Akteure: Service Provider (SP), Identity Provider (IdP), User Agent (Browser), SAML Assertion.
- ELGA-Beispiel-Flow: Patient ruft ELGA auf → SP (ELGA) leitet zum IdP (z. B. A-Trust) um → Authentifizierung (z. B. Handy-Signatur) → SAML-Assertion zurück → ELGA validiert → Zugriff. Quelltreue-Hinweis: in der Folie sind Schritte 5 und 6 nicht explizit.

**SAML-Assertion** (siehe [[ASP - Identitaetsprotokoll - SAML Assertion]], Folie 31):

- XML-Dokument, vom IdP signiert. Felder: `Issuer`, `Subject/NameID`, `Conditions/NotBefore/NotOnOrAfter`, `AuthnInstant`, `AuthnContextClassRef`.
- Beispiel mit `PasswordProtectedTransport` als Authentifizierungsmethode, 10 Minuten Gültigkeit.
- Digitale Signatur: Folie 31 nicht explizit, im Fließtext aber als Voraussetzung benannt.

**OpenID Connect** (siehe [[ASP - Identitaetsprotokoll - OpenID Connect]], Folien 32–33):

- Modernes Identitätsprotokoll **auf Basis von OAuth2**.
- Nutzt **JSON Web Tokens (JWT)**, insbesondere das **ID-Token**, um Identität zu bestätigen.
- Leichtgewichtig, web/mobile-tauglich, flexibler als SAML2 für moderne Anwendungen.
- ELGA-Beispiel-Flow: 1) Service Request → 2) Authentication Redirect → 3) Authentication → 4) Authorization Code → 5) Token Request (Code + Client Secret, Backend↔IdP) → 6) Token Response (ID-Token) → 7) Rechte-Prüfung. Wesentlicher Sicherheits-Vorteil: das ID-Token wandert nicht durch den Browser.

**JWT ID-Token** (siehe [[ASP - Identitaetsprotokoll - JWT ID-Token]], Folie 34):

- Drei-Teil-Struktur `HEADER.PAYLOAD.SIGNATURE`, durch Punkte getrennt.
- Standard-Claims: `sub` (Subject/Benutzer), `iss` (Issuer/IdP), `aud` (Audience/Empfänger), `exp` (Expiration), `iat` (Issued At), `jti` (JWT ID gegen Replay).
- HS256 in der Folie, RS256/ES256 in Produktion (im PDF nicht hervorgehoben).

**Begriffs-Klarheit aus ASP** (besonders wichtig für die Brücke):

> Aus [[ASP - Identitaetsprotokoll - OpenID Connect]] (Abgrenzungs-Sektion):
> „**OAuth2 ist reines Autorisierungsprotokoll** (Access Tokens für Ressourcenzugriff). OIDC erweitert es um die Authentifizierungs-Schicht (ID-Token mit Identitätsdaten)."

Auch [[ASP - Identitaetsprotokoll - SAML2]] (Abgrenzung) sagt: „SAML vs. OAuth2: OAuth2 ist ein Autorisierungs-Protokoll (Stichwort ‚Access Token'), nicht primär ein Authentifizierungs-Protokoll. OIDC setzt auf OAuth2 auf und macht daraus ein Authentifizierungs-Protokoll."

**Autorisierung als eigenes Konzept** (siehe [[ASP - Identitaetsmanagement - Autorisierung]]):

- „Authorization is a decision to allow a particular action based on an identifier or attribute" (Clarke).
- Autorisierung ≠ Authentifizierung. Auth. klärt *wer*, Autorisierung *was darf der/die*. Beide trennbar.
- Wie konkrete Rechte vergeben werden, regelt das **Berechtigungsmodell**.

**Berechtigungsmodelle** (siehe [[ASP - Berechtigungsmodelle - Uebersicht]], Folien 13–16):

- Sechs Modelle: **RBAC** (Rollen), **ABAC** (Attribute), **IBAC** (Identitäten direkt), **MAC** (zentrale Sicherheitsregeln), **DAC** (Eigentümer entscheidet), **CBAC** (Kontext, z. B. Tageszeit/Standort).
- eHealth-Praxis: typische Kombination RBAC + ABAC + MAC + CBAC.

**IdM-Modelle** (siehe [[ASP - Identitaetsmanagement - Modelle]], Folien 24–27):

- Vier Modelle: zentral (SP = IdP), isoliert (getrennt), benutzer-zentriert (Daten beim Nutzer), föderiert (mehrere kooperierende IdPs).
- ELGA = isoliertes Modell (A-Trust = IdP, ELGA = SP).
- eIDAS-Notifizierung = föderiertes Modell.

## Sicht aus Fach MSI

MSI behandelt das Sicherheits-Thema kompakt in *einem* Note, fokussiert auf den FHIR-Anwendungsfall.

**SMART on FHIR** (siehe [[MSI - HL7 FHIR - SMART on FHIR]], Seiten 75–76 + Seite 6 „Neues in FHIR"):

- „Substitutable Medical Applications, Reusable Technologies" — community-getriebener Sicherheitsstandard für FHIR-Anwendungen.
- **Sicherheit ist nicht Teil der FHIR-API** (kein Pflichtbestandteil der REST-Spezifikation), aber empfohlen.
- SMART on FHIR = **„essentiell OAuth2"**. (Wörtlich aus dem Note.)
- Dokumentation: `http://docs.smarthealthit.org/`. Sicherheitscheckliste: `http://hl7.org/fhir/safety.html`.

**SMART Scopes** (Folien 6 „Neues in FHIR"):

- Definieren Zugriffsrechte via OAuth2.
- Format: `[context]/[Ressourcentyp].[operation]` — Beispiel `patient/*.read` (lesender Zugriff auf alle Ressourcen *des Patienten*).

**Security-Metadaten-Labels:**

- FHIR-Ressourcen können `meta.security`-Labels tragen (Vertraulichkeitsklassen, Zugriffsbeschränkungen).
- Referenz: `http://hl7.org/fhir/security-labels.html`.

**Auditing- und Datenschutz-Ressourcen:**

| Ressource | Zweck | Verbindlichkeit |
|---|---|---|
| `AuditEvent` | Server-Log bei jedem Ressourcenzugriff | für FHIR-Server empfohlen |
| `Provenance` | Warum wurde eine Ressource modifiziert? | empfohlen |
| `Consent` | Einwilligung für Datenzugriff/Operationen | situationsabhängig |

**Begriffs-Aussage aus MSI** (zitatpflichtig wegen des Konflikt-Risikos zur ASP-Sicht):

> Aus [[MSI - HL7 FHIR - SMART on FHIR]]: „SMART on FHIR (…) verwendet **OAuth2 für Authentifizierung und Autorisierung**."

## Gemeinsamkeiten

| Aussage | Beide Fächer |
|---|---|
| OAuth2 ist Grundlage moderner Web-/Mobile-Auth-Lösungen | ASP über OIDC, MSI über SMART on FHIR |
| Tokens sind digital signiert, kurzlebig, mit Audience-Bindung | ASP (JWT-Claims), MSI (`meta.security`, OAuth2-Tokens) |
| Sicherheit braucht eigene Schicht über dem fachlichen Standard | ASP: IdM ist eigene Vorlesung; MSI: „Sicherheit ist nicht Teil der FHIR-API" |
| Trennung Authentifizierung ↔ Autorisierung | ASP explizit; MSI implizit über OAuth2 + Scopes |
| Audit-Logging als Sicherheits-Eigenschaft | ASP über `Accountability` (Security Eigenschaften); MSI über `AuditEvent` |

## Unterschiede / Konflikte / unterschiedliche Schwerpunkte

**1. Inhalts-Konflikt: „OAuth2 für Authentifizierung?"**

Das ist der wichtigste Cross-Fach-Befund.

- **ASP** sagt klar (in zwei verschiedenen Notes): OAuth2 ist **reines Autorisierungsprotokoll**. Erst OIDC macht aus OAuth2 ein Authentifizierungs-Protokoll, indem es das ID-Token mit Identitätsdaten hinzufügt.
- **MSI** schreibt: „SMART on FHIR (…) verwendet **OAuth2 für Authentifizierung und Autorisierung**."

Diese MSI-Aussage ist unscharf. ASP's Trennung ist die technisch korrekte: OAuth2 (RFC 6749) ist ein Delegations-Framework für Zugriffsrechte (Access Tokens), keine Authentifizierungsmethode. SMART on FHIR im echten Standard nutzt **OAuth2 + OIDC** (oder mindestens OAuth2 plus separate Identitäts-Behauptung) — der MSI-Note vereinfacht das.

In der mündlichen Prüfung: nicht aus MSI heraus argumentieren „OAuth2 ist Authentifizierung". Stattdessen: *„MSI nennt SMART on FHIR ‚essentiell OAuth2'. Technisch genauer ist die ASP-Sicht — OAuth2 regelt nur die Autorisierung, die Identität kommt über OIDC oder eine zusätzliche Identity-Layer."*

**2. SAML im FHIR-Kontext nicht behandelt.**

ASP führt SAML2 ausführlich aus (Folien 29–31). MSI thematisiert SAML im SMART-on-FHIR-Note **nicht**. Der Note erwähnt am Ende „IHE XUA / IUA als IHE-Profile für die gleiche Problematik" — **IHE XUA basiert technisch auf SAML**. Das ist im MSI-MOC als Lücke vermerkt (XUA-Note existiert nicht im Vault).

In der Cross-Fach-Logik bedeutet das: SAML ist im FHIR-/eHealth-Kontext über IHE XUA präsent, wird aber nirgends im Vault eigenständig behandelt. Wer „Welche eHealth-Anwendungen nutzen SAML?" beantworten muss, antwortet aus ASP-SAML2 + dem Hinweis-Verweis aus dem MSI-MOC, nicht aus einem MSI-Note.

**3. Detailtiefe der Token-Mechanik.**

- ASP: detaillierte JWT-Anatomie (Header/Payload/Signature, alle Claim-Felder, HS256/RS256-Vergleich, Replay-Schutz via `jti`).
- MSI: erwähnt Tokens nur als Mechanismus, ohne Header-/Claim-/Signatur-Details.

Konsequenz: JWT-Detailfragen werden aus ASP beantwortet.

**4. Berechtigungsmodelle vs. SMART Scopes — getrennte Welten.**

- ASP listet sechs generische Berechtigungsmodelle (RBAC, ABAC, IBAC, MAC, DAC, CBAC) ohne FHIR-Bezug.
- MSI nennt nur SMART Scopes als FHIR-spezifischen Mechanismus mit Format `[context]/[Ressourcentyp].[operation]`.

Mapping ist nicht trivial: SMART Scopes sind **am ehesten ABAC-artig** (Attribute = context + Ressourcentyp + Operation), aber tragen auch RBAC-Züge (`patient/*` vs. `practitioner/*` ist quasi-rollenbasiert). Beide Notes machen dieses Mapping nicht — die Brücke macht es als Synthese-Punkt sichtbar.

**5. ELGA-Login als Querschnitt, aber unterschiedlich genutzt.**

ASP nutzt ELGA-Login als wiederkehrendes Beispiel — sowohl im SAML2-Note (Folie 30) als auch im OIDC-Note (Folie 33). Die Folien zeigen denselben fachlichen Use Case (Patient → Akte) zweimal, einmal mit SAML2-Mechanik, einmal mit OIDC-Mechanik. ELGA in der Realität nutzt **isoliertes IdM-Modell** mit A-Trust als IdP.

MSI nutzt ELGA-Login im SMART-on-FHIR-Note **nicht** als Beispiel — der Note bleibt protokoll-generisch.

**6. Audit-Mechanik: ASP-Eigenschaft vs. MSI-Ressource.**

- ASP behandelt Audit/Logging über die Security-Eigenschaft `Accountability` und die Anforderung an Authentifizierungs-Mechanik (Token-Tracing, `jti`).
- MSI hat **eigene FHIR-Ressource** `AuditEvent` plus `Provenance` plus `Consent` — also einen ressourcen-zentrierten Audit-Apparat *innerhalb* von FHIR.

Das ist kein Konflikt, sondern eine **Schicht-Trennung**: ASP sagt „eHealth-Systeme brauchen Audit", MSI sagt „in FHIR werden Audits als eigene Ressourcen modelliert".

**7. IdP-/SP-Vokabular vs. FHIR-Vokabular.**

- ASP-Vokabular: Service Provider, Identity Provider, User Agent, Resource Owner, Client, Authorization Code, Client Secret, Access Token, ID-Token, SAML Assertion.
- MSI-Vokabular im SMART-Note: SMART Scopes, FHIR-Server, Resource Server, `meta.security`, `AuditEvent`, `Provenance`, `Consent`.

Wer in der Prüfung zwischen den Welten wechselt, sollte das Vokabular synchronisiert nutzen: FHIR-Server = Resource Server (in OAuth2-Sprech), Patient-App = Client.

## Synthese für die mündliche Prüfung

**Diskussions-Achse 1: „Wie funktioniert SMART on FHIR?"**

Antwort braucht beide Fächer. Aus MSI das *Was*: OAuth2-basierter Sicherheits-Standard, Scopes, AuditEvent, Provenance, Consent. Aus ASP das *Wie*: OAuth2-Autorisierungs-Flow, ggf. mit OIDC für Identität, JWT-basierte Tokens, ID-Token-Claims. Korrekte Antwort schließt mit: SMART on FHIR ist im Prinzip OAuth2-Autorisierung, nicht Authentifizierung — die Identität kommt aus einer zusätzlichen Schicht.

**Diskussions-Achse 2: „SAML2 vs. OIDC — wann was?"**

Aus [[ASP - Identitaetsprotokoll - SAML2]] und [[ASP - Identitaetsprotokoll - OpenID Connect]]:

| Achse | SAML2 | OIDC |
|---|---|---|
| Format | XML | JSON / JWT |
| Gewicht | schwergewichtig | leichtgewichtig |
| Use Case | klassische Web-Apps, Enterprise, IHE XUA | Web/Mobile, moderne APIs, SMART on FHIR |
| Token-Lebensweg | Assertion via Browser | Authorization Code via Browser, ID-Token Server↔Server |
| Sicherheit | Assertion-Signatur | Token außerhalb des Browsers, Code one-time |

Pointe für eHealth: ELGA-Login ist klassisch SAML2-basiert (entspricht „Enterprise/Federated"); SMART on FHIR ist OAuth2/OIDC-basiert (entspricht „Modern Mobile/API").

**Diskussions-Achse 3: „OAuth2 — Authentifizierung oder Autorisierung?"**

Klare Antwort aus ASP: **Autorisierung**. Wer aus MSI heraus „beides" sagt, ist technisch unscharf. Saubere Antwort: OAuth2 regelt die Delegation von Zugriffsrechten (Access Tokens). Authentifizierung ist eine *separate* Frage, die meist via OIDC obendrauf gelöst wird. SMART on FHIR baut deshalb in der Praxis auf OAuth2 + OIDC (oder OAuth2 + IHE XUA + SAML) auf, nicht auf OAuth2 allein.

**Diskussions-Achse 4: „Berechtigungsmodelle und SMART Scopes."**

Die Brücke ist hier kein Konflikt, sondern eine *fehlende Verbindung* in den Vault-Notes. SMART-Scopes (`patient/*.read`) sind in der Mechanik ABAC-artig (kontextuelle Attribute) mit RBAC-Zügen (Patient vs. Practitioner). Die ASP-Berechtigungsmodelle-Übersicht ordnet Scopes nicht zu — die Cross-Fach-Antwort macht das auf: „SMART Scopes implementieren effektiv eine Kombination aus RBAC und ABAC, nicht ein einzelnes Modell."

**Diskussions-Achse 5: „Wie wird ein FHIR-Zugriff geprüft?"**

Antwort kombiniert ASP-Mechanik und MSI-Ressourcen:

1. App fordert Authorization Code beim IdP (OIDC, ASP).
2. Backend tauscht Code + Client Secret gegen Access Token (mit SMART Scopes) und ID-Token (OIDC, ASP).
3. App ruft FHIR-Endpunkt mit Access Token im Authorization-Header (MSI).
4. FHIR-Server prüft Token-Signatur (`aud`, `exp`, `iss`), prüft Scope gegen die angeforderte Operation (MSI/ASP-Schnittstelle).
5. FHIR-Server schreibt `AuditEvent` (MSI), aktualisiert `Provenance` bei Änderungen.

**Anschlussfragen, die ohne Cross-Fach-Verständnis schwer zu beantworten sind:**

- „Wann nutzt man OAuth2 ohne OIDC?" → wenn nur Autorisierung gebraucht wird, z. B. App ruft auf APIs zu, ohne den User zu identifizieren. Aus ASP-Begriffsklarheit, in MSI nicht beantwortet.
- „Wie wird die Identität in SMART on FHIR garantiert?" → über zusätzliche OIDC-Schicht oder IHE XUA. MSI's „OAuth2 für Authentifizierung" reicht hier nicht.
- „Welche FHIR-Ressource entspricht dem ASP-Konzept ‚Accountability'?" → `AuditEvent`. Beide Fächer braucht.
- „Wie modelliert man Patientenzustimmung in einem FHIR-Server?" → `Consent`-Ressource (MSI), eingebettet in ein DSGVO-Compliance-Framework (ASP-Teilbereich; siehe Brücke 6).
- „Was wäre eine SMART-on-FHIR-Realisierung des ASP-RBAC-Modells?" → Scope-Pattern `practitioner/Patient.read` + Rollen-basierte Token-Vergabe durch IdP.

## Verwandt

**ASP:**
- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsprotokoll - SAML Assertion]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Identitaetsprotokoll - JWT ID-Token]]
- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Identitaetsmanagement - Autorisierung]]
- [[ASP - Identitaetsmanagement - Modelle]]
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Multifaktor-Authentifizierung]]
- [[ASP - Authentifizierung - Level of Assurance]]
- [[ASP - Berechtigungsmodelle - Uebersicht]]
- [[ASP - Security Eigenschaften - Accountability]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Diagram - OIDC Authentifizierungsflow]]
- [[ASP - Diagram - IdM Modelle Vergleich]]

**MSI:**
- [[MSI - HL7 FHIR - SMART on FHIR]]
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - IHE XDS - Architektur]]

**Andere Brücken:**
- [[Cross - ELGA als nationaler eHealth-Use-Case]] (ELGA-Login im IdM-isolierten Modell — Anwendungsfall)
- [[Cross - HL7 FHIR und CDA in MSI vs EHR]] (FHIR als Ziel-Standard, gegen den die Sicherheit greift)

**MOCs:**
- [[ASP - MOC]]
- [[MSI - MOC]]

## Quelle

Cross-Fach-Synthese aus den oben gelisteten ASP- und MSI-Konzept-Notes. Keine externen Ergänzungen außerhalb der Vault-Quellen.

**Wichtiger Quellen-Konflikt:**

- ASP-OIDC-Note (Abgrenzung): „OAuth2 ist reines Autorisierungsprotokoll (Access Tokens für Ressourcenzugriff). OIDC erweitert es um die Authentifizierungs-Schicht."
- ASP-SAML2-Note (Abgrenzung): identisch — „OAuth2 ist ein Autorisierungs-Protokoll (…), nicht primär ein Authentifizierungs-Protokoll."
- MSI-SMART-on-FHIR-Note (Beschreibung): „SMART on FHIR (…) verwendet OAuth2 für Authentifizierung und Autorisierung."

Die ASP-Aussage ist die technisch korrektere; die MSI-Aussage ist im FHIR-Kontext üblich-unscharf. In der Synthese-Sektion explizit benannt, nicht harmonisierend übermalt.

**Fach-Zuordnung der Quellen:**

| Note | Fach |
|---|---|
| ASP - Identitaetsprotokoll - SAML2 / SAML Assertion / OpenID Connect / JWT ID-Token | ASP |
| ASP - Identitaetsmanagement - Autorisierung / Modelle | ASP |
| ASP - Berechtigungsmodelle - Uebersicht | ASP |
| MSI - HL7 FHIR - SMART on FHIR | MSI |
