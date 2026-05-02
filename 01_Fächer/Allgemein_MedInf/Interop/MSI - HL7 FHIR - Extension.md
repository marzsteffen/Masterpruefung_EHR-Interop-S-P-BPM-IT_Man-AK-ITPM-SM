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

# MSI - HL7 FHIR - Extension

> [!info] Kurzdefinition
> Extensions sind URL-identifizierte Erweiterungen von FHIR-Ressourcen oder Datentypen. Sie ergänzen den Standard um nationale oder anwendungsspezifische Felder und können alleinstehend oder als Teil eines Profils auftreten.

## Beschreibung

- Extensions sind **alleinstehende Erweiterungen** einer Ressource (oder eines Datentyps) oder gehören zu einem Profil
- **Wichtig**: Eine Extension hat nie einen normalen Feldnamen – sie wird über eine **URL identifiziert**
- Die URL ist eindeutig und verweist auf die Definition der Extension (eine `StructureDefinition`)

### Wo dürfen Extensions auftreten?

- Auf **DomainResources** (alle klinischen Ressourcen)
- Auf **komplexen Datentypen** (erweiterbar und definierbar)
- Auf **primitiven Datentypen** (erweiterbar, aber nur via Underscore-Syntax: `_fieldName`)
- **Nicht** auf `Resource` direkt (technische Basis-Ressourcen sind nicht erweiterbar)

### Extension vs. ModifierExtension

- `extension`: erweitert eine Ressource um zusätzliche Information, **ändert nicht die Semantik** bestehender Felder
- `modifierExtension`: erweitert und **kann die Interpretation** bestehender Felder verändern – Systeme, die die Extension nicht kennen, dürfen die Ressource **nicht** verarbeiten

## Beispiel

```xml
<!-- Extension auf Patient: Geburtszeit -->
<extension url="http://hl7.org/fhir/StructureDefinition/patient-birthTime">
  <valueDateTime value="1974-12-25T14:35:45-05:00"/>
</extension>
```

- `url` = Pflichtfeld; identifiziert die Extension eindeutig
- `value[x]` = der Wert (Choice Element: valueDateTime, valueString, valueCodeableConcept, …)

## Abgrenzung

- **Extension** vs. **Profil**: Extensions definieren neue Felder; Profile schränken bestehende ein oder machen sie verpflichtend. Beides wird über StructureDefinitions beschrieben.
- **Alleinstehende Extension** vs. **Profil-Extension**: Alleinstehend = kann auf jeder Ressource ohne Profil verwendet werden. Profil-Extension = nur im Kontext eines bestimmten Profils gültig.
- **Extension** (erlaubt, ignorierbar) vs. **ModifierExtension** (muss verstanden werden, ändert Semantik).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine FHIR-Extension und wie wird sie identifiziert?

**Anwendungsfrage:** Österreich möchte das SVNR-Ausstellungsdatum zusätzlich zur SVNR speichern. Wie würde man das via Extension umsetzen?

**Diskussionsfrage:** Was ist der Unterschied zwischen `extension` und `modifierExtension`? Warum ist ModifierExtension potenziell gefährlich für Interoperabilität?

**Mögliche Anschlussfragen:**
- Warum werden Extensions über URLs identifiziert und nicht über Feldnamen?
- Kann jedes System Extensions ignorieren? (→ `extension` ja, `modifierExtension` nein)
- Wo sind Standard-Extensions von HL7 definiert? (→ `http://hl7.org/fhir/StructureDefinition/...`)

## Verwandt

- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Element]]
- [[MSI - HL7 FHIR - Ressourcentypen]]
- [[MSI - HL7 FHIR - Ressource Aufbau]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seite 37
