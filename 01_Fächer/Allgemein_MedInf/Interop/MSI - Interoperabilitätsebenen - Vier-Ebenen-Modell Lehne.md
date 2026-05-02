---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - Paper - Why Digital Medicine Depends on Interoperability]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Interoperabilitätsebenen - Vier-Ebenen-Modell Lehne

> [!info] Kurzdefinition
> Interoperabilität nach Lehne et al. (2019): Vier Ebenen statt drei – Technical, Syntactic, Semantic, Organizational. Trennung zwischen Format/Struktur (syntaktisch) und Bedeutung (semantisch) ist explizit.

## Beschreibung

Lehne et al. unterscheiden im Paper bewusst vier Ebenen, weil sie Format/Struktur (Syntax) als eigenständigen Diskussionspunkt sehen, der weder vollständig in „technisch" (Übertragung) noch in „semantisch" (Bedeutung) aufgeht.

**Technical interoperability** – sichert grundlegende Datenaustausch-Fähigkeiten (z. B. Daten von USB-Stick zum Computer bewegen). Erfordert Kommunikationskanäle und Übertragungsprotokolle. Mit heutigen digitalen Netzen relativ einfach erreichbar. Reicht aber nicht: „moving data from A to B is not enough."

**Syntactic interoperability** – spezifiziert Format und Struktur der Daten (z. B. in einem XML-Dokument). Wird unterstützt durch Standardisierungs-Organisationen wie HL7 oder IHE. Beispiele: HL7 FHIR (~140 Healthcare-Concepts, modern web-API-fähig), openEHR (Archetypen über Reference-Model).

**Semantic interoperability** – während Standards wie FHIR und openEHR die Basis-Semantik definieren, ist semantische Interoperabilität der Bereich der medizinischen Terminologien, Nomenklaturen und Ontologien. Sie sichern, dass Bedeutung über Systeme hinweg geteilt werden kann – „digital lingua franca" für medizinische Begriffe. Beispiele: SNOMED CT (>340.000 Konzepte) als allgemein, ergänzt durch domänenspezifische LOINC, IDMP, HGNC, HPO.

**Organizational interoperability** – höchste Schicht: betrifft Organisationen, Gesetze, Policies. Datenaustausch ist kein Selbstzweck, sondern soll die Arbeit der Health Professionals und die Patientengesundheit verbessern. Erfordert gemeinsame Geschäftsprozesse und Workflows zwischen Institutionen, Anreize/Regulierung für interoperablen Datenaustausch.

## Bestandteile / Aufbau

| Ebene | Was wird geregelt? | Typische Bausteine |
|---|---|---|
| Technical | Übertragung A→B | Kommunikationskanäle, Protokolle |
| Syntactic | Format & Struktur | HL7-Standards, FHIR, openEHR, IHE |
| Semantic | Bedeutung | SNOMED CT, LOINC, IDMP, HGNC, HPO |
| Organizational | Workflows, Policies, Recht | Gesetzliche Rahmen, Anreize, gemeinsame Prozesse |

## Beispiel

Aus dem Paper: Patient wechselt zwischen Krankenhäusern – damit der Wechsel reibungslos funktioniert, müssen Daten technisch übertragen, syntaktisch korrekt strukturiert (z. B. FHIR-Bundle), semantisch in Begriffen verstanden (SNOMED CT/LOINC) und organisatorisch erlaubt (Datenschutz-Vereinbarung) sein. In Deutschland scheitert es laut Paper teilweise schon an der organisatorischen Ebene zwischen Abteilungen desselben Hauses.

## Abgrenzung

- **Im Vergleich zum Drei-Schichten-Modell** (Folie 5 der Hauptvorlesung) wird die Schicht zwischen „technisch" (reine Übertragung) und „semantisch" (Bedeutung) als eigenständig „syntactic" benannt. Im Drei-Schichten-Modell ist Format/Struktur in beiden Schichten implizit verteilt.
- **Im Vergleich zu Benson/Grieve** (Technology / Data / Human / Institutional) hat Lehne einen Bedeutungs-Fokus statt eines People-Process-Fokus.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Ebenen unterscheidet Lehne et al. 2019, und worin unterscheidet sich das vom Drei-Schichten-Modell der Vorlesung?

**Anwendungsfrage:** Ein Krankenhaus stellt FHIR-Endpunkte bereit. Welche Ebenen sind damit erfüllt, welche nicht?

**Diskussionsfrage:** Ist die Trennung zwischen syntactic und semantic überhaupt sinnvoll, wenn FHIR „beides" macht? (Argument des Papers: Format-Definition allein erzeugt noch keine inhaltliche Eindeutigkeit – dafür braucht es zusätzliche Terminologien.)

**Mögliche Anschlussfragen:**
- Welche Standards gehören in welche Ebene?
- Warum reicht „technical interoperability" nicht?
- Welcher Schritt ist laut Paper am schwersten – und warum?

## Verwandt

- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilitätsebenen - Benson Grieve Layer-Modell]]
- [[MSI - Interoperabilitätsebenen - Technisch]]
- [[MSI - Interoperabilitätsebenen - Syntaktisch]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilitätsebenen - Organisatorisch]]

## Quelle

- Vorlesung: [[MSI - Paper - Why Digital Medicine Depends on Interoperability]]
- Folien/Seitenangabe: Sektion „Interoperability", S. 1–2 des Papers
