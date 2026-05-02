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

# EHR - MU Stage 3

> [!info] Kurzdefinition
> **Meaningful Use Stage 3** (ab 2017 optional, ab 2018 verpflichtend): dritte und letzte Stufe des Programms mit **vereinfachter Struktur** (8 Core-Requirements für EPs, keine Menu-Optionen mehr). Schwerpunkt: **Interoperabilität, Health Information Exchange und Outcomes**.

## Beschreibung

Aus Folie 32:

> „Optional for providers in 2017. Mandatory for everyone in 2018.
> Physicians: 8 overall (core) requirements. No menu options anymore.
> Hospitals: depend on whether Stage 1 or Stage 2 has been reached."

Aus Folie 33:

> „More emphasis on interoperability and health information exchange.
> MACRA - Medicare Access and CHIP Reauthorization Act of 2015 (CHIP = State Children's Health Insurance Program).
> Moving gradually from 'pay for service' to 'pay for performance' – providers are rewarded for improved health outcomes rather than specific services."

## Bestandteile / Aufbau

### Wesentliche Strukturänderungen gegenüber Stage 2

| Aspekt | Stage 2 | Stage 3 |
|---|---|---|
| Anforderungs-Sets | Core + Menu (Auswahl) | Nur Core (alle verbindlich) |
| Anzahl Anforderungen für EPs | 17 Core + 5/10 Menu = 22 | 8 Core |
| Schwerpunkt | Exchange beginnt | Volle Interoperabilität, Outcomes |
| Optional/Pflicht | – | Optional 2017, mandatory 2018 |

### Verknüpfung mit MACRA

- MACRA (2015): kombiniert Anreize aus mehreren Programmen, schiebt Stage 3 in einen größeren Rahmen
- „Pay for Performance" wird formalisiert
- Hospitals: Anforderungen abhängig davon, welche Stufe sie zuvor erreicht haben

## Beispiel

Ein Hausarzt muss in Stage 3 typischerweise:
1. Patient Electronic Access via FHIR-API anbieten
2. Coordination of Care durch HIE-Teilnahme
3. Public Health and Clinical Data Registry Reporting
4. Strukturierte Patient-generated Health Data einbinden

(Konkrete 8 Core-Requirements im PDF nicht aufgelistet – verweist auf CMS-Originaldokument).

## Abgrenzung

- Stage 3 = letzte Phase des klassischen MU – danach geht das Programm in MIPS (Merit-based Incentive Payment System) unter MACRA über.
- „No menu options anymore": **Vereinheitlichung** als Lehre aus Stage 1/2 – Menu-Auswahl führte zu „Cherry-Picking" einfacher Optionen.
- Hospitals haben eigene, stage-abhängige Anforderungs-Sets – sie sind nicht 1:1 mit den 8 Physician-Cores vergleichbar.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Meaningful Use Stage 3, und wann wurde es verpflichtend?

**Anwendungsfrage:** Warum wurde das Menu-Konzept in Stage 3 abgeschafft? Welcher methodische Lerneffekt steckt dahinter?

**Diskussionsfrage:** „Pay for Performance" über MACRA – welche Anreizverschiebung folgt daraus für Versorger? Welche Risiken bestehen (z. B. Risikoselektion, Code-Inflation)?

**Mögliche Anschlussfragen:**
- Was ist MACRA, und wie verbindet es sich mit MU-3?
- Welche 8 Core-Requirements sind in MU-3 für EPs definiert? (im PDF nicht ausgeführt – Anschlussrecherche an CMS-Quellen)
- Wie wirkt sich MU-3 auf FHIR-Adoption aus?
- Was ist der Unterschied zwischen MU-3 und MIPS Promoting Interoperability?

## Verwandt

- [[EHR - VL - Meaningful Use]]
- [[EHR - MU Stage 2]]
- [[EHR - MACRA und Value Based Care]]
- [[EHR - USCDI US Core Data for Interoperability]]

## Quelle

- Vorlesung: [[EHR - VL - Meaningful Use]]
- Folien/Seitenangabe: Folien 32–33 (MU-3 Status, MACRA, Pay-for-Performance)
