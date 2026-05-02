---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Aufwandsschätzung - CoCoMo

> [!info] Kurzdefinition
> CoCoMo (Constructive Cost Model) ist ein algorithmisches Aufwandsschätzungsverfahren für Softwareentwicklung. Es basiert auf **Lines of Code (LOC) / KDSI** und Berechnungsfaktoren. Es besteht aus drei Phasen: Basic, Intermediate, Detailed CoCoMo.

## Beschreibung

Aus Folien 46–48:

- Algorithmisches Verfahren zur Aufwandsabschätzung in der Softwareentwicklung.
- **Voraussetzungen:**
  - Ermittlung von **LOC (Lines of Code) / KDSI (Kilo Delivered Source Instructions)**.
  - Ermittlung von Berechnungsfaktoren.

## Bestandteile / Aufbau

### Phase 1: Basic CoCoMo (Folie 47)

**Hauptformeln:**

```
Aufwand [Personenmonate] = A × Größe[KDSI]^B
Projektdauer [Monate]    = C × Aufwand^D
```

**Werte je nach Projektkomplexität:**

| Projekttyp | A | B | C | D |
|---|---|---|---|---|
| **Organic Projects** | 2,4 | 1,05 | 2,5 | 0,38 |
| **Semi-detached Projects** | 3,0 | 1,12 | 2,5 | 0,35 |
| **Embedded Projects** | 3,6 | 1,20 | 2,5 | 0,32 |

### Phase 2: Intermediate CoCoMo (Folie 48)

**Hauptformel:**

```
Aufwand [Personenmonate] = (K1 × ... × K15) × Aufwand[Basic CoCoMo]
```

- 15 **Kostentreiber** (K1 bis K15).
- Werte sind geschätzt und ohne Berücksichtigung von Phasen.

### Phase 3: Detailed CoCoMo (Folie 48)

- Wie Phase 2, nur **mit verfeinerter Aufgabenliste**.

## Beispiel

*Im PDF nicht durch konkrete Zahlenrechnung illustriert.*

## Abgrenzung

- **CoCoMo basiert auf LOC** – problematisch bei modernen Frameworks/Sprachen mit unterschiedlicher Ausdrucksstärke.
- **Function Point** ([[ITPM - Aufwandsschätzung - Function Point]]) ist **sprachunabhängig** und funktional.
- Es gibt **CoCoMo II** (1995) – im PDF nicht erwähnt; aktualisierte Modelle für moderne Entwicklungsstile.
- **Organic / Semi-detached / Embedded** entsprechen Projekt-Komplexitätsklassen, nicht zu verwechseln mit der Klassifikation aus VL 1 ([[ITPM - Projekt - Klassifikation]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Phasen hat CoCoMo, und auf welcher Größe basiert das Verfahren?

**Anwendungsfrage:** Sie haben ein Projekt mit 50 KDSI als „Semi-detached" eingestuft. Berechnen Sie nach Basic CoCoMo den Aufwand und die Dauer. *(Aufwand = 3,0 × 50^1,12 ≈ 239 PM; Dauer = 2,5 × 239^0,35 ≈ 17 Monate.)*

**Diskussionsfrage:** Welche Kritik gibt es an LOC-basierten Verfahren in modernen Projekten?

**Mögliche Anschlussfragen:**
- Was sind die 15 Kostentreiber in Intermediate CoCoMo? *(im PDF nicht aufgeführt)*
- Wie unterscheidet sich Detailed von Intermediate CoCoMo?
- Vergleich CoCoMo vs. Function Point?

## Verwandt

- [[ITPM - Aufwandsschätzung - Schätzverfahren Übersicht]]
- [[ITPM - Aufwandsschätzung - Function Point]]
- [[ITPM - Aufwandsschätzung - Analogiemethode]]
- [[ITPM - Projekt - Klassifikation]]

## Quelle

- Vorlesung: [[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]
- Folien/Seitenangabe: 46–48
