---
fach: asp
typ: pruefungsfrage
status: offen
niveau: vertiefung
tags:
  - fach/allgemein/asp
  - typ/pruefungsfrage
  - status/offen
---

# ASP - PF - Identitätsmanagement Detail

## Kontext

Prüfungskarten für die mündliche Masterprüfung ASP. Thema: Identitätsmanagement – Definition, Akteure, Authentifizierungs- und Autorisierungskonzepte, IdM-Lebenszyklus, Berechtigungsmodelle, SAML2, OIDC, MFA, IdM-Modelle.

## Verlinkte Konzepte

- [[ASP - Identitaetsmanagement - Definition]]
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Identitaetsmanagement - Authentifizierungsklassen]]
- [[ASP - Identitaetsmanagement - Multifaktor-Authentifizierung]]
- [[ASP - Identitaetsmanagement - Autorisierung]]
- [[ASP - Identitaetsmanagement - Lebenszyklus]]
- [[ASP - Identitaetsmanagement - Modelle]]
- [[ASP - Berechtigungsmodelle - Uebersicht]]
- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Identitaetsprotokoll - JWT ID-Token]]
- [[ASP - Identitaetsprotokoll - SAML Assertion]]

---

## Karten

### Definition

Was ist Identitätsmanagement (IdM), welche Aspekte umfasst es, und welche vier Akteure gibt es in einem IdM-System?

?

**Definition (Folie 18, Microsoft):** „Identity and access management combines processes, technologies, and policies to manage digital identities and specify how they are used to access resources."

**Drei Aspekte:**
| Aspekt | Inhalt |
|---|---|
| Prozesse | Registrierung, Authentifizierung, Autorisierung, Wartung, Löschung |
| Technologien | IdP-Systeme, Verzeichnisdienste, Protokolle (SAML, OIDC), Tokens |
| Richtlinien (Policies) | Regeln zu Identitätserstellung, Authentifizierung, Zugriff, Audit |

**Geltungsbereiche:** innerhalb einer Anwendung / eines Systems / eines Netzwerks oder Landes.

**Vier Akteure (Folie 23):**
| Akteur | Rolle | Beispiel |
|---|---|---|
| Benutzer | will Zugriff auf Service | Patient |
| Identity Provider (IdP) | prüft Identität, gibt Identitätsdaten weiter | A-Trust |
| Service Provider (SP) | bietet den Service an | ELGA |
| Kontrollorgan | überwacht Policy-Einhaltung | Staat / Datenschutzbehörde |

---

Wie unterscheiden sich Identifizierung, Authentisierung und Authentifizierung – und wer führt jeweils welche Handlung durch?

?

**Drei-Schritt-Sequenz am Reisepass-Beispiel (Folie 8):**

