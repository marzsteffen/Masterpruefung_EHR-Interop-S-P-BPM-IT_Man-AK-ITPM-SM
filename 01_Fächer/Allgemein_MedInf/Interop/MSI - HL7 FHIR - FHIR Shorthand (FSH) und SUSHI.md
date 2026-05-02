---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - FHIR Shorthand (FSH) und SUSHI

> [!info] Kurzdefinition
> **FHIR Shorthand (FSH)** ist eine domänenspezifische Sprache zum Erstellen von FHIR-Profilen, Value Sets und anderen IG-Artefakten. **SUSHI** ist der Compiler, der FSH-Definitionen in valide FHIR-Ressourcen (JSON/XML) übersetzt.

## Beschreibung

Aus Seite 5:

- **FSH Specification:** `https://www.hl7.org/fhir/uv/shorthand/`
- **FSH Online Playground:** `https://fshonline.fshschool.org/`
- **SUSHI ist ein Compiler für die FHIR Shorthand Specification (FSH)**

SUSHI steht für: **S**USHI **U**nshes **S**HI (rekursives Akronym – im PDF nicht erwähnt).

Weitere Details (Syntax, Beispielcode) wurden im PDF nicht ausgeführt. Die Vorlesung beschränkt sich auf die Einführung des Konzepts und Verweise auf externe Ressourcen.

## Bestandteile / Aufbau

| Komponente | Rolle |
|---|---|
| FSH | Menschenlesbare Definitionssprache für FHIR-Artefakte (Profile, ValueSets, Instanzen) |
| SUSHI | Compiler: transformiert `.fsh`-Dateien in FHIR JSON/XML |
| IG Publisher | Baut aus den kompilierten Artefakten einen vollständigen Implementation Guide |

## Beispiel

Im PDF kein Codebeispiel. Playground: `https://fshonline.fshschool.org/`

## Abgrenzung

- **FSH ≠ StructureDefinition**: FSH ist die Autoren-Syntax; StructureDefinition ist das generierte Ergebnis.
- **SUSHI ≠ Validator**: SUSHI kompiliert FSH → FHIR; Validierung (ob die Ressource konform ist) ist ein separater Schritt.
- **FSH ≠ ART-DECOR**: ART-DECOR ist ein weiteres Template/Profiling-Werkzeug, primär für CDA. FSH ist FHIR-spezifisch.

## Prüfungsrelevanz

**Mittel** (Konzept bekannt sein, keine Syntax-Details erwartet).

**Typische Definitionsfrage:** Was ist FHIR Shorthand und was macht SUSHI?

**Anwendungsfrage:** Ein Implementierungsteam will ein AT-spezifisches Patientenprofil erstellen. Welchen Toolchain-Schritt deckt FSH/SUSHI ab?

**Diskussionsfrage:** Welche Vorteile hat FSH gegenüber dem direkten Bearbeiten von StructureDefinition-JSON?

**Mögliche Anschlussfragen:**
- In welchem Zusammenhang steht FSH zu Implementation Guides? (→ FSH ist der Authoring-Input für IGs)
- Welche anderen Profilierungs-Tools gibt es? (→ Simplifier.net, ART-DECOR für CDA)

## Verwandt

- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Implementation Guide]]
- [[MSI - HL7 CDA - ART-DECOR]]

## Quelle

- Vorlesung: [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]
- Folien/Seitenangabe: Seite 5
