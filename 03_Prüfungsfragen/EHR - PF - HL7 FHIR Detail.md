---
fach: ehr
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/ehr
---

# EHR - PF - HL7 FHIR Detail

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

> [!warning] Honeypot-Hinweis
> FHIR ist ein bekanntes Halluzinations-Risikofeld. Alle Karten in dieser Note sind strikt aus den Konzept-Notes der FHIR-Grundlagen-Vorlesung abgeleitet. Keine Codes, HTTP-Statuscodes oder Resource-Details ohne direkte Quellstütze. Bei spezifischen technischen Fragen am Prüfungstag: Lieber „im Detail nicht sicher" sagen als falsche Spezifika nennen.

## Kontext

Dieser Kartensatz deckt HL7 FHIR in der Tiefe ab: Motivation, Resource-Konzept, Resource-Kategorien, Data Types & Cardinality, Extensions & 80/20-Regel, Profile & Must Support, Implementation Guides, References, REST/CRUD, Search, Bundles (Document, Message, Transaction), 6 Exchange Paradigmen, Resource Granularität sowie die praktische Erstellung von Patient- und Observation-Resources. Inhaltsbasis ist ausschließlich die FHIR-Grundlagen-Vorlesung.

## Verlinkte Konzepte

- [[EHR - FHIR - Motivation]]
- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Resource Kategorien]]
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - Data Types und Cardinality]]
- [[EHR - FHIR - Extensions und 80 20 Regel]]
- [[EHR - FHIR - Profiles und Must Support]]
- [[EHR - FHIR - Implementation Guides]]
- [[EHR - FHIR - References]]
- [[EHR - FHIR - Search]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - 6 Exchange Paradigms]]
- [[EHR - FHIR - Resource Granularität]]
- [[EHR - FHIR - Transaction Bundle]]
- [[EHR - FHIR - Patient Resource erstellen]]
- [[EHR - FHIR - Observation Resource erstellen]]
- [[EHR - HL7 FHIR - 5 Levels]]

---

## Karten

### Definition

Warum wurde FHIR entwickelt – welche Probleme der Vorgänger-Standards adressiert es, und welche Markt-Kennzahl belegt seine Verbreitung?

?

FHIR (Fast Healthcare Interoperability Resources) entstand aus den Schwächen der HL7-Vorgänger: **CDA** hat eine sehr steile Lernkurve und ist nicht „developer friendly"; **HL7 v3 Messaging** wird kaum genutzt – Provider bleiben bei v2; **HL7 v2** ist weit verbreitet aber alt; alle HL7-Standards bieten keine Unterstützung für **verteilte Information** (z. B. Blutdruckmessungen in Graz und Innsbruck). FHIR-Antwort: „From implementers for implementers" – Spezifikation für Implementierer geschrieben; bekannte Web-Technologien (XML, JSON, RDF, RESTful); frei verfügbar; Reference Implementations + Test-Server + Starter-APIs sofort verfügbar. **Markt-Kennzahl**: 75 % der Digital-Health-Unternehmen nutzen FHIR (Studie N = 141). FHIR ersetzt nicht sofort v2 oder CDA – Co-Existenz ist Alltag. FHIR ist kein EHR-System, sondern ein Exchange-Format/-API.

Was ist eine FHIR-Resource, welche 5 Hauptkategorien gibt es, und welche Beispiele gehören jeweils dazu?

?

Eine **Resource** ist die kleinste atomare Einheit des FHIR-Datenmodells – „Atoms of health information exchange." Jede Resource beschreibt ein „Thing" (Patient, Observation, MedicationRequest). Sie hat immer ein **`resourceType`**-Feld als Pflicht. FHIR hält die Resource-Anzahl bewusst begrenzt (~150) – Variation läuft über Attribute und Coding. **5 Hauptkategorien**: (1) **Foundation** – Infrastruktur (ValueSet, Composition, MessageHeader, CapabilityStatement); (2) **Base** – Stammdaten (Patient, Practitioner, Organization, Encounter, Location, Device); (3) **Clinical** – Versorgungsinhalte (Condition, Observation, MedicationRequest, AllergyIntolerance, Procedure, CarePlan, Specimen); (4) **Financial** – Abrechnung (Claim, Contract, Coverage); (5) **Specialized** – spezielle Domänen (ResearchStudy, ResearchSubject). Entsprechung zu HL7 FHIR 5 Levels: Base ≈ Level 3 Master Data; Clinical ≈ Level 4 Operational Data.

