---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Macro-Level Interoperabilität]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - ContSys - ISO 13940

> [!info] Kurzdefinition
> ISO 13940 (ContSys) ist ein internationales **System of Concepts to support continuity of care**. Es liefert ein ontologisches Backbone für Versorgungs­prozesse: Akteure, Aktivitäten, Health States, Health Conditions und Clinical Pathways – als Grundlage für Daten-Mehrfachnutzung.

## Beschreibung

Die Vorlesung positioniert ContSys (ISO 13940) als **die ontologische Grundlage** auf der Schicht „Process Composability" in Tolks LCIM. Das wesentliche Argument der Folien:

> „Health data policy shall empower pervasive data stewardship.
> Policy: data sharing regulations shall be harmonized against an explicit ontology (ContSys).
> Rationale: the continuity of health care processes (including the treatment process) is based on effective digitalization, the prerequisite for effective digitalization is multiple use of data, the prerequisite for multiple use of data is a compatible system of concepts."

Konzeptuelle Bausteine, die in der Folien-Grafik gezeigt werden:
- **Healthcare actor** beobachtet einen **Health state** und führt eine **Healthcare activity** durch (mit **Healthcare activity period** und **Healthcare activity goal**).
- Eine **Health condition** wird als **Observed condition** erfasst und zeigt eine **Health condition evolution**.
- Ein **Clinical pathway** governs die Auswahl der Aktivitäten und adressiert die Health condition.

## Bestandteile / Aufbau

Zentrale ContSys-Konzepte (laut Folie):
- Healthcare actor (Versorgungs-Akteur)
- Health state / Health condition / Observed condition
- Health condition evolution
- Healthcare activity / Healthcare activity period / Healthcare activity goal
- Healthcare investigation
- Clinical pathway

Impacts laut Folie „Health data policy shall empower pervasive data stewardship":
- Selection und Adaptation eines Concept Systems (ContSys ISO 13940)
- Etablierung des Prinzips ontologischer Kompatibilität von Datenanforderungen
- Comprehensive Management Environment für Datenanforderungen
- Tool für systematische Validierung von Datenanforderungen
- Linking von Data Needs, Information Models, Terminologien und Message Templates zu validierten Anforderungen

## Beispiel

PDF-Beispiel: Eine Ambulanz-Guideline („when blood pressure < 100 mmHg") wird in narrative Sprache verfasst. Sekundärnutzungs-Anforderungen („we need to know who, when and why") müssen daraus ableitbar sein. ContSys liefert die Konzepte (Healthcare actor, Healthcare activity period), mit denen die Guideline strukturiert verlinkt werden kann.

## Abgrenzung

- ContSys ist eine **Ontologie / Concept System**, kein Datenformat. Es legt fest, *was* die Begriffe bedeuten, nicht *wie* sie übertragen werden (das machen FHIR, CDA).
- Zum Verhältnis FHIR ↔ ContSys: ContSys liefert die Bedeutungs-Schicht, die FHIR-Resourcen mit ihren Referenzen abbildet (Patient, Encounter, Condition, CarePlan).
- ContSys ist nicht zu verwechseln mit Snomed CT (Terminologie für klinische Begriffe).
- **Versionsangabe:** Im PDF nicht explizit angegeben. ISO 13940:2015 ist die international gültige Version (Ergänzung außerhalb der Vorlesung).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was beschreibt ISO 13940 (ContSys), und was unterscheidet es von einem Datenformat?

**Anwendungsfrage:** Wie könnte eine Ambulanz-Guideline gegen ContSys strukturiert werden, um spätere Sekundärnutzung zu ermöglichen?

**Diskussionsfrage:** Warum reicht es nicht, nur Datenformate zu standardisieren – warum braucht es zusätzlich ein gemeinsames Konzept-System?

**Mögliche Anschlussfragen:**
- Wie verhält sich ContSys zu HL7 FHIR (Mapping)?
- Welche Rolle spielt der „Healthcare actor" in ContSys – und wie unterscheidet sich das vom FHIR-Practitioner?
- Was ist „pervasive data stewardship" und wie hängt es mit ContSys zusammen?
- In welchen Ländern ist ContSys praktisch im Einsatz? (Antwort aus Vortrag: Estland, basierend auf Metsalliks Berufserfahrung)

## Ergänzung außerhalb der Vorlesung

ISO 13940:2015 trägt den vollständigen Titel „Health informatics – System of concepts to support continuity of care". Die Norm ist eine internationale Weiterentwicklung des europäischen Vorgängers EN 13940. Sie ist insbesondere in skandinavischen und baltischen Ländern als Backbone für nationale eHealth-Architekturen verbreitet.

## Verwandt

- [[EHR - Interoperabilität - LCIM nach Tolk]]
- [[EHR - Architektur - ISO 23903 3D]]
- [[EHR - HL7 FHIR - 5 Levels]]
- [[EHR - Governance - Data Sharing Rollen]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folien „Levels of interoperability" (oberste Schicht ISO 13940), „Concepts (ContSys)", „Health data policy shall empower pervasive data stewardship", „Ambulance guidelines / Secondary usage requirements"
