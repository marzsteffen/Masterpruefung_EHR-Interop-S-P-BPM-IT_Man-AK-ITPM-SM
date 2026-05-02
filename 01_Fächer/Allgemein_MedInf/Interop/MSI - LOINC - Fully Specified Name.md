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

# MSI - LOINC - Fully Specified Name

> [!info] Kurzdefinition
> Für jeden LOINC-Code gibt es zwei Bezeichnungs­formen: den **Fully Specified Name** (FSN) als formale Notation `Component:Property:Timing:Sample:Scale:Method` und den besser lesbaren **long common name**.

## Beschreibung

Wörtlich aus Folie 24:

> „Für jeden Loinc-Code wird ein ‚Fully Specified Name' angegeben, der alle Informationen für das Mapping enthält (‚5–6 Achsen'):
>
> Component: Property: Timing: Sample: Scale: Method
> Leukocytes:NCnc:PT:Bld:Qn
>
> Daneben gibt es einen (besser lesbaren) ‚long common name', z. B.
> Leukocytes [#/volume] in Blood"

Der FSN ist die kanonische Form, die das Mapping zu anderen Systemen erlaubt; der long common name ist für die menschliche Lesbarkeit gedacht.

## Bestandteile / Aufbau

| Form | Zweck | Beispiel |
|---|---|---|
| Fully Specified Name | Formale Notation, Mapping | `Leukocytes:NCnc:PT:Bld:Qn` |
| Long common name | Lesbarkeit | `Leukocytes [#/volume] in Blood` |

Die Folie spricht von „5–6 Achsen", weil die Method oft nicht spezifiziert wird. Die sechste Achse (Method) ist optional bzw. bleibt bei vielen Codes leer.

## Beispiel

Aus Folie 24:
- Code `26464-8`
- FSN: `Leukocytes:NCnc:PT:Bld:Qn`
- Long common name: `Leukocytes [#/volume] in Blood`

## Abgrenzung

- **FSN ≠ Display Name in CDA.** Im CDA wird der `displayName`-Attribut häufig auf einen kürzeren Begriff (z. B. „Leukozyten") gesetzt, nicht auf den FSN oder long common name.
- **FSN ≠ Code-Wert.** Der FSN ist die *Bezeichnung*, der numerische Code (`26464-8`) ist der *Identifier*.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Fully Specified Name eines LOINC-Codes?

**Anwendungsfrage:** Zerlegen Sie den FSN `Leukocytes:NCnc:PT:Bld:Qn` in seine Bestandteile.

**Diskussionsfrage:** Warum gibt es zusätzlich zum FSN den long common name?

**Mögliche Anschlussfragen:**
- Welche Rolle spielt der FSN beim Mapping zwischen Lab-Systemen?
- Wie verhält sich der FSN zur Sechs-Achsen-Struktur? → [[MSI - LOINC - Sechs-Achsen-Struktur]]
- Welche Sprache hat der long common name? Internationale Übersetzungen?

## Verwandt

- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Sechs-Achsen-Struktur]]
- [[MSI - LOINC - Verwendung in CDA]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 24
