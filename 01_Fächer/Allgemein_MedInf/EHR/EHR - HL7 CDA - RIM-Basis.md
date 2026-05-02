---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - CCR und CCD]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - HL7 CDA - RIM-Basis

> [!info] Kurzdefinition
> **CDA** (Clinical Document Architecture, HL7 v3) basiert auf dem **RIM** (Reference Information Model) – dem zentralen Datenmodell von HL7 v3. Jedes XML-Element in einem CDA-Dokument muss einer **RIM-Klasse oder einem Klassen-Attribut** entsprechen.

## Beschreibung

Aus Folie 24:

> „CDA is based on RIM – Reference Information Model.
> Each XML-element in a CDA document must correspond to a RIM class or class attribute."

CDA ist der HL7-v3-Standard für klinische Dokumente. Es spezifiziert, wie ein Dokument strukturiert wird, das menschen-lesbar bleibt und gleichzeitig maschinen-verarbeitbare Strukturen enthält. CCD und C-CDA sind Implementierungen auf CDA-Basis.

## Bestandteile / Aufbau

### CDA-Aufbau (vereinfacht)

| Ebene | Inhalt |
|---|---|
| **Header** | Patient, Author, Custodian, Encounter, Document-Metadaten |
| **Body** | Eine oder mehrere **Sections** |
| **Section** | Section-Code (LOINC), Title, narrative `text`-Block, optional strukturierte `entry`-Elemente |
| **Entry** | Strukturierte Daten (Observations, Substance Administrations, Acts) – maschinen­verarbeitbar |

### RIM-Verbindung

Jedes XML-Element verweist auf eine **RIM-Klasse**:
- **Act** (Aktivität, z. B. Observation, Procedure)
- **Entity** (Akteur, z. B. Patient, Practitioner)
- **Role** (Rolle, z. B. Patient bei Versorger)
- **Participation** (Verbindung Act ↔ Role)
- **ActRelationship** (Verbindung zwischen Acts)

## Beispiel

Die Diagnose „Hypertonie" in einem CDA-Dokument:
- XML-Element: `<observation classCode="OBS" moodCode="EVN">`
- `classCode="OBS"` → RIM-Klasse `Observation` (Subklasse von `Act`)
- `moodCode="EVN"` → Event-Mood (tatsächlich beobachtetes Ereignis)
- `<code code="38341003" codeSystem="2.16.840.1.113883.6.96">` → SNOMED-CT-Code für „Hypertensive disorder"

So wird klinische Bedeutung über RIM-Strukturen + Coding-Standards transportiert.

## Abgrenzung

- **CDA ≠ FHIR:** CDA ist Dokument-zentriert, RIM-basiert, XML-only. FHIR ist Resource-zentriert, REST-basiert, JSON/XML, mit eigenem Datenmodell (deutlich pragmatischer als RIM).
- **RIM ist abstrakt:** RIM beschreibt **Akte und Rollen** generisch – CDA spezialisiert das auf klinische Dokumente. HL7 v3 Messaging spezialisiert es auf Nachrichten.
- **CDA ist menschen-lesbar by design** – jedes Section enthält einen narrativen `text`-Block.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worauf basiert CDA und welche Rolle spielt das RIM?

**Anwendungsfrage:** Wie wird eine SNOMED-CT-codierte Diagnose in einem CDA-Dokument strukturell abgebildet?

**Diskussionsfrage:** RIM ist sehr abstrakt und kompliziert – das hat zur Entwicklung von FHIR beigetragen. Welche Stärken hat RIM trotzdem?

**Mögliche Anschlussfragen:**
- Welche RIM-Hauptklassen gibt es? (Act, Entity, Role, Participation, ActRelationship)
- Was sind classCode, moodCode, statusCode in CDA?
- Wie unterscheidet sich CDA-Level 1, Level 2 und Level 3? (Antwort: Level 1 = nur Narrative; Level 2 = mit Section-Codes; Level 3 = mit strukturierten Entries)
- Wie verhält sich CDA-Inhalt in einer FHIR-Bundle-Migration?

## Verwandt

- [[EHR - CCD - Continuity of Care Document]]
- [[EHR - C-CDA - Consolidated CDA]]
- [[EHR - ELGA - Technologie-Architektur]]
- [[MSI - HL7 CDA]]
- [[MSI - HL7 - RIM]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folie 24 (CCD/CDA-RIM)
