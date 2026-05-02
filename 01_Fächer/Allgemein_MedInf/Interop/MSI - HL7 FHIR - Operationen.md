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

# MSI - HL7 FHIR - Operationen

> [!info] Kurzdefinition
> FHIR-Operationen (erkennbar am `$`-Präfix) erweitern die Standard-REST-API um komplexe Funktionalität, die nicht in CRUD abgebildet werden kann. Sie sind auf vier Ebenen definierbar (Endpunkt, Ressourcentyp, Instanz, Version) und werden als OperationDefinition beschrieben.

## Beschreibung

> **Hinweis**: Diese Note behandelt FHIR REST-Operationen (allgemein). Für Terminologie-Service-Operationen (`$expand`, `$lookup`, `$validate-code`, `$translate`) siehe [[MSI - HL7 FHIR - Terminology Service]].

### Erkennungsmerkmal: `$`-Präfix

```
POST http://fhir.someserver.org/fhir/Patient/1/$everything
```

- Alles mit `$` ist eine Operation
- Klare Abgrenzung von CRUD-Endpunkten

### HTTP-Methode: POST vs. GET

| Methode | Verwendung |
|---|---|
| `POST` | Operation kann Änderungen auf Ressource verursachen |
| `GET` | Idempotente Operationen (jeder Aufruf erzeugt exakt gleiches Ergebnis) oder Operationen, die Daten nicht ändern |

### Definierbare Ebenen

Operationen können auf vier verschiedenen Ebenen definiert werden:

| Ebene | URL-Pattern | Beispiel |
|---|---|---|
| **Endpunkt** | `[base]/$opName` | `$extensions` – alle Extensions am Server finden |
| **Ressourcentyp** | `[base]/Patient/$opName` | `$count` – alle Patienten zählen |
| **Instanz** | `[base]/Patient/1/$opName` | `$patientSummary` – Summary für Patient 1 |
| **Version** | `[base]/Patient/1/_history/3/$opName` | `$difference` – Vergleich zur aktuellen Version |

### OperationDefinition

- Operationen können **selbst definiert** werden
- Dazu dient die FHIR-Ressource `OperationDefinition`
- Beschreibt: Name, Ebene, Ein-/Ausgabe-Parameter, Idempotenz
- Liste bestehender Standard-Operationen: `http://hl7.org/fhir/operationslist.html`

## Bestandteile / Aufbau

```
POST [base]/Patient/1/$everything
```

Liefert: alle Ressourcen, die mit Patient 1 verknüpft sind (Observations, MedicationRequests, …) als Bundle.

## Abgrenzung

- **FHIR-Operationen ($)** vs. **REST CRUD**: CRUD ist standardisiert für Create/Read/Update/Delete von einzelnen Ressourcen. Operationen sind für komplexe Geschäftslogik, die nicht durch CRUD ausdrückbar ist.
- **Terminologie-Operationen** (`$expand`, `$lookup`, `$validate-code`, `$translate`) sind eine Unterkategorie der Operationen – sie arbeiten auf Terminologie-Ressourcen (CodeSystem, ValueSet, ConceptMap).
- **POST-Operation** vs. **POST-Create**: Bei Create via `POST /Patient` wird eine neue Ressource erzeugt; bei `POST /Patient/$validate` wird validiert (keine neue Ressource).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind FHIR-Operationen und wie erkennt man sie?

**Anwendungsfrage:** Ein System benötigt alle Gesundheitsdaten eines Patienten in einem Aufruf. Welche Operation und welche Ebene wäre geeignet?

**Diskussionsfrage:** Wann sollte man eine Operation statt CRUD verwenden? Welche Vorteile/Nachteile hat das Design als Operation?

**Mögliche Anschlussfragen:**
- Auf welchen Ebenen können Operationen definiert werden? (→ Endpunkt, Typ, Instanz, Version)
- Was ist der Unterschied zwischen GET- und POST-Operationen? (→ Idempotenz)
- Wie werden eigene Operationen definiert? (→ OperationDefinition)
- Was gibt `$everything` auf Patienteninstanz-Ebene zurück?

## Verwandt

- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - Validierung]]
- [[MSI - HL7 FHIR - Search]]
- [[MSI - HL7 FHIR - Bundle]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 71–72
