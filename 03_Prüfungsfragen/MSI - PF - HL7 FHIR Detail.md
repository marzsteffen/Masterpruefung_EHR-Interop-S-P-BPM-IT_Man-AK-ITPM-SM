---
fach: msi
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - fach/allgemein/msi
  - typ/pruefungsfrage
  - status/offen
  - flashcards
---

# MSI - PF - HL7 FHIR Detail

## Kontext

Tiefenkarte zu HL7 FHIR (Fast Healthcare Interoperability Resources). Abgedeckt: Definition/80-20-Regel, Paradigmen, Versionen, Resource-Hierarchie, Ressource-Aufbau, Identity/Identifier, Elemente und Datentypen, REST API, Search, References, Extensions, Profile, Bundles, Deployment-Muster, Validierung, SMART on FHIR, Implementation Guides, FSH/SUSHI, FhirPath, CDS Hooks, CQL, Questionnaire/SDC. Terminologie-spezifische Karten (CodeSystem, ValueSet, ConceptMap, Binding Strengths, Terminology Service) → [[MSI - PF - HL7 FHIR Terminologie]]. CDA-Vergleich → [[MSI - PF - HL7 CDA Detail]].

## Verlinkte Konzepte

- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - Versionen]]
- [[MSI - HL7 FHIR - Paradigmen]]
- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Ressourcentypen]]
- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - Element]]
- [[MSI - HL7 FHIR - Reference]]
- [[MSI - HL7 FHIR - Extension]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Operationen]]
- [[MSI - HL7 FHIR - Search]]
- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 FHIR - Deployment Muster]]
- [[MSI - HL7 FHIR - Validierung]]
- [[MSI - HL7 FHIR - SMART on FHIR]]
- [[MSI - HL7 FHIR - Implementation Guide]]
- [[MSI - HL7 FHIR - FHIR Shorthand (FSH) und SUSHI]]
- [[MSI - HL7 FHIR - FhirPath]]
- [[MSI - HL7 FHIR - CDS Hooks]]
- [[MSI - HL7 FHIR - CQL]]
- [[MSI - HL7 FHIR - Questionnaire und SDC IG]]

---

## Karten

### Definition

Was ist HL7 FHIR, und welche drei Kerneigenschaften machen es für moderne Health-IT besonders geeignet? Was besagt die 80/20-Regel?

?

**FHIR** (*Fast Healthcare Interoperability Resources*): offener, entwicklerorientierter Interoperabilitätsstandard von HL7 International.

**Drei Kerneigenschaften:**
1. **Entwickler-Fokus**: Einsatz moderner Webtechnologien (REST, JSON, XML, HTTP) – vertrautes Technologie-Stack
2. **Entwicklung anhand echter Use Cases**: praxisorientiert, kein rein theoretisches Modell
3. **Open Source**: frei verfügbare Referenzimplementierungen

**80/20-Regel:**
- 80 % der Health-IT-Use-Cases werden durch den Standard out-of-the-box abgedeckt
- 20 % werden über Profilierung, Extensions und Implementation Guides abgedeckt
- Konsequenz: ältere Standards (HL7 v2, CDA) sind für Mobilgeräte und API-basierte Anwendungen zu schwergewichtig — FHIR schließt diese Lücke

**FHIR ist mehr als Ressourcen**: umfasst auch Nachrichten, Dokumente, Operationen, Prozessmanagement, Referenzimplementierungen und Community-Erweiterungen (CDS Hooks, FHIRCast, …).

---

Welche vier Austausch-Paradigmen existieren im Gesundheitswesen? Ordnen Sie je einen Standard zu. Wo ordnet sich FHIR ein?

?

| Paradigma | Ansatz | Beispiel-Standard |
|---|---|---|
| **Nachrichtenbasiert** | Events/Trigger werden übertragen | HL7 v2 |
| **Dokumentenbasiert** | Abgeschlossene Informationseinheit (Arztbrief, Befund) | HL7 CDA |
| **Anwendungsspezifisch** | Auf klinische Domänen ausgerichtet | DICOM, HL7 CCD |
| **Ressourcenbasiert** | Atomare Einheiten, einzeln verwaltet und kombiniert | HL7 FHIR |

