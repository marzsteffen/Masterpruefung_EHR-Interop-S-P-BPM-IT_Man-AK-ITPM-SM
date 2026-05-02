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

# EHR - FHIR - Data Types und Cardinality

> [!info] Kurzdefinition
> Jedes FHIR-Datenelement hat einen **Data Type** (primitive wie boolean, string, date – oder komplex wie Identifier, HumanName, CodeableConcept) und eine **Cardinality** in `min..max`-Notation, die min. und max. Vorkommen festlegt (`*` = beliebig oft).

## Beschreibung

### Data Types

Aus den Folien 15–18:

> „Each data element has a Type. For example, the identifier is of the Identifier type, and clicking on the link takes you to the definition of what this type means.
> Some types are simple (or primitive) like active, which is a boolean (true or false), while others like identifier and name have another nested structure within and are complex.
> Containts other complex types like CodeableConcept and Period."

Quelle Datatypes-Übersicht: hl7.org/fhir/datatypes.html.

### Cardinality

Aus Folie 19:

> „The 'Card.' field stands for Cardinality and represents the minimum and maximum times a particular data element can appear using the notation minimum..maximum. A maximum value of * means 'as many times as needed' or ∞."

## Bestandteile / Aufbau

### Primitive Data Types (Auswahl)
- `boolean` – true/false
- `string` – beliebiger Text
- `integer`, `decimal`
- `date`, `dateTime`, `time`, `instant`
- `uri`, `url`, `canonical`
- `code` – aus einem ValueSet
- `id`, `oid`, `uuid`

### Komplexe Data Types (Auswahl)
- **Identifier** – mit System + Value + Type + Period
- **HumanName** – mit family, given, prefix, suffix, use
- **Address** – mit line, city, postalCode, country
- **ContactPoint** – Telefon/E-Mail mit Use
- **Period** – Start/End
- **CodeableConcept** – mit Coding (System + Code + Display) + Text
- **Coding** – einzelner Code aus einem CodeSystem
- **Quantity** (mit Sub-Typen Money, Age, Distance, Duration, Count) – Wert + Einheit (oft UCUM)
- **Reference** – Verweis auf eine andere Resource

### Cardinality-Notation

| Cardinality | Bedeutung |
|---|---|
| `0..1` | Optional, höchstens einmal |
| `1..1` | Pflicht, genau einmal |
| `0..*` | Optional, beliebig oft (Liste) |
| `1..*` | Mindestens einmal, beliebig oft |
| `0..0` | Verboten (in Profilen genutzt) |

## Beispiel

Patient.identifier hat Data Type **Identifier** (komplex) und Cardinality **0..\*** in der Base-Resource. Im US-Core-Profile wird das auf **1..\*** verschärft (mindestens ein Identifier ist Pflicht – siehe [[EHR - FHIR - Profiles und Must Support]]).

Patient.active hat Data Type **boolean** und Cardinality **0..1**.

Patient.name hat Data Type **HumanName** und Cardinality **0..\*** (ein Patient kann mehrere Namen haben: Geburtsname, aktueller Name, Aliase).

## Abgrenzung

- **Data Type ≠ Resource:** Data Types sind Bausteine **innerhalb** von Resources – sie haben keine eigenständige REST-API.
- **Primitive ≠ Komplex:** Primitive sind atomar, komplex haben innere Struktur (verschachtelte Felder).
- **Cardinality in Profil ≠ Cardinality in Base:** Profile können Cardinality verschärfen (z. B. 0..1 → 1..1), nie lockern.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen primitiven und komplexen Data Types in FHIR? Nenne 3 Beispiele für jede Klasse.

**Anwendungsfrage:** Welche Cardinality bedeutet „Pflichtfeld, aber nur einmal"? Welche „optional, beliebig oft wiederholbar"?

**Diskussionsfrage:** CodeableConcept ist einer der wichtigsten komplexen Data Types. Warum bietet er sowohl `coding` als auch `text` an?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen Identifier und Reference?
- Warum ist Quantity mit UCUM-Einheit gekoppelt?
- Was bedeutet Cardinality `0..0` und wo wird sie genutzt? (Antwort: in Profilen, um Felder explizit zu verbieten)
- Was ist eine `code`-Type vs. ein `Coding`-Type?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Profiles und Must Support]]
- [[EHR - FHIR - Extensions und 80 20 Regel]]
- [[EHR - FHIR - References]]
- [[MSI - HL7 FHIR - Datentypen]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 14–19 (Data Elements, Data Types primitive/komplex, Identifier-Beispiel, Cardinality)
