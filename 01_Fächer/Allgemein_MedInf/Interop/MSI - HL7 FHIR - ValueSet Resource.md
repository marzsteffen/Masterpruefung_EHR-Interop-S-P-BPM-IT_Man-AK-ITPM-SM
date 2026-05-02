---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR und Terminologieserver]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - ValueSet Resource

> [!info] Kurzdefinition
> Eine FHIR-Resource für **Auswahlen von Codes aus Codesystemen** für einen bestimmten Kontext. Drei Hauptteile: **Metadata** (Name, Publisher, Version …), **Content Logical Definition (compose)** mit Ein-/Ausschluss­regeln, und **Expansion** als zur Laufzeit erzeugte Liste der Konzepte. Definitionen können intensional (über Filter) oder extensional (Aufzählung) sein.

## Beschreibung

Folien 40+41 fassen zusammen:

> „Value Sets enthalten Codes aus Codesystemen, die für einen bestimmten Kontext relevant/zulässig sind
> können intensional und extensional definiert werden
> können eine ‚Composition' (Ein-/Ausschluss-Regeln) und eine ‚Expansion' (Liste von Codes) haben
> können Codes aus verschiedenen Codesystemen enthalten
> können ein Codesystem vollständig enthalten
>
> Konzept = Referenz auf ein Konzept in einem Codesystem
>
> FHIR Value Sets bestehen aus:
> – Metadata (Name, Publisher, Version …)
> – Content Logical Definition (compose) – Ein- und Ausschlusskriterien
>   – Codesysteme + Codes aufgelistet, oder Filter
>   – Wenn CodeSystem ohne Filter angegeben: gesamtes CodeSystem wird verwendet
> – Expansion – ‚Inhalt des Value Sets': Konzepte
>   – Ändert sich – ja nach Content Logical Definition – im Laufe der Zeit
>
> Beispiel: https://www.hl7.org/fhir/valueset-administrative-gender.html"

Folie 42 zeigt die UML-Struktur:
- ValueSet (DomainResource) mit Metadaten (url, identifier, version, name, title, status, experimental, date, publisher, contact, description, useContext, jurisdiction, immutable, purpose, copyright).
- `compose` (0..1) mit `lockedDate`, `inactive` und `include[1..*]` / `exclude[0..*]` (jeweils ConceptSet mit system, version, valueSet).
- ConceptSet kann konkrete `concept`-Referenzen enthalten (mit `designation`) oder `filter` (property, operator, value).
- `expansion` (0..1) mit `identifier`, `timestamp`, `total`, `offset`, `parameter`, `contains[0..*]` (system, abstract, inactive, version, code, display, designation; rekursiv).

## Bestandteile / Aufbau

| Teil | Inhalt | Pflicht? |
|---|---|---|
| Metadata | url, identifier, version, status, publisher … | wesentlich |
| Compose (Content Logical Definition) | include + exclude mit ConceptSet (System + Codes oder Filter) | optional aber meist nötig |
| Expansion | konkrete Liste (zur Laufzeit erzeugt) | bei Bedarf |

