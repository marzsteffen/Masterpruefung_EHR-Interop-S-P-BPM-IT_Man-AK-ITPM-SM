---
fach: ehr
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/ehr
---

# EHR - PF - Grundlagen und Frameworks

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz deckt die Grundlagenbegriffe, Anforderungs-Frameworks und Interoperabilitäts-Konzepte des Fachs EHR ab. Basis sind die Vorlesungen zu Einführung & Definitionen, Macro-Level Interoperabilität sowie das BPHC/Cerner-Funktionsspezifikationsdokument. Abgefragt werden Definitionen (ISO TR 20514, HIMSS, IOM, Waegemann), Anforderungs-Methodik (ISO 18308, Functional Requirements Document), Klassifikationen und Frameworks (Zachman, LCIM, Logic Modes, MITRE HISCF) sowie fundamentale Unterscheidungen (System vs. Exchange Format, strukturell vs. semantisch, Zentralisierungsmodelle).

## Verlinkte Konzepte

- [[EHR - Definition - ISO TR 20514]]
- [[EHR - Definition - HIMSS]]
- [[EHR - Abgrenzung - EMR CPR EPR PHR]]
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - Anforderungen - Funktional vs Technisch]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[EHR - ISO 18308 - Anforderungsspezifikation]]
- [[EHR - Klassifikation - Waegemann 5 Level]]
- [[EHR - Integrated Care - Macro Meso Micro Level]]
- [[EHR - Methodik - Zachman Framework]]
- [[EHR - Interoperabilität - LCIM nach Tolk]]
- [[EHR - Datensharing - Logic Modes]]
- [[EHR - eHealth Capabilities - Information Flows]]
- [[EHR - Maturity Model - MITRE HISCF]]
- [[EHR - Beschaffung - Functional Requirements Document]]
- [[EHR - EMR - 24 Funktionsbereiche]]
- [[EHR - Beispiel - Cerner PowerChart Office]]
- [[EHR - Healthcare Systems - Zentralisierungs-Modelle]]
- [[EHR - Interoperabilität - Strukturell vs Semantisch]]
- [[EHR - System vs Exchange Format]]

---

## Karten

### Definition

Welche mindestens fünf Kernbestandteile enthält die EHR-Definition nach ISO/TR 20514?
?
Die ISO/TR 20514-Definition eines „Integrated Care EHR" umfasst: (1) **Repository** – Ablage, kein flüchtiger Datenstrom; (2) **Information** – semantisch interpretierbar, mehr als rohe Daten; (3) **Computer processable form** – maschinenlesbar und austauschbar; (4) **Stored and transmitted securely** – Sicherheit ist Teil der Definition, kein Add-on; (5) **Accessible by multiple authorized users** – Mehrnutzersystem; (6) **Standardized Information Model, independent of the EHR system itself** – Interoperabilität ist gefordert; (7) **Primary purpose**: Unterstützung kontinuierlicher, effizienter und qualitativer integrierter Versorgung. Kurzformel: EHR = Repository + standardisiertes Modell + sicherer Multi-User-Zugriff + Continuity-of-Care-Ziel.

Nenne alle 8 IOM Core Requirements (Institute of Medicine, 2003) für EHR-Systeme.
?
1. **Health Information and Data** – vollständiger elektronischer Chart, alle entscheidungsrelevanten Daten. 2. **Result Management** – Verwaltung aller Testergebnisse (Labor, Radiologie). 3. **Order Management** – alle Verschreibungen elektronisch, reduziert Handschriftfehler. 4. **Decision Support** – Warnungen/Reminder zu Wechselwirkungen, Leitlinien, Prävention, Outbreak Detection. 5. **Electronic Communications and Connectivity** – interoperabler Datenaustausch mit Versorgern, Laboren, Patienten. 6. **Patient Support** – Patientenzugang zu Lehrmaterial, Eingabe eigener Daten (Home-Monitoring). 7. **Administrative Processes** – Terminverwaltung, Eligibility-Prüfung, Practice Management. 8. **Reporting to Authorities** – standardisierte Reports an Behörden (state, federal, local).

