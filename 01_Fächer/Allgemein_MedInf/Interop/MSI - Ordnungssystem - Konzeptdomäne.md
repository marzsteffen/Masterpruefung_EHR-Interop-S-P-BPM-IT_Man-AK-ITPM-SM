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

# MSI - Ordnungssystem - Konzeptdomäne

> [!info] Kurzdefinition
> Eine Konzeptdomäne (engl. *Concept Domain*) ist eine bestimmte Kategorie von ähnlichen Konzepten. In unterschiedlichen Bereichen können unterschiedliche Terminologien für dieselbe Konzeptdomäne verwendet werden.

## Beschreibung

Wörtlich aus Folie 7:

> „Konzeptdomäne (engl. *Concept Domain*): eine bestimmte Kategorie von ähnlichen Konzepten. In unterschiedlichen Bereichen können unterschiedliche Terminologien für dieselbe Konzeptdomäne verwendet werden. Beispiel: Die Konzeptdomäne ‚Diagnosen' kann verschiedenste Terminologien für Diagnosen enthalten: ICD9, ICD10, ICD10-GM…"

Das ist eine wichtige Trennung: Die *Konzeptdomäne* ist die Aufgabe (Diagnosen codieren), die *Terminologie* ist die konkrete Lösung dafür (ICD-10 oder ICD-10-GM oder SNOMED CT-Subset).

## Bestandteile / Aufbau

- Konzeptdomäne als abstrakte Kategorie.
- Eine oder mehrere Terminologien pro Konzeptdomäne.

## Beispiel

Aus Folie 7: Konzeptdomäne „Diagnosen" → ICD-9, ICD-10, ICD-10-GM, …

Weitere typische Konzeptdomänen (in der Vorlesung impliziert): Laborbefunde (LOINC, hauseigene Codes), Anatomie/Prozeduren (APPC, OPS), Wirkstoffe (ATC), Pflegediagnosen (NANDA-I, POP, ICNP).

## Abgrenzung

- **Konzeptdomäne ≠ Terminologie.** Die Domäne nennt das Was, die Terminologie das Wie.
- **Konzeptdomäne ≠ Value Set.** Ein Value Set ist eine versionierte Sicht auf Codes – es kann eine Konzeptdomäne füllen, ist aber nicht dasselbe.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Konzeptdomäne, und wie verhält sie sich zu einer Terminologie?

**Anwendungsfrage:** Nennen Sie drei Konzeptdomänen im klinischen Alltag und je zwei mögliche Terminologien.

**Diskussionsfrage:** Warum ist es sinnvoll, mehrere Terminologien für dieselbe Konzeptdomäne zuzulassen, statt einer zu standardisieren?

**Mögliche Anschlussfragen:**
- Welche Konzeptdomäne wird durch SNOMED CT abgedeckt? (Antwort: viele – „cross-cutting".)
- Wie wird die Wahl der richtigen Terminologie für eine Konzeptdomäne in einem Implementierungs-Projekt getroffen?
- Wie wird in FHIR die Konzeptdomäne über Bindings ausgedrückt? → [[MSI - HL7 FHIR - Resource]] (im Paper noch nicht definiert)

## Verwandt

- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Ordnungssystem - Klassifikation]]

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 7
