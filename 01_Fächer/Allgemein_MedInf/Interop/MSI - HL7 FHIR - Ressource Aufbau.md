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

# MSI - HL7 FHIR - Ressource Aufbau

> [!info] Kurzdefinition
> Eine FHIR-Ressource besteht aus einer definierten Struktur mit Identity/ID, Metadaten, einem menschenlesbaren narrativen Text und fachlichen Datenelementen. Die Ressourcenhierarchie unterscheidet zwischen `Resource` (technisch) und `DomainResource` (medizinisch/organisatorisch).

## Beschreibung

### Generelle Struktur

Seite 17 des Vortrags zeigt das Diagramm „Generelle Struktur einer FHIR Ressource" (Abbildung, nicht als Text extrahierbar). Die Struktur besteht konzeptionell aus:

1. **Identity / ID** → eindeutige Identifizierung (siehe [[MSI - HL7 FHIR - Ressource Identity]])
2. **Metadaten** (`meta`) → serverseitig verwaltet (siehe [[MSI - HL7 FHIR - Ressource Metadaten]])
3. **Narrativer Text** (`text`) → menschenlesbarer Teil
4. **Contained Resources** → eingebettete Ressourcen (in DomainResources)
5. **Extensions** → Erweiterungen (in DomainResources)
6. **Fachliche Datenelemente** → domänenspezifische Felder

### Ressourcen-Hierarchie

```
Resource
└── DomainResource
    └── Patient, Observation, Condition, MedicationRequest, ...
```

**Resource** (Basis, technisch):
- Relevant für die **technische Umsetzung**
- Definiert: `id`, `meta` (Metadaten), `implicitRules`, `language`
- Jede Resource hat einen eigenen **REST-Ressourcen-Endpunkt** (z. B. `http://hapi.fhir.org/baseR4/Bundle`)
- Resource ist **NICHT erweiterbar** (keine Extensions, kein narrativer Text)

**DomainResource** (erbt von Resource, medizinisch/organisatorisch):
- Relevant für **medizinische oder organisatorische Abläufe**
- Fügt hinzu: `text` (Narrative), `contained`, `extension`, `modifierExtension`
- DomainResource **ist erweiterbar** (via Extensions)
- Die meisten FHIR-Ressourcen (Patient, Observation, etc.) sind DomainResources

### Narrativer Text (`text`)

- Soll von **jedem FHIR-System angezeigt werden können**
- Muss **genug Information enthalten**, um die Ressource allein verständlich zu machen
- Beinhaltet **nicht alle** strukturellen Informationen → „Invers zu CDA"

> **Vergleich CDA ↔ FHIR bezüglich Narrative**: In CDA ist der narrative Teil die **Primärquelle** – maschinenlesbare Daten sind optional. In FHIR sind strukturierte Daten primär; der Narrative-Text ist ein **Pflicht-Ergänzungsfeld** für Anzeigbarkeit.

## Abgrenzung

- `Resource` vs. `DomainResource`: Resource = technische Basis (z. B. Bundle, Binary, Parameters sind Resources, keine DomainResources). DomainResource = klinisch/organisatorisch relevant (Patient, Practitioner, Observation, …).
- `text` (Narrative) ist ein FHIR-Pflichtfeld in DomainResources (soll befüllt sein), aber kein Pflichtfeld für Interoperabilität im maschinellen Sinne.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Aus welchen Teilen besteht eine FHIR-Ressource strukturell?

**Anwendungsfrage:** Warum ist der Unterschied zwischen `Resource` und `DomainResource` relevant für Entwickler?

**Diskussionsfrage:** FHIR kehrt die CDA-Philosophie bezüglich Narrative um. Was sind die Implikationen für die semantische Interoperabilität?

**Mögliche Anschlussfragen:**
- Welche FHIR-Ressourcen sind keine DomainResources? (→ Bundle, Binary, Parameters)
- Was passiert mit dem narrativen Text, wenn eine Ressource maschinell verarbeitet wird?
- Warum ist `Resource` nicht erweiterbar, aber `DomainResource` schon?

## Verwandt

- [[MSI - HL7 FHIR - Ressourcentypen]]
- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - Element]]
- [[MSI - HL7 FHIR - Extension]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Levels]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 17, 20, 22–23
