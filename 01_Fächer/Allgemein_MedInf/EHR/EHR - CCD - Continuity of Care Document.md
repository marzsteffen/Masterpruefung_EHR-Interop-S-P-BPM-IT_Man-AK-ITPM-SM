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

# EHR - CCD - Continuity of Care Document

> [!info] Kurzdefinition
> **CCD** ist die **HL7-CDA-Implementation des CCR** (Continuity of Care Record). CCD nutzt CDA-XML-Strukturen, basiert auf dem HL7 RIM und hat sich gegenüber der ASTM-XML-Variante des CCR durchgesetzt. Wurde in MU Stage 1 als bevorzugter Exchange-Standard etabliert.

## Beschreibung

Aus den Folien:

> „CCD: HL7-CDA's CCR implementation. CDA is based on RIM – Reference Information Model. Each XML-element in a CDA document must correspond to a RIM class or class attribute."

> „Most Electronic Health Record vendors have adopted the HL7-CCD rather than the ASTM-CCR since it is a newer format."

## Bestandteile / Aufbau

### Beziehung CCR → CCD

| Aspekt | CCR (ASTM E2369-12) | CCD (HL7-CDA) |
|---|---|---|
| Format | ASTM XML | HL7 CDA XML |
| Datenmodell | ASTM-eigen | basiert auf HL7 RIM |
| Sektionen | 6 Sektionen (mandated core) | dieselben 6 Sektionen, aber CDA-strukturiert |
| Verbreitung | abnehmend (fading out) | dominant; in MU Stage 1 als Exchange-Standard |

### Visualisierung

CCDs sind XML-basiert und können per **XSLT-Stylesheets** transformiert werden in:
- HTML (Web-Sicht)
- PDF (papierähnliche Ansicht)
- Word-Dokumente
- weitere Formate

## Beispiel

In **MU Stage 1** verlangte CMS:

> „EHRs must be able to generate a CCD (or equivalent CCR) that has the sections of allergies, medications, problems, and laboratory results, in addition to patient header information."

Das machte CCD zum De-facto-Standard für Care Transitions in den USA ab 2011.

## Abgrenzung

- **CCR ist Inhalts-Spezifikation, CCD ist Format-Implementierung** – CCD hat denselben Inhalt wie CCR, aber im CDA-Format.
- **CCD ↔ C-CDA:** C-CDA (Consolidated CDA) ist eine Konsolidierung mehrerer CDA-Dokumente, von denen CCD eines ist – siehe [[EHR - C-CDA - Consolidated CDA]].
- **CCD ↔ FHIR:** FHIR ist eine moderne API-First-Alternative; CCD ist Dokument-zentriert. Beide existieren parallel.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein CCD und wie verhält es sich zum CCR?

**Anwendungsfrage:** Welche Vorteile hat CCD gegenüber der ASTM-XML-Variante? Warum hat sich CCD durchgesetzt?

**Diskussionsfrage:** CDA ist Dokument-zentriert, FHIR ressourcen-/API-zentriert. Welche Use-Cases bevorzugen welches Modell?

**Mögliche Anschlussfragen:**
- Was ist HL7 RIM und welche Rolle spielt es im CDA?
- Wie funktioniert XSLT-basierte Visualisierung von CCDs?
- Wie hat sich CCD in C-CDA weiterentwickelt?
- Welche Rolle spielen CCDs im ELGA-Kontext? (Antwort: ELGA basiert ebenfalls auf HL7-CDA, mit eigenen Implementation Guides)

## Verwandt

- [[EHR - CCR - Continuity of Care Record]]
- [[EHR - C-CDA - Consolidated CDA]]
- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - VL - Meaningful Use]]
- [[EHR - MU Stage 1]]
- [[EHR - ELGA - Technologie-Architektur]]
- [[MSI - HL7 CDA]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folien 23–27 (CCR Implementations, CCD HL7-CDA, Visualization, MU-Bezug)
