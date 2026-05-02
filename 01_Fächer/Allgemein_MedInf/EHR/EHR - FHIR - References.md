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

# EHR - FHIR - References

> [!info] Kurzdefinition
> FHIR-**References** verbinden Resources über URLs, statt Daten zu nesten. Eine „Sache" wird **einmal** beschrieben und kann **mehrfach referenziert** werden – relativ, absolut, intern oder extern, optional versions-spezifisch.

## Beschreibung

Aus den Folien 37–43:

> „In CDA, there is little support for referencing other 'objects'.
> The same medical doctor can be described several times within a single CDA document – Can be in different participations.
>
> In FHIR, a 'thing' (Resource) is defined/described once and can be referenced many times."

> „References are always URLs – Absolute or relative – Internal or external."

## Bestandteile / Aufbau

### Reference-Arten

| Typ | Beispiel | Anwendung |
|---|---|---|
| **Relative Internal** | `Patient/example` | innerhalb desselben FHIR-Servers |
| **Absolute External** | `https://server.com/Patient/12345` | über Server-Grenzen hinweg |
| **Versionsspezifisch** | `Patient/example/_history/2` | exakte historische Version |
| **Contained** | im selben JSON/XML eingebettet, mit Hash-Reference | nur für Resources ohne unabhängige Existenz |

### Pflicht-Eigenschaften

- References **müssen immer auf eine Resource zeigen**
- External URL **muss nicht** ein FHIR-RESTful-Server sein
- Aber: RESTful Server ist der **bevorzugte Ansatz**

### Beispiele aus Folie 40

```xml
<!-- Relative Reference -->
<subject>
  <reference value="Patient/034AB16"/>
</subject>

<!-- Absolute Reference auf Profile -->
<profile>
  <reference value="http://fhir.hl7.org/svc/StructureDefinition/c8973a22-2b5b-4e76-9c66-00639c99e61b"/>
</profile>

<!-- Version-spezifisch -->
<patient>
  <reference value="Patient/example/_history/2"/>
</patient>
```

## Beispiel

Ein Hausarzt versorgt drei Patienten am gleichen Tag. In CDA müssten seine Daten in jedem der drei Documents wiederholt werden. In FHIR existiert er **einmal** als `Practitioner/dr-mustermann`-Resource, und alle drei `Encounter`-Resources referenzieren ihn:

```json
{
  "resourceType": "Encounter",
  "subject": { "reference": "Patient/p001" },
  "participant": [
    {
      "individual": { "reference": "Practitioner/dr-mustermann" }
    }
  ]
}
```

Vorteile: weniger Redundanz, atomare Updates, eindeutige Identität.

## Abgrenzung

- **Reference ≠ Identifier:** Identifier ist eine Business-ID (z. B. SVNR). Reference ist ein technischer Verweis auf eine FHIR-Resource. Eine Reference kann durch einen Identifier zusätzlich qualifiziert werden (`Reference.identifier`).
- **External Reference ≠ FHIR-only:** Eine Reference darf auf eine beliebige URL zeigen, der RESTful-FHIR-Server ist aber Standard.
- **Versions-Reference vs. Latest:** Wenn man eine bestimmte historische Version referenziert, friert man den Stand ein – wichtig für Audit-Sicherheit.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie funktionieren References in FHIR? Welche Arten gibt es?

**Anwendungsfrage:** Schreibe eine FHIR-Reference in JSON-Form auf den Patient mit ID 12345. Relative und absolute Variante.

**Diskussionsfrage:** Eine Reference ohne Versionsangabe verweist auf den **aktuellen** Stand der Ziel-Resource. Welche Probleme können entstehen, wenn sich diese Resource nach dem Erzeugen der referenzierenden Resource ändert?

**Mögliche Anschlussfragen:**
- Was ist eine Contained Resource und wann nutzt man sie?
- Wie wirken sich References auf die Konsistenz von Bundles aus?
- Wie unterscheidet sich Reference in FHIR von Foreign Keys in relationalen Datenbanken?
- Welche Implikationen haben absolute References für Privacy (URLs verraten Server-Strukturen)?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - REST API und CRUD]]
- [[EHR - HL7 CDA - RIM-Basis]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 37–43 (References vs Nesting, URL-Arten, Examples)
