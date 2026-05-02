---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Einführung und Definitionen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - ISO 18308 - Anforderungsspezifikation

> [!info] Kurzdefinition
> ISO 18308 ist ein internationaler Standard, der **minimale Anforderungen an EHR-Systeme** beschreibt – das „Was", aber nicht das „Wie". Versionen 2004 und 2011. Deckt strukturelle, funktionale, sicherheits- und legaltechnische Anforderungen sowie eine Referenzarchitektur ab.

## Beschreibung

ISO 18308 wird in der Vorlesung als formale **Requirement Specification** für EHR-Systeme eingeführt (Folien 73–83).

**Grundprinzip:**
- Beschreibt „WHAT", nicht „HOW"
- Macht **keine** Vorgaben zu Technologien, Standards, Hardware, Software
- Beschreibt **keinen** spezifischen klinischen Prozess oder kein konkretes Klinik-Datenmodell

**Inhaltliche Bereiche:**

### Strukturmodell
- EHR soll **Sektionen** enthalten – pro Sektion sollen unterschiedliche Sichten erstellbar sein
- Realisierung der Sektionen wird **nicht** beschrieben
- Mindestliste an Inhalten ist **nicht** mandatory, aber Anamnese, körperliche Untersuchung etc. werden erwähnt

### Privacy and Security
- Anforderungen für Privacy, Vertraulichkeit, Consent, Access und Audit Control
- **Keine** technischen Detail-Anforderungen
- Zugriffsrechte (auch Änderungen) müssen auf **Sektions-Ebene** möglich sein
- **Anonymisierung für Forschung** ist **nicht** beschrieben

### Legal Aspects
- Spezifiziert **Actor Identification**
- Es muss möglich sein, jeden Record-Zustand einer früheren Version wiederherzustellen → **keine Löschungen**, sondern **Versionierung**
- Jede Aktion (Read, Write, Insert, Update, Verify, Transmit) muss aufgezeichnet werden – mit Datum, Zeit, Ort

### Exchange Specification
- Schlägt Standards wie HL7, DICOM vor – **mandatiert** sie aber **nicht**
- Austausch von Teilen der EHR muss möglich sein
- Listet mögliche Technologien (XML, CORBA, .NET) – ohne Vorgabe

## Bestandteile / Aufbau

Abkürzungen aus dem Standard-Kontext (Folie 74):
- SDO = Standardization Organization
- IS = International Standard
- SIG = Special Interest Group
- TC = Technical Committee
- ISO = International Organization for Standardization
- TS = Technical Specification
- TR = Technical Report

## Beispiel

Konsequenz aus „no deletions, only versioning": Wenn ein Arzt eine Diagnose ändert, wird die alte Version nicht überschrieben, sondern als historischer Stand erhalten – jede ältere Version muss rekonstruierbar sein.

## Abgrenzung

- ISO 18308 ist **funktional** auf normativer Ebene – im Sinne von [[EHR - Anforderungen - Funktional vs Technisch]] ein „Was"-Dokument.
- Abgrenzung zu HL7, DICOM, IHE: Diese sind konkrete Implementierungs-Standards. ISO 18308 ist agnostisch.
- ISO/TR 20514 (siehe [[EHR - Definition - ISO TR 20514]]) ist **definitorisch**, ISO 18308 ist **anforderungsspezifizierend** – beide Standards sollten nicht verwechselt werden.
- Anonymisierung für Forschung ist **explizit nicht** Teil – wer das braucht, muss zusätzliche Vorgaben heranziehen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was beschreibt ISO 18308? Was beschreibt sie nicht?

**Anwendungsfrage:** Warum mandatiert ISO 18308 keine Technologien? Welcher methodische Vorteil ergibt sich daraus?

**Diskussionsfrage:** „Keine Löschungen, nur Versionierung" – wie verhält sich diese Forderung zu DSGVO Artikel 17 (Recht auf Löschung)? Spannungsfeld zwischen Versorgungs-Lückenlosigkeit und Datenschutz.

**Mögliche Anschlussfragen:**
- Welche Versionen von ISO 18308 gibt es, und worin unterscheiden sie sich? (PDF nennt 2004 und 2011, aber keine Detail-Differenzen)
- Wie verhält sich ISO 18308 zu ISO/TR 20514?
- Was bedeutet „Section-level access rights" praktisch (Beispiel ELGA)?
- Welche typischen Lücken hat ISO 18308 (Anonymisierung, konkrete CDS-Anforderungen)?

## Verwandt

- [[EHR - Definition - ISO TR 20514]]
- [[EHR - Anforderungen - Funktional vs Technisch]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[ASP - Audit Trail]]
- [[ASP - Versionierung statt Löschung]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 73–83 (ISO 18308: Abkürzungen, Process, Publications, Requirement Specification, Privacy/Security, Legal Aspects, Exchange Specification)
