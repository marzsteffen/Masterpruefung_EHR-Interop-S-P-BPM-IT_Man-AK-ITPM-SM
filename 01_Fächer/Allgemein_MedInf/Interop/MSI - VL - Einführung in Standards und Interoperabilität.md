---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/01 Einführung/01_INF03-Einführung.pdf
datum_vorlesung: 2024-10-17
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - VL - Einführung in Standards und Interoperabilität

## Überblick

Konzeptionelle Einführung in das Themenfeld: Was bedeutet (semantische) Interoperabilität, welche Ebenen werden unterschieden, was sind Standards, wozu dienen sie und warum ist Interoperabilität schwer? Die Vorlesung baut den begrifflichen Rahmen auf, der in den nachfolgenden Einheiten zu Terminologien, CDA und FHIR konkret befüllt wird. Bezug auf Benson/Grieve „Principles of Health Interoperability" als Leitliteratur.

## Lernziele (laut Vorlesung)

- Verschiedene Definitionen von Interoperabilität und semantischer Interoperabilität auseinanderhalten können.
- Drei Ebenen der Interoperabilität benennen und an einem Praxisbeispiel anwenden können.
- Den Nutzen von Standards begründen können (Multiplier Effect, Vermeidung von Vendor-Lock-in, Risiko- und Kostenreduktion).
- Verstehen, warum Interoperabilität in der Praxis trotz Standards schwierig bleibt.
- Strukturierte vs. unstrukturierte Daten und gängige Datentypen unterscheiden.

## Behandelte Konzepte

### Interoperabilität – Begriff und Ebenen
- [[MSI - Interoperabilität - Definition]]
- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilitätsebenen - Technisch]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilitätsebenen - Organisatorisch]]
- [[MSI - Interoperabilitätsebenen - Benson Grieve Layer-Modell]]
- [[MSI - Interoperabilität - Voraussetzungen]]
- [[MSI - Interoperabilität - Herausforderungen]]

### Standards
- [[MSI - Standards - Definition]]
- [[MSI - Standards - Nutzen]]

### Daten und Datenaustausch
- [[MSI - Daten - DIKW-Pyramide]]
- [[MSI - Daten - Strukturiert vs Unstrukturiert]]
- [[MSI - Daten - Datentypen]]
- [[MSI - Daten - Metadaten]]
- [[MSI - Datenaustausch - Formen]]
- [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]

## Roter Faden

„Perfekte eHealth-Welt" als Vision (Folie 2) → was Interoperabilität bedeutet (Folie 4) → drei Ebenen (Folie 5) → alternative Layer-Sicht nach Benson/Grieve (Folie 6) → warum Standards überhaupt? (Folien 7–9) → Standards-Definition und Aspekte (Folie 11–12) → Daten / Information / Wissen / Handeln (DIKW, Folie 13) → strukturierte vs. unstrukturierte Daten (Folien 14–15) → Datentypen (Folie 16) → Metadaten (Folie 17) → Wege des Datenaustauschs (Folien 18–19) → Was braucht es für semantische Interoperabilität? (Folie 23) → Warum ist Interoperabilität schwer? (Folie 24) → Nutzen-Argumentation (Folie 25) → Hinweis auf Diskussions-Paper Lehne et al. 2019 (Folie 26–27).

## Zentrale Aussagen / Take-aways

- Semantische Interoperabilität = beide Seiten verstehen die Bedeutung der ausgetauschten Information; nicht jede technisch übertragbare Information ist auch maschinenverständlich.
- Standards dürfen nicht als nachträgliche Implementierungs-Entscheidung verstanden werden – die Reihenfolge ist zentral: erst Standards verstehen, dann Problem lösen, sonst entstehen Einschränkung und großer Aufwand.
- Strukturierte Daten brauchen einheitliche Datenstruktur, einheitliche Datentypen UND ein kontrolliertes Vokabular (Codesystem), damit ihre Bedeutung erhalten bleibt.
- Drei Ebenen der Interoperabilität sind ineinander verschachtelt: organisatorisch umschließt semantisch, semantisch umschließt technisch.
- „Interoperability is hard" – nicht wegen mangelnder Standards, sondern weil Computer bit-perfekt arbeiten müssen, doppelte Übersetzung nötig ist und Entwickler/Nutzer-Welten unterschiedlich sprechen.

## Begleitübung

- `INF03_Übung 1.pdf` – „Semantische Interoperabilität – ja! aber wie?" (Besprechung 24.10.2024). Wendet die hier eingeführten Begriffe auf Praxisbeispiele an. Pfad: `Folien/Medizinische Standards und Semantische Interop/01 Einführung/INF03_Übung 1.pdf`.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - Kursüberblick]]
- [[MSI - Paper - Why Digital Medicine Depends on Interoperability]] (Pflichtlektüre laut Folie 26)
- [[MSI - VL - Semantik Theorie]] (Vertiefung Terminologien)
- [[MSI - VL - HL7 CDA und e-Befunde]] (Beispiel Puls in CDA, Folie 14)
- [[MSI - VL - HL7 FHIR und Terminologieserver]]

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/01 Einführung/01_INF03-Einführung.pdf`
- Folienanzahl: 28
- Vortragende: Carina Seerainer, MSc
