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

# MSI - HL7 CDA - Definition

> [!info] Kurzdefinition
> HL7 Clinical Document Architecture („CDA") – ISO-Standard ISO/HL7 27932:2009. XML-Format für medizinische Befunde, optimiert für EDV-Weiterverarbeitung. Kann maschinenlesbare medizinische Informationen (Diagnosen, Laborwerte) tragen, Anhänge/Bilder einbetten und mit Stylesheet beliebig dargestellt werden. Metadaten sind für das Gesundheitswesen optimiert.

## Beschreibung

Wörtlich aus Folie 3:

> „**HL7 Clinical Document Architecture (‚CDA')**
> – ISO-Standard: XML für medizinische Befunde (ISO/HL7 27932:2009)
> – Für EDV-Weiterverarbeitung optimiert
> – Kann maschinenlesbare medizinische Informationen tragen, z. B. Diagnosen, Laborwerte
> – Anhänge und Bilder können eingebettet werden
> – Kann mithilfe eines Stylesheets ‚beliebig' dargestellt werden
> – Metadaten für Gesundheitswesen optimiert"

CDA ist Teil von HL7 V3 und basiert auf dem RIM (Reference Information Model, ISO/HL7 21731:2006), siehe [[MSI - HL7 RIM - Reference Information Model]]. Der CDA-Standard hat eine eigene Refinement-Sicht des RIM, das R-MIM ([[MSI - HL7 CDA - R-MIM]]).

## Bestandteile / Aufbau

| Eigenschaft | Wert |
|---|---|
| Standard-Familie | HL7 V3 |
| ISO-Normen | ISO/HL7 27932:2009 (CDA) + ISO/HL7 21731:2006 (RIM-Fundament) |
| Format | XML |
| Zweck | Austausch und Weiterverarbeitung medizinischer Befunde |
| Anhänge | Bilder, Multimedia, eingebettete PDFs (NonXMLBody) |
| Anzeige | über XSLT-Stylesheet (z. B. ELGA_Referenzstylesheet) |

## Beispiel

Aus dem ELGA-Kontext: Ein Allgemeiner Laborbefund oder ein Entlassungsbrief Ärztlich liegen als CDA-Dokumente vor – siehe `Entlassungsbrief_BeispielA.xml` im CDA-Materialien-Ordner.

## Abgrenzung

- **CDA ≠ HL7 V3 als Ganzes**: CDA ist eine Spezifikation *innerhalb* von HL7 V3. HL7 V3 umfasst auch Nachrichten und andere Dokument-Typen.
- **CDA ≠ HL7 V2**: V2 ist ein älterer, ASCII-basierter Nachrichten-Standard (siehe Beispiel auf Folie 14 der Einführungs-Vorlesung).
- **CDA ≠ FHIR**: FHIR ist ein parallel entwickelter, modernerer Web-API-Standard. CDA und FHIR können dasselbe codieren, aber syntaktisch komplett unterschiedlich.
- **CDA ≠ PDF**: Ein PDF im NonXMLBody bleibt ein eingebettetes PDF; das macht das umgebende Dokument trotzdem zu CDA-Level-1.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Was ist HL7 CDA? Welcher ISO-Standard? Welcher Familie zugehörig?

**Anwendungsfrage:** Welche Vorteile hat CDA gegenüber HL7 v2 für klinische Dokumente?

**Diskussionsfrage:** Welche Konsequenzen hat es, wenn ein CDA-Dokument nur ein eingebettetes PDF enthält (CDA-Level 1)? Welche Funktion bleibt erhalten, welche nicht?

**Mögliche Anschlussfragen:**
- Wie verhält sich CDA zu RIM und R-MIM?
- Wie wird CDA dargestellt, wenn nur XML vorliegt?
- Welche Eigenschaften muss ein CDA-Dokument haben?
- Wie unterscheidet sich CDA von FHIR konzeptionell?

## Verwandt

- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 RIM - Reference Information Model]]
- [[MSI - HL7 CDA - R-MIM]]
- [[MSI - HL7 CDA - Eigenschaften]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - Datenaustausch - Formen]] (CDA als Dokumenten-Modus)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 3
