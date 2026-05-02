---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - FHIR Grundlagen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - FHIR - Profiles und Must Support

> [!info] Kurzdefinition
> **Profiles** sind lokale Einschränkungen/Erweiterungen einer FHIR-Base-Resource für eine spezifische Domäne (Land, Organisation, Use-Case). **Must Support** ist eine Marker-Eigenschaft auf einem Datenelement, die Implementierern signalisiert, dass dieses Element bereitgestellt/verarbeitet werden muss – ohne dabei Pflicht zu sein.

## Beschreibung

Aus den Folien 21–24:

> „International FHIR specification need to be constrained further for local use—usually within a nation, an organization, or [implementation].
> Implementers to constrain and extend the base specification of a resource for a particular use case."

Beispiel **US Core Patient Profile** (Folie 22–23):
- Extra-Felder wie **race** und **ethnicity**, die im Base-Profile fehlen
- Cardinality von Identifier verschärft auf **1..\*** (mind. eins Pflicht)
- „**S**"-Quadrat in Rot kennzeichnet **Must Support**

## Bestandteile / Aufbau

### Was ein Profile macht

| Aktion | Beispiel |
|---|---|
| Cardinality verschärfen | Identifier von 0..* auf 1..* |
| Pflichtfelder hinzufügen | Race, Ethnicity in US Core |
| Datatypes weiter einschränken | bestimmte Identifier-Systeme erlauben |
| Coding via ValueSet einschränken | nur SNOMED CT für Conditions |
| Extensions definieren | US-spezifische Felder |
| Must Support markieren | Felder, die System unterstützen muss |

Profiles dürfen Cardinality **nur verschärfen, nie lockern**.

### Must Support vs Mandatory

Aus Folie 24:

| Aspekt | **Mandatory** | **Must Support** |
|---|---|---|
| Cardinality | min ≥ 1 (Pflicht) | unverändert (kann optional bleiben) |
| Sender-Pflicht | muss Wert liefern | muss Verarbeitung beherrschen |
| Empfänger-Pflicht | muss Wert akzeptieren | muss Wert akzeptieren und sinnvoll behandeln |
| Markierung | Cardinality `1..*` oder `1..1` | Roter „S"-Marker |

In der Praxis bedeutet **Must Support**: Das System muss das Feld lesen/schreiben können – aber wenn keine Daten vorliegen, ist das ok. Ein typischer Anwendungsfall: Ethnicity in US Core – ein System muss es unterstützen, aber der Patient kann sich verweigern.

## Beispiel

US Core Patient Profile (Folie 23):
- Extra-Felder: race, ethnicity
- Identifier: Cardinality verschärft auf **1..\***
- „S"-Marker auf vielen Feldern → System muss diese unterstützen, auch wenn nicht alle gefüllt sind

URL: build.fhir.org/ig/HL7/US-Core/StructureDefinition-us-core-patient.html

## Abgrenzung

- **Profile ≠ Resource:** Ein Profile schränkt eine Resource ein, ist aber keine eigenständige Resource. Technisch ist ein Profile eine `StructureDefinition`-Resource.
- **Profile ≠ Extension:** Profile passt vorhandene Felder an; Extension fügt **neue** Felder hinzu (siehe [[EHR - FHIR - Extensions und 80 20 Regel]]).
- **Must Support ≠ Mandatory:** Must Support sagt „behandeln können", Mandatory sagt „muss vorhanden sein".

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein FHIR-Profile? Was unterscheidet Must Support von Mandatory?

**Anwendungsfrage:** Wie würde ein österreichisches Patient-Profile (AT Core) aussehen, das die SVNR als Pflicht-Identifier vorsieht?

**Diskussionsfrage:** Profiles erlauben lokale Anpassung, aber zu viele Profile fragmentieren Interoperabilität. Welche Trade-offs entstehen?

**Mögliche Anschlussfragen:**
- Wie wird ein Profile technisch beschrieben? (Antwort: StructureDefinition-Resource mit baseDefinition + Differential + Snapshot)
- Welche bekannten Profile-Sets gibt es? (US Core, AT Core, ELGA-Profile, IPS, IPA)
- Wie funktioniert Profile-Validierung in der Praxis?
- Was passiert bei Konflikten zwischen mehreren angewendeten Profiles?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Data Types und Cardinality]]
- [[EHR - FHIR - Extensions und 80 20 Regel]]
- [[EHR - FHIR - Implementation Guides]]
- [[EHR - USCDI US Core Data for Interoperability]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 21–24 (Profiles, US Core Patient, Must Support vs Mandatory)
