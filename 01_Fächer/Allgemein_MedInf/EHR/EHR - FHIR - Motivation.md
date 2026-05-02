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

# EHR - FHIR - Motivation

> [!info] Kurzdefinition
> FHIR (Fast Healthcare Interoperability Resources) wurde entwickelt, weil ältere HL7-Standards (v2, v3, CDA) für moderne Web-Implementierungen ungeeignet sind: zu steile Lernkurve, fehlende Unterstützung für verteilte Information, schlechte Entwicklerfreundlichkeit. FHIR setzt auf bekannte Web-Technologien.

## Beschreibung

Aus den Folien 3–4:

> „CDA has a very steep 'learning curve'. CDA is not very 'developer friendly'.
> HL7-v3 nearly not used for messages – Users stick to HL7-v2 messages.
> HL7 standards do not have support for distributed information – You may have one blood pressure reading in Graz, another one in Innsbruck – how do you combine?
>
> Focus on implementation – 'From implementers for implementers'.
> Usual scenarios are kept simple.
> Based on (for implementers) known technologies: XML, JSON, RDF, RESTful web service.
> Freely available to everyone – Was not always the case with HL7-v3 / CDA.
> Demonstrates 'best practices'."

Folie 6 ergänzt:

> „Specification is written for a single target group: the implementers. Reference implementations are immediately available. Public test servers are available. Starter APIs in different languages (Java, C#, Delphi, …) are published together with the specification."

## Bestandteile / Aufbau

### Treiber für FHIR

| Problem mit Vorgängern | FHIR-Antwort |
|---|---|
| CDA: steile Lernkurve, RIM-Komplexität | Pragmatisches Datenmodell, kein RIM-Zwang |
| HL7 v3 Messaging: kaum genutzt | REST + JSON/XML statt v3 Messaging |
| HL7 v2: weit verbreitet, aber alt | FHIR ergänzt (nicht ersetzt) v2 graduell |
| Keine Unterstützung verteilter Daten | References per URL → globale Adressierung von Resources |
| Spezifikationen teils kostenpflichtig | Frei verfügbar |
| Wenig Implementer-Support | Reference Implementations, Test-Server, Starter-APIs |
| Keine modernen Web-Technologien | XML + JSON + RDF + REST |

### Marktdruck

Folie 2: **75 % der Digital-Health-Companies** nutzen FHIR (Studie mit N = 141 Unternehmen).

## Beispiel

Konkretes Problem aus der Vorlesung: Ein Patient hat eine Blutdruckmessung in Graz, eine andere in Innsbruck. Wie kombinieren? Mit FHIR sind beide Messungen `Observation`-Resources mit eindeutiger URL – ein Aggregator kann sie über REST-Calls zusammenziehen, ohne zentralen Speicher.

## Abgrenzung

- FHIR ersetzt **nicht** v2 oder CDA von heute auf morgen – Co-Existenz ist Alltag (siehe ELGA mit CDA).
- FHIR ist **nicht** bedeutet automatisch semantische Interoperabilität – Coding-Standards (LOINC, SNOMED) bleiben Voraussetzung.
- FHIR ist **kein** EHR-System, sondern Exchange-Format/-API (siehe [[EHR - System vs Exchange Format]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Warum wurde FHIR entwickelt? Welche Probleme der Vorgänger-Standards adressiert es?

**Anwendungsfrage:** Welcher konkrete Use-Case (z. B. verteilte BP-Messungen) wird durch FHIR einfacher als durch CDA?

**Diskussionsfrage:** „From implementers for implementers" – ist das eine Stärke (pragmatisch, schnell adoptiert) oder eine Schwäche (möglicher Verlust von theoretischer Strenge wie bei RIM)?

**Mögliche Anschlussfragen:**
- Welche Web-Technologien sind die FHIR-Grundlage?
- Wie unterscheidet sich FHIR von HL7 v2 in der Verbreitung?
- Was ist der Unterschied zwischen „FHIR" und „RIM"?
- Wie reagiert FHIR auf das Verteilungs-Problem konkret? (Antwort: References per URL)

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - FHIR - References]]
- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - System vs Exchange Format]]
- [[EHR - HL7 FHIR - 5 Levels]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 2–6 (Why FHIR, Specification, History)
