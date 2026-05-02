---
fach: itm-ak
typ: konzept
status: offen
quelle: "[[ITM-AK - VL - Controlling]]"
tags:
  - fach/vertiefung/itm-ak
  - typ/konzept
  - status/offen
---

# ITM-AK - DRG und LKF

> [!info] Kurzdefinition
> DRGs (Diagnosis Related Groups) sind ein Erstattungssystem, bei dem ähnliche Behandlungsfälle pauschal vergütet werden. In Österreich heißt das System LKF (Leistungsorientierte Krankenanstaltenfinanzierung) – das Krankenhaus erhält Punkte je Fall, die in Euro umgerechnet werden.

## Beschreibung

### Hintergrund (Folie 50)
- Erstattung im Krankenhaus.
- Unterscheidung von Krankheiten und Patient:innen nach **Schwere der Krankheit, Alter, Operationen, ICU, Medikamente**.
- **Diagnosenbezogene Gruppen (DRGs).**
- In Österreich: **LKF.**

### Krankenhaus­vergütung (Folie 51)
- Basierend auf der Kodierung erhält das Krankenhaus **Punkte (Österreich) oder Geld** (z. B. Fallpauschale in Deutschland).

### Krankenhauskostenerstattung in Österreich (Folie 53)
- **LKF-System**
- **MBDS-Datensatz**
- **Xdok (Jahr)**
- **Berechnung der Punkte**
- **Umrechnung in Euro**

## Bestandteile / Aufbau

| Element | Funktion |
|---|---|
| **DRG (international)** | Einteilung der Fälle in Gruppen mit ähnlichem Ressourcenverbrauch |
| **LKF (Österreich)** | Punkte-System für stationäre Leistungen |
| **MBDS** | Mindestbasisdatensatz – die Datenbasis für die Punkteberechnung (siehe [[ITM-AK - ICD-10 und MBDS]]) |
| **Xdok** | Software zur Erfassung (jahresaktuell) |
| **Punkte-zu-Euro-Umrechnung** | Konvertierung in Erstattungswert |

Folie 54 zeigt zwei Test-Patient-Beispiele aus dem KDok-System des BMG:
- Testpatient ohne Aufdehnung (Diabetes mellitus mit Fehl-/Mangelernährung): **1.860 Punkte**.
- Testpatient mit Aufdehnung (PTA – perkutane transluminale Angioplastie): **3.383 Punkte**.

## Beispiel

Im PDF anhand der LKF-Screenshots (Folie 54). Konkrete Punkte-zu-Euro-Werte und das Punktegewicht pro Diagnose werden im PDF nicht angegeben, da diese jährlich variieren.

## Abgrenzung

- **DRG ≠ LKF:** DRG ist der internationale Begriff (USA, Deutschland mit G-DRG); LKF ist die österreichische Variante. Beide folgen demselben Prinzip: Gruppierung nach Diagnose, Pauschalvergütung.
- **DRG/LKF ≠ Fee-for-Service:** Fee-for-Service vergütet einzelne Leistungen; DRG/LKF pauschalisiert über Fall.
- **DRG/LKF ≠ Bundled Payments:** DRG/LKF deckt typischerweise nur die stationäre Akutphase; Bundled Payments umspannen den vollen Care Cycle inkl. ambulant/Reha (siehe [[ITM-AK - Bundled Payments und Value-Based Reimbursement]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Erläutern Sie DRG, MBDS und wie sie mit der Krankenhausvergütung zusammenhängen." (Frage zur Wiederholung Folie 62)

**Anwendungsfrage:** „Wie funktioniert die Krankenhausvergütung im österreichischen Gesundheitswesen?" (Frage zur Wiederholung Folie 62)

**Diskussionsfrage:** Welche Anreize setzt das LKF-System – und wo führt es zu Fehlsteuerung?
- Positiv: Vergleichbarkeit und Transparenz; Effizienzanreiz pro Fall.
- Risiken: Up-Coding (Diagnose schwerer codieren als nötig); Drehtüreffekt (frühe Entlassung, dann Wiederaufnahme); Abwälzung auf Reha; Vermeidung kostenintensiver, niedrig vergüteter Patient:innen.
- Bezug zu Porter/Kaplan 2011: DRG/LKF beheben das Costing-Problem nicht, weil sie Erstattung ohne Cycle-Cost-Bezug pauschalieren.

**Mögliche Anschlussfragen:**
- Wie wird das LKF-Punktegewicht ermittelt?
- Welche Rolle spielt das österreichische LKF gegenüber dem deutschen G-DRG?
- Wie verändern Bundled Payments die DRG-/LKF-Logik?

## Verwandt

- [[ITM-AK - Medizinisches Controlling]]
- [[ITM-AK - ICD-10 und MBDS]]
- [[ITM-AK - A-IQI - Austrian Inpatient Quality Indicators]]
- [[ITM-AK - Bundled Payments und Value-Based Reimbursement]]
- [[ITM-AK - Costing Myth - Charges als Cost Surrogate]]
- [[EHR - ELGA - Architektur]]

## Quelle

- Vorlesung: [[ITM-AK - VL - Controlling]]
- Folien/Seitenangabe: 50–54
