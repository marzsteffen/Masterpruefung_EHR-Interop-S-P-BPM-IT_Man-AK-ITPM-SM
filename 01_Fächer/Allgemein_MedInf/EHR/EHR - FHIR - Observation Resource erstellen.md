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

# EHR - FHIR - Observation Resource erstellen

> [!info] Kurzdefinition
> Eine **Observation-Resource** beschreibt eine Messung oder Beobachtung (Vital Sign, Lab-Wert, Befund). Mindest-Pflicht: `status`, `code` (was wird beobachtet), `subject` (Reference auf den Patienten). Wert über `value[x]` (Quantity, CodeableConcept, string, …).

## Beschreibung

Observation ist eine der breitesten FHIR-Resources – sie deckt alles ab, was als Messung oder Beobachtung dokumentiert wird (siehe [[EHR - FHIR - Resource Granularität]]). Der Trick: Was beobachtet wird, steht im **`code`** (typischerweise LOINC); der Wert in **`value[x]`**.

## Bestandteile / Aufbau

### Pflicht-Felder

| Feld | Datatype | Cardinality | Inhalt |
|---|---|---|---|
| `resourceType` | string | 1..1 | Immer `"Observation"` |
| `status` | code | **1..1** | `registered` / `preliminary` / `final` / `amended` / `corrected` / `cancelled` / `entered-in-error` |
| `code` | CodeableConcept | **1..1** | Was wird beobachtet (LOINC, SNOMED CT) |

### Häufige weitere Felder

| Feld | Datatype | Bedeutung |
|---|---|---|
| `subject` | Reference(Patient) | Wer wurde beobachtet (in der Praxis fast immer gesetzt) |
| `effectiveDateTime` / `effectivePeriod` | dateTime/Period | Wann wurde gemessen |
| `value[x]` | Quantity / CodeableConcept / string / boolean / Range / Ratio / SampledData | Der Wert |
| `category` | CodeableConcept | `vital-signs`, `laboratory`, `social-history`, `imaging`, … |
| `performer` | Reference(Practitioner) | Wer hat gemessen |
| `interpretation` | CodeableConcept | normal / high / low / critical |
| `referenceRange` | BackboneElement | Normbereich |

### Typische Status-Werte

| Status | Bedeutung |
|---|---|
| `final` | Ergebnis ist final |
| `preliminary` | Vorläufig, kann sich ändern |
| `corrected` | Nach Korrektur (siehe Update-Workflow unten) |
| `amended` | Inhaltlich geändert nach Erstveröffentlichung |
| `entered-in-error` | War falsch erfasst, soll nicht mehr verwendet werden |

## Beispiel-JSON: Body Weight

```json
{
  "resourceType": "Observation",
  "status": "final",
  "category": [
    {
      "coding": [
        {
          "system": "http://terminology.hl7.org/CodeSystem/observation-category",
          "code": "vital-signs",
          "display": "Vital Signs"
        }
      ]
    }
  ],
  "code": {
    "coding": [
      {
        "system": "http://loinc.org",
        "code": "29463-7",
        "display": "Body weight"
      }
    ]
  },
  "subject": {
    "reference": "Patient/697701"
  },
  "effectiveDateTime": "2026-04-30T08:30:00+02:00",
  "valueQuantity": {
    "value": 78.5,
    "unit": "kg",
    "system": "http://unitsofmeasure.org",
    "code": "kg"
  }
}
```

### Beispiel-JSON: Blutdruck (mit Components)

Blutdruck hat zwei Werte (systolisch + diastolisch) – wird mit `component` modelliert:

```json
{
  "resourceType": "Observation",
  "status": "final",
  "code": {
    "coding": [{ "system": "http://loinc.org", "code": "85354-9", "display": "Blood pressure panel" }]
  },
  "subject": { "reference": "Patient/697701" },
  "effectiveDateTime": "2026-04-30T08:30:00+02:00",
  "component": [
    {
      "code": { "coding": [{ "system": "http://loinc.org", "code": "8480-6", "display": "Systolic blood pressure" }] },
      "valueQuantity": { "value": 130, "unit": "mmHg", "system": "http://unitsofmeasure.org", "code": "mm[Hg]" }
    },
    {
      "code": { "coding": [{ "system": "http://loinc.org", "code": "8462-4", "display": "Diastolic blood pressure" }] },
      "valueQuantity": { "value": 85, "unit": "mmHg", "system": "http://unitsofmeasure.org", "code": "mm[Hg]" }
    }
  ]
}
```

### Workflow: Observation anlegen und korrigieren

| Schritt | HTTP | Anmerkung |
|---|---|---|
| 1. Observation bauen mit `subject` → Patient-Reference | – | – |
| 2. POST | `POST [base]/Observation` | Status 201 Created |
| 3. Server vergibt ID, z. B. `obs-1`, Version 1 | – | – |
| 4. **Korrektur**: Wert ändern, `status` auf `corrected`, ID einsetzen | – | – |
| 5. PUT | `PUT [base]/Observation/obs-1` | Status 200 OK, Version 2 |
| 6. History abrufen | `GET [base]/Observation/obs-1/_history` | Bundle mit allen Versionen |

## Abgrenzung

- **Observation ≠ Condition:** Observation ist eine Messung/Beobachtung (z. B. „Husten als Symptom"); Condition ist eine Diagnose (z. B. „Pneumonie") – siehe Mapping in [[EHR - FHIR - Resource Granularität]].
- **`subject` ≠ `performer`:** subject = der Patient, performer = wer gemessen hat.
- **`effectiveDateTime` ≠ `issued`:** effective = wann gemessen, issued = wann ins System eingegeben.
- **Status nutzen, nicht löschen:** Falsche Observation auf `entered-in-error` setzen, statt DELETE – Audit Trail bleibt erhalten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Pflichtfelder hat eine FHIR-Observation? Wozu dient `code` und wozu `value[x]`?

**Anwendungsfrage:** Schreibe eine Observation für „Patient hat HbA1c 7,2 %" als JSON. Welche LOINC-Codes und Einheiten kommen zum Einsatz? (Antwort: LOINC 4548-4 oder 17856-6, UCUM `%`)

**Diskussionsfrage:** Warum hat Observation ein `status`-Feld als Pflicht und nicht z. B. einen `version`-State?

**Mögliche Anschlussfragen:**
- Wie wird Blutdruck modelliert – ein Wert oder zwei?
- Was ist der Unterschied zwischen `valueQuantity`, `valueCodeableConcept`, `valueString`?
- Wie korrigiert man eine fehlerhafte Observation? (Antwort: PUT mit `status=corrected`)
- Welche Rolle spielt `_history` für Audit?
- Was ist `entered-in-error` und warum statt DELETE?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Resource Granularität]]
- [[EHR - FHIR - References]]
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - Patient Resource erstellen]]
- [[EHR - FHIR - Transaction Bundle]]
- [[MSI - LOINC]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Praxis-Hintergrund: Übungs-PDF SS23_FHIR Ressource creation.pdf
