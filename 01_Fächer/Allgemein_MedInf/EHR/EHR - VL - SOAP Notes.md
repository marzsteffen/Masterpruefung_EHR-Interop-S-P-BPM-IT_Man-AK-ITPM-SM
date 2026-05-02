---
fach: ehr
typ: vorlesung
status: offen
quelle_pdf: SS23 SOAP.pdf
datum_vorlesung: SS2023
tags:
  - fach/allgemein/ehr
  - typ/vorlesung
  - status/offen
---

# EHR - VL - SOAP Notes

## Überblick

Vorlesung zu **SOAP-Notes** als zentralem Dokumentationsformat in der ärztlichen Versorgung. Das Akronym steht für **S**ubjective, **O**bjective, **A**ssessment, **P**lan und folgt dem natürlichen Ablauf einer Patientenbegegnung. Die Vorlesung erklärt jede Komponente, zeigt Beispiele, diskutiert Progress Notes und Templates in EMR-Systemen sowie die Variante **APSO**.

## Lernziele (laut Vorlesung)

Implizit aus dem Aufbau:
- Das SOAP-Prinzip definieren und an einem Patientenbeispiel anwenden können
- Inhalte jeder der vier SOAP-Komponenten unterscheiden
- Coding-Bezug der Assessment-Komponente kennen (ICD-10, SNOMED-CT)
- Die Plan-Komponente in ihre Sub-Komponenten zerlegen können
- SOAP von APSO unterscheiden und die Diskussion einordnen

## Behandelte Konzepte

### Das SOAP-Prinzip
- [[EHR - SOAP - Prinzip]]

### Die vier Komponenten
- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Plan]]

### Anwendung im EMR
- [[EHR - SOAP - Progress Notes]]
- [[EHR - SOAP - Templates]]
- [[EHR - SOAP - APSO Variante]]

## Roter Faden

Die Vorlesung beginnt mit der Beobachtung, dass „Healthcare is event driven" – ein Patient kommt, weil etwas nicht stimmt. Daraus leitet sich der natürliche Ablauf einer Visite ab: Der Arzt fragt zuerst (Subjective), misst dann (Objective), schließt daraus eine Diagnose (Assessment) und plant die Behandlung (Plan).

Jede der vier Komponenten wird einzeln charakterisiert: Subjective enthält die narrative Patientenschilderung mit Onset, Chronology, Quality, Severity, modifying factors. Objective umfasst alle messbaren, reproduzierbaren Fakten. Assessment ist die ärztliche Diagnose – narrativ und/oder kodiert (ICD-10, später SNOMED-CT). Plan beschreibt die Behandlung in mehreren Sub-Komponenten (Diagnostic, Therapeutic, Referrals, Patient Education, Disposition).

Anschließend diskutiert die Vorlesung, wie SOAP-Notes in **Progress Notes** wiederkehren – jede Folge-SOAP-Note baut auf der vorigen auf (S: Vergleich mit prior complaints; O: Verlaufsmessung; A: war die Diagnose richtig; P: ggf. Behandlung anpassen). Customized SOAP **Templates** in EMR-Systemen erhöhen Effizienz und Vollständigkeit, etwa für Verletzungs- oder Diabetes-Routinen.

Den Abschluss bildet die **APSO-Variante** – manche Ärzte lesen lieber „Assessment, Plan, Subjective, Objective", weil so die Diagnose und der Behandlungsplan vorne stehen.

## Zentrale Aussagen / Take-aways

- SOAP folgt dem natürlichen Visiten-Ablauf – das macht es als Dokumentationsraster intuitiv und international etabliert.
- Die Trennung zwischen Subjective (Patient sagt) und Objective (gemessen/beobachtet) ist zentral – sie macht klinisches Denken transparent.
- Assessment ist der einzige Teil, in dem die Diagnose explizit gemacht wird – inklusive Coding für Reimbursement und Statistik.
- Plan ist nicht nur „Therapie", sondern enthält auch Diagnostik, Überweisungen, Patientenaufklärung und Entlassungs-Disposition.
- Progress Notes verbinden mehrere SOAP-Notes zu einem Verlauf – die Struktur erlaubt Vergleichbarkeit über Zeit.
- APSO ist nicht ein anderer Inhalt, sondern eine andere **Lese-Reihenfolge** – die Diskussion betrifft Lesbarkeit, nicht Vollständigkeit.

## Querverweise zu anderen Vorlesungen

- [[EHR - VL - Einführung und Definitionen]] – problem-orientierter Record als 3D-Datenmodell mit SOAP als 3. Dimension
- [[EHR - Datenmodelle - Klassische Record Typen]] – SOAP als Sub-Struktur des problem-orientierten Records
- [[EHR - VL - CCR und CCD]] – CCR/CCD enthalten SOAP-artige Strukturen
- [[EHR - VL - FHIR Grundlagen]] – Encounter/Observation/Condition/CarePlan als FHIR-Pendant zu SOAP
- [[MSI - ICD-10]] – Coding der Assessment-Komponente
- [[MSI - SNOMED CT]] – Coding der Assessment-Komponente

## Quelle

- PDF: SS23 SOAP.pdf
- Folienanzahl: 21
- Vortragender: DI Dr. Sten Hanke
