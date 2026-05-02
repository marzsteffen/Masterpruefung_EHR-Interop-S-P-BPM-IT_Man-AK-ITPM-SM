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

# MSI - HL7 FHIR - Ressource Identity

> [!info] Kurzdefinition
> FHIR unterscheidet drei Identifikations-Konzepte: `ID` (server-lokale technische Nummer), `Identity` (globale URI = Endpunkt + Typ + ID) und `Identifier` (logische, systemübergreifende Identifikation wie SVNR oder Patientennummer). Sie werden häufig verwechselt.

## Beschreibung

### ID

- Technische **Identifikationsnummer am Server**
- Teil der Identity
- Serverlokal: dieselbe Ressource kann auf verschiedenen Servern unterschiedliche IDs haben
- Beispiel: `Patient/123` → ID ist `123`

### Identity

- **Eindeutige globale URI** einer Ressource
- Setzt sich zusammen aus: `FHIR-Endpunkt + Ressourcentyp + ID`
- Beispiel: `http://hapi.fhir.org/baseR4/Patient/123`
- Bleibt stabil, solange die Ressource am selben Server liegt

### Identifier

- **Logische Identifikation** einer Ressource in anderen Systemen (außerhalb des FHIR-Servers)
- Eigenes Feld in vielen Ressourcen (`Patient.identifier`, `Observation.identifier`, …)
- In der Regel **mehr als ein Identifier** pro Ressource (z. B. SVNR, lokale Patientennummer, GKK-Nummer)
- Beispiel: Sozialversicherungsnummer (SVNR) = `Identifier`

> **Häufiger Irrtum in FHIR-Tutorials**: Viele stellen fälschlicherweise den `Identifier` als die eindeutige Identifikation der Ressource dar. Das ist falsch – die technische Identifikation am Server ist die `ID` (Teil der Identity). Der `Identifier` dient der fachlichen Identifikation in externen Systemen.

## Bestandteile / Aufbau

| Konzept | Typ | Scope | Beispiel |
|---|---|---|---|
| `ID` | Technisch | Serverlokal | `123` |
| `Identity` | Technisch | Global (URI) | `http://server/fhir/Patient/123` |
| `Identifier` | Fachlich | Systemübergreifend | SVNR `1234010190` |

## Abgrenzung

- `ID` ist **nicht stabil** bei Server-Migration – wenn eine Ressource auf einen anderen Server verschoben wird, ändert sich die ID.
- `Identifier` bleibt stabil, weil er unabhängig vom Server ist (z. B. SVNR ändert sich nicht beim Serverwechsel).
- `Identity` ist stabil, solange dieselbe Server-URL verwendet wird.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen `ID`, `Identity` und `Identifier` in FHIR?

**Anwendungsfrage:** Ein Patient hat eine Sozialversicherungsnummer und eine interne Krankenhausnummer. Wie würde man diese in FHIR abbilden?

**Diskussionsfrage:** Warum ist der Identifier für systemübergreifende Interoperabilität wichtiger als die ID? Welche Probleme entstehen, wenn man nur auf die ID setzt?

**Mögliche Anschlussfragen:**
- Wie sucht man in FHIR nach einem Patienten anhand des Identifiers (nicht der ID)? (→ `GET /Patient?identifier=...`)
- Was passiert mit der ID, wenn eine Ressource auf einen neuen Server migriert wird?
- Kann eine Ressource mehrere Identifier haben? (→ Ja, idR mehrere: SVNR + lokale PatID + …)

## Verwandt

- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Search]]
- [[MSI - HL7 CDA - II Instance Identifier]]
- [[MSI - Identifikator - OID]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 18, 21