**FHIR → ressourcenbasiert** als Kernparadigma.

Vorteile ressourcenbasiert: granulare Abfragen, unabhängige Änderbarkeit, leichtgewichtig.
Nachteile: keine native Gesamtübersicht (→ löst FHIR mit Bundle/Dokument) und keine nativen Prozessmodelle.

**FHIR unterstützt auch** Nachrichten und Dokumente — es ist nicht rein ressourcenbasiert, aber das ist sein Kernansatz.

---

Erläutern Sie die FHIR-Versionshistorie. Was sind normative Ressourcen, und ab welcher Version wurden sie eingeführt?

?

| Kurzname | Versionsnummer | Besonderheit |
|---|---|---|
| DSTU1 | 0.0 | erster Draft |
| DSTU2 | 1.0 | – |
| STU3 | 3.0 | – |
| R4 | 4.0.1 | **erste normative Ressourcen** |
| R5 | 5.0 | aktuelle Version |

**Versionszyklus**: ~18 Monate zwischen Major Releases.

**Normative Ressourcen (ab R4):**
- Vorher: alle Ressourcen „Standard for Trial Use" (STU) — jederzeit änderbar
- Ab R4: ausgewählte Ressourcen (z. B. Patient, Observation) sind normativ: nur bei zwingend nötigem Grund geändert, immer **abwärtskompatibel**
- Nicht alle Ressourcen sind normativ; nicht normative bleiben STU oder experimentell

**Reifegrad**: FHIR Maturity Model (FMM) — in der Spezifikation durch Farben/Nummern markiert. Nicht-normative Ressourcen mit niedrigem FMM sollten in Produktivsystemen mit Vorsicht eingesetzt werden.

---

Was ist der Unterschied zwischen `Resource` und `DomainResource` in FHIR? Welche Felder hat jede Klasse?

?

```
Resource (abstrakte Basisklasse)
├── id            ← serverlokal, technische ID
├── meta          ← Metadaten (nur Server darf schreiben)
├── implicitRules ← Regeln, die die Interpretation einschränken
└── language      ← Dokumentsprache
    │
    └── DomainResource (erbt Resource)
        ├── text              ← narrativer Text (Pflicht, menschenlesbar)
        ├── contained         ← eingebettete Ressourcen (Anti-Pattern)
        ├── extension         ← optionale Erweiterungsfelder
        └── modifierExtension ← semantisch modifizierende Erweiterungen
            └── [domänenspezifische Felder]
```

**Resource**: technische Basisklasse, **nicht erweiterbar** (keine Extensions, kein Narrative). Beispiele: `Bundle`, `Binary`, `Parameters`.

**DomainResource**: klinisch/organisatorisch relevant, **erweiterbar** via Extensions. Alle klinischen Ressourcen (Patient, Observation, Condition, …) sind DomainResources.

**Vergleich Narrative CDA vs. FHIR**: In CDA ist der Narrative die Primärquelle. In FHIR sind strukturierte Daten primär; Narrative ist ein Anzeige-Ergänzungsfeld.

---

Was ist der Unterschied zwischen `ID`, `Identity` und `Identifier` in FHIR? Welcher ist für systemübergreifende Interoperabilität am wichtigsten?

?

| Konzept | Typ | Scope | Beispiel |
|---|---|---|---|
| **ID** | Technisch | Serverlokal | `123` (nur gültig auf diesem Server) |
| **Identity** | Technisch | Global (URI) | `http://hapi.fhir.org/baseR4/Patient/123` |
| **Identifier** | Fachlich | Systemübergreifend | SVNR `1234010190` |

**Wichtige Punkte:**
- **ID** ist serverlokal: bei Server-Migration ändert sich die ID
- **Identifier** bleibt stabil, weil er unabhängig vom Server ist (SVNR ändert sich nicht)
- Für systemübergreifende Interoperabilität → **Identifier verwenden**
- Häufiger Irrtum in FHIR-Tutorials: Identifier wird als primäre ID dargestellt — falsch

**Suche nach Identifier** (nicht ID):
```
GET /Patient?identifier=urn:oid:1.2.40.0.10|1234010190
```

---

### Anwendung

