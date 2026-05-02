---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR Starter (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - REST API

> [!info] Kurzdefinition
> Die FHIR REST API basiert auf HTTP und bietet standardisierte CRUD-Operationen (Create, Read, Update, Delete) sowie Search und History auf Basis der Ressourcen-URLs. Daten werden in XML oder JSON übertragen.

## Beschreibung

### XML vs. JSON

| Aspekt | XML | JSON |
|---|---|---|
| Status | Standardrepräsentation | Leichtgewichtig, für Mobile bevorzugt |
| Lesbarkeit | Leicht lesbar | Schwerer lesbar |
| Gewicht | Schwergewichtig | Leichtgewichtig |
| Anfordern via URL-Parameter | `?_format=xml` | `?_format=json` |
| Anfordern via HTTP-Header | `Accept: application/fhir+xml` | `Accept: application/fhir+json` |

### API-Operationen (CRUD)

| HTTP-Methode | Operation | URL-Pattern | Beschreibung |
|---|---|---|---|
| `GET` | Read All | `/Patient` | Alle Instanzen (returns Bundle) |
| `GET` | Read | `/Patient/{id}` | Einzelne Ressource per ID |
| `POST` | Create | `/Patient` + Body | Neue Ressource anlegen |
| `PUT` | Update | `/Patient/{id}` + Body | Ressource überschreiben |
| `DELETE` | Delete | `/Patient/{id}` | Ressource löschen (logisch) |
| `GET` | Search | `/Patient?gender=M` | Filtern nach Parametern |
| `GET` | History | `/Patient/{id}/_history` | Versionshistorie abrufen |

### History / Versionierung

- Ressourcen haben eine **Versionshistorie**
- `DELETE` erzeugt eine Tombstone-Version (logisches Löschen) – die History ist weiterhin abrufbar
- Erste Version nach DELETE liefert Status 410 Gone
- Ältere Versionen bleiben über `_history` abrufbar

### Testserver (im Vortrag verwendet)

- `http://hapi.fhir.org/baseR4` (R4 Test-Server)
- Spezifikation: `https://www.hl7.org/fhir/http.html`

## Bestandteile / Aufbau

Jede REST-Interaktion folgt dem Muster:

```
HTTP-Methode  [Base-URL]/[Ressourcentyp]/[ID][?Parameter]
```

Beispiel:
```
GET   http://hapi.fhir.org/baseR4/Patient/123
POST  http://hapi.fhir.org/baseR4/Patient      (Body: Patient-Resource in JSON)
PUT   http://hapi.fhir.org/baseR4/Patient/123  (Body: aktualisierte Patient-Resource)
DELETE http://hapi.fhir.org/baseR4/Patient/123
GET   http://hapi.fhir.org/baseR4/Patient?family=Muster&gender=male
```

## Abgrenzung

- **FHIR REST API** vs. **FHIR Operations** ($): Die REST API deckt CRUD und Search ab. Operationen (mit `$`) sind für komplexere Funktionalität (z. B. `$everything`, `$validate`) – sie sind kein Teil der Standard-CRUD-Paradigma.
- **Update (PUT)** überschreibt die gesamte Ressource – kein partielles Update (Patch). Partielles Update ist via `PATCH` möglich (im Standard definiert, aber seltener implementiert).
- **DELETE** in FHIR ist logisch (soft delete) – die History bleibt erhalten; kein physisches Löschen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche HTTP-Methoden verwendet FHIR für welche Operationen?

**Anwendungsfrage:** Wie ruft man alle Beobachtungen (Observations) eines bestimmten Patienten ab?

**Diskussionsfrage:** Was ist der Unterschied zwischen FHIR REST (CRUD) und FHIR Operations ($)? Wann braucht man Operationen?

**Mögliche Anschlussfragen:**
- Wie gibt man JSON statt XML an? (→ URL-Parameter `_format=json` oder Accept-Header)
- Was passiert bei `GET /Patient`? Was wird zurückgeliefert? (→ Bundle mit allen Patienten)
- Was ist der Unterschied zwischen PUT und PATCH in FHIR?
- Wie funktioniert die Versionshistorie? Was passiert nach DELETE?

## Verwandt

- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 FHIR - Search]]
- [[MSI - HL7 FHIR - Operationen]]
- [[MSI - HL7 FHIR - Validierung]]
- [[MSI - HL7 FHIR - SMART on FHIR]]
- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Deployment Muster]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 14, 59, 62, 67, 69
