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

# EHR - FHIR - Search

> [!info] Kurzdefinition
> Die FHIR-Search-API erlaubt das Auffinden von Resources über parametrisierte HTTP-GET-Requests. Sie unterstützt **allgemeine Parameter** (für alle Resources), **resource-spezifische Parameter**, **Modifiers** (`:exact`, `:contains`, `:missing`), **Operatoren** (`gt`, `le`) und **Chaining** über mehrere Resources hinweg.

## Beschreibung

Aus den Folien 50–69:

> „Primary mechanism: GET [base]/{resourcename}?a=b
> Where:
> - [base] is the base URI, e.g. https://myfhirserver.com
> - {resourcename} is the name of the resource
> - ? is the 'where' statement
> - a=b is the query pair
>
> Example: https://myfhirserver.com/Patient?_id=1234"

## Bestandteile / Aufbau

### Allgemeine Search-Parameter (für ALLE Resources)

- `_id`, `_lastUpdated`, `_profile`, `_query`, `_security`, `_tag`, `_text`, `_filter`, `_content`

### Resource-spezifische Parameter

Jede Resource hat eigene Such-Parameter, dokumentiert in der Resource-Description. Beispiele für Patient: `name`, `family`, `given`, `gender`, `birthdate`, `identifier`, `address`.

### Search-Verhalten nach Datentyp

- **String:** „part of" (case-insensitive). `Patient?name=Williams` findet alle Patienten, deren Name „Williams" enthält.
- **Token:** exakter Match auf Code/System.
- **Date:** Datum-Vergleiche mit Operatoren.
- **Number/Quantity:** numerische Vergleiche.

### Modifiers (Folie 55)

```
Resource?parameter:modifier=term
```

| Modifier | Beispiel | Bedeutung |
|---|---|---|
| `:exact` | `Patient?given:exact=John` | exakter Match |
| `:contains` | `Patient?given:contains=ilia` | Substring |
| `:missing` | `Patient?gender:missing=true` | Feld nicht gesetzt |

### Operators (Folie 68–69)

| Operator | Beispiel | Bedeutung |
|---|---|---|
| `gt` | `Observation?value-quantity=gt100` | greater than |
| `le` | `Encounter?date=le2017-04-02` | less or equal |
| `lt`, `ge`, `eq`, `ne`, `sa` (starts after), `eb` (ends before), `ap` (approximately) | analog | numerische / zeitliche Vergleiche |

### Chaining (Folie 64)

Suche, die über References zu anderen Resources springt:
```
[base]/AllergyIntolerance?patient.name=Andrew
```
sucht alle AllergyIntolerance-Resources, deren referenzierter Patient den Namen „Andrew" hat.

### Format-Auswahl (Folie 62)

Per Parameter `_format`:
- `_format=xml`
- `_format=json`
- `_format=rdf` (nicht immer unterstützt)

### Rückgabeformat

> „When successful, the found resources are always returned as a 'Bundle' – Either as XML, JSON or RDF."

## Beispiel

HAPI FHIR Public Server (Folien 59–60):

```
# Alle Patienten mit Vornamen "Sally"
GET http://hapi.fhir.org/baseR4/Patient?given=Sally

# Alle weiblichen Patienten mit Namen "Andrew"
GET http://hapi.fhir.org/baseR4/Patient?name=Andrew&gender=female

# Patient mit ID 697701
GET http://hapi.fhir.org/baseR4/Patient/697701

# Alle Patienten geboren vor 1950
GET http://hapi.fhir.org/baseR4/Patient?birthdate=lt1950-01-01
```

Allergie-Suche mit Chain (Folie 64):
```
GET http://hapi.fhir.org/baseDstu3/AllergyIntolerance?patient.name=Andrew
```

## Abgrenzung

- **Search ≠ Read:** Read holt eine bestimmte Resource per ID; Search liefert ein Bundle mit Treffern.
- **General vs. Resource-specific Parameters:** General gelten für alle Resources, resource-specific sind aus der Resource-Definition abgeleitet.
- **Modifier ≠ Operator:** Modifier ändert das Match-Verhalten eines Parameters; Operator ist ein Wert-Präfix für Vergleiche.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie funktioniert FHIR-Search? Welche Parameter-Typen gibt es?

**Anwendungsfrage:** Schreibe eine FHIR-Search-Query, die alle Observationen mit Wert > 100 findet.

**Diskussionsfrage:** String-Search ist „part of" + case-insensitive. Wann ist das hilfreich, wann problematisch (z. B. bei kurzen Suchbegriffen)?

**Mögliche Anschlussfragen:**
- Wie funktioniert Chaining – auf welcher Tiefe ist es maximal sinnvoll?
- Was ist Reverse Chaining (`_has`)?
- Wie verhält sich ein FHIR-Server bei sehr großen Search-Ergebnissen? (Antwort: Pagination via `_count` und Bundle-Links)
- Welche Performance-Implikationen hat ein `:contains`-Modifier auf große Datenbestände?

## Verwandt

- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - References]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 50–69 (Search Mechanism, Parameters, Modifiers, Chaining, Operators, HAPI-Übungen, Format)