Welche HTTP-Methoden verwendet die FHIR REST API? Erläutern Sie CRUD + Search + History. Was passiert bei `DELETE`?

?

| HTTP-Methode | Operation | URL-Pattern | Rückgabe |
|---|---|---|---|
| `GET` | Read All | `/Patient` | Bundle mit allen Instanzen |
| `GET` | Read | `/Patient/{id}` | einzelne Ressource |
| `POST` | Create | `/Patient` + Body | neue Ressource + Location-Header |
| `PUT` | Update | `/Patient/{id}` + Body | überschreibt gesamte Ressource |
| `DELETE` | Delete | `/Patient/{id}` | logisches Löschen |
| `GET` | Search | `/Patient?gender=M` | Bundle (searchset) |
| `GET` | History | `/Patient/{id}/_history` | alle Versionen |

**DELETE in FHIR = logisches Löschen (soft delete)**:
- Erzeugt eine Tombstone-Version
- History bleibt abrufbar über `_history`
- Nach DELETE liefert `GET /Patient/{id}` HTTP 410 Gone
- Kein physisches Löschen

**Format-Steuerung**: JSON via `?_format=json` oder `Accept: application/fhir+json`; XML via `?_format=xml` oder `Accept: application/fhir+xml`.

---

Wie funktioniert FHIR-Suche? Was wird zurückgeliefert, und was ist der Unterschied zwischen Identifier-Suche und ID-Abfrage?

?

**Grundform:**
```
GET /[Ressourcentyp]?[parameter]=[wert]
```

**Ergebnis**: immer ein **Bundle vom Typ `searchset`** (nicht die Ressource direkt).

**Parameter-Typen**: string (Name, Adresse), token (Codes, Identifier: `system|code`), reference (Referenz), date (Datumsbereiche), number/quantity, composite.

**Parameterkombination**: mehrere Parameter = AND-Verknüpfung.
```
GET /Observation?patient=Patient/123&code=8480-6
```

**Identifier-Suche vs. ID-Abfrage:**
```
GET /Patient?identifier=urn:oid:1.2.40.0.10|1234010190  ← fachlich, systemübergreifend
GET /Patient/123                                         ← technisch, serverlokal
```
Für systemübergreifende Suche → immer Identifier-Suche verwenden, da ID serverlokal ist.

**SearchParameter sind selbst FHIR-Ressourcen** (`SearchParameter`): eigene Suchparameter können erstellt und registriert werden.

---

Welche fünf Referenz-Arten gibt es in FHIR? Was ist das Anti-Pattern bei Contained Resources?

?

| Art | Format | Beispiel |
|---|---|---|
| **Absolut** | Volle URL | `http://server/fhir/Patient/1` |
| **Relativ** | Typ/ID | `Patient/1` |
| **Versionsspezifisch** | Typ/ID/_history/Version | `Patient/1/_history/2` |
| **Kanonisch** | URL mit optionaler Pipe-Version | `http://hl7.org/fhir/ValueSet/vs\|0.8` |
| **Lokal** | #-Referenz | `#p1` (zeigt auf Contained Resource) |

**Contained Resources — Anti-Pattern:**
```xml
<Condition>
  <contained>
    <Practitioner><id value="p1"/>...</Practitioner>
  </contained>
  <asserter><reference value="#p1"/></asserter>
</Condition>
```
- Brechen (fast) alle Vorteile von FHIR (keine eigene ID, kein eigener Endpoint, kein Caching)
- Nur verwenden, wenn die Anzahl separater Abfragen minimiert werden muss und keine bessere Lösung existiert
- **Empfohlene Alternativen**: FHIR Document oder Bundles

---

Was ist `extension` vs. `modifierExtension`? Wann ist eine Extension eine Pflichtkenntnis für verarbeitende Systeme?

?

**Extension** (URL-identifiziertes Erweiterungsfeld):
- Identifiziert ausschließlich über URL (keine normalen Feldnamen)
- Tritt auf: DomainResources, komplexe Datentypen, primitive Datentypen (via `_field`)
- Beispiel:
  ```xml
  <extension url="http://hl7.org/fhir/StructureDefinition/patient-birthTime">
    <valueDateTime value="1974-12-25T14:35:45-05:00"/>
  </extension>
  ```

