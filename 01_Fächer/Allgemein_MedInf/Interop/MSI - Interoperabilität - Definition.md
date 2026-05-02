---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Einführung in Standards und Interoperabilität]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Interoperabilität - Definition

> [!info] Kurzdefinition
> Interoperabilität bedeutet, dass Dokumente und Nachrichten zwischen Systemen übertragen werden können, Befunde und Berichte in andere Systeme übernommen werden können und Daten aus anderen Systemen automatisch zur Verfügung stehen. „Both ends exchange, understand and act on the data received."

## Beschreibung

Die Vorlesung trennt zwei Begriffsstufen:

**Interoperabilität (allgemein)** bedeutet:
- Dokumente und Nachrichten können übertragen werden.
- Befunde und Berichte können in andere Systeme übernommen werden.
- Daten aus anderen Systemen stehen automatisch zur Verfügung.

**Semantische Interoperabilität** bedeutet darüber hinaus:
- Dieselben Daten müssen nicht mehrfach eingegeben werden.
- Daten, die schon in anderen Systemen vorliegen, müssen nicht nochmals erfasst werden.
- Daten können weiterverarbeitet werden: Warnungen, Erinnerungen, Zusammenfassungen, Berechnungen, Verläufe, Statistiken etc.

Der zentrale Anspruch lautet (Zitat in Folie 4 / 5): „Both ends exchange, understand and act on the data received." – nicht nur Übertragen, sondern Verstehen und Handeln.

## Bestandteile / Aufbau

Die Vorlesung positioniert Interoperabilität als geschichtetes Konstrukt – siehe [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]. Reine Übertragung (technisch) ist Voraussetzung, aber nicht hinreichend. Ohne semantische Schicht bleiben Daten zwar lesbar, aber nicht maschinell weiterverarbeitbar.

## Beispiel

Aus Folie 14 (CDA-Snippet zum Puls):
```
<code code="8867-4" displayName="Heart Beat" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC">
<value xsi:type="PQ" value="59" unit="/min"/>
```
Erst durch Code (LOINC) plus typisierten Wert (physical quantity „59 /min") wird der Pulswert maschinell vergleichbar – das ist semantische Interoperabilität in einem CDA-Dokument.

## Abgrenzung

- **Interoperabilität ≠ semantische Interoperabilität.** Ein PDF lässt sich übertragen, aber sein Inhalt ist nicht strukturiert weiterverarbeitbar (Folie 25, „PDF-Müllhalde"-Zitat ÖÄK).
- **Interoperabilität ≠ Datenaustausch.** Datenaustausch ist die Tätigkeit, Interoperabilität die Eigenschaft der beteiligten Systeme.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen Interoperabilität und semantischer Interoperabilität?

**Anwendungsfrage:** Sie tauschen ein PDF mit einem Befund aus – ist das Interoperabilität? Ist es semantische Interoperabilität? Begründen Sie.

**Diskussionsfrage:** Warum reicht reine Übertragung nicht aus? Welche Auswertungen werden erst durch semantische Interoperabilität möglich?

**Mögliche Anschlussfragen:**
- Welche drei Ebenen der Interoperabilität gibt es?
- Welcher Standard adressiert welche Ebene?
- Was bedeutet „understand and act on the data received" konkret?

## Verwandt

- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Standards - Definition]]
- [[MSI - Daten - Strukturiert vs Unstrukturiert]]

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 4, 14
