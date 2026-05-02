---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - FHIR Grundlagen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - FHIR - Resource Granularität

> [!info] Kurzdefinition
> FHIR hält die Anzahl der Resource-Typen **bewusst begrenzt**. Statt für jeden Begriff eine eigene Resource zu erschaffen, werden breite Resources mit feinen **Attributen und Coding** differenziert. Beispiel: **Observation** deckt sowohl Subjective- als auch Objective-Daten einer SOAP-Note ab.

## Beschreibung

Aus Folie 30:

> „FHIR wants to keep the number of resources limited.
> Some resources cover a broad scope.
> Example: 'Observation' resource – 'S' and 'O' in SOAP …
> Differentiation by attributes and coding."

## Bestandteile / Aufbau

### Designprinzip

Statt einzelne Resources für jede klinische Beobachtung zu definieren (BloodPressure, Weight, Height, Temperature, PainScore, …), nutzt FHIR **eine Resource „Observation"** und differenziert über:
- **`code`** (CodeableConcept, typischerweise LOINC) – was wird beobachtet?
- **`value[x]`** (Quantity, CodeableConcept, string, …) – der Messwert
- **`category`** (CodeableConcept) – vital-signs, laboratory, social-history etc.

### Vorteile

- Weniger Resource-Typen zu lernen/implementieren
- Neue Beobachtungstypen ohne Spezifikations-Änderung möglich
- Einheitliche Such- und Verarbeitungs-Logik

### Konsequenzen

- Coding-Standards (LOINC, SNOMED CT) werden zur tragenden Säule
- Profile und ValueSets werden essenziell, um Use-Case-spezifische Subsets zu definieren

## Beispiel

**SOAP Mapping zu FHIR-Observations:**

| SOAP-Block | FHIR-Resource(s) | Coding |
|---|---|---|
| **Subjective** (z. B. „Patient klagt über Schmerzen") | Observation mit `category=social-history` oder `category=patient-reported`; oder Condition | LOINC, SNOMED |
| **Objective** (z. B. Blutdruck 140/90) | Observation mit `category=vital-signs`, `code=85354-9 (Blood pressure panel)` | LOINC |
| **Assessment** (Diagnose) | Condition | ICD-10/SNOMED |
| **Plan** | CarePlan, MedicationRequest, ServiceRequest | je nach Subkomponente |

### Übungsaufgabe aus dem PDF (Folie 31)

> „How does FHIR code 'weight' in an 'Observation Resource'? Are there other coding systems used?"

**Antwort** (eigene Erschließung): Body Weight wird üblicherweise als **LOINC 29463-7** (Body Weight) kodiert; alternativ **SNOMED CT 27113001** (Body weight). Einheit per UCUM (kg = `[kg]` bzw. `kg`).

## Abgrenzung

- Granularitäts-Entscheidung ≠ Schwäche: FHIR's Observation-Breite ist **bewusst gewählt** und durch Coding kompensiert.
- Manche Use-Cases verlangen spezialisierte Resources (z. B. Imaging mit ImagingStudy, AllergyIntolerance separat) – Granularität ist nicht beliebig erweiterbar nach Belieben.
- Im Gegensatz zu CDA, das pro Section unterschiedliche Templates hat, ist FHIR Resource-zentriert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie geht FHIR mit der Granularität klinischer Beobachtungen um? Welches Designprinzip steckt dahinter?

**Anwendungsfrage:** Wie würdest du eine Blutdruck­messung in FHIR abbilden? Welche Felder, welche Codes, welche Einheit?

**Diskussionsfrage:** Vor- und Nachteile der „Observation deckt alles"-Strategie? Wann ist eine spezialisierte Resource (z. B. AllergyIntolerance) gerechtfertigt, wann reicht Observation?

**Mögliche Anschlussfragen:**
- Wie unterscheidet sich Observation von Condition?
- Wie wird ein Schmerz-Score in FHIR abgebildet? (Antwort: Observation mit LOINC-Code, valueCodeableConcept oder valueQuantity je nach Skala)
- Welche LOINC-Codes sind für Vital Signs Standard? (z. B. 8480-6 Systolic BP, 8462-4 Diastolic BP, 85354-9 Panel)
- Was sind FHIR Observation Categories?

## Verwandt

- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Resource Kategorien]]
- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[MSI - LOINC]]

## Quelle

- Vorlesung: [[EHR - VL - FHIR Grundlagen]]
- Folien/Seitenangabe: Folien 30–31 (Granularity, Observation-Beispiel, Übung Weight)
