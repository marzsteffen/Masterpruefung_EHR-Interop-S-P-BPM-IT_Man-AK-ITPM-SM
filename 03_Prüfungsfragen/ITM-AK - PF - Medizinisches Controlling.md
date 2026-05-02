---
fach: itm-ak
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - fach/vertiefung/itm-ak
  - typ/pruefungsfrage
  - status/offen
  - flashcards
---

# ITM-AK - PF - Medizinisches Controlling

## Kontext

Prüfungsfragen zum Themenblock **Medizinisches Controlling** aus der Vorlesung ITM-AK. Umfasst medizinisches Controlling als Funktion, DRG- und LKF-Vergütungssystem, ICD-10-Kodierung und MBDS sowie A-IQI als österreichisches Qualitätsmesssystem.

Quellen: 4 Konzept-Notes auf Basis der VL [[ITM-AK - VL - Controlling]].

---

## Verlinkte Konzepte

- [[ITM-AK - Medizinisches Controlling]]
- [[ITM-AK - DRG und LKF]]
- [[ITM-AK - ICD-10 und MBDS]]
- [[ITM-AK - A-IQI - Austrian Inpatient Quality Indicators]]

---

## Karten

### Definitionen

Was ist medizinisches Controlling und welche neun Aufgaben umfasst es laut Folie 55?
?
**Definition:** Spezielle Form des operativen Controllings im Krankenhaus mit Fokus auf medizinische Aspekte – insbesondere Optimierung der Erstattungspunkte und Kostenberechnung für Behandlungen; Bindeglied zwischen klinischem und nicht-klinischem Personal.
**Neun Aufgaben (Folie 55):**
1. Codierung (ICD-10, MEL/MBDS)
2. Reimbursement
3. Prozessmanagement
4. Operatives Controlling
5. Qualitätsmanagement
6. Moderation zwischen klinischem und nicht-klinischem Personal
7. Budgetierung
8. Evidenzbasierte Medizin
9. Gesundheitstechnologie-Bewertung

---

Was sind DRG und LKF und wie unterscheiden sie sich?
?
**DRG (Diagnosis Related Groups):** Internationales Erstattungsprinzip – ähnliche Behandlungsfälle werden zu Gruppen zusammengefasst und pauschal vergütet. Einteilung nach Schwere der Krankheit, Alter, Operationen, ICU-Aufenthalt, Medikamente.
**LKF (Leistungsorientierte Krankenanstaltenfinanzierung):** Österreichische Umsetzung des DRG-Prinzips. Das Krankenhaus erhält **Punkte** pro Fall; Punkte werden in Euro umgerechnet.
**Unterschied:** DRG ist der internationale Begriff (z. B. G-DRG in Deutschland mit direkter Euro-Vergütung); LKF ist die österreichische Variante mit Punkte-System. Beide verfolgen das Grundprinzip der Pauschalvergütung nach Fallgruppen.

---

Was sind ICD-10 und MBDS und wie hängen sie mit der Krankenhausvergütung zusammen?
?
**ICD-10** (International Classification of Diseases, 10. Revision): Internationaler Standard zur Kodierung von Diagnosen als alphanumerische Codes.
**MBDS** (Mindestbasisdatensatz): Österreichische Datenbasis – enthält pro stationärem Aufenthalt: Patient:innen-Stammdaten, eine **Hauptdiagnose**, mehrere **Nebendiagnosen** (alle in ICD-10) und **MELs** (medizinische Einzelleistungen).
**Vergütungskreislauf:**
1. Arzt kodiert Diagnosen (ICD-10) und Leistungen (MEL) im KIS.
2. Daten fließen in den MBDS-Datensatz.
3. Software (Xdok) berechnet daraus LKF-Punkte.
4. Punkte werden in Euro umgerechnet – das ist die Erstattung.

---

Was sind A-IQI und seit wann gelten sie in Österreich?
?
**A-IQI** (Austrian Inpatient Quality Indicators): Österreichische stationäre Qualitätsindikatoren, obligatorisch für jedes öffentliche Krankenhaus seit der **Gesundheitsreform 2013**.
**Gemessene Indikatoren:**
- Sterblichkeit (Mortalität)
- Dauer des stationären Aufenthalts
- Aufnahmequote auf der Intensivstation
- Komplikationsrate
- Durchgeführte Verfahren (z. B. CT-Scans)
**Rückmeldung:** Ampel-System (grün/gelb/rot) pro Diagnose; bei Auffälligkeiten: **Peer-Review**-Verfahren.
**Datenbasis:** MBDS-Daten – die Datenerfassung für Erstattung und Qualitätsmessung erfolgt auf derselben Grundlage.

---

### Anwendung

