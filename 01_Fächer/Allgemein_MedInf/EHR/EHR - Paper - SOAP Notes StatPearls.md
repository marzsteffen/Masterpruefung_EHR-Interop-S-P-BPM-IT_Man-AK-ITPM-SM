---
fach: ehr
typ: vorlesung
status: offen
quelle_pdf: SOAP Notes - StatPearls - NCBI Bookshelf.pdf
datum_vorlesung: 2020-09-03
tags:
  - fach/allgemein/ehr
  - typ/vorlesung
  - status/offen
---

# EHR - Paper - SOAP Notes StatPearls

## Überblick

StatPearls-Bookshelf-Artikel von Podder, Lew & Ghassemzadeh (NCBI/NLM, Last Update 2020-09-03). Vertiefende Beschreibung der SOAP-Note als Dokumentations- und Reasoning-Framework. Ergänzt die Vorlesung um konkrete Substrukturen (OLDCARTS, HEADSS, Review of Systems), die wichtige Abgrenzung Symptoms vs. Signs, das Konzept der Differential Diagnosis innerhalb des Assessment, die SOAPE-Erweiterung sowie eine kritische Diskussion der Schwächen von SOAP im EMR-Zeitalter.

## Lernziele (laut Quelle)

Die Quelle nennt explizit das Ziel, „SOAP als kognitives Framework für Clinical Reasoning" zu vermitteln. Implizit:
- Standardisierte Mnemonics (OLDCARTS, HEADSS, ROS) für strukturierte Subjective-Erfassung kennen
- Symptoms (Subjective) von Signs (Objective) sicher unterscheiden
- Differential Diagnosis als Teil von Assessment dokumentieren können
- Schwächen der SOAP-Struktur im EMR-Kontext kritisch reflektieren
- SOAPE als Erweiterung kennen, die Verlauf integriert

## Behandelte Konzepte

### Substrukturen zu Subjective
- [[EHR - SOAP - OLDCARTS]]
- [[EHR - SOAP - HEADSS]]
- [[EHR - SOAP - Review of Systems]]

### Grundlegende Abgrenzung
- [[EHR - SOAP - Symptoms vs Signs]]

### Substruktur zu Assessment
- [[EHR - SOAP - Differential Diagnosis]]

### Erweiterungen und Kritik
- [[EHR - SOAP - SOAPE Erweiterung]]
- [[EHR - SOAP - Schwächen und Kritik]]

## Roter Faden

Der Artikel beginnt mit dem historischen Kontext: SOAP wurde **vor fast 50 Jahren von Larry Weed** entwickelt. Es fungiert nicht nur als Dokumentations­schema, sondern als **kognitives Framework für Clinical Reasoning** – eine Checkliste, die als Lernhilfe und Information-Retrieval-Index dient.

Die Substrukturen werden methodisch eingeführt:
- **HPI** strukturiert man mit dem Mnemonic **OLDCARTS** (Onset, Location, Duration, Characterization, Alleviating/Aggravating factors, Radiation, Temporal factor, Severity).
- **Social History** strukturiert man mit **HEADSS** (Home/Environment, Education/Employment/Eating, Activities, Drugs, Sexuality, Suicide/Depression).
- Der **Review of Systems (ROS)** ist eine systemorientierte Frageliste, die Symptome aufdeckt, die der Patient nicht spontan nennt.

Eine zentrale Klärung erfolgt zur **Symptoms vs. Signs**-Abgrenzung – der häufigste Fehler in der Praxis. Im Assessment wird die **Differential Diagnosis** als Liste möglicher Diagnosen mit Wahrscheinlichkeitsranking eingeführt.

Im Block „Issues of Concern" wird **APSO** mit Studienevidenz untermauert (besser für Speed, Accuracy und Usability bei chronischen Visiten). Die zentrale Schwäche von SOAP ist die fehlende explizite Zeitdimension – die **SOAPE-Erweiterung** schließt diese Lücke (E = Evaluate plan effectiveness).

Im Abschnitt „Clinical Significance" diskutiert der Artikel kritisch, dass moderne EMRs SOAP-Notes mit großen Datenmengen überfrachten – die Dichte schadet, wenn nicht klinisch relevant.

## Zentrale Aussagen / Take-aways

- SOAP ist mehr als ein Format – es ist ein **Reasoning-Framework**.
- Mnemonics wie **OLDCARTS** und **HEADSS** sind in der ärztlichen Ausbildung internationaler Standard für die strukturierte Anamnese.
- Die Unterscheidung **Symptoms (Subjective) vs. Signs (Objective)** ist die häufigste Fehlerquelle bei SOAP – Beispiel: „stomach pain" (Symptom) vs. „abdominal tenderness to palpation" (Sign).
- **APSO ist studiengestützt überlegen** für Lese-Effizienz bei chronischen Folgevisiten.
- SOAP **dokumentiert keinen Verlauf explizit** – die SOAPE-Erweiterung adressiert das, hat sich aber praktisch nicht durchgesetzt.
- EMR-Dokumentation **kann SOAP unterminieren**, wenn sie unselektiv große Datenmengen einbettet.

## Querverweise zu anderen Vorlesungen

- [[EHR - VL - SOAP Notes]] – Vorlesungs-Quelle, deren Inhalte hier vertieft werden
- [[EHR - VL - Einführung und Definitionen]] – Bezug zum problem-orientierten Record nach Weed
- [[EHR - Datenmodelle - Klassische Record Typen]] – SOAP als 3. Dimension des problem-orientierten Records

## Quelle

- PDF: SOAP Notes - StatPearls - NCBI Bookshelf.pdf
- Autoren: Vivek Podder (Tairunnessa Memorial Medical College and Hospital), Valerie Lew (Riverside Community Hospital), Sassan Ghassemzadeh (UC Riverside)
- Publikation: StatPearls [Internet], Treasure Island (FL): StatPearls Publishing; 2021 Jan-
- Bookshelf ID: NBK482263 · PMID: 29489268
- Last Update: 3. September 2020
- Lizenz: CC BY 4.0
