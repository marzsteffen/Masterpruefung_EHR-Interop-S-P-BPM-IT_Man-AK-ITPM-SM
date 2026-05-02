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

# MSI - Terminologie - Referenz vs Interface Terminologie

> [!info] Kurzdefinition
> Begriffspaar laut Folie 10: „Referenz"-Terminologie als zugrundeliegende, strukturell vollständige Wissens­basis vs. „Interface"-Terminologie als oberflächliche, anwender­freundliche Sicht. Im Vorlesungs-PDF nur als Stichwort genannt, nicht weiter definiert.

## Beschreibung

Folie 10 listet als drittes Stichwort:

> „‚Referenz'- bzw. ‚Interface'-Terminologie"

Eine Definition wird im PDF nicht ausgeschrieben. Nach gängiger Lehrmeinung (außerhalb des PDFs):

> **Ergänzung außerhalb der Vorlesung** – Standardlehrmeinung (z. B. Benson/Grieve, *Principles of Health Interoperability*; HL7-Glossar):
> - **Referenz-Terminologie**: vollständige, formal modellierte Konzept­sammlung mit Beziehungen, geeignet für Reasoning und systemübergreifende Speicherung. Beispiel: SNOMED CT.
> - **Interface-Terminologie**: anwender­seitige, kontext­bezogene Auswahl/Anzeige­terminologie, die auf eine Referenz­terminologie *gemappt* ist. Beispiel: lokale Befund-Picklisten.

Diese Ergänzung ist **außerhalb des PDFs** und sollte beim Lernen entsprechend gekennzeichnet bleiben.

## Bestandteile / Aufbau

Aus dem PDF lediglich die zwei Begriffe als Paar. Vollständige Auseinandersetzung folgt vermutlich in der Vorlesung 03 „Terminologien Anwendung" oder im Block FHIR + Terminologieserver.

## Beispiel

Im PDF nicht ausgeführt.

## Abgrenzung

- **Referenz vs. Interface**: Referenz = stabile semantische Basis; Interface = anwendergerechte Sicht.
- **Interface-Terminologie ≠ Value Set**: ein Value Set ist eine codeseitige Auswahl, eine Interface-Terminologie ist anzeige­seitig (Begriffe, Picklisten, Sprachvarianten).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Aufgabe hat eine Referenz-Terminologie, welche eine Interface-Terminologie?

**Anwendungsfrage:** Geben Sie ein Beispielpaar (Interface lokal → Referenz international).

**Diskussionsfrage:** Welcher Aufwand entsteht, wenn man Interface-Terminologien gegen eine Referenz-Terminologie pflegt? Wer trägt ihn?

**Mögliche Anschlussfragen:**
- Wie passen Mappings zwischen den beiden? → [[MSI - Terminologie - Mapping]]
- Was ist die Rolle eines Terminologie­servers in dieser Architektur?
- Wo passt das in FHIR (Bindings)? (im PDF nicht behandelt)

## Verwandt

- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Mapping]]
- [[MSI - Terminologie - SNOMED CT Konzepte]] (Querverweis spätere Vorlesung)

## Ergänzung außerhalb der Vorlesung

Die ausgeschriebene Definition stammt nicht aus dem Vorlesungs-PDF, sondern aus Benson/Grieve und gängiger Medizininformatik-Literatur. Vor der Prüfung sollte die exakte Definition aus der Vorlesung 03 oder dem FHIR-Block ergänzt werden, falls dort ausgeführt.

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 10 (nur als Stichwort)
