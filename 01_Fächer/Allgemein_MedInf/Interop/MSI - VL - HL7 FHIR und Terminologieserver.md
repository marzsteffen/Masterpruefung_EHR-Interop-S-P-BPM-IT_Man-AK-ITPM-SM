---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/06_HL7 FHIR + Terminologieserver.pdf
datum_vorlesung: 2024-12-13
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - VL - HL7 FHIR und Terminologieserver

## Überblick

Vorlesung zum Terminologie-Management aus FHIR-Sicht. Drei Teile: (1) Was ist ein Terminologieserver, welche Aufgaben hat er, welche Austausch-Standards gibt es (ClaML, CTS2, IHE SVS, IHE SVCM, FHIR); (2) FHIR-Terminologie-Bausteine: codierte Datentypen (`code`, `Coding`, `CodeableConcept`), Terminology Binding mit Binding Strength (required/extensible/preferred/example), die Resources CodeSystem, ValueSet, ConceptMap, der FHIR Terminology Service mit Operationen `$expand`, `$lookup`, `$validate-code`, `$translate`; (3) IHE SVCM als FHIR-basiertes Profil und konkrete FHIR-Terminologie-Server (Ontoserver, tx.fhir.org, LOINC FHIR).

> Hinweis: PDF stammt aus WS 2023/24, ist aber die im WS 2024/25 verwendete Folie. Die Folien 1–4 sind organisatorisch (Bewertung) und werden hier nicht als Konzept erfasst.

## Lernziele (laut Vorlesung)

- Terminologieserver als Architektur-Komponente verstehen: Provider → Server → Consumer.
- Austauschstandards (ClaML, CTS2, IHE SVS, IHE SVCM, FHIR Terminology) abgrenzen.
- Codierte FHIR-Datentypen sicher unterscheiden: `code` vs. `Coding` vs. `CodeableConcept`.
- Terminology-Binding-Strength-Levels (required, extensible, preferred, example) korrekt zuordnen.
- FHIR-Terminology-Resources (CodeSystem, ValueSet, ConceptMap) und deren Bestandteile (compose, expansion, equivalence) lesen.
- FHIR-Terminology-Service-Operationen anwenden: `$expand`, `$lookup`, `$validate-code`, `$translate`.
- IHE-SVCM-Transaktionen (ITI-95 bis ITI-101) und ihre Beziehung zu den FHIR-Operationen verstehen.

## Behandelte Konzepte

### Terminologieserver – Grundlagen
- [[MSI - Terminologieserver - Definition]]
- [[MSI - Terminologieserver - Aufgaben]]
- [[MSI - Terminologieserver - Architektur]]
- [[MSI - Terminologieserver - Austauschstandards]]

### Austauschstandards für Terminologien
- [[MSI - IHE SVS - Sharing Value Sets]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]
- [[MSI - ClaML - Classification Markup Language]]

### FHIR – Codierte Datentypen
- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]
- [[MSI - HL7 FHIR - Terminology Binding Strength]]

### FHIR – Terminologie-Resources & Service
- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - Terminology Framework]]

## Roter Faden

1. Was leistet ein Terminologieserver (zentrale Bereitstellung, Synchronisation lokal ↔ zentral). → 2. Aufgaben: Anzeige/Suche, Export, Wartung, Publikation, intensionale Value-Set-Definition, Mapping. → 3. Beispiel-Architektur mit Providern (international: ICD-10, HL7, LOINC, UCUM, epSOS, TISS-28, SAPS 3; national: HL7 Österreich, PZN, APPC/BURA; kollaborativ: BMG, ELGA), Webportal/Webservices, OID-Portal, Consumer (Webservices oder Webfrontend). → 4. Standards: FHIR Terminology Resources/Operationen, ClaML (CEN/TS 14463), CTS2 (veraltet), IHE SVCM (FHIR-basiert), IHE SVS (XML/SOAP). → 5. Internationale Beispiele: Canada Infoway, SNOMED FHIR DevDays, Ontoserver. → 6. FHIR-Codierung: `code` (primitiv, required binding), `Coding` (system+code+display), `CodeableConcept` (mehrere Codings + text). → 7. Binding Strength: required, extensible, preferred, example. → 8. Terminology Service: CodeSystem (Konzepte + Definitionen + Hierarchien + Properties + Designations + Filter), ValueSet (Metadata + compose + expansion), ConceptMap (Source/Target, Group, Element, TargetElement mit equivalence). → 9. Operationen: `$expand`, `$lookup`, `$validate-code`, `$translate`. → 10. IHE SVCM: ITI-95 (Query Value Set), ITI-96 (Query Code System), ITI-97 (Expand Value Set), ITI-98 (Lookup Code), ITI-99 (Validate Code), ITI-100 (Query Concept Map), ITI-101 (Translate Code). → 11. Reale FHIR-Terminologien: Termgit ELGA, simplifier.net, Ontoserver, tx.fhir.org.

