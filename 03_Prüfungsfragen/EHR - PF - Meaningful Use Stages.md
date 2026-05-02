---
fach: ehr
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/ehr
---

# EHR - PF - Meaningful Use Stages

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Detail-Kartensatz zu den drei Phasen des Meaningful Use Programms. Stage 1 (ab 2011) fokussiert auf grundlegende EHR-Nutzung, Stage 2 (2014–2016) auf Datenaustausch, Stage 3 (optional 2017, verpflichtend 2018) auf Interoperabilität und Outcomes. Dazu kommen MACRA als Folgeprogramm und CQM als zentrales Mess-Instrument. Überblickskarten zum Gesamtprogramm sind in [[EHR - PF - Internationale Vergleichssysteme]] – hier werden Stage-Details, Strukturunterschiede und Designentscheidungen des Programms vertieft.
**Achtung Honeypot:** Die konkreten 8 Core-Requirements von MU Stage 3 sind im VL-PDF nicht aufgelistet – keine Karten dazu.

## Verlinkte Konzepte

- [[EHR - MU Stage 1]]
- [[EHR - MU Stage 2]]
- [[EHR - MU Stage 3]]
- [[EHR - Meaningful Use - Definition und Ziele]]
- [[EHR - Meaningful Use - 3 Hauptkomponenten]]
- [[EHR - Medicare und Medicaid Incentives]]
- [[EHR - MACRA und Value Based Care]]
- [[EHR - Clinical Quality Measures CQM]]
- [[EHR - MU Auswirkungen und Bilanz]]

---

## Karten

### Definition

Welche Anforderungsstruktur stellt Meaningful Use Stage 1 an Eligible Professionals und an Hospitals?
?
**Eligible Professionals (EPs):** (1) **15 Core Objectives** – alle verpflichtend; (2) **5 von 10 Menu-Objectives** – Auswahl; (3) **6 CQMs** insgesamt: 3 aus Core/Alternate Core + 3 aus einem Set von 38. **Hospitals:** (1) **14 Core Objectives** – alle verpflichtend; (2) **5 von 10 Menu-Objectives** – Auswahl; (3) **15 CQMs**. Zusätzliche Grundregel: **80 % der Patienten** müssen im zertifizierten EHR erfasst sein. Anreize: bis zu 44.000 US$ (Medicare) bzw. 63.750 US$ (Medicaid) pro EP bei vollständiger Erfüllung.

Nenne mindestens sechs Core-Objectives von MU Stage 1 und zwei Menu-Objectives.
?
**Core-Objectives (aus der Vorlesung):** (1) **CPOE** (Computerized Provider Order Entry) für Medikamenten-Orders; (2) **e-Prescribing**; (3) **Drug-Drug- und Drug-Allergy-Interaction Checks**; (4) Patientendemografien aufnehmen; (5) Vital Signs aufnehmen (Größe, Gewicht, Blutdruck); (6) Smoking Status aufnehmen; (7) Klinische Zusammenfassung nach Encounter an Patienten; (8) Privacy-/Security-Risk-Analyse; (9) Capability for Health Information Exchange. **Menu-Objectives (Auswahl aus der VL):** Drug Formulary Checks · Lab-Ergebnisse im EHR · Patienten-spezifische Bildungsressourcen · **Reconciliation** (Abgleich von Medikamenten-/Problem-Listen bei Übergaben) · Patient Electronic Access.

Was ist der Hauptfokus von MU Stage 2, und wie unterscheidet sie sich strukturell von Stage 1?
?
Stage 2 (2014–2016) betont laut Vorlesung: „More emphasis on the **use** of EHRs and **exchange**." Der Hauptunterschied: Stage 1 bewies grundlegende EHR-Nutzung; Stage 2 verlangt nachweisbaren **Datenaustausch** zwischen Stellen (Care Transitions, strukturierter Lab-Import, Vital-Signs-Erfassung strukturiert). Strukturell: erweitertes Core-Set + erweiterte Menu-Optionen. Neue Beispiele aus der VL: **Vital Signs strukturiert** (Pflicht Core), **Laboratory Results strukturiert** (Core), **Progress Notes elektronisch** (Menu). Schwelle: Stage-2-Anforderungen sind höher als Stage 1; Provider müssen Stage 1 absolviert haben, bevor sie Stage 2 anerkannt bekommen.

