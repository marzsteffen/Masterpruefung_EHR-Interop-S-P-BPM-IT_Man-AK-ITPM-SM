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

# MSI - HL7 FHIR - Ressourcentypen

> [!info] Kurzdefinition
> FHIR unterscheidet zwischen `Resource` (technische Basis mit Metadaten und Endpunkt, nicht erweiterbar) und `DomainResource` (medizinisch/organisatorisch relevante Erweiterung von Resource mit Narrative, Contained und Extensions). Die meisten klinischen FHIR-Ressourcen sind DomainResources.

## Beschreibung

### Typ 1: Resource

- Definiert **Metadaten** (`meta`) und **Identity** (`id`, `implicitRules`, `language`)
- Hat einen eigenen **REST-Ressourcen-Endpunkt** (z. B. `http://hapi.fhir.org/baseR4/Bundle`)
- Relevant für **technische Umsetzung**
- **NICHT erweiterbar** (keine Extensions, kein Narrative, kein Contained)

Beispiele für Resources (keine DomainResources):
- `Bundle` (Container für mehrere Ressourcen)
- `Binary` (binäre Inhalte)
- `Parameters` (Ein-/Ausgabe für Operationen)

### Typ 2: DomainResource (erbt von Resource)

- Ist **eine Resource** (erbt alle Resource-Felder)
- Zusätzlich: `text` (menschenlesbarer Narrativ), `contained`, `extension`, `modifierExtension`
- Relevant für **medizinische oder organisatorische Abläufe**
- **Erweiterbar** via Extensions (primitiv und komplex)

Beispiele für DomainResources (= die meisten klinischen Ressourcen):
- `Patient`, `Practitioner`, `Organization`
- `Observation`, `Condition`, `MedicationRequest`
- `AllergyIntolerance`, `Procedure`, `DiagnosticReport`

## Bestandteile / Aufbau

```
Resource
├── id
├── meta (versionId, lastUpdated, source, profile, security, tag)
├── implicitRules
└── language

DomainResource (erbt von Resource)
├── [alle Resource-Felder]
├── text (Narrative)
├── contained (eingebettete Ressourcen)
├── extension
└── modifierExtension
    └── [domänenspezifische Felder, z. B. Patient.name, .birthDate, …]
```

## Abgrenzung

- `Resource` ist die **abstrakte Basisklasse** – sie wird nicht direkt instanziiert (außer bei technischen Typen wie Bundle, Binary).
- `DomainResource` ist ebenfalls abstrakt, aber fast alle konkreten klinischen Ressourcen sind DomainResources.
- Die Trennung Resource / DomainResource ist wichtig für Profilierung: DomainResources erlauben Extensions; Resources nicht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen `Resource` und `DomainResource` in FHIR?

**Anwendungsfrage:** Ein Entwickler möchte eine Ressource um ein nationales Feld erweitern. Muss er prüfen, ob die Ressource eine DomainResource ist?

**Diskussionsfrage:** Warum sind technische Ressourcen wie `Bundle` nicht erweiterbar? Was würde passieren, wenn man `Bundle` mit Extensions anreichern könnte?

**Mögliche Anschlussfragen:**
- Welche Felder hat jede FHIR-Ressource gemeinsam? (→ id, meta, implicitRules, language)
- Welches Feld macht eine DomainResource erweiterbar? (→ extension / modifierExtension)
- Was ist der Unterschied zwischen `extension` und `modifierExtension`?

## Verwandt

- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - Extension]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Bundle]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 22–23
