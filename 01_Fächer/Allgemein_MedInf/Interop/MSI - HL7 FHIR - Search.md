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

# MSI - HL7 FHIR - Search

> [!info] Kurzdefinition
> Die FHIR-Suche erfolgt via HTTP GET mit URL-Parametern. Suchparameter sind selbst FHIR-Ressourcen (SearchParameter) und können kombiniert werden. Suchergebnisse werden als Bundle vom Typ `searchset` zurückgeliefert.

## Beschreibung

### Grundform

```
GET /[Ressourcentyp]?[parameter]=[wert]
```

Beispiele:
```
GET /Patient?gender=male
GET /Patient?family=Muster&given=Hans
GET /Observation?patient=Patient/123&code=8480-6
```

- Parameter können **kombiniert** werden (AND-Verknüpfung bei mehreren Parametern)
- Ergebnis ist immer ein **Bundle vom Typ `searchset`**

### Suchparameter-Typen

Häufige Typen (im Vortrag nicht vollständig aufgelistet, im Standard definiert):
- **string**: Felder wie Name, Adresse
- **token**: Codes und Identifier (exakter Match: `system|code`)
- **reference**: Referenz auf andere Ressource
- **date**: Datumsbereiche
- **number/quantity**: Numerische Werte
- **composite**: Kombination mehrerer Felder

### SearchParameter als Ressource

- **Suchparameter sind selbst FHIR-Ressourcen** (`SearchParameter`)
- `SearchParameter` definiert: was gesucht werden kann und mit welchen anderen Parametern Kompatibilität besteht
- HAPI (populäre Java-FHIR-Implementierung) automatisiert einfache `SearchParameter`, wenn der Feldname mit dem Parameternamen übereinstimmt
- Eigene Suchparameter können erstellt und auf dem Server registriert werden
- Referenz: `http://hl7.org/fhir/searchparameter.html`

### Sonderfall: Identifier-Suche

> Wichtig (aus Übung explizit hervorgehoben): Suche nach Identifier (z. B. SVNR) ist **NICHT** dasselbe wie Suche nach ID!
```
GET /Patient?identifier=urn:oid:1.2.40.0.10|1234010190
```
vs.
```
GET /Patient/123  (direkte ID-Abfrage)
```

## Abgrenzung

- **Search (`GET ?parameter`)** vs. **Read (`GET /id`)**: Search findet Ressourcen anhand von Feldinhalten; Read ruft eine spezifische Ressource per ID ab.
- **FHIR Search** vs. **SQL/Datenbank-Query**: FHIR Search ist HTTP-basiert und über `SearchParameter`-Ressourcen konfigurierbar; keine direkte Abfragesprache wie SQL.
- **Identifier-Suche** vs. **ID-Abfrage**: Identifier ist ein fachliches Merkmal (z. B. SVNR); ID ist die technische Server-ID. Für systemübergreifende Suche immer Identifier verwenden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie funktioniert Suche in FHIR? Was wird zurückgeliefert?

**Anwendungsfrage:** Eine Apotheke sucht einen Patienten anhand der SVNR. Wie sieht der FHIR-Aufruf aus?

**Diskussionsfrage:** Warum sind Suchparameter als Ressourcen modelliert? Welche Vorteile hat das gegenüber fest codierten Suchkriterien?

**Mögliche Anschlussfragen:**
- Wie kann man nach einem Patienten über seinen Identifier suchen? (→ `?identifier=system|wert`)
- Was ist der Unterschied zwischen `GET /Patient` und `GET /Patient?_count=10`?
- Wie werden Suchparameter kombiniert (AND vs. OR)?

## Verwandt

- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Operationen]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 59, 64–66