| | extension | modifierExtension |
|---|---|---|
| **Semantik** | Ergänzt Information, ändert nichts | **Kann Interpretation** bestehender Felder verändern |
| **Unbekannt?** | Systeme dürfen ignorieren | Systeme dürfen Ressource **NICHT** verarbeiten |
| **Einsatz** | Nationale Felder (z. B. SVNR-Datum) | Semantisch kritische Modifikation (selten) |

**Nicht erweiterbar** (keine Extensions möglich): technische `Resource`-Basisklasse (Bundle, Binary, Parameters).

---

Wie funktioniert SMART on FHIR? Welche drei FHIR-Ressourcen unterstützen Auditing und Datenschutz?

?

**SMART on FHIR** (Substitutable Medical Applications, Reusable Technologies):
- Community-Standard für Sicherheit in FHIR-Systemen
- Sicherheit ist **kein integraler Bestandteil** der FHIR-API — SMART ist eine Empfehlung
- Technologie: essentiell **OAuth2** (Bearer-Token, Scopes)
- Scopes definieren Zugriffsrechte: Format `[context]/[Ressourcentyp].[operation]`
  - Beispiel: `patient/*.read` → lesender Zugriff auf alle Ressourcen des Patienten

**FHIR-Ressourcen für Auditing/Datenschutz:**

| Ressource | Zweck | Verbindlichkeit |
|---|---|---|
| **AuditEvent** | Technisches Logging: wer hat wann auf was zugegriffen | Empfohlen (verpflichtend für konforme Server) |
| **Provenance** | Fachliche Nachvollziehbarkeit: warum wurde eine Ressource angelegt/geändert | Empfohlen |
| **Consent** | Einwilligung des Patienten für Datenzugriff und Operationen | Situationsabhängig |

**AuditEvent vs. Provenance**: AuditEvent = technisches Access-Log; Provenance = fachliche Änderungshistorie.

---

### Diskussion / Vergleich

Was ist der Unterschied zwischen FHIR Facade und FHIR Server? Warum garantiert keines dieser Muster allein Interoperabilität?

?

**FHIR Facade** — FHIR als Interface-Schicht über bestehende Systeme:
- Vorteile: keine Synchronisationsprobleme, keine zusätzlichen Systeme, bestehende Systeme bleiben unverändert, niedrige Einstiegshürde
- Nachteile: IDs der Ressourcen schwer konsistent zu halten; FHIR-Standard wird nur nach Bedarf genutzt (kein voller Funktionsumfang)
- Typischer Einsatz: Krankenhaus mit KIS/LIS, das FHIR-Schnittstellen nach außen anbieten möchte

**FHIR Server** — FHIR als primäres Datenhaltungssystem:
- Vorteile: volle FHIR-Funktionalität (History, Suche, Terminologie-Integration), standardkonformes Datenmodell
- Nachteile: zusätzliches System, Migrationsbedarf, Doppelhaltung möglich
- Typischer Einsatz: Greenfield-Projekte, nationale Plattformen

**„FHIR Server ≠ Interoperabilität":**
Semantische Interoperabilität entsteht erst durch:
1. Vereinbarte Profile (nationale/projektspezifische StructureDefinitions)
2. Einheitliche Terminologien und Value Sets
3. Implementation Guides als gemeinsame Spezifikation

---

Was ist ein FHIR-Profil (StructureDefinition) und was kann es definieren? Was ist der Unterschied zwischen Differential Table und Snapshot Table?

?

**Profil (StructureDefinition)**: spezialisiert eine Basis-Ressource für einen Anwendungsfall oder nationalen Kontext.

**Was ein Profil definiert:**
- Kardinalitäten einschränken (z. B. `0..1` → `1..1`) oder verbieten (`0..0`)
- Extensions hinzufügen (nationale Felder, z. B. SVNR-Ausstellungsdatum)
- Terminology Bindings verstärken (z. B. `preferred` → `required`)
- Slicing auf mehrfach vorkommende Felder anwenden

**Differential Table vs. Snapshot Table:**
- **Differential Table**: zeigt nur die **Änderungen gegenüber dem Basisprofil** (Diff)
- **Snapshot Table**: zeigt **alle Elemente**, inkl. geerbter Felder vollständig (vollständige Sicht)

