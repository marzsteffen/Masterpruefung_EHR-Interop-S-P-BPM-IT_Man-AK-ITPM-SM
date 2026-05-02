---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Meaningful Use]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Clinical Quality Measures CQM

> [!info] Kurzdefinition
> **Clinical Quality Measures (CQM)** sind standardisierte, messbare Indikatoren der klinischen Versorgungsqualität, die unter Meaningful Use von Providern an CMS berichtet werden müssen. Bilden zusammen mit „Use" und „Exchange" die dritte Hauptkomponente des Programms.

## Beschreibung

CQMs sind **standardisierte Qualitäts­indikatoren** – jede mit definiertem Zähler, Nenner und ggf. Ausschlüssen, vergleichbar zur Logik der WHO 100 Core Health Indicators ([[EHR - Indikatoren - WHO 100 Core Health Indicators]]). Sie werden vom Secretary of Health and Human Services bzw. CMS ausgewählt und regelmäßig aktualisiert.

## Bestandteile / Aufbau

### Anzahlen unter MU Stage 1

- **Eligible Professionals (EPs):** 6 CQMs gesamt – 3 aus Core/Alternate Core + 3 aus zusätzlichem Set von 38
- **Hospitals:** 15 CQMs

### Aufbau eines CQM (analog zu WHO Indikatoren)

- **Numerator:** Zähler (Anzahl der Patienten, die das Qualitätsziel erreichen)
- **Denominator:** Nenner (Anzahl der eligible Patienten in der Zielpopulation)
- **Exclusions:** Ausschlüsse (z. B. Patienten mit Kontraindikationen)
- **Stratification:** Aufschlüsselung nach Alter, Geschlecht, ethnischer Zugehörigkeit
- **Time period:** Erfassungszeitraum (typischerweise Kalenderjahr oder Reporting Period)

### Beispiel-CQMs (Ergänzung außerhalb der Vorlesung – im PDF nicht ausgeführt)

- Diabetes: HbA1c Poor Control (Patienten mit HbA1c > 9 %)
- Hypertonie: Controlling High Blood Pressure (Patienten mit BP < 140/90)
- Krebsvorsorge: Cervical Cancer Screening
- Tabakprävention: Tobacco Use Screening and Cessation Intervention

## Beispiel

CQM „Controlling High Blood Pressure":
- **Denominator:** Patienten 18–85 mit Hypertonie-Diagnose im Reporting-Jahr
- **Numerator:** davon Patienten mit BP < 140/90 in der letzten Visite des Jahres
- **Result:** Anteil als Performance-Wert
- Ein Provider mit hohem Anteil erhält Anreiz; mit niedrigem Anteil ggf. Payment Adjustment.

## Abgrenzung

- CQM ≠ Process Measure ausschließlich: CQMs umfassen Process- (wurde X getan?), Outcome- (wurde Ziel erreicht?) und Patient-Experience-Measures.
- CQM ≠ alle Quality Measures – das CMS unterhält weitere Measure-Sets (z. B. HEDIS, Hospital Compare).
- CQM ≠ WHO Core Health Indicators: CQM sind US-spezifisch und versorger-bezogen, WHO 100 sind international und bevölkerungs­bezogen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind Clinical Quality Measures, und welche Rolle spielen sie im Meaningful Use Programm?

**Anwendungsfrage:** Skizziere ein CQM für die Diabetes-Versorgung – Numerator, Denominator, Exclusions.

**Diskussionsfrage:** CQM-Reporting setzt strukturierte Daten im EHR voraus. Welche strukturellen Hürden gibt es in der Praxis (Free-Text-Notes, fehlende Codes, Daten in PDFs)?

**Mögliche Anschlussfragen:**
- Welche CQMs sind Process-, welche Outcome-Measures?
- Wie verhält sich CQM zu Pay for Performance (MACRA)?
- Welche Standards definieren CQMs technisch? (Antwort: HQMF / Health Quality Measure Format; QRDA / Quality Reporting Document Architecture; eCQM)
- Wie werden CQMs aus FHIR-Daten gerechnet? (Stichwort: CQL – Clinical Quality Language)

## Verwandt

- [[EHR - VL - Meaningful Use]]
- [[EHR - Meaningful Use - 3 Hauptkomponenten]]
- [[EHR - MU Stage 1]]
- [[EHR - MACRA und Value Based Care]]
- [[EHR - Indikatoren - WHO 100 Core Health Indicators]]

## Quelle

- Vorlesung: [[EHR - VL - Meaningful Use]]
- Folien/Seitenangabe: Folien 9, 12, 14 (CQM als 3. Hauptkomponente, Anzahl Anforderungen)
