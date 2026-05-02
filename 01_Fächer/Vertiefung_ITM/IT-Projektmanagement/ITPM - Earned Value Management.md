---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Werkzeuge 01]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Earned Value Management

> [!info] Kurzdefinition
> Earned Value Management (EVM, auch Leistungswertanalyse / Fertigstellungswertmethode / Arbeitswertanalyse) ist die Standardmethode des PMBOK Guide für Projekt-Controlling. Sie integriert die drei Größen des Magischen Dreiecks (Zeit, Aufwand, Qualität/Umfang) in eine gemeinsame Bewertung.

## Beschreibung

EVM wurde **1967 vom amerikanischen Verteidigungsministerium** verpflichtend für alle Auftragnehmer eingeführt und ist die Standardmethode des PMBOK Guide für Projekt-Controlling. Die Methode versucht, die drei Elemente des **Magischen Dreiecks** (Zeit, Aufwand, Qualität/Umfang) gleichzeitig in die Projektbeurteilung einfließen zu lassen.

Berechnet werden drei Basiswerte und daraus zwei Leistungs-Indizes, die eine **Prognose des weiteren Projektverlaufs** erlauben.

## Bestandteile / Aufbau

**Basiswerte:**

| Größe | Bedeutung |
|---|---|
| **Earned Value (EV)** | Fertigstellungswert |
| **Actual Cost (AC)** | Ist-Kosten |
| **Planned Value (PV)** | Planwert |

**Indizes:**

- **Cost Performance Index (CPI):** `CPI = EV / AC`
- **Schedule Performance Index (SPI):** `SPI = EV / PV`

**Interpretation:**

| CPI | Bedeutung | SPI | Bedeutung |
|---|---|---|---|
| < 1 | Über Budget | < 1 | Hinter Zeitplan |
| = 1 | Im Budget | = 1 | Im Zeitplan |
| > 1 | Unter Budget | > 1 | Vor Zeitplan |

## Beispiel

*Im PDF nicht durch konkretes Zahlenbeispiel illustriert.* Die Vorlesung verweist auf weiterführende Quellen:
- `https://en.wikipedia.org/wiki/Earned_value_management`
- `https://www.projectsmart.co.uk/earned-value-management-explained.php`
- YouTube-Video: `https://www.youtube.com/watch?v=ijS_8FuiGWU`

## Abgrenzung

- EVM ist eine **klassische** Controlling-Methode und passt zu plan-getriebenen Vorgehen mit fixiertem Umfang.
- In agilen Projekten wird EVM seltener eingesetzt, weil der Umfang dort variabel ist (alternative Metriken: Velocity, Burn-Down/Burn-Up). *(im PDF nicht definiert)*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie werden CPI und SPI berechnet, und wie sind sie zu interpretieren?

**Anwendungsfrage:** Ein Projekt zeigt CPI = 0,8 und SPI = 1,1. Was bedeutet das für Budget und Zeitplan? Welche Steuerungsmaßnahmen leiten Sie ab?

**Diskussionsfrage:** Welche Schwächen hat EVM in IT-Projekten – insbesondere in solchen mit unklaren Anforderungen?

**Mögliche Anschlussfragen:**
- In welchem Standard ist EVM verankert (PMBOK Guide)?
- Welche Voraussetzungen muss die Projektplanung erfüllen, damit EVM überhaupt anwendbar ist?
- Gibt es agile Pendants oder Adaptionen?

## Verwandt

- [[ITPM - Klassisches PM - Definition]]
- [[ITPM - Klassisches PM - Vorteile und Nachteile]]
- [[ITPM - PMBOK - Grundlagen]]
- [[ITPM - Projektsteuerung - Magisches Dreieck]]

## Quelle

- Vorlesung: [[ITPM - VL - Werkzeuge 01]]
- Folien/Seitenangabe: 12–14
