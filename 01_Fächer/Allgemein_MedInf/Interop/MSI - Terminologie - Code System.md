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

# MSI - Terminologie - Code System

> [!info] Kurzdefinition
> Eine Sammlung von Konzept­identifikatoren in einer computer­verarbeitbaren Form. Eine Terminologie mit zugehörigem Regelwerk (z. B. Regeln zur Codierung von Begriffen, Benennung etc.).

## Beschreibung

Wörtlich aus Folie 10:

> „Code System: Eine Sammlung von Konzeptidentifikatoren in einer computerverarbeitbaren Form. Terminologie mit zugehörigem Regelwerk (z. B. Regeln zur Codierung von Begriffen, Benennung etc.)."

Ein Code System ist also eine Terminologie *plus* ein Regelwerk – z. B. wie Codes vergeben werden, wie Bezeichnungen heißen, wie versioniert wird.

In CDA-Beispielen (Folie 14 der Einführung, Folie 18 dieser VL) erscheint das Code System konkret als `codeSystem`-OID, etwa `2.16.840.1.113883.6.1` (LOINC) oder `1.2.40.0.34.5.38` (APPC).

## Bestandteile / Aufbau

- Konzept­identifikatoren (Codes).
- Regelwerk: Codierungs-, Benennungs-, Versionierungsregeln.
- In Austausch­standards meist via OID identifiziert.

## Beispiel

Aus der serviceEvent-Folie 18 dieser Vorlesung:
```
<code code="1.4.0.4-2-3-1"
      displayName="Röntgen.unpaariges Organ.Prozedur nicht näher bestimmt.Appendix"
      codeSystem="1.2.40.0.34.5.38"
      codeSystemName="APPC" />
```
Das Code System ist hier APPC (Austrian Procedure Coding Catalogue), identifiziert über die OID `1.2.40.0.34.5.38`.

## Abgrenzung

- **Code System vs. Terminologie**: das Code System ist eine Terminologie + Regeln.
- **Code System vs. Value Set**: ein Value Set ist eine Sicht auf 1–n Code Systems; das Code System ist die Quelle.
- **Code System vs. Klassifikation**: ein Code System kann eine Klassifikation enthalten oder darauf basieren – aber auch andere Strukturen (z. B. Ontologie wie SNOMED CT).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Code System, und wie unterscheidet es sich von einer reinen Terminologie?

**Anwendungsfrage:** Erklären Sie, welche Bedeutung die `codeSystem`-OID in einem CDA-`<code>`-Element hat.

**Diskussionsfrage:** Warum braucht es ein Regelwerk zusätzlich zu den reinen Codes?

**Mögliche Anschlussfragen:**
- Wie wird ein Code System in FHIR repräsentiert? (FHIR CodeSystem-Resource – im PDF nicht definiert.)
- Wo finde ich die OIDs österreichischer Code Systems? (termgit.elga.gv.at – Folie 27 dieser VL.)
- Welche Rolle spielt das Code System für die Versionierung?

## Verwandt

- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Referenz vs Interface Terminologie]]
- [[MSI - Identifikator - OID]] (im PDF in Vorlesung 01 nur erwähnt, nicht definiert)
- [[MSI - HL7 CDA - serviceEvent]] (Querverweis Vorlesung 04)

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 10 (Definition), 18 (Beispiel APPC in serviceEvent)
