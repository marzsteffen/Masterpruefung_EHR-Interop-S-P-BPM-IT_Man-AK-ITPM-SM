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

# EHR - FHIR - REST API und CRUD

> [!info] Kurzdefinition
> FHIR nutzt **REST** (Representational State Transfer) als primäre API-Architektur. Resources werden über HTTP-Verben **CRUD**-mäßig manipuliert: **POST** (Create), **GET** (Read), **PUT** (Update), **DELETE** (Delete) – plus Search, Batch, Transaction und Versionierung.

## Beschreibung

Aus Folie 44:

> „REST = Representational state transfer.
> Stateless operations – each request is handled as an independent transaction (no remembrance of state).
> Request/response – Requests are made to a resource's URL – Response comes as XML, HTML, JSON or other predefined format.
> GET, POST, PUT, DELETE – So resources can also be altered/deleted on the target server …"

Folie 45 ergänzt:

> „The FHIR RESTful API – For use with relative references – No obligation, but recommended. Allow to retrieve, search, update, delete … individual resources. Several reference implementations available."

## Bestandteile / Aufbau

### CRUD-Mapping

| Operation | HTTP | URL-Beispiel | Bedeutung |
|---|---|---|---|
| **Create** | POST | `[base]/Patient` | Neue Patient-Resource erstellen, Server vergibt ID |
| **Read** | GET | `[base]/Patient/12345` | Patient mit ID 12345 abrufen |
| **Update** | PUT | `[base]/Patient/12345` | Patient mit ID 12345 ersetzen |
| **Delete** | DELETE | `[base]/Patient/12345` | Patient mit ID 12345 löschen |
| **Patch** | PATCH | `[base]/Patient/12345` | Teilaktualisierung |
| **Read History** | GET | `[base]/Patient/12345/_history` | Versionsverlauf |
| **Read Specific Version** | GET | `[base]/Patient/12345/_history/2` | exakte Version |

### Eigenschaften

- **Stateless:** jede Request ist unabhängig, kein Server-Side-Session-Status
- **Standard-Formate:** JSON, XML, RDF/Turtle (per `_format`-Parameter oder `Accept`-Header)
- **Versionierung:** automatische History-Verwaltung pro Resource
- **Batch / Transaction:** mehrere Operationen in einer Request (Bundle mit type=batch oder type=transaction)
- **Capability Statement:** `[base]/metadata` listet, was der Server kann

### Folie 48: FHIR RESTful APIs

> „Standardized way to interact with FHIR resources over HTTP.
> Key aspects:
> - CRUD operations (Create, Read, Update, Delete) on resources
> - Search functionality with standardized parameters
> - Versioning of resources
> - Batch and transaction support for multiple operations
> All CRUD operations on a FHIR server can be done using similar HTTP operations."

## Beispiel

Patient mit ID 697701 abrufen (HAPI Public Test Server, Folie 59):

```
GET http://hapi.fhir.org/baseR4/Patient/697701
Accept: application/fhir+json
```

Antwort: `Patient`-Resource als JSON.

Neuen Patienten erstellen:

```
POST http://hapi.fhir.org/baseR4/Patient
Content-Type: application/fhir+json

{
  "resourceType": "Patient",
  "name": [{"family": "Mustermann", "given": ["Max"]}],
  "gender": "male",
  "birthDate": "1980-05-15"
}
```

Antwort: 201 Created mit Location-Header `Patient/<neue-id>`.

## Abgrenzung

- **REST ≠ Messaging:** REST ist synchron, request/response auf Resource-URL. Messaging ist event-driven mit MessageHeader.
- **REST ≠ Documents:** REST liefert einzelne Resources oder Search-Bundles; Documents liefern eine Composition mit allen referenzierten Resources.
- **Stateless:** Authentifizierung via Token (OAuth2/SMART) ist keine Server-Session, sondern stateless.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet REST und welche HTTP-Verben werden für CRUD genutzt?

**Anwendungsfrage:** Wie würdest du einen Patienten mit ID 12345 lesen, dann seinen Nachnamen ändern, dann den Patienten löschen? (Antwort: GET, PUT, DELETE auf `[base]/Patient/12345`)

**Diskussionsfrage:** Stateless ist ein Kernprinzip von REST. Welche Konsequenzen hat das für Performance, Skalierung und Authentifizierung?

**Mögliche Anschlussfragen:**
- Was passiert bei einer 404 / Not Found?
- Wie funktioniert Versionierung in FHIR?
- Was ist ein Capability Statement?
- Wie sieht eine Batch- vs. Transaction-Bundle aus?
- Wie wird Security gehandhabt? (Stichwort: SMART on FHIR, OAuth2)

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Search]]
- [[EHR - FHIR - References]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - 6 Exchange Paradigms]]
- [[ASP - OAuth2]]
- [[ASP - SMART on FHIR]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 44–49 (RESTful Web Services, FHIR RESTful API, CRUD)