Was sind FHIR Data Types – welche Kategorien gibt es, und wie funktioniert Cardinality-Notation?

?

**Data Types** sind Bausteine innerhalb von Resources – sie haben keine eigenständige REST-API. Zwei Kategorien: **Primitive** (atomar): boolean, string, integer, decimal, date, dateTime, uri, code, id. **Komplex** (innere Struktur): Identifier (System + Value), HumanName (family, given), Address, ContactPoint, Period (Start/End), **CodeableConcept** (mit Coding = System+Code+Display; plus Text für Freitext), Quantity (Wert + Einheit, oft UCUM), Reference (Verweis auf andere Resource). CodeableConcept ist besonders wichtig: es erlaubt sowohl maschinenlesbaren Code als auch menschenlesbaren Text. **Cardinality-Notation** `min..max` (max `*` = beliebig oft): `0..1` optional, höchstens einmal; `1..1` Pflicht, genau einmal; `0..*` optional, wiederholbar; `1..*` mindestens einmal, wiederholbar; `0..0` verboten (nur in Profilen). Profile können Cardinality nur **verschärfen**, nie lockern.

Welche 6 Exchange-Paradigmen definiert FHIR – und welcher Use-Case passt zu welchem Paradigma?

?

FHIR definiert 6 Austausch-Paradigmen (Quelle: build.fhir.org/exchange-module.html): (1) **REST** – CRUD auf einzelne Resources über HTTP; für atomare Abfragen und Updates. (2) **Documents** – statische, immutable, signierbare Resource-Sammlungen (Bundle mit Composition); für Entlassungsbriefe. (3) **Messaging** – event-driven Kommunikation (Bundle mit MessageHeader); für Lab-Orders, Insurance-Transaktionen. (4) **Services** – komplexe Operationen die nicht in CRUD passen (CDS-Hooks, Workflow-Management, `$evaluate`); für Drug-Interaction-Checks. (5) **Database/Persistence** – native Speicherung von FHIR-Resources; für FHIR-native Datenbanken (HAPI mit JPA). (6) **Subscription** – Real-Time Notifications bei Resource-Events; für Vital-Sign-Monitoring, Befund-Push. Paradigmen sind nicht exklusiv – ein FHIR-Server unterstützt typischerweise mehrere. REST + Subscription ergänzen sich (Pull + Push).

---

### Anwendung

Wie funktioniert FHIR REST/CRUD – welche HTTP-Verben entsprechen welchen Operationen, und welche Besonderheiten gibt es?

?

FHIR REST ist **stateless** (jede Request unabhängig). **CRUD-Mapping**: POST → Create (Server vergibt ID, Antwort 201 Created + Location-Header); GET `[base]/Patient/12345` → Read; PUT `[base]/Patient/12345` → Update (Vollersatz); DELETE → Löschen; PATCH → Teilaktualisierung. Zusätzlich: GET `[base]/Patient/12345/_history` → Versionsverlauf; GET `[base]/Patient/12345/_history/2` → exakte Version. **Capability Statement**: `GET [base]/metadata` → Server-Fähigkeiten (welche Resources, welche Operationen). **Formate**: JSON, XML, RDF (per `_format`-Parameter oder `Accept`-Header). **HAPI Test Server**: `http://hapi.fhir.org/baseR4`. Beim Create via POST vergibt immer der Server die ID – nicht der Client. Beim Update via PUT muss ID bekannt sein. Fehler-Response: 404 Not Found, 400 Bad Request etc.

Wie funktioniert FHIR-Search – welche Parameter-Arten, Modifiers und Operators gibt es?

?

Grundprinzip: `GET [base]/{ResourceName}?a=b`. Bei Erfolg wird immer ein **Bundle** (type=searchset) zurückgegeben. **Parameter-Arten**: (1) Allgemeine Parameter für alle Resources: `_id`, `_lastUpdated`, `_profile`, `_tag`, `_text`, `_content` etc. (2) Resource-spezifische Parameter (z. B. für Patient: `name`, `family`, `given`, `gender`, `birthdate`, `identifier`, `address`). **Verhalten nach Datentyp**: String-Suche ist „part of" + case-insensitive. **Modifiers** (`parameter:modifier`): `:exact` (exakter Match), `:contains` (Substring), `:missing` (Feld nicht gesetzt). **Operators** (Wert-Präfix): `gt` (greater than), `le` (less or equal), `lt`, `ge`, `eq`, `ne`, `sa` (starts after), `eb` (ends before), `ap` (approximately). **Chaining** über References: `AllergyIntolerance?patient.name=Andrew` – springt von AllergyIntolerance über die Patient-Reference zu dessen Namen. Beispiele: `Patient?given=Sally`, `Patient?birthdate=lt1950-01-01`, `Observation?value-quantity=gt100`.

