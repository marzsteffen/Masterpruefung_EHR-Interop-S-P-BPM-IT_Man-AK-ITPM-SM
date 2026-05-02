---
fach: msi
typ: moc
status: offen
tags:
  - fach/allgemein/msi
  - typ/moc
  - status/offen
---

# MSI - MOC

> [!info] Map of Content – Medizinische Standards und Semantische Interoperabilität

## Beschreibung des Fachs

Standards für den Austausch und die semantische Verknüpfung medizinischer Daten: HL7 v2, HL7 CDA, HL7 FHIR, IHE-Profile, Terminologien (SNOMED CT, LOINC, ICD), Interoperabilitätsebenen.

## Vorlesungen

- [[MSI - VL - Kursüberblick]]
- [[MSI - VL - Einführung in Standards und Interoperabilität]]
- [[MSI - Paper - Why Digital Medicine Depends on Interoperability]] (Lehne et al. 2019)
- [[MSI - VL - Semantik Theorie]]
- [[MSI - Paper - Cimino Desiderata]] (Cimino 1998 – vollständige 12 Desiderata)
- [[MSI - VL - Terminologien Anwendung]]
- [[MSI - VL - HL7 CDA und e-Befunde]]
- [[MSI - VL - HL7 FHIR und Terminologieserver]]
- [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]

## Themenbereiche

### HL7-Familie
- [[MSI - Datenaustausch - Formen]] (Übersicht: Nachrichten / Dokumente / Ressourcen)
- [[MSI - Standards - Definition]]
- [[MSI - Standards - Nutzen]]
- [[MSI - HL7 - International Patient Summary]]
- [[MSI - openEHR - Archetypes]] (alternativer syntaktischer Ansatz)

#### HL7 CDA – Grundlagen
- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 RIM - Reference Information Model]]
- [[MSI - HL7 CDA - R-MIM]]
- [[MSI - HL7 CDA - Eigenschaften]]
- [[MSI - HL7 CDA - Header]]
- [[MSI - HL7 CDA - Body und Sections]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - ELGA - EIS Stufen]]

#### HL7 CDA – Datentypen, Identifikatoren, Codierung
- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - HL7 CDA - II Instance Identifier]]
- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - Terminology Binding]]
- [[MSI - HL7 CDA - nullFlavor]]

#### HL7 CDA – Praxis & Leitfäden
- [[MSI - HL7 CDA - Stylesheet und Validierung]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - ART-DECOR]]
- [[MSI - HL7 CDA - Kardinalität und Konformität]]

#### HL7 CDA – Maschinenlesbare Daten
- [[MSI - HL7 CDA - Laborparameter Entry]]
- [[MSI - HL7 CDA - Problem-Bedenken Entry]]
- [[MSI - HL7 CDA - Medikation Entry]]
- [[MSI - HL7 CDA - Translation]]

#### HL7 FHIR – Grundlagen
- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - Paradigmen]]
- [[MSI - HL7 FHIR - Versionen]]

#### HL7 FHIR – Ressourcen-Struktur
- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Ressourcentypen]]
- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - Element]]
- [[MSI - HL7 FHIR - Reference]]
- [[MSI - HL7 FHIR - Extension]]

#### HL7 FHIR – REST API & Abfrage
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 FHIR - Search]]
- [[MSI - HL7 FHIR - Operationen]]
- [[MSI - HL7 FHIR - Validierung]]
- [[MSI - HL7 FHIR - FhirPath]]

#### HL7 FHIR – Profil & Deployment
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Implementation Guide]]
- [[MSI - HL7 FHIR - FHIR Shorthand (FSH) und SUSHI]]
- [[MSI - HL7 FHIR - Deployment Muster]]

#### HL7 FHIR – Sicherheit & Klinische Entscheidungsunterstützung
- [[MSI - HL7 FHIR - SMART on FHIR]]
- [[MSI - HL7 FHIR - CDS Hooks]]
- [[MSI - HL7 FHIR - CQL]]
- [[MSI - HL7 FHIR - Questionnaire und SDC IG]]

#### HL7 FHIR – Terminologie
- [[MSI - HL7 FHIR - Terminology Framework]]
- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]
- [[MSI - HL7 FHIR - Terminology Binding Strength]]
- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]
- [[MSI - HL7 FHIR - Terminology Service]]

### IHE-Profile

#### Dokumentenaustausch
- [[MSI - IHE XDS - Architektur]]
- [[MSI - IHE XDS - Dokument-Metadaten]]

#### Terminologie-Profile
- [[MSI - IHE SVS - Sharing Value Sets]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]

### Terminologien & Klassifikationen

#### Begriffsfundament
- [[MSI - Begriff - Synonyme Homonyme Eponyme]]
- [[MSI - Begriff - Konzept Bezeichnung Code]]

#### Ordnungssystem-Typen
- [[MSI - Ordnungssystem - Konzeptdomäne]]
- [[MSI - Ordnungssystem - Klassifikation]]
- [[MSI - Ordnungssystem - Nomenklatur]]
- [[MSI - Ordnungssystem - Thesaurus]]
- [[MSI - Ordnungssystem - Ontologie]]
- [[MSI - Ordnungssystem - Taxonomie]]
- [[MSI - Ordnungssystem - Semantische Treppe]]

