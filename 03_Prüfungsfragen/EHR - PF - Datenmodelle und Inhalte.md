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

# EHR - PF - Datenmodelle und Inhalte

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz deckt das Themenfeld klinischer Datenmodelle und Inhaltsspezifikationen ab: die CCR-Spezifikation (ASTM), ihre CDA-Implementierung als CCD und die Konsolidierung in C-CDA; das HL7 CDA-Datenmodell (RIM-Basis, CDA-Levels 1–2–3); die klassischen medizinischen Record-Typen (Zeit-, Quellen-, Problem-orientiert); unterstützte Coding Standards (LOINC, ICD, SNOMED, DICOM); das ontologische Konzept-System ContSys (ISO 13940) als Backbone für Sekundärnutzung; und die WHO 100 Core Health Indicators als Referenzrahmen für Public-Health-Reporting. Die Themen entstammen primär der CCR/CCD-Vorlesung und der Macro-Level-Interoperabilitäts-Vorlesung.

## Verlinkte Konzepte

- [[EHR - CCR - Continuity of Care Record]]
- [[EHR - CCD - Continuity of Care Document]]
- [[EHR - C-CDA - Consolidated CDA]]
- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - HL7 CDA - Levels 1 2 3]]
- [[EHR - Datenmodelle - Klassische Record Typen]]
- [[EHR - Standards - Unterstützte Coding Standards]]
- [[EHR - ContSys - ISO 13940]]
- [[EHR - Indikatoren - WHO 100 Core Health Indicators]]

---

## Karten

### Definition

Was ist der CCR – welche 6 Sektionen sind definiert, und was macht ihn zu einer Summary statt einer vollständigen Akte?

?

**CCR** (Continuity of Care Record, Standard ASTM E2369-12) ist ein US-Standard für eine kompakte Versorgungs-Zusammenfassung – „somewhat like ELGA Entlassungsbrief, but more." Die 6 mandatierten Kern-Sektionen: (1) **Provider Info** – wer hat das CCR erstellt (Optional Extension); (2) **Patient Identifying Info** – demografische und administrative Daten; (3) **Insurance and Financial Info** – Leistungsanspruch, Zuzahlung; (4) **Patient's Health Status** – Probleme/Diagnosen, Medikamente, Immunisierungen, Vitalzeichen, Laborbefunde, Prozeduren; (5) **Care Documentation** – spezialitäten-spezifische Info, Disease-Management, frühere Encounters, Payer Attachments, Patienten-eigene Dokumentation; (6) **Care Plan Recommendation** – Empfehlungen zum weiteren Plan (Text). **Warum Summary statt Akte**: CCR ist auf das Nötige für eine Care Transition beschränkt – nicht jedes jemals erhobene Datum, sondern der aktuelle Status + Plan. Use-Case: Krankenhaus → Reha.

Worauf basiert CDA – welche Hauptelemente hat ein CDA-Dokument, und was bedeutet RIM-Konformität konkret?

?

**CDA** (Clinical Document Architecture, HL7 v3) basiert auf dem **RIM** (Reference Information Model) – dem zentralen Datenmodell von HL7 v3. Grundsatz: jedes XML-Element muss einer RIM-Klasse oder einem Klassen-Attribut entsprechen. **Dokumentstruktur**: (1) **Header** – Patient, Author, Custodian, Encounter, Dokument-Metadaten; (2) **Body** – eine oder mehrere Sections; (3) **Section** – LOINC-Code + Titel + narrativer `text`-Block + optional strukturierte `entry`-Elemente; (4) **Entry** – maschinenverarbeitbare strukturierte Daten (Observations, Substance Administrations, Acts). **RIM-Hauptklassen**: Act (Aktivität), Entity (Akteur), Role (Rolle), Participation (Act ↔ Role Verbindung), ActRelationship (Act-Act-Verbindung). Beispiel: `<observation classCode="OBS" moodCode="EVN">` → RIM-Klasse Observation (Subklasse von Act), Event-Mood = tatsächlich beobachtetes Ereignis. CDA ist by design **Menschen-lesbar** – der narrative Text-Block ist Pflicht auf jeder Ebene.

Welche drei Strukturierungs-Levels unterscheidet CDA – und was verändert sich in der maschinellen Verarbeitbarkeit?

?

CDA-Levels sind **kumulativ** (Level 3 enthält immer Level 1+2): **Level 1** – nur Header strukturiert; Body ist unstrukturiertes Narrativ oder PDF-Attachment; maschinell verarbeitbar: nur Metadaten. **Level 2** – Body in Sections unterteilt; jede Section trägt einen LOINC-Section-Code + Narrativ; maschinell: Sections adressierbar, Inhalt nicht. **Level 3** – innerhalb der Sections existieren strukturierte Entries (Observations, Procedures, Medication mit codierten Werten); maschinell: jeder Datenpunkt auswertbar. Beispiel Diagnose „Hypertonie" Level 3: `<observation classCode="OBS" moodCode="EVN">` mit SNOMED-CT-Code 38341003, Datum, Wert – automatisiert abfragbar. **LCIM-Bezug**: Level 1 ≈ Technical Integration; Level 2 = Teil-Semantik; Level 3 = vollständige strukturelle + semantische Interoperabilität. **Praxis**: CCD muss unter MU für automatisierte Lab-Auswertung Level 3 sein.

