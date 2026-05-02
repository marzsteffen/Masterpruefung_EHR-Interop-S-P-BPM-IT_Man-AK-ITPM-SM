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

# EHR - ELGA - Technologie-Architektur

> [!info] Kurzdefinition
> ELGA (Elektronische Gesundheitsakte Österreichs) basiert auf **HL7-v3 CDA-Dokumenten (XML)** mit eigenem **Implementation Guide pro Dokumenttyp**. Architektur: **dezentrale Repositories** + **zentrales System für Zugriffsautorisierung und Document-Lookup über IHE-Profile (XDS)**.

## Beschreibung

Aus Folie 9:

> „Electronic Health Records – Austria – Technology
> - Based on HL7-v3 CDA (XML) documents
> - Implementation Guide for each type of document
> - Decentralized repositories
> - Central system for access authorization and document lookup using IHE profiles (XDS, …)."

## Bestandteile / Aufbau

| Komponente | Rolle |
|---|---|
| **HL7-v3 CDA (XML)** | Container-Format für klinische Dokumente (Entlassungsbriefe, Befunde, e-Medikation, e-Impfpass) |
| **Implementation Guides** | Dokumenttyp-spezifische Profile, die Pflichtfelder, Codes, Strukturen festlegen |
| **Dezentrale Repositories** | Daten werden bei den datenerzeugenden Versorgern gespeichert (Krankenhäuser, Apotheken etc.) |
| **Zentrales System** | Indiziert die dezentralen Repositories, prüft Zugriffsrechte, ermöglicht Document-Lookup |
| **IHE-Profile (XDS u. a.)** | Cross-Enterprise Document Sharing; standardisiert das Document-Lookup zwischen Einrichtungen |

## Beispiel

Zeitlicher Ausbau von ELGA-Inhalten (Folie 8):
- Anfangs: Entlassungsbriefe, Laborbefunde, Radiologie­befunde
- 2017–2018: **e-Medikation** hinzugefügt
- 2021: **e-Impfpass** hinzugefügt
- Offen: COVID-19-Test-Ergebnisse, Reha-Berichte, Befunde nicht-stationärer Versorger

## Abgrenzung

- **Architektur-Typ:** semi-zentralisiert (dezentrale Daten + zentraler Index) – siehe [[EHR - Architektur - Registry vs Repository]] (zentrale Registry, dezentrale Repositories).
- **Datenformat:** CDA, **nicht** FHIR (Stand 2024). Eine schrittweise FHIR-Migration ist im Diskurs, im PDF nicht detailliert.
- **Implementation Guides:** Sind Dokument-Profile, vergleichbar mit FHIR-Profilen, aber CDA-basiert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie ist ELGA technologisch aufgebaut – welche Standards und welche Architektur kommen zum Einsatz?

**Anwendungsfrage:** Wie funktioniert ein Dokument-Abruf in ELGA aus technischer Sicht? (Patient autorisiert → Zentrales System prüft → IHE-XDS-Lookup → dezentrales Repository liefert Dokument)

**Diskussionsfrage:** Warum CDA und nicht FHIR? Welche historischen, technischen und organisatorischen Gründe bestehen für die CDA-Wahl? Wie würde eine FHIR-Migration aussehen?

**Mögliche Anschlussfragen:**
- Welche Dokumenttypen sind in ELGA inzwischen verfügbar?
- Was ist IHE XDS und wie funktioniert es konkret? (siehe [[MSI - IHE XDS]])
- Welche Privacy-Mechanismen schützen die Daten in ELGA? (Stichwort: Berechtigungs-/Widerspruchs-System, Audit Trails)
- Wie verhält sich ELGA zu EHDS (European Health Data Space)?

## Verwandt

- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - Architektur - Registry vs Repository]]
- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - Healthcare Systems - Zentralisierungs-Modelle]]
- [[EHR - EHDS - European Health Data Space]]
- [[MSI - IHE XDS]]
- [[MSI - HL7 CDA]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folien 8–9 (ELGA – Technology, e-Medikation, e-Impfpass)
