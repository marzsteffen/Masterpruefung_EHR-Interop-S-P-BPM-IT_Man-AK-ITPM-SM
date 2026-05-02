---
fach: asp
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/asp
---

# ASP - PF - Authentifizierung und Autorisierung

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Themenbereich Authentifizierung & Autorisierung aus ASP. Umfasst die Schutzziele Authenticity, Non-repudiation und Accountability, die Grundbegriffe digitaler Identität und des Authentifizierungsprozesses, Zertifikate und PKI, das IdM-System (Lebenszyklus, Akteure, Modelle, Berechtigungsmodelle) sowie die Identitätsprotokolle SAML2 und OpenID Connect inkl. JWT ID-Token. Quellen: VL Einführung und Motivation, VL Hash MAC Digitale Signaturen Zertifikate, VL Identitätsmanagement.

## Verlinkte Konzepte

- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Security Eigenschaften - Non-repudiation]]
- [[ASP - Security Eigenschaften - Accountability]]
- [[ASP - Identitaetsmanagement - Digitale Identitaet]]
- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Identitaetsmanagement - Authentifizierungsklassen]]
- [[ASP - Identitaetsmanagement - Multifaktor-Authentifizierung]]
- [[ASP - Identitaetsmanagement - Autorisierung]]
- [[ASP - Berechtigungsmodelle - Uebersicht]]
- [[ASP - Identitaetsmanagement - Definition]]
- [[ASP - Identitaetsmanagement - Lebenszyklus]]
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Modelle]]
- [[ASP - Authentifizierung - Level of Assurance]]
- [[ASP - Zertifikate - X.509]]
- [[ASP - Zertifikate - CSR]]
- [[ASP - Zertifikate - PKI]]
- [[ASP - Zertifikate - Signaturverifikation]]
- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsprotokoll - SAML Assertion]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Identitaetsprotokoll - JWT ID-Token]]

---

## Karten

### Definition

Frage: Was ist eine digitale Identität, und aus welchen drei Teilstücken besteht sie laut Vorlesung?

?

Antwort: Eine digitale Identität ist das digitale Abbild einer Person oder eines Objekts in der digitalen Welt; sie ermöglicht Identifikation und Authentifizierung. Die drei Teilstücke (Folie 5) sind:
1. **Eindeutige ID** – technische Grundlage für die Zuweisung zur Entität (z. B. UUID, Benutzer-ID).
2. **Identitätsdaten (Attribute)** – beschreibende Eigenschaften (z. B. Name, Geburtsdatum).
3. **Authentifizierungs- und Identifikationsdaten** – Mittel zur Anmeldung (z. B. Passwort, digitales Zertifikat).

---

Frage: Wie unterscheidet die Vorlesung Identifizierung, Authentisierung und Authentifizierung? Wer führt jeweils welche Aktion durch?

?

Antwort: Die Vorlesung (Folie 8) trennt drei Begriffe:
- **Identifizierung** – das Subjekt *behauptet* eine Identität (Assoziation von Attributen mit einem Individuum).
- **Authentisierung** – das Subjekt *übergibt* einen Identitätsnachweis (z. B. Reisepass, Passwort-Eingabe).
- **Authentifizierung** – der Prüfende *verifiziert* den Nachweis auf Gültigkeit.

Merkhilfe: Beim Reisepass-Beispiel → „Ich bin Max Mustermann" = Identifizierung; Reisepass herausreichen = Authentisierung; Beamte prüft den Pass = Authentifizierung.

---

Frage: Welche vier Klassen von Authentifizierungs-Faktoren nennt die Vorlesung, und je ein Beispiel?

?

