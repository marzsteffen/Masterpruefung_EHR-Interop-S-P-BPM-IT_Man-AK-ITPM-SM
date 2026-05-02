---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR und Terminologieserver]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologieserver - Definition

> [!info] Kurzdefinition
> Ein Terminologieserver stellt Terminologien in standardisierter Form für Benutzer zur Verfügung. Er unterstützt semantische Interoperabilität in verteilten Systemen, indem lokal verwaltete Semantik (dezentral) mit zentral vereinbarter und gepflegter Semantik synchronisiert wird – manuell oder automatisiert. Voraussetzung: hohe Strukturierung der Daten und automatische Verarbeitbarkeit.

## Beschreibung

Wörtlich aus Folie 6:

> „Terminologieserver stellt Terminologien in standardisierter Form für Benutzer zur Verfügung
> – Unterstützung der semantischen Interoperabilität in verteilten Systemen
> – Synchronisation von lokaler Semantik (dezentral verwaltet) mit zentral vereinbarter und verwalteter Semantik
>   – Manuell und automatisiert
>
> Über eine Web-Anbindung können Vokabulare veröffentlicht werden
> – Primärsysteme können ihre lokalen Terminologien via Webservices synchronisieren und pflegen
> – Endbenutzer können auf Terminologien über eine Weboberfläche zugreifen
>
> Wesentlich ist, dass die Daten eine hohe Strukturierung aufweisen und sich automatisch verarbeiten lassen."

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| **Funktion** | Standardisierte Bereitstellung von Terminologien |
| **Use Case** | Synchronisation lokaler ↔ zentraler Semantik |
| **Schnittstelle** | Webservices (für Primärsysteme), Weboberfläche (für Endbenutzer) |
| **Voraussetzung** | Hohe Strukturierung, automatische Verarbeitbarkeit |
| **Nutzungsmodi** | Manuell und automatisiert |

## Beispiel

ELGA Termgit (`https://termgit.elga.gv.at/`) ist der österreichische Terminologieserver für ELGA-Codesysteme und -Value-Sets. SNOMED FHIR DevDays (`confluence.ihtsdotools.org`) ist ein international verfügbares Beispiel. CSIRO Ontoserver (`https://ontoserver.csiro.au/`) ist ein Produkt-Terminologieserver auf FHIR-Basis.

## Abgrenzung

- **Terminologieserver ≠ Code System**: Server stellt mehrere Code Systems + Value Sets bereit; ein Code System ist Inhalt davon.
- **Terminologieserver ≠ OID-Register**: Folie 8 zeigt das österreichische OID-Portal als *separates* System neben dem Terminologieserver.
- **Terminologieserver ≠ Standard**: Server ist die Implementierung; Standards (FHIR Terminology, IHE SVCM, …) regeln den Austausch.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Was ist ein Terminologieserver? Welche Aufgabe hat er?

**Anwendungsfrage:** Welcher Terminologieserver steht in Österreich produktiv zur Verfügung? Welche Inhalte enthält er?

**Diskussionsfrage:** Welche semantische-Interoperabilitäts-Voraussetzung wird durch einen Terminologieserver erfüllt – und welche nicht?

**Mögliche Anschlussfragen:**
- Welche Aufgaben hat ein Terminologieserver konkret? → [[MSI - Terminologieserver - Aufgaben]]
- Welche Architektur hat ein Terminologieserver? → [[MSI - Terminologieserver - Architektur]]
- Welche Standards regeln den Austausch? → [[MSI - Terminologieserver - Austauschstandards]]

## Verwandt

- [[MSI - Terminologieserver - Aufgaben]]
- [[MSI - Terminologieserver - Architektur]]
- [[MSI - Terminologieserver - Austauschstandards]]
- [[MSI - Terminologie - Management in Österreich]]
- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[MSI - Interoperabilität - Voraussetzungen]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 6