#### Terminologie-Bausteine
- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Vokabular und kontrolliertes Vokabular]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Referenz vs Interface Terminologie]]
- [[MSI - Terminologie - Mapping]]

#### Anforderungen, Strukturen, Cimino
- [[MSI - Terminologie - Anforderungen]]
- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Terminologie - Multiple Consistent Views]]
- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - Mehrachsigkeit]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]

#### Funktionen und Anwendungen
- [[MSI - Terminologie - Funktionen]]
- [[MSI - Terminologie - Pflegediagnose vs ärztliche Diagnose]]

#### LOINC
- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Inhalt]]
- [[MSI - LOINC - Sechs-Achsen-Struktur]]
- [[MSI - LOINC - Fully Specified Name]]
- [[MSI - LOINC - Verwendung in CDA]]

#### UCUM
- [[MSI - UCUM - Definition]]
- [[MSI - UCUM - Aufbau]]
- [[MSI - UCUM - Beispiele]]

#### Identifikatoren
- [[MSI - Identifikator - OID]]
- [[MSI - Identifikator - Übersicht eHealth]]

#### Anwendung & Management
- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Mapping in CDA]]
- [[MSI - Terminologie - Management in Österreich]]
- [[MSI - HL7 - eHDSI MyHealth EU]]
- [[MSI - HL7 - IPS Allergie-Codierung]]

#### Terminologie-Austauschformate
- [[MSI - ClaML - Classification Markup Language]]

#### Terminologieserver
- [[MSI - Terminologieserver - Definition]]
- [[MSI - Terminologieserver - Aufgaben]]
- [[MSI - Terminologieserver - Architektur]]
- [[MSI - Terminologieserver - Austauschstandards]]

### Usability & Barrierefreiheit
- [[MSI - Barrierefreiheit - Definition und Normen]]
- [[MSI - Barrierefreiheit - WCAG Prinzipien]]

### Interoperabilitätsebenen
- [[MSI - Interoperabilität - Definition]]
- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilitätsebenen - Technisch]]
- [[MSI - Interoperabilitätsebenen - Syntaktisch]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilitätsebenen - Organisatorisch]]
- [[MSI - Interoperabilitätsebenen - Benson Grieve Layer-Modell]]
- [[MSI - Interoperabilitätsebenen - Vier-Ebenen-Modell Lehne]]
- [[MSI - Interoperabilität - Voraussetzungen]]
- [[MSI - Interoperabilität - Herausforderungen]]
- [[MSI - Interoperabilität - Anwendungsbereiche Lehne]]
- [[MSI - Daten - DIKW-Pyramide]]
- [[MSI - Daten - Strukturiert vs Unstrukturiert]]
- [[MSI - Daten - Datentypen]]
- [[MSI - Daten - Metadaten]]
- [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]

### Mapping & Transformation
- 

## Cross-Fach-Verbindungen

- HL7 FHIR Resources → Grundlage für [[EHR - MOC]] (ELGA, IPS)
- IHE XUA / IUA → auch in [[ASP - MOC]] (Authentifizierung)
- Profilierung & Implementation Guides → Schnittstelle zu [[EHR - MOC]]

## Prüfungsfragen-Sammlungen

### Themenbereiche

- [[MSI - PF - Interoperabilitaetsebenen]]
- [[MSI - PF - HL7-Familie]]
- [[MSI - PF - IHE-Profile]]
- [[MSI - PF - Terminologien und Klassifikationen]]
- [[MSI - PF - Usability und Barrierefreiheit]]

### Detail-Karten

- [[MSI - PF - Cimino Desiderata]]
- [[MSI - PF - Terminologien Detail]]
- [[MSI - PF - Terminologieserver]]
- [[MSI - PF - HL7 CDA Detail]]
- [[MSI - PF - HL7 FHIR Detail]]
- [[MSI - PF - HL7 FHIR Terminologie]]

## Diagramme

- [[MSI - Diagram - HL7 CDA Aufbau]] – ClinicalDocument-Struktur: Header (4 Cluster) + Body (Level 1/2/3) + Clinical Statements
- [[MSI - Diagram - HL7 FHIR REST und Bundle]] – HTTP-Methoden mit URL-Mustern, Resource-Hierarchie (Resource / DomainResource), Bundle-Typen
- [[MSI - Diagram - IHE XDS Akteure]] – 6 Akteure (PIS, Source, Consumer, Registry, Repository, OnDemand) + ITI-Transaktionen
- [[MSI - Diagram - Cimino Desiderata Uebersicht]] – alle 12 Desiderata nach Kategorien (Inhalt/Struktur, Anwendbarkeit, Kontext, Lebenszyklus)
- [[MSI - Diagram - Interoperabilitaetsebenen]] – Drei-Schichten-Modell · Benson-Grieve (4 Layer) · Lehne Vier-Ebenen (2019)
- [[MSI - Diagram - Semantische Treppe]] – Glossar → Nomenklatur → Klassifikation → Thesaurus → Ontologie

## Lern-Status

- [ ] Alle Vorlesungen extrahiert
- [ ] Alle Konzept-Notes inhaltlich geprüft
- [ ] Karteikarten erstellt
- [ ] Erste Lerndurchgänge abgeschlossen
- [ ] Cross-Fach-Verbindungen ausgearbeitet