Welche 5 Stufen unterscheidet Waegemann (1999) bei der Klassifikation elektronischer Gesundheitsakten?
?
Level 1 – **Automated Record**: lokal, administrativ, basale Patienteninformationen. Level 2 – **Computerized Medical Record**: lokal, vollständige medizinische Infos als gescannte Dokumente (keine Struktur). Level 3 – **Electronic Medical Record (EMR)**: lokal, strukturiert, auf medizinischer Terminologie basierend. Level 4 – **Electronic Patient Record (EPR)**: organisationsübergreifend, vollständiges Set elektronischer Records. Level 5 – **Electronic Health Record (EHR)**: lebenslange Dokumentation inkl. Einträgen aus Hilfsberufen (Pflege, Physiotherapie etc.).

Welche vier High-Level-Anforderungsblöcke stellt das HIMSS Electronic Health Record Definitional Model (Version 1.0) an EHR-Systeme?
?
1. **Access & Reliability**: sicherer Echtzeit-Zugriff, 24/7-Verfügbarkeit (> 99,9 %), Access Audit Trails, Vertraulichkeit. 2. **Data Entry**: direkte oder automatische Eingabe, Point-of-Care-Dokumentation, Linking von Labor/Bildern/Wearables, Coded Data (HL7, XML, JSON), Voice Recognition, OCR. 3. **User Friendliness**: einfache Eingabe und Abruf, Filterbarkeit, Time-Series-Ansicht, konsistente GUIs, akzeptable Antwortzeiten. 4. **Data Protection**: granulare Zugriffsregeln, verschlüsselte Repositories, Backup & Recovery, sicherer Transport (HTTPS), Authentifizierung, Logging mit Patienteneinsicht ins Log.

---

### Anwendung

Was beschreibt ISO 18308 – und was beschreibt sie bewusst nicht? Welcher methodische Vorteil folgt daraus?
?
ISO 18308 beschreibt **minimale Anforderungen** an EHR-Systeme: Strukturanforderungen (Sektionen, Sichten), Privacy & Security (Consent, Access Control, Audit), Legal Aspects (Actor Identification, Versionierung statt Löschung, Logging jeder Aktion) und Exchange (Empfehlung von Standards wie HL7, DICOM, ohne Mandatierung). Sie beschreibt **nicht**: konkrete Technologien, Hardware/Software, klinische Prozessdetails, ein spezifisches Datenmodell, Anonymisierung für Forschung. Methodischer Vorteil: Technology-Agnostizität erlaubt langfristig stabile, vendor-neutrale Ausschreibungen – konkrete Technologien veralten schneller als die Anforderungen selbst.

Welche sechs Dimensionen des Zachman-Frameworks können zur Analyse einer eHealth-Entscheidungssituation genutzt werden? Wende sie auf ein konkretes Beispiel an.
?
Zachman-Dimensionen: **Who** (Person/Rolle/Stakeholder), **Why** (Zweck/Mission/Auftrag), **How** (Logik/Prozess/Algorithmus), **What** (Inputs/Outputs/Daten/Zustände), **Where** (Quellsystem/Zielsystem/Ort), **When** (Zeitpunkt/Trigger/Frequenz). Beispiel-Anwendung auf „Soll ein Patient Selbstmessungs-Daten ins EHR einbringen?": Who – Patient, Arzt, Datenschutzbeauftragte; Why – Monitoring einer chronischen Erkrankung, informierte Entscheidungen; How – Validierungsalgorithmus (Plausibilitätsprüfung); What – Blutdruck, Gewicht, Blutzucker, Zeitstempel; Where – PHR-App → FHIR-Endpunkt des Krankenhaus-EHR; When – täglich nach Messung, Trigger: Messgerät-Sync.

Welche drei Modi des Datenteilens (Logic Modes) werden unterschieden? In welchem Modus befindet sich ELGA heute, und was wäre der Zielzustand?
?
(1) **Transactional**: bilateral/multilateral, vertragliche Standards, Secondary Use nachrangig – gängigste Realität. (2) **Shared Registries**: zentrale Struktur, monopolistische oder föderierte Governance, statische Standards, wenig Multipurpose. (3) **Informational**: diverse Governance, hohe Ecosystem Agility, fundamentaler Multipurpose-Dateneinsatz, dynamische Standards – intendiertes Zielmodell. ELGA heute: am ehesten **Shared Registries** (zentrales Repository-Konzept, fixe Formate, Governance durch ELGA GmbH). Zielzustand (EHDS-Vision): **Informational** – dieselben Daten für Versorgung, Forschung, Policy und Funding.

