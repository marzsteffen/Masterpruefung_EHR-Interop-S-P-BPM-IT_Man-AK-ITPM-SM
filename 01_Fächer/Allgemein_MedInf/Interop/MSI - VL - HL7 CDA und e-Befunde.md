---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/04 CDA/04_e-Befunde_CDA.pdf
datum_vorlesung: 2024-11-14
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - VL - HL7 CDA und e-Befunde

## Überblick

Längste Vorlesung der LV (69 Folien) zu HL7 CDA in Österreich. Vier Teile: (1) CDA-Auffrischung mit RIM-Fundament, Aufbau, Eigenschaften, Datentypen, OID, codierte Werte, nullFlavor; (2) CDA-Praxis: Anzeige (Stylesheet), Konformitätsprüfung (Schema + Schematron), IHE-XDS-Registrierung, Implementierungsleitfäden, Templates, ART-DECOR; (3) Übernahme maschinenlesbarer Daten: Lab, Diagnose, Medikation – jeweils mit kommentierten CDA-Snippets; (4) Exkurs Usability & Barrierefreiheit (WCAG 2.1, vier Prinzipien).

Die VL deckt weite Teile des Stoffes ab und ist hochgradig prüfungsrelevant – die mündliche Prüfung in MSI berührt CDA fast immer, die Snippet-Lese-Fähigkeit ist erwartet.

## Lernziele (laut Vorlesung)

- CDA als HL7-V3-Standard und ISO/HL7 27932:2009 einordnen, Bezug zum RIM beschreiben.
- Aufbau eines CDA-Dokuments (Header, Body, Sections, Entries) und CDA-Levels (1/2/3) erklären.
- ELGA-Interoperabilitätsstufen (EIS BASIC, STRUCTURED, ENHANCED, FULL SUPPORT) sicher von CDA-Levels trennen.
- CDA-Datentypen kennen (ST, II, CNE/CWE, TS/IVL_TS, PQ/IVL_PQ usw.) und ihre Verwendung erkennen.
- OID-Konzept und Instance Identifier (II) im CDA-Kontext erklären.
- Codierungs-Varianten in CDA verstehen (minimal / gebräuchlich / vollständig mit originalText) inkl. nullFlavor und Translation.
- Konformitätsprüfung mit Schema und Schematron beschreiben (ART-DECOR, ELGA Online-Validator).
- IHE-XDS-Architektur (Patient Identity Source, Document Source/Repository, Registry, Consumer mit ITI-Transaktionen) und Mapping zu CDA-Metadaten benennen.
- CDA Templates auf vier Ebenen (Document/Header/Section/Entry) und ihre Rolle für Konformitätsprüfung erklären.
- WCAG-2.1-Prinzipien (Wahrnehmbar/Bedienbar/Verständlich/Robust) und gesetzliche Verpflichtungen für Barrierefreiheit benennen.

## Behandelte Konzepte

### CDA-Grundlagen
- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 RIM - Reference Information Model]]
- [[MSI - HL7 CDA - R-MIM]]
- [[MSI - HL7 CDA - Eigenschaften]]
- [[MSI - HL7 CDA - Header]]
- [[MSI - HL7 CDA - Body und Sections]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - ELGA - EIS Stufen]]

### Datentypen, Identifikatoren, Codierung
- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - HL7 CDA - II Instance Identifier]]
- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - Terminology Binding]]
- [[MSI - HL7 CDA - nullFlavor]]

### Praxis: Anzeige, Validierung, XDS, Leitfäden
- [[MSI - HL7 CDA - Stylesheet und Validierung]]
- [[MSI - IHE XDS - Architektur]]
- [[MSI - IHE XDS - Dokument-Metadaten]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - ART-DECOR]]
- [[MSI - HL7 CDA - Kardinalität und Konformität]]

### Maschinenlesbare Daten
- [[MSI - HL7 CDA - Laborparameter Entry]]
- [[MSI - HL7 CDA - Problem-Bedenken Entry]]
- [[MSI - HL7 CDA - Medikation Entry]]
- [[MSI - HL7 CDA - Translation]]

### Usability und Barrierefreiheit
- [[MSI - Barrierefreiheit - Definition und Normen]]
- [[MSI - Barrierefreiheit - WCAG Prinzipien]]

## Roter Faden

1. CDA als XML-Standard für medizinische Befunde, ISO/HL7 27932:2009 → 2. Schematischer Aufbau (Header + Body + Entries) und XML-Sicht → 3. CDA basiert auf RIM (HL7 V3, ISO/HL7 21731:2006); RIM-Backbone Entity/Role/Participation/Act + Role Link/Act Relationship → 4. R-MIM als CDA-spezifische Refined Sicht → 5. Eigenschaften medizinischer Dokumente (Persistenz, Verwaltung, Kontext, Authentisierung, Ganzheit, Lesbarkeit) → 6. ELGA-CDA-Header und Body-Daten (Pflichtsektionen Entlassungsbrief) → 7. CDA-Levels 1/2/3 vs. ELGA-EIS-Stufen → 8. Datentypen, II/OID, codierte Werte, Terminology Binding (DYNAMIC/STATIC), nullFlavor → 9. Praxis: Stylesheet, Schema, Schematron, ELGA-Online-Validator, IHE-XDS-Architektur, Dokument-Metadaten → 10. Implementierungsleitfäden + Templates (4 Ebenen) + ART-DECOR + Kardinalität (M/R/O, must support) → 11. Übernahme maschinenlesbarer Daten an Lab/Diagnose/Medikation-Entries mit kommentierten Snippets → 12. Exkurs Usability/Barrierefreiheit (Bevölkerungsstatistik 30 % behindert/chronisch krank, §4 BGG, WCAG 2.1, vier Prinzipien).