**Profilierung veröffentlichen**: via Simplifier.net, build.fhir.org, profiles.ihe.net.

**Österreichisches Beispiel**: `AustrianPatient` — verpflichtende SVNR als Identifier, Extension für Staatsbürgerschaft, österreichisches Value Set für Geschlecht.

---

Welche Bundle-Typen gibt es in FHIR und welcher wird wann verwendet?

?

Bundle ist ein Container-Ressourcentyp (`Resource`, nicht `DomainResource` — keine Extensions, kein Narrative).

| Bundle-Typ | Verwendung |
|---|---|
| **document** | FHIR-Dokument (unveränderliche Momentaufnahme, erster Entry = Composition) |
| **message** | FHIR-Nachricht (event-basiert, wie HL7 v2) |
| **transaction** | Atomare Gruppe: alles oder nichts |
| **transaction-response** | Antwort auf Transaction |
| **batch** | Gruppe von Operationen (nicht atomar) |
| **searchset** | Suchergebnis (`GET /Patient?…`) |
| **collection** | Generische Sammlung |
| **history** | Versionshistorie |

**Abgrenzungen:**
- `transaction` vs. `batch`: Transaction = atomar; Batch = Einzeloperationen, die unabhängig voneinander scheitern können
- FHIR-Dokument = Bundle(document) mit Composition als erstem Entry → ähnlich CDA
- Contained Resources vs. Bundle: Bundle bevorzugen — kein Anti-Pattern

---

Wie überwindet FHIR die Stärken des dokumentenbasierten Paradigmas (CDA)? Vergleichen Sie FHIR Document mit CDA.

?

**CDA-Stärken, die FHIR adressiert:**

| Aspekt | HL7 CDA | FHIR-Äquivalent |
|---|---|---|
| Persistentes Dokument | ClinicalDocument-Root | Bundle(type=document) + Composition |
| Narrativer Text als Primärquelle | `<text>` in Sections | Composition.section.text |
| Strukturierte Entries | CDA Level 3 | FHIR-Ressourcen als Bundle-Entries |
| Authentisierung | legalAuthenticator | Composition.attester |
| Custodian | `<custodian>` | Composition.custodian |

**Wichtiger Unterschied**: In CDA ist der Narrative die rechtlich maßgebliche Primärquelle; in FHIR sind strukturierte Ressourcen primär, Narrative ist Ergänzungsfeld.

**Wann CDA bevorzugen?**
- Wenn Rechtssicherheit durch Narrative-first-Ansatz wichtig ist
- Wenn ELGA-konforme Dokumente gefordert sind (Österreich: CDA-basiert)
- Wenn XSLT-basiertes Rendering zentraler Bestandteil ist

**Wann FHIR bevorzugen?**
- API-basierte Integration, Mobile Apps, REST-Ökosystem
- Wenn granulare Abfragen von Einzelressourcen benötigt werden

---

Was prüft `$validate` in FHIR, und was prüft ein einfaches XML/JSON-Schema nicht? Was ist eine `OperationOutcome`?

?

**FHIR-Validierung via `$validate`:**
```
POST [base]/Patient/ID/$validate
{Body: Patient-Ressource}
```

**Was $validate prüft, Schema nicht:**
- Kardinalitäten im Kontext von Profilen (über Basis-Schema hinaus)
- Terminology Bindings: ist der Code im gültigen Value Set?
- Profil-Konformität (gegen StructureDefinition)
- Bedingungsregeln (FhirPath-Invarianten in StructureDefinitions)

**Schema (XSD/JSON Schema) prüft nur**: Wohlgeformtheit, Datentypen, elementare Struktur.

**OperationOutcome**: standardisierte FHIR-Ressource für Validierungsergebnisse und Fehlerantworten:
```json
{
  "resourceType": "OperationOutcome",
  "issue": [{
    "severity": "error",
    "code": "invalid",
    "diagnostics": "Patient.identifier: required element missing"
  }]
}
```
`severity`: `fatal` | `error` | `warning` | `information`

---

Was sind Implementation Guides, FSH/SUSHI, FhirPath, CDS Hooks und CQL — und wie hängen sie zusammen?

