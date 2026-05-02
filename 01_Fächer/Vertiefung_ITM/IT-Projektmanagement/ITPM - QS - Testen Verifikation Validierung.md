---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Qualitätsmanagement]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - QS - Testen Verifikation Validierung

> [!info] Kurzdefinition
> In Software-Engineering-Referenzmodellen sind **Testen, Verifikation, Validierung** und **Qualitätssicherung** eigenständige Aufgaben. **Verifikation** prüft gegen die **Spezifikation**, **Validierung** gegen den **Einsatzzweck**. Testen ist eine Methode für beide.

## Beschreibung

Aus Folien 12–13:

Testen wird oft als **Teil der Qualitätssicherung** betrachtet. In Referenzmodellen sind diese vier jedoch **eigenständige** Aufgaben/Prozesse.

## Bestandteile / Aufbau

### Definitionen (Folie 12)

| Begriff | Definition |
|---|---|
| **Testen** | Prozess, ein Programm auszuführen, um **Fehler zu finden**. Methode der Verifikation und Validierung. |
| **Verifikation** | Bestätigung, dass die festgelegten **Anforderungen erfüllt** wurden – Prüfung **gegen die Spezifikation**. |
| **Validierung** | Bestätigung, dass die Anforderungen für einen **speziellen Gebrauch oder eine Anwendung** erfüllt wurden – Prüfung **gegen den Einsatzzweck** in einer bestimmten Umgebung. |
| **Qualitätssicherung (QS)** | Übergreifend: Sicherstellung, dass Maßnahmen umgesetzt und wirksam sind, das Produkt „gut genug" ist. |

### Warum Verifikation UND Validierung? (Folie 13)

- Wir können **nicht davon ausgehen**, dass ein Projekt **valide und vollständige Anforderungen** hat.
- Dasselbe Produkt kann **verschiedene Einsatzzwecke** und **unterschiedliche Umgebungen** haben – für das eine mehr, für das andere weniger geeignet.

## Beispiel

*Im PDF nicht durch konkretes Beispiel illustriert.*

> Standardlehrbuch-Merkhilfe: **Verifikation = „Are we building the product right?"**, **Validierung = „Are we building the right product?"**

## Abgrenzung

- **Verifikation** ist **spezifikations-orientiert** (intern, technisch).
- **Validierung** ist **zweck-orientiert** (extern, fachlich).
- **Testen** ist eine **Technik**, die für beides eingesetzt wird.
- **QS** ist die **organisatorische Klammer**.
- Verbindung zum **V-Modell** ([[ITPM - V-Modell - Vorgehensmodell]]): jedes Spezifikations-Level hat sein gegenüberliegendes Test-Level.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich Verifikation und Validierung? Wo liegt das Testen?

**Anwendungsfrage:** Sie haben ein Patientenportal entwickelt. Welche Tests gehören zur Verifikation, welche zur Validierung?

**Diskussionsfrage:** Warum reicht Verifikation alleine nicht? Welche Risiken bestehen, wenn nur gegen die Spezifikation geprüft wird?

**Mögliche Anschlussfragen:**
- Welche Verbindung zum V-Modell-Vorgehensmodell?
- Welche Stakeholder sind in Verifikation und Validierung involviert?
- Wie verhält sich die Definition of Done zur Verifikation?

## Verwandt

- [[ITPM - Qualität - Definition]]
- [[ITPM - QS - Plan]]
- [[ITPM - V-Modell - Vorgehensmodell]]
- [[ITPM - Agile - Definition of Done]]
- [[ITPM - RE - Anforderungsprüfung]]

## Quelle

- Vorlesung: [[ITPM - VL - Qualitätsmanagement]]
- Folien/Seitenangabe: 12–13
