---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/HL7 FHIR Anna Lin/2024-12-05-FHJ-FHIR-Starter.pdf
datum_vorlesung: 2024-12-05
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - VL - HL7 FHIR Starter (Anna Lin)

## Überblick

Gastvortrag (FHIR-Workshop) von Anna M. Lin, MSc (Assistenzprofessorin, FH OÖ Campus Hagenberg). Kompakter Einstieg in HL7 FHIR: Paradigmen im Gesundheitsbereich, FHIR-Definition und Versionierung, Ressourcen-Struktur (Identity, Metadaten, Narrative, Typen, Elemente, Reference, Extensions), Terminologie in FHIR (Codes, ValueSets, Profile), REST API (CRUD, Search, History, Operationen) sowie Sicherheits- und Deployment-Aspekte.

> Gastvortrag im Rahmen von INF03, WS 2024/25. Inhalte basieren auf HL7-Austria-Workshop-Materialien von Andreas Schuler und Oliver Krauss.

## Lernziele (laut Vorlesung)

- Paradigmen in Gesundheitsstandards abgrenzen: nachrichtenbasiert, dokumentenbasiert, anwendungsspezifisch, ressourcenbasiert.
- FHIR als Standard einordnen: Eigenschaften, 80/20-Regel, Versionen (R4/R5), Stärken und Schwächen.
- Aufbau einer FHIR-Ressource verstehen: ID vs. Identifier vs. Identity, Metadaten, Narrative, DomainResource vs. Resource.
- Strukturelle Bausteine kennen: Elemente, Datentypen, Kardinalitäten, Reference-Typen, Contained Resources, Extensions.
- REST-API beherrschen: CRUD-Operationen, Search, History, Custom Operations.
- Profile und Terminologie verstehen: Codes, ValueSets, Bindings, Profil-Konzept, Deployment-Muster.

## Behandelte Konzepte

### FHIR – Grundlagen
- [[MSI - HL7 FHIR - Paradigmen]]
- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - Versionen]]

### FHIR – Ressourcen-Struktur
- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Ressourcentypen]]
- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - Element]]
- [[MSI - HL7 FHIR - Reference]]
- [[MSI - HL7 FHIR - Extension]]

### FHIR – Terminologie (Ergänzung zu 06er-VL)
- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]] *(ergänzt: Quantity)*
- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]
- [[MSI - HL7 FHIR - ValueSet Resource]] *(ergänzt: Composition-Details)*
- [[MSI - HL7 FHIR - ConceptMap Resource]] *(ergänzt: Nuancen)*
- [[MSI - HL7 FHIR - Terminology Binding Strength]]

### FHIR – Profil & Deployment
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Deployment Muster]]

### FHIR – REST API
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 FHIR - Search]]
- [[MSI - HL7 FHIR - Operationen]]
- [[MSI - HL7 FHIR - Validierung]]

### FHIR – Sicherheit
- [[MSI - HL7 FHIR - SMART on FHIR]]

## Roter Faden

1. **Kontextualisierung**: Wo steht FHIR im Paradigmen-Vergleich? Ressourcenbasiert vs. Nachrichten- / Dokumenten-basiert. Vorteile (leichtgewichtig, modular) und Nachteile (kein Gesamtüberblick, kein Prozessmodell). → 2. **Was ist FHIR?** Definition, 80/20-Regel, Open Source, Entwickler-Fokus, moderne Technologien. → 3. **Versionierung**: R4 normativ und abwärtskompatibel, R5 aktuell. → 4. **Aufbau einer Ressource**: generelle Struktur (Diagramm), DomainResource/Resource-Hierarchie, ID vs. Identifier vs. Identity, Metadaten, Narrative (Invers zu CDA: Narrative ist Zusatz, kein Primärinhalt). → 5. **Elemente und Datentypen**: primitive und komplexe Typen, Backbone, Kardinalitäten, Choice Elements, Reference (absolut/relativ/kanonisch/contained). → 6. **Extensions**: URL-basiert, alleinstehend oder profilgebunden. → 7. **Terminologie**: die 4 Code-Typen (code, Coding, CodeableConcept, Quantity), ValueSet vs. CodeSystem, Composition-Regeln, Expansion, ConceptMap, Binding Strength. → 8. **Profile**: Zweck, StructureDefinition, Veröffentlichung über Simplifier.net. → 9. **REST API**: CRUD, Search, History, Custom Operations ($). → 10. **Sicherheit**: SMART on FHIR = OAuth2, Auditing (AuditEvent, Provenance, Consent). → 11. **Deployment**: Facade vs. Server; ohne Profile keine echte Interoperabilität.

## Zentrale Aussagen / Take-aways

- **FHIR ist ressourcenbasiert** – atomic, unabhängig änderbar, leichtgewichtig. Kein Gesamtüberblick ohne FHIR Documents/Bundles.
- **80/20-Regel**: 80 % der UseCases out-of-the-box, 20 % durch Profilierung abgedeckt.
- **Seit R4 gibt es normative Ressourcen** – diese sind abwärtskompatibel und ändern sich nur noch selten. Empfehlung: immer die neueste Version.
- **ID ≠ Identifier ≠ Identity**: ID ist serverlokal, Identifier ist systemübergreifend (z. B. SVNR), Identity ist die globale URI.
- **Metadaten werden nur vom Server verwaltet** (versionId, lastUpdated, source, profile, security, tag).
- **Narrative ist Pflicht (soll), aber nicht primär** – im Gegensatz zu CDA, wo der narrative Teil die Primärquelle ist.
- **Contained Resources sind (fast immer) ein Anti-Pattern** – besser Bundles oder FHIR Documents verwenden.
- **FHIR Server ≠ Interoperabilität**: ohne Profilierung und Implementation Guides bleibt FHIR ein leerer Standard.
- **SMART on FHIR = OAuth2**: Sicherheit ist nicht Teil der FHIR-API, aber essenziell empfohlen.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - HL7 FHIR und Terminologieserver]] (Terminologie-Fokus; komplementär zum Starter)
- [[MSI - VL - HL7 CDA und e-Befunde]] (Vergleich CDA ↔ FHIR: Narrative, Struktur, Paradigma)
- [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]] (Folgevorlesung: FhirPath, IGs, SUSHI, CDS Hooks)
- [[EHR - MOC]] (Cross-Fach: FHIR als Basis für ELGA-Anwendungen, IPS)

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/HL7 FHIR Anna Lin/2024-12-05-FHJ-FHIR-Starter.pdf`
- Folienanzahl: 81
- Vortragende: Anna M. Lin, MSc (Assistenzprofessorin, Medizin- und Bioinformatik, FH OÖ Campus Hagenberg)
- Dank/Basis: Workshop-Materialien von Andreas Schuler und Oliver Krauss (HL7 Austria)
- Testserver im Vortrag: http://hapi.fhir.org/baseR4
