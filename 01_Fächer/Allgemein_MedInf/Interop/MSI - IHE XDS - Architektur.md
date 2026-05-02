---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - IHE XDS - Architektur

> [!info] Kurzdefinition
> IHE XDS (*Cross Enterprise Document Sharing*) ist ein IHE-Profil zum institutions­übergreifenden Austausch klinischer Dokumente. Akteure: **Patient Identity Source, Document Source, Document Repository, Document Registry, Document Consumer, On-Demand Document Source**. Standardisierte Transaktionen mit ITI-Nummern (ITI-8/44, ITI-41, ITI-42, ITI-43, ITI-18, ITI-61).

## Beschreibung

Folie 34 zeigt die XDS-Architektur als Grafik:

**Akteure (Aktoren)**:
- **Patient Identity Source** – stellt Patient-Identitäten bereit.
- **Document Source** – sendet Dokumente in das Repository.
- **Document Repository** – speichert die Dokumente persistent.
- **Document Registry** – führt das Inventar/Index, vermittelt Suchanfragen.
- **Document Consumer** – fragt das Registry ab und holt Dokumente vom Repository.
- **On-Demand Document Source** – Variante: erzeugt Dokumente erst bei Anfrage.

**Transaktionen (laut Diagramm-Beschriftungen Folie 34)**:

| Transaktion | Bedeutung |
|---|---|
| `[ITI-8]` Patient Identity Feed | Patient Identity Source → Document Registry |
| `[ITI-44]` Patient Identity Feed HL7v3 | Patient Identity Source → Document Registry (HL7 v3 Variante) |
| `[ITI-41]` Provide & Register Document Set – b | Document Source → Document Repository |
| `[ITI-42]` Register Document Set – b | Document Repository → Document Registry |
| `[ITI-43]` Retrieve Document Set | Document Consumer ← Document Repository |
| `[ITI-18]` Registry Stored Query | Document Consumer ↔ Document Registry |
| `[ITI-61]` Register On-Demand Document Entry | On-Demand Document Source → Document Registry |

> Hinweis Quelltreue: Die Folie zeigt die Architektur primär als Bild. Vertiefte Beschreibungen der Transaktionen sind im PDF nicht ausgeführt.

## Bestandteile / Aufbau

Die XDS-Architektur trennt **Speicherung** (Repository) und **Suche** (Registry). Der Document Source bringt Dokumente ein (über Provide & Register, das automatisch zu Register Document Set führt). Der Consumer fragt zuerst die Registry per Stored Query, holt dann konkret das Dokument vom Repository per Retrieve Document Set.

Das ist ein klassisches Beispiel für **ungerichtete Kommunikation** (siehe [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]) – Sender und Empfänger sind im Sende-Zeitpunkt nicht bekannt.

## Beispiel

ELGA nutzt eine XDS-basierte Architektur. Wenn ein Krankenhaus einen Entlassungsbrief in ELGA „einbringt", läuft das als Provide & Register über ITI-41 in das ELGA-Repository, dort meldet sich das Repository über ITI-42 bei der Registry an. Wenn ein Hausarzt später ELGA fragt, ob es Dokumente zu seinem Patienten gibt, läuft das als Stored Query (ITI-18) gegen die Registry, das eigentliche Dokument holt er per ITI-43.

## Abgrenzung

- **XDS ≠ XDS.b**: Beim Übergang HL7-V2-basierter ITI-15 zu Web-Service-basiertem ITI-41/42 wurde die Suffix-Kennzeichnung „-b" eingeführt. Heute ist „-b" Standard.
- **XDS ≠ XCA** (Cross-Community Access): XCA verbindet *mehrere* Communities/Affinity Domains; XDS arbeitet innerhalb einer Affinity Domain.
- **Document Repository ≠ Document Registry**: Repository hält die *Dokumente* selbst, Registry den *Index/die Metadaten*.
- **On-Demand Document Source ≠ Document Source**: On-Demand erzeugt das Dokument erst bei Anfrage; reguläre Source legt fertige Dokumente ab.

## Prüfungsrelevanz

**Sehr hoch.** ELGA basiert auf XDS, und IHE-Profile sind ein expliziter MOC-Themen­bereich.

**Typische Definitionsfrage:** Welche Akteure gibt es in IHE XDS? Welche Transaktionen verbinden sie?

**Anwendungsfrage:** Skizzieren Sie den Ablauf, wenn ein Krankenhaus einen Entlassungsbrief in ELGA einbringt und ein Hausarzt später danach sucht.

**Diskussionsfrage:** Warum trennt XDS Repository und Registry?

**Mögliche Anschlussfragen:**
- Wie mappt CDA in XDS-Metadaten? → [[MSI - IHE XDS - Dokument-Metadaten]]
- Welche IHE-Profile gibt es noch? (XCA, XDR, XDM, PIX/PDQ – im PDF nur indirekt erwähnt)
- Wie verhält sich XDS zur ungerichteten Kommunikation? → [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]

## Verwandt

- [[MSI - IHE XDS - Dokument-Metadaten]]
- [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]
- [[MSI - HL7 CDA - Definition]]
- [[EHR - ELGA - Architektur]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 34
