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

# MSI - HL7 CDA - R-MIM

> [!info] Kurzdefinition
> R-MIM (*Refined Message Information Model*) ist die CDA-spezifische, aus dem RIM abgeleitete Informationsmodell-Sicht. Sie definiert genau die Klassen und Beziehungen, die für ein CDA-Dokument verwendet werden – mit allen Restriktionen und Default-Werten gegenüber dem allgemeinen RIM.

## Beschreibung

Folie 9 zeigt das CDA R-MIM als großes UML-Diagramm. Es enthält Hauptelemente wie:
- **ClinicalDocument** als Wurzelklasse.
- **Author**, **Custodian**, **LegalAuthenticator**, **DataEnterer**, **InformationRecipient**, **AssignedEntity** etc. als Header-Beteiligte.
- **AssociatedEntity**, **AssignedAuthor**, **HealthCareFacility**, **Performer**, **AuthoringDevice** als weitere Akteure.
- **Section**, **Component**, **bodyChoice**, **NonXMLBody** als Body-Strukturen.
- **Observation**, **SubstanceAdministration**, **Supply**, **Procedure**, **Encounter**, **Organizer**, **Act**, **RegionOfInterest**, **ObservationMedia**, **Inference**, **ExternalAct**, **ExternalDocument**, **ExternalObservation**, **ExternalProcedure** als Clinical-Statement-Klassen.

Hochauflösendes Diagramm laut Folie: `https://wiki.hl7.de/images/Cdaab1_cda_rmim.jpg`.

> Hinweis Quelltreue: Die Folie 9 zeigt das Diagramm primär als Übersicht. Die einzelnen Klassen werden im Vorlesungs-PDF nicht detailliert besprochen.

## Bestandteile / Aufbau

R-MIM ist eine *Refinement* des RIM:
- Übernimmt die Backbone-Klassen Entity, Role, Participation, Act vom RIM.
- Definiert spezifische Subklassen und Constraints für medizinische Dokumente.
- Legt fest, welche Beziehungen zulässig sind und welche Default-Werte gelten.
- Bildet die Basis für das CDA XML-Schema.

## Beispiel

Wie das R-MIM auf ein CDA-Dokument abbildet, ist in Folie 10 sichtbar: `legalAuthenticator` (Participation) → `assignedEntity` (Role) → `assignedPerson` + `representedOrganization` (Entities). Diese Konstellation ist im R-MIM klar restriktiv für CDA-Header festgelegt.

## Abgrenzung

- **R-MIM ≠ RIM**: R-MIM ist eine *Refinement*-Sicht des RIM für CDA. RIM ist das allgemeine Informationsmodell, R-MIM die CDA-spezifische Auswahl mit Constraints.
- **R-MIM ≠ XML-Schema**. Aus dem R-MIM wird ein XML-Schema generiert; das Schema ist die technische Validier­ungsform, das R-MIM die abstrakte Modellierung.
- **R-MIM ≠ Implementierungs­leitfaden**. Implementierungs­leitfäden (z. B. ELGA-Allgemeiner Leitfaden) schränken das R-MIM weiter ein („Profilierung").

## Prüfungsrelevanz

**Mittel.** Der Begriff R-MIM wird typischerweise nur in Vertiefungs­fragen abgefragt; das Verständnis seines Verhältnisses zu RIM und zu CDA-Schema ist aber wichtig.

**Typische Definitionsfrage:** Was ist das R-MIM und wie verhält es sich zum RIM?

**Anwendungsfrage:** Wo passt das R-MIM in der Toolchain RIM → R-MIM → XML-Schema → ELGA-Leitfaden?

**Diskussionsfrage:** Warum braucht es ein R-MIM zusätzlich zum RIM? Welche Probleme lösen die Constraints?

**Mögliche Anschlussfragen:**
- Wo wird das R-MIM publiziert?
- Welche Tools (z. B. ART-DECOR) helfen beim Arbeiten mit R-MIM-Refinements?
- Wie hängt das R-MIM mit den ELGA-Templates zusammen? → [[MSI - HL7 CDA - Templates]]

## Verwandt

- [[MSI - HL7 RIM - Reference Information Model]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Templates]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 9 (mit Verweis auf hochauflösendes Diagramm `https://wiki.hl7.de/images/Cdaab1_cda_rmim.jpg`)
