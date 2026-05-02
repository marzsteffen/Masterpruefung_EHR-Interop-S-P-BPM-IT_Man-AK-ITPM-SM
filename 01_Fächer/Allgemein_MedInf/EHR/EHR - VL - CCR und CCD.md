---
fach: ehr
typ: vorlesung
status: offen
quelle_pdf: SS24_CCR-CCD.pdf
datum_vorlesung: SS2024
tags:
  - fach/allgemein/ehr
  - typ/vorlesung
  - status/offen
---

# EHR - VL - CCR und CCD

## Überblick

Vorlesung zu **Continuity of Care Record (CCR)** und **Continuity of Care Document (CCD)** als US-amerikanischen Austausch-Standards für klinische Versorgungs-Zusammenfassungen. Eingebettet in eine Einleitung zur modernen EHR-Welt (zentralisierte vs. dezentralisierte Gesundheitssysteme, Interoperabilitäts-Schichten, Trennung System ↔ Exchange-Format) und mit einem Schlenker zur österreichischen ELGA-Architektur. Der Hauptteil behandelt CCR (ASTM E2369-12), CCD (HL7-CDA-Implementation des CCR), C-CDA (Consolidated CDA) und ihre Rolle in Meaningful Use Stage 1/2.

## Lernziele (laut Vorlesung)

Implizit:
- Gesundheitssystem-Typen (zentral, semi-zentral, dezentral) nach ihren EHR-Architektur-Konsequenzen einordnen
- Strukturelle und semantische Interoperabilität abgrenzen
- System ≠ Exchange-Format als grundlegende Trennung verinnerlichen
- ELGA-Architektur in Grundzügen kennen (CDA, IHE-Profile, dezentrale Repositories)
- CCR und CCD inhaltlich und technisch unterscheiden
- C-CDA als Konsolidierung mehrerer CDA-Dokumenttypen verstehen
- Den MU-Bezug der CCR/CCD einordnen

## Behandelte Konzepte

### Kontextueller Rahmen
- [[EHR - Healthcare Systems - Zentralisierungs-Modelle]]
- [[EHR - Interoperabilität - Strukturell vs Semantisch]]
- [[EHR - System vs Exchange Format]]

### Österreichischer Kontext
- [[EHR - ELGA - Technologie-Architektur]]

### CCR und seine Implementierungen
- [[EHR - CCR - Continuity of Care Record]]
- [[EHR - CCR - Patient Identification]]
- [[EHR - CCD - Continuity of Care Document]]
- [[EHR - C-CDA - Consolidated CDA]]
- [[EHR - HL7 CDA - RIM-Basis]]

## Roter Faden

Die Vorlesung beginnt mit einer Einordnung: EHRs sind heute weltweit verbreitet, aber **Interoperabilität bleibt das Hauptproblem**. Die Vorlesung trennt strukturelle (Format) und semantische (Coding) Interoperabilität und betont, dass semantische Interoperabilität schwieriger ist – mit globalen Standardisierungs­tendenzen zu LOINC, SNOMED-CT, UCUM, ATC, ICD.

Eine zentrale konzeptuelle Trennung wird eingeführt: **EHR als System vs. Exchange-Format**. Selbst wenn alle Krankenhäuser eines Landes dasselbe System nutzen (Slowenien-Beispiel mit OpenEHR), bleibt ein Exchange-Format nötig, sobald Daten zwischen Stellen oder zum Patienten fließen sollen.

Österreich wird als Beispiel diskutiert: ELGA basiert auf **HL7-v3 CDA (XML)** mit **dezentralen Repositories** und einem **zentralen System für Zugriffsautorisierung und Document-Lookup über IHE-Profile (XDS)**. e-Medikation (2017–2018) und e-Impfpass (2021) sind Erweiterungen.

Der Hauptteil widmet sich der US-Antwort: **CCR** (Continuity of Care Record, ASTM E2369-12) als XML-Spezifikation für eine kompakte Versorgungs­zusammenfassung mit 6 Sektionen, gemeint als „minimum requirement" für EHR-Exchange im Rahmen von Meaningful Use. CCR ist **kein vollständiger Health Record**, sondern eine **Summary**.

CCR hat zwei Implementierungen: **ASTM-XML** (verblasst) und **CCD** (HL7-CDA-Implementation – bevorzugt). CCD baut auf dem **HL7 RIM** (Reference Information Model) auf – jedes XML-Element muss einer RIM-Klasse oder einem Klassen-Attribut entsprechen.

In **MU Stage 2** wurde **C-CDA** (Consolidated CDA) standardisiert: 9 Dokumenttypen, von denen CCD einer ist. C-CDA ist heute der dominante US-Dokumenten-Standard für Care Transitions.

## Zentrale Aussagen / Take-aways

- Interoperabilität ist mehr als Format: strukturell, semantisch, prozessual.
- EHR-System und Exchange-Format sind zwei verschiedene Dinge – auch eine homogene Systemwelt braucht einen Exchange-Standard.
- ELGA setzt CDA + IHE-XDS ein, mit dezentralen Repositories und zentralem Index.
- CCR ist eine Summary, nicht ein Full Record. 6 Sektionen mit Mandated Core und Optional Extensions.
- CCD = HL7-CDA-Implementation des CCR; CCD wurde in MU Stage 1 als bevorzugter Exchange-Standard etabliert.
- C-CDA bündelt 9 Dokumenttypen unter einer konsolidierten Spezifikation und ist seit MU Stage 2 verpflichtend.

## Querverweise zu anderen Vorlesungen

- [[EHR - VL - Meaningful Use]] – CCR/CCD als verpflichtender Exchange-Standard in MU 1/2
- [[EHR - VL - Einführung und Definitionen]] – Standards (HL7, ICD, SNOMED, LOINC) und Architektur-Designfragen
- [[EHR - VL - Macro-Level Interoperabilität]] – Tolk LCIM strukturell/semantisch/prozessual
- [[EHR - VL - FHIR Grundlagen]] – FHIR als Nachfolger von CDA/CCD im Exchange
- [[MSI - HL7 CDA]] – CDA als Container-Standard
- [[MSI - HL7 - RIM]] – Reference Information Model als Basis für CDA
- [[MSI - IHE XDS]] – IHE Cross-Enterprise Document Sharing als ELGA-Backbone

## Quelle

- PDF: SS24_CCR-CCD.pdf
- Folienanzahl: 30
- Vortragender: DI Dr. Sten Hanke
- Eingebettete Folien-Auszüge: Conceptual Model des CCR (Jozef Aerts, SS 2019)
