---
fach: ehr
typ: vorlesung
status: offen
quelle_pdf: BPHC_EMR_Functional_Specs-Cerner.pdf
datum_vorlesung: 2003-10-28
tags:
  - fach/allgemein/ehr
  - typ/vorlesung
  - status/offen
---

# EHR - Spec - BPHC EMR Functional Specs Cerner

## Überblick

Vendor-Antwortdokument von **Cerner Corporation** auf einen funktionalen Anforderungskatalog des **Bureau of Primary Health Care (BPHC)**, einer Behörde des US Department of Health and Human Services. Stand: Version 5.2, 28.10.2003. Beschreibt 37 Seiten lang, wie das Cerner-System „PowerChart Clinical Office" 24 funktionale Anforderungsbereiche an ein EMR erfüllt – jeweils mit Min/Opt-Markierung, Vendor-Capability-Spalte (Yes / Modulname), Future-Version und 3rd-Party-Provider.

Das PDF ist **kein Lehrmaterial im engeren Sinn**, sondern wird in der EHR-Einführungsvorlesung ([[EHR - VL - Einführung und Definitionen]], Folie 67) als **konkretes Beispiel** für ein Functional Requirements Document referenziert. Lerngegenstand ist daher primär die Methodik (RFP-Pattern), nicht jeder einzelne Cerner-Feature-Eintrag.

## Lernziele (laut Vorlesung)

Das Dokument selbst enthält keine Lernziele. Aus der Referenz in der Einführungsvorlesung implizit:
- Den Aufbau eines Functional Requirements Document erkennen und erstellen können
- Min/Opt-Anforderungen unterscheiden
- Eine Vendor Capability Matrix lesen und kritisch bewerten
- Die typischen Funktionsbereiche eines EMR benennen

## Behandelte Konzepte

### Methodik der EHR-Beschaffung
- [[EHR - Beschaffung - Functional Requirements Document]]
- [[EHR - EMR - 24 Funktionsbereiche]]

### Konkretes Vendor-Beispiel
- [[EHR - Beispiel - Cerner PowerChart Office]]

## Roter Faden

Das Dokument beginnt mit einem **Vendor Profile** (Cerner: Firmensitz Kansas City, $751,8 Mio. Jahresumsatz 2003, 24 Jahre im Markt, 231 Klienten, 528 Sites, 2.399 Millennium-Anwendungen). Es folgt eine Beschreibung des **Antwort-Schemas**: Min vs. Opt, Vendor Capabilities, Future Version, 3rd Party Provided.

Die eigentliche Anforderungs-Matrix umfasst **24 nummerierte Funktionsbereiche** in drei großen Blöcken:
- **Klinische Funktionen** (Sektionen 1–18): General/Coding, Demographics, Medical History, Encounters, Progress Notes, Problem Lists, CPGs, Care Plan, Prevention, Patient Education, Alerts, Orders, Results, Medications, Confidentiality & Security, Decision Support, Cost Measuring/Quality Assurance, Disease Management/Clinical Registries
- **Technische Funktionen** (Sektionen 19–21): Technical, Clinical IT Data Dictionary, Input Mechanisms
- **Ergonomie & Implementierung** (Sektionen 23–24): Ergonomic Presentation, Implementation and Support

Jede Anforderung wird einzeln mit Min/Opt markiert und Cerner gibt sein konkretes Modul (PowerChart Clinical Office, PowerNote, PowerForms, PowerChart Support Office, MediSource Foundation, Discern Expert, PowerInsight, Clinical Outcomes etc.) an, das die Anforderung erfüllt.

## Zentrale Aussagen / Take-aways

- **Functional Requirements Documents sind RFP-Werkzeuge** – sie zwingen Vendoren zu strukturierten Antworten und ermöglichen Vergleichbarkeit.
- **Min/Opt-Trennung** ist methodisch zentral: Ein Vendor ohne „Yes" auf einem Min-Eintrag fällt aus der Auswahl, ein Opt-Eintrag ist Verhandlungsmasse.
- Die **Coding-Standard-Liste eines US-EMR** ist deutlich umfangreicher als die in der Einführungsvorlesung genannte: zusätzlich zu ICD-9-CM, ICD-10, CPT-4/5, SNOMED II/III/CT, LOINC sind APG, NDC, NIC/NOC, NANDA, APC, HCPCS Pflichtbestandteile (US-spezifisch).
- **HIPAA-Konformität** ist Pflichtanforderung in einem US-EMR – nicht optional.
- Cerner antwortet 2003 mit „ICD-10 will be available when it becomes industry standard" – ein interessantes historisches Detail (in den USA wurde ICD-10-CM erst 2015 verpflichtend).
- Verfügbarkeitsanforderung: 99,5 % Verfügbarkeit, 90 % der Zeit < 2 s Antwortzeit, 80 % sub-second.
- **RBAC** (Role Based Access Control) wird explizit als Standard für Zugriffskontrolle genannt.

## Querverweise zu anderen Vorlesungen

- [[EHR - VL - Einführung und Definitionen]] – referenziert dieses Dokument explizit
- [[EHR - Anforderungen - HIMSS High-Level Requirements]] – ähnliche Strukturierung in 4 Bereichen
- [[EHR - Anforderungen - IOM 8 Core Requirements]] – die 8 IOM-Anforderungen tauchen in den BPHC-Sektionen verteilt wieder auf
- [[ASP - HIPAA]] – hier als Pflicht­anforderung referenziert
- [[ASP - RBAC]] – Role Based Access Control als geforderter Standard

## Quelle

- PDF: BPHC_EMR_Functional_Specs-Cerner.pdf
- Foliendokumentation: 37 Seiten Anforderungsmatrix + Vendor Profile
- Vendor: Cerner Corporation (Kansas City, MO)
- Auftraggeber: BPHC (Bureau of Primary Health Care, US-Behörde)
- Stand: Version 5.2, 28.10.2003
