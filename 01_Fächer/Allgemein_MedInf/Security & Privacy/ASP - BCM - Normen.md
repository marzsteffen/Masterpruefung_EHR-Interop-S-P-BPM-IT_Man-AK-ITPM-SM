---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Business Continuity Management]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - BCM - Normen (BSI 200-4, BSI 100-4, BSI 100-2, ISO 27005)

> [!info] Kurzdefinition
> Vier in der Vorlesung genannte Normen rund um BCM und Risikomanagement: BSI 200-4 (Business Continuity Management), BSI 100-4 (Notfallmanagement, Vorgänger), BSI 100-2 (IT-Grundschutz Vorgehensweise), ISO 27005:2022 (Informationssicherheits-Risikomanagement).

## Beschreibung

Folie 7 (BIA) und Folie 22 (Risikodefinition) nennen die relevanten Normen.

### BSI 200-4 – Business Continuity Management
- **Aktueller BSI-Standard für BCM.**
- Definiert u. a. den Begriff BCM-Risiko: „Risiken, die sich unmittelbar auf die Verfügbarkeit von zeitkritischen Ressourcen auswirken."

### BSI 100-4 – Notfallmanagement
- **Vorgänger-Standard von BSI 200-4** (Notfallmanagement-Standard im IT-Grundschutz-Kompendium älterer Generation).
- Im PDF nur als Bullet-Point in Folie 7 erwähnt, ohne weitere Erklärung.

### BSI 100-2 – IT-Grundschutz Vorgehensweise
- **Allgemeine IT-Grundschutz-Methodik** des BSI.
- Im PDF nur als Bullet-Point in Folie 7 erwähnt.

### ISO 27005:2022 – Informationssicherheits-Risikomanagement
- Internationaler Standard für Informationssicherheits-Risikomanagement.
- Definiert Risiko als „effect of uncertainty on objectives".
- Im Kontext Informationssicherheit: „Information security risks can be expressed as effect of uncertainty on information security objectives."
- Bezieht sich auf Ausnutzung von Schwachstellen von Informationswerten.

## Bestandteile / Aufbau

| Norm | Herausgeber | Geltungsbereich | Status |
|---|---|---|---|
| BSI 200-4 | BSI (Deutschland) | Business Continuity Management | aktuell |
| BSI 100-4 | BSI (Deutschland) | Notfallmanagement | älterer Standard |
| BSI 100-2 | BSI (Deutschland) | IT-Grundschutz Vorgehensweise | älterer Standard |
| ISO 27005:2022 | ISO/IEC | Informationssicherheits-Risikomanagement | aktuell, Version 2022 |

## Beispiel

Wer in Österreich ein BCMS aufbaut, würde sich primär an **BSI 200-4** für die Methodik und an **ISO 27005** für die Risikobegriffe orientieren. BSI 100-2/100-4 sind in der österreichischen Praxis weniger gebräuchlich; sie werden vor allem in Deutschland im Bundesverwaltungs-Umfeld angewandt.

## Abgrenzung

- **BSI 200-x ist die neue Generation**, die BSI 100-x ablöst. BSI 100-2 und 100-4 werden in der Vorlesung nur als Kontext genannt.
- **BSI vs. ISO:** BSI ist ein deutscher (sehr detaillierter) Standard. ISO ist international, abstrakter. In der Praxis ergänzen sie sich.
- **Im PDF werden NIST-Standards (z. B. NIST SP 800-34 für Contingency Planning) nicht erwähnt** – relevant in nordamerikanischen Kontexten, aber außerhalb dieser Vorlesung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Normen sind für BCM und BCM-Risikomanagement relevant?

**Anwendungsfrage:** Welche Norm würden Sie anwenden, um a) ein BCMS aufzubauen, b) Risiken zu bewerten?

**Diskussionsfrage:** Welche Vor- und Nachteile bringt die Orientierung an BSI vs. ISO? (BSI: sehr detailliert, deutsch; ISO: international, abstrakter, kompatibler mit globalen Audits.)

**Mögliche Anschlussfragen:**
- Welche aktuelle Version hat ISO 27005? (2022.)
- Was ist der Unterschied zwischen BSI 200-4 und BSI 100-4?
- Welche andere Norm wäre relevant, wird aber im PDF nicht genannt? (ISO 22301 für BCM auf internationaler Ebene – im PDF nicht erwähnt.)

## Verwandt

- [[ASP - BCM - Risikoanalyse]]
- [[ASP - BCM - Business Impact Analyse]]
- [[ASP - BCM - Managementsystem]]
- [[ASP - VL - Informationssicherheits-Risikomanagement]]

## Quelle

- Vorlesung: [[ASP - VL - Business Continuity Management]]
- Folien/Seitenangabe: Folien 7, 22

## Ergänzung außerhalb der Vorlesung

International für BCM relevant ist auch **ISO 22301** (Societal security – Business continuity management systems), das parallel zu BSI 200-4 verwendet wird. ISO 27001/27002 betreffen das Information Security Management System (ISMS). NIST SP 800-34 („Contingency Planning Guide") ist das US-amerikanische Pendant zu BSI 200-4. Die ISO-27005-Version 2022 ersetzt die Version 2018 und harmonisiert stärker mit ISO 31000 (allgemeines Risikomanagement).
