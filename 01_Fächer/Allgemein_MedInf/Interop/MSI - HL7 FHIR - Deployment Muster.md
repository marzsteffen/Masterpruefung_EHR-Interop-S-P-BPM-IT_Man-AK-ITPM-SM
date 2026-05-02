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

# MSI - HL7 FHIR - Deployment Muster

> [!info] Kurzdefinition
> Für die Einführung von FHIR in einer Organisation gibt es zwei Grundmuster: den FHIR Facade (FHIR-Interface über bestehende Systeme) und den FHIR Server (FHIR als zentrale Datenhaltung). Keines dieser Muster garantiert allein Interoperabilität – diese entsteht erst durch Profilierung.

## Beschreibung

### Muster 1: FHIR Facade

**Prinzip**: FHIR als Interface-Schicht über bestehende (Nicht-FHIR-)Systeme

| Vorteile | Nachteile |
|---|---|
| Keine Synchronisationsprobleme | IDs der Ressourcen sind schwer konsistent zu halten |
| Keine zusätzlichen Systeme | FHIR-Standard wird nur nach Bedarf genutzt (kein voller Funktionsumfang) |
| Bestehende Systeme bleiben unverändert | |
| Niedrige Einstiegshürde | |

**Einsatz**: Krankenhäuser mit gewachsenen Systemen (z. B. KIS, LIS), die FHIR-Schnittstellen nach außen anbieten wollen, ohne die interne Datenhaltung zu ändern.

### Muster 2: FHIR Server (zentralisierte Datenhaltung)

**Prinzip**: FHIR als primäres Datenhaltungssystem

| Vorteile | Nachteile |
|---|---|
| Volle FHIR-Funktionalität (abhängig vom Server) | Zusätzliches System zu verwalten |
| Vollständige History, Suche, Terminologie-Integration | Probleme bei doppelter Datenhaltung |
| Standardkonformes Datenmodell | Migration bestehender Daten notwendig |

**Einsatz**: Neue Systeme (Greenfield), nationale Plattformen, Research-Infrastruktur.

### Kritische Anmerkung

> „FHIR Server ≠ Interoperabilität"
>
> Ohne Spezifikation wie kommuniziert werden soll, Einschränkung von Codierungen und Spezifikationen der Ressourcen besteht keine Interoperabilität. **Profilierung & Implementierungsleitfäden führen zu Interoperabilität** mit anderen Organisationen.

Beide Muster sind technische Deployment-Entscheidungen. Semantische Interoperabilität entsteht erst durch:
- Vereinbarte Profile (nationale oder projektspezifische StructureDefinitions)
- Einheitliche Terminologien und Value Sets
- Implementation Guides als gemeinsame Spezifikation

## Abgrenzung

- **FHIR Facade** ist kein vollständiger FHIR-Server – er bietet nur die Teile an, die gebraucht werden. Die zugrundeliegenden Daten bleiben im Legacy-System.
- **FHIR Server** bietet potenziell vollen Funktionsumfang, aber nur wenn entsprechend konfiguriert und profiliert.
- Hybrid-Ansätze sind möglich: zentraler FHIR-Server mit Facades auf Legacy-Systemen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen FHIR Facade und FHIR Server?

**Anwendungsfrage:** Ein Krankenhaus hat ein bestehendes KIS ohne FHIR-Unterstützung. Welches Deployment-Muster wäre geeignet, um FHIR-Schnittstellen nach außen anzubieten?

**Diskussionsfrage:** Warum reicht ein technischer FHIR-Endpunkt für Interoperabilität nicht aus? Was muss organisatorisch und inhaltlich hinzukommen?

**Mögliche Anschlussfragen:**
- Was sind die Hauptnachteile eines FHIR Facade? (→ ID-Konsistenz, nur Teil-Implementierung)
- Was sind typische Probleme bei der Migration zu einem FHIR Server? (→ Datenmigration, Doppelhaltung)
- Wie verhält sich das ELGA-Ökosystem zu diesen Mustern?

## Verwandt

- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - Interoperabilität - Voraussetzungen]]
- [[MSI - Interoperabilität - Herausforderungen]]
- [[MSI - IHE XDS - Architektur]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seite 78
