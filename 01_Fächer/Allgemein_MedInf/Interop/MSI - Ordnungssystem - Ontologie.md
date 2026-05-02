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

# MSI - Ordnungssystem - Ontologie

> [!info] Kurzdefinition
> Formale Repräsentation von Wissen – Konzepte mit ihren Beziehungen untereinander. Höchste Stufe der semantischen Treppe.

## Beschreibung

Wörtlich aus Folie 7:

> „Ontologie: Formale Repräsentation von Wissen – Konzepte mit ihren Beziehungen untereinander."

Auf Folie 8 (semantische Treppe) ist die Ontologie die oberste Stufe – „nach oben wird der Grad der inneren Strukturierung und Vernetzung immer höher."

In Cimino's Desiderata (Folie 14) verlangt das fünfte Desideratum „Formal Definition" ein logisch konsistentes, formales System mit Beziehungen wie „is-a", „part-of" (Vererbung von Klassenattributen), „caused-by", „treated-with" – das ist die Ontologie-Charakteristik.

## Bestandteile / Aufbau

- Konzepte als Knoten.
- Beziehungen als typisierte Kanten:
  - „is-a" – Subklassen-Beziehung
  - „part-of" – Teil-Ganzes-Beziehung
  - „caused-by" – Ursache
  - „treated-with" – Therapie
- Logisch konsistentes, formales System.

## Beispiel

Aus Folie 22 (Cimino Fig. 2): „Joint Swelling" ist mit „is-a"-Beziehungen zu „Swelling", „Pathologic Function", „Finding" verbunden, mit „site-of"-Beziehung zu „Joint", „has-abnormality" zu „Right Knee" usw. Das gesamte Vokabular kombiniert Definitional Knowledge (wie Konzepte sich definieren), Assertional Knowledge (wie Konzepte sich kombinieren) und Contextual Knowledge (wie Konzepte verwendet werden).

SNOMED CT ist ein praktisches Beispiel für eine Ontologie (Folie 20–21 zeigt formale Beziehungen wie `116680003|is a|`, `260870009|priority|`, `425391005|using access device|`).

## Abgrenzung

- **Ontologie vs. Thesaurus**: Thesaurus hat Synonyme und Hinweise; Ontologie hat formal definierte logische Beziehungen.
- **Ontologie vs. Klassifikation**: Klassifikation ist hierarchisch; Ontologie kann polyhierarchisch und mit beliebigen Beziehungen sein.
- **Ontologie ≠ Datenbank-Schema**: ein Schema definiert Speicherform, eine Ontologie definiert Bedeutung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was zeichnet eine Ontologie gegenüber Klassifikation und Thesaurus aus?

**Anwendungsfrage:** Welche Beziehungs-Typen verlangt Cimino's „Formal Definition"-Desideratum?

**Diskussionsfrage:** Ist SNOMED CT eine Ontologie? Argumentieren Sie mit den Beziehungen aus Folie 20–21.

**Mögliche Anschlussfragen:**
- Was bedeutet „Vererbung von Klassenattributen" über is-a-Beziehungen?
- Welche Reasoning-Möglichkeiten erlaubt eine Ontologie? (z. B. Subsumption-Check)
- Wie verhält sich eine Ontologie zur Polyhierarchy-Forderung Cimino's? → [[MSI - Terminologie - Hierarchien]]

## Verwandt

- [[MSI - Ordnungssystem - Thesaurus]]
- [[MSI - Ordnungssystem - Semantische Treppe]]
- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - SNOMED CT Konzepte]] (Querverweis spätere Vorlesung)

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 7, 8, 14, 22