Antwort: Laut Folie 9:
1. **Wissen** („etwas wissen") – Passwort, PIN
2. **Besitz** („etwas besitzen") – Smartcard, Bankomatkarte
3. **Biometrische Eigenschaft** („etwas sein") – Fingerprint, Gesichtserkennung
4. **Verhaltensmuster** („etwas tun") – Tippverhalten, Verweildauer in Apps

---

Frage: Aus welchen sechs Bestandteilen besteht eine PKI laut Vorlesung?

?

Antwort: Laut Folie 18:
1. **Digitale Zertifikate** – ausgestellte Bindungen zwischen Public Key und Identität
2. **CA (Certification Authority)** – stellt Zertifikate aus und signiert sie
3. **RA (Registration Authority)** – nimmt Antragsteller entgegen, prüft die Identität
4. **CRL (Certificate Revocation List)** – Liste widerrufener Zertifikate
5. **Verzeichnisdienst** – stellt ausgestellte Zertifikate öffentlich zum Abruf bereit
6. **VA (Validation Authority)** – beantwortet Online-Statusanfragen (z. B. per OCSP)

---

### Anwendung

Frage: Skizzieren Sie den CSR-Ablauf bei der Zertifikatsausstellung: Welcher Schlüssel wird übertragen, welcher nicht – und warum?

?

Antwort: Laut Folie 17 (CSR-Ablauf):
1. Antragsteller erzeugt ein Schlüsselpaar (Public + Private Key).
2. Antragsteller erstellt einen CSR mit dem Public Key und eigenen Identitätsdaten.
3. Antragsteller signiert den CSR mit dem eigenen **Private Key** (Proof of Possession).
4. CSR (= Public Key + Daten + Signatur) wird an den Vertrauensdiensteanbieter gesendet.
5. CA prüft Identität, erstellt das Zertifikat, signiert es mit dem CA-Private-Key und schickt es zurück.

→ **Der Private Key verlässt nie den Antragsteller.** Nur der Public Key wird übertragen. Die Signatur des CSR beweist der CA, dass der Antragsteller tatsächlich Besitzer des zugehörigen Private Keys ist.

---

Frage: Aus welchen zwei Pflichtschritten besteht die vollständige Signaturverifikation, und was passiert, wenn nur einer erfüllt ist?

?

Antwort: Laut Folie 19 müssen beide Schritte erfüllt sein:

**1. Kryptografische Verifikation:**
- Empfänger berechnet Hash der Nachricht neu.
- Signatur wird mit dem Public Key des Senders entschlüsselt.
- Beide Hash-Werte werden verglichen.

**2. Zertifikatsvalidierung:**
- Gültigkeitszeitraum (NotBefore / NotOnOrAfter)
- Schlüsselverwendung (z. B. „Digitale Signatur" erlaubt?)
- Revozierungsstatus (CRL oder OCSP)
- Vertrauenswürdigkeit der CA (Wurzel-Zertifikat bekannt?)
- Personenbindung (eindeutiger Identifier vorhanden?)

Wenn nur Schritt 1 erfüllt: Signatur ist kryptografisch gültig, aber es fehlt der Nachweis, dass das Zertifikat noch gilt → nicht akzeptabel. Wenn nur Schritt 2 erfüllt: Zertifikat ist gültig, aber Nachricht könnte manipuliert sein → nicht akzeptabel.

---

Frage: Skizzieren Sie den SAML2-Flow am ELGA-Beispiel. Welche Akteure sind beteiligt, und in welcher Reihenfolge werden Nachrichten ausgetauscht?

?

Antwort: Laut Folien 29–30:

Akteure: Benutzer (Patient) · ELGA (Service Provider) · A-Trust/IdP (Identity Provider)

Ablauf:
1. Benutzer sendet Service Request an ELGA.
2. ELGA sendet Authentication Redirect → leitet Benutzer zum IdP.
3. IdP führt Authentifizierung mit dem Benutzer durch.
4. IdP sendet Authentication Response mit **SAML-Assertion** zurück (über den Benutzer-Browser an ELGA).
5. ELGA validiert die SAML2-Assertion → gewährt Zugriff.

Die SAML-Assertion ist ein signiertes XML-Dokument mit Issuer, Subject, Gültigkeitszeitraum und Authentifizierungsmethode.

---

Frage: Was sind Level of Assurance (LoA), welche drei Stufen gibt es laut Vorlesung, und wie hängt LoA mit der Schlüsselspeicherung zusammen?

?

Antwort: Laut Folie 32 (VL Hash/MAC/Zertifikate):

LoA klassifiziert die Vertrauenswürdigkeit einer elektronischen Identifizierung gemäß der **eIDAS-Verordnung** in drei Stufen: **Low**, **Medium**, **High**.

Kernaussage der Vorlesung: Die **Schlüssel-Speicherung beeinflusst direkt die Qualität der Authentifizierung** – wer Schlüssel in einer Hardware-Sicherheits-Umgebung erzeugt und verwendet, kann ein höheres LoA erreichen.

*(Detailkriterien je Stufe sind im PDF nicht spezifiziert. [Ergänzung]: LoA „High" setzt eine zertifizierte Hardware-Einheit voraus; qualifizierte elektronische Signaturen nach eIDAS erfordern LoA „High".)*

---

### Diskussion

Frage: Wie grenzt die Vorlesung Authenticity, Non-repudiation und Accountability voneinander ab? Welche Abhängigkeit besteht zwischen den drei Schutzzielen?

?

Antwort: Laut Folien 13–14 (VL Einführung):

- **Authenticity** – Echtheit und Vertrauenswürdigkeit einer Partei: „Ist diese Person wirklich die, die sie vorgibt zu sein?"
- **Non-repudiation** – Nicht-Abstreitbarkeit: „Die Person kann eine durchgeführte Handlung nicht glaubwürdig leugnen." (Beweisbarkeit auch gegenüber Dritten.)
- **Accountability** – Zurechenbarkeit: „Jede Handlung ist einem Akteur eindeutig zuordnbar." (Primär intern/organisatorisch.)

**Abhängigkeit:** Authenticity ist Voraussetzung für beide anderen – ohne gesicherte Identität ist weder Non-repudiation noch Accountability möglich. Non-repudiation geht über Accountability hinaus: sie muss auch gegenüber Dritten (z. B. Gericht) standhalten.

*(Abgrenzung Non-repudiation vs. Accountability „intern vs. extern" ist im PDF nicht explizit gezogen.)*

---

Frage: Warum reicht eine HMAC nicht aus, um Non-repudiation zu garantieren? Was wäre nötig?

?

Antwort: Laut Note zu Non-repudiation (VL Einführung, Folie 14):

Ein **HMAC** nutzt einen **geteilten symmetrischen Schlüssel** – beide Parteien (Sender und Empfänger) kennen ihn. Damit kann der Empfänger die Nachricht theoretisch selbst erzeugt haben. Ein Dritter kann nicht unterscheiden, wer das HMAC erstellt hat → **keine Non-repudiation**.

Für Non-repudiation wird ein **asymmetrisches Verfahren** benötigt: Nur der Inhaber des Private Keys kann signieren; der Empfänger und jeder Dritte können mit dem öffentlichen Schlüssel verifizieren, aber nicht selbst signieren. *(Konkrete kryptografische Details sind im PDF der Einführungsvorlesung nicht ausgeführt; detailliert in VL Hash/MAC/Signaturen.)*

---

Frage: Der IdM-Lebenszyklus hat fünf Phasen. Welche Phase ist laut Vorlesung besonders kritisch im Hinblick auf DSGVO-Konformität – und warum?

?

Antwort: Laut Folien 19–21 (VL Identitätsmanagement) sind die fünf Phasen: Erstellung, Verwendung, Wartung, Löschung, Governance.

**DSGVO-Bezug** (aus Prüfungsrelevanz-Sektion der Note):
- **Löschung** ist in der Praxis am häufigsten unzureichend umgesetzt – „untote Konten" widersprechen dem Grundsatz der Speicherbegrenzung (Art. 5 DSGVO).
- **Erstellung** → Datenminimierung (nur notwendige Attribute erheben).
- **Verwendung** → Zweckbindung.
- **Governance** basiert laut Vorlesung oft auf rechtlichen Vorgaben (inkl. DSGVO).

*(Konkrete DSGVO-Artikelnummern sind im Vault-Inhalt der Vorlesungs-Note nicht spezifiziert.)*

---

### Vergleich

Frage: Vergleichen Sie SAML2 und OpenID Connect: Welche technischen Unterschiede gibt es, und wann wird welches Protokoll bevorzugt?

?

Antwort: Laut Folien 29–33 (VL Identitätsmanagement):

| Kriterium | SAML2 | OpenID Connect (OIDC) |
|---|---|---|
| Format | XML (schwergewichtig) | JSON Web Token (leichtgewichtig) |
| Token-Transport | Assertion geht über Browser | ID-Token wird Server-zu-Server ausgetauscht (nur Authorization Code über Browser) |
| Zielplattform | ältere Web-Apps, Enterprise-Dienste | Web- und mobile Anwendungen |
| Flexibilität | weniger flexibel | moderner, flexibler |

**Sicherheitsvorteil OIDC:** Das eigentliche ID-Token verlässt nie den Browser – nur ein kurzlebiger Authorization Code geht über den User Agent. Das reduziert das Risiko eines Token-Diebstahls im Browser.

**SAML2** wird bevorzugt für Legacy-Systeme und interne Unternehmensinfrastrukturen (z. B. ELGA mit A-Trust).

---

Frage: Vergleichen Sie RBAC und ABAC als Berechtigungsmodelle. Welches Modell eignet sich besser für ein Krankenhaus, und warum?

?

Antwort: Laut Folien 13–16 (VL Identitätsmanagement):

**RBAC (Role Based Access Control):**
- Zugriff basiert auf zugewiesenen **Rollen** (z. B. „Arzt", „Pflege", „Patient").
- Vorteil: Einfaches Management, klare Hierarchien.
- Nachteil: Starr – bei feingranularen Anforderungen entsteht eine Rollen-Explosion.

**ABAC (Attribute Based Access Control):**
- Zugriff basiert auf **Attributen** von Nutzer, Ressource und Umfeld (z. B. Abteilung, Standort, Gerät).
- Vorteil: Sehr flexibel, dynamisch, feingranular.
- Nachteil: Komplex in der Verwaltung.

**Krankenhaus:** In der Praxis eine **Kombination** sinnvoll – RBAC für Basisrollen (Arzt/Pflege/Patient), ABAC-Zusätze für Stationsbindung oder „nur eigene Station", MAC für zentrale gesetzliche Vorgaben (z. B. ELGA-Patientenverfügungs-Sperren).

---

Frage: Welche vier IdM-Modelle nennt die Vorlesung? Welches Modell stärkt die Datenhoheit der Benutzer am meisten, welches die Ausfallsicherheit?

?

Antwort: Laut Folien 24–27 (VL Identitätsmanagement):

1. **Zentrales Modell** – SP = IdP, Identitätsdaten beim SP. Vorteil: unabhängig. Nachteil: Implementierungsaufwand.
2. **Isoliertes Modell** – SP und IdP getrennt, Daten beim IdP. Vorteil: Spezialist für Auth. Nachteil: Ausfall des IdP sperrt alle Dienste.
3. **Benutzer-zentriertes Modell** – Identitätsdaten beim Benutzer (z. B. Smartcard). Vorteil: **Datenhoheit beim Nutzer**. Nachteil: Benutzer kann Daten verlieren/weitergeben.
4. **Föderiertes Modell** – mehrere IdPs mit Vertrauensbasis. Vorteil: **Hohe Ausfallsicherheit**, Identitätsdaten nicht einfach löschbar. Nachteil: Hohe Betriebs- und Synchronisationskosten.

---

## Mögliche Anschlussfragen des Prüfers

- Welcher Krypto-Baustein liefert Authentizität, welcher zusätzlich Non-repudiation – und warum ist das so?
- Wie hängt der Level of Assurance mit der konkreten Hardware-Schlüsselspeicherung zusammen?
- Welche PKI-Bestandteile kommen bei der Ausstellung und beim Widerruf eines Arztsignatur-Zertifikats zum Einsatz?
- Warum signiert der Antragsteller den CSR mit seinem eigenen Private Key?
- Was ist der Unterschied zwischen dem OIDC Authorization Code und dem ID-Token – und warum läuft der Token-Tausch Server-zu-Server?
- Welche Felder einer SAML-Assertion oder eines JWT ID-Tokens sind prüfungsrelevant?
- Sind zwei Passwörter eine echte 2-Faktor-Authentifizierung? Begründung?
- In welcher IdM-Lebenszyklusphase entstehen typischerweise DSGVO-Verstöße in der Praxis?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
