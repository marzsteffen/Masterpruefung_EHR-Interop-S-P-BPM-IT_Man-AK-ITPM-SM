---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/03 Terminologien Anwendung/03_Terminologien_Anwendung.pdf
datum_vorlesung: 2024-10-31
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - VL - Terminologien Anwendung

## Überblick

Praxis-orientierte Vorlesung „Semantik in der Praxis": Wie werden Terminologien konkret in Standards (CDA, FHIR, HL7 v2) gebunden? Wie sehen Value Sets, ihre Wartung und ihr Management in Österreich aus? **LOINC und UCUM** werden hier im Detail behandelt (die anderen eHealth-Terminologien aus der Auswahl-Liste der Vorlesung 02 werden in dieser LV bewusst *nicht* einzeln durchgegangen). Abschluss: internationale Anwendungsbeispiele (Lethe, eHDSI/MyHealth@EU, IPS-Allergien).

## Lernziele (laut Vorlesung)

- Identifier-Systeme im eHealth-Kontext kennen (Patientenindex, GDA-Index, OID, PZN, IDMP, bPK-GH …).
- Code Systeme von Value Sets sicher unterscheiden – Eigenschaften „in der idealen Welt".
- Value Set Binding in einem CDA-Leitfaden lesen können (DYNAMIC, Pflicht, OID).
- LOINC-Code zerlegen können (6 Achsen: Component, Property, Time, System, Scale, Method); Fully Specified Name vs. long common name.
- UCUM-Aufbau und Schreibweise verstehen (Präfixe, Basiseinheiten, abgeleitete Einheiten, Syntaxregeln, Annotationen).
- Praktisches Mapping zwischen Lokalsystem, ELGA-CDA und Empfängersystem nachvollziehen.
- Internationale Architekturen erklären (eHDSI/NCP-Modell, MyHealth@EU); IPS-Allergie-Codierung als Beispiel.

## Behandelte Konzepte

### Anwendung in Standards
- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Mapping in CDA]]
- [[MSI - Terminologie - Management in Österreich]]

### Identifikatoren
- [[MSI - Identifikator - OID]]
- [[MSI - Identifikator - Übersicht eHealth]]

### LOINC
- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Inhalt]]
- [[MSI - LOINC - Sechs-Achsen-Struktur]]
- [[MSI - LOINC - Fully Specified Name]]
- [[MSI - LOINC - Verwendung in CDA]]

### UCUM
- [[MSI - UCUM - Definition]]
- [[MSI - UCUM - Aufbau]]
- [[MSI - UCUM - Beispiele]]

### Internationale Anwendungen
- [[MSI - HL7 - eHDSI MyHealth EU]]
- [[MSI - HL7 - IPS Allergie-Codierung]]

## Roter Faden

Wiederholung der eHealth-Terminologien-Auswahl (Folie 5) und Identifier-Systeme (Folie 6) → Begriffsfrage „Was ist ein Value Set?" (Folie 8) → wie findet man Terminologien (Folie 9) → Code Systeme vs. Value Sets in der idealen Welt (Folie 10) → Value Set Binding im CDA-Leitfaden mit OID + DYNAMIC (Folien 11–12) → Terminologien in FHIR (Folie 13: Patient mit Bindings) → Terminologien in HL7 v2 (Folien 14–15: NK1-Beziehung, OBX mit LOINC) → Wartung von Value Sets in ELGA (Folie 16) → Terminologie-Management in Österreich (Folie 17) → Mapping mit konkretem Lab-Beispiel (Folien 18–19) → LOINC im Detail (Folien 21–26) → UCUM im Detail (Folien 27–29) → internationale Value-Set-Beispiele: Lethe-Übung (Folien 31–32), eHDSI/NCP/MyHealth@EU (Folien 33–34), IPS-Allergie-Codierung (Folie 35) → Diskussions-Fragestellung „Welcher Nutzen, wenn alle Diagnosen/Laborwerte/Impfungen/Medikationen in Österreich kodiert wären?" (Folie 36).

## Zentrale Aussagen / Take-aways

