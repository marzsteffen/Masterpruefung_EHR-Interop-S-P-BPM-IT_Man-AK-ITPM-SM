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

# MSI - HL7 - International Patient Summary

> [!info] Kurzdefinition
> International Patient Summary (IPS) ist eine Spezifikation für Patient-Summary-Daten, gemeinsam entwickelt von HL7 und dem European Committee for Standardization (CEN). Sie soll Klinikern den Zugang zu relevanten, akkuraten und aktuellen medizinischen Patienteninformationen über Systemgrenzen hinweg ermöglichen.

## Beschreibung

Wörtlich aus Lehne et al. (2019), Sektion „Interoperability for medical communication":

> „Existing specifications for patient summary data such as the International Patient Summary (IPS) developed by HL7 and the European Committee for Standardization (CEN) can further help clinicians to access relevant, accurate, and up-to-date medical information about their patients."

Im Paper als Lösungsansatz für das Problem genannt, dass EHRs „too often … are disconnected, proprietary solutions buried in systems that do not talk to each other". Außerdem wird IPS implizit referenziert in der Sektion „International cooperation": 2019 erstes grenzüberschreitendes Austausch-Beispiel zwischen EU-Ländern (electronic prescription und a digital patient summary).

> Hinweis Quelltreue: Welche FHIR-Resources, welche Sektionen, welche Versionen IPS umfasst, wird im Paper **nicht** ausgeführt.

## Bestandteile / Aufbau

Aus dem Paper:
- Träger: HL7 + CEN.
- Zweck: Patient-Summary, das relevant, akkurat und aktuell ist.
- Anwendungsfall: grenzüberschreitender Datenaustausch in der EU (Beispiel 2019).

## Beispiel

Aus Paper-Sektion „International cooperation": „2019 has seen the first exchange of common data models between European countries (an electronic prescription and a digital patient summary)." → praktisches IPS-Pilot-Beispiel zwischen EU-Mitgliedstaaten.

## Abgrenzung

- **IPS ≠ ELGA-Patientensicht.** ELGA ist ein nationales System, IPS ist eine internationale Spezifikation. Sie können sich überschneiden, sind aber nicht dasselbe.
- **IPS ≠ Discharge Summary.** Patient Summary ist ein Bridge-Document zwischen Versorgungs-Settings, kein Ersatz für detaillierte Befunde.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist die International Patient Summary, und wer steht dahinter?

**Anwendungsfrage:** Welcher praktische Nutzen ergibt sich aus IPS für einen Patienten, der zwischen EU-Ländern reist und medizinische Hilfe braucht?

**Diskussionsfrage:** Welche Hürden bleiben trotz IPS bestehen? (Antwort des Papers: organisatorische Ebene – Infrastruktur, Recht, Anreize.)

**Mögliche Anschlussfragen:**
- Auf welchen Standards basiert IPS technisch? (FHIR + CDA – im Paper nicht detailliert.)
- Wie verhält sich IPS zur ELGA-Patientensicht? → [[EHR - ELGA - Architektur]]
- Welche Inhaltskategorien sieht IPS vor? (im Paper nicht aufgelistet.)

## Verwandt

- [[MSI - Interoperabilität - Anwendungsbereiche Lehne]]
- [[MSI - HL7 FHIR - Resource]]
- [[MSI - HL7 CDA - Header]]
- [[EHR - MOC]]

## Quelle

- Vorlesung: [[MSI - Paper - Why Digital Medicine Depends on Interoperability]]
- Folien/Seitenangabe: Sektion „Interoperability for medical communication" + „Interoperability for international cooperation", S. 3–4 des Papers