Welche Bundle-Typen gibt es – und woran unterscheidet man Document von Message von Transaction?

?

**Bundle** ist eine FHIR-Resource, die mehrere Resources zusammenfasst. Bundle-Typ wird durch `Bundle.type` und die erste Entry-Resource bestimmt: **document** – erste Resource ist **Composition**; statisch, immutable, digital signierbar; für Entlassungsbriefe, Discharge Summaries. **message** – erste Resource ist **MessageHeader**; event-driven, request/response-fähig, asynchron möglich. **transaction** – keine spezifische erste Resource; enthält pro Entry `request.method` + `request.url`; **All-or-Nothing**: alle oder keine Operationen werden ausgeführt; Rollback bei Fehler. **batch** – wie transaction, aber Fehler bei einem Entry lässt andere bestehen. **searchset** – Rückgabe einer Search-Operation. **Schlüsselinformationen zu Document**: Composition liefert Context (Title, Date, Author, Sections), alle referenzierten Resources IM Bundle enthalten, immutable nach Erstellung. **Transformation Document↔Message**: nur die erste Resource tauschen (Composition ↔ MessageHeader) + Bundle.type ändern.

Wie unterscheiden sich Profile und Extensions in FHIR – und was ist der Unterschied zwischen Must Support und Mandatory?

?

