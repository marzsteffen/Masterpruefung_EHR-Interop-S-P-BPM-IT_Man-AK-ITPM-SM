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

# EHR - PF - SOAP Notes Detail

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz deckt das SOAP-Themengebiet in der Tiefe ab: das SOAP-Grundprinzip (S/O/A/P), alle Unter-Strukturen (OLDCARTS, HEADSS, Review of Systems, Differential Diagnosis, Plan-Sub-Komponenten), Varianten und Erweiterungen (APSO, SOAPE), Templates, Progress Notes, das EHR-Lesbarkeitsproblem sowie die empirische Studie Lin et al. 2013 zur APSO-Adoption. Inhaltsbasis sind die SOAP-Notes-Vorlesung und das StatPearls-Paper (SOAP Notes StatPearls). **Honeypot-Hinweis:** SOAP Inhalte sind quelltreu – keine Extrapolationen über das PDF hinaus, Ergänzungen aus StatPearls sind als solche kenntlich.

## Verlinkte Konzepte

- [[EHR - SOAP - Prinzip]]
- [[EHR - SOAP - Subjective]]
- [[EHR - SOAP - Objective]]
- [[EHR - SOAP - Assessment]]
- [[EHR - SOAP - Plan]]
- [[EHR - SOAP - Progress Notes]]
- [[EHR - SOAP - APSO Variante]]
- [[EHR - SOAP - HEADSS]]
- [[EHR - SOAP - OLDCARTS]]
- [[EHR - SOAP - Review of Systems]]
- [[EHR - SOAP - Symptoms vs Signs]]
- [[EHR - SOAP - Differential Diagnosis]]
- [[EHR - SOAP - SOAPE Erweiterung]]
- [[EHR - SOAP - Schwächen und Kritik]]
- [[EHR - SOAP - Templates]]
- [[EHR - Progress Notes - EHR Lesbarkeitsproblem]]
- [[EHR - Studie - APSO Adoption Lin 2013]]

---

## Karten

### Definition

Was bedeutet SOAP – welche vier Komponenten hat das Schema, und welche Informationsquelle liefert jeweils den Inhalt?

?

**SOAP** ist das Standard-Dokumentationsschema für Patientenbegegnungen in der Medizin. Vier Komponenten: (S) **Subjective** – aktuelle Beschwerden in narrativer Form, so wie der Patient sie beschreibt; Informationsquelle: Patient. (O) **Objective** – messbare, reproduzierbare, nachvollziehbare Fakten; Informationsquelle: Untersucher (Messung, Beobachtung). (A) **Assessment** – ärztliche Diagnose für diese Visite, narrativ und/oder kodiert (ICD-10, SNOMED-CT); Informationsquelle: Arzt (Interpretation). (P) **Plan** – was der Versorger als nächstes tun wird; Informationsquelle: Arzt (Entscheidung). Schlüsselzitat aus der Vorlesung: „Healthcare is event driven – we go to a physician when something is wrong. Healthcare documentation is governed by the SOAP principle." SOAP ist die dritte Dimension des problem-orientierten medizinischen Records (Weed, 1960er). SOAP ≠ APSO: gleiche Inhalte, andere Reihenfolge.

Was ist OLDCARTS – welche 8 Aspekte bildet es ab, und wo in SOAP wird es verwendet?

?

**OLDCARTS** ist ein Mnemonic zur strukturierten Erfassung der **History of Present Illness (HPI)** im Subjective-Block. Die 8 Buchstaben: **O** Onset (wann begann es?), **L** Location (wo?), **D** Duration (wie lange schon?), **C** Characterization (wie beschreibt der Patient das Symptom?), **A** Alleviating and Aggravating factors (was lindert/verschlimmert?), **R** Radiation (strahlt aus oder bleibt lokal?), **T** Temporal factor (tageszeitliche Muster?), **S** Severity (Skala 1–10). Eingeleitet wird die HPI mit einem one-line opening: „47-year-old female presenting with abdominal pain." OLDCARTS ist eine Substruktur des Subjective-Blocks, nicht für die gesamte SOAP-Note. Verwandtes Mnemonic: **OPQRST** (Onset, Provocation/Palliation, Quality, Region, Severity, Time) – ähnliche Aspekte, andere Reihenfolge.