| Begriff | Handelnder | Was passiert |
|---|---|---|
| **Identifizierung** | Subjekt | behauptet, eine bestimmte Identität zu sein (z. B. „Ich bin Max Mustermann.") |
| **Authentisierung** | Subjekt | übergibt / präsentiert einen Identitätsnachweis (z. B. Reisepass vorzeigen) |
| **Authentifizierung** | Prüfender | überprüft den Nachweis auf Gültigkeit (z. B. Reisepass-Echtheitsprüfung) |

**Definitionen:**
- Identifizierung: „Identification is the association of a personal identifier with an individual presenting attributes." [Clarke]
- Authentifizierung: „Authentication is proof of an attribute." [Clarke] / „The process of verifying a subject's identity or other claim." [GINI-SA]

**Wichtig:** Authentifizierung ≠ Autorisierung: Auth. klärt „Wer?", Autorisierung klärt „Was darf der/die?"

---

Welche vier Klassen von Authentifizierungs-Faktoren gibt es, und welche typischen Schwächen haben sie?

?

**Vier Klassen (Folie 9):**

| Klasse | Slogan | Beispiele | Schwäche |
|---|---|---|---|
| Wissen | „etwas wissen" | Passwort, PIN | Phishing, Erraten, Wiederverwendung |
| Besitz | „etwas besitzen" | Reisepass, Smartcard, Bankomatkarte | Diebstahl, Verlust |
| Biometrische Eigenschaft | „etwas sein" | Fingerprint, Gesichtserkennung, Iris | unveränderbar bei Kompromittierung; Datenschutz |
| Verhaltensmuster | „etwas tun" | Tippverhalten, Verweildauer in Apps | unsicher als alleiniger Faktor; Datenschutz |

**Kernregel für MFA:** Echte Multifaktor-Authentifizierung kombiniert Faktoren aus **verschiedenen Klassen**. Zwei Passwörter sind kein 2FA – beide liegen in der Klasse „Wissen".

---

Welche sechs Berechtigungsmodelle kennt die Vorlesung, und was ist das Kernprinzip jedes Modells?

?

**Sechs Modelle (Folien 13–14, 16):**

| Modell | Kernprinzip | Vorteil | Nachteil |
|---|---|---|---|
| **RBAC** (Role-Based) | Zugriff basierend auf **Rollen** (z. B. Arzt, Pflege) | einfaches Management | starr, Rollen-Explosion bei feiner Granularität |
| **ABAC** (Attribute-Based) | Zugriff basierend auf **Attributen** (Abteilung, Standort, Gerät) | sehr flexibel, feingranular | komplex in der Verwaltung |
| **IBAC** (Identity-Based) | Zugriff basierend direkt auf **Identität** | direkte Kontrolle | schlecht skalierbar |
| **MAC** (Mandatory) | **Zentrale Autorität** legt Regeln fest | sehr hohe Sicherheit | schwer dynamisch anpassbar |
| **DAC** (Discretionary) | **Ressourcenbesitzer** entscheidet | flexibel, nutzerfreundlich | unsichere Entscheidungen möglich |
| **CBAC** (Context-Based) | Entscheidung basierend auf **Kontext** (Zeit, Ort, Netzwerk) | Zero-Trust-tauglich, dynamisch | komplex, rechenintensiv |

---

### Anwendung

Was ist Multifaktor-Authentifizierung (MFA), und welche Faktoren kombiniert die Handy-Signatur?

?

**MFA (Folie 10):** Kombination verschiedener Authentifizierungsklassen zur Erhöhung der Sicherheit.

**Handy-Signatur (Folie 10):**
| Faktor | Klasse |
|---|---|
| Signatur-PIN | Wissen |
| Schlüsselmaterial im Smartphone / Sicherheits-Token | Besitz |
| Fingerprint zur Geräteentsperrung | Biometrie |

**Online-Banking (Push-TAN):**
| Faktor | Klasse |
|---|---|
| Benutzername + PIN | Wissen |
| Mobiltelefon mit Banking-App | Besitz |

**Trade-off:** Mehr Faktoren = mehr Sicherheit, aber weniger Benutzerfreundlichkeit. Die Vorlesung weist explizit auf diesen Konflikt hin.

**Falsche MFA:** Zwei Passwörter = kein echter zweiter Faktor (beide Klasse Wissen).

---

Welche fünf Phasen hat der IdM-Lebenszyklus, und welche Kernfragen stellt jede Phase?

?

**Fünf Phasen (Folien 19–21):** Erstellung → Verwendung ↔ Wartung → Löschung, alle unter Governance.

| Phase | Kernfragen |
|---|---|
| **Erstellung** | Wie werden Daten erhoben? Welche Anmeldedaten werden erstellt? Wo gespeichert? Verifizierung? |
| **Verwendung** | Auf welche Anwendungen darf zugegriffen werden? Wer führt Authentifizierung durch? Welches Protokoll? |
| **Wartung** | Welche Attribute können geändert werden? Was bleibt unveränderbar (z. B. IDs)? Haben Attribute eine Lebensdauer (z. B. Zertifikate)? |
| **Löschung** | Wie können Identitäten widerrufen werden? Automatische Löschung? Systeminformation? Dokumentation? |
| **Governance** | Policies für alle Phasen; Authentifizierungs- und Autorisierungsregeln; Rückverfolgbarkeit (Logging); rechtliche Basis (DSGVO) |

**eHealth-Beispiel:** ELGA-Identität: Erstellung per ID-Austria-Registrierung; Verwendung beim Aktenzugriff; Wartung bei Namensänderung; Löschung bei Tod/Opt-out; Governance durch ELGA-Verordnung + DSGVO.

---

Skizziere den SAML2-Flow am ELGA-Beispiel. Welche Akteure sind beteiligt und was wird übertragen?

?

**SAML2 (Folie 29/30):** XML-basiertes Identitätsprotokoll. Transportiert Authentifizierungsergebnisse und Benutzerattribute als signierte XML-SAML-Assertions.

**Flow:**
1. Benutzer → Service Request → ELGA (SP)
2. ELGA → Authentication Redirect → Benutzer → A-Trust (IdP)
3. IdP ↔ Benutzer: Authentifizierung (z. B. Handy-Signatur)
4. IdP → Authentication Response mit **SAML-Assertion** → Benutzer → ELGA
5. ELGA validiert SAML-Assertion → gewährt Zugriff

**Was übertragen wird:** SAML-Assertion (XML-Dokument mit Identitätsdaten, signiert durch IdP)

**Typischer Einsatz:** Ältere Webanwendungen, interne Unternehmensdienste, eHealth-Enterprise-Setups.

---

Skizziere den OIDC-Flow am ELGA-Beispiel. Was ist der entscheidende Sicherheitsunterschied zu SAML2?

?

**OIDC (Folie 32/33):** Modernes Identitätsprotokoll auf Basis von OAuth2. Nutzt **JSON Web Tokens (JWT)** als ID-Token.

**Flow:**
1. Benutzer → Service Request → ELGA (SP)
2. ELGA → Authentication Redirect → Benutzer → IdP
3. IdP ↔ Benutzer: Authentifizierung
4. IdP → **Authorization Code** → Benutzer → ELGA-Backend
5. ELGA-Backend → **Token Request** (Code + Client Secret) → IdP
6. IdP → **ID-Token** (JWT mit Identitätsdaten) → ELGA-Backend
7. ELGA prüft Rechte → Zugriff gewährt

**Entscheidender Sicherheitsunterschied zu SAML2:**
- Bei SAML2 durchläuft die SAML-Assertion den Browser des Nutzers.
- Bei OIDC geht nur ein kurzlebiger **Authorization Code** durch den Browser. Das eigentliche **ID-Token** wird Server-zu-Server zwischen ELGA-Backend und IdP ausgetauscht → geringeres Risiko für Token-Diebstahl im Browser.

---

### Diskussion

Warum ist Authentifizierung nicht dasselbe wie Autorisierung, und warum müssen beide separat berücksichtigt werden?

?

**Authentifizierung** klärt: „*Wer* ist die Person?" → Prüfung der Identität.
**Autorisierung** klärt: „*Was darf* die Person?" → Vergabe von Zugriffsrechten an die authentifizierte Identität. (Folie 11: „Through authorization, rights are assigned to a digital identity." [GINI-SA])

