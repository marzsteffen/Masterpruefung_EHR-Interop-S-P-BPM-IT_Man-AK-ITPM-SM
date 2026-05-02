---
fach: ehr
typ: vorlesung
status: offen
quelle_pdf: SS24_Einführung Definitionen.pdf
datum_vorlesung: SS2024
tags:
  - fach/allgemein/ehr
  - typ/vorlesung
  - status/offen
---

# EHR - VL - Einführung und Definitionen

## Überblick

Einführungsvorlesung in das Themengebiet Electronic Health Records. Stellt verschiedene Definitionen (ISO/TR 20514, HIMSS) gegenüber, grenzt verwandte Begriffe wie EMR, CPR, EPR und PHR ab und entwickelt aus den Definitionen die funktionalen Anforderungen an EHR-Systeme. Behandelt zwei zentrale Anforderungs-Frameworks (HIMSS High-Level Requirements und IOM 8 Core Requirements 2003) sowie die ISO 18308 als Anforderungsspezifikation. Schließt mit Architektur-Designfragen (zentral/dezentral, Registry/Repository), der Klassifikation nach Waegemann (5 Level) und den klassischen Typen medizinischer Records.

## Lernziele (laut Vorlesung)

- EHR über mehrere etablierte Definitionen (ISO, HIMSS) abgrenzen können
- EHR von verwandten Begriffen (EMR, CPR, EPR, PHR) unterscheiden
- Funktionale Anforderungen an EHR-Systeme benennen und begründen können
- ISO 18308 als Anforderungsspezifikation einordnen
- Designentscheidungen (zentral vs. dezentral, Registry vs. Repository) und ihre Auswirkungen kennen
- Anhand der 8 IOM-Core-Requirements bestehende Systeme (z. B. ELGA) bewerten können

## Behandelte Konzepte

### Definitionen und Abgrenzung
- [[EHR - Definition - ISO TR 20514]]
- [[EHR - Definition - HIMSS]]
- [[EHR - Abgrenzung - EMR CPR EPR PHR]]

### Funktionen und Anforderungen
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - Anforderungen - Funktional vs Technisch]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[EHR - Standards - Unterstützte Coding Standards]]

### Anforderungsspezifikation und Klassifikation
- [[EHR - ISO 18308 - Anforderungsspezifikation]]
- [[EHR - Klassifikation - Waegemann 5 Level]]

### Architektur und Datenmodell
- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - Architektur - Registry vs Repository]]
- [[EHR - Datenmodelle - Klassische Record Typen]]

### Patientenzugang
- [[EHR - Portal - Patientenportal]]

## Roter Faden

Die Vorlesung beginnt mit der Frage „Was ist ein EHR?" und arbeitet zwei prominente Definitionen heraus (ISO/TR 20514 als Repository-zentriert, HIMSS als longitudinaler Workflow-zentrierter Datensatz). Aus den Definitionsbestandteilen (z. B. „accessible by multiple authorized users", „standardized information model", „secure transmission") leitet der Vortragende „hot topics" ab: Eigentum, Sicherheit, Interoperabilität.

Anschließend erfolgt die Abgrenzung zu EMR, CPR, EPR und PHR – wichtig, weil im Sprachgebrauch oft synonym verwendet, aber inhaltlich verschieden (Reichweite, Lebensdauer, Kontrolle).

Aus den Definitionen werden dann konkrete Funktionen entwickelt (Datenintegration, Decision Support, Patient Support, …). Diese münden in funktionale Anforderungen, die in zwei Frameworks systematisiert werden: HIMSS-High-Level (Access, Data Entry, User Friendliness, Data Protection) und die IOM 8 Core Requirements (2003).

ISO 18308 wird als formale Anforderungsspezifikation eingeführt, die das „Was" beschreibt, aber keine Technologien vorschreibt. Daran schließt die Waegemann-Klassifikation als historische Stufenfolge der EHR-Reife an.

Der letzte Block widmet sich Architektur-Designfragen (zentral/dezentral, Registry/Repository – mit explizitem ELGA-Bezug) und den klassischen Record-Strukturen (zeit-, quellen-, problemorientiert mit SOAP).

## Zentrale Aussagen / Take-aways

- Es gibt keine kanonische EHR-Definition; jede etablierte Definition (ISO/TR 20514, HIMSS) betont andere Aspekte. In der mündlichen Prüfung muss man mehrere Definitionen vergleichen können.
- EHR ≠ EMR ≠ PHR. Die Abgrenzung läuft über Reichweite (eine Organisation vs. übergreifend), Lebensdauer und wer die Kontrolle ausübt (Versorger vs. Patient).
- Funktionale Anforderungen beschreiben „was" das System tun muss, technische Anforderungen „wie" – diese Unterscheidung zieht sich durch beide Anforderungs-Frameworks (HIMSS, IOM).
- ISO 18308 schreibt keine Technologien vor, sondern beschreibt Mindestanforderungen – wichtig, um den Standard nicht mit konkreten Spezifikationen wie HL7 oder DICOM zu verwechseln.
- Designentscheidungen wie zentral/dezentral oder Registry/Repository sind keine rein technischen Fragen – sie haben Konsequenzen für Datenhoheit, Verfügbarkeit und Informationssouveränität.
- ELGA dient durchgehend als reales Beispiel zur Diskussion der Designfragen und wird als Vergleichssystem zu HIS, e-Card etc. herangezogen.

## Querverweise zu anderen Vorlesungen

- [[EHR - VL - SOAP Notes]] – SOAP als Substruktur des problemorientierten Records
- [[EHR - VL - Meaningful Use]] – setzt die IOM/HIMSS-Anforderungen in einen US-Förderkontext
- [[EHR - VL - CCR und CCD]] – konkretisiert Datenmodelle für Austausch
- [[EHR - VL - FHIR Grundlagen]] – moderner Interoperabilitätsstandard, der viele der hier formulierten Anforderungen umsetzt
- [[ASP - MOC]] – Privacy, Authentifizierung, Audit Trails (in der Vorlesung nur grob skizziert)
- [[MSI - MOC]] – HL7, DICOM, LOINC, SNOMED-CT als Grundlage der Standards-Anforderungen

## Quelle

- PDF: SS24_Einführung Definitionen.pdf
- Folienanzahl: 89
- Vortragender: DI Dr. Sten Hanke