Erläutern Sie die Krankenhausvergütung in Österreich anhand der zwei LKF-Beispielfälle.
?
**Vergütungslogik (Folie 53–54):**
1. Behandlung des Patienten → Kodierung von Hauptdiagnose + Nebendiagnosen + MELs.
2. Software (Xdok) berechnet LKF-Punkte aus Diagnose-Kombination.
3. Punkte × Punktewert (€/Punkt) = Erstattung.
**Folie-54-Beispiele:**
- Testpatient **ohne Aufdehnung** (Diabetes mellitus mit Fehl-/Mangelernährung): **1.860 Punkte**.
- Testpatient **mit Aufdehnung** (PTA – perkutane transluminale Angioplastie): **3.383 Punkte**.
→ Komplexere Fälle mit mehr Leistungen / schwereren Diagnosen erhalten mehr Punkte und damit höhere Erstattung.

---

Welche Daten enthält ein MBDS-Datensatz und welche IT-Voraussetzungen erfordert er?
?
**MBDS-Inhalt pro stationärem Aufenthalt:**
- Patient:innen-Stammdaten (Alter, Geschlecht, Wohnort)
- Aufenthaltsdaten (Aufnahme-/Entlassdatum, Aufnahmegrund)
- **Hauptdiagnose** (ICD-10-Code, eine)
- **Nebendiagnosen** (ICD-10, mehrere)
- **MELs** (medizinische Einzelleistungen)
**IT-Voraussetzungen:**
- Strukturierte Diagnose-Erfassung im KIS mit ICD-10-Integration.
- Kodierungs-Software (Xdok/KDok – jahresaktuell gepflegt).
- Schnittstelle zum LKF-Berechnungssystem und zur A-IQI-Datenlieferung.
- Datenqualitätssicherung (Vollständigkeit, Plausibilitätsprüfung).

---

Was passiert in A-IQI, wenn ein Krankenhaus eine rote Ampel bei einer bestimmten Diagnose erhält?
?
**Schritt 1:** Rote A-IQI-Ampel = die Kennzahl (z. B. Komplikationsrate, Mortalität) liegt auffällig über dem Erwartungswert für diese Diagnose.
**Schritt 2:** **Peer-Review** wird ausgelöst – unabhängige Expertinnen und Experten aus anderen Krankenhäusern prüfen gemeinsam mit der betroffenen Klinik die Fälle.
**Schritt 3:** Ursachenanalyse – Daten-, Kodierungs- oder echter Versorgungsproblem?
**Schritt 4:** Definition und Umsetzung von Verbesserungsmaßnahmen.
→ Peer-Review ist keine Bestrafung, sondern ein Lernverfahren – ähnlich der M&M-Konferenz, aber institutionsübergreifend.

---

Welche Rolle spielt das medizinische Controlling als Mediator zwischen klinischem und nicht-klinischem Personal?
?
**Spannungsfeld:** Ärzt:innen und Pflegende denken in Diagnosen und Behandlungen; Verwaltung und Controlling denken in Budgets, Punkten und Erlösen.
**Medizinisches Controlling als Brücke:**
- Übersetzt klinische Dokumentation in korrekte ICD-10-Codes (Kodierung).
- Erklärt dem klinischen Personal, welche Diagnosen und Leistungen für die Erstattung dokumentiert werden müssen.
- Erklärt der Verwaltung, welche medizinischen Komplexitäten warum welche Kosten verursachen.
- Moderiert bei Konflikten (z. B. Arzt will Patienten länger behalten → Controlling sieht Kostendruck).
→ Fehlt diese Funktion, kommt es zu Kodierfehlern, Erlösverlusten oder Fehlanreizen.

---

### Diskussion und Vergleich

Vergleichen Sie DRG/LKF und Bundled Payments als zwei Erstattungsmodelle.
?
| Aspekt | DRG / LKF | Bundled Payments |
|---|---|---|
| **Vergütungseinheit** | Einzelner stationärer Fall | Gesamter Behandlungszyklus (stationär + ambulant + Reha) |
| **Zeitraum** | Nur Akutaufenthalt | Voller Care Cycle (z. B. 90 Tage nach OP) |
| **Incentive** | Effizienz pro Fall | Koordination über alle Versorgungsstufen |
| **Risiko** | Krankenhaus trägt Risiko pro Fall | Anbieter-Konsortium trägt Risiko über Zyklus |
| **Problem** | Drehtüreffekt (frühe Entlassung + Wiederaufnahme zählt doppelt) | Komplexe Vertragsgestaltung; Attribuierungsproblem |
→ Bundled Payments sind ein Schritt Richtung Value-based Healthcare; DRG/LKF beheben das Costing-Problem nicht, weil sie Erstattung ohne Cycle-Cost-Bezug pauschalieren (Porter/Kaplan 2011).

---

