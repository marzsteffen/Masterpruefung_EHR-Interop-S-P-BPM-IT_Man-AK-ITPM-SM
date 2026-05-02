---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR Starter (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - Reference

> [!info] Kurzdefinition
> Der FHIR-Datentyp `Reference` verlinkt auf andere FHIR-Ressourcen. Es gibt fünf Referenz-Arten (absolut, relativ, versionsspezifisch, kanonisch, lokal). Contained Resources sind eingebettete Ressourcen im `contained`-Feld – ein Anti-Pattern, das vermieden werden sollte.

## Beschreibung

### Referenz-Arten

Eine `Reference.reference` MUSS auf eine FHIR-Ressource zeigen. Es gibt fünf Formen:

| Art | Format | Beispiel |
|---|---|---|
| **Absolut** | Volle URL | `http://hapi.fhir.org/baseR4/Patient/1` |
| **Relativ** | Typ/ID | `Patient/1` |
| **Versionsspezifisch** | Typ/ID/_history/Version | `Patient/1/_history/2` |
| **Kanonisch** | URL mit optionaler Pipe-Version | `http://hl7.org/fhir/ValueSet/my-valueset\|0.8` |
| **Lokal** | #-Referenz auf Contained | `#1` |

### Kanonische URLs

- Die **Definition** einer FHIR-Ressource (StructureDefinition) ist selbst eine FHIR-Ressource
- Profile und StructureDefinitions existieren in verschiedenen FHIR-Versionen
- Einige Ressourcen haben eine **Version zusätzlich zur Meta-Version**
- Kanonische URL mit Pipe-Syntax `URL|Version` garantiert den Abruf der korrekten Version

### Contained Resources

- Jede Referenz kann „contained" sein: die referenzierte Ressource wird im `contained`-Feld der übergeordneten Ressource eingebettet
- Referenz zeigt mit `#Nr` auf das Contained-Objekt
- Beliebig verschachtelbar

```xml
<Condition>
  <contained>
    <Practitioner>
      <id value="p1"/>
      <name>
        <family value="Person"/>
        <given value="Patricia"/>
      </name>
    </Practitioner>
  </contained>
  <asserter>
    <reference value="#p1"/>
  </asserter>
</Condition>
```

> **Anti-Pattern-Warnung**: Contained Resources brechen (fast) alle Vorteile von FHIR und sollten nur mit guter Begründung verwendet werden (z. B. wenn die Anzahl separater Abfragen minimiert werden muss). Es gibt fast immer bessere Lösungen: **FHIR Document** oder **Bundles**.

## Abgrenzung

- **Reference** vs. **Identifier**: Reference zeigt auf eine konkrete Ressource am Server (ID-basiert). Identifier ist ein fachliches Identifikationsmerkmal (z. B. SVNR) – man kann per Identifier suchen, aber References sind ID-basiert.
- **Kanonische URL** vs. **Absolute URL**: Kanonische URLs referenzieren die *Definition* einer Ressource (z. B. ein Profil), absolute URLs zeigen auf eine *Instanz*.
- **Contained Resources** vs. **Bundle**: Beide gruppieren Ressourcen, aber Bundles sind eigenständige Entitäten und brechen die FHIR-Vorteile nicht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Referenz-Arten gibt es in FHIR? Was ist der Unterschied?

**Anwendungsfrage:** Wann würde man versionsspezifische Referenzen verwenden? (→ Wenn sich die referenzierte Ressource geändert haben könnte und die historische Version wichtig ist)

**Diskussionsfrage:** Warum sind Contained Resources ein Anti-Pattern? Welche FHIR-Vorteile brechen sie?

**Mögliche Anschlussfragen:**
- Wie wird eine kanonische URL mit Version gebildet? (→ `URL|Version`)
- Was passiert mit Contained Resources, wenn die übergeordnete Ressource gelöscht wird?
- In welchem Szenario sind Contained Resources trotzdem gerechtfertigt?

## Verwandt

- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Element]]
- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 FHIR - Versionen]]
- [[MSI - HL7 FHIR - Profil]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 28–32
