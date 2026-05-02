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

# MSI - ClaML - Classification Markup Language

> [!info] Kurzdefinition
> ClaML (*Classification Markup Language*) ist eine XML-Notation für hierarchische medizinische Klassifikationen wie ICD-10. CEN/TS 14463:2003 / EN 14463:2007. Seit 2005 von der WHO eingesetzt. Aktuelle Version: ClaML 3.0.

## Beschreibung

Folie 12 zeigt den Aufbau:

> „XML-Notation, entwickelt für Klassifikationen, etwa ICD-10
> – Seit 2005 von WHO eingesetzt
> – Aktuelle Version: ClaML 3.0
>
> Überblick über den Aufbau
> – Wurzelelement einer Klassifikation: ClaML mit Subelementen wie title und identifier
> – Konzepte (also z. B. Kapitel, Gruppen, Diagnosen): Class
> – Attribute über meta code value Paare bzw. Modifier und ModifierClass
> – Textelemente über rubric-Elemente"

Quelle des Class-Elements-Diagramms laut Folie: DIMDI ClaML Kurzdokumentation. Das Class-Element hat Attribute (`code`, `kind`, `usage`, `variants`) und Subelemente (`Meta`, `SuperClass`, `SubClass`, `ModifiedBy`, `ExcludeModifier`, `Rubric`). Rubric enthält ein `Label`, das wiederum Reference, Term, Para, Fragment enthalten kann.

## Bestandteile / Aufbau

| Element | Funktion |
|---|---|
| `<ClaML>` | Wurzelelement der Klassifikation |
| `<Title>`, `<Identifier>` | Klassifikations-Metadaten |
| `<Class>` | Konzept (Kapitel, Gruppe, Diagnose) |
| `<Class @code>` | Code des Konzepts |
| `<SuperClass>`, `<SubClass>` | Hierarchie-Beziehungen |
| `<Meta name=… value=…/>` | Beliebige Attribute |
| `<Rubric>` mit `<Label>` | Textelemente |
| `<ModifiedBy>`, `<ExcludeModifier>` | Modifier-Beziehungen |

## Beispiel

Aus Folie 13 (gekürzter ClaML-2.0-Auszug für HL7 Administrative Gender):

```xml
<ClaML version="2.0.0">
  <Meta name="description" value=""/>
  <Meta name="status_date" value="2019-06-26 14:26:59.0"/>
  <Meta name="last_change_date" value=""/>
  <Meta name="unvollstaendig" value="false"/>
  <Meta name="gueltigkeitsbereich" value="optional"/>
  <Meta name="statusCode" value="1"/>
  <Identifier authority="" uid="2.16.840.1.113883.5.1"/>
  <Title date="2019-06-26" name="HL7 Administrative Gender" version="2019..."/>
  <RubricKinds>
    <RubricKind inherited="false" name="preferred"/>
  </RubricKinds>
  <Class code="F">
    <Meta name="Level" value="0"/>
    <Meta name="Type" value="L"/>
    <Meta name="TS_ATTRIBUTE_MEANING" value="Weiblich"/>
    <Meta name="TS_ATTRIBUTE_ISLEAF" value="true"/>
    <Meta name="TS_ATTRIBUTE_MAJORREVISION" value="1"/>
    <Meta name="TS_ATTRIBUTE_MINORREVISION" value="0"/>
    <Meta name="TS_ATTRIBUTE_STATUS" value="1"/>
    <Meta name="TS_ATTRIBUTE_STATUSDATE" value="2019-06-26"/>
    <Rubric kind="preferred">
      <Label>Female</Label>
    ...
```

ClaML-Kurzdokumentation: `https://www.dimdi.de/static/.downloads/deutsch/claml-kurzdokumentation-20200526.pdf`.

## Abgrenzung

- **ClaML ≠ FHIR CodeSystem**: ClaML ist ein XML-Format speziell für Klassifikationen; FHIR CodeSystem ist die FHIR-Resource für allgemeine Code Systems. Konvertierungen sind möglich.
- **ClaML ≠ HL7 V3 RIM**: andere Welt; ClaML kann RIM-unabhängig genutzt werden.
- **ClaML ≠ ICD-10 selbst**: ClaML ist die Markup-Sprache, ICD-10 ist eine *Klassifikation*, die *in* ClaML kodiert sein kann.

## Prüfungsrelevanz

**Mittel.**

**Typische Definitionsfrage:** Was ist ClaML? Welche Norm steht dahinter, welche Version ist aktuell?

**Anwendungsfrage:** Welche XML-Elemente strukturieren ein ClaML-Dokument?

**Diskussionsfrage:** Wann würden Sie ClaML verwenden, wann FHIR CodeSystem?

**Mögliche Anschlussfragen:**
- Welche WHO-Klassifikationen nutzen ClaML? (ICD-10 als prominentes Beispiel)
- Wie wird die Hierarchie ausgedrückt? (SuperClass/SubClass)
- Was leistet `<Meta>` zusätzlich?

## Verwandt

- [[MSI - Terminologieserver - Austauschstandards]]
- [[MSI - Ordnungssystem - Klassifikation]]
- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - Terminologie - Definition]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 12, 13 (Quelle: DIMDI ClaML Kurzdokumentation)
