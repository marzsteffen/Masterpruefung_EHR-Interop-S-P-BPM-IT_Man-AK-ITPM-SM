---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - Paper - Cimino Desiderata]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologie - Multiple Consistent Views

> [!info] Kurzdefinition
> Cimino-Desideratum 2.9: Wenn ein Vokabular mehreren Funktionen mit unterschiedlichen Granularitäten und Hierarchien dient, müssen anwendungs­spezifische Sichten möglich sein – aber sie müssen *konsistent* sein, d. h. derselbe Term darf in einer Sicht nicht widersprüchlich erscheinen.

## Beschreibung

Wörtlich aus dem Cimino-Paper, Sektion 2.9 *Multiple Consistent Views*:

> „If a vocabulary is intended to serve multiple functions, each requiring a different level of granularity, there will be a need for providing multiple views of the vocabulary, suitable for different purposes. For example, if an application restricts coding of patient diagnoses to coarse-grained concepts (such as ‚Diabetes Mellitus'), the more fine-grained concepts (such as ‚Insulin-Dependent Type II Diabetes Mellitus') could be collapsed into the coarse concept and appear in this view as synonyms (see Figs. 1a and 1b). Alternatively, an application may wish to hide some intermediate classes in a hierarchy if they are deemed irrelevant (see Fig. 1c). Similarly, although the vocabulary may support multiple hierarchies, a particular application may wish to limit the user to a single, strict hierarchy (see Fig. 1d).
>
> We must be careful to confine the ability to provide multiple consistent views, such that inconsistent views do not result. For example, if we create a view in which concepts with multiple parents appear in several places in a single hierarchy, care must be taken that each concept has an identical appearance within the view (see Figs. 1e and 1f)."

Cimino's Fig. 1 (auf Folie 17 der LV) zeigt sechs Varianten:
- (a) polyhierarchische Anordnung mit zwei Eltern für E.
- (b) Kollabieren spezifischer Konzepte als Synonyme allgemeinerer Eltern.
- (c) Verstecken von Zwischenebenen.
- (d) Konversion in strikte Hierarchie (E erscheint einmal mit gewähltem Vater).
- (e) Strikte Hierarchie mit mehrfacher Erscheinung von E – konsistente Kinder (akzeptabel).
- (f) Mehrfache Erscheinung von E mit *unterschiedlichen* Kindern – inkonsistent, **nicht akzeptabel**.

## Bestandteile / Aufbau

Drei legitime View-Strategien (a/b → c → d) plus zwei Konsistenzfälle (e konsistent, f inkonsistent):

| Strategie | Wann sinnvoll? |
|---|---|
| Kollabieren auf gröbere Konzepte | Anwendung erlaubt nur grobe Codierung |
| Zwischenebenen verstecken | Anwendung braucht Zwischenebenen nicht |
| In strikte Hierarchie konvertieren | Anwendung kann nur Monohierarchie verarbeiten |
| Mehrfaches Auftauchen mit konsistenten Kindern | Anwendung braucht single-tree-Sicht über polyhierarchische Quelle |

Die zentrale Anforderung ist **Konsistenz**: Egal welche Sicht erzeugt wird, derselbe Term muss in der Sicht überall identische Subtermini haben.

## Beispiel

Cimino's Beispiel: Ein Diabetes-View, der auf grobgranulare Diagnosen beschränkt ist, kollabiert „Insulin-Dependent Type II Diabetes Mellitus" als Synonym auf „Diabetes Mellitus". Eine andere Anwendung benötigt die Feingranularität – beide Sichten müssen konsistent sein.

Praktisch im DACH-Raum: ELGA-Befund mit ICD-10-Sicht (grobgranular für Statistik) vs. SNOMED-CT-Sicht (feingranular für klinische Auswertung) auf demselben Konzept.

## Abgrenzung

- **Multiple Consistent Views ≠ Polyhierarchy.** Polyhierarchy ist eine Eigenschaft des Vokabulars; Multiple Consistent Views sind anwendungs­spezifische Sichten auf das Vokabular.
- **Multiple Consistent Views ≠ Mapping.** Mapping verbindet Konzepte zwischen Vokabularen; Views sind innerhalb eines Vokabulars.
- **Multiple Consistent Views ≠ Multiple Granularities.** Multiple Granularities ist die Anforderung, dass das Vokabular unterschiedlich grob/fein arbeiten kann; Multiple Consistent Views regelt die *Sicht* auf eine gewählte Granularität.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was meint Cimino mit „Multiple Consistent Views"? Wodurch unterscheidet sich das von Polyhierarchy?

**Anwendungsfrage:** Geben Sie ein Beispiel, in dem zwei verschiedene Anwendungen unterschiedliche Sichten auf dieselbe SNOMED-CT-Subhierarchie brauchen.

**Diskussionsfrage:** Wie verhindert man inkonsistente Sichten technisch?

**Mögliche Anschlussfragen:**
- Welche der sechs Cimino-Fig. 1 Varianten ist nicht akzeptabel und warum?
- Wie verhält sich Multiple Consistent Views zu FHIR ValueSet-Composition?
- Welche Trade-offs entstehen, wenn man eine polyhierarchische Quelle in eine strikte Hierarchie kollabiert?

## Verwandt

- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Mapping]]

## Quelle

- Vorlesung: [[MSI - Paper - Cimino Desiderata]]
- Folien/Seitenangabe: Sektion 2.9 (Seite 7 des PDFs) + Fig. 1 (Seite 16)