Was sind die wesentlichen Änderungen in MU Stage 3 – und wie verbindet es sich mit MACRA?
?
MU Stage 3 (optional 2017, **verpflichtend 2018**): (1) **Keine Menu-Optionen mehr** – alle 8 Core-Requirements für EPs sind verpflichtend; (2) Hospitals haben stage-abhängige eigene Anforderungs-Sets; (3) Stärkerer Fokus auf **Interoperabilität** und **Health Information Exchange**; (4) Verknüpfung mit **MACRA** (Medicare Access and CHIP Reauthorization Act, 2015): MACRA konsolidiert MU und andere Anreizprogramme (PQRS, Value-Based Modifier) und steuert den Übergang von **Pay for Service** zu **Pay for Performance** – Provider werden für Outcomes und Qualität, nicht für Einzelleistungen vergütet. Die konkreten 8 Core-Requirements sind im Vorlesungs-PDF nicht aufgelistet.

---

### Anwendung

Du bist niedergelassener Hausarzt und musst in MU Stage 1 fünf Menu-Objectives wählen. Welche würdest du priorisieren – und warum ist Reconciliation besonders relevant?
?
Sinnvolle Wahl für einen Hausarzt: (1) **Patient Electronic Access** – Patienten können auf Befunde zugreifen, stärkt Engagement; (2) **Reconciliation** (Medikamenten-/Problem-Listen-Abgleich) – bei Übergaben von Spital/Reha kritisch, verhindert Medikationsfehler; (3) **Patientenspezifische Bildungsressourcen** – passt zu Prävention/chronischer Versorgung; (4) **Lab-Ergebnisse im EHR** – direkte Verfügbarkeit ohne Medienbruch; (5) **Drug Formulary Checks** – Kostentransparenz für Patienten und Effizienz. Warum **Reconciliation besonders relevant**: Bei Entlassung aus dem Krankenhaus ändert sich die Medikation häufig; ohne Abgleich (Reconciliation) entstehen gefährliche Medikationsfehler durch veraltete Listen im Primärversorger-EHR. Die Vorlesung übersetzt Reconciliation explizit als „Abstimmung".

Skizziere am Beispiel Diabetes den Aufbau eines CQM – mit Numerator, Denominator und Exclusion.
?
Beispiel-CQM (im Geiste der in der VL beschriebenen Logik): **„HbA1c Poor Control"** – misst, wie viele Diabetes-Patienten eine schlechte Blutzuckerkontrolle haben (höher = schlechter). **Denominator**: alle Patienten mit Typ-2-Diabetes-Diagnose im Reporting-Zeitraum, Alter 18–75, im EHR dokumentiert (= eligible population). **Numerator**: davon Patienten mit HbA1c > 9 % (schlechte Kontrolle). **Exclusions**: Patienten in Palliativversorgung, Patienten ohne HbA1c-Messung im Zeitraum. **Result**: Anteil als Prozentsatz; niedriger Anteil = gute Versorgungsqualität. Unter MU werden CQMs berichtet – unter MACRA fließen sie in Pay-for-Performance-Boni ein. Anforderung Stage 1: 6 CQMs (3 Core + 3 aus 38 Optionen); Hospitals: 15 CQMs.

Welche der drei MU-Hauptkomponenten (Use / Exchange / Quality Reporting) liegt im Fokus jeder Stage – und was impliziert das als Reifegrad-Logik?
?
Die drei MU-Hauptkomponenten bauen als Reifegrad aufeinander auf: **Stage 1 → Komponente 1 (Use)**: Nachweis, dass das EHR tatsächlich genutzt wird – CPOE, e-Prescribing, Demografien, Vital Signs, 80 %-Patientenerfassung. **Stage 2 → Komponente 2 (Exchange)**: Datenaustausch zwischen Versorgern, strukturierter Lab-Import, elektronische Care-Summaries bei Transitions, strukturierte Vital-Signs-Dokumentation. **Stage 3 → Komponente 3 (Quality Reporting / Outcomes)**: volle Interoperabilität, HIE-Teilnahme, Clinical Data Registry Reporting, kein Menu mehr – alle Anforderungen verpflichtend. **Reifegrad-Logik**: Erst Use sicherstellen → dann Exchange über Grenzen hinweg → dann Outcome messen. Das entspricht grob den LCIM-Schichten (Technical / Syntax-Semantics / Process Composability).