Was ist HEADSS – welche Aspekte deckt es ab, und in welchem Kontext wird es besonders eingesetzt?

?

**HEADSS** ist ein Mnemonic zur strukturierten Erhebung der **Social History** im Subjective-Block. Buchstaben: **H** Home and Environment (Wohnsituation, Familie), **E** Education, Employment, Eating (Schul-/Berufssituation, Ernährung), **A** Activities (Hobbies, Sport), **D** Drugs (Tabak, Alkohol, illegale Drogen), **S** Sexuality (Orientierung, Aktivität, Risiken), **S** Suicide/Depression (Suizidgedanken, depressive Symptomatik). Besonders verbreitet in der **Adoleszenten- und Jugendmedizin**, weil es psychosoziale Risikofaktoren systematisch adressiert. Erweiterte Variante: **HEEADSSS** (zusätzlich Eating als eigener Block und Safety/Spirituality). HEADSS ≠ OLDCARTS: HEADSS = Sozialanamnese (Lebenskontext), OLDCARTS = HPI (akute Beschwerde).

Was ist der Unterschied zwischen Symptom und Sign – wo in SOAP werden sie dokumentiert, und warum ist die Trennung klinisch bedeutsam?

?

**Symptom**: subjektive Beschreibung des Patienten → gehört in **Subjective**. **Sign (Befund)**: objektiver, reproduzierbarer Befund des Untersuchers → gehört in **Objective**. Beispiel aus StatPearls: „stomach pain" (Symptom, Subjective) vs. „abdominal tenderness to palpation" (Sign, Objective). Weitere Beispiele: „Ich fühle Fieber" (Symptom) vs. „Körpertemperatur 38,7 °C axillär" (Sign); „shortness of breath" (Symptom) vs. „SpO2 89 %, RR 28/min" (Sign). **Klinische Bedeutung**: Die Trennung ist Voraussetzung für valides klinisches Reasoning – aus Symptom + Sign + Test-Ergebnis → Assessment (Differentialdiagnose). SNOMED-CT unterscheidet in seiner Concept-Hierarchie entsprechend Sub-Klassen innerhalb von „Clinical finding". Häufiger Fehler: Befunde wie „Druckschmerz im rechten Unterbauch" werden in Subjective dokumentiert.

---

### Anwendung

Was gehört typischerweise in den Objective-Block einer SOAP-Note – und welche Inhalte werden oft falsch zugeordnet?

?

