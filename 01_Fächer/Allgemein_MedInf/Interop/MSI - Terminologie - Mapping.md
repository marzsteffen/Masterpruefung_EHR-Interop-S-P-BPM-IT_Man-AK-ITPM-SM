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

# MSI - Terminologie - Mapping

> [!info] Kurzdefinition
> Ein Begriff/Konzept aus einer Terminologie entspricht einem Begriff/Konzept einer anderen Terminologie (Cross-Mapping) oder steht in Beziehung zu einem Begriff aus derselben Terminologie. Mappings ermöglichen das Übersetzen zwischen Codesystemen.

## Beschreibung

Wörtlich aus Folie 9:

> „Mapping, Cross-Mapping: Ein Begriff/Konzept aus einer Terminologie entspricht einem Begriff/Konzept einer anderen Terminologie (Cross) oder steht in Beziehung zu einem Begriff aus derselben Terminologie."

Mapping ist die Brücke zwischen Terminologien (z. B. ICD-10 ↔ ICD-10-GM, SNOMED CT ↔ ICD-10) und innerhalb einer Terminologie (z. B. zwischen Versionen, Synonymen, Hierarchie-Pfaden).

> Hinweis Quelltreue: Die Vorlesung 02 nennt nur die Definition. Konkrete Mapping-Beispiele und Mapping-Tools werden in der Vorlesung **nicht** vertieft.

## Bestandteile / Aufbau

Zwei Mapping-Typen laut Folie 9:
- **Cross-Mapping**: zwischen verschiedenen Terminologien.
- **Mapping innerhalb einer Terminologie**: Beziehungen zwischen Konzepten derselben Terminologie.

## Beispiel

Im PDF nicht ausgeführt. Typische Mapping-Use-Cases (außerhalb der Folie): Abrechnungs-Mapping (klinischer Code → DRG/LKF-relevanter Code), internationaler Befundtransfer (SNOMED CT → ICD-10), Lab-Daten-Mapping (lokale Lab-Codes → LOINC).

## Abgrenzung

- **Mapping ≠ Terminologie-Erstellung.** Beim Mapping verändert man die beteiligten Terminologien nicht; man stellt nur Beziehungen her.
- **Mapping ≠ Postkoordination**. Postkoordination kombiniert Konzepte zur Laufzeit innerhalb einer Terminologie ([[MSI - Terminologie - Präkoordination vs Postkoordination]]).
- **Cross-Mapping ≠ 1:1-Identität.** Mappings können auch „one-to-many" oder unscharf sein – darauf weist die Folie nicht explizit hin, aber die Definition sagt nur „entspricht oder steht in Beziehung zu".

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Cross-Mapping?

**Anwendungsfrage:** Wann brauchen Sie ein Mapping zwischen Terminologien? Geben Sie zwei Beispiele aus dem österreichischen Kontext.

**Diskussionsfrage:** Welche Probleme entstehen, wenn die Mapping-Beziehung nicht 1:1 ist? Wer entscheidet bei Mehrdeutigkeit?

**Mögliche Anschlussfragen:**
- Welche Tools/Standards adressieren Mappings (z. B. SNOMED CT Map sets, FHIR ConceptMap)?
- Wie verhält sich Mapping zur Postkoordination?
- Wie geht ELGA mit Mappings um? (Die Folie nennt termgit.elga.gv.at als Anlaufstelle, ohne Mappings explizit zu zeigen.)

## Verwandt

- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]
- [[MSI - Ordnungssystem - Konzeptdomäne]]

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 9