**Definitions­arten**:
- **Extensional**: explizite Aufzählung der Codes.
- **Intensional**: Regeln/Filter (z. B. „alle Konzepte unterhalb eines SNOMED-Knotens").

## Beispiel

Aus Folie 40+41: `https://www.hl7.org/fhir/valueset-administrative-gender.html` als FHIR-Standard-ValueSet für Geschlechts-Codes.

ELGA-Beispiel (siehe [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]): `ELGA_AdministrativeGender` mit OID `1.2.40.0.34.10.4` – als FHIR-ValueSet würde es eine canonical URL haben, z. B. `https://termgit.elga.gv.at/ValueSet-elga-administrativegender.html`.

## Abgrenzung

- **ValueSet ≠ CodeSystem**: ValueSet wählt Codes aus; CodeSystem definiert die Codes.
- **Compose ≠ Expansion**: Compose ist die Definition (statisch); Expansion ist die zur Laufzeit erzeugte Liste (kann sich ändern, wenn das zugrunde liegende CodeSystem wächst).
- **Intensional vs. Extensional**: Intensional erlaubt Wachstum mit dem Codesystem; Extensional ist eingefroren.
- **`include` vs. `exclude`**: explizite Ein- bzw. Ausschluss-Regeln. `include` ist Pflicht (mind. eines), `exclude` ist optional.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche Bestandteile hat eine FHIR ValueSet-Resource? Was unterscheidet Compose und Expansion?

**Anwendungsfrage:** Wie definieren Sie ein ValueSet, das alle SNOMED-Konzepte unterhalb von „Emotional state finding" enthält? (Intensional via Filter `concept is-a 106126000`.)

**Diskussionsfrage:** Welche Vor- und Nachteile haben intensionale vs. extensionale Definition?

**Mögliche Anschlussfragen:**
- Wie wird ein ValueSet expandiert? → [[MSI - HL7 FHIR - Terminology Service]] (`$expand`)
- Wie wird ein Code in einem ValueSet validiert? (`$validate-code`)
- Wie unterscheidet sich das von der CDA-Value-Set-Spezifikation? → [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]

## Verwandt

- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - HL7 FHIR - Terminology Framework]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]], [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: 40, 41, 42 (06er-VL); Seiten 43–51 (Anna Lin Starter)

## Ergänzung aus Anna-Lin-Gastvortrag

**Drei Identifikatoren eines ValueSets** (Seite 45):

| Feld | Eindeutigkeit | Veränderlichkeit |
|---|---|---|
| `id` | Server-spezifisch (kann auf anderem Server anders sein) | Kann sich bei Migration ändern |
| `url` | Globale kanonische ID des ValueSets | Ändert sich **nie** |
| `identifier` | Externe Referenz (z. B. OID in HL7v3) | Kontextabhängig |

```xml
<ValueSet>
  <id value="example-inline"/>
  <url value="http://hl7.org/fhir/ValueSet/example-inline"/>
  <identifier>
    <system value="http://acme.com/identifiers/valuesets"/>
    <value value="loinc-cholesterol-inl"/>
  </identifier>
</ValueSet>
```

**Inline CodeSystem innerhalb des ValueSets** (Seite 47):

Ein ValueSet kann ein eigenes CodeSystem inline definieren (inkl. Versionierung, Konzepte mit Designations):
```xml
<ValueSet>
  <codeSystem>
    <system value="http://acme.com/config/fhir/codesystems/cholesterol"/>
    <version value="4.2.3"/>
    <caseSensitive value="true"/>
    <concept>
      <code value="chol-mmol"/>
      <display value="SChol (mmol/L)"/>
      <definition value="Serum Cholesterol, in mmol/L"/>
    </concept>
  </codeSystem>
</ValueSet>
```

**Composition-Operatoren im Filter** (Seite 49): `=`, `is-a`, `is-not-a`, `regex`, `in`, `not-in`

**Begriffliche Klarstellung** (Seite 46): Expanded Value Sets wurden nicht „erweitert", sondern **ausgeklappt** – d. h. die intensionale Definition wurde zur Laufzeit zu einer expliziten Liste aufgelöst. Der englische Begriff „expand" bedeutet hier „entfalten".

**Composition: Import und Exclude** (Seiten 48–50):

`import` selektiert ein gesamtes ValueSet; `include` selektiert einzelne Werte; `exclude` schließt Werte aus (setzt voraus, dass sie durch `import`/`include` bereits enthalten sind):

```xml
<!-- Import + Include -->
<compose>
  <import value="http://hl7.org/fhir/ValueSet/v2-0136"/>
  <include>
    <system value="http://hl7.org/fhir/data-absent-reason"/>
    <concept>
      <code value="asked"/>
      <display value="Don't know"/>
    </concept>
  </include>
</compose>

<!-- Include mit Filter (parent = LP43571-6 in LOINC) -->
<compose>
  <include>
    <system value="http://loinc.org"/>
    <filter>
      <property value="parent"/>
      <op value="="/>
      <value value="LP43571-6"/>
    </filter>
  </include>
</compose>

<!-- Exclude eines einzelnen Konzepts -->
<compose>
  <exclude>
    <system value="http://loinc.org"/>
    <concept>
      <code value="5932-9"/>
      <display value="Cholesterol [Presence] in Blood by Test strip"/>
    </concept>
  </exclude>
</compose>
```

**Expansion-Struktur** (Seite 51):

Eine Expansion hat eine eindeutige `identifier`-UUID, einen `timestamp` und eine `contains`-Liste mit allen aufgelösten Konzepten:

```xml
<expansion>
  <identifier value="urn:uuid:bf99fe50-2c2b-41ad-bd63-bee6919810b4"/>
  <timestamp value="2015-07-14T10:00:00Z"/>
  <contains>
    <system value="http://hl7.org/fhir/v2/0136"/>
    <code value="Y"/>
    <display value="Yes"/>
  </contains>
  <contains>
    <system value="http://hl7.org/fhir/v2/0136"/>
    <code value="N"/>
    <display value="No"/>
  </contains>
</expansion>
```

**Historische Abgrenzung CodeSystem vs. ValueSet** (Seite 43):

- In FHIR **STU2** war CodeSystem kein eigenständiger Ressourcentyp — das „System" der Codes war immer einem ValueSet zugeordnet.
- Ab **STU3** ist CodeSystem als eigene Ressource eingeführt worden.
- Im Starter-PDF wird noch die STU2-Perspektive beschrieben: „Code System muss ValueSets enthalten, um die Codes zu gruppieren."
- Prüfungsrelevant: Die aktuelle FHIR-Version (R4/R5) hat CodeSystem als vollständig eigenständige Ressource.
