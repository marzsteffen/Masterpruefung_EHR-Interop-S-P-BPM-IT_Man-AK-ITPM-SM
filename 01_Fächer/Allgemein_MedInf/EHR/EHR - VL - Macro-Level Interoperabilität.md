---
fach: ehr
typ: vorlesung
status: offen
quelle_pdf: FH Joanneum. Graz. Macro-level e-health 2025.pdf
datum_vorlesung: 2025
tags:
  - fach/allgemein/ehr
  - typ/vorlesung
  - status/offen
---

# EHR - VL - Macro-Level Interoperabilität

## Überblick

Gastvortrag von Janek Metsallik (Tallinn University of Technology, TalTech) zu Makro-Ebene-Interoperabilität in eHealth. Entwickelt aus einer fortlaufenden Patienten-Story („Martin", 51, Präventionsplanung) eine systemische Sicht auf Entscheidungsfindung, Datenherkunft und Datennutzung. Stellt Frameworks vor (Zachman, Tolk LCIM, ContSys/ISO 13940, ISO 23903, MITRE HISCF, FHIR-Level-Modell) und diskutiert Datensharing-Logiken sowie das European Health Data Space (EHDS).

## Lernziele (laut Vorlesung)

Das PDF formuliert keine expliziten Lernziele. Implizit ergibt sich:
- Macro/Meso/Micro-Ebenen integrierter Versorgung benennen können
- Interoperabilitätsschichten (Tolk LCIM) auf Gesundheitsdaten anwenden
- Governance-Rollen im Datensharing identifizieren
- ContSys (ISO 13940) als ontologisches Backbone für Datenanforderungen einordnen
- HL7 FHIR-Level-Modell und MITRE-Maturity-Modell als Bewertungsraster nutzen
- EHDS als europäisches Programm einordnen

## Behandelte Konzepte

### Konzeptueller Rahmen
- [[EHR - Integrated Care - Macro Meso Micro Level]]
- [[EHR - Methodik - Zachman Framework]]
- [[EHR - Interoperabilität - LCIM nach Tolk]]

### Daten und Indikatoren
- [[EHR - Indikatoren - WHO 100 Core Health Indicators]]
- [[EHR - Datensharing - Logic Modes]]

### Standards und Referenzmodelle
- [[EHR - ContSys - ISO 13940]]
- [[EHR - HL7 FHIR - 5 Levels]]
- [[EHR - Architektur - ISO 23903 3D]]

### Governance und Capabilities
- [[EHR - Governance - Data Sharing Rollen]]
- [[EHR - eHealth Capabilities - Information Flows]]
- [[EHR - Maturity Model - MITRE HISCF]]

### Strategische Initiativen
- [[EHR - EHDS - European Health Data Space]]

## Roter Faden

Der Vortrag beginnt mit der Definition **integrierter Versorgung** auf drei Ebenen (Macro/Meso/Micro nach Shaw et al., 2017) und stellt dann eine konkrete Patienten-Story vor: „Martin", 51 Jahre, will einen persönlichen Präventionsplan entwickeln. An Martins Entscheidungspunkten wird das **Zachman-Framework** (Who/Why/How/What/Where/When) angewendet.

Aus der Story ergibt sich die Frage, wie Martins persönliche Daten mit den Daten der Gesundheitsversorgung zusammenfinden. Hier kommt **Tolks LCIM** (2003) ins Spiel mit den Schichten Technical Integration → Syntax/Semantik → Process Composability.

Anschließend zeigt der Vortrag, wie staatliche Gesundheits-Stellen Indikatoren erheben (am Beispiel **WHO Tobacco Use Indicator SDG 3.a.1**) und welche Spannungsfelder zwischen Datenangebot und -nachfrage entstehen. Es folgt eine Typologie der **Data-Sharing-Logiken** (transactional / shared registries / informational).

Standards werden eingeführt: **ContSys (ISO 13940)** als ontologisches Backbone, **HL7 FHIR** mit seinen 5 Inhaltsschichten, **ISO 23903** als 3D-Referenzarchitektur (Viewpoint, Composition, Domains).

Auf Governance-Ebene führt der Vortrag explizite **Rollen** ein (Data Provider, Steward, Custodian, Consumer, Policy Owner/Controller). Das **MITRE Health Information Sharing Capability Framework** liefert ein Maturity-Modell mit 11 Capabilities × 6 Purposes (Empowering, Clinical, Management, Research, Policy, Funding).

Den Abschluss bilden ein Hinweis auf das **European Health Data Space (EHDS)** und eine „Cartography"-Übung, in der Studierende für eine konkrete Vision Akteure, Daten und Systeme kartieren.

## Zentrale Aussagen / Take-aways

- Interoperabilität auf Makro-Ebene ist **mehr als Datenformat-Kompatibilität** – sie umfasst Prozess-Komposabilität und Governance.
- ContSys (ISO 13940) wird als „ontologisches Backbone" propagiert: ohne ein gemeinsames Konzeptsystem keine echte Mehrfachnutzung von Daten.
- Daten-Mehrfachnutzung (multiple use of data) erfordert die **Trennung von Erfassung (Capture), Verwahrung (Custody) und Nutzung (Use)** – und entsprechende Governance-Rollen.
- Punkt-zu-Punkt-Datenaustausch ist immer noch Realität – das Ziel ist „Diverse, High agility, Fundamental multipurpose, Dynamic standards" (informational mode).
- HL7 FHIR liefert Schichten von Daten-Encoding bis Knowledge Sharing – moderne EHRs nutzen alle 5 Ebenen.
- MITRE-Maturity zeigt: Sicherheit (Security) ist meist hoch entwickelt, Datenqualität und Sustainability hinken nach.

## Querverweise zu anderen Vorlesungen

- [[EHR - VL - Einführung und Definitionen]] – grundsätzliche Anforderungen, die hier auf Makro-Ebene gehoben werden
- [[EHR - VL - FHIR Grundlagen]] – das FHIR-Level-Modell wird hier strategisch eingeordnet
- [[MSI - MOC]] – HL7 FHIR, SNOMED, ICD, ATC, LOINC als Bausteine in der LCIM-Schichtung
- [[ASP - MOC]] – Consent, Privacy, Security als Bestandteile des MITRE HISCF

## Quelle

- PDF: FH Joanneum. Graz. Macro-level e-health 2025.pdf
- Folienanzahl: ca. 35 (Foliennummerierung im PDF nicht explizit)
- Vortragender: Janek Metsallik (E-Health Architect, TalTech, Estonia)
