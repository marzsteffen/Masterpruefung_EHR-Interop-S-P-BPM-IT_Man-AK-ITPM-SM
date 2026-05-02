---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Macro-Level Interoperabilität]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Indikatoren - WHO 100 Core Health Indicators

> [!info] Kurzdefinition
> Globale Referenzliste der WHO mit 100 standardisierten Kern-Indikatoren zur Bewertung des Gesundheitszustands von Bevölkerungen. Macht Public-Health-Vergleiche zwischen Ländern erst möglich, weil sie Numerator, Denominator, Disaggregation und Methode festlegt.

## Beschreibung

Vorlesung verweist auf die WHO-Liste der 100 Core Health Indicators (SCORE for health data). Beispiel-Indikator (Folie):

**Tobacco use among persons aged 15+ years [SDG 3.a.1]**
- **Definition:** age-standardized prevalence of current tobacco use among persons aged 15+ years
- **Smoked tobacco products:** Zigaretten, Zigarillos, Zigarren, Cheroots, Bidis, Pipes, Shisha, roll-your-own, Kreteks etc.
- **Smokeless tobacco:** Snuff, Plug, Snus, Chimo, Gutkha, Khaini, Pan etc.
- **Current use:** Nutzung zum Zeitpunkt der Befragung, täglich oder gelegentlich
- **Numerator:** Anzahl aktueller Tabaknutzer ≥ 15 Jahre
- **Denominator:** Gesamtbevölkerung ≥ 15 Jahre
- **Disaggregation:** Alter, Geschlecht
- **Method:** (Anzahl Befragte ≥ 15 die Tabak nutzen) / (Anzahl Befragte ≥ 15) × 100

## Bestandteile / Aufbau

Jeder Core Health Indicator hat:
- **SDG-Referenz** (Sustainable Development Goal)
- **Definition**
- **Numerator** (Zähler)
- **Denominator** (Nenner)
- **Disaggregation** (welche zusätzlichen Dimensionen ausgewertet werden, typischerweise Alter und Geschlecht)
- **Method** (Berechnungsformel)

## Beispiel

Public-Health-Researcher will Risikofaktoren für kardiovaskuläre Erkrankungen untersuchen → braucht **Smoking Status** der Bevölkerung. Wenn Smoking Status nicht strukturiert in EHRs liegt (siehe LCIM Schicht „Syntax and Semantics"), muss er ihn neu erheben. Die WHO-Indikatoren-Definition gibt ihm vor, *wie* er ihn definieren soll.

## Abgrenzung

- 100 Core Health Indicators sind **Public-Health-Indikatoren**, nicht klinische Indikatoren – sie messen Bevölkerungsgesundheit.
- Sie sind **nicht** dasselbe wie Quality Indicators (Krankenhaus-Qualitäts­messung) oder klinische Outcomes.
- Quelle: WHO SCORE-Tools, verlinkt im PDF: score.tools.who.int/tools/enable-data-use-for-policy-and-action/tool/global-reference-list-of-100-core-health-indicators-72/

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wozu dient die WHO-Liste der 100 Core Health Indicators?

**Anwendungsfrage:** Welche Komponenten enthält ein Indikator wie SDG 3.a.1, und warum ist die genaue Definition von Numerator und Denominator essenziell?

**Diskussionsfrage:** Warum gelingt es vielen EHR-Systemen nicht, diese Indikatoren ohne zusätzliche manuelle Erhebung zu liefern? Welche Schicht von LCIM verhindert das?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen Smoked und Smokeless Tobacco im Indikator?
- Wie würde man Smoking Status in einem FHIR-Profil strukturieren, damit dieser Indikator automatisch ableitbar ist?
- Welche Rolle spielen die SDGs für Public-Health-Reporting?

## Verwandt

- [[EHR - Interoperabilität - LCIM nach Tolk]]
- [[EHR - Datensharing - Logic Modes]]
- [[EHR - Standards - Unterstützte Coding Standards]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folien „WHO List of 100 Core Health Indicators", „Tobacco use among persons aged 15+ years"