---

### Anwendung

Erkläre die Evolutionskette CCR → CCD → C-CDA mit den jeweiligen Treibern – warum ist CCR heute „fading out"?

?

**CCR** (ASTM E2369-12): Inhalts-Spezifikation, implementiert entweder als ASTM-XML oder als HL7-CDA. **CCD** (HL7-CDA-Implementation des CCR): gleiche 6 Sektionen, aber im CDA-Format mit RIM-Basis; implementierbar als HTML/PDF/Word via XSLT-Stylesheets. Treiber: „Most EHR vendors adopted CCD rather than ASTM-CCR since it is a newer format." In MU Stage 1 wurde CCD als bevorzugter Exchange-Standard festgeschrieben. **C-CDA** (Consolidated CDA): HL7 konsolidiert 9 CDA-Dokumenttypen unter einer Implementation Guide – CCD ist einer davon. In MU Stage 2 wurde C-CDA als verpflichtender Standard für Care Transitions eingeführt, CCD als „most appropriate document for care transitions" innerhalb C-CDA hervorgehoben. **Warum CCR „fading out"**: die ASTM-XML-Variante des CCR hat keine Marktakzeptanz erlangt; CCD/C-CDA hat den Use-Case übernommen; internationale Standardisierung erfolgte über HL7, nicht ASTM.

Welche 9 Dokumenttypen enthält C-CDA – und bei welcher Care-Transition-Situation wird welcher eingesetzt?

?

C-CDA konsolidiert 9 CDA-Dokumenttypen: (1) **CCD** (Continuity of Care Document) – „most appropriate for care transitions" allgemein; (2) **Consultation Note** – Facharzt-Überweisung; (3) **Diagnostic Imaging Report** – Radiologiebefund; (4) **Discharge Summary** – Entlassungsbrief; (5) **History and Physical (H&P)** – Aufnahme-Untersuchung; (6) **Operative Note** – OP-Bericht; (7) **Procedure Note** – interventioneller Eingriff; (8) **Progress Note** – Folgevisite; (9) **Unstructured Document** – nicht-strukturierte Inhalte. Situations-Mapping: Krankenhaus → Reha → **CCD** + **Discharge Summary**; Facharzt → Hausarzt → **Consultation Note**; OP → Nachbehandler → **Operative Note**; Routinevisite → **Progress Note**. Hinweis: Die exakte Liste der 9 ist im PDF nicht vollständig enumeriert; obige ist die Standardliste aus dem HL7 C-CDA Implementation Guide.

Was ist der WHO-Indikator „Tobacco use among persons aged 15+ years" – welche Komponenten hat er, und warum ist die genaue Definition prüfungsrelevant?

?

SDG-Referenz: **SDG 3.a.1**. **Definition**: age-standardized prevalence of current tobacco use among persons aged 15+ years. Umfasst: smoked tobacco (Zigaretten, Zigarren, Bidis, Shisha, Kreteks etc.) + smokeless tobacco (Snuff, Snus, Gutkha etc.) + „current use" = tägliche oder gelegentliche Nutzung zum Befragungszeitpunkt. **Numerator**: Anzahl aktueller Tabaknutzer ≥ 15 Jahre. **Denominator**: Gesamtbevölkerung ≥ 15 Jahre. **Disaggregation**: Alter, Geschlecht. **Method**: (Befragte ≥ 15 die Tabak nutzen) / (Befragte ≥ 15) × 100. **Warum prüfungsrelevant**: zeigt exemplarisch, dass Public-Health-Vergleiche erst möglich werden, wenn alle Länder exakt dieselbe Definition verwenden – Numerator-/Denominator-Exaktheit verhindert Äpfel-Birnen-Vergleiche. Direkte Verbindung zu LCIM: wenn EHRs Smoking Status nicht auf Level 3 (strukturiert, codiert) speichern, ist dieser Indikator nicht automatisch ableitbar.

---

### Diskussion

CDA ist Dokument-zentriert, FHIR ist Resource-/API-zentriert – welche Use-Cases bevorzugen welches Modell?

?

**CDA-Stärken**: Dokument-Integrität (ein Dokument = ein signierter, unveränderlicher Nachweis); rechtliche Bindung (Entlassungsbrief als CDA ist ein juristisches Dokument); Menschen-Lesbarkeit by design; bewährte Validierung via Schematron. Ideal für: Entlassungsbriefe, Befunde, Atteste, Archive. **FHIR-Stärken**: API-First, granulare Abfragen (nur Laborbefunde der letzten 6 Monate), REST-Interface, JSON, deutlich niedrigere Implementierungs-Komplexität, dynamische Aktualisierung. Ideal für: CDS-Hooks (Clinical Decision Support), Patientenportale, Mobile Apps, Real-Time-Zugriff. **Hybride Realität**: FHIR Document Bundle (ResourceType = composition) kann CDA-Inhalte abbilden; SMART on FHIR ergänzt FHIR um Zugriffssteuerung; viele Systeme exportieren CDA für Archivzwecke und nutzen FHIR für Live-Abfragen. Die Wahl ist kein „entweder/oder", sondern Use-Case-getrieben.

