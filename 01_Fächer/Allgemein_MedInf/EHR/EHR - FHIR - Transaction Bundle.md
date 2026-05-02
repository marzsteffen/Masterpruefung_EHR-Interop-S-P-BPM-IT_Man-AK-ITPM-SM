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

# EHR - FHIR - Transaction Bundle

> [!info] Kurzdefinition
> Ein **Transaction Bundle** ist eine Bundle vom Typ `transaction`, die mehrere REST-Operationen (POST, PUT, DELETE) atomar zum FHIR-Server schickt: **alle oder keine** werden ausgeführt. Wichtig für referenzielle Konsistenz – z. B. einen Patient + zugehörige Observation in einem Schritt anlegen.

## Beschreibung

### All-or-Nothing-Logik

> Transactions bundles are used to transfer several resource actions to a server. The server will try to perform all actions (creating resources, updating resources etc.). ONLY when all actions of the bundle are successfully performed the transaction is successful (all or nothing). In comparison to a collection bundle where the bundle is stored as such.

Wenn auch nur eine Operation scheitert, wird die gesamte Transaction zurückgerollt. Damit lassen sich konsistente Multi-Resource-Updates absichern.

### Aufbau

```
Bundle (type=transaction)
├── entry[0]
│     ├── fullUrl: urn:uuid:patient
│     ├── resource: { resourceType: "Patient", ... }
│     └── request: { method: "POST", url: "Patient" }
├── entry[1]
│     ├── fullUrl: urn:uuid:observation
│     ├── resource: { resourceType: "Observation", subject: { reference: "urn:uuid:patient" }, ... }
│     └── request: { method: "POST", url: "Observation" }
```

Der Trick mit `urn:uuid:` als `fullUrl`: Damit kann die Observation auf den noch-nicht-existierenden Patienten verweisen, **bevor** der Server die echte ID vergeben hat. Der Server löst diese internen Verweise automatisch auf, sobald er die Patient-Resource erstellt hat.

## Bestandteile / Aufbau

### Pro Entry erforderlich

| Feld | Inhalt |
|---|---|
| `fullUrl` | Eindeutiger Identifier innerhalb des Bundles, z. B. `urn:uuid:patient-1`. Wird zur internen Referenzierung genutzt. |
| `resource` | Die eigentliche Resource (Patient, Observation, …) |
| `request.method` | `POST` (Create), `PUT` (Update/Upsert), `DELETE`, `GET`, `PATCH` |
| `request.url` | Ziel-Pfad relativ zum Server, z. B. `Patient` (für POST) oder `Patient/12345` (für PUT) |

### Häufige Operationen

| Operation | request.method | request.url |
|---|---|---|
| Create neu | POST | `Patient` |
| Update mit ID | PUT | `Patient/12345` |
| Conditional Update | PUT | `Patient?identifier=...` |
| Conditional Create | POST | `Patient` mit Header `If-None-Exist: identifier=...` |
| Delete | DELETE | `Patient/12345` |

### Conditional Update (siehe Folie 23 des Übungs-PDFs)

Statt blind einen neuen Patienten anzulegen, kann man **conditional** updaten:

```json
"request": {
  "method": "PUT",
  "url": "Patient?name=Mustermann"
}
```

Logik: „Wenn Patient mit Name=Mustermann existiert → updaten; sonst neu anlegen." Verhindert Duplikate.

## Beispiel: Patient + Observation in einem Bundle

```json
{
  "resourceType": "Bundle",
  "type": "transaction",
  "entry": [
    {
      "fullUrl": "urn:uuid:patient-1",
      "resource": {
        "resourceType": "Patient",
        "name": [{ "family": "Mustermann", "given": ["Max"] }],
        "gender": "male",
        "birthDate": "1980-05-15"
      },
      "request": {
        "method": "POST",
        "url": "Patient"
      }
    },
    {
      "fullUrl": "urn:uuid:obs-1",
      "resource": {
        "resourceType": "Observation",
        "status": "final",
        "code": {
          "coding": [{ "system": "http://loinc.org", "code": "29463-7", "display": "Body weight" }]
        },
        "subject": { "reference": "urn:uuid:patient-1" },
        "valueQuantity": { "value": 78.5, "unit": "kg", "system": "http://unitsofmeasure.org", "code": "kg" }
      },
      "request": {
        "method": "POST",
        "url": "Observation"
      }
    }
  ]
}
```

POST gegen `[base]/` (Bundle-Root, nicht `[base]/Bundle`!) → Server erstellt beide Resources atomar, ersetzt `urn:uuid:patient-1` durch die echte Server-ID, und liefert ein Antwort-Bundle mit allen vergebenen IDs.

## Abgrenzung

- **Transaction ≠ Batch:** `batch` führt jede Operation **unabhängig** aus – ein Fehler bei Entry 2 lässt Entry 1 bestehen. `transaction` rollt alles zurück.
- **Transaction ≠ Collection:** `collection`-Bundles sind reine Datencontainer ohne ausgeführte Operationen.
- **POST gegen `[base]/`** (nicht `[base]/Bundle`!): Der Bundle-Root ist der korrekte Endpoint für Transactions/Batches.
- **fullUrl mit `urn:uuid:`** ist nur **innerhalb** des Bundles gültig – der Server ersetzt es durch echte URLs in der Antwort.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Transaction Bundle, und welche Garantien bietet es?

**Anwendungsfrage:** Schreibe ein Transaction Bundle, das einen Patienten und eine zugehörige Observation in einem Schritt anlegt. Wie verweist die Observation auf den (noch nicht existierenden) Patienten?

**Diskussionsfrage:** Wann wählt man Transaction, wann Batch? Welche Trade-offs (Konsistenz vs. Toleranz für Teilfehler) entstehen?

**Mögliche Anschlussfragen:**
- Was ist Conditional Update / Conditional Create?
- Wie funktioniert die UUID-Auflösung in Transactions technisch?
- Was passiert, wenn Entry 5 von 10 fehlschlägt?
- Welche Performance-Implikationen haben große Transaction Bundles?
- Welche Bundle-Typen gibt es noch und wofür? (siehe [[EHR - FHIR - Bundles Document und Message]])

## Verwandt

- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - References]]
- [[EHR - FHIR - Patient Resource erstellen]]
- [[EHR - FHIR - Observation Resource erstellen]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Praxis-Hintergrund: Übungs-PDF SS23_FHIR Ressource creation.pdf, Folien 18–23 (Bundles and Transactions, Conditional Update)
