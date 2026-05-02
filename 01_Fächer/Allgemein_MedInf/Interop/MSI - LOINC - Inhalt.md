---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Terminologien Anwendung]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - LOINC - Inhalt

> [!info] Kurzdefinition
> LOINC deckt mehrere Inhalts-Bereiche ab: Labor (klinische Chemie, Hämatologie, Serologie, Mikrobiologie etc.), Blutbank, Antibiotika-Empfindlichkeit, Molekulargenetik, Klinik (Vitalzeichen, EKG, Bildgebung, Beatmung etc.), Panels, sowie Dokumente und Abschnitte.

## Beschreibung

Folie 22 listet die Inhalts-Bereiche von LOINC:

**Laborteil**
- Klinische Chemie
- Hämatologie
- Serologie
- Mikrobiologie
- Parasitologie
- Virologie
- Toxikologie

**Blutbank**

**Antibiotika-Empfindlichkeit**

**Molekulargenetik**

**Klinischer Teil, z. B.**
- Vitalzeichen
- Hämodynamische Bestimmungen
- Flüssigkeitsbilanzierung
- EKG
- Ultraschall in der Geburtshilfe
- Echokardiographie
- Bildgebung in der Urologie
- Endoskopische Untersuchungen in der Gastroenterologie
- Beatmung

**Panels** (Bündel von Tests)

**Dokumente, Abschnitte** (z. B. „Physician Discharge Summary" als Dokumentenklasse, Folie 25)

## Bestandteile / Aufbau

LOINC ist also nicht nur „Lab" – die Reichweite erstreckt sich auf klinische Beobachtungen, Bildgebung, Funktionsdiagnostik bis hin zu Dokumententypen. Daher heißt LOINC „Logical Observation Identifiers Names and Codes" – Beobachtung im weitesten Sinne.

## Beispiel

- Lab: `26464-8` „Leukozyten" (Folie 25, ELGA-Laborbefund).
- Klinik: Vitalzeichen-Codes (z. B. Heart Rate aus VL 01, `8867-4`).
- Dokument: `11490-0` „Physician Discharge summary" (Folie 25, ELGA-Section-Codierung).
- Section in einem CDA: `42349-1` „Reason for Referral" (Folie 25).

## Abgrenzung

- **Lab-Codes ≠ Order-Codes.** LOINC codiert das Konzept (was gemessen wird); Order-Codes können hauseigene Verschreibungs-Codes sein.
- **Document-Class-Codes (LOINC) ≠ ICD-10-Codes.** LOINC-Document-Classes sind für Dokument­typisierung gemacht, ICD-10 für Diagnosen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Inhalts-Bereiche umfasst LOINC?

**Anwendungsfrage:** Geben Sie für eine ELGA-Section drei mögliche LOINC-Codes (z. B. Aufnahmegrund, Anamnese, Discharge Summary).

**Diskussionsfrage:** Warum codiert LOINC auch Dokumententypen? Welche Vorteile bringt das gegenüber proprietären Document-Type-Codes?

**Mögliche Anschlussfragen:**
- Welche Bereiche von LOINC werden in ELGA verwendet? (Lab, Document Classes, Sections)
- Wie unterscheiden sich Panels und Einzel-Codes?
- Welche Versionierung hat LOINC? (im PDF nicht detailliert)

## Verwandt

- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Sechs-Achsen-Struktur]]
- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - HL7 CDA - Sektion]] (Querverweis Vorlesung 04 – noch nicht definiert)

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 22, 25
