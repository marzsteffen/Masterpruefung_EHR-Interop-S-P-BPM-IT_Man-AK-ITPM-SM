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

# MSI - UCUM - Beispiele

> [!info] Kurzdefinition
> Sammlung typischer UCUM-Schreibweisen aus dem klinischen Alltag mit ihrer menschen­lesbaren Bedeutung. Illustriert die Sprach-Konstruktion (Präfixe, abgeleitete Einheiten, Annotationen, kombinierte Ausdrücke).

## Beschreibung

Tabellen-Auszug aus Folie 29:

| UCUM | Bedeutung |
|---|---|
| `%` | percent |
| `%{vol}` | percent by volume |
| `10*6/uL` | million per microliter |
| `fL` | femtoliter |
| `fmol/g` | femtomole per gram |
| `g/dL` | gram per deciliter |
| `mg/dL` | milligram per deciliter |
| `mg/g{feces}` | milligram per gram of feces |
| `mm[Hg]` | millimeter of mercury |
| `U/dL` | enzyme unit per deciliter |
| `U/L` | enzyme unit per liter |
| `[IU]/10*9{RBCs}` | international unit per billion red blood cells |

Die Folie betont: „UCUM ist ein Standard für die **Schreibweise** von Einheiten, und daher keine vollständige Liste an Einheiten."

## Bestandteile / Aufbau

Die Tabelle zeigt typische Phänomene:
- **Reines Präfix-Beispiel**: `mg`, `dL` (Präfix + Basiseinheit).
- **Annotationen**: `{vol}`, `{feces}`, `{RBCs}` – Lesekontext, ändert die Einheit nicht.
- **Eckige Klammern für abgeleitete Einheiten**: `[Hg]` für Mercury, `[IU]` für International Unit.
- **Multiplikations-Notation**: `10*6` für „×10⁶".
- **Verkettung**: `[IU]/10*9{RBCs}` kombiniert abgeleitete Einheit + Multiplikator + Annotation.

## Beispiel

Direkt aus der Tabelle. In CDA (Folie 25): `<value unit="G/L" value="26"/>` – `G/L` für Gramm pro Liter.

## Abgrenzung

- **Schreib­variation**: `mmHg` (umgangs­sprachlich) vs. `mm[Hg]` (UCUM-valide). UCUM verlangt die eckige Klammer, weil sie das spezifische Mercury-Druck-System markiert.
- **Annotation vs. Einheit**: `mg/g{feces}` ist *nicht* eine andere Einheit als `mg/g`; die Annotation `{feces}` markiert nur den Kontext.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Erkennen Sie die Bedeutung folgender UCUM-Schreibweisen: `mm[Hg]`, `10*6/uL`, `[IU]/10*9{RBCs}`.

**Anwendungsfrage:** Wie schreiben Sie „Tausend pro Mikroliter" und „Mikromol pro Liter" in UCUM?

**Diskussionsfrage:** Warum sind Annotationen kein Bestandteil der Einheit, sondern nur Kontext?

**Mögliche Anschlussfragen:**
- Wann verwendet UCUM Klammern (`[]` vs. `{}` vs. `()`)?
- Welche typischen Fehler treten beim Schreiben von UCUM-Einheiten in einem Lab-System auf?
- Welche Tools validieren UCUM-Strings? (im PDF nicht behandelt)

## Verwandt

- [[MSI - UCUM - Definition]]
- [[MSI - UCUM - Aufbau]]
- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - Daten - Datentypen]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 29