**Warum Trennung wichtig ist:**

| Szenario | Problem ohne Trennung |
|---|---|
| Reinigungskraft ist authentifiziert | Ohne Autorisierung hätte sie Zugriff auf alle Patientenakten |
| Arzt aus externer Klinik | Authentifizierung möglich per eID; Autorisierungsregeln müssen extern definiert sein |
| API-Zugriff | OAuth2 trennt explizit Autorisierung (Access Token) von Authentifizierung (ID-Token per OIDC) |

**Technisch:** Autorisierung setzt stets eine erfolgreiche Authentifizierung voraus, ist aber eine eigene Entscheidungsschicht (Subject + Resource + Action → Decision nach Berechtigungsmodell).

---

Welche vier IdM-Modelle gibt es, und welche Schwachstelle hat jeweils das isolierte und das föderierte Modell?

?

**Vier Modelle (Folien 24–27):**

| Modell | IdP-SP-Verhältnis | Identitätsdaten | Schwäche |
|---|---|---|---|
| **Zentral** | identisch (SP = IdP) | beim SP | hohe Eigentverantwortung; Implementierungsfehler |
| **Isoliert** | getrennt, 1 IdP | beim IdP | **Ausfall des IdP** → alle Services des SP nicht nutzbar |
| **Benutzer-zentriert** | getrennt, Daten beim User | beim Benutzer | **Datenverlust/-weitergabe** durch den Benutzer möglich |
| **Föderiert** | mehrere IdPs vertrauen einander | verteilt | hohe Kosten für Betrieb + Synchronisation; **Vertrauensbasis** zwischen IdPs nötig |

**eHealth-Beispiele:**
- Isoliert: ELGA (SP) + A-Trust (IdP)
- Benutzer-zentriert: ID Austria (Daten auf Smartphone)
- Föderiert: eIDAS – dt. Bürger nutzt dt. IdP für österreichischen SP

**Single Sign-On** ist typisch für isoliertes oder föderiertes Modell.

---

Welches Berechtigungsmodell eignet sich für eHealth, und warum reicht RBAC allein oft nicht aus?

?

**RBAC Stärke (eHealth):** Klar definierte Rollen (Arzt, Pflege, Patient, Verwaltung) → einfaches Management, klare Hierarchien.

**RBAC-Schwäche in eHealth:**
- **Rollen-Explosion:** Feingranulare Anforderungen (z. B. „Arzt nur eigene Station", „Belegarzt nur eigene Patienten") erfordern sehr viele Rollen.
- **Kontextblind:** RBAC berücksichtigt nicht, ob es gerade Nacht ist, ob ein Notfall vorliegt, von welchem Gerät zugegriffen wird.