Wie stark lud MU Stage 1 für einen durchschnittlichen EP im ersten Jahr – und wie stand das im Verhältnis zum Anreiz?
?
Im ersten Implementierungsjahr entstanden typischerweise: **Produktivitätsverluste ca. 20 %** im ersten Monat; **EHR-bedingte Erlösverluste ca. 11.200 US$**; **Lern- und Anschaffungskosten ca. 10.325 US$** – Gesamtaufwand ca. **21.500 US$**. Demgegenüber stand der durchschnittliche MU-1-Anreiz 2011 von Ø **18.600 US$** – also ein Negativsaldo von ca. 2.900 US$ im ersten Jahr. Die Amortisation erfolgte erst über mehrere Folgejahre durch weitere Anreize und langfristige Produktivitätsgewinne. Für Hospitals war die Rechnung günstiger (Ø 1,6 Mio. US$ Anreiz bei proportional größerer Infrastruktur).

---

### Diskussion

Was war die inhaltliche Eskalationslogik von Stage 1 → Stage 2 → Stage 3 – und was zeigt das über die Strategie des Programms?
?
Stage 1 (2011): „Haben die Provider überhaupt ein EHR und nutzen es?" – Fokus auf grundlegende Datenerfassung und interne Nutzung. Stage 2 (2014): „Tauschen die Provider Daten aus?" – Fokus auf elektronischem Austausch, strukturierten Imports, Care Transitions. Stage 3 (2018): „Verbessert das EHR messbar die Versorgungsqualität?" – Fokus auf Interoperabilität, Outcomes, vollständiger Verpflichtung (kein Cherry-Picking via Menu). Die Strategie war gradualistisch: niemals alle Anforderungen auf einmal, sondern schrittweises Anheben der Schwellen. Kritik: Die Schritte waren zu klein und zu langsam – bis Stage 3 verpflichtend war (2018), war die Industrie 9 Jahre unter Programm, und Interoperabilität war immer noch ungelöst. MACRA musste eingreifen.

Warum war Stage 2 (Exchange) technisch herausfordernd – welche Standards standen zur Verfügung und welche fehlten?
?
Stage 2 verlangte nachweisbaren elektronischen Datenaustausch bei Care Transitions und anderen Übergabe-Szenarien. **Technisch verfügbare Standards 2014**: HL7 v2 (weit verbreitet, aber point-to-point), **Consolidated CDA (C-CDA)** als Standard für Care-Summary-Dokumente, **Direct Project** (sicherer, SMTP-basierter Nachrichtenkanal). **Fehlende Grundlage**: echte Interoperabilität setzte semantische Übereinstimmung voraus (LOINC, SNOMED) – die in vielen Systemen nicht konsistent implementiert war. Außerdem: kein funktionierender nationale Health Information Exchange (HIE) Infrastructure. Das Ergebnis: viele Provider erfüllten formell die Exchange-Anforderung (sie konnten eine C-CDA-Datei senden), aber der Empfänger konnte sie oft nicht sinnvoll verarbeiten – Strukturell-ohne-Semantik-Problem (vgl. [[EHR - Interoperabilität - Strukturell vs Semantisch]]).

Das Menu-Optionen-Konzept von Stage 1/2 wurde in Stage 3 abgeschafft. Was war das Problem – und welches Policy-Design-Prinzip steht dahinter?
?
**Problem in Stage 1/2**: Provider wählten bevorzugt die **einfachsten** Menu-Objectives aus, die mit minimalem technischem Aufwand zu erfüllen waren – sog. **Cherry-Picking**. Schwierige Objectives (z. B. strukturierter Datenaustausch, Reconciliation) wurden vermieden, obwohl sie für die Versorgungsqualität wichtiger gewesen wären. Ergebnis: das Programm verbesserte formal die EHR-Nutzungsrate, aber nicht die Bereiche, die echten Nutzen gebracht hätten. **Policy-Design-Reaktion Stage 3**: Abschaffung der Menu-Optionen, alle 8 Core-Requirements verpflichtend. **Prinzip**: Wenn man messbaren Fortschritt in schwierigen Bereichen will, muss man diese verpflichtend machen – optionale Anforderungen werden systematisch vermieden. Lesson Learned für zukünftige eHealth-Programme: Pflicht-Mindeststandards sind effektiver als Menü-Flexibilität.

