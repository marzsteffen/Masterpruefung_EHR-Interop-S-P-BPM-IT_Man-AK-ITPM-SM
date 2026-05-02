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

# EHR - Definition - ISO TR 20514

> [!info] Kurzdefinition
> ISO/TR 20514 definiert ein „Integrated Care EHR" als sichere, computerverarbeitbare Sammlung von Gesundheitsinformationen einer betreuten Person, die für mehrere autorisierte Nutzer verfügbar ist und auf einem standardisierten Informationsmodell basiert.

## Beschreibung

ISO/TR 20514 liefert die in der Vorlesung als Referenzdefinition genutzte Beschreibung eines Integrated Care EHR:

> "A repository of information regarding the health status of a subject of care, in computer processable form, stored and transmitted securely and accessible by multiple authorized users, having a standardized or commonly agreed logical information model that is independent of EHR systems and whose primary purpose is the support of continuing, efficient and quality integrated health care."

Die Definition wird in der Vorlesung in einzelne Bestandteile zerlegt, die jeder für sich prüfungsrelevant sind.

## Bestandteile / Aufbau

Die zerlegten Definitionsbestandteile (laut Folie 24):

- **Repository** – die EHR ist eine Ablage, kein flüchtiger Datenstrom
- **Information** (mehr als „Daten") – semantisch interpretierbar
- **Health status** – Gesundheitszustand, nicht nur Episoden
- **Subject of care** (typischerweise ein einzelner Patient)
- **Computer processable form** – maschinenlesbar, austauschbar
- **Stored and transmitted securely** – Sicherheit ist Bestandteil der Definition
- **Accessible by multiple authorized users** – Mehrnutzersystem
- **Standardized Information Model** (z. B. RIM)
- **Independent of the EHR System itself** – Interoperabilität ist gefordert
- **Primary purpose**: Unterstützung kontinuierlicher, effizienter und qualitativer integrierter Versorgung

## Beispiel

Die Vorlesung leitet aus der Definition direkt „hot topics" ab:

```
- Shared ownership: wer „besitzt" die EHR?
- Vollständigkeit: alle Encounter, ggf. organisationsübergreifend
- Sicherheit
- Multiple users: wer hat Zugriff auf was, wer entscheidet?
- Unabhängigkeit vom System → Interoperabilität
```

## Abgrenzung

- Diese Definition ist EHR-zentriert und betont **Repository** und **standardisiertes Informationsmodell**. Die HIMSS-Definition ([[EHR - Definition - HIMSS]]) betont demgegenüber den **Workflow** und die Generierung von Records aus Encountern.
- „Integrated Care EHR" ≠ EMR: ISO/TR 20514 zielt auf organisationsübergreifend integrierte Versorgung, EMR ([[EHR - Abgrenzung - EMR CPR EPR PHR]]) ist auf eine einzelne Organisation beschränkt.
- Begriff **RIM** wird im PDF erwähnt, aber nicht definiert (siehe [[MSI - HL7 - RIM]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie definiert ISO/TR 20514 ein Integrated Care EHR – nenne mindestens fünf der zentralen Bestandteile.

**Anwendungsfrage:** Welche Anforderungen an ELGA ergeben sich direkt aus dieser Definition (Stichwort „accessible by multiple authorized users", „standardized information model")?

**Diskussionsfrage:** Was bedeutet „independent of the EHR System itself" praktisch – welche Konsequenzen hat das für proprietäre Systeme?

**Mögliche Anschlussfragen:**
- Worin unterscheidet sich diese Definition von der HIMSS-Definition?
- Welche Bestandteile der Definition motivieren den Einsatz von Standards wie HL7 FHIR?
- Wie würde ein System aussehen, das diese Definition nicht erfüllt?
- Was ist der Unterschied zwischen „Information" und „Daten" in dieser Definition?

## Verwandt

- [[EHR - Definition - HIMSS]]
- [[EHR - Abgrenzung - EMR CPR EPR PHR]]
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - ISO 18308 - Anforderungsspezifikation]]
- [[MSI - HL7 - RIM]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 22–25 (Definition + Zerlegung + „hot topics")
