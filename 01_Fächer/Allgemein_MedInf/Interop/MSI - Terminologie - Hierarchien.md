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

# MSI - Terminologie - Hierarchien

> [!info] Kurzdefinition
> Hierarchie-Typen in Ordnungssystemen: streng monohierarchisch (Taxonomie – jedes Konzept hat genau einen Vater) vs. polyhierarchisch (mehrere Väter pro Konzept zulässig).

## Beschreibung

Folie 17 stellt die Hierarchie-Typen mit Cimino's Fig. 1 (sechs Beispielfälle) dar:

> „Streng monohierarchisch: Taxonomie oder Polyhierarchien"

**Cimino Fig. 1** – Multiple views of a polyhierarchy (laut Folientext):
- (a) Internal arrangements of nine concepts in a polyhierarchy, where E has two parents (E ist Kind von B und von C).
- (b) Hierarchy has been collapsed so that specific concepts serve as synonyms of their more general parents (E enthält G und H als Synonym; F enthält I).
- (c) Intermediate levels in the hierarchy have been hidden.
- (d) Conversion to a strict hierarchy (E erscheint zweimal, einmal pro Pfad).
- (e) Strict hierarchy with multiple contexts for term E (akzeptable Konvertierung).
- (f) Multiple contexts for E are shown, but are inconsistent (different children) – durchgekreuzt: nicht akzeptabel.

Cimino's Forderung (siehe [[MSI - Terminologie - Cimino Desiderata]]): Polyhierarchy mit formalen Beziehungen ist Pflicht für eine moderne medizinische Terminologie.

## Bestandteile / Aufbau

| Hierarchie-Typ | Definition | Beispiel |
|---|---|---|
| Monohierarchie / Taxonomie | Genau ein Vater pro Konzept | Linné's Systema Naturae |
| Polyhierarchie | Mehrere Väter pro Konzept | SNOMED CT |

Konvertierungsstrategien laut Cimino Fig. 1:
- **Akzeptabel** (Folie 17): Kollabieren in Synonyme, Verstecken von Zwischenebenen, Mehrfachauftauchen mit konsistenten Kindern.
- **Nicht akzeptabel** (durchgekreuzt): Mehrfachauftauchen mit unterschiedlichen Kindern (Inkonsistenz).

## Beispiel

Aus Folie 17: Konzept E hat zwei Eltern (B und C). In einer reinen Taxonomie müsste E doppelt gelistet werden – mit allen Pfaden in beiden Zweigen identisch (Variante e), sonst entstehen Inkonsistenzen (Variante f).

Praktisches medizinisches Beispiel (außerhalb der Folie): Eine „Pneumonie der linken Unterlappen" ist sowohl Pneumonie (Erkrankung) als auch lokalisiert im linken Unterlappen (Anatomie) – polyhierarchisch beide Eltern legitim.

## Abgrenzung

- **Hierarchie ≠ Mehrachsigkeit**: Mehrachsigkeit teilt eine Terminologie in mehrere unabhängige Achsen ([[MSI - Terminologie - Mehrachsigkeit]]); innerhalb einer Achse kann es mono- oder polyhierarchisch sein.
- **Polyhierarchie ≠ Ontologie**: Ontologie kann polyhierarchisch sein, aber Polyhierarchie reicht nicht aus, um eine Ontologie zu sein – es fehlen die formalen Beziehungstypen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was unterscheidet Monohierarchie von Polyhierarchie?

**Anwendungsfrage:** Begründen Sie an einem medizinischen Beispiel, warum Polyhierarchie nötig ist.

**Diskussionsfrage:** Welche Kompromisse muss man eingehen, wenn man eine polyhierarchische Terminologie in eine monohierarchische umwandelt? (Cimino Fig. 1 d–f: Doppelung mit Konsistenz­bedingung, sonst Inkonsistenzen.)

**Mögliche Anschlussfragen:**
- Welches Cimino-Desideratum verlangt Polyhierarchie? (Desideratum 4)
- Wie löst SNOMED CT die Polyhierarchy-Forderung technisch?
- Wie verhält sich die Hierarchie zur Komposition (Postkoordination)?

## Verwandt

- [[MSI - Ordnungssystem - Taxonomie]]
- [[MSI - Ordnungssystem - Klassifikation]]
- [[MSI - Ordnungssystem - Ontologie]]
- [[MSI - Terminologie - Mehrachsigkeit]]
- [[MSI - Terminologie - Cimino Desiderata]]

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 17 (mit Cimino Fig. 1, Quelle: Cimino 1998)