Ein Krankenhaus schreibt ein neues EMR-System aus. Was bedeuten die Spalten Min, Opt, Yes, Module Name und 3rd Party Provided in der Anforderungsmatrix?
?
**Min**: Pflichtanforderung – Vendor ohne Erfüllung scheidet aus. **Opt**: optional, wünschenswert, kein Ausschlusskriterium. **Yes**: Vendor markiert „X", wenn Anforderung aktuell vollständig erfüllt ist. **Module Name**: Name des konkreten Software-Moduls, das die Anforderung bereitstellt (z. B. „PowerChart Clinical Office with PowerNote"). **Future Version (Date)**: Versionsname und geplantes Datum für noch nicht erfüllte Anforderungen – schafft Verhandlungsbasis, ist aber Risikoposition. **3rd Party Provided**: Drittanbieter-Lösung via Interface – Vendor übernimmt die Schnittstellenverantwortung, nicht die Kernfunktion.

---

### Diskussion

Wie unterscheiden sich die ISO TR 20514-Definition und die HIMSS-Definition eines EHR in Schwerpunkt und Intention?
?
ISO TR 20514 ist **formal-abstrakt und normativ**: betont Repository-Charakter, standardisiertes und systemunabhängiges Informationsmodell sowie Continuity of Care. HIMSS ist **workflow-zentriert und enumerativ**: betont Longitudinalität, Entstehung aus Encounters, listet konkrete Inhalte (Vital Signs, Lab, Medikation, Immunisierung) und fordert Workflow-Automatisierung plus CDS. ISO = „Was das System SEIN muss" (Eigenschaften); HIMSS = „Was das System TUN und ENTHALTEN muss" (Funktion). ISO impliziert Interoperabilität als Kernpflicht (standardized model, independent of system); HIMSS setzt sie voraus ohne sie normativ zu verankern. In der mündlichen Prüfung: beide Definitionen ergänzen sich – ISO für Anforderungsableitung, HIMSS für operative Systembewertung.

Was unterscheidet EMR, CPR, EPR und PHR voneinander – und wer kontrolliert jeweils die Daten?
?
**EMR** (Electronic Medical Record): auf eine einzelne Versorgungs-Organisation beschränkt; Kontrolle beim Versorger. **CPR** (Computer-based Patient Record, Richard 1997): lebenslang und organisationsübergreifend, potenziell international; Kontrolle beim Versorger. **EPR** (Electronic Patient Record): organisationsübergreifend, aber nicht zwingend lebenslang; nur relevante Informationen; Kontrolle beim Versorger. **PHR** (Personal Health Record): „patient-side view" – vom Patienten gemanagt und kontrolliert. **EHR**: organisationsübergreifend, standardisiertes Modell, Zugang für multiple Versorger; Kontrolle beim Versorger, Zugangsrecht für Patienten. Kritische Diskussionsachse: Wenn PHR-Daten in eine EHR integriert werden, wer verantwortet dann Datenqualität und Haftung?

Warum ist semantische Interoperabilität schwieriger als strukturelle – und was passiert praktisch, wenn Struktur ohne Semantik vorliegt?
?
**Strukturelle Interoperabilität**: gemeinsames Format (HL7 v2, CDA-XML, FHIR-JSON) – die Nachricht wird technisch korrekt übertragen und ist menschenlesbar. **Semantische Interoperabilität**: beide Seiten nutzen dieselben Codes in denselben Terminologien (LOINC für Tests, SNOMED CT für klinische Begriffe, UCUM für Einheiten, ICD für Diagnosen). Ohne Semantik: Daten ankommen, aber CDS, Alerting und maschinelle Auswertung schlagen fehl. Gründe für Schwierigkeit: Sprach-/Kulturunterschiede (Diagnosebegriffe variieren), proprietäre Codes in Altsystemen, Wartungskosten und Lizenzfragen für Terminologien (SNOMED = kostenpflichtig außerhalb bestimmter Mitglieder), institutionelle Hoheitsansprüche. Laut Vorlesung: „The whole world is standardizing" – aber clinical research (CDISC/FDA) bleibt Ausnahme.

