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

# MSI - UCUM - Aufbau

> [!info] Kurzdefinition
> UCUM definiert eine Sprache aus vier Bestandteilen plus Annotationen: Präfixe (Multiplikatoren wie d, u), Basiseinheiten (m, g, s …), abgeleitete Einheiten (atomic unit symbols), Syntaxregeln zur Kombination (Multiplikation, Division, Potenzierung, Klammern), und Annotationen in geschwungenen Klammern.

## Beschreibung

Folie 28 listet die fünf Bestandteile von UCUM:

**1) Präfixe**
- Eine Liste von Zeichen, die als Symbole für Multiplikatoren verwendet werden können (z. B. `d` für Dezi-, `u` für Mikro-).

**2) Basiseinheiten**
- Eine Liste von Basisgrößen für Länge, Masse, Zeit, Temperatur, elektrische Ladung, Lichtstärke und Winkel (z. B. `m`, `g`, `s`).

**3) Abgeleitete Einheiten** (atomic unit symbols)
- Eine Liste von „atomaren Symbolen", in der weitere Einheiten aufgeführt sind, zusammen mit Umrechnungsfaktoren und Formeln für die Rückführung auf Basiseinheiten.

**4) Syntaxregeln zur Kombination der Symbole**
- Operatoren für **Multiplikation** (`.`), **Division** (`/`), **Potenzierung** (`^` bzw. Exponent in der Schreibweise) und **Gruppierungs­klammern** (`()`).

**5) Annotationen**
- Zur Interpretation, in geschwungener Klammer, z. B. `{total}`. Annotationen verändern die Einheit nicht, sondern liefern Zusatz-Kontext.

## Bestandteile / Aufbau

| Bestandteil | Zweck | Beispielsymbol |
|---|---|---|
| Präfix | Multiplikator | `d` (Dezi-), `u` (Mikro-) |
| Basiseinheit | Grundgröße | `m`, `g`, `s` |
| Abgeleitete Einheit | Atom-Symbol mit Umrechnung | – |
| Syntax | Verknüpfung | Multiplikation, Division, Potenz, Klammern |
| Annotation | Interpretations-Hinweis | `{total}`, `{feces}`, `{RBCs}` |

## Beispiel

Aus Folie 29:
- `mg/dL` – milligram per deciliter (Präfix `m` an Basiseinheit `g`, geteilt durch Präfix `d` an `L`)
- `mm[Hg]` – millimeter of mercury (Präfix `m` + `m` für Meter; `[Hg]` ist abgeleitete Einheit für Quecksilber-Druck-Skala)
- `10*6/uL` – million per microliter (Multiplikator-Schreibweise `10*6`, Präfix `u` an `L`)
- `[IU]/10*9{RBCs}` – international unit per billion red blood cells (mit Annotation `{RBCs}`)
- `mg/g{feces}` – milligram per gram of feces (mit Annotation `{feces}`)

## Abgrenzung

- **UCUM-Sprache vs. Einheits-Liste**: UCUM ist primär eine Sprache zur *Schreibweise*, keine geschlossene Liste. Beliebige zulässige Kombinationen können neue Einheits-Ausdrücke erzeugen.
- **Annotation ≠ Einheit**. `{RBCs}` verändert die Einheit `[IU]/10*9` nicht – es ist nur ein Lese-Hinweis.
- **`mmHg` vs. `mm[Hg]`**: Letzteres ist UCUM-konform; ersteres ist eine umgangs­sprachliche Schreibweise und nicht UCUM-valide.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Bestandteile definieren die UCUM-Sprache?

**Anwendungsfrage:** Schreiben Sie die folgenden Einheiten in UCUM: Millimeter Quecksilbersäule, Mikromol pro Liter, Milligramm pro Gramm Stuhl.

**Diskussionsfrage:** Warum sind Annotationen wichtig? Welches Problem lösen sie?

**Mögliche Anschlussfragen:**
- Welche Operatoren erlaubt UCUM zur Kombination?
- Was unterscheidet UCUM von einer ISO-Einheits-Liste?
- Wie sehen typische UCUM-Beispiele aus? → [[MSI - UCUM - Beispiele]]

## Verwandt

- [[MSI - UCUM - Definition]]
- [[MSI - UCUM - Beispiele]]
- [[MSI - Daten - Datentypen]] (physical quantity)
- [[MSI - LOINC - Verwendung in CDA]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 28
