---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Terminologien Anwendung]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - UCUM - Definition

> [!info] Kurzdefinition
> UCUM (*Unified Code for Units of Measure*) ist ein Code-System zur Codierung von Maßeinheiten. Zweck: elektronischer Datenaustausch von physikalischen Größen mit eindeutiger Verarbeitung und Umrechnung auf SI-Basiseinheiten. Ergänzt LOINC um die Einheits-Schreibweise.

## Beschreibung

Folie 27 listet:

> „**Unified Code for Units of Measure** zur Codierung von Maßeinheiten
> – Zweck: elektronischer Datenaustausch von physikalischen Größen
> – **Eindeutige Verarbeitung und Umrechnung auf SI-Basiseinheiten möglich**
> – Ergänzt LOINC als Standard für die Identifikation von Mess- und Untersuchungsmethoden
> – Orientiert sich an ISO-Normen und SI-Einheiten
> – Formulierung von zusammengesetzten Einheiten enthalten
> – OID für UCUM: 2.16.840.1.113883.6.8.
> – Website: http://unitsofmeasure.org/ (Regenstrief inst.)
> – Verwendet von HL7, DICOM, FDA etc."

## Bestandteile / Aufbau

UCUM ist primär eine **Schreibweise**, nicht eine vollständige Liste an Einheiten (Folie 29). Die Sprache wird über vier Komponenten + eine Annotations-Form definiert (siehe [[MSI - UCUM - Aufbau]]).

| Eigenschaft | Detail |
|---|---|
| Pflege | Regenstrief Institute |
| OID | `2.16.840.1.113883.6.8` |
| Standard-Familie | HL7, DICOM, FDA |
| Bezugs-System | SI + ISO-Normen |
| Use Case | physikalische Größen elektronisch austauschen, automatisch umrechnen |

## Beispiel

Aus Folie 25 (CDA-Lab-Observation):
```
<value unit="G/L" value="26" xsi:type="PQ"/>
```
`G/L` ist die UCUM-Schreibweise für „Gramm pro Liter". Aus Folie 29:
- `mg/dL` = milligram per deciliter
- `mm[Hg]` = millimeter of mercury
- `[IU]/10*9{RBCs}` = international unit per billion red blood cells (mit Annotation `{RBCs}`)

## Abgrenzung

- **UCUM ≠ ISO-Einheits-Liste.** UCUM definiert die *Schreibweise* und *Kombinations­regeln*; konkrete Einheits-Mengen ergeben sich kompositorisch.
- **UCUM ≠ LOINC.** LOINC sagt, *was* gemessen wird; UCUM sagt, in *welcher Einheit* das Ergebnis ausgedrückt wird.
- **UCUM ≠ menschen­lesbare Einheits­schreibweise.** „mmHg" und „mm[Hg]" unterscheiden sich – UCUM verlangt die eckige Klammer.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist UCUM und welchen Zweck verfolgt es?

**Anwendungsfrage:** Welche UCUM-Schreibweise verwenden Sie für „Millimeter Quecksilbersäule"?

**Diskussionsfrage:** Warum ergänzt UCUM LOINC, statt es zu ersetzen?

**Mögliche Anschlussfragen:**
- Welche Komponenten definieren die UCUM-Sprache? → [[MSI - UCUM - Aufbau]]
- Welche OID identifiziert UCUM in CDA?
- Welche typischen UCUM-Schreibweisen kommen in einem Laborbefund vor? → [[MSI - UCUM - Beispiele]]

## Verwandt

- [[MSI - UCUM - Aufbau]]
- [[MSI - UCUM - Beispiele]]
- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - Daten - Datentypen]] (physical quantity)
- [[MSI - Identifikator - OID]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 27
