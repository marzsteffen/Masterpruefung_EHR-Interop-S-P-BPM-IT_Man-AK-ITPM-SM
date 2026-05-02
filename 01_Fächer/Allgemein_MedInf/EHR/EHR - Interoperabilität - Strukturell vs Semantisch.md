---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - CCR und CCD]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Interoperabilität - Strukturell vs Semantisch

> [!info] Kurzdefinition
> Zwei zentrale Schichten der Interoperabilität: **strukturelle Interoperabilität** sorgt für gemeinsame Austauschformate (XML, JSON, HL7-Strukturen), **semantische Interoperabilität** sorgt für gemeinsame Bedeutung (Coding-Systeme wie LOINC, SNOMED CT, ICD). Semantik ist deutlich schwieriger.

## Beschreibung

Aus Folie 3:

> „Major problem however is interoperability!
> - structural: exchange formats
> - semantic: coding systems
>
> Semantic interoperability is harder than structural interoperability …
> Fortunately, the whole world is standardizing more and more to:
> - LOINC for tests
> - SNOMED-CT
> - UCUM for Units of Measure
> - ATC, ICD, …
> Except for … clinical research (CDISC, FDA, …)."

## Bestandteile / Aufbau

| Schicht | Was wird vereinheitlicht? | Beispiele |
|---|---|---|
| **Strukturell** | Format und Aufbau der Nachricht | HL7 v2 (Pipe-/Hash-Format), CDA (XML), FHIR (JSON/XML), CSV |
| **Semantisch** | Bedeutung der Daten­elemente | LOINC (Tests), SNOMED CT (klinisch), UCUM (Maßeinheiten), ATC (Wirkstoffe), ICD-10/11 (Diagnosen) |

## Beispiel

Konkretes Beispiel aus der Vorlesung:
- **Strukturell** kompatibel: Sender und Empfänger einigen sich auf CDA-XML. Die Nachricht kann technisch gelesen werden.
- **Semantisch** kompatibel: Beide Seiten nutzen dasselbe LOINC-Code für „HbA1c-Wert in mmol/mol", denselben UCUM-Code für die Einheit. Erst dann kann die Software den Wert verarbeiten.

Ohne semantische Interoperabilität bleiben die Daten **lesbar** (für Menschen), aber **nicht maschinell verarbeitbar**.

## Abgrenzung

- Diese 2-Schichten-Sicht ist eine vereinfachte Variante der drei Schichten in [[EHR - Interoperabilität - LCIM nach Tolk]] (Technical Integration / Syntax & Semantics / Process Composability).
- Strukturell heißt nicht „nur Format, ohne Inhalt" – auch eine strukturelle Spezifikation kann Pflichtfelder definieren (z. B. CCD verlangt 6 Sektionen).
- **Semantik ohne Struktur** ist nicht nutzbar, **Struktur ohne Semantik** ist halb nutzbar (Mensch-lesbar).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen struktureller und semantischer Interoperabilität?

**Anwendungsfrage:** An welcher Schicht scheitert ein typischer EHR-Datenaustausch zwischen zwei Krankenhäusern in Österreich heute?

**Diskussionsfrage:** Warum ist semantische Interoperabilität schwieriger als strukturelle? Welche organisatorischen, sprachlichen, kulturellen und finanziellen Hürden bestehen?

**Mögliche Anschlussfragen:**
- Welcher Standard kodiert was? (LOINC: Tests; SNOMED: alles klinische; ICD: Diagnosen; UCUM: Einheiten; ATC: Wirkstoffe; RxNorm: US-Medikation; PZN: AT-Medikation)
- Was ist CDISC und warum ist Clinical Research dort eine Ausnahme? (Antwort: CDISC ist ein eigenes Standard-Set für klinische Studien, FDA-getrieben)
- Wie verbinden sich Struktur und Semantik in HL7 FHIR? (Antwort: FHIR definiert Struktur via Resource-Schemas und Semantik via CodeableConcept-Bindings auf externe Terminologien)

## Verwandt

- [[EHR - Interoperabilität - LCIM nach Tolk]]
- [[EHR - Standards - Unterstützte Coding Standards]]
- [[EHR - System vs Exchange Format]]
- [[EHR - HL7 CDA - RIM-Basis]]
- [[MSI - SNOMED CT]]
- [[MSI - LOINC]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folie 3 („Electronic Health Records and Interoperability")