**Profile** schränken/erweitern eine Base-Resource für einen konkreten Use-Case ein. Technisch ist ein Profil eine `StructureDefinition`-Resource. Profile dürfen Cardinality nur **verschärfen**, nie lockern. Aktionen: Cardinality verschärfen (Identifier 0..* → 1..*), Pflichtfelder hinzufügen, Coding via ValueSet einschränken, Extensions definieren, Must-Support markieren. Beispiel US Core Patient: Race + Ethnicity-Extensions, Identifier mind. 1. **Extensions** fügen neue Felder hinzu, ohne die Core-Definition zu ändern. Sie haben eine canonical URL, können beliebige Data Types enthalten, können einfach oder komplex (Sub-Extensions) sein. **Modifier Extension**: verändert die Bedeutung der Resource – Empfänger muss sie verstehen oder Resource ablehnen. **Must Support vs Mandatory**: Mandatory = Cardinality ≥ 1 (Feld muss vorhanden sein); Must Support = System muss Feld lesen/schreiben können, aber Daten können fehlen (markiert durch rotes „S"-Quadrat in IG). Beispiel: Ethnicity in US Core ist Must Support – Patient kann ablehnen, System muss es aber unterstützen.

Welche Pflichtfelder hat eine Observation-Resource – wie wird Blutdruck mit zwei Werten modelliert, und wie korrigiert man eine fehlerhafte Observation?

?

**Pflichtfelder** (Cardinality 1..1 in Base-Resource): `resourceType` = `"Observation"`, `status` (registered/preliminary/final/amended/corrected/cancelled/entered-in-error), `code` (CodeableConcept, was wird beobachtet – typisch LOINC). In der Praxis fast immer: `subject` (Reference auf Patient), `effectiveDateTime` (wann gemessen), `value[x]` (Quantity, CodeableConcept, string etc.), `category` (vital-signs, laboratory, social-history etc.). **Blutdruck mit zwei Werten**: da systolischer und diastolischer Wert zusammengehören, nutzt man ein **`component`**-Array innerhalb einer Observation. Code des Panel: LOINC 85354-9 (Blood pressure panel); systolisch: LOINC 8480-6; diastolisch: LOINC 8462-4. Einheit: UCUM `mm[Hg]`. **Fehlerkorrektur**: Status auf `corrected` setzen + PUT gegen die bekannte ID → neue Version in `_history`. **Nicht DELETE verwenden** – `entered-in-error` setzen, damit Audit Trail erhalten bleibt. Unterschied: `effectiveDateTime` = wann gemessen, `issued` = wann ins System eingegeben.

---

### Diskussion

Die 80/20-Regel und das Race-Beispiel: Was macht ein Konzept zum Extension-Kandidaten – und welche ethischen Implikationen hat das?

?

**80/20-Regel**: FHIR beschreibt 80 % der globalen Versorgungsrealität in Base-Resources. Die übrigen 20 % – kulturell variante, regional spezifische, hochspezialisierte Konzepte – werden über Extensions abgebildet. FHIR zitiert explizit: „Do not try to describe concepts that are cultural dependent – Race, Religion, …" **Race-Beispiel** (US Census Bureau): White, Black or African American, American Indian and Alaska Native, Asian, Native Hawaiian etc. – in den USA selbst Bestandteil des US Core IG (Pflicht-Extension), in Deutschland gesetzlich nicht erfassbar. **Ethische Implikationen**: Die Entscheidung, was „80 %" und was „20 %" ist, ist keine neutrale technische Entscheidung – sie spiegelt die dominanten Implementierungskulturen wider (US/EU). Konzepte aus dem Globalen Süden (z. B. traditionelle Medizin, lokale Krankheitskonzepte) landen systemisch in den 20 % und müssen als Extensions eingebaut werden. Das begünstigt Interoperabilitätslücken für ressourcenschwache Länder. FHIR-Mechanismus: Extensions sind global adressierbar (canonical URL), können aber lokal bleiben.

References in FHIR vs. CDA: Welches grundlegende Designproblem löst FHIR mit seinem Reference-Mechanismus?

?

In **CDA** gibt es wenig Support für das Referenzieren von Objekten – derselbe Arzt kann in einem CDA-Dokument mehrfach vollständig beschrieben sein, wenn er mehrere Rollen hat (Autor, Unterzeichner, behandelnder Arzt). Das erzeugt Redundanz, Inkonsistenz und Pflegeaufwand. In **FHIR** gilt: „A 'thing' (Resource) is defined/described once and can be referenced many times." Mechanismus: References sind immer URLs – relativ (`Patient/034AB16`), absolut (`https://server.com/Patient/12345`), versionsspezifisch (`Patient/example/_history/2`) oder contained (eingebettet mit Hash-Reference). Ein Practitioner wird einmal als Resource angelegt; alle Encounter, Observations, MedicationRequests referenzieren ihn per URL. **Kritische Dimension**: Ohne Versionsangabe verweist eine Reference auf den aktuellen Stand der Ziel-Resource – ändert sich diese nachträglich, kann die Bedeutung der referenzierenden Resource sich verändern. Versionierte References frieren den Stand ein (wichtig für Audit-Sicherheit).

FHIR Resource Granularität: Warum deckt Observation sowohl den Subjective- als auch den Objective-Block einer SOAP-Note ab – und welche Konsequenz hat das für Coding-Standards?

?

Aus der Vorlesung: „FHIR wants to keep the number of resources limited. Some resources cover a broad scope. Example: 'Observation' resource – 'S' and 'O' in SOAP … Differentiation by attributes and coding." Die **Observation-Resource** deckt ab: patientenberichtete Symptome (→ Subjective) mit `category=social-history` oder `patient-reported`; sowie objektive Messungen (→ Objective) mit `category=vital-signs` oder `laboratory`. Was die Beobachtung inhaltlich ist, steht im **`code`**-Feld (CodeableConcept, typisch LOINC oder SNOMED CT). **Konsequenz für Coding-Standards**: Coding-Standards (LOINC, SNOMED) werden zur **tragenden Säule** – ohne sie ist eine Observation bedeutungslos. Profile und ValueSets werden essenziell, um Use-Case-spezifische Subsets zu definieren. Beispiel: Body Weight → LOINC 29463-7, Einheit kg (UCUM). Observation vs. Condition: Observation = Messung/Beobachtung; Condition = Diagnose (Assessment-Block in SOAP).

Transaction vs. Batch Bundle: Wann wählt man welches, und welche Garantien bieten sie?

?

**Transaction Bundle** (`Bundle.type=transaction`): alle Entries werden **atomar** ausgeführt – all-or-nothing. Scheitert ein Entry, rollt der Server alles zurück. Vorteil: referenzielle Konsistenz (Patient + zugehörige Observation in einem Schritt anlegen, ohne dass die Observation mit einer nicht-existierenden Patient-ID im System landet). **Technischer Trick**: `fullUrl` mit `urn:uuid:` als temporäre ID – der Server löst interne Referenzen auf, sobald die echten IDs vergeben wurden. **Batch Bundle** (`Bundle.type=batch`): jedes Entry wird unabhängig ausgeführt. Fehler bei Entry 3 lässt Entries 1 und 2 bestehen. Vorteil: robuster bei teilweisem Scheitern, kein kompletter Rollback. **Wann was**: Transaction für logisch zusammenhängende Daten (Patient + erste Observation bei Aufnahme); Batch für unabhängige Updates (z. B. tägliche Bulk-Synchronisation von Lab-Werten). POST eines Transaction-Bundles geht an `[base]/` (Bundle-Root), nicht an `[base]/Bundle`.

Warum braucht man Implementation Guides (IGs), wenn es schon den FHIR-Standard gibt – und welche Elemente enthält ein IG?

?

Der FHIR-Standard ist das technische Fundament, aber er ist bewusst generisch gehalten (80/20-Regel). Er legt nicht fest, welche Resources ein österreichisches EHR welchen Coding-Standards unterstützen muss, wie Österreich-spezifische Identifier (SVNR) strukturiert werden, oder welche Exchange-Paradigmen für welchen Use-Case zu nutzen sind. Ein **Implementation Guide (IG)** kombiniert: **Profiles + Extensions + Examples + Exchange Paradigms + detaillierte Dokumentation** für einen konkreten Use-Case. Formel: „FHIR IGs = FHIR Profiles + Examples + Exchange Paradigm + LOTS of Documentation." Bekannte IGs: **US Core** (USA, für ONC-Zertifizierung), **AT Core** (Österreich, HL7-AT, ELGA-kompatibel), **NDHM/ADBM** (Indien), **Nphies** (Saudi-Arabien). Tools: FHIR Registry (fhir.org/guides/registry/), Simplifier.net (Hosting/Editing). **Kritische Einschränkung**: Zu viele oder inkompatible IGs fragmentieren Interoperabilität. Internationale IGs (z. B. IPS – International Patient Summary) müssen mit nationalen IGs kombinierbar bleiben.

Profile erlauben lokale Anpassung – aber zu viele Profile fragmentieren Interoperabilität. Wie ist dieser Trade-off zu bewerten?

?

**Argument für Profile**: Ohne lokale Anpassung kann FHIR keine nationalen Anforderungen erfüllen (österreichische SVNR, deutsche Krankenversicherungsnummer, US-Sozialversicherung als Identifier). Medizinische Fachgebiete (Onkologie, Kardiologie) brauchen zusätzliche Felder. Regulatorische Anforderungen (ONC in den USA, ELGA in Österreich) erfordern Pflichtfelder. **Argument gegen proliferierende Profile**: Wenn jede Organisation eigene Profile baut, kann System A (US Core) nicht mit System B (EU-Core) kommunizieren, auch wenn beide FHIR sprechen. International Patient Summary (IPS) ist ein HL7-Versuch, ein gemeinsames Minimum zu definieren. **Lösungsansätze**: Schichtenmodell – internationales Profil als Basis (IPS) + nationales Profil (AT Core) als Einschränkung + organisationales Profil ganz oben. FHIR-IG-Hierarchien bauen aufeinander auf. **Konkretes Beispiel**: AT Core Patient muss alle US Core Patient-Felder unterstützen (via Basis-FHIR), fügt aber SVNR-Extension und österreichische ValueSets hinzu. Das erfordert sorgfältige Governance der IG-Familie.

---

## Mögliche Anschlussfragen des Prüfers

- Was ist ein Capability Statement und wie wird es abgerufen?
- Was ist SMART on FHIR und welche Rolle spielt OAuth2?
- Wie unterscheidet sich Contained Resource von einer Referenced Resource?
- Was ist der Unterschied zwischen `Medication` und `MedicationRequest`?
- Welche FHIR-Version ist aktuell im produktiven Einsatz? (FHIR R4, R4B, R5 coexistieren je nach Kontext)
- Wie funktioniert Reverse Chaining (`_has`) in FHIR Search?
- Was sind FHIR Operations (Services), und wie unterscheiden sie sich von REST-Resources?
- Was bedeutet FMM (FHIR Maturity Model) Level 0–5?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
