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

# MSI - Begriff - Konzept Bezeichnung Code

> [!info] Kurzdefinition
> Grundbegriffsmodell der Vorlesung: Ein **Objekt** der Welt wird durch ein **Konzept/Begriff** gedanklich zusammengefasst, sprachlich durch eine **Bezeichnung/Terminus** repräsentiert, technisch durch einen **Code** identifiziert. Konzepte haben **Attribute** mit **Ausprägungen** und **Beziehungen** zu anderen Konzepten.

## Beschreibung

Folie 6 definiert die Begriffsfamilie:

- **Objekt, Gegenstand**: Ausschnitt der realen (oder vorstellbaren) Welt. Beispiel der Folie: eine Aspirin-Packung.
- **Begriff, Konzept**: gedankliche Zusammenfassung von Objekten. Wörtlich: „ein Konzept ist der Bedeutungsinhalt einer Idee. Es bezeichnet eine semantische Einheit, die grundsätzlich geistig repräsentiert oder ‚begriffen' wird. Die sprachliche Repräsentation eines Konzeptes oder Begriffes ist die Bezeichnung. Je nach Kontext oder Autor wird ein Konzept auch Begriff, Klasse, Objekt, Entität, Element, Idee etc. genannt."
- **Bezeichnung, Benennung, Terminus**: Wort mit festgelegter Bedeutung innerhalb einer Fachsprache oder eines Fachgebietes. Beispiel: „Aspirin C" (oder „ASPIRIN C BRTBL"). Ausprägungen: „display term", „preferred term", „short name", „long common name".
- **Eigenschaften, Attribute, Merkmal**: z. B. Wirkstoff.
- **Code, Identifier**: z. B. `0004386` (PZN – Pharmazentralnummer).
- **Ausprägung**: etwa die eines Attributs.
- **Beziehungen** zwischen Begriffen/Konzepten.

## Bestandteile / Aufbau

| Element | Bedeutung | Beispiel laut Folie |
|---|---|---|
| Objekt | Welt-Ausschnitt | Aspirin-Packung |
| Konzept/Begriff | Geistige Zusammenfassung | „Aspirin" als Idee |
| Bezeichnung/Terminus | Sprachliche Form | „Aspirin C", „ASPIRIN C BRTBL" |
| Attribut/Merkmal | Eigenschaft | Wirkstoff |
| Code/Identifier | Maschineller Identifikator | `0004386` (PZN) |
| Ausprägung | Wert eines Attributs | – |
| Beziehung | Verbindung zwischen Konzepten | – |

## Beispiel

Aus Folie 6: PZN `0004386` ist der Code; „Aspirin C" ist die Bezeichnung; das zugrundeliegende Konzept ist die Idee „Aspirin C als Medikament"; das Objekt ist die konkrete Schachtel im Regal.

## Abgrenzung

- **Konzept ≠ Bezeichnung.** Mehrere Bezeichnungen (Synonyme) können auf dasselbe Konzept zeigen.
- **Code ≠ Konzept.** Ein Code ist nur der maschinen­lesbare Identifikator des Konzepts; er sollte nach Cimino keinen Bedeutungsanteil tragen → [[MSI - Terminologie - Cimino Desiderata]] (Non-semantic Concept Identifiers).
- **Bezeichnung ≠ Begriff.** „display term" und „preferred term" sind verschiedene Bezeichnungen desselben Konzepts.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Trennen Sie Objekt, Konzept, Bezeichnung und Code.

**Anwendungsfrage:** Identifizieren Sie für ein Medikament konkret: Welches ist das Objekt, welches das Konzept, welche die Bezeichnung, welcher der Code?

**Diskussionsfrage:** Warum lohnt sich diese strikte Trennung in einer Terminologie? Was geht schief, wenn man Bezeichnung und Konzept verwechselt?

**Mögliche Anschlussfragen:**
- Wie verhalten sich „preferred term" und „display term" zueinander?
- Welche Rolle hat die PZN in einem österreichischen Kontext?
- Wie modelliert SNOMED CT diese Trennung (Concept-ID, FSN, Synonym)?

## Verwandt

- [[MSI - Begriff - Synonyme Homonyme Eponyme]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Ordnungssystem - Ontologie]] (Beziehungen formalisiert)

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 6
