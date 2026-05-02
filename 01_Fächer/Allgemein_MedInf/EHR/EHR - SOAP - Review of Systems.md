---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - Paper - SOAP Notes StatPearls]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - SOAP - Review of Systems

> [!info] Kurzdefinition
> **Review of Systems (ROS)** ist eine systemorientierte Frageliste innerhalb des Subjective-Blocks einer SOAP-Note. Sie deckt Symptome auf, die der Patient nicht spontan nennt – durch systematisches Abfragen nach Organsystemen.

## Beschreibung

Aus StatPearls:

> „This is a system based list of questions that help uncover symptoms not otherwise mentioned by the patient."

Beispiele aus dem Artikel:
- **General:** Weight loss, decreased appetite
- **Gastrointestinal:** Abdominal pain, hematochezia
- **Musculoskeletal:** Toe pain, decreased right shoulder range of motion

## Bestandteile / Aufbau

Typische Organ-/System-Kategorien (StatPearls listet nur Beispiele, nicht erschöpfend):

| System | Beispielsymptome |
|---|---|
| General/Konstitutionell | Gewichtsverlust, Appetit, Fieber, Müdigkeit |
| Haut | Ausschlag, Juckreiz, Veränderungen |
| HEENT (Head, Eyes, Ears, Nose, Throat) | Kopfschmerz, Sehstörung, Hörminderung, Halsschmerz |
| Kardiovaskulär | Brustschmerz, Palpitationen, Belastungsdyspnoe |
| Pulmonal | Husten, Auswurf, Dyspnoe |
| Gastrointestinal | Bauchschmerz, Übelkeit, Stuhl, Hämatochezie |
| Urogenital | Dysurie, Hämaturie, Frequency |
| Muskuloskeletal | Gelenkschmerzen, Bewegungseinschränkung |
| Neurologisch | Schwäche, Parästhesien, Schwindel |
| Psychiatrisch | Depression, Angst, Schlafstörung |
| Endokrin | Polyurie, Hitze-/Kälteintoleranz |
| Hämatologisch | Blutungsneigung, Lymphknotenschwellung |

## Beispiel

ROS bei einem Patienten mit Bauchschmerzen:
- **General:** Kein Gewichtsverlust, kein Fieber
- **Gastrointestinal:** Bauchschmerz (Chief Complaint), Übelkeit, kein Erbrechen, regelmäßiger Stuhlgang, keine Hämatochezie
- **Urogenital:** Keine Dysurie, normale Miktion
- **Muskuloskeletal:** Keine Auffälligkeit
- (übrige Systeme: unauffällig)

## Abgrenzung

- ROS ≠ HPI: HPI fokussiert auf das Chief Complaint (mit OLDCARTS), ROS scannt **alle** Systeme breit.
- ROS ≠ Physical Examination: ROS sammelt **patientenberichtete Symptome** (gehört zu Subjective). Die Untersuchung der Systeme gehört in **Objective** als Physical Exam.
- ROS ist häufig der zeitintensivste Teil – wird im EMR oft mit Checkboxen/strukturierten Templates erfasst.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Review of Systems, und wozu dient er?

**Anwendungsfrage:** Bei welchem Patiententyp ist ROS besonders wertvoll? (Antwort: bei diffusen Beschwerden, multimorbiden Patienten oder Erstvorstellung; weniger zentral bei eindeutiger akuter Pathologie)

**Diskussionsfrage:** ROS in EMR-Systemen wird oft als Checkbox-Liste implementiert – mit dem Risiko mechanischen Abhakens. Welche Trade-offs zwischen Vollständigkeit, Effizienz und klinischer Tiefe entstehen?

**Mögliche Anschlussfragen:**
- Wie unterscheidet sich ROS von der Physical Examination?
- Welche Rolle spielt ROS in einer EMR-basierten Screening-Anwendung?
- Welche Mindest-Anzahl an Systemen wird für unterschiedliche Visit-Levels (z. B. CMS Evaluation/Management Coding) verlangt? (im PDF nicht definiert)
- Was ist „pertinent ROS"?

## Verwandt

- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - OLDCARTS]]
- [[EHR - SOAP - HEADSS]]
- [[EHR - SOAP - Objective]]

## Quelle

- Vorlesung: [[EHR - Paper - SOAP Notes StatPearls]]
- Folien/Seitenangabe: Sektion „Review of Systems (ROS)"