Inhalte des **Objective**-Blocks laut Vorlesung: Vital signs (Blutdruck, Temperatur, Herzfrequenz), Findings from physical examination (oft als normal/abnormal kodiert), Laboratory results, Measurements (Height, Weight, BMI), ECG. Außerdem laut Folie: **Current medications and allergies**, **Family history** – das sind pragmatische Zuordnungen, die inhaltlich diskutierbar sind (sie sind nicht im klassischen Sinn „messbare Fakten", aber etabliert in der Dokumentationspraxis). Falsch zugeordnet werden: Patientenaussagen über Schmerz (gehört Subjective), Diagnose (gehört Assessment), Plan (gehört Plan). **EMR-Konsequenz**: EMR-Systeme bieten typischerweise mehrere Tabs für Objective: Vital Signs Tab, Physical Examination Tab, Laboratory Results Tab, ECG Tab – jeder Tab deckt einen Unterbereich ab.

Welche 5 Sub-Komponenten hat der Plan-Block einer SOAP-Note – und was ist häufiger Fehler?

?

Plan-Sub-Komponenten laut Vorlesung (Beispiel Appendektomie-Patient): (1) **Diagnostic component** – weitere Diagnostik und Monitoring (z. B. „continue to monitor labs"); (2) **Therapeutic component** – therapeutische Maßnahmen (z. B. „advance diet"); (3) **Referrals** – Überweisungen (z. B. „follow up with Cardiology within three days of discharge"); (4) **Patient education component** – Patientenaufklärung (z. B. „progress is good"); (5) **Disposition component** – Entlass-Disposition (z. B. „discharge to home in the morning"). **Häufiger Fehler**: Plan wird auf Therapie/Medikation reduziert. Diagnostik (Lab-Orders) und Patient Education sind ebenso Pflichtbestandteile. Disposition entfällt bei ambulanten Visiten, ist bei stationären Aufenthalten zentral. FHIR-Mapping: ServiceRequest (Diagnostik), MedicationRequest (Therapie), ReferralRequest, CarePlan (übergreifend), Goal.

Was ist eine Differential Diagnosis im SOAP-Schema – wie wird sie aufgebaut, und welche Rolle spielen „don't miss"-Diagnosen?

?

Die **Differential Diagnosis (DD)** ist eine Substruktur des **Assessment**-Blocks. Aufbau: eine geordnete Liste möglicher Diagnosen von der **wahrscheinlichsten zur unwahrscheinlichsten**, mit dem Clinical Reasoning dahinter. Struktur laut StatPearls: Problem 1 → Liste der DD (most → least likely) + Discussion (was unterscheidet die Diagnosen) + Plan for Problem 1. **„Don't miss"-Diagnosen**: potenziell gefährliche Diagnosen, die unbedingt ausgeschlossen werden müssen, auch wenn sie weniger wahrscheinlich sind – z. B. Lungenembolie bei atypischem Brustschmerz. Beispiel: Patient mit Brustschmerz → DD: (1) Akutes Koronarsyndrom (don't miss), (2) Lungenembolie (don't miss, Wells-Score 3), (3) Muskuloskeletaler Schmerz, (4) Reflux. FHIR-Mapping: mehrere `Condition`-Resourcen mit verschiedenem `verificationStatus` (provisional, differential, refuted). DD ≠ Working Diagnosis (= aktuell wahrscheinlichste Diagnose).

Was sind SOAP-Templates – welche Vorteile bieten sie, und mit welchem konkreten Beispiel wird das in der Vorlesung illustriert?

?

**SOAP-Templates** sind in EMR-Systemen anlegbare, fachspezifische Vorlagen für wiederkehrende Patiententypen. Laut Vorlesung: „Some EMR systems allow to build customized SOAP templates. For example, a department specialized in injuries may want to build an 'injury SOAP template'." Vorteile: **Less typing, more (automated) coding** (ICD-10 / SNOMED vorausgefüllt); **Standardized questions** (kein Vergessen wichtiger HPI-Items); **Completeness** (alle Felder vorhanden); **Standardized therapies** (Therapiebausteine vorgeschlagen). Aufbau eines Injury-Templates: Subjective mit „Mechanism of Injury", „Time of Injury"; Objective mit Wundgröße, Lokalisation, Pulsstatus; Assessment mit vorkodierten Verletzungsdiagnosen; Plan mit Wundversorgung, Tetanus-Schutz, Disposition. Weitere Template-Beispiele: Diabetes-Routine, Wellness-Visit. Abgrenzung: Template ≠ klinischer Pathway (Template = Dokumentationshilfe, Pathway = Prozesslogik mit Entscheidungen).

Was sind Progress Notes – und wie unterscheidet sich SOAPE von reinen Progress Notes?

?

**Progress Notes**: aufeinander aufbauende SOAP-Notes über mehrere Visiten; jede Folge-SOAP-Note bezieht sich auf die vorige: S (Verbesserung der Beschwerden?), O (Verlauf der Messwerte?), A (War Diagnose korrekt? Anpassung nötig?), P (Plan­anpassung?). **SOAPE**: Erweiterung von SOAP um einen fünften Block **E = Evaluate** – explizite Bewertung, wie gut der vorherige Plan gewirkt hat. Fragen im E-Block: Hat der Plan das Ziel erreicht? Wo bleibt der Patient hinter den Erwartungen zurück? Welche Konsequenz für den nächsten SOAP-Zyklus? Unterschied: Progress Notes bilden Verlauf über mehrere getrennte SOAP-Notes ab; SOAPE integriert die Verlaufsbewertung **innerhalb einer einzelnen Note**. Laut StatPearls: SOAPE hat sich praktisch **nicht durchgesetzt** – SOAP bleibt der Standard, obwohl SOAPE die fehlende Zeitdimension explizit adressiert.

---

### Diskussion

Welche drei Hauptschwächen hat das SOAP-Schema – und wie werden sie adressiert?

?

(1) **Fehlende Zeitdimension**: SOAP dokumentiert einen Zustand pro Visite ohne explizite Bewertung der Veränderung gegenüber dem Vorwert. Adressierung: SOAPE-Erweiterung (E = Evaluate) – hat sich aber nicht durchgesetzt. (2) **Lese-Reihenfolge ineffizient für chronische Visiten**: Bei Folgevisiten muss der Arzt erst durch S und O scrollen, bevor er Diagnose und Plan findet. Adressierung: APSO-Variante (Assessment und Plan vorne) – durch Lin-2013-Studie teilweise bestätigt (hohe subjektive Präferenz). (3) **EMR-Datenüberfrachtung**: EMRs begünstigen unkritisches Anhängen großer Datenmengen; Notes bis zu 17 Seiten; klinisches Reasoning „extraordinarily difficult to locate." Adressierung: sorgfältige Selektion klinisch relevanter Daten, Templates mit Fokus, Summary-Algorithmen, LLMs. Wichtig: Die Kritik richtet sich teils an SOAP selbst, teils an seine EMR-Implementierung – SOAP bleibt trotzdem der dominante Standard.

Lin et al. (2013): Was hat die APSO-Adoptionsstudie gezeigt – und wie ist der Widerspruch zwischen subjektivem und objektivem Befund zu interpretieren?

?

Setting: 13 ambulante Kliniken, Allscripts EHR V10.2, Messung nach 2 Monaten. **Adoption**: Mandate-Kliniken 100 % (47/47), Voluntary-Kliniken 51 % (37/73), gesamt 70 %. **Satisfaction-Survey (n=64)**: 81 % fanden klinisch relevante Daten leichter, 82 % browsten schneller, 75 % bevorzugten APSO beim Lesen, 83 % Reader-Satisfaction. **Objektiver Zeittest (n=14)**: klinische Fragen aus 10 APSO + 10 SOAP Notes beantwortet – **kein signifikanter Zeitunterschied** (P = 0.37), keine Genauigkeitsdifferenz (P = 0.54). **Interpretationsansätze für den Widerspruch**: (a) Aufgabendesign misst nicht das, was Provider als „faster browsing" wahrnehmen (ergonomisches vs. gemessenes Zeitgefühl); (b) n = 14 zu klein für statistischen Effekt; (c) subjektive Satisfaction ist ein valider Outcome in sich – Provider-Burnout und EHR-Adoption sind reale Konsequenzen. Limitation: Single-Center, nur ambulant, nicht randomisiert kontrolliert.

Das EHR-Lesbarkeitsproblem: Welche drei Ursachen nennt Lin et al. – und welche systemischen Konsequenzen entstehen?

?

Lin et al. (2013): EHR-Progress-Notes können bis zu **17 elektronische Seiten** umfassen. Drei Hauptursachen: (1) **Billing requirements** – CMS Evaluation/Management Levels erzwingen Dokumentationsumfang für Reimbursement; Provider füllen Sections nicht aus klinischem Bedürfnis, sondern zur Erreichung des Billing-Levels. (2) **Regulatory statements** – Pflicht-Boilerplates aus regulatorischen Vorgaben ohne klinischen Wert. (3) **Automatische Einbettung von Testergebnissen** – alle Lab-Ergebnisse, alle Vital-Signs-Verläufe werden unkritisch eingefügt. **Systemische Konsequenzen**: Clinical Reasoning „extraordinarily difficult to locate"; Missing data durch Übersehen → Produktivitätsverlust und erhöhte Kosten; Provider-Frustration, die EHR-Adoption und -Deployment hemmt. Paradox: EHRs sollten die Lesbarkeit gegenüber handgeschriebenen Notes verbessern – das Lesbarkeitsproblem ist ein neues, strukturelles Problem der EHR-Ära. Note-Cloning (Copy-Forward) verschärft das Problem zusätzlich.

APSO vs. SOAP beim Schreiben vs. Lesen – wann ist welche Reihenfolge sinnvoller, und welche Lösung schlägt die Vorlesung vor?

?

**SOAP-Reihenfolge (S → O → A → P)**: folgt dem chronologischen Visitenablauf – natürlich beim **Schreiben**, weil der Arzt zuerst hört (S), dann misst (O), dann interpretiert (A), dann entscheidet (P). Geeignet für akute Erstvorstellungen, bei denen der Leser den Diagnoseprozess nachvollziehen soll. **APSO-Reihenfolge (A → P → S → O)**: stellt Diagnose und Plan vorne – optimal beim **Lesen** von Folgevisiten bei chronischen Erkrankungen, wo der Leser primär „Was ist die Diagnose, was tun wir?" wissen will. Studie Lin: 75 % bevorzugten APSO beim Lesen, subjektiv schneller und besser findbar. **Vorlesungs-Lösungsansatz**: die Vorlesung formuliert dies als offene Diskussionsfrage: „How would you resolve this issue?" Pragmatische Antwort: **Entkopplung von Dokumentation und Anzeige** – das EMR speichert strukturiert in FHIR-Resourcen (Condition, CarePlan, Encounter, Observation), das Display rendert auf Wunsch SOAP oder APSO. Das Papier-/Template-basierte SOAP bleibt Standard, aber dynamische Anzeige wird zum UX-Thema.

Review of Systems vs. Physical Examination: Wo liegt die Trennlinie, und welches Checkbox-Risiko bringt ROS im EMR mit sich?

?

**Review of Systems (ROS)**: systembasierte Frageliste innerhalb **Subjective** – erfasst Symptome, die der Patient nicht spontan nennt. Inhalt: patientenberichtete Symptome pro Organsystem (General, Kardiovaskulär, Pulmonal, GI, Urogenital, Muskuloskeletal, Neurologisch, Psychiatrisch etc.). **Physical Examination**: Untersucher-basierte Befunde in **Objective** – Ärztliches Abhorchen, Palpation, Perkussion etc. **Trennlinie**: ROS = was Patient sagt; PE = was Arzt findet. Beispiel: Patient sagt „Husten" (ROS, Subjective) → Arzt auskultatiert „Feuchte Rasselgeräusche rechts basal" (Physical Exam, Objective). **Checkbox-Risiko im EMR**: EMR-Systeme implementieren ROS oft als Checkbox-Liste pro System. Risiko: mechanisches Abhaken ohne klinische Auseinandersetzung; Erfassung von Systemen, die für den Vorstellungsgrund irrelevant sind; Compliance-getriebene Vollständigkeit statt klinischer Relevanz. Trade-off: Vollständigkeit (alle Systeme abgehakt) vs. Effizienz und klinische Tiefe.

Templates: Standardisierung vs. „Cookie-cutter medicine" – wo liegt die Grenze?

?

**Pro Templates**: weniger Tipparbeit, automated coding, standardisierte Fragen für Vollständigkeit, standardisierte Therapie-Vorschläge. Besonders wertvoll für häufige, wiederkehrende Patiententypen (Diabetes-Routine, Verletzungen, Wellness). Ermöglicht Sekundärnutzung (Qualitätssicherung, Forschung) durch konsistente Felder. **Kritik „Cookie-cutter medicine"**: Templates können klinisches Denken verflachen, wenn Ärzte Felder mechanisch ausfüllen, ohne zu prüfen ob sie für diesen Patienten relevant sind. Patienten die nicht ins Template passen, werden möglicherweise schlechter dokumentiert. **Grenze**: Templates sollen den Kern abdecken, aber Freitext-Felder für Individualität bewahren. Modernes Konzept: **Smart Phrases / Macros** (EMR-spezifisch) + dynamische Templates, die Felder je nach Assessment einblenden/ausblenden. KI/LLM-Integration könnte künftig kontextuelle Templates generieren, ohne starres Schema.

---

## Mögliche Anschlussfragen des Prüfers

- Welche FHIR-Resourcen entsprechen S/O/A/P jeweils?
- Was ist „Note Cloning" oder „Copy-Forward" – und welche Risiken entstehen?
- Welche Rolle spielt Patient Education im Plan-Block für Health-Literacy-Strategien?
- Warum wurde SOAPE entwickelt, und warum setzte es sich trotzdem nicht durch?
- Was sind CMS Evaluation/Management (E/M) Coding Levels?
- Welche Alternativen zu SOAP gibt es (DAR, PIE)?
- Was ist „pertinent ROS" vs. vollständigem ROS?
- Wie unterscheiden sich SOAP-Notes für Erst- vs. Folgevisiten strukturell?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
