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

# ITPM - Aufwandsschätzung - Function Point

> [!info] Kurzdefinition
> Die Function-Point-Methode ist ein algorithmisches Schätzverfahren für Software-Projekte. Sie ermittelt Funktionen, bewertet deren Komplexität und Qualität und summiert sie zu Function Points, die per Tabellen in Aufwand übersetzt werden.

## Beschreibung

Aus Folie 45:

- Berechnung von Function Points durch **Ermittlung von Funktionen**, **Bewertung der Komplexität und Qualität** der Funktionen.
- **Anwendbar für Software-Projekte.**

## Bestandteile / Aufbau

### Fünf Hauptfunktionsgruppen (Folie 45)

- **Externe Inputs**
- **Externe Outputs**
- **Interne Dateien**
- **Externe Abfragen**
- **Externe Schnittstellen**

### Drei Komplexitätsgruppen (Folie 45)

- **Niedrig**
- **Mittel**
- **Hoch**

### Berechnungsweg (Folie 45)

```
Funktionen ermitteln → in Hauptfunktionsgruppen einordnen →
Komplexität bewerten → Function Points (per Tabelle) →
Aufwand (per Tabelle)
```

- Zuordnung der Hauptfunktionsgruppen und deren Quantität zu **Function Points** durch **Tabellen**.
- Zuordnung der Function Points zu **Aufwand** durch **Tabelle**.

## Beispiel

*Im PDF nicht durch konkretes Berechnungsbeispiel illustriert.* Konkrete Tabellenwerte sind im PDF nicht enthalten.

## Abgrenzung

- **Function Point** ist **funktionalitätsbasiert** und unabhängig von der Implementierungssprache (im Gegensatz zu CoCoMo, das LOC verwendet).
- **CoCoMo** (siehe [[ITPM - Aufwandsschätzung - CoCoMo]]) basiert auf **Lines of Code**.
- **IFPUG** (International Function Point Users Group) ist die Standardisierungsorganisation – im PDF nicht namentlich erwähnt.
- Es gibt Varianten (Mark II, COSMIC) – im PDF nicht erwähnt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche fünf Hauptfunktionsgruppen kennt die Function-Point-Methode?

**Anwendungsfrage:** Sie sollen ein Patientenportal mit Function Points schätzen – welche Schritte gehen Sie durch?

**Diskussionsfrage:** Welcher Vorteil der FP-Methode gegenüber CoCoMo? Welcher Nachteil?

**Mögliche Anschlussfragen:**
- Welche drei Komplexitätsgruppen?
- Wo bekommt man die Tabellen her?
- Wie verhält sich FP zu Story Points?

## Verwandt

- [[ITPM - Aufwandsschätzung - Schätzverfahren Übersicht]]
- [[ITPM - Aufwandsschätzung - CoCoMo]]
- [[ITPM - Aufwandsschätzung - Analogiemethode]]
- [[ITPM - Agile - Story Points]]

## Quelle

- Vorlesung: [[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]
- Folien/Seitenangabe: 45
