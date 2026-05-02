---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - CQL

> [!info] Kurzdefinition
> CQL (Clinical Quality Language) ist eine HL7-Sprache zum Erstellen wiederverwendbarer Ausdrücke (Expressions) für klinische Entscheidungsunterstützung (CDS-Logik) und zur Auswertung von Qualitätsmetriken (Clinical Quality Measures). CQL kann auch als Basis für CDS-Hooks-Trigger und -Inhalte dienen.

## Beschreibung

Aus Seite 8:

- **Specification:** `https://cql.hl7.org/` (Clinical Quality Language)
- Sprache, die **Expressions** erstellen lässt, die **wiederverwendbar** für:
  - CDS-Logik
  - Auswertung von Qualitätsmetriken (Quality Measures)
- Kann auch als **Basis für CDS-Hooks-Trigger und -Inhalte** dienen
- Beispiele für per CQL definierte Measures: `https://ecqi.healthit.gov/ep-ec?qt-tabs_ep=ec-ecqms&global_measure_group=eCQMs`

Weitere Details (Syntax, Funktionen, Integration) wurden im PDF nicht ausgeführt.

## Bestandteile / Aufbau

Im PDF nicht ausgeführt. Erwähnte Konzepte:

| Begriff | Bedeutung laut PDF |
|---|---|
| Expression | Wiederverwendbarer Ausdruck, der CDS-Logik oder Qualitätskriterien kapselt |
| Clinical Quality Measures | Metriken zur Bewertung klinischer Qualität, per CQL definiert |
| CDS-Logik | Entscheidungslogik für klinische Unterstützungssysteme |

## Beispiel

Auf `https://ecqi.healthit.gov/` sind Beispiele für eCQMs (Electronic Clinical Quality Measures) abrufbar, die per CQL definiert wurden.

## Abgrenzung

- **CQL ≠ CDS Hooks**: CQL definiert die Logik (Was soll geprüft werden?); CDS Hooks definiert, wann und wie diese Logik ausgelöst und kommuniziert wird.
- **CQL ≠ FhirPath**: FhirPath navigiert innerhalb einer Ressource; CQL ist eine vollständige Ausdruckssprache mit Variablen, Funktionen, Bibliotheken.
- **CQL ≠ SQL**: CQL ist auf klinische Daten und FHIR-Datenmodelle ausgerichtet, nicht auf relationale Datenbanken.

## Prüfungsrelevanz

**Mittel.**

**Typische Definitionsfrage:** Was ist CQL und wofür wird es verwendet?

**Anwendungsfrage:** Ein Krankenhaus möchte automatisch messen, wie viele Diabetiker einen HbA1c-Wert im Zielbereich haben. Welche Technologie käme dabei zum Einsatz?

**Diskussionsfrage:** Warum ist eine standardisierte Ausdruckssprache wie CQL vorteilhaft gegenüber proprietären Implementierungen?

**Mögliche Anschlussfragen:**
- Wie hängen CQL und CDS Hooks zusammen? (→ CQL als Logik-Basis für Hook-Trigger)
- Was sind Electronic Clinical Quality Measures (eCQMs)?

## Verwandt

- [[MSI - HL7 FHIR - CDS Hooks]]
- [[MSI - HL7 FHIR - FhirPath]]
- [[MSI - HL7 FHIR - Questionnaire und SDC IG]]

## Quelle

- Vorlesung: [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]
- Folien/Seitenangabe: Seite 8
