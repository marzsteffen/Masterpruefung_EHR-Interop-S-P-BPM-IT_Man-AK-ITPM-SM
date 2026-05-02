---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/02 Semantik/02_Semantik_Theorie_und_Beispiele.pdf
datum_vorlesung: 2024-10-24
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - VL - Semantik Theorie

## Überblick

Theorievorlesung zu medizinischen Ordnungssystemen, ihren Begriffen, ihrer Strukturierung (Hierarchien, Mehrachsigkeit, Prä-/Postkoordination) und Cimino's klassischen Desiderata für kontrollierte medizinische Vokabulare. Zweite Hälfte der Vorlesung führt einen Überblick über wichtige eHealth-Terminologien ein – die einzelnen Terminologien werden in der nachfolgenden Vorlesung (Terminologien Anwendung) und im Block zu HL7 FHIR + Terminologieserver detailliert.

## Lernziele (laut Vorlesung)

- Die Begriffe Objekt, Konzept, Bezeichnung, Code, Attribut, Beziehung sicher trennen können.
- Ordnungssysteme (Klassifikation, Nomenklatur, Thesaurus, Ontologie, Taxonomie, Terminologie) definieren und auf der semantischen Treppe einordnen.
- Code System vs. Value Set vs. Referenz-/Interface-Terminologie unterscheiden.
- Cimino's 11 Desiderata für kontrollierte medizinische Vokabulare benennen und an Beispielen anwenden.
- Hierarchie-Typen (mono- vs. polyhierarchisch), Mehrachsigkeit und Prä-/Postkoordination an konkreten Beispielen (APPC, SNOMED CT) erklären.
- Wichtige eHealth-Terminologien überblicksartig benennen und begründen, wozu Terminologien insgesamt nötig sind.

## Behandelte Konzepte

### Begriffsfundament
- [[MSI - Begriff - Synonyme Homonyme Eponyme]]
- [[MSI - Begriff - Konzept Bezeichnung Code]]

### Ordnungssysteme – Typen und Treppe
- [[MSI - Ordnungssystem - Konzeptdomäne]]
- [[MSI - Ordnungssystem - Klassifikation]]
- [[MSI - Ordnungssystem - Nomenklatur]]
- [[MSI - Ordnungssystem - Thesaurus]]
- [[MSI - Ordnungssystem - Ontologie]]
- [[MSI - Ordnungssystem - Taxonomie]]
- [[MSI - Ordnungssystem - Semantische Treppe]]

### Terminologie – Bausteine
- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Vokabular und kontrolliertes Vokabular]]
- [[MSI - Terminologie - Mapping]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Referenz vs Interface Terminologie]]

### Anforderungen, Strukturen, Cimino
- [[MSI - Terminologie - Anforderungen]]
- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - Mehrachsigkeit]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]

### Wozu und welche
- [[MSI - Terminologie - Funktionen]]
- [[MSI - Terminologie - Pflegediagnose vs ärztliche Diagnose]]

## Roter Faden

Begriffliche Fundierung (Eigennamen/Homonyme/Synonyme/… zeigen, warum Ordnungssysteme nötig sind) → Begriffsklärung Objekt/Begriff/Bezeichnung/Code → Typologie der Ordnungssysteme (Konzeptdomäne, Klassifikation, Nomenklatur, Thesaurus, Ontologie, Taxonomie) → semantische Treppe als ranking → Terminologie als computer­verarbeitbare Sammlung → Code System / Value Set / Referenz-Interface → Anforderungen an Ordnungssysteme → Cimino's Desiderata (klassisches Paper, hier vollständig durchgearbeitet) → Hierarchie-Typen, Mehrachsigkeit, Prä-/Postkoordination → Auswahl-Liste eHealth-Terminologien → Quartett-Übung → Pflege- vs. ärztliche Diagnosen → „Wozu Terminologien?".

## Zentrale Aussagen / Take-aways

- Eine Konzeptdomäne (z. B. „Diagnosen") kann durch *mehrere* Terminologien abgedeckt werden (ICD-9, ICD-10, ICD-10-GM …) – Wahl ist Anwendungsfrage, nicht ontologisch fix.
- Auf der semantischen Treppe (Glossar → Nomenklatur → Klassifikation → Thesaurus → Ontologie) wächst der Grad der inneren Strukturierung und Vernetzung – Ontologie ganz oben.
- Code System enthält Codes mit Regeln, Value Set ist eine versionierte Sicht über 1–n Terminologien.
- Cimino (1998) verlangt explizit **non-semantic concept identifiers** – Codes sollen keine Bedeutung tragen (Diskussionsanker für Vergleich z. B. APPC, ICD-10).
- Postkoordination erlaubt das Codieren medizinischer Ausdrücke, für die noch keine SCTID existiert – die Stärke von SNOMED CT.
- Disjunktheit ist eine zentrale Anforderung: „Sonstiges"-Konzepte sind problematisch (Cimino, „Rejection of Not Elsewhere Classified").

## Begleitübung

- `INF03_Übung 2_semantic.pdf` – „Semantic Dashboard" (Einstieg laut Folie 2 dieser VL, Besprechung 14.11.2024). Pfad: `Folien/Medizinische Standards und Semantische Interop/02 Semantik/INF03_Übung 2_semantic.pdf`. Ergänzende Übung „Terminologie-Quartett" (Folie 26): Recherche zu einer eHealth-Terminologie als Steckbrief (Hierarchischer/mehrachsiger Aufbau, internationale Verbreitung, Wichtigkeit, „Superkraft").

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - Einführung in Standards und Interoperabilität]]
- [[MSI - Paper - Cimino Desiderata]] (Vertiefung des klassischen Originalpapers)
- [[MSI - VL - Terminologien Anwendung]] (Vertiefung der eHealth-Terminologien)
- [[MSI - VL - HL7 FHIR und Terminologieserver]] (FHIR-Terminologie-Resources, Code System / Value Set in FHIR)

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/02 Semantik/02_Semantik_Theorie_und_Beispiele.pdf`
- Folienanzahl: 30
- Vortragende: Carina Seerainer, MSc
- Externe Referenzen laut Folien: Cimino JJ (1998) Desiderata for Controlled Medical Vocabularies; HL7-Glossar `https://hl7.at/hl7-glossar/`; Termgit ELGA `https://termgit.elga.gv.at/`.
