---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR und Terminologieserver]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - Terminology Framework

> [!info] Kurzdefinition
> Das FHIR Terminology Framework beschreibt das Zusammenspiel der Terminologie-Bausteine in HL7 FHIR: CodeSystem, ValueSet, ConceptMap, Terminology Bindings und die zugehörigen Service-Operationen bilden ein kohärentes System zur semantischen Interoperabilität.

## Beschreibung

Folie 50 der Vorlesung zeigt das FHIR Terminology Framework als Überblicksdiagramm (Quelle: Gefyra GmbH 2020) ohne begleitenden Fließtext. Der Rahmen wird durch die umgebenden Folien (31–52) aufgebaut.

Das Framework besteht aus vier Schichten:

**1. Terminologie-Quellen (CodeSystem)**
Codesysteme definieren Konzepte, deren Bedeutung, Hierarchien, Display-Values und Eigenschaften. Sie stellen den „Namensraum" der Codes bereit. Beispiele: ICD-10, LOINC, SNOMED CT. Ergänzt werden sie durch CodeSystem-Supplements für lokale Erweiterungen.

**2. Auswahl und Kontextualisierung (ValueSet)**
ValueSets selektieren Codes aus einem oder mehreren CodeSystems für einen bestimmten Kontext. Sie werden intensional (über Kompositionsregeln) oder extensional (explizite Liste) definiert und zur Laufzeit expandiert. Ein FHIR-Element verweist via Terminology Binding auf ein ValueSet.

**3. Verknüpfung (ConceptMap)**
ConceptMaps beschreiben unidirektionale Mappings zwischen zwei ValueSets bzw. CodeSystems. Sie dokumentieren die Äquivalenz-Beziehung (equivalent, wider, narrower, …) und ermöglichen Code-Übersetzung zwischen Systemen.

**4. Service-Operationen (Terminology Service)**
Der FHIR Terminology Service stellt Operationen bereit, um das Framework programmatisch zu nutzen:
- `$expand` → Expansion eines ValueSets
- `$lookup` → Details zu einem Code aus einem CodeSystem
- `$validate-code` → Prüfung, ob ein Code in einem ValueSet gültig ist
- `$translate` → Übersetzung via ConceptMap

**Einbettung in Resources:**
FHIR-Datenelemente verwenden die Datentypen `code`, `Coding` und `CodeableConcept` zur Aufnahme codierter Werte. Die Verbindung zu einem ValueSet wird über das Terminology Binding mit definierten Binding Strength Levels (required, extensible, preferred, example) hergestellt.

## Bestandteile / Aufbau

| Baustein | Rolle im Framework |
|---|---|
| CodeSystem | Quelle der Codes (Konzepte, Hierarchien, Bedeutungen) |
| ValueSet | Auswahl von Codes für einen bestimmten Verwendungskontext |
| ConceptMap | Unidirektionales Mapping zwischen zwei ValueSets / CodeSystems |
| Terminology Binding | Verbindet FHIR-Ressource-Element mit einem ValueSet |
| Terminology Service | Operationen zur Laufzeitnutzung des Frameworks |
| Coding / CodeableConcept | Datentypen zur Aufnahme codierter Werte in Resources |

## Beispiel

```
CodeSystem: http://loinc.org  (definiert z. B. "8480-6" = Systolic blood pressure)
ValueSet:   http://hl7.org/fhir/ValueSet/...  (wählt relevante LOINC-Codes aus)
Observation.code → Binding: preferred → ValueSet oben
$lookup?system=http://loinc.org&code=8480-6  → liefert Details
$validate-code?url=<ValueSet>&code=8480-6   → true
```

## Abgrenzung

- Das Terminology Framework ist kein eigener FHIR-Ressource-Typ, sondern ein konzeptioneller Rahmen, der beschreibt, wie CodeSystem, ValueSet und ConceptMap **zusammenarbeiten**.
- Abzugrenzen von IHE SVCM, das dasselbe Framework über definierte Transaktionen (ITI-95–101) als Integrationsprofil spezifiziert.
- Im Gegensatz zu CTS2 (veraltet) oder IHE SVS (XML/SOAP) ist das FHIR Terminology Framework REST-basiert und direkt in die FHIR-Ressourcenwelt eingebettet.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was versteht man unter dem FHIR Terminology Framework, und welche Bausteine gehören dazu?

**Anwendungsfrage:** Ein nationales eHealth-System will SNOMED-CT-Codes für Diagnosen verwenden. Wie greifen CodeSystem, ValueSet, Binding und $validate-code zusammen?

**Diskussionsfrage:** Binding Strength `extensible` erlaubt Abweichungen, wenn kein passender Code vorhanden ist. Welche Probleme entstehen dadurch für die semantische Interoperabilität? (Benson/Grieve-Zitat: „It is amazing how often everyone agrees that a coded element is essential for exchange, but there is no prospect of agreeing to a value set for said exchange.")

**Mögliche Anschlussfragen:**
- Worin unterscheiden sich CodeSystem und ValueSet? Kann ein ValueSet ein ganzes CodeSystem enthalten?
- Was ist der Unterschied zwischen intensionaler und extensionaler ValueSet-Definition?
- Warum ist ConceptMap unidirektional – und was bedeutet das für Round-Trip-Mapping?
- Welche Binding Strength ist für nationale ELGA-Profile typisch, und warum?
- Wie verhält sich FHIR Terminology Framework gegenüber dem CDA-Ansatz (Terminology Binding in CDA vs. FHIR)?

## Verwandt

- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - Terminology Binding Strength]]
- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Mapping]]
- [[MSI - HL7 CDA - Terminology Binding]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: Folie 50 (Diagramm „FHIR Terminology Framework", Quelle: Gefyra GmbH 2020); Kontext: Folien 31–52 (gesamter FHIR-Terminologie-Block)

## Ergänzung außerhalb der Vorlesung

*Folie 50 enthält ausschließlich ein Diagramm ohne begleitenden Text. Die obige Beschreibung der vier Schichten und des Zusammenspiels der Bausteine ist eine Synthese aus den umgebenden Folien 31–52 derselben Vorlesung – kein externes Wissen.*
