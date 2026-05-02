---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Einführung in Standards und Interoperabilität]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Daten - Metadaten

> [!info] Kurzdefinition
> „Daten über Daten": beschreiben den Inhalt eines Dokuments/Datensatzes (z. B. Schlagwörter, Autor, Datum, Fachrichtung), um Suchen, Filtern, Gruppieren und Sortieren zu ermöglichen, ohne den ganzen Inhalt herunterladen zu müssen.

## Beschreibung

Folie 17 definiert Metadaten als „Daten über Daten" – Beispiel: Inhaltsangabe in einem Buch.

In einem CDA-Dokument zählen laut Folie:
- **Schlagwörter (serviceEvents)**
- **Autor**
- **Datum**
- **Fachrichtung**

Die Folie nennt explizit den Zweck:
- **Suchen, filtern, gruppieren, sortieren.**
- Umgang mit dem Dokument möglich, ohne den gesamten Inhalt kennen/herunterladen zu müssen → **Dokumentenübersicht.**

Die rhetorische Frage am Ende der Folie lautet: „Ist das schon semantische Interoperabilität?" – Diskussionsanker, in der Vorlesung nicht abschließend beantwortet.

## Bestandteile / Aufbau

CDA-typische Metadaten laut Folie 17:
- Organisation des Autors
- Titel des Dokuments
- Fachrichtung
- APPC-Code (Austrian Privacy Policy Code, in der Folie als Such-Filter-Beispiel im Screenshot)
- Gesundheitsdienstleistung
- Dokumententyp
- Erstellungsdatum

(Alle aus dem ELGA-Suchmaske-Screenshot der Folie.)

## Beispiel

Aus Folie 17 (Screenshot ELGA-Suchmaske): Suche über Erstellungsdatum-Bereich, Fachrichtung, Dokumententyp, APPC-Code – ohne ein einziges Dokument zu öffnen.

## Abgrenzung

- **Metadaten ≠ Inhalt.** Metadaten beschreiben das Dokument; der eigentliche Befundtext ist Content.
- **Metadaten ≠ semantische Interoperabilität.** Die Folie stellt diese Frage offen. Fachlich: Metadaten unterstützen das Auffinden, garantieren aber nicht das maschinelle Verstehen des Inhalts.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind Metadaten und wozu dienen sie?

**Anwendungsfrage:** Welche typischen Metadaten enthält ein CDA-Dokument? Ordnen Sie die Funktionen Suchen/Filtern/Gruppieren/Sortieren konkreten Metadatenfeldern zu.

**Diskussionsfrage:** Sind Metadaten allein semantische Interoperabilität? (Kritische Antwort: nicht ausreichend – Inhalt bleibt evtl. opak.)

**Mögliche Anschlussfragen:**
- Was ist APPC?
- Wie verknüpft IHE XDS Metadaten mit Dokumenten? (im PDF nicht definiert)
- Welche Metadaten sind in FHIR vorgesehen? (Resource.meta – im PDF nicht definiert)

## Verwandt

- [[MSI - Daten - Strukturiert vs Unstrukturiert]]
- [[MSI - Datenaustausch - Formen]]
- [[MSI - HL7 CDA - serviceEvent]] (im PDF in der Einführung nur erwähnt)
- [[EHR - ELGA - Architektur]] (Suchmaske-Screenshot)

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 17