**Typische Kombination in der Praxis (Übungsaufgabe Folie 15/16):**
- **RBAC** als Grundstruktur (Rollen: Arzt/Pflege/Patient)
- **ABAC** für Feingranularität (Stationsbindung, Fachabteilung)
- **MAC** für zentral vorgeschriebene Regeln (ELGA-Gesetze, DSGVO-Sperren)
- **CBAC** für Kontext-Zugriff (Notfall außerhalb regulärer Zeiten)

---

### Vergleich

Vergleiche SAML2 und OIDC hinsichtlich Format, Einsatzgebiet und Sicherheitsmodell.

?

| Aspekt | SAML2 | OpenID Connect (OIDC) |
|---|---|---|
| Format | **XML** (schwergewichtig) | **JSON / JWT** (leichtgewichtig) |
| Einsatzgebiet | Ältere Webanwendungen, Enterprise, interne Dienste | Web- und Mobile-Apps, moderne Cloud-Dienste |
| Übertragener Token | SAML-Assertion (XML, durch Browser) | ID-Token (JWT, Server-zu-Server) |
| Sicherheitsmodell | Assertion geht durch Browser | Authorization Code durch Browser, ID-Token nur Server-zu-Server |
| Basis | OASIS-Standard (2005) | Aufbau auf OAuth 2.0 (RFC 6749) |
| ELGA-Beispiel | Folie 30: SP leitet zu IdP um, IdP schickt Assertion zurück | Folie 33: IdP schickt Code, Backend tauscht gegen ID-Token |
| Stärke | Enterprise-Integration, standardisierte Federation | Flexibel, schneller implementierbar |

---

Vergleiche RBAC, ABAC und CBAC hinsichtlich Entscheidungsgrundlage, Flexibilität und Einsatz.

?

| Aspekt | RBAC | ABAC | CBAC |
|---|---|---|---|
| Entscheidungsgrundlage | Rolle des Benutzers | Attribute (User, Resource, Umfeld) | Kontext (Zeit, Ort, Netzwerk) |
| Flexibilität | niedrig – starr an Rollen | hoch – beliebige Attribute | sehr hoch – dynamisch anpassbar |
| Verwaltungsaufwand | gering | hoch (viele Attribute konfigurieren) | sehr hoch (komplexe Infrastruktur) |
| Skalierbarkeit | gut für große Organisationen mit klaren Rollen | gut für feingranulare Anforderungen | gut für Zero-Trust-Umgebungen |
| eHealth-Beispiel | Arzt hat alle Lese-/Schreibrechte | Arzt nur auf Patienten der eigenen Station | Arzt hat erweiterten Zugriff im Notfallmodus |
| Schwäche | Rollen-Explosion | Audit-Nachvollziehbarkeit schwierig | Rechenintensiv, komplex |

---

Vergleiche die vier Authentifizierungsklassen nach Kompromittierbarkeit und Ersetzbarkeit.

?

| Klasse | Kompromittierung | Ersetzbar? | Datenschutzrisiko |
|---|---|---|---|
| **Wissen** (Passwort, PIN) | Phishing, Brute Force, Datenleck | ✅ leicht ersetzbar | gering |
| **Besitz** (Smartcard, Token) | Diebstahl, Verlust | ✅ ersetzbar (neu ausstellen) | gering |
| **Biometrie** (Fingerprint, Iris) | physische Datenbankleaks | ❌ nicht ersetzbar – einmal kompromittiert, immer | hoch – biometrische Daten = sensible Daten |
| **Verhaltensmuster** (Tippverhalten) | Nachahmung, Aufzeichnung | ⚠️ teilweise veränderbar (Lernen), aber langsam | hoch – kontinuierliches Behavioral-Profiling |

**Konsequenz für eHealth:**
- Biometrie bietet hohe Sicherheit, ist aber bei Kompromittierung irreversibel → besonders schützenswerter Faktor.
- MFA-Kombination sollte mindestens einen ersetzbaren Faktor enthalten.
- Reine Wissens-Faktoren (nur Passwort) sind für sicherheitskritische eHealth-Anwendungen unzureichend.

---

## Mögliche Anschlussfragen

- Was ist Single Sign-On, und in welchem IdM-Modell ist es typisch?
- Welche DSGVO-Pflichten greifen in welchen Lebenszyklusphasen?
- Was enthält eine SAML-Assertion konkret? Und ein JWT ID-Token?
- Warum sind zwei Passwörter kein echter zweiter Faktor?
- Welches Berechtigungsmodell adressiert die DSGVO-Anforderungen am besten, und warum?
- Was passiert bei Ausfall des IdP im isolierten vs. federierten Modell?
- Was ist der Unterschied zwischen Access Token (OAuth2) und ID-Token (OIDC)?

## Eigene Notizen

<!-- Platz für persönliche Ergänzungen, Eselsbrücken, etc. -->