- **Value Sets in CDA werden über OID + DYNAMIC referenziert** (Folie 11). Beispiel-OIDs aus Folie 11: ELGA_AllergyOrIntoleranceAgent (`1.2.40.0.34.10.180`), ELGA_AdministrativeGender (`1.2.40.0.34.10.4`), ELGA_MaritalStatus (`1.2.40.0.34.10.11`).
- **Code Systeme sind versionspflichtig**: Bei Löschungen oder Sinnänderungen von Codes muss dem Codesystem eine neue OID gegeben werden – Cimino's „Concept Permanence" auf Implementierungs­ebene.
- **Value Sets sind Anwendungs-spezifisch**: Selber Code kann in mehreren Value Sets erscheinen. Value Sets sollten *nur gültige Codes* enthalten (Verwendung zur Validierung).
- **Wartungs­zyklen**: strukturelle Value Sets (CDA-Header) ändern sich selten; inhaltliche Value Sets (Arzneimittel, Laboranalysen, Diagnose-Codierungen) jährlich bis wöchentlich.
- **Mapping-Praxis** (Folie 18): Lokale Lab-Codes („Eiweiß im Harn", „Protein im Urin", „Gesamteiweiß im Harn", „Gesamteiweiß im Urin", „Totalprotein im Harn") → derselbe Parameter, unterschiedliche Codes/Einheiten. Über LOINC + UCUM lässt sich der Befund vereinheitlichen.
- **LOINC = Logical Observation Identifiers Names and Codes**: 6-Achsen-Struktur (Component:Property:Time:System:Scale:Method), präkoordiniert pro Konzept, betrieben vom Regenstrief Institute (seit 1994), Browser via search.loinc.org.
- **UCUM = Unified Code for Units of Measure**: Schreibweise für Maßeinheiten, eindeutig auf SI-Basiseinheiten umrechenbar; OID `2.16.840.1.113883.6.8`; verwendet von HL7, DICOM, FDA.
- **eHDSI / MyHealth@EU**: NCP-zu-NCP-Architektur für grenzüberschreitenden Datenaustausch (Prescription, Patient Summary). Value Sets einsehbar auf termgit.elga.gv.at.
- **IPS-Allergie-Codierung** (Folie 35): Dimensionen Allergie/Intoleranz, Auslösende Substanz, Manifestation, Kritikalität, Sicherheit der Diagnose, Zeitbereich – jede Dimension hat eigenes ELGA-Value-Set. „No-Info-Codes" für absentOrUnknownAllergies.

## Begleitübungen

- **Lethe Interoperability Framework** als Zwischenübung (Folien 31–32). Aufgabe: Datenfelder (Dementia Type, Water Intake, Smoking, SpO2, Height, Weight, Emotion recording) so spezifizieren, dass semantische Interoperabilität gewährleistet ist – mit Datentyp, FHIR Observation.code (LOINC oder SNOMED), value DT (Quantity oder CodeableConcept), UCUM-Einheit, optional FHIR Profile, optional Value Set (z. B. LetheEmotions als SNOMED-CT-Subset von 106126000 |Emotional state finding|).
- **Übung 2 zweiter Teil: Semantic Dashboard** (Besprechung 14.11.2024). Pfad: `Folien/Medizinische Standards und Semantische Interop/02 Semantik/INF03_Übung 2_semantic.pdf`.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - Semantik Theorie]] (Theorie zu Value Set, Code System; Auswahl-Liste der Terminologien)
- [[MSI - VL - HL7 CDA und e-Befunde]] (CDA-Leitfaden-Mechanik)
- [[MSI - VL - HL7 FHIR und Terminologieserver]] (FHIR-Terminologie-Resources)
- [[MSI - HL7 - International Patient Summary]] (IPS-Allergie als Beispiel)

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/03 Terminologien Anwendung/03_Terminologien_Anwendung.pdf`
- Folienanzahl: 37
- Vortragende: Carina Seerainer, MSc
- Externe Referenzen: search.loinc.org, loinc.org/kb/abbreviations/, unitsofmeasure.org, termgit.elga.gv.at, international-patient-summary.net, ELGA-CDA-Beispielbefunde-GitLab.
