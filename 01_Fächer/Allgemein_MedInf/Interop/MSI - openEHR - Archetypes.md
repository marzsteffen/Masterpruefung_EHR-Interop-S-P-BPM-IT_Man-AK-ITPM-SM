---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - Paper - Why Digital Medicine Depends on Interoperability]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - openEHR - Archetypes

> [!info] Kurzdefinition
> openEHR ist eine Initiative zum strukturierten Austausch von Gesundheitsdaten. Sie erlaubt es klinischen Fachpersonen und IT-Experten, klinische Inhalte über sogenannte **Archetypes** zu definieren – Spezifikationen klinischer Konzepte, die auf einem zugrundeliegenden Referenz-Modell aufbauen.

## Beschreibung

Wörtlich aus Lehne et al. (2019), Sektion „Syntactic interoperability":

> „Another initiative to improve the structured exchange of health data is openEHR. OpenEHR allows medical professionals and health IT experts to define clinical content using so-called archetypes, specifications of clinical concepts based on an underlying reference model. OpenEHR includes a portable language for querying, the Archetype Querying Language (AQL), as well as tools for defining and publishing the archetypes."

> Hinweis Quelltreue: Die genaue Modellarchitektur, Versions-/Standardisierungsstand (z. B. ISO 13606) und Vergleich zu FHIR werden im Paper **nicht** ausgearbeitet.

## Bestandteile / Aufbau

Aus dem Paper:
- **Reference Model** als Basis – im Paper nicht weiter spezifiziert.
- **Archetypes** – Spezifikationen klinischer Konzepte auf Basis des Reference Models.
- **AQL (Archetype Querying Language)** – portable Abfragesprache.
- **Tools** zum Definieren und Publizieren der Archetypes.

## Beispiel

Im Paper kein konkretes openEHR-Beispiel ausgeführt.

## Abgrenzung

- **openEHR vs. HL7 FHIR**: Beide adressieren laut Paper die syntaktische Schicht für strukturierten Gesundheitsdaten-Austausch, aber mit unterschiedlichen Architekturen (FHIR: Resource-Set + REST; openEHR: Reference Model + Archetypes + AQL). Das Paper stellt sie als parallele Initiativen vor, ohne explizite Wertung.
- **openEHR ≠ EHR-System.** openEHR ist eine Spezifikation, kein Produkt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind openEHR-Archetypes, und worauf bauen sie auf?

**Anwendungsfrage:** Wofür ist AQL gedacht, und worin unterscheidet es sich von FHIR-Search?

**Diskussionsfrage:** FHIR und openEHR – konkurrierend oder komplementär? (Im Paper als parallel beschrieben; vertiefend siehe [[MSI - VL - HL7 FHIR und Terminologieserver]].)

**Mögliche Anschlussfragen:**
- Was ist das openEHR Reference Model? (Im Paper nicht definiert.)
- Welche Standardisierungs-Pfade hat openEHR? (Im Paper nicht behandelt.)
- Welche Verbreitung hat openEHR im DACH-Raum? (Im Paper nicht behandelt.)

## Verwandt

- [[MSI - Interoperabilitätsebenen - Syntaktisch]]
- [[MSI - HL7 FHIR - Resource]] (alternative Spezifikation)
- [[MSI - Interoperabilität - Anwendungsbereiche Lehne]]

## Quelle

- Vorlesung: [[MSI - Paper - Why Digital Medicine Depends on Interoperability]]
- Folien/Seitenangabe: Sektion „Syntactic interoperability", S. 2 des Papers
