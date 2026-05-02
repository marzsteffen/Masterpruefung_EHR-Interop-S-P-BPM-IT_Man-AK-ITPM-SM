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

# MSI - Interoperabilität - Voraussetzungen

> [!info] Kurzdefinition
> Damit eine Transaktion semantisch interoperabel ablaufen kann, braucht es drei Bündel: Inhalt & Syntax (Standards + Profile), Semantik (Informationsmodell + Terminologien + Identifikatoren) und organisatorische Rahmenbedingungen (Recht, Prozesse, Akzeptanz).

## Beschreibung

Folie 23 fasst die Voraussetzungen für semantische Interoperabilität zusammen:

**Inhalt & Syntax**
- Standards → HL7 V2.x, HL7 CDA, FHIR u. a.
- Einigung auf Struktur und Inhalt → Implementierungsleitfäden, Profile.

**Semantik**
- Gemeinsames Informationsmodell → HL7 RIM.
- Terminologien: Code-Systeme, Value Sets, Klassifikationen und Ontologien → LOINC, ICD-10, SNOMED CT, APPC.
- Eindeutige Identifikation von Objekten → OID, MPI, eHVD.

**Organisational Interoperability** (darüber hinaus)
- Gesetzliche Grundlage
- Gemeinsames Verständnis und Definition der Prozesse
- → Akzeptanz!

Wichtig: Die Vorlesung *erwähnt* HL7 RIM, OID, MPI, eHVD, LOINC, ICD-10, SNOMED CT, APPC, jedoch ohne sie an dieser Stelle zu definieren. Im PDF sind sie als Beispiele markiert, nicht als Lerninhalt.

## Bestandteile / Aufbau

Strukturell drei Bündel (siehe oben). Wer eine semantisch interoperable Lösung baut, muss aus jedem Bündel die zum Use Case passenden Elemente kombinieren.

## Beispiel

Aus der Vorlesung (Folie 21): elektronische Terminvergabe für Zuweisungen Hausarzt → MR/Labor in Graz. Inhalt & Syntax über FHIR-Ressourcen oder HL7-Nachrichten, semantisch über Terminologien (z. B. LOINC für Untersuchungsanforderung), organisatorisch über Vereinbarungen zwischen Praxen und Instituten.

## Abgrenzung

- Diese Sicht entspricht funktional dem Drei-Schichten-Modell (Folie 5), gliedert aber explizit nach Voraussetzungs-Buckets statt nach Schichten. Sie ist eher ein Werkzeug für Projektplanung („was brauche ich konkret?").

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Voraussetzungen braucht es für semantische Interoperabilität?

**Anwendungsfrage:** Ein Projekt führt einen elektronischen Laborbefund ein. Welche Elemente aus Inhalt&Syntax / Semantik / Organisational müssen Sie konkret festlegen?

**Diskussionsfrage:** Welcher der drei Bereiche wird in der Praxis am häufigsten unterschätzt – und warum?

**Mögliche Anschlussfragen:**
- Was ist HL7 RIM? (im PDF nur erwähnt, nicht definiert)
- Wofür stehen OID / MPI / eHVD? (im PDF nur erwähnt, nicht definiert)
- Wie verhalten sich Implementierungsleitfäden zu Profilen?

## Verwandt

- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilitätsebenen - Organisatorisch]]
- [[MSI - Standards - Definition]]
- [[MSI - HL7 RIM]] (im PDF nur erwähnt, nicht definiert)
- [[MSI - Identifikator - OID]] (im PDF nur erwähnt, nicht definiert)
- [[MSI - Identifikator - MPI]] (im PDF nur erwähnt, nicht definiert)
- [[MSI - Identifikator - eHVD]] (im PDF nur erwähnt, nicht definiert)

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 23
