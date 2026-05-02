---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: "2024-12-06-Neues-in-FHIR.pdf"
datum_vorlesung: 2024-12-06
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - VL - Neues in HL7 FHIR (Anna Lin)

## Überblick

Zweite Gastvorlesungseinheit von Anna M. Lin (2024-12-06) mit Überblick über fortgeschrittene FHIR-Themen: FhirPath als Abfragesprache, Implementation Guides und Profilierungswerkzeuge (FSH/SUSHI), SMART on FHIR Scopes, CDS Hooks, Clinical Quality Language (CQL) und das Questionnaire/SDC-Ökosystem. Die Vorlesung ist knapp und verweist stark auf externe Spezifikationen und Playgrounds. Die HAPI-Übungsaufgaben (Seiten 1 und 3) wurden nicht verarbeitet.

## Lernziele (laut Vorlesung)

- FhirPath als Abfragesprache für FHIR-Ressourcen kennen
- Implementation Guides lesen; Differential Table vs. Snapshot Table verstehen
- FHIR Shorthand (FSH) und SUSHI als Profilierungswerkzeuge kennen
- SMART on FHIR Scopes für die Zugriffskontrolle verstehen
- CDS Hooks als Trigger-basiertes klinisches Entscheidungsunterstützungssystem kennen
- CQL als wiederverwendbare Ausdruckssprache für Qualitätsmetriken kennen
- Questionnaires und das SDC-Implementierungsleitfaden-Ökosystem kennen

## Behandelte Konzepte

### Abfragesprache
- [[MSI - HL7 FHIR - FhirPath]]

### Profilierung & Implementation Guides
- [[MSI - HL7 FHIR - Implementation Guide]]
- [[MSI - HL7 FHIR - FHIR Shorthand (FSH) und SUSHI]]

### Sicherheit
- [[MSI - HL7 FHIR - SMART on FHIR]] (Ergänzung: Scopes)

### Klinische Entscheidungsunterstützung
- [[MSI - HL7 FHIR - CDS Hooks]]
- [[MSI - HL7 FHIR - CQL]]

### Formulare & strukturierte Datenerfassung
- [[MSI - HL7 FHIR - Questionnaire und SDC IG]]

## Roter Faden

Die Vorlesung erweitert die grundlegende FHIR-Einführung um praxisrelevante Werkzeuge und Ökosysteme: Wie navigiert man FHIR-Ressourcen programmatisch (FhirPath)? Wie erstellt und verteilt man Profile (FSH/SUSHI, IGs)? Wie sichert man den Zugriff granular ab (SMART Scopes)? Wie bindet man klinische Logik an FHIR-Events (CDS Hooks, CQL)? Wie erfasst man strukturierte Daten über Formulare (SDC)?

## Zentrale Aussagen / Take-aways

- FhirPath ist die Standard-Navigationssprache für FHIR-Ressourcen (analog zu XPath für XML).
- FSH/SUSHI senkt die Einstiegshürde für die Erstellung von Implementation Guides deutlich.
- SMART Scopes (Format: `[context]/[Ressourcentyp].[operation]`) ermöglichen granulare OAuth2-Zugriffsrechte.
- CDS Hooks verbinden FHIR-Server mit externer Entscheidungslogik über standardisierte Trigger.
- CQL ist die gemeinsame Sprache hinter Qualitätsmessungen und CDS-Logik.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - HL7 FHIR Starter (Anna Lin)]] (Grundlagen)
- [[MSI - VL - HL7 FHIR und Terminologieserver]] (Terminologie-Aspekte)

## Quelle

- PDF: `2024-12-06-Neues-in-FHIR.pdf`
- Folienanzahl: 9 (davon 2 HAPI-Übungsseiten übersprungen)
- Vortragende: Anna M. Lin
