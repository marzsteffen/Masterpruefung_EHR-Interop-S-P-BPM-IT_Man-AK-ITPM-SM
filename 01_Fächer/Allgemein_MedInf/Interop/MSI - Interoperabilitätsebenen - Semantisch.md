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

# MSI - Interoperabilitätsebenen - Semantisch

> [!info] Kurzdefinition
> Semantische Interoperabilität erlaubt beiden Seiten, die Bedeutung der ausgetauschten Information zu verstehen – über kulturelle und sprachliche Grenzen hinweg. Daten werden nicht nur übertragen, sondern in ihrer Bedeutung erhalten und maschinell weiterverarbeitbar.

## Beschreibung

Wörtlich aus Folie 5:
> „Semantic Interoperability allows both sides to understand the meaning of the information exchanged across cultural and linguistic barriers."

Auf Folie 14 wird semantische Interoperabilität als Eigenschaft strukturierter Daten konkretisiert:
- Strukturierte Daten besitzen eine **einheitliche Datenstruktur** und **Datentypen**.
- Die **Bedeutung** der Information ist beschrieben durch ein **kontrolliertes Vokabular** = „Codesystem".
- Strukturierte Daten sind Informationen, die von Computersystemen **eindeutig und unter Bewahrung der Bedeutung** weiterverarbeitet werden können.
- Werden diese Daten zwischen Systemen ausgetauscht: interoperable Daten. Bleibt dabei die ursprüngliche Bedeutung erhalten: semantische Interoperabilität.

## Bestandteile / Aufbau

Auf Folie 5 der semantischen Schicht zugeordnet:
- Standards and profiles
- Clinical procedures
- Terminologies
- Medical guidelines

Auf Folie 23 listet die Vorlesung als notwendige Voraussetzungen für semantische Interoperabilität:
- **Inhalt & Syntax**: Standards (HL7 V2.x, HL7 CDA, FHIR u. a.); Einigung auf Struktur und Inhalt → Implementierungsleitfäden, Profile.
- **Semantik**: gemeinsames Informationsmodell (HL7 RIM); Terminologien (Code-Systeme, Value Sets, Klassifikationen, Ontologien) → LOINC, ICD-10, SNOMED CT, APPC; eindeutige Identifikation von Objekten → OID, MPI, eHVD.

In der Benson/Grieve-Sicht (Folie 6) entspricht diese Ebene dem **Data layer**: „exchange meaning from A to B", Identifiers and Codes, SNOMED CT.

## Beispiel

Vital-Sign-Eintrag in CDA (Folie 14):
```
<code code="8867-4" displayName="Heart Beat" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC">
<value xsi:type="PQ" value="59" unit="/min"/>
```
Dieser Schnipsel kombiniert Datentyp (PQ = physical quantity), Wert mit Einheit und LOINC-Code. So bleibt die Bedeutung über Systeme hinweg erhalten.

## Abgrenzung

- Semantische Interoperabilität ≠ technische Interoperabilität: ein PDF ist technisch übertragbar, aber maschinell nicht in seiner Bedeutung erfassbar.
- Semantische Interoperabilität ≠ strukturierte Daten allein: Struktur ohne kontrolliertes Vokabular reicht nicht (Folie 14: „Bedeutung beschrieben durch kontrolliertes Vokabular").

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet semantische Interoperabilität, und welche Voraussetzungen hat sie?

**Anwendungsfrage:** Was unterscheidet einen semantisch interoperablen Pulswert von einem Freitext-Pulswert? (Datentyp + Code + Einheit vs. nur Zeichenkette.)

**Diskussionsfrage:** Welche Hürden machen semantische Interoperabilität in der Praxis schwer? (siehe [[MSI - Interoperabilität - Herausforderungen]])

**Mögliche Anschlussfragen:**
- Welche Komponenten sind laut Vorlesung notwendig (Inhalt+Syntax, Semantik, organisatorisch)?
- Wo passt SNOMED CT, wo LOINC, wo ICD-10 hinein?
- Was ist HL7 RIM und welche Rolle spielt es? (in dieser Vorlesung nur erwähnt, nicht definiert)

## Verwandt

- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilität - Voraussetzungen]]
- [[MSI - Daten - Strukturiert vs Unstrukturiert]]
- [[MSI - Daten - Datentypen]]
- [[MSI - Terminologie - SNOMED CT Konzepte]]
- [[MSI - Terminologie - LOINC Struktur]]
- [[MSI - Terminologie - HL7 RIM]] (im PDF nur erwähnt, nicht definiert)

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 4, 5, 14, 23
