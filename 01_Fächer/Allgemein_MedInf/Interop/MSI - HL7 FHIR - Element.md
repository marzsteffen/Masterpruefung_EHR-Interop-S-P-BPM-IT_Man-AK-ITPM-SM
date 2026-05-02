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

# MSI - HL7 FHIR - Element

> [!info] Kurzdefinition
> Felder in FHIR-Ressourcen bestehen aus Elementen. Ein Element entspricht einem Feld, hat einen Datentyp (primitiv oder komplex), eine Kardinalität und optional Choices ([x]). Backbone Elements gruppieren logisch zusammengehörige Felder implizit.

## Beschreibung

### Grundbegriffe

- **1 Element = 1 Feld** in einer Ressource
- **Backbone Element**: Implizite Gruppierung von zusammengehörigen Feldern innerhalb einer Ressource (keine eigenständige Ressource, kein eigener Typ)

### Datentypen

**Primitive Datentypen** (z. B. `string`, `boolean`, `integer`, `date`, `uri`):
- Erweiterbar (via Underscore-Extensions: `_fieldName`)
- Aber **nicht eigenständig definierbar** (kein eigener Namespace)
- Reifegrad in der FHIR-Doku durch Farben markiert (nicht alle sind normativ/grün)

**Komplexe Datentypen** (z. B. `Coding`, `CodeableConcept`, `HumanName`, `Address`, `Reference`):
- Erweiterbar **und** definierbar (können selbst Extensions haben, können profiliert werden)
- Können andere komplexe Datentypen verwenden (Beispiel: `CodeableConcept.coding` enthält `Coding`)
- Können Ressourcen **indirekt** über `Reference` verwenden

### Kardinalitäten

Jedes Feld hat eine Kardinalität (`min..max`):

| Kardinalität | Bedeutung |
|---|---|
| `0..0` | Feld nicht erlaubt (nur in Profilen zum Verbieten) |
| `0..1` | Optional, maximal einmal |
| `0..*` | Optional, beliebig wiederholbar |
| `1..1` | Verpflichtend, genau einmal |
| `1..*` | Verpflichtend, mindestens einmal wiederholbar |

> Verpflichtende Felder (`1..`) sind in der Basis-Spezifikation selten – Profile können Felder auf `1..` hochsetzen.

### Choice Elements [x]

- Markiert mit `[x]` im Feldnamen
- Unter dem Feld werden mehrere Typoptionen angeboten
- Eine Ressource kann **nur eine der Optionen** umsetzen
- Der Feldname in der Ressource enthält den vollen Typnamen
- Beispiel: `Patient.deceased[x]` → in der Ressource entweder `Patient.deceasedBoolean` oder `Patient.deceasedDateTime`

## Beispiel

```xml
<!-- Choice Element: nur eine der folgenden Optionen -->
<deceasedBoolean value="false"/>
<!-- oder -->
<deceasedDateTime value="2024-01-15"/>
```

```xml
<!-- Backbone Element: Component in Observation (Gruppierung für Blutdruck) -->
<component>
  <code>...</code>
  <valueQuantity>...</valueQuantity>
</component>
```

## Abgrenzung

- **Element** vs. **Ressource**: Elemente sind Felder innerhalb einer Ressource; Ressourcen sind eigenständige FHIR-Entitäten mit eigenem Endpunkt.
- **Backbone Element** vs. **eigenständiger komplexer Datentyp**: Backbone Elements existieren nur im Kontext ihrer Ressource (kein Wiederverwendung); Datentypen (Coding, HumanName) sind universell wiederverwendbar.
- **Primitive vs. komplexe Datentypen**: Primitive können nicht eigenständig profiliert werden; komplexe Datentypen können per StructureDefinition eingeschränkt oder erweitert werden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein FHIR-Element, und was ist der Unterschied zwischen primitivem und komplexem Datentyp?

**Anwendungsfrage:** Ein nationales Profil will ein Feld verpflichtend machen und ein anderes verbieten. Wie werden Kardinalitäten dafür eingesetzt?

**Diskussionsfrage:** Warum sind Choice Elements ([x]) nützlich, aber potenziell problematisch für Interoperabilität? (→ Wenn jeder eine andere Option wählt, ist kein einheitlicher Datenaustausch möglich)

**Mögliche Anschlussfragen:**
- Was ist ein Backbone Element? Gib ein Beispiel. (→ `Observation.component` für Blutdruckmessung)
- Was bedeutet `0..0` in einem Profil? (→ Feld ist verboten – Einschränkung)
- Kann ein komplexer Datentyp andere Ressourcen referenzieren? (→ Ja, indirekt via `Reference`)

## Verwandt

- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Reference]]
- [[MSI - HL7 FHIR - Extension]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 24–26, 33–34
