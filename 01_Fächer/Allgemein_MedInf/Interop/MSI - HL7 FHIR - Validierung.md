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

# MSI - HL7 FHIR - Validierung

> [!info] Kurzdefinition
> Die FHIR-Validierung prüft eine Ressource gegen ihre StructureDefinition via der `$validate`-Operation. Das Ergebnis ist eine `OperationOutcome`-Ressource mit Issues (Fehlern, Warnungen, Informationen).

## Beschreibung

### `$validate`-Operation

- Validierung ist eine **Operation** auf eine Ressource (nicht ein CRUD-Vorgang)
- Prüft die Ressource gegen die **StructureDefinition der Basisressource** (oder eines Profils)

**Aufruf:**
```
POST [base]/Patient/ID/$validate
{
  "resourceType": "Patient",
  ...
}
```

**Antwort (OperationOutcome):**
```json
{
  "resourceType": "OperationOutcome",
  "text": { ... },
  "issue": [{
    "severity": "information",
    "code": "informational",
    "diagnostics": "No issues detected during validation"
  }]
}
```

### OperationOutcome

- Standardisierte FHIR-Ressource für Validierungsergebnisse und Fehlerantworten
- Felder:
  - `severity`: `error` | `warning` | `information` | `fatal`
  - `code`: standardisierter Fehlertyp
  - `diagnostics`: menschenlesbare Beschreibung

## Abgrenzung

- **$validate** vs. **$evaluate**: $validate prüft Struktur und Terminologie; $evaluate (in CDS Hooks / CQL) führt klinische Logik aus.
- **Validierung** vs. **Schema-Validierung (XML/JSON Schema)**: FHIR-Validierung prüft über das Schema hinaus auch Kardinalitäten, Terminologie-Bindings und Profil-Konformität.
- **Client-seitige Validierung** vs. **Server-seitige Validierung**: `$validate` ist server-seitig. Client-seitige Validierung kann mit Bibliotheken (z. B. HAPI Validator) vor dem Senden erfolgen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie funktioniert die FHIR-Validierung und was wird zurückgeliefert?

**Anwendungsfrage:** Ein FHIR-Client schickt eine fehlerhafte Patientenressource. Wie kann er vorab prüfen, ob die Ressource valide ist?

**Diskussionsfrage:** Reicht eine strukturelle Validierung (Schema) für Interoperabilität aus? Was prüft FHIR zusätzlich? (→ Terminologie-Bindings, Profil-Konformität, Kardinalitäten)

**Mögliche Anschlussfragen:**
- Was enthält eine `OperationOutcome`-Ressource?
- Kann man eine Ressource gegen ein spezifisches Profil validieren? (→ Ja, mit Parameter `profile`)
- Welche Tools gibt es für die FHIR-Validierung? (→ HAPI Validator, Firely Validator)

## Verwandt

- [[MSI - HL7 FHIR - Operationen]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Terminology Service]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seite 77