Warum reichen gemeinsame Datenformate (FHIR, CDA) nicht aus – welche Rolle spielt ContSys (ISO 13940) als Ontologie-Schicht?

?

Datenformate (FHIR, CDA) lösen die **syntaktische** Interoperabilität: Daten können übertragen und gelesen werden. Sie lösen nicht die **semantische** Interoperabilität auf Prozessebene: Bedeutet „Healthcare activity" in System A dasselbe wie in System B? Ist eine „Observation" in FHIR konzeptuell deckungsgleich mit einer „Healthcare investigation" in ContSys? **ContSys (ISO 13940)** liefert ein ontologisches Konzept-System als gemeinsames Vokabular: Healthcare actor, Health state, Health condition, Healthcare activity, Clinical pathway. Damit können Datenfelder verschiedener Systeme gegen ContSys validiert und verlinkt werden. Laut Vorlesung: „Prerequisite for multiple use of data is a compatible system of concepts." Ohne geteilte Ontologie können Daten aus verschiedenen EHRs zwar technisch zusammengeführt werden, aber ihre inhaltliche Bedeutung bleibt kontextabhängig – Sekundärnutzung (Forschung, Policy) wird fehleranfällig. ContSys ist laut Vorlesung in Estland produktiv im Einsatz.

Warum können viele EHR-Systeme die WHO 100 Core Health Indicators nicht ohne manuelle Erhebung liefern – auf welcher LCIM-Ebene liegt das Problem?

?

Das Problem liegt überwiegend auf **LCIM-Ebene 4 (Syntax and Semantics)** und teils auf **Ebene 5 (Pragmatics/Process Composability)**. Konkret: (1) **Fehlende strukturierte Erfassung**: Smoking Status wird in vielen EHRs als Freitext dokumentiert – kein maschinenlesbares Coding (kein SNOMED-CT-Code, kein LOINC-Code). CDA Level 1 genügt nicht für automatisierte Auswertung; Level 3 wäre nötig. (2) **Inkonsistente Definitionen**: „Current use" (daily + occasional) ist nicht in allen EHR-Templates identisch umgesetzt – Numerator und Denominator können variieren. (3) **Fehlende Populationsperspektive**: EHRs bilden individuelle Patientenakten ab, nicht Bevölkerungsstichproben. WHO-Indikatoren erfordern Kohorten-Sicht (alle Patienten ≥ 15 in einem Zeitraum). (4) **Privacy-Aggregation**: selbst wenn Einzeldaten vorhanden sind, ist die Aggregation über Institutionen hinweg datenschutzrechtlich oft ungelöst. Lösung: strukturierte FHIR-Profile für Risikofaktoren + ContSys als gemeinsame Ontologie + pseudonymisierte Sekundärnutzungs-Infrastruktur (vgl. EHDS HealthData@EU).

Klassische Record-Typen (Zeit-, Quellen-, problem-orientiert): welcher ist die Basis für SOAP – und warum erzwingt das eine bestimmte EHR-Architektur?

?

Der **problem-orientierte medizinische Record** (Weed, 1960er) ist die Grundlage für SOAP-Notes. Er organisiert Daten primär nach Medizinischen Problemen/Diagnosen/Symptomen, sekundär nach Zeit, und führt als dritte Dimension **SOAP** (Subjective, Objective, Assessment, Plan) ein. **Architektur-Konsequenz**: ein EHR, das problem-orientierte Records unterstützen soll, muss Probleme/Diagnosen als primären Anker modellieren (Problem-Liste als Core Entity). Zeitliche Sicht (alle Vitalzeichen über Zeit) und Quellen-Sicht (alle Befunde von Radiologe X) müssen als Sekundärsichten darüber gelegt werden. Modernes EHR-Gegenbeispiel: rein zeitlich-sequenzielle EMR-Systeme (alteingesessene Papier-digitalisierungs-Systeme) können keine saubere Problem-Liste führen, was CDS (Clinical Decision Support) erschwert. **SOAP im LCIM**: erst wenn SOAP-Elemente strukturiert codiert vorliegen (Level 3 CDA oder FHIR-Observation/Condition), sind sie für LCIM-Ebenen oberhalb Syntax nutzbar.

---

## Mögliche Anschlussfragen des Prüfers

- Was sind die „Mandated Core Elements" im CCR und welche sind „Optional Extensions"?
- Welche LOINC-Codes klassifizieren typische CDA-Sections? (z. B. 11450-4 Active Problems, 10160-0 Medications)
- Welche RIM-Klassen gibt es – und was ist moodCode?
- Wie unterscheidet sich CCR von der Patient Summary im EHDS/IPS-Kontext?
- Was ist pervasive data stewardship, und wie hängt es mit ContSys zusammen?
- Wie würde man Smoking Status in einem FHIR-Profil strukturieren, damit SDG 3.a.1 ableitbar ist?
- Welcher klassische Record-Typ war historisch in Papierakten am häufigsten?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
