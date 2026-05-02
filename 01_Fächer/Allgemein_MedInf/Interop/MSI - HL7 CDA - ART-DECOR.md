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

# MSI - HL7 CDA - ART-DECOR

> [!info] Kurzdefinition
> ART-DECOR® ist ein webbasiertes Tool zur Modellierung von CDA-Implementierungs­leitfäden, Templates und Value Sets. Verbindet **Template Associations** (Datasets ↔ Templates) und **Terminology Associations** (Concepts ↔ Code Systems / Value Sets). Aus dem Modell werden Schematrons und Dokumentationen automatisch generiert.

## Beschreibung

Folie 40 zeigt die ART-DECOR-Oberfläche am Beispiel ELGA-Templates (eMedikation Rezept):
- Tabs: Project, Datasets, Scenarios, Terminology, Templates, Issues.
- Hierarchischer Template-Baum links: CDA Document Level Template → Befund Bildgebende Diagnostik, ELGA CDA Dokument eMedikation (Rezept/Abgabe/Medikationsliste/Pharmazeutische Empfehlung), Entlassungsbrief (Pflege/Ärztlich), Laborbefund, Pflegesituations­bericht.
- Rechts: Template-Detail mit ID, Status, Name, Beschreibung, Kontext, Label, Klassifikation, Offen/Geschlossen, Assoziation, „Benutzt von / Benutzt", Item-Liste mit Datentypen, Kardinalität, Konformität.

Beispiel-Template aus dem Screenshot:
- ID: `1.2.40.0.34.11.8.1`
- Name: eMedikationRezept
- Beschreibung: Template Spezieller Implementierungsleitfaden ELGA eMedikation Rezept
- Klassifikation: CDA Document Level Template
- Offen/Geschlossen: Offen (auch andere als die definierten Elemente sind erlaubt)
- Items: hl7:templateId (mehrfach – ELGA, IHE PHARM Prescription, IHE PCC Medical Documents, EIS Full Support), hl7:id, hl7:code (mit Beispiel `<code code="57833-6" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC" displayName="Prescription for medication"/>`).

URL: `https://elga.art-decor.org/index.php?prefix=elga-` für ELGA-Inhalte.

Folie 41 zeigt die **ART-DECOR Associations** als Schema:
- **Template Associations**: Templates ↔ Concepts (im Dataset).
- **Terminology Associations**: Concepts ↔ Code + Code System; Choice list (mit Optionen A, B) ↔ Value Set ↔ Code + Code System.

Quelle des Schemas: Dr. K. Heitmann, 2017.

## Bestandteile / Aufbau

| ART-DECOR-Bereich | Inhalt |
|---|---|
| Datasets | Konzept-Modelle (was wird inhaltlich gefordert?) |
| Templates | XML-Strukturen, die Konzepte umsetzen |
| Terminology | Code Systems + Value Sets |
| Scenarios | Use-Case-Bündel |
| Issues | Tracking offener Punkte |

Output:
- ELGA CDA Schematron (für Validierung) – Folie 32.
- HTML-/PDF-Dokumentation des Leitfadens.
- Wiederverwendbare Templates für andere Leitfäden.

## Beispiel

Aus Folie 40: Das eMedikation-Rezept-Template hat eine `hl7:code`-Konformität, die festlegt:
- `@code` = 57833-6 (Fixed)
- `@displayName` = "Prescription for medication" (Fixed)
- `@codeSystem` = 2.16.840.1.113883.6.1 (Fixed = LOINC)

Die Folie liefert direkt das Code-Beispiel:
```xml
<code code="57833-6" displayName="Prescription for medication"
      codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>
```

## Abgrenzung

- **ART-DECOR ≠ XML-Editor**: ART-DECOR ist ein Modellierungs-Tool für Leitfäden, kein XML-Editor für einzelne Dokumente.
- **ART-DECOR ≠ Validator**: Aus ART-DECOR werden Schematron-Regeln *generiert*, die dann der Validator (z. B. ELGA Online-Validator) anwendet.
- **Dataset ≠ Template**: Dataset ist die *konzeptuelle* Spezifikation (was wird gefordert), Template ist die *technische* Umsetzung (wie wird es im XML codiert).

## Prüfungsrelevanz

**Mittel** (Werkzeug-Kontext) bis **Hoch** (Diskussions­fragen über die Toolchain).

**Typische Definitionsfrage:** Was ist ART-DECOR und wozu wird es eingesetzt?

**Anwendungsfrage:** Welche Bestandteile eines CDA-Leitfadens werden in ART-DECOR modelliert?

**Diskussionsfrage:** Warum trennt ART-DECOR Datasets, Templates und Terminology in eigene Bereiche?

**Mögliche Anschlussfragen:**
- Wie verhalten sich Template Associations und Terminology Associations zueinander?
- Welche Outputs erzeugt ART-DECOR? (Schematron, Dokumentation)
- Wo finde ich die ELGA-ART-DECOR-Inhalte?

## Verwandt

- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Management in Österreich]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 40, 41 (Quelle Schema: Dr. K. Heitmann, 2017)