MU Stage 3 verknüpft sich mit MACRA und Pay for Performance. Welche Risiken entstehen durch diese Anreizverschiebung?
?
**Pay for Performance (P4P)** vergütet Provider für gute CQM-Werte statt für Einzelleistungen. Plausible **Risiken**: (1) **Risikoselektion** – Provider bevorzugen gesunde, einfach behandelbare Patienten, bei denen gute Outcomes wahrscheinlich sind; Patienten mit Multimorbidität oder sozialer Benachteiligung werden weniger attraktiv; (2) **Outcome-Code-Inflation** – Dokumentation wird optimiert, um gemessene Outcomes gut aussehen zu lassen, ohne tatsächliche Verbesserung; (3) **Vernachlässigung schwer messbarer Aspekte** – Empathie, End-of-Life-Care, Patientenpräferenzen fließen nicht in CQMs ein; (4) **EHR-Click-Burden steigt** – um CQM-Reporting zu ermöglichen, müssen Provider strukturiert dokumentieren → Burnout-Risiko. **Gegenargument**: P4P setzt richtige Anreize für koordinierte Versorgung chronisch Kranker, wenn Risikoadjustierung korrekt erfolgt. Die Vorlesung nennt die Risikoselektion explizit.

Wie valide ist die MU-Bilanz – und was sind die zentralen ungeklärten Fragen nach Ende des Programms?
?
**Formaler Erfolg**: EHR-Adoption in US-Krankenhäusern stieg von < 10 % (2008) auf > 95 % (2017). **Problematische Evidenz**: 82–92 % Self-Report-Verbesserungen (CDS, Kommunikation, Medikationsfehler) sind anfällig für Sunk-Cost-Bias und Social-Desirability-Bias; keine randomisierten Kontrollgruppen. **Unintended Consequences**: (1) **Note-Bloat** – EHR-Dokumente wuchsen durch Copy-Paste und Compliance-Checkboxen auf hunderte Seiten an, wurden unlesbar (→ [[EHR - Progress Notes - EHR Lesbarkeitsproblem]]); (2) **Provider-Burnout** durch Click-Burden; (3) **Daten-Friedhöfe** – riesige Datenmengen ohne Secondary-Use-Infrastruktur. **Ungeklärte Kernfrage**: Hat MU die Patientenversorgung substantiell verbessert? Die wissenschaftliche Literatur zeigt gemischte Ergebnisse – Adoption war erfolgreich, Outcome-Nachweis bleibt umstritten.

Ist die Schwelle „80 % der Patienten im EHR" (MU Stage 1) hoch oder niedrig – und was verrät der Vergleich mit dem ELGA-Ansatz?
?
**US-Kontext**: 80 % erscheint niedrig – ein Provider darf 20 % seiner Patienten außerhalb des zertifizierten EHR führen. Diese Toleranz war politisch notwendig, um die Adoption nicht zu blockieren (Übergangszeitraum, technische Lücken). Inhaltlich: 20 % nicht im EHR bedeutet 20 % ohne potenziellen CDS-Vorteil, ohne vollständige Medikationsliste, ohne strukturierten Datenaustausch. **Vergleich ELGA**: ELGA zielt auf alle Patienten ab, hat aber strukturell andere Lücken (Reha-Zentren, Privatkliniken). ELGA-Anbindung ist nicht als Prozentziel, sondern als Sektormandat definiert – wer angeschlossen ist, muss alle Dokumente einstellen. **Lesson**: Prozentziele (MU) vs. Sektormandate (ELGA) sind komplementäre Ansätze mit je eigenen Lücken. 80 % war als Startschwelle pragmatisch – aber keine Klinik sollte dauerhaft 20 % analoger Patienten akzeptieren.

---

## Mögliche Anschlussfragen des Prüfers

- Was sind MIPS (Merit-based Incentive Payment System) und APMs (Alternative Payment Models) unter MACRA?
- Welche konkreten 8 Core-Requirements hat MU Stage 3 für EPs? (im PDF nicht ausgeführt – Verweis auf CMS-Dokumentation)
- Wie verhält sich das Direct Project (Stage 2) zu modernen FHIR-basierten API-Austauschen (Stage 3+)?
- Welche Rolle spielte HL7 C-CDA in Stage 2 – und warum reichte das nicht für echte Interoperabilität?
- Wie wirkt sich Note-Bloat konkret auf die Patientensicherheit aus?
- Welcher Ansatz ist besser für Outcome-Verbesserung: strukturierte Anforderungen (MU) oder marktbasierte Anreize (z. B. ACOs)?
- Wie hätte das MU-Programm aussehen sollen, wenn man es 2024 neu designen würde?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