Welche Anreize setzt das LKF-System – und wo führt es zu Fehlsteuerung?
?
**Positive Anreize:**
- Effizienzanreiz pro Fall (wer günstig behandelt, behält die Differenz).
- Vergleichbarkeit zwischen Krankenhäusern durch einheitliche Gruppen.
**Fehlsteuerungsrisiken:**
- **Up-Coding:** Diagnose schwerer kodieren als medizinisch gerechtfertigt (höhere Punkte, aber falscher MBDS).
- **Drehtüreffekt:** Patient früh entlassen, dann wiederkommen → zwei DRG-Fälle statt einem = höhere Vergütung.
- **Abwälzung auf Reha:** Akutkrankenhaus entlässt früh; Reha-Einrichtung trägt Rest.
- **Selektion:** Vermeidung kostenintensiver, niedrig vergüteter Patient:innen (z. B. Multimorbide).
→ Systemkritik von Porter/Kaplan 2011: DRG/LKF erzeugen keine echten Kosteninformationen; echte Kosten (TDABC) wären nötig.

---

Diskutieren Sie die Stärken und Schwächen von A-IQI als Qualitätsmesssystem.
?
**Stärken:**
- Standardisiert, flächendeckend, kontinuierlich (kein einmaliger Audit).
- Basiert auf ohnehin verpflichtend erhobenen MBDS-Daten – kein Zusatzaufwand.
- Peer-Review schafft interinstitutionelles Lernen.
- Transparenz: Vergleichsdaten öffentlich verfügbar (kliniksuche.at).
**Schwächen:**
- Begrenzte Indikatorenauswahl – nicht alle relevanten Qualitätsaspekte abgedeckt.
- **Patient:innen-Outcomes** (Lebensqualität, funktionelle Erholung) bleiben außen vor → nur Donabedian-Ergebnis im engeren Sinn.
- **Risikoadjustierung komplex:** Kliniken mit schwerkrankem Klientel haben strukturell schlechtere Kennzahlen.
- **„Teaching to the test":** Fokus auf gemessene Indikatoren verzerrt Prioritäten.
- **Nur stationär:** Ambulante Qualität ist nicht erfasst.
→ A-IQI ist ein Schritt Richtung outcome-orientierter Steuerung, aber kein Ersatz für VBHC-Outcome-Messung im Porter/Lee-Sinne.

---

Vergleichen Sie A-IQI und ISO-9001-Zertifizierung als zwei Ansätze der Qualitätssicherung im Krankenhaus.
?
| Aspekt | A-IQI | ISO 9001 Zertifizierung |
|---|---|---|
| **Art** | Datenbasiert, kontinuierlich | Audit-basiert, periodisch (alle 3 Jahre) |
| **Verpflichtung** | Gesetzlich (öff. KH seit 2013) | Freiwillig |
| **Gegenstand** | Klinische Ergebnisindikatoren | QM-System (Prozesse, Führung, Verbesserung) |
| **Fokus** | Was kommt am Ende raus (Outcomes) | Wie ist das System aufgestellt (Prozess) |
| **Rückmeldung** | Ampel-System + Peer-Review bei Auffälligkeit | Auditbericht, Nichtkonformitäten |
| **Adressat** | Krankenhaus + Fördergeber + Öffentlichkeit | Krankenhaus + Zertifizierungsstelle |
→ Idealerweise ergänzen sich beide: ISO 9001 strukturiert das QM-System; A-IQI misst, ob das System klinisch wirkt. Weder das eine noch das andere ist allein ausreichend.

---

Diskutieren Sie das Spannungsfeld zwischen Erstattungsoptimierung und Patientenversorgung im medizinischen Controlling.
?
**Kernspannung:** Das medizinische Controlling hat als Aufgabe die Optimierung der LKF-Erstattungspunkte – aber nicht auf Kosten der medizinischen Versorgungsqualität.
**Mögliche Konfliktfelder:**
- **Up-Coding vs. korrekte Dokumentation:** Übertriebenes Hochkodieren ist wirtschaftlich attraktiv, aber Abrechnungsbetrug.
- **Frühe Entlassung vs. klinische Notwendigkeit:** LKF-Anreiz zur Effizienz kann klinisch unfertige Entlassungen begünstigen.
- **Mengendruck vs. Qualität:** Mehr Fälle = mehr Punkte; aber überforderte Klinik kann Qualität nicht halten.
**Ausweg:**
- Value-based Healthcare würde die Vergütungslogik umkehren: Outcomes statt Fälle/Leistungen bezahlen.
- Medizinisches Controlling als Profession hat eine Compliance-Funktion: Erst korrekte Kodierung, dann Erlösoptimierung.

---

## Anschlussfragen

- Wie unterscheiden sich LKF (Österreich) und G-DRG (Deutschland) konkret?
- Welche Schnittstellen bestehen zwischen MBDS und ELGA?
- Wie verändert sich medizinisches Controlling mit zunehmender Value-based Healthcare?
- Welche Rolle spielt das New Public Management für A-IQI-Einführung?
- Wie hängt A-IQI mit der Balanced Scorecard eines Krankenhauses zusammen?

---

## Eigene Notizen

<!-- Platz für handschriftliche Ergänzungen oder Lernfortschritt -->
