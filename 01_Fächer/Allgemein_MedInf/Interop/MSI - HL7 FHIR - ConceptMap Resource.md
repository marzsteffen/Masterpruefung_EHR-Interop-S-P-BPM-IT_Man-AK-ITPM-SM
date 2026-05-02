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

# MSI - HL7 FHIR - ConceptMap Resource

> [!info] Kurzdefinition
> Eine FHIR-Resource, die die **Beziehung zwischen zwei Konzepten** (oder Datenelementen oder Klassen) beschreibt – **unidirektional** und **kontextabhängig** (Source/Target-ValueSet). Für jedes Mapping muss der **Equivalence-Typ** angegeben werden: `relatedto | equivalent | equal | wider | subsumes | narrower | specializes | inexact | unmatched | disjoint`.

## Beschreibung

Folie 43:

> „Beschreibt die Beziehung zwischen zwei Konzepten (oder Datenelementen oder Klassen)
> Unidirektionale Verbindung
> abhängig vom Kontext (=ValueSet)
> Für jedes Mapping muss der Typ angegeben werden (z. B. equivalent | equal | wider | subsumes | narrower | specializes…)"

Tabelle aus Folie 43 (TargetElement):
| Element | Card. | Type | Beschreibung |
|---|---|---|---|
| `target` | 0..* | BackboneElement | Concept in target system for element. *Rule: If the map is narrower or inexact, there SHALL be some comments* |
| `code` | 0..1 | code | Code that identifies the target element |
| `display` | 0..1 | string | Display for the code |
| `equivalence` | 1..1 | code | `relatedto | equivalent | equal | wider | subsumes | narrower | specializes | inexact | unmatched | disjoint` (ConceptMapEquivalence Required) |

Folie 44 zeigt die UML-Struktur:
- ConceptMap (DomainResource) mit Metadata, `source[x]` (uri/canonical(ValueSet)), `target[x]` (uri/canonical(ValueSet)).
- `group[0..*]`: Source/Target-Codesystem-Paar.
- `element[1..*]` pro Group: SourceElement (`code`, `display`).
- `target[0..*]` pro Element: TargetElement (`code`, `display`, `equivalence`, `comment`).
- `dependsOn`/`product`: zusätzliche Abhängigkeiten/Resultate via OtherElement (property, system, value, display).
- `unmapped[0..1]` pro Group: was passiert, wenn nichts passt (mode, code, display, url-canonical).

## Bestandteile / Aufbau

| Teil | Funktion |
|---|---|
| Metadata | url, identifier, version, status, publisher … |
| `source[x]` / `target[x]` | Source-/Target-ValueSet oder URI |
| `group` | Source-/Target-CodeSystem-Paar mit Mappings |
| `group.element` | Source-Element (code/display) |
| `group.element.target` | Target-Element mit `equivalence` |
| `group.unmapped` | Default-Fallback, wenn kein Mapping greift |

**Equivalence-Codes** (laut Folie 43):

| Code | Bedeutung |
|---|---|
| `relatedto` | irgendwie verwandt (vageste Form) |
| `equivalent` | bedeutungsäquivalent |
| `equal` | identisch |
| `wider` | Target-Konzept ist breiter |
| `subsumes` | Target-Konzept umfasst das Source-Konzept |
| `narrower` | Target-Konzept ist enger |
| `specializes` | Target-Konzept ist eine Spezialisierung |
| `inexact` | nicht exakt – Comment Pflicht |
| `unmatched` | kein passendes Target |
| `disjoint` | Konzepte schließen sich aus |

## Beispiel

Aus Folie 50 (FHIR Terminology Framework):
- Source: `263204007 |Fracture of shaft of ulna|` aus SNOMED CT.
- Target: `S52.209A "Unspecified fracture of shaft of unspecified ulna, initial encounter for closed fracture"` aus ICD-10-CM.
- Equivalence: vermutlich `wider` oder `inexact` (im PDF nicht expliziert).

## Abgrenzung

- **ConceptMap ≠ ValueSet**: ConceptMap verbindet Codes; ValueSet wählt sie aus.
- **Unidirektional ≠ symmetrisch**: ConceptMap geht in eine Richtung. Eine zweite Map ist nötig für die Gegenrichtung.
- **Equivalence ≠ Confidence**: Equivalence beschreibt die *semantische Beziehung*; Confidence (im PDF nicht behandelt) wäre ein Maß für die Sicherheit.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Was leistet die FHIR-ConceptMap-Resource? Welche Equivalence-Typen gibt es?

**Anwendungsfrage:** Wie codieren Sie ein Mapping „SNOMED `appendectomy` ist breiter als ICD-10 `K35-K38`"? (Equivalence `wider`.)

**Diskussionsfrage:** Warum ist eine ConceptMap unidirektional? Welche Probleme entstehen, wenn man sie symmetrisch interpretiert?

**Mögliche Anschlussfragen:**
- Welche FHIR-Operation nutzt die ConceptMap? (`$translate` auf ConceptMap.)
- Was passiert, wenn keiner der targets matcht? (`group.unmapped` greift.)
- Welche Cimino-Desiderata adressiert ConceptMap? (Recognize Redundancy, Multiple Consistent Views.)

## Verwandt

- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - Terminology Framework]]
- [[MSI - Terminologie - Mapping]]
- [[MSI - Terminologie - Cimino Desiderata]]

## Ergänzung aus Anna-Lin-Gastvortrag

**Mehrere Ziele und fehlende Mappings** (Seite 52):

- Mapping von Concept A kann immer **mehrere Ziele** in Concept B haben:
  - Weil mehrere gleichwertige Ziele existieren (Mehrdeutigkeit)
  - Weil Mappings Dependencies haben können
- **Nicht jedes Concept muss ein Mapping haben** – es sollte aber!

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 43, 44, 50 (06er-VL); Seite 52 (Anna Lin Starter)
