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

# EHR - Klassifikation - Waegemann 5 Level

> [!info] Kurzdefinition
> Klassifikation elektronischer Gesundheitsakten nach Waegemann (1999) in fünf Reife-Stufen: vom rein automatisierten administrativen Datensatz (Level 1) bis zur lebenslangen, organisationsübergreifenden EHR (Level 5).

## Beschreibung

Modell von Waegemann (1999), Folien 84–85. Beschreibt eine **Reifestufung** elektronischer Akten – jede Stufe baut auf der vorigen auf und ergänzt sie um Tiefe, Reichweite oder Strukturierung.

## Bestandteile / Aufbau

| Level | Bezeichnung | Inhalt laut PDF |
|---|---|---|
| **1** | Automated Record | Lokaler elektronischer Record mit basalen Patienteninformationen für administrative Zwecke |
| **2** | Computerized Medical Record | Lokales Set von Records mit vollständigen medizinischen Informationen, **als gescannte Dokumente** |
| **3** | Electronic Medical Record | Lokal, aber **strukturiert und auf medizinischer Terminologie** basiert |
| **4** | Electronic Patient Record | **Organisationsübergreifend**, vollständiges Set elektronischer medizinischer Records |
| **5** | Electronic Health Record | **Lebenslange** medizinische Dokumentation einer Person mit medizinisch relevanten Einträgen aus „Hilfsberufen" |

## Beispiel

Aus den Definitionen ableitbare Beispiele:
- Krankenhaus mit gescannten Akten ohne Strukturierung → Level 2
- HIS mit strukturierten Diagnose-/Befund-Daten → Level 3
- ELGA-ähnliche Systeme, die Daten mehrerer Versorger zusammenführen → Level 4 oder 5
- Lebenslange Akte inkl. Pflege/Therapeuten/Hebammen → Level 5

## Abgrenzung

- Die Waegemann-Klassifikation ist **deskriptiv/historisch** und stellt eine Reifestufung dar – keine normative Vorgabe wie ISO 18308.
- Verhältnis zu [[EHR - Abgrenzung - EMR CPR EPR PHR]]: Level 3 entspricht ungefähr **EMR**, Level 4 ungefähr **EPR**, Level 5 dem ausgereiften **EHR**.
- 1999 entstanden – einige Aspekte (z. B. Patient-generierte Daten, mobile Apps, FHIR-basierte API-Access) fehlen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie klassifiziert Waegemann elektronische Gesundheits­akten?

**Anwendungsfrage:** In welchem Level befindet sich ein typisches österreichisches Krankenhaus-HIS? Wo steht ELGA?

**Diskussionsfrage:** Ist eine Stufung von „gescannt" zu „strukturiert" zu „organisationsübergreifend" zu „lebenslang" 2024 noch zeitgemäß, oder fehlen wichtige Dimensionen (Patient-zentrierung, KI-/LLM-Verarbeitbarkeit, Patient-generated Data)?

**Mögliche Anschlussfragen:**
- Was unterscheidet Level 2 von Level 3 in der Praxis?
- Welche Rolle spielen Hilfsberufe in Level 5 (warum sind sie dort hervorgehoben)?
- Wie bildet sich diese Klassifikation in die EHR/EMR/PHR-Begriffe ab?
- Welche heutigen Systeme erreichen Level 5 wirklich?

## Verwandt

- [[EHR - Abgrenzung - EMR CPR EPR PHR]]
- [[EHR - Definition - ISO TR 20514]]
- [[EHR - Architektur - Zentral vs Dezentral]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 84–85 (Classification of EHRs (Waegemann 1999) – 5 levels)
