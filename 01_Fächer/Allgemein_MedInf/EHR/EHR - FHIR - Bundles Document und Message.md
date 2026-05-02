---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - FHIR Grundlagen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - FHIR - Bundles Document und Message

> [!info] Kurzdefinition
> Ein **Bundle** ist eine FHIR-Resource, die mehrere Resources zu einer Einheit zusammenfasst. Charakter und Zweck der Bundle bestimmt die **erste Resource (entry[0])**: bei **Composition** = Document, bei **MessageHeader** = Message. Bundles sind das Rückgabeformat von Search-Operationen und der Container für CDA-ähnliche Dokumente.

## Beschreibung

Aus den Folien 32–34, 70–75:

> „Documents and messages are equivalent.
> First resource in 'Bundle' defines whether the intention is a 'document' or a 'message'.
> Simple exchange of first resource within a Bundle transforms a message into a document and vice versa."

> „FHIR Document Bundles allow for the exchange of collections of resources as a single unit.
> 'FHIR Bundles are a way to package multiple resources into a single larger resource.'
> - Contain a Composition resource (which is another resource) as the first entry, providing context
> - Include all referenced resources within the bundle
> - Are immutable once created
> - Can be digitally signed for integrity and non-repudiation."

## Bestandteile / Aufbau

### Bundle-Typen (`Bundle.type`)

| Type | Erste Resource | Charakter |
|---|---|---|
| `document` | **Composition** | wie CDA, statisch, signierbar, immutable |
| `message` | **MessageHeader** | event-driven, request/response |
| `transaction` | – | atomare Operations-Liste |
| `batch` | – | unabhängige Operations-Liste |
| `searchset` | – | Search-Antwort |
| `history` | – | History einer Resource |
| `collection` | – | beliebige Sammlung |

### Document Bundle (Folie 34)

```
Bundle (type=document)
├── Composition (entry[0]) ← Header, Sections-Übersicht, Referenzen
├── Patient
├── Practitioner (Author)
├── Encounter
├── Observation 1
├── Observation 2
└── Condition
```

Wichtige Eigenschaften:
- **Immutable** nach Erstellung
- Kann **signiert** und **authentifiziert** werden
- Composition liefert Kontext (Title, Date, Author, Custodian, Sections)
- Alle Referenzierungen aufgelöst (alle benötigten Resources im Bundle enthalten)

### Message Bundle (Folie 33)

```
Bundle (type=message)
├── MessageHeader (entry[0]) ← Event-Code, Source, Destination
├── Resource 1 (z. B. Patient)
└── Resource 2 (z. B. ServiceRequest)
```

Eigenschaften:
- **Event-driven**: MessageHeader trägt Event-Code (z. B. `admin-notify`, `medication-administration`)
- **Request/Response**-fähig
- Asynchron möglich
- Ähnlich HL7 v2/v3 Messaging-Pattern

## Beispiel

**Indian Discharge Letter als FHIR Document** (Folie 72):

URL: `nrces.in/ndhm/fhir/r4/StructureDefinition-DischargeSummaryRecord.html` – ein Document Bundle mit Composition, Patient, Encounter, Observations etc., zusammen versendet.

**Saudi-Arabien Nphies** (Folie 75): Nutzt FHIR Messaging extensiv für Krankenversicherungs­transaktionen – Bundle vom Typ `message` mit MessageHeader für jede Transaktion.

## Abgrenzung

- **Document ≡ Message in der Bundle-Struktur** – nur die erste Resource unterscheidet. Beim Tausch der ersten Resource wird ein Document zur Message und umgekehrt.
- **Bundle ist eine Resource** – es kann selbst per REST gelesen/erstellt werden.
- **Bundle ≠ JSON-Array:** ein Bundle hat eigene Metadaten (type, total, link, entry).
- **CDA-Document ↔ FHIR-Document-Bundle:** funktional ähnlich; FHIR-Document-Bundle ist die strukturelle Antwort auf CDA-Documents.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein FHIR Bundle? Welche Bundle-Typen gibt es?

**Anwendungsfrage:** Wie wird aus einem Document-Bundle ein Message-Bundle? (Antwort: Composition als erste Resource gegen MessageHeader tauschen, Bundle.type ändern)

**Diskussionsfrage:** Documents sind immutable und signiert; Messages sind event-driven. Welcher Typ ist sinnvoller für ein Entlassungs­dokument, welcher für eine Lab-Order?

**Mögliche Anschlussfragen:**
- Wie unterscheidet sich `transaction` von `batch`?
- Welche Bundle-Type wird beim Search-Result verwendet? (Antwort: `searchset`)
- Wie funktioniert die digitale Signatur eines Document-Bundles?
- Was passiert, wenn eine im Bundle referenzierte Resource fehlt?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - References]]
- [[EHR - FHIR - 6 Exchange Paradigms]]
- [[EHR - CCD - Continuity of Care Document]]
- [[MSI - HL7 FHIR - Bundle]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 32–34 (Documents/Messages), 70–75 (Document Bundles, Indian Discharge Letter, Messaging, Nphies-Beispiel)
