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

# MSI - Terminologie - Mehrachsigkeit

> [!info] Kurzdefinition
> Mehrachsige Terminologie = Terminologie mit zwei oder mehr voneinander unabhängigen Teilklassifikationen (Achsen). Ein Code in einer mehrachsigen Terminologie setzt sich aus mehreren Teilcodes zusammen, je einer pro Achse.

## Beschreibung

Folie 18 zeigt Mehrachsigkeit am Beispiel **APPC (Austrian Procedure Coding Catalogue)**:

> „Zwei oder mehr voneinander unabhängige Teilklassifikationen"

Die Folie zeigt vier APPC-Achsen-Tabellen:
- **Modalität** (z. B. 0 unbestimmt, 1 Röntgen, 2 CT, 3 MRT, 4 US, 5 NUK, 6 PET, 7 Endoskopie, 8 Mikroskopische Untersuchung, …).
- **Lateralität** (0 unbestimmt, 1 rechts, 2 links, 3 beidseits, 4 unpaariges Organ, 5 atypische Situation – Transplantat etc.).
- **Prozeduren** (umfangreich, eigene Hierarchie: Tomographie 0-1, Dual-energy X-ray absorptiometry 0-2, Enteroklysma 1-1, …).
- **Anatomie** (Maßnahme ohne regionale Zuordnung 0, Ganzkörper 0-1, Körperstamm 0-2, Schädel 1, Hirn 1-1, …).

**Beispiel CT Colonografie**: APPC-Code `2.0.2-3-7.4-2-3` – der zusammen­gesetzte Code besteht aus:
- `2` = CT (Modalität)
- `0` = undefiniert (Lateralität)
- `2-3-7` = virtuelle Endoskopie (Prozedur)
- `4-2-3` = Colon (Anatomie)

→ Klartext: „CT.undefiniert.virtuelle-endoskopie.colon".

Die Folie zeigt zusätzlich ein CDA-`<code>`-Element mit `codeSystem="1.2.40.0.34.5.38"` und `codeSystemName="APPC"` und einem zusammengesetzten Code.

## Bestandteile / Aufbau

- Mehrere unabhängige Achsen.
- Pro Achse eine eigene Klassifikation (oft mit eigener Hierarchie).
- Codeerstellung durch Kombination eines Wertes pro Achse.

| Achse (APPC) | Beispiel-Wert |
|---|---|
| Modalität | 2 (CT) |
| Lateralität | 0 (undefiniert) |
| Prozedur | 2-3-7 (virtuelle Endoskopie) |
| Anatomie | 4-2-3 (Colon) |

## Beispiel

APPC-Code `2.0.2-3-7.4-2-3` für „CT-Colonografie", siehe oben.

## Abgrenzung

- **Mehrachsig ≠ polyhierarchisch.** Polyhierarchie betrifft mehrere Eltern pro Konzept innerhalb einer Achse; Mehrachsigkeit teilt die Terminologie in unabhängige Achsen.
- **Mehrachsig ≠ präkoordiniert vs. postkoordiniert.** Mehrachsige Terminologien sind oft präkoordiniert pro Achse, aber zwischen den Achsen postkoordiniert.
- **Mehrachsiger Code ≠ non-semantic identifier.** APPC-Codes tragen Bedeutung durch ihre Achsen-Struktur – das verstößt gegen Cimino's Desideratum 11 (Non-semantic Concept Identifiers).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine mehrachsige Terminologie? Geben Sie ein Beispiel.

**Anwendungsfrage:** Erklären Sie den APPC-Code `2.0.2-3-7.4-2-3` Stelle für Stelle.

**Diskussionsfrage:** Welche Vor- und Nachteile hat ein mehrachsiger semantischer Code im Vergleich zu einem opaken Identifier?

**Mögliche Anschlussfragen:**
- Welche Cimino-Desiderata werden durch Mehrachsigkeit (APPC) verletzt? (Non-semantic Concept Identifiers, evtl. Concept Permanence bei Achsen-Erweiterung.)
- Welche anderen Beispiele für mehrachsige Klassifikationen kennen Sie? (TNM hat T/N/M/Stage als Achsen; ICD-O kombiniert Topographie und Morphologie – letzteres im PDF nicht erwähnt.)
- Wie verhält sich die Mehrachsigkeit zur Postkoordination in SNOMED?

## Verwandt

- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]
- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Terminologie - APPC]] (Querverweis spätere Vorlesung – noch nicht definiert)

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 18
