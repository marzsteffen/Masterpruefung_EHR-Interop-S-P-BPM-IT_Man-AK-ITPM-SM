---
fach: ehr
typ: vorlesung
status: offen
quelle_pdf: SS24_FHIR.pdf
datum_vorlesung: SS2024
tags:
  - fach/allgemein/ehr
  - typ/vorlesung
  - status/offen
---

# EHR - VL - FHIR Grundlagen

## Überblick

Umfassende Einführung in HL7 **FHIR** (Fast Healthcare Interoperability Resources): Motivation, Datenmodell (Resources, Data Types, Cardinality), Profile/Extensions, Resource-Granularität, Referenzen statt Nesting, RESTful API + CRUD, Search-Mechanismen, Bundles für Documents und Messages, sechs Exchange-Paradigmen und Implementation Guides. Der Vortrag positioniert FHIR als „From implementers for implementers"-Standard mit deutlichen Vorteilen gegenüber HL7 v3 / CDA.

## Lernziele (laut Vorlesung)

Implizit:
- Motivation für FHIR (Probleme mit CDA/v3) wiedergeben können
- FHIR-Resources, Data Types, Cardinality verstehen und am Patient-Beispiel erklären
- Profile, Extensions und 80/20-Regel als Anpassungs-Mechanismen kennen
- Resource-Granularität an Beispielen wie Observation (Subjective + Objective) bewerten können
- FHIR-Referenzen und ihre Vorteile gegenüber Nesting verstehen
- REST-API + CRUD beherrschen, Search anwenden können (Modifiers, Operators, Chaining)
- Bundles für Documents und Messages unterscheiden
- Die sechs Exchange-Paradigmen kennen
- Implementation Guides als praktisches Werkzeug einordnen

## Behandelte Konzepte

### Motivation und Datenmodell
- [[EHR - FHIR - Motivation]]
- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Resource Kategorien]]
- [[EHR - FHIR - Data Types und Cardinality]]
- [[EHR - FHIR - Resource Granularität]]

### Anpassung an lokale Use-Cases
- [[EHR - FHIR - Profiles und Must Support]]
- [[EHR - FHIR - Extensions und 80 20 Regel]]

### Verknüpfung von Resources
- [[EHR - FHIR - References]]

### Austausch
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - Search]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - 6 Exchange Paradigms]]

### Praxis
- [[EHR - FHIR - Implementation Guides]]

## Roter Faden

Die Vorlesung beginnt mit der Beobachtung „**75 % der Digital-Health-Companies nutzen FHIR**" und entwickelt die Motivation: CDA hat eine steile Lernkurve, ist nicht entwicklerfreundlich, HL7 v3 wird kaum für Messaging genutzt, und keiner der älteren Standards unterstützt **verteilte Information** (BP-Wert in Graz und Innsbruck zusammenführen).

FHIR macht alles, was bisher fehlte, anders: **„From implementers for implementers"**, einfache Standardszenarien, basiert auf bekannten Web-Technologien (XML, JSON, RDF, REST), frei verfügbar, mit Reference-Implementations, public Test-Servern und Starter-APIs in Java, C#, Delphi.

Das Datenmodell baut auf **Resources** (atomare Einheiten wie Patient, Observation, Practitioner) mit **Data Elements** (Felder) auf, die wiederum **Data Types** haben (primitive wie boolean oder komplex wie Identifier). **Cardinality** in min..max-Notation steuert Pflicht/Optional/Wiederholung. Resources werden zu **Categories** zusammengefasst (Foundation, Base, Clinical, Financial, Specialized).

**Lokale Anpassung** erfolgt über zwei Mechanismen: **Profiles** machen aus der internationalen Resource eine lokal eingeschränkte/erweiterte Variante (z. B. US Core Patient mit zusätzlichem race/ethnicity-Feld); **Extensions** fügen neue Datenelemente hinzu, ohne die Core-Definition zu ändern. Die **80/20-Regel** sagt: FHIR beschreibt die häufigsten 80 % der medizinischen Welt; die 20 % kulturell oder lokal bedingten Aspekte werden über Extensions abgebildet.

Ein wichtiger Designaspekt ist **References statt Nesting**: Eine Sache wird **einmal** definiert und kann **mehrfach referenziert** werden – im Gegensatz zu CDA, wo derselbe Arzt mehrfach auftauchen konnte.

Der Datenaustausch erfolgt primär per **REST-API mit CRUD** (Create/Read/Update/Delete) auf Resource-URLs. **Search** ist mit Modifiers (`:exact`, `:contains`, `:missing`), Operators (`gt`, `le`) und Chaining (Folge-Reference-Suche) sehr mächtig.

FHIR-**Bundles** binden mehrere Resources zusammen – sie können Documents (mit Composition als Root), Messages (mit MessageHeader) oder beliebige andere Sammlungen sein. **Sechs Exchange-Paradigmen** decken verschiedene Use-Cases: REST, Documents, Messaging, Services, Database/Persistence, Subscription.

Den Abschluss bilden **Implementation Guides (IGs)**: praxisnahe Bundles aus Profiles + Extensions + Beispielen + Exchange-Paradigm + Dokumentation für eine konkrete Anwendungs­domäne (US Core, AT Core, ADBM Indien, Nphies Saudi-Arabien).

## Zentrale Aussagen / Take-aways

- FHIR ist primär für Implementer designt – nicht akademisch, sondern pragmatisch.
- „Almost everything is a Resource" – kompaktes Vokabular, große Reichweite über Attribute und Coding.
- **Documents = Messages = REST-Bundles** – nur die erste Resource im Bundle bestimmt den Charakter.
- 80/20-Regel: lieber pragmatische Abdeckung als utopische Vollständigkeit.
- Implementation Guides sind das, was FHIR praktisch macht – ohne IG kein Roll-out.

## Querverweise zu anderen Vorlesungen

- [[EHR - VL - Macro-Level Interoperabilität]] – HL7 FHIR 5 Levels und USCDI als Strategie
- [[EHR - VL - CCR und CCD]] – CDA als Vorgänger; FHIR Bundle ähnelt CCD
- [[EHR - HL7 FHIR - 5 Levels]] – Schichten-Modell (Foundation, Conformance, Master Data, Operational, Knowledge)
- [[EHR - HL7 CDA - RIM-Basis]] – RIM vs. FHIR-Datenmodell-Vergleich
- [[MSI - HL7 FHIR]] – tieferer Standard-Bezug aus dem MSI-Fach
- [[MSI - HL7 FHIR - Resource]] – Detail-Ansicht aus MSI
- [[MSI - HL7 FHIR - Bundle]] – Detail-Ansicht aus MSI

## Quelle

- PDF: SS24_FHIR.pdf
- Folienanzahl: 80
- Vortragender: DI Dr. Sten Hanke
- Begleitende Notebooks: FHIRAPI.ipynb, Abgabe1.ipynb (im Übung-Ordner)
