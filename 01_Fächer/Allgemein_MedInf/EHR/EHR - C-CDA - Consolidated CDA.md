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

# EHR - C-CDA - Consolidated CDA

> [!info] Kurzdefinition
> **C-CDA** (Consolidated CDA) ist eine **HL7-Konsolidierung von neun CDA-Dokumenttypen** unter einer einheitlichen Implementation Guide. Wurde in MU Stage 2 als verpflichtender Exchange-Standard für Care Transitions etabliert; das CCD ist einer dieser neun Dokumenttypen.

## Beschreibung

Aus Folie 28:

> „MU-Stage 2: CCD, but not the CCR, was included as part of the standard for clinical document exchange.
> HL7 developed the 'consolidated CDA' (C-CDA).
> C-CDA includes nine document types, one of which is an updated version of the CCD.
> MU-2 requires that healthcare providers use C-CDA document exchange regularly in care transitions and the CCD has been identified as the most appropriate document for this purpose."

Quelle laut Folie: HL7 Implementation Guide für C-CDA, hl7.org/implement/standards/product_brief.cfm?product_id=379.

## Bestandteile / Aufbau

### Die 9 Dokumenttypen von C-CDA

Aus Folie 29 (visuell, basierend auf Quelle Corepoint Health), die typischen C-CDA-Dokumenttypen sind:

1. **CCD** (Continuity of Care Document) – Updated Version, „most appropriate" für Care Transitions
2. **Consultation Note**
3. **Diagnostic Imaging Report**
4. **Discharge Summary**
5. **History and Physical (H&P)**
6. **Operative Note**
7. **Procedure Note**
8. **Progress Note**
9. **Unstructured Document**

(Die exakte Liste der 9 ist im PDF nicht enumeriert; obige Liste ist die übliche C-CDA-Aufzählung; gegebenenfalls Verifikation am HL7-IG.)

### Verhältnis zu CCD und CCR

```
CCR (ASTM, fading)
   ↓ HL7-Implementation
CCD (Continuity of Care Document, CDA-basiert)
   ↓ Konsolidierung mit 8 weiteren CDA-Doc-Typen
C-CDA (Consolidated CDA, mandatory in MU-2)
```

## Beispiel

C-CDA-Use-Case bei Care Transition:
- Patient wird vom Krankenhaus entlassen → das EHR generiert eine **Discharge Summary** (C-CDA-Dokumenttyp) und/oder einen **CCD** (für die Folge-Versorger).
- Spezialist überweist zum Hausarzt → **Consultation Note**
- Operation → **Operative Note**
- Folgevisite → **Progress Note**

C-CDA bietet damit für jeden typischen Care-Transition-Fall einen passenden Dokument-Typ.

## Abgrenzung

- **CCD ist ein Dokumenttyp innerhalb von C-CDA** – nicht zu verwechseln. „CCD" wird oft auch als Sammelbegriff für alle C-CDA-Dokumente verwendet, das ist aber unpräzise.
- C-CDA ≠ FHIR Document Bundle: FHIR hat eigene Document-Resource-Konstrukte; sie können CDA-Inhalte abbilden, sind aber strukturell anders.
- C-CDA-Compliance ist in den USA seit MU Stage 2 verbindlich; international weniger verbreitet.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist C-CDA und wie verhält es sich zu CCD und CCR?

**Anwendungsfrage:** Welcher der 9 C-CDA-Dokumenttypen wird bei welcher Care-Transition-Situation typischerweise eingesetzt?

**Diskussionsfrage:** Konsolidierung mehrerer Dokumenttypen unter einer Spezifikation – welche Vorteile (Interoperabilität, Wiederverwendbarkeit), welche Nachteile (Komplexität, Bloat) entstehen?

**Mögliche Anschlussfragen:**
- Welche der 9 Dokumenttypen sind in einem typischen ELGA-Setup verfügbar? (z. B. Entlassungsbrief ≈ Discharge Summary)
- Wie ist C-CDA technisch umgesetzt – ein gemeinsames Stylesheet, ein gemeinsames Schema?
- Welche Rolle spielt C-CDA in modernen FHIR-/Bundles-Welten?
- Welche Schwächen hat C-CDA in der Praxis? (Anschluss: Stichworte „Section Bloat", inkonsistente Coding)

## Verwandt

- [[EHR - CCD - Continuity of Care Document]]
- [[EHR - CCR - Continuity of Care Record]]
- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - VL - Meaningful Use]]
- [[EHR - MU Stage 2]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folien 28–29 (C-CDA, Document Types, MU-2-Bezug)