## Zentrale Aussagen / Take-aways

- **CDA ≠ HL7 V3**, sondern **Teil von HL7 V3** und basiert auf RIM. Verwechslung kostet Punkte.
- **CDA-Level ≠ ELGA-EIS-Stufe.** CDA-Level beschreibt die *Strukturierungstiefe des Body* (1 unstrukturiert / 2 Section-strukturiert / 3 Entry-strukturiert). EIS-Stufe ist eine ELGA-spezifische **Konformitätsstufe** zu Implementierungsleitfäden (BASIC/STRUCTURED < ENHANCED < FULL SUPPORT).
- **Sechs Eigenschaften eines CDA-Dokuments**: Persistenz, Verwaltung (stewardship/Custodian), Kontext, Authentisierung (potential für authentication), Ganzheit (wholeness), Lesbarkeit (human readability) – Lesbarkeit auch *ohne* spezifisches Stylesheet möglich.
- **OID ist ISO/IEC 9834-1**: hierarchische Baumstruktur, Dot-Notation, Eindeutigkeit durch Registrierungsstellen. OID-Baum ist organisatorisch, nicht inhaltlich. Österreichisches OID-Portal verpflichtet zur Meldung wichtiger OIDs.
- **Codierte Werte in CDA** kommen in drei Varianten: minimal (code + codeSystem), gebräuchlich (+ displayName + codeSystemName), vollständig (+ codeSystemVersion + originalText/reference).
- **nullFlavor**: NI (no information), UNK (unknown), MSK (masked), NA (not applicable), OTH (other) – wenn nullFlavor gesetzt, dürfen keine anderen Attribute mit Wert gleichzeitig stehen. Für codierte Elemente bevorzugt der ELGA-Leitfaden konkrete Codes („716186003 No known allergy" SNOMED) gegenüber nullFlavor.
- **Schematron ergänzt das XML-Schema**: Schema prüft Struktur/Datentypen, Schematron prüft inhaltliche Constraints inkl. Value Sets und Templates. ELGA Online-Validator nutzt beide.
- **IHE XDS-Akteure** (Folie 34): Patient Identity Source, Document Source, Document Repository, Document Registry, Document Consumer, On-Demand Document Source. Transaktionen ITI-8/ITI-44 (Patient Identity Feed), ITI-41 (Provide & Register), ITI-42 (Register Document Set-b), ITI-43 (Retrieve Document Set), ITI-18 (Registry Stored Query), ITI-61 (Register On-Demand).
- **Templates haben vier Ebenen**: Document Level (Gesamtstruktur), Header Level (Metadaten), Section Level (Abschnitte), Entry Level (codierte Einträge). Plus „Compilations" wie Adresspartikel.
- **Translation-Mechanismus**: Wenn lokal kein Code aus dem ELGA-Value-Set passt, kann `<code nullFlavor="OTH">` mit `<originalText>` und `<translation code="…">` in einem alternativen System (z. B. LOINC oder SNOMED CT) verwendet werden.
- **Barrierefreiheit ist gesetzlich vorgeschrieben** für Behörden, Bundesverwaltung (BGStG), Verkäufer öffentlich angebotener Güter und Bundesförderungs­nehmer. WCAG 2.1 hat vier Prinzipien: Wahrnehmbar, Bedienbar, Verständlich, Robust.

## Begleitübungen

- **`INF03_Übung 4_CDA-Laborbefund.pdf`** – nach Vorgabe des Nutzers in dieser Note **bewusst ausgelassen** und nicht als Konzept-Note erfasst. Pfad: `Folien/Medizinische Standards und Semantische Interop/04 CDA/INF03_Übung 4_CDA-Laborbefund.pdf`. Falls die Übung später für die Prüfungsvorbereitung doch relevant wird: gezielt nachladen.
- **CDA-Materialien-Ordner** auf Moodle/im Vault enthält XML-Beispielbefunde (`Entlassungsbrief_BeispielA.xml`, `Entlassungsbrief_BeispielA_Fehler.xml`, `ELGA-043-Laborbefund_EIS-FullSupport.xml`), Stylesheet (`ELGA_Stylesheet_v1.0.xsl`) und Changelog. Diese Materialien werden in den „hands on"-Folien (15, 30, 33) referenziert.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - Einführung in Standards und Interoperabilität]]
- [[MSI - VL - Semantik Theorie]] (Konzept Bezeichnung Code, Cimino-Desiderata)
- [[MSI - VL - Terminologien Anwendung]] (LOINC, UCUM, Value Sets, OID, Mapping in CDA)
- [[MSI - VL - HL7 FHIR und Terminologieserver]] (FHIR als Nachfolger, Vergleich)
- [[EHR - ELGA - Architektur]] (Cross-Fach – ELGA als CDA-Anwender)
- [[ASP - MOC]] (Authentisierung, signatureCode)

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/04 CDA/04_e-Befunde_CDA.pdf`
- Folienanzahl: 69
- Vortragende: Carina Seerainer, MSc
- Externe Referenzen: HL7-AT-Wiki (`https://wiki.hl7.at/`), `https://elga.art-decor.org/`, ELGA Online-Validator (`https://ovp.elga.services.at/validation.html`), OID-Portal (`https://www.gesundheit.gv.at/OID_Frontend/`), WCAG 2.1 (`https://www.w3.org/TR/WCAG21/`).
