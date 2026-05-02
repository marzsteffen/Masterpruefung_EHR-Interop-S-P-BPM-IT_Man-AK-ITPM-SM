---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 RIM - Reference Information Model

> [!info] Kurzdefinition
> RIM (Reference Information Model) ist das **standardisierte Informationsmodell** des HL7 V3 und liefert das semantische Fundament aller V3-Spezifikationen, einschließlich CDA. ANSI- und ISO-Standard (ISO/HL7 21731:2006). Backbone aus vier Klassen: **Entity, Role, Participation, Act** + zwei Beziehungs-Klassen: **Role Link, Act Relationship**.

## Beschreibung

Folie 6:

> „CDA ist ein Teil des HL7 V3 Standard und baut auf einem standardisierten Informationsmodell, dem RIM (Reference Information Model), auf
> Das RIM ist ein ANSI- und ISO-Standard (ISO/HL7 21731:2006) und bietet ein festes semantisches Fundament"

Der RIM-Backbone (Folie 7) zeigt vier Hauptklassen mit ihren Attributen:

- **Entity** – „etwas, das existiert" (Person, Organisation, Material, …)
  - `classCode: CS`, `determinerCode: CS`, `code: CE`, `statusCode: CS`, `id: II`
- **Role** – „in welcher Rolle wird die Entity wahrgenommen" (Patient, Practitioner, Organization-Member, …)
  - `classCode: CS`, `code: CE`, `effectiveTime: IVL<TS>`, `statusCode: CS`, `id: II`
- **Participation** – „wie nimmt eine Role an einem Act teil" (Subject, Performer, Author, …)
  - `typeCode: CS`, `time: IVL<TS>`, `statusCode: CS`
- **Act** – „etwas, das geschieht oder geschehen soll" (Observation, Procedure, Encounter, SubstanceAdministration, …)
  - `classCode: CS`, `moodCode: CS`, `code: CD`, `statusCode: CS`, `effectiveTime: GTS`, `id: II`

Beziehungs-Klassen:
- **Role Link** – verknüpft Roles untereinander.
- **Act Relationship** – verknüpft Acts untereinander.

## Bestandteile / Aufbau

| Backbone-Klasse | Bedeutung | Schlüssel-Attribute |
|---|---|---|
| Entity | Reale/abstrakte Existenz | classCode, determinerCode, code, statusCode, id |
| Role | Rolle einer Entity | classCode, code, effectiveTime, statusCode, id |
| Participation | Teilnahme einer Role an einem Act | typeCode, time, statusCode |
| Act | Handlung/Vorgang | classCode, moodCode, code, statusCode, effectiveTime, id |
| Role Link | Beziehung zwischen Roles | typeCode, effectiveTime |
| Act Relationship | Beziehung zwischen Acts | typeCode |

Folie 8 illustriert ein Beispiel:
- PersonA und PersonB sind Entities (`classCode <=PSN`).
- PersonA spielt die Role Practitioner (`classCode <=PRT`).
- PersonB spielt die Role Patient (`classCode <=PAT`).
- Practitioner nimmt als Performer (`typeCode <=PRF`) an einer Observation teil.
- Patient nimmt als Subject (`typeCode <=SUBJECT`) an derselben Observation teil.
- Observation ist ein Act (`classCode <=OBS`, `moodCode <=EVN`).

## Beispiel

Aus Folie 10 (RIM-Klassen im CDA):
```
<legalAuthenticator>          ←  Participation
  <time value="20080530140803"/>
  <signatureCode code="S"/>
  <assignedEntity>             ←  Role
    <id assigningAuthorityName="h.elga" root="1.1.2.3.127.4"/>
    <assignedPerson>           ←  Entity
      <name>Dr. Cardiologist</name>
    </assignedPerson>
    <representedOrganization>  ←  Entity
      <name>General University Hospital Graz</name>
      <telecom value="tel:+43-316-385.2544"/>
      ...
    </representedOrganization>
  </assignedEntity>
</legalAuthenticator>
```

Der `legalAuthenticator` ist die Participation, `assignedEntity` ist die Role, `assignedPerson` und `representedOrganization` sind Entities.

## Abgrenzung

- **RIM ≠ CDA**. RIM ist das abstrakte Informationsmodell; CDA ist eine spezifische Refinement (R-MIM) für medizinische Dokumente.
- **RIM ≠ Datenbank-Schema**. RIM modelliert Bedeutung, nicht Speicherung.
- **RIM ≠ Ontologie wie SNOMED CT**. RIM modelliert das *Informations*-Modell (wie Daten zusammenhängen), nicht die *Konzept*-Bedeutung (was ein Begriff bedeutet).

## Prüfungsrelevanz

**Hoch** – RIM-Verständnis trennt oberflächliche von vertieften CDA-Antworten.

**Typische Definitionsfrage:** Was ist das HL7 RIM? Welche vier Backbone-Klassen kennt es?

**Anwendungsfrage:** Identifizieren Sie in einem CDA-Snippet, welche Elemente Entities, Roles, Participations, Acts sind.

**Diskussionsfrage:** Wieso braucht es Roles als Zwischenstufe zwischen Entity und Participation? Was geht dadurch?

**Mögliche Anschlussfragen:**
- Welche ISO-Norm definiert RIM?
- Was bedeutet `moodCode` an einem Act? (z. B. EVN = Event, INT = Intent)
- Wie verhält sich RIM zum CDA R-MIM? → [[MSI - HL7 CDA - R-MIM]]

## Verwandt

- [[MSI - HL7 CDA - R-MIM]]
- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - Interoperabilität - Voraussetzungen]] (RIM als „gemeinsames Informationsmodell")

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 6, 7, 8, 10
