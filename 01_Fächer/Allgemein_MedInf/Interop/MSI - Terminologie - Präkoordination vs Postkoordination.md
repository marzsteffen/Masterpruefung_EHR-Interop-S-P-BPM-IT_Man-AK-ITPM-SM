---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Semantik Theorie]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologie - Präkoordination vs Postkoordination

> [!info] Kurzdefinition
> Präkoordination = ein Konzept ist direkt als einzelner Code verfügbar. Postkoordination = ein Konzept wird zur Laufzeit aus mehreren Konzepten und Beziehungen zusammen­gesetzt. Hauptanwendungsfall der Postkoordination: Codieren eines medizinischen Ausdrucks, für den (noch) keine SCTID existiert.

## Beschreibung

Folie 19 stellt das Begriffspaar gegenüber:

> „Präkoordination vs. Postkoordination"

Beispiele auf Folie 19:
- **Präkoordiniert (LOINC)**: `26464-8 LOINC (2.16.840.1.113883.6.1) Leukocytes : NCnc : Pt : Bld : Qn :` – ein vorhandener LOINC-Code für die Leukozytenzahl.
- **Mehrachsig zusammengesetzt (APPC)**: `CT Colonografie 2.0.2-3-7.4-2-3 → CT.undefiniert.virtuelle-endoskopie.colon` – siehe [[MSI - Terminologie - Mehrachsigkeit]].

Die Folie nennt drei Vor-/Nachteils-Dimensionen:
- Erstellung und Pflege von Terminologien.
- Anwendung von Terminologien (lesend und schreibend).
- Validierung.

Folie 20–21 vertiefen das an einem **SNOMED-CT-Beispiel** „Laparoskopische Notfall-Appendektomie":

**Präkoordiniert** in SNOMED CT vorhanden als Konzept `174041007 | laparoscopic emergency appendectomy |`. Definition enthält u. a. Beziehungen:
- `116680003 | is a | = 80146002 | appendectomy |`
- `260870009 | priority | = 25876001 | emergency |`
- `425391005 | using access device | = 86174004 | laparoscope |`

**Postkoordiniert** kann derselbe Sachverhalt ausgedrückt werden:
```
80146002 | appendectomy | : 260870009 | priority | = 25876001 | emergency |, 425391005 | using access device | = 86174004 | laparoscope |
```
Diese Postkoordinations-Expression hat laut Folie 21 „die gleiche Bedeutung wie" der präkoordinierte Code `174041007`.

> **Hauptanwendungsfall und Stärke der Postkoordination** (Folie 21): Möglichkeit der Codierung eines medizinischen Ausdrucks, wenn es dafür (noch) keine SCTID gibt.

## Bestandteile / Aufbau

| Modus | Wann gut? | Wann problematisch? |
|---|---|---|
| Präkoordination | Häufige Konzepte, schnelle Eingabe, einfache Validierung | Riesige Code-Listen für alle Kombinationen, wartungsintensiv |
| Postkoordination | Beliebige Konzepte ausdrückbar, ohne dass jeder einen eigenen Code braucht | Komplexere Validierung und Vergleichbarkeit, Schreib-/Lese-Komplexität, Tools nötig |

## Beispiel

Aus Folie 20–21 das SNOMED-Beispiel oben.

Aus dem klinischen Alltag (außerhalb der Folie): Wenn ein Befund „CT virtuelle Colonoskopie mit Kontrastmittel" lautet, kann in APPC zusammengesetzt werden; wenn es in SNOMED CT keinen präkoordinierten Code gibt, kann postkoordiniert werden.

## Abgrenzung

- **Postkoordination ≠ Mehrachsigkeit.** Mehrachsige Terminologien (APPC) machen *immer* eine Form von Komposition, aber jede Achse ist intern präkoordiniert.
- **Postkoordination ≠ Mapping.** Postkoordination kombiniert Konzepte innerhalb einer Terminologie; Mapping verbindet Konzepte zwischen Terminologien.
- **Postkoordination ≠ Freitext-Eingabe.** Postkoordination ist *strukturiert* und maschinell verarbeitbar – nur eben aus mehreren Codes zusammen­gesetzt.

## Prüfungsrelevanz

**Sehr hoch.** Klassisches SNOMED-Thema.

**Typische Definitionsfrage:** Was ist Präkoordination, was Postkoordination?

**Anwendungsfrage:** Schreiben Sie den postkoordinierten SNOMED-CT-Ausdruck für „Laparoskopische Notfall-Appendektomie".

**Diskussionsfrage:** Welche Stärke hat Postkoordination, und welche praktischen Probleme bringt sie mit sich? (Stärke: Ausdrücken neuer Konzepte ohne neuen Code. Problem: Vergleichbarkeit, Validierung, Tool-Anforderungen.)

**Mögliche Anschlussfragen:**
- Welche SNOMED-CT-Konzepte werden in der postkoordinierten Form aus dem Beispiel verwendet (priority, using access device)?
- Welche Cimino-Desiderata stützen Postkoordination? (Multiple Granularities, Formal Definition.)
- Wie verhält sich Postkoordination zu „Komposition zur Sprache" aus den Anforderungen ([[MSI - Terminologie - Anforderungen]])?

## Verwandt

- [[MSI - Terminologie - Mehrachsigkeit]]
- [[MSI - Terminologie - Anforderungen]]
- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Terminologie - SNOMED CT Konzepte]] (Querverweis spätere Vorlesung)
- [[MSI - Terminologie - LOINC Struktur]] (Querverweis spätere Vorlesung)

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 19, 20, 21
