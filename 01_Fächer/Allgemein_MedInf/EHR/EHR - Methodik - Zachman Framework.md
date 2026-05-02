---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Macro-Level Interoperabilität]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Methodik - Zachman Framework

> [!info] Kurzdefinition
> Analyse-Framework für Entscheidungssituationen und Enterprise Architecture mit den sechs Fragen-Dimensionen **Who, Why, How, What, Where, When**. In der Vorlesung als Werkzeug genutzt, um Martins Entscheidungssituation systematisch zu zerlegen.

## Beschreibung

Das Zachman-Framework ist ein klassisches Enterprise-Architecture-Modell. Die Vorlesung verwendet es nicht als vollständige EA-Methode, sondern als **Strukturhilfe zur Analyse einer Entscheidungssituation**.

| Dimension | Inhalt laut Folie |
|---|---|
| **Who** | Person, Rolle, Organisation, Community, Teilnehmer, Stakeholder |
| **Why** | Purpose, Mission, Auswahl der nächsten Aktion, alternative Wege, Request, Task |
| **How** | Logik, Formel, Algorithmus, Konversion, Prozedur, Wissen |
| **What** | Inputs, Outputs, Daten, Information, Umstände, Bedingung, Status |
| **Where** | Location, Source-/Target-System, physische oder Computer-Records, Application |
| **When** | Exakter Zeitpunkt, vor/nach einem Ereignis, periodisch, Frequenz, während eines Ereignisses |

Quelle laut Folie: sciencedirect.com/topics/computer-science/zachman-framework.

## Beispiel

Anwendung auf Martins Entscheidung „Soll ich einen Präventionsplan machen?":
- **Why:** Herausfinden, ob Newspaper-Guideline auf sein Profil passt
- **How:** Guideline („men over 45, BMI über Norm, Family-History Heart" → Status-Review)
- **Who:** Home-User / Visitor / Patient
- **What:** Alter, Geschlecht, Gewicht, Größe, Familien­anamnese, Health Records, Health Goals
- **Where:** persönliches Gedächtnis, Familie, Patientenportal
- **When:** Newspaper-Kampagne als Trigger

## Abgrenzung

- Zachman ist ein **Klassifikations**-Framework, kein Vorgehensmodell – es sagt nicht, *wie* man eine Architektur entwickelt, sondern *welche Fragen* zu stellen sind.
- Verwandte Frameworks (in der VL nicht erwähnt): TOGAF, ArchiMate. Zachman ist methodisch älter und konzeptueller.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche sechs Dimensionen unterscheidet das Zachman-Framework?

**Anwendungsfrage:** Wie würdest du die Entscheidung „Speichere ich den Blutdruck zentral oder dezentral?" mit Zachman zerlegen?

**Diskussionsfrage:** Ist Zachman für die Analyse von eHealth-Systemen auf Makro-Ebene ausreichend, oder fehlen Dimensionen (z. B. Privacy, Consent, Trust)?

**Mögliche Anschlussfragen:**
- Warum ist Zachman trotz seines Alters (1987) noch relevant?
- Welche Verbindung sieht Metsallik zwischen Zachman-Dimensionen und Daten-Governance-Rollen?
- Welche der 6 Dimensionen ist in eHealth typischerweise am schwächsten dokumentiert?

## Verwandt

- [[EHR - Architektur - ISO 23903 3D]]
- [[EHR - Governance - Data Sharing Rollen]]
- [[EHR - Integrated Care - Macro Meso Micro Level]]

## Quelle

- Vorlesung: [[EHR - VL - Macro-Level Interoperabilität]]
- Folien/Seitenangabe: Folie „Analysis framework for the elements of decision-making (Zachman)"