## Zentrale Aussagen / Take-aways

- **Terminologieserver = standardisierte Bereitstellung von Terminologien**: für Primärsysteme via Webservices und Endbenutzer via Webfrontend. Wesentlich: hohe Strukturierung + automatische Verarbeitbarkeit.
- **OID-Portal ergänzt Terminologieserver**: das ELGA-Beispiel zeigt OID-Register als separates System neben dem Terminologie­server.
- **FHIR `code`-Datentyp ist *required* gebunden** und braucht kein Codesystem – sicher international interoperable Werte (z. B. `gender: male`, `Bundle.type: document`).
- **`CodeableConcept` ist der Standard-Datentyp** für medizinische Codes in FHIR. Er enthält mehrere `Coding`-Elemente plus optionalen `text` als Freitext. `Coding` direkt wird selten verwendet.
- **Binding Strength entscheidet die Verbindlichkeit**: `required` (SHALL), `extensible` (SHALL, wenn ein Code passt – sonst alternate Codings/Text erlaubt), `preferred` (Empfehlung), `example` (nur Beispielwert).
- **Benson/Grieve-Zitat (Folie 36)**: „It is amazing how often everyone agrees that a coded element is essential for exchange, but there is no prospect of agreeing to a value set for said exchange." – sehr häufig bleiben Bindings nur Empfehlungen.
- **Drei Terminology-Resources**: CodeSystem (Quelle), ValueSet (Auswahl), ConceptMap (Beziehung). Dazu **Naming System** (identifiziert das Codesystem über OID/URI).
- **Vier zentrale Operationen** des FHIR Terminology Service: `$expand` (Liste der Konzepte aus einem ValueSet), `$lookup` (Details zu einem Code), `$validate-code` (Code in ValueSet?), `$translate` (Code via ConceptMap übersetzen).
- **CodeSystem-Supplements** erlauben lokale Erweiterungen eines internationalen Codesystems: zusätzliche Codes, zusätzliche Display-Werte (Übersetzungen), zusätzliche Properties (Annotationen).
- **ConceptMap ist unidirektional** und kontextabhängig (Quell- und Ziel-ValueSet). Equivalence-Werte: `relatedto | equivalent | equal | wider | subsumes | narrower | specializes | inexact | unmatched | disjoint`.
- **IHE SVCM ersetzt CTS2** als FHIR-basierter Standard und nutzt FHIR-Operationen unter ITI-Transaktionsnummern (95–101). IHE SVS ist der ältere XML/SOAP-Standard und arbeitet auf Value Sets (ITI-48 Retrieve Value Set, ITI-60 Retrieve Multiple Value Sets).

## Begleitübungen

- Folie 2 erwähnt **Übung 5** als laufende Übung im LV-Kontext. Pfad und Inhalt sind im PDF nicht weiter spezifiziert. Im Verzeichnis `Folien/Medizinische Standards und Semantische Interop/` liegt keine `INF03_Übung 5_*.pdf`, weshalb Übung 5 hier weder als eigene Quell- noch als Konzept-Note erfasst wird.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - Terminologien Anwendung]] (Code System / Value Set / Mapping in CDA-Sicht)
- [[MSI - VL - HL7 CDA und e-Befunde]] (CDA als „Vorgänger"-Encoding)
- [[MSI - VL - FHIR Starter Anna Lin]] (Vertiefung FHIR-Resourcen, JSON, REST)
- [[MSI - VL - Neues in FHIR Anna Lin]] (FHIR-Versionsdiff)
- [[MSI - openEHR - Archetypes]] (alternativer syntaktischer Ansatz – im Paper Lehne)
- [[EHR - MOC]] (Cross-Fach – Termgit ELGA als Anwendung)

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/06_HL7 FHIR + Terminologieserver.pdf`
- Folienanzahl: 37 (Folien 1–4 organisatorisch, ab Folie 5 inhaltlich)
- Vortragende: Carina Seerainer, MSc (PDF-Stand WS 2023/24, im Kurs WS 2024/25 verwendet)
- Externe Referenzen: `https://www.hl7.org/fhir/terminologies.html`, `https://www.hl7.org/fhir/terminology-service.html`, `https://termgit.elga.gv.at/`, `https://ontoserver.csiro.au/`, `https://r4.ontoserver.csiro.au/fhir`, `http://tx.fhir.org`, `https://loinc.org/fhir/`, `https://profiles.ihe.net/ITI/SVCM/index.html`, `http://wiki.ihe.net/index.php/Sharing_Value_Sets`.
