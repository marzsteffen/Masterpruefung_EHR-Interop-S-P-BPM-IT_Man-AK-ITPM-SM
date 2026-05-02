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

# MSI - HL7 CDA - Translation

> [!info] Kurzdefinition
> Wenn im vorgegebenen Value Set kein passender Code gefunden wird, kann ein `<code nullFlavor="OTH">` mit `<originalText>` und einem `<translation>` aus einem alternativen Codesystem (LOINC, SNOMED CT oder lokales System) angegeben werden. Auch bei Diagnose-Codierung möglich, wenn das Hauptcodesystem fixiert ist (ICD-10) und ein zusätzliches alternatives System (SNOMED) verwendet werden soll.

## Beschreibung

Folie 50 (Laborparameter Entry II):

> „Mögliche Laboranalysen sind im Value Set ELGA_Laborparameter fixiert
> Wenn dort kein passender Code gefunden wird, kann man eine sogenannte translation verwenden"

Beispiel-Snippet:
```xml
<component typeCode="COMP">
  <observation classCode="OBS" moodCode="EVN">
    <templateId root="1.3.6.1.4.1.19376.1.3.1.6"/>
    <id extension="OBS-1-11"
        root="2.16.840.1.113883.2.16.1.99.3.1"/>
    <code nullFlavor="OTH">                          <!-- Code mit Nullflavor "Other" -->
      <originalText>Eosinophile pro 100 Zellen /KM</originalText>
      <translation code="11152-6" codeSystem="2.16.840.1.113883.6.1"
                   displayName="Eosinophils/100 cells in Bone marrow"
                   codeSystemName="LOINC"/>
                                                     <!-- Code, der nicht im Value Set
                                                          ELGA_Laborparameter enthalten ist
                                                          (LOINC oder lokales System) -->
    </observation>
  </component>
</component>
```

Hier wird `nullFlavor="OTH"` verwendet, weil im pflichtgebundenen Value Set ELGA_Laborparameter kein Code für „Eosinophile pro 100 Zellen /KM" existiert. Stattdessen wird im `<translation>` ein LOINC-Code (`11152-6`) angegeben.

Folie 53 (Übernahme der maschinenlesbaren Diagnose) zeigt das gleiche Mechanismus für Diagnosen:

```xml
<code code="E10" displayName="Primär insulinabhängiger Diabetes mellitus, Typ-2-Diabetes"
      codeSystem="1.2.40.0.34.5.56" codeSystemName="ICD-10 BMG 2014">
  <originalText>
    <reference value="#entldiag-1"/>
  </originalText>
  <translation code="46635009" displayName="Diabetes mellitus type I"
               codeSystem="2.16.840.1.113883.6.96" codeSystemName="SNOMED CT">
    <originalText> <reference value="#entldiag-1"/> </originalText>
  </translation>
</code>
```

Hier ist das ICD-10-Codesystem laut Leitfaden fixiert; zusätzlich wird via `<translation>` ein SNOMED-CT-Code angegeben (alternatives Codesystem oder lokales System).

> Hinweis Diskrepanz im Folien-Beispiel: Folie 53 zeigt einen ICD-10-Code für „Typ-2-Diabetes" (E10) mit Translation auf SNOMED-Code „Diabetes mellitus type I" (46635009). Die Übersetzung passt im Folien-Snippet semantisch nicht. Vorlesungs­note bei Prüfungsvorbereitung kritisch lesen.

Wichtig laut Folie 53: **Alle Informationen in lokales System übernehmen!**
- Diagnosesicherheit: Gesichert oder nur Verdacht?
- Seitigkeit: rechts oder links?
- Status: noch aktiv oder schon abgeschlossen?

## Bestandteile / Aufbau

Zwei Translation-Patterns:

**Pattern A** (Hauptcode aus erlaubtem System fehlt):
- `<code nullFlavor="OTH">`
- `<originalText>` mit Klartext
- `<translation>` mit Code aus alternativem System

**Pattern B** (Hauptcode aus erlaubtem System vorhanden, Mehrfach-Codierung erwünscht):
- `<code code="..." codeSystem="..." />` (Hauptcode)
- `<translation code="..." codeSystem="..." />` (Zusatz-Code)

## Beispiel

Pattern A (Folie 50): „Eosinophile pro 100 Zellen /KM" → nullFlavor OTH + LOINC-Translation `11152-6`.

Pattern B (Folie 53): ICD-10 `E10` als Hauptcode + SNOMED `46635009` als Translation.

## Abgrenzung

- **Translation ≠ neuer Code im Hauptsystem**: Translation erweitert nicht das Pflichtvalueset; sie liefert nur einen alternativen Eintrag.
- **`<originalText>` ≠ `<translation>`**: originalText ist Klartext, translation ist eine codierte Übersetzung in ein anderes Codesystem.
- **nullFlavor OTH ≠ Translation allein**: OTH zeigt an, dass kein Code aus dem vorgesehenen Value Set passt; ohne `<translation>` wäre die Information nicht maschinell auswertbar.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Was ist eine Translation in CDA, und wann wird sie eingesetzt?

**Anwendungsfrage:** Wie codieren Sie einen Lab-Parameter, der nicht im Value Set ELGA_Laborparameter enthalten ist?

**Diskussionsfrage:** Welche Vor-/Nachteile hat das Translation-Pattern gegenüber dem Erweitern des Value Sets?

**Mögliche Anschlussfragen:**
- Welches nullFlavor wird in Pattern A verwendet?
- Welche Informationen muss das lokale System bei der Übernahme einer maschinenlesbaren Diagnose zusätzlich erfassen? (Folie 53: Diagnosesicherheit, Seitigkeit, Status)
- Wie passt Translation zu Cimino's „Recognize Redundancy"?

## Verwandt

- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - nullFlavor]]
- [[MSI - HL7 CDA - Laborparameter Entry]]
- [[MSI - HL7 CDA - Problem-Bedenken Entry]]
- [[MSI - Terminologie - Mapping]]
- [[MSI - Terminologie - Cimino Desiderata]] (Recognize Redundancy)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 50, 53
