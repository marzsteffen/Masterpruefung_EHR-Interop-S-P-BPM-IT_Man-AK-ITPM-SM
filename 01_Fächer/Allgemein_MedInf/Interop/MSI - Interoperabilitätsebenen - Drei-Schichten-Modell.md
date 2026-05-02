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

# MSI - Interoperabilitätsebenen - Drei-Schichten-Modell

> [!info] Kurzdefinition
> Interoperabilität wird in drei verschachtelte Ebenen unterteilt: Technische Interoperabilität (innen), Semantische Interoperabilität (mittlere Schicht), Organisatorische Interoperabilität (umschließende Schicht). Jede äußere Ebene setzt die inneren voraus.

## Beschreibung

Die Vorlesung präsentiert (Folie 5) das Modell mit drei ineinander geschachtelten „Tropfen":

- Innen: **Technical Interoperability** – ermöglicht den Austausch von Information aus technischer Sicht und garantiert Datensicherheit/Privacy, Datenintegrität, Zugriff auf relevante Daten zu identifiziertem Patienten.
- Mitte: **Semantic Interoperability** – erlaubt beiden Seiten, die Bedeutung der ausgetauschten Information zu verstehen, über kulturelle und sprachliche Grenzen hinweg.
- Außen: **Organisational Interoperability** – Wille und Fähigkeit zusammenzuarbeiten und Information auszutauschen; abhängig von Gesetzen, Policies und Kooperationsvereinbarungen.

Der Gesamtanspruch übergreifend: „Both ends exchange, understand and act on the data received."

## Bestandteile / Aufbau

| Ebene | Was | Stichworte aus Folie 5 |
|---|---|---|
| Organisational | Rahmen | Legal framework, Cooperative workflows, Policies, Standards and profiles |
| Semantic | Bedeutung | Standards and profiles, Clinical procedures, Terminologies, Medical guidelines |
| Technical | Übertragung | Transport protocols, Standards, Profiles, Services and messages, Health metadata |

Verschachtelung: Eine Schicht kann nur funktionieren, wenn die innenliegenden tragen.

## Beispiel

Eintragung am elektronischen Impfpass (Folie 8) als Übungsbeispiel der Vorlesung:
- Technisch: Welches Transportprotokoll, welches Format?
- Semantisch: Welche Codes für Impfstoff, Dosis, Datum?
- Organisatorisch: Wer darf eintragen, gesetzliche Grundlage, Workflow zwischen Arzt, Apotheke, Patient?

## Abgrenzung

- Im PDF ebenfalls erwähnt: alternative Schichten-Sicht aus Benson/Grieve mit vier Layern (Technology / Data / Human / Institutional). Siehe [[MSI - Interoperabilitätsebenen - Benson Grieve Layer-Modell]].
- Das Drei-Schichten-Modell ist die in der Vorlesung primär verwendete Sicht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Ebenen der Interoperabilität unterscheidet man?

**Anwendungsfrage:** Ordnen Sie konkrete Standards/Konzepte (Transportprotokoll, SNOMED CT, gesetzlicher Rahmen) den drei Ebenen zu.

**Diskussionsfrage:** Welche Ebene ist in der Praxis am schwersten herzustellen, und warum? (Antwort der Vorlesung: organisatorisch – „Akzeptanz" laut Folie 23.)

**Mögliche Anschlussfragen:**
- Wieso sind die drei Ebenen verschachtelt und nicht parallel?
- Welche typischen Standards adressieren welche Ebene?
- Vergleichen Sie das Drei-Schichten-Modell mit der Benson/Grieve-Sicht.

## Verwandt

- [[MSI - Interoperabilitätsebenen - Technisch]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilitätsebenen - Organisatorisch]]
- [[MSI - Interoperabilitätsebenen - Benson Grieve Layer-Modell]]
- [[MSI - Interoperabilität - Voraussetzungen]]

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 5, 8