Was ist der Unterschied zwischen einem EHR-System und einem EHR-Exchange-Format – und warum braucht auch eine homogene Systemlandschaft ein Exchange-Format?
?
**EHR-System**: erfasst, speichert, stellt Daten bereit; kann proprietär oder offen sein (Cerner Millennium, OpenEHR, Epic). **Exchange-Format**: standardisiertes Protokoll für Transport zwischen Stellen (HL7 v2, CDA, FHIR). Gegenbeispiel: Slowenien nutzt OpenEHR landesweit – sobald Daten dezentral aggregiert oder an Patienten weitergegeben werden, braucht es einen definierten Austauschstandard. FHIR macht bewusst keine Vorgabe zur internen Datenhaltung – das trennt System von Format. Konsequenz: Auch ein Mono-Vendor-Markt schützt nicht vor Exchange-Problemen an Systemgrenzen (Bundesland-, Versorgungs-, Sektoren-Grenzen). Diese Trennung ist architektonisch fundamental: ein System muss mehrere Exchange-Formate bedienen können.

Welche Konsequenzen hat die politische Zentralisierung (oder Dezentralisierung) eines Gesundheitssystems für EHR-Implementierungen?
?
**Zentralisiert** (UK-NHS): Top-down-Mandat möglich, Chance auf ein einheitliches System – aber Zentralprojekt-Risiko (NHS National Programme for IT: > 10 Mrd. £ Fehlinvestition). **Semi-zentralisiert** (Österreich): bundeslandspezifische HIS, ELGA als nationale Klammer mit dezentralen Repositories – Folge: Lücken (Reha-Zentren ohne ELGA-Anbindung laut Vorlesungsbeispiel, private Kliniken mit Eigenystemen). **Dezentralisiert** (USA): Anreiz statt Mandat (HITECH/Meaningful Use), Vendor-Vielfalt (Epic, Cerner, Allscripts), Interoperabilität via Exchange-Standards als Kompensation. Fazit: Zentralisierung senkt Koordinationskosten, erhöht Systemrisiko; Dezentralisierung fördert Innovation, erschwert Interoperabilität. Österreichs semi-zentraler Ansatz versucht Balance – mit nachweisbaren Lücken.

Auf welcher LCIM-Schicht scheitern typische EHR-Datenaustausche in AT/EU heute? Was wäre nötig, um Process Composability zu erreichen?
?
**Technical Integration** (Schicht 1): meistens realisiert – Systeme sind vernetzt, HTTPS-Transport, HL7-v2-Verbindungen existieren. **Syntax & Semantics** (Schicht 2): häufig Hauptbaustelle – Daten sind strukturell übertragen, aber unterschiedliche Terminologien (SNOMED vs. ICD vs. proprietäre Codes), fehlender Master Data, verschiedene Patientenidentifier. **Process Composability** (Schicht 3): selten erreicht – Datenflüsse erfüllen nicht die Bedürfnisse nachgelagerter Entscheidungsfindung, weil Timing, Kontext und Actionability fehlen. Für Process Composability nötig: semantisch normierte Daten (LOINC, SNOMED, UCUM), Prozess-Ontologien (ISO 13940 ContSys), Einigung über Erhebungszeitpunkte und -kontexte, CDS-Integration. Laut Tolk: ohne Process Composability bleibt Interoperabilität auf Datentransport beschränkt, nicht auf Entscheidungsunterstützung.

---

## Mögliche Anschlussfragen des Prüfers

- ISO 18308 verbietet Löschungen und verlangt Versionierung. Wie verhält sich das zu DSGVO Art. 17 (Recht auf Löschung)?
- Warum liegt „Data Quality" im MITRE HISCF meist auf Reife-Stufe 2, während „Data Security" regelmäßig auf Stufe 4 liegt – welche Anreizstruktur erklärt die Asymmetrie?
- Welche der 24 Funktionsbereiche des BPHC/Cerner-RFP wären 2025 durch FHIR-API-First-Architektur am stärksten transformiert?
- Warum scheitern viele eHealth-Projekte trotz starker Macro-Ebene-Politik auf Meso- oder Micro-Ebene?
- Ist die Waegemann-Klassifikation (1999) 2025 noch zeitgemäß – welche Dimensionen fehlen (z. B. Patient-generated Data, KI-Verarbeitbarkeit)?
- Welcher Logic Mode ist Voraussetzung für echten Secondary Use (Forschung, Policy) von Gesundheitsdaten?
- Warum macht FHIR keine Vorgabe zur internen Datenhaltung – und was bedeutet das für eine Migrations-Strategie?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
