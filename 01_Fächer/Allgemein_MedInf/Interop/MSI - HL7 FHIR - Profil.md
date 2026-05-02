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

# MSI - HL7 FHIR - Profil

> [!info] Kurzdefinition
> Ein FHIR-Profil (StructureDefinition) spezialisiert eine Basis-Ressource für einen bestimmten Anwendungsfall oder nationalen Kontext: Felder werden verpflichtend gemacht, eingeschränkt oder um Extensions ergänzt. Erst Profilierung ermöglicht echte Interoperabilität – ein FHIR-Server allein garantiert sie nicht.

## Beschreibung

### Wozu werden Profile benötigt?

FHIR-Basis-Ressourcen decken sehr allgemeine Szenarien ab. Profile schaffen die Möglichkeit, Anwendungsfälle und bestimmte Kontexte (z. B. nationale Anforderungen) auf Grundlage der Basisressourcen zu beschreiben:

- **Strukturierte Darstellung** des Anwendungsfalls
- **Maschinelle Verarbeitbarkeit** (Validierung)
- **Basis für Validierung** von Ressourcen gegen nationale/internationale Anforderungen
- **Verfügbarkeit durch Veröffentlichung** in Registries

### Was definiert ein Profil?

Ein Profil (StructureDefinition) kann:
- **Kardinalitäten einschränken** (z. B. optionales Feld → verpflichtend: `0..1` → `1..1`)
- **Felder verbieten** (`0..0`)
- **Extensions hinzufügen** (nationale Felder)
- **Terminology Bindings verstärken** (z. B. `preferred` → `required`)
- **Slicing** anwenden (mehrfach vorkommende Felder nach Kriterien aufteilen)

### Verwendung in einer Ressource

```xml
<Patient>
  <id value="1"/>
  <meta>
    <profile value="http://hl7.at/fhir/3.0/StructureDefinition/AustrianPatient"/>
  </meta>
  ...
</Patient>
```

> `meta.profile` ist **optional** – eine Ressource muss nicht angeben, welche Profile sie erfüllt. Die Angabe erleichtert die Validierung, ist aber nicht zwingend für die Konformität.

### Profile veröffentlichen

Um Profile der Allgemeinheit zugänglich zu machen, werden sie in **FHIR Registries** verwaltet:
- **Simplifier.net**: frei und kommerziell verfügbar, Dependency Management
- **build.fhir.org**: HL7-Build-Server für offizielle IGs
- **profiles.ihe.net**: IHE-Profile (z. B. IHE SVCM)

### Implementation Guide (IG) als Kontext

> „Ohne Spezifikation wie kommuniziert werden soll, Einschränkung von Codierungen und Spezifikationen der Ressourcen besteht keine Interoperabilität. Profilierung & Implementierungsleitfäden führen zu Interoperabilität mit anderen Organisationen."

Ein **Implementation Guide (IG)** bündelt mehrere Profile, Extensions, ValueSets und ConceptMaps zu einem kohärenten Anwendungsfall (z. B. HL7 IPS IG, ELGA FHIR IG, AT Core Profile).

## Beispiel

Nationales Profil für österreichische Patienten (`AustrianPatient`):
- Verpflichtend: `Patient.identifier` mit SVNR
- Extension: `patient-citizenship` für Staatsbürgerschaft
- Binding: `Patient.gender` auf österreichisches Administrative-Gender-ValueSet

## Abgrenzung

- **Profil** vs. **Extension**: Profile beschreiben die Struktur und Einschränkungen; Extensions fügen neue Felder hinzu. Beides sind StructureDefinitions, aber unterschiedliche Typen.
- **FHIR Server** ≠ **Interoperabilität**: Ein FHIR-Server kann Ressourcen ohne Profile speichern und abrufen. Echte semantische Interoperabilität entsteht erst durch Profilierung.
- **Basisprofil** vs. **nationales Profil** vs. **Projekt-Profil**: Profil-Hierarchie von allgemein nach spezifisch.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein FHIR-Profil, und wozu dient es?

**Anwendungsfrage:** Österreich möchte SVNR und Versicherungskennzeichen als Pflichtfelder für Patientenressourcen einführen. Wie löst man das in FHIR?

**Diskussionsfrage:** „FHIR Server ≠ Interoperabilität" – was bedeutet das? Warum reicht ein technischer FHIR-Endpunkt für semantische Interoperabilität nicht aus?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen dem Differential Table und dem Snapshot Table in einer StructureDefinition? (→ Differential: Abweichungen vom Basisprofil; Snapshot: vollständige Definition)
- Wie sind Profile hierarchisch organisiert? (→ national → regional → projekt)
- Was ist ein Implementation Guide und wie unterscheidet er sich von einem Profil?

## Verwandt

- [[MSI - HL7 FHIR - Extension]]
- [[MSI - HL7 FHIR - Terminology Binding Strength]]
- [[MSI - HL7 FHIR - Validierung]]
- [[MSI - HL7 FHIR - Deployment Muster]]
- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 - International Patient Summary]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 57, 78–79