?

**Implementation Guide (IG):** bündelt Profile, Extensions, ValueSets, ConceptMaps zu einem kohärenten Anwendungsfall. Ohne IG keine Interoperabilität. Beispiele: IPS (International Patient Summary), AT Core Profile (Österreich R5).

**FSH/SUSHI — Autoring-Toolchain für IGs:**
- **FSH** (FHIR Shorthand): domänenspezifische Autoren-Sprache für Profile, ValueSets, Instanzen (Spec: `hl7.org/fhir/uv/shorthand/`)
- **SUSHI**: Compiler FSH → valide FHIR JSON/XML → IG Publisher baut daraus den IG
- Analogie: FSH ≈ Markdown, SUSHI ≈ Pandoc, IG ≈ fertige Webseite

**FhirPath:** Navigations- und Abfragesprache innerhalb einer FHIR-Ressource (analog XPath für XML). Verwendet in StructureDefinitions (Invarianten), CQL, CDS Hooks.

**CDS Hooks:** Protokoll für event-getriebene klinische Entscheidungsunterstützung. Trigger-Ereignis (z. B. Patientenansicht öffnen) → externe CDS-Logik → Pop-Up im KIS. CDS Hooks ist kein Teil der FHIR-Spezifikation, baut aber auf FHIR auf.

**CQL** (Clinical Quality Language): Ausdruckssprache für CDS-Logik und klinische Qualitätsmetriken. Liefert die Logik hinter CDS-Hook-Triggern.

**Zusammenhang**: FhirPath navigiert; CQL evaluiert Logik; CDS Hooks triggert und kommuniziert; IGs bündeln alles in eine Spezifikation; FSH/SUSHI erstellt IGs.

---

Welche Vorteile hat FHIR gegenüber HL7 v2 und CDA — und welche Schwächen hat FHIR trotzdem?

?

| Aspekt | HL7 v2 | HL7 CDA | HL7 FHIR |
|---|---|---|---|
| **Technologie** | proprietäres Pipe-Format | XML (schwergewichtig) | REST, JSON/XML, HTTP |
| **Mobile-Tauglichkeit** | Nein | Schlecht | Gut |
| **Granularität** | Nachricht (Gesamtereignis) | Dokument (Gesamtdokument) | Ressource (atomar) |
| **Erweiterbarkeit** | Schwach | Mittels Templates | Profile + Extensions |
| **Abwärtskompatibilität** | Ja (aber Chaos durch Eigenimplementierungen) | Ja (ISO-Standard) | Ab R4 normative Ressourcen |
| **Community** | Groß, aber veraltet | Mittel | Stark wachsend |

**FHIR-Schwächen:**
1. **Stabilität**: häufige Versionen (pre-R4), obwohl normative Ressourcen dieses Problem adressieren
2. **Schwer zu meistern**: volle Implementierung komplex (Profilierung, Terminologie, IGs)
3. **FHIR Server ≠ Interoperabilität**: ohne Profile und IGs kein echter semantischer Datenaustausch
4. **Koexistenz statt Ablösung**: HL7 v2 bleibt dominant in Krankenhäusern — FHIR Facade überbrückt

---

## Mögliche Anschlussfragen des Prüfers

- Was ist der Unterschied zwischen `PUT` (Update) und `PATCH` in FHIR?
- Was gibt `GET /Patient/1/$everything` zurück?
- Was ist ein Backbone Element, und warum ist es keine eigenständige Ressource?
- Wie wird Paginierung bei großen Suchergebnissen realisiert? (→ `Bundle.link` mit `next`)
- Welche FHIR-Ressource modelliert ein interaktives Formular? (→ `Questionnaire` / `QuestionnaireResponse`)
- Was ist der Unterschied zwischen Questionnaire und QuestionnaireResponse?
- Was macht der SDC IG gegenüber dem Basis-Questionnaire zusätzlich? (→ Pre-population, Datenextraktion)
- Welche Österreich-spezifischen FHIR-IGs kennen Sie? (→ AT Core Profile R5, ELGA FHIR IG)
- Wie unterscheiden sich AuditEvent und Provenance?
- Was ist kanonische URL-Versionierung? (`URL|Version`)

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
