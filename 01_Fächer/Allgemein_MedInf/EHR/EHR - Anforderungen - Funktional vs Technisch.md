---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Einführung und Definitionen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Anforderungen - Funktional vs Technisch

> [!info] Kurzdefinition
> Funktionale Anforderungen beschreiben **welche Funktionen** ein System bereitstellen muss; technische Anforderungen beschreiben **wie** diese mittels Technologie umgesetzt werden. Die Unterscheidung ist Grundlage für strukturierte Anforderungsdokumente.

## Beschreibung

Aus Folie 41:

> "Functional requirements describe which functions / functionalities need to be delivered by a system. Technical requirements describe how these functional requirements will be met using technology."

Die Trennung ist methodisch wichtig, weil sie es erlaubt, **was** ein System leisten muss, unabhängig von einer konkreten Technologieentscheidung zu spezifizieren – z. B. um Vendor-Bindung beim Einkauf zu vermeiden.

## Bestandteile / Aufbau

- **Funktionale Anforderung** (Beispiel laut PDF): „Provides secure, reliable, real-time access to patient health record information."
- **Technische Anforderung** (impliziter Beispielraum): „Verfügbarkeit > 99,9 %, Antwortzeit < x ms, https für Transport."

## Beispiel

Die Vorlesung verweist auf das Dokument `BPHC_EMR_Functional_Specs-Cerner.pdf` (auf Moodle) als Beispiel für ein funktionales Anforderungsdokument, mit dem ein Krankenhaus Anbieter zu Angeboten auffordert.

## Abgrenzung

- Nicht-funktionale Anforderungen (z. B. Performance, Security, Usability) liegen häufig **zwischen** rein funktional und rein technisch und werden in der Vorlesung nicht explizit als eigene Kategorie eingeführt.
- ISO 18308 ([[EHR - ISO 18308 - Anforderungsspezifikation]]) ist ein funktionales Anforderungsdokument auf normativer Ebene – es schreibt das „Was" vor, ohne Technologien zu mandatieren.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen funktionalen und technischen Anforderungen an ein EHR?

**Anwendungsfrage:** Wie würdest du eine Anforderung wie „Audit Trail" als funktionale Anforderung formulieren – und wie technisch konkretisieren?

**Diskussionsfrage:** Warum trennen RFPs (Request for Proposal) explizit zwischen funktionalen und technischen Anforderungen? Was geht verloren, wenn diese vermischt werden?

**Mögliche Anschlussfragen:**
- Wie wird diese Trennung in HIMSS-High-Level-Requirements umgesetzt?
- Welche Rolle spielt diese Trennung beim Einkauf eines EHR-Systems?
- Wo passen ISO-Normen wie 18308 in dieses Schema?

## Verwandt

- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[EHR - ISO 18308 - Anforderungsspezifikation]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folie 41 (Difference functional vs technical), Folie 67 (Beispiel BPHC/Cerner)
