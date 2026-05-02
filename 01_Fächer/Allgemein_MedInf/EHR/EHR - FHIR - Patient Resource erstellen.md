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

# EHR - FHIR - Patient Resource erstellen

> [!info] Kurzdefinition
> Eine **Patient-Resource** wird als JSON- oder XML-Dokument gemäß FHIR-Schema gebaut und per **HTTP POST** an den Patient-Endpoint eines FHIR-Servers gesendet. Der Server vergibt eine ID und antwortet mit **201 Created** plus Location-Header.

## Beschreibung

Die Patient-Resource ist die zentrale Stammdaten-Resource in FHIR. Beim **Erstellen** (POST) vergibt der Server die ID; beim **Update** (PUT) muss die ID bekannt sein. JSON-Validierung erfolgt typischerweise über das offizielle FHIR JSON Schema (HL7.org/FHIR → Downloads).

## Bestandteile / Aufbau

### Pflicht- und übliche Felder einer Patient-Resource

| Feld | Datatype | Cardinality | Inhalt |
|---|---|---|---|
| `resourceType` | string | 1..1 | Immer `"Patient"` |
| `id` | id | 0..1 | Vom Server vergeben (bei Update Pflicht) |
| `identifier` | Identifier | 0..* | Business-IDs (z. B. SVNR) |
| `active` | boolean | 0..1 | Wahr/falsch |
| `name` | HumanName | 0..* | Familien-, Vorname |
| `telecom` | ContactPoint | 0..* | Telefon, E-Mail |
| `gender` | code | 0..1 | `male`/`female`/`other`/`unknown` |
| `birthDate` | date | 0..1 | YYYY-MM-DD |
| `address` | Address | 0..* | Strasse, Stadt, PLZ, Land |

In der Base-Resource ist **technisch nichts Pflicht** außer `resourceType`. Das macht Patient besonders flexibel – aber Profile (z. B. US Core, AT Core) verschärfen Cardinalities (siehe [[EHR - FHIR - Profiles und Must Support]]).

### Beispiel-JSON

```json
{
  "resourceType": "Patient",
  "active": true,
  "identifier": [
    {
      "system": "urn:oid:1.2.40.0.10.1.4.3.1",
      "value": "1234010180"
    }
  ],
  "name": [
    {
      "use": "official",
      "family": "Mustermann",
      "given": ["Max"]
    }
  ],
  "telecom": [
    { "system": "phone", "value": "+43-664-1234567", "use": "mobile" },
    { "system": "email", "value": "max.mustermann@example.com" }
  ],
  "gender": "male",
  "birthDate": "1980-05-15",
  "address": [
    {
      "use": "home",
      "line": ["Hauptstrasse 1"],
      "city": "Graz",
      "postalCode": "8010",
      "country": "AT"
    }
  ]
}
```

### Workflow: Patient anlegen

| Schritt | HTTP | Beispiel |
|---|---|---|
| 1. Resource bauen | – | JSON wie oben |
| 2. POST an Server | `POST [base]/Patient` | Body = JSON |
| 3. Server-Antwort prüfen | – | Status `201 Created`, `Location: [base]/Patient/12345` |
| 4. ID extrahieren | – | `12345` |
| 5. (Optional) GET zur Verifikation | `GET [base]/Patient/12345` | Status `200 OK` |

### Tools

- **Validierung lokal:** VSCode + offizielles `fhir.schema.json` für Autocomplete und Schema-Errors
- **REST-Calls:** Insomnia, Postman, curl
- **Public Test-Server:** HAPI FHIR (`http://hapi.fhir.org/baseR4`), FH JOANNEUM (`http://diam.fh-joanneum.at:8021/hapi-fhir-jpaserver/`)

## Beispiel

curl-Beispiel für den Create-Call:

```bash
curl -X POST \
  -H "Content-Type: application/fhir+json" \
  -H "Accept: application/fhir+json" \
  --data @patient.fhir.json \
  http://hapi.fhir.org/baseR4/Patient
```

Antwort:
```
HTTP/1.1 201 Created
Location: http://hapi.fhir.org/baseR4/Patient/697701/_history/1
ETag: W/"1"
```

## Abgrenzung

- **Patient ist eine Base-Resource** (siehe [[EHR - FHIR - Resource Kategorien]]).
- **Patient.identifier (Business-ID) ≠ Patient.id (technische FHIR-ID).** Identifier ist z. B. SVNR, ID ist die Server-vergebene FHIR-ID.
- **POST vs. PUT:** POST → Server vergibt ID; PUT → Client kennt ID schon. PUT ohne existierende ID erstellt die Resource (Create via Update).
- Eine Patient-Resource beschreibt eine **Person als Versorgungs-Subjekt**, nicht eine `Person`-Resource (administrativ) oder `RelatedPerson` (Angehörige).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie erzeugt man eine FHIR-Patient-Resource? Welche Felder sind typischerweise enthalten?

**Anwendungsfrage:** Schreibe eine minimale Patient-Resource mit Name, Geschlecht und Geburtsdatum als JSON.

**Diskussionsfrage:** In der Base-Resource ist nichts Pflicht außer `resourceType`. Welche Risiken birgt das, und warum existieren Profile?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen `identifier` und `id`?
- Welche Status-Codes erwartet man bei POST/GET/PUT/DELETE?
- Wie validiert man eine Resource gegen ein Profile?
- Was ist `active=false` und wann wird es gesetzt?
- Wie verhält sich Patient zu Person und RelatedPerson?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Data Types und Cardinality]]
- [[EHR - FHIR - Profiles und Must Support]]
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - Observation Resource erstellen]]
- [[EHR - FHIR - Transaction Bundle]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Praxis-Hintergrund: Übungs-PDF SS23_FHIR Ressource creation.pdf (nicht als eigene Quell-Note übernommen, da reine Hands-on-Anleitung; relevante Inhalte hier generisch aufgenommen)
