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

# MSI - Interoperabilitätsebenen - Technisch

> [!info] Kurzdefinition
> Technische Interoperabilität ermöglicht den Austausch von Information aus technischer Sicht und garantiert Datensicherheit/Privacy, Datenintegrität sowie Zugriff auf die relevanten Daten zu einem identifizierten Patienten.

## Beschreibung

Wörtlich aus Folie 5:

> „Technical Interoperability enables the exchange of information from a technical standpoint and guarantees:
> - data security and privacy
> - data integrity
> - access to relevant data associated with an identified patient"

Diese Schicht ist die innerste der drei Ebenen und Voraussetzung für alle weiter außen liegenden. Sie deckt Aspekte ab wie Transportprotokolle, technische Standards, Profile, Services und Messages, Health-Metadaten.

## Bestandteile / Aufbau

Aus Folie 5 dem inneren Tropfen zugeordnet:
- Transport protocols
- Standards
- Profiles
- Services and messages
- Health metadata

In der Layer-Sicht von Benson/Grieve (Folie 6) entspricht diese Ebene dem **Technology layer**: Datenaustausch von A nach B, Interchange formats, APIs, HL7 v2 / v3 / CDA / FHIR.

## Beispiel

Aus der Vorlesung: HL7 v2 als Nachrichtenformat (Folie 19, EDIFACT- und HL7-Snippet) – syntaktisch korrekte Übermittlung einer Aufnahme- oder Bestellmeldung.

## Abgrenzung

- Datensicherheit/Privacy ist Teil der technischen Ebene laut Folie 5 – obwohl im Vault thematisch mit ASP verbunden, hier in dieser Definition explizit als technische Garantie geführt.
- Technisch ≠ semantisch: ein technisch korrekt übertragenes PDF erfüllt diese Ebene; semantische Interoperabilität ist es trotzdem nicht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was garantiert technische Interoperabilität?

**Anwendungsfrage:** Welche Standards/Bausteine adressieren primär die technische Ebene? (Transportprotokolle, Interchange-Formate wie HL7 v2/v3/FHIR.)

**Diskussionsfrage:** Reicht technische Interoperabilität, um klinischen Mehrwert zu erzeugen? Warum (nicht)?

**Mögliche Anschlussfragen:**
- Wo in den drei Ebenen liegt Datenintegrität?
- Welche Rolle spielen APIs?
- Wie verhält sich „access to relevant data associated with an identified patient" zur EHR/ELGA-Architektur? → [[EHR - MOC]]

## Verwandt

- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilitätsebenen - Benson Grieve Layer-Modell]]
- [[MSI - Datenaustausch - Formen]]
- [[ASP - MOC]] (Datensicherheit & Privacy als Querbezug)

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 5, 6
