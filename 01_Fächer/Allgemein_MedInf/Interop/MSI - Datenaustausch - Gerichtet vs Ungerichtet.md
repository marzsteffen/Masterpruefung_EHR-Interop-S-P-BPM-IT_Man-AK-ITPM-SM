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

# MSI - Datenaustausch - Gerichtet vs Ungerichtet

> [!info] Kurzdefinition
> Unterscheidung des Datenaustauschs danach, ob Sender und Empfänger zum Zeitpunkt des Sendens bekannt sind (gerichtet) oder ob Daten in einem geteilten Repository hinterlegt und abgefragt werden (ungerichtet).

## Beschreibung

Auf Folie 18 stellt die Vorlesung den Begriff **„Gerichtete vs. ungerichtete Kommunikation"** ein und stellt die diskursive Frage:
> „Wie relevant sind Standards bei (un)gerichteter Kommunikation?"

Die Folie liefert die Definitionen nicht im Volltext aus, sondern arbeitet sie in der Diskussion heraus. Was die Folie zeigt, ist eine IHE-typische Architektur-Skizze (Patient Identity Source, Document Source, Document Repository, Document Registry, Document Consumer mit Transaktionen wie „Provide and Register Document Set-b", „Register Document Set-b", „Retrieve Document Set", „Registry Stored Query", „Patient Identity Feed") – als Beispiel für einen ungerichteten Modus.

## Bestandteile / Aufbau

Implizit aus der Folie:
- **Gerichtete Kommunikation**: Sender adressiert konkreten Empfänger. Beispiel: HL7-v2-Nachricht von KIS an Labor (Folie 19 mit Beispielnachricht).
- **Ungerichtete Kommunikation**: Sender legt Daten in ein gemeinsames Repository, Empfänger holen sie selbst ab. Beispiel: ELGA / IHE XDS – Dokumente werden registriert und können von berechtigten Konsumenten gefunden werden.

> Hinweis Quelltreue: Die exakten Definitionen werden im PDF nicht ausgeschrieben. Die obige Charakterisierung folgt der Folie 18 (Architekturbild + Frage), kombiniert mit dem späteren CDA/IHE-Kontext der LV.

## Beispiel

- **Gerichtet**: HL7-v2-ADT-Nachricht von Aufnahme an Abrechnung (Folie 19).
- **Ungerichtet**: ELGA-Befund wird vom Krankenhaus in Repository abgelegt; ein Hausarzt fragt später per Document Registry nach.

## Abgrenzung

- Gerichtet ≠ synchron: gerichtete Kommunikation kann auch asynchron sein (Mail an konkreten Empfänger).
- Ungerichtet ≠ Broadcast: Es ist eher ein Pull-Modus, kein aktives Push an viele.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich gerichtete und ungerichtete Kommunikation im Gesundheitswesen?

**Anwendungsfrage:** Ordnen Sie zu: Laborauftrag KIS→Labor, ELGA-Entlassungsbrief, Hausarzt holt ELGA-Befund ab, Tumor-Board-Mitteilung.

**Diskussionsfrage:** Welche Standards sind für welchen Modus prädestiniert? (Gerichtet: HL7 v2 / FHIR Messaging. Ungerichtet: IHE XDS, ELGA, FHIR Document/Repository-Pattern.)

**Mögliche Anschlussfragen:**
- Was zeigt die IHE-XDS-Skizze auf Folie 18? → IHE XDS – im PDF nur als Bild erwähnt, nicht definiert.
- Welche Konsequenz hat ungerichtete Kommunikation für Berechtigungen und Privacy? → [[ASP - MOC]]
- Wo passt FHIR-Subscriptions hin? (im PDF nicht behandelt)

## Verwandt

- [[MSI - Datenaustausch - Formen]]
- [[MSI - IHE XDS - Architektur]] (im PDF nur als Bild erwähnt, nicht definiert)
- [[EHR - ELGA - Architektur]]
- [[ASP - MOC]]

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 18
