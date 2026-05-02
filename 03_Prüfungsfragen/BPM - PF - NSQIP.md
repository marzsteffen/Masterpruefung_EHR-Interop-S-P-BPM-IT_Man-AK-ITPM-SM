---
fach: bpm
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/bpm
---

# BPM - PF - NSQIP

## Kontext

Kartenset zur mündlichen Masterprüfung BPM (eHealth, FH JOANNEUM). Themenbereich: ACS-NSQIP als ergebnisbasiertes Qualitätsverbesserungsprogramm – Ursprung, Methodik (Datenerhebung, Risikoadjustierung, O/E-Ratio), Wirksamkeitsbelege (Hall et al. 2009, österreichische Beobachtungsstudie) und Einordnung in den BPM-Kontext.

## Verlinkte Konzepte

- [[BPM - NSQIP - Programm]]
- [[BPM - NSQIP - Datenerhebung]]
- [[BPM - NSQIP - Risikoadjustierung]]
- [[BPM - NSQIP - O-E-Ratio]]
- [[BPM - NSQIP - Wirksamkeit Hall et al]]
- [[BPM - NSQIP - Beobachtungsstudie Oesterreich]]
- [[BPM - Komplikation - Definition]]
- [[BPM - Value-Based Care]]

---

## Karten

### Definition

Was ist ACS-NSQIP, woher kommt es, und welche vier Eigenschaften unterscheiden es von anderen Qualitätsprogrammen?
?
**Definition** (Folie 2):

> Das ACS NSQIP ist ein **ergebnisbasiertes, datengesteuertes, risikoadjustiertes** Programm zur Verbesserung der chirurgischen Qualität, mit dem Chirurgen und medizinische Zentren ihre Ergebnisse zuverlässig melden und möglicherweise die Versorgung verbessern und die Kosten senken können.

**Ursprung:** Veterans Health Administration (VA), Ende der 1980er Jahre. Auslöser: US-Gesetz **99-166**, das jährliche risikobereinigte Berichte chirurgischer Ergebnisse verlangte – obwohl es weder risikobereinigte Daten noch nationale Durchschnittswerte gab. Die VA musste beides erst aufbauen. Heute: über 750 Spitäler weltweit.

**Vier Unterscheidungsmerkmale ggü. anderen QM-Programmen:**

1. **Krankenakte statt Verrechnung:** NSQIP identifiziert **61 % mehr Komplikationen** als administrative Daten – darunter 97 % mehr OP-Stelleninfektionen und 100 % mehr Harnwegsinfekte.
2. **Risikoadjustiert:** Kliniken, die schwer kranke Patienten behandeln, werden nicht für ihr Patientenkollektiv bestraft.
3. **Casemix-berücksichtigend:** Spitäler mit komplexen Fällen können sich sinnvoll mit weniger komplexen Häusern vergleichen.
4. **30-Tage-Outcome:** Die Hälfte oder mehr aller Komplikationen tritt nach Entlassung auf – NSQIP erfasst sie trotzdem (z. B. ½ der Herzstillstände nach Kolektomie post-Entlassung).

---

Was ist die O/E-Ratio im NSQIP-Kontext, wie wird sie berechnet, und wie interpretiert man sie?
?
**O/E-Ratio** = Observed-vs-Expected-Ratio (beobachtete vs. erwartete Ereignisse).

```
O = Σ beobachteter Todesfälle / Komplikationen
E = Σ erwarteter Ereignisse (aus Risikoadjustierungsmodell)
─────────────────────────────────
O/E = O / E
```

**Interpretation:**
- **O/E < 1** → Klinik erbringt **bessere Leistung als erwartet** (besser als der statistische „Par").
- **O/E = 1** → erwartungsgerechte Leistung.
- **O/E > 1** → **signifikanter Überschuss** an unerwünschten Ereignissen → Trigger für Ursachenanalyse.

**Golfplatz-Analogie (Folie 12):** Die O/E-Ratio ist wie das „Par" auf einem Golfplatz – die erwartete Punktzahl. Es ist nicht peinlich, ein Par-72-Loch in 72 Schlägen zu beenden; peinlich ist nur, schlechter als Par zu sein.

**Praxisbeispiel:** Klinik mit 100 Hernien-OPs, 5 beobachtete Komplikationen (O=5), Modell erwartet 7 (E=7) → O/E = 0,71 → besser als erwartet. Bei 9 Komplikationen: O/E = 1,29 → schlechter als erwartet → Ursachenanalyse einleiten (Ishikawa, 5-Warum).

**Wichtig (Folie 14):** Die Rangliste der Krankenhäuser nach *unadjustierter* Mortalität hat **wenig Ähnlichkeit** mit der Rangliste nach *adjustierter* Mortalität – Verschiebungen sind drastisch. Krankenhäuser, die unadjustiert gut wirken, können adjustiert mittelmäßig sein und umgekehrt.

---

Was ist Risikoadjustierung im NSQIP, welche Prädiktoren verwendet das Modell, und was zeigt das Beispiel aus Folie 10?
?
**Ziel:** Berechnung der *erwarteten* Wahrscheinlichkeit eines unerwünschten Ereignisses (Mortalität, Komplikation) aus präoperativen Patientenfaktoren → faire Vergleichbarkeit zwischen Krankenhäusern unabhängig vom Schweregrad der Patientenpopulation.

**Methodik:** Stepwise-in/-out-Analyse – statistisch signifikante Prädiktoren aus einem Pool werden per logistischer Regression selektiert.

**Prädiktoren (Folie 9, Auszug):**
Alter, Geschlecht, ASA-Klassifikation, BMI, Anzahl weiße Blutkörperchen, BUN (Harnstoff), Hämatokrit, Thrombozyten, Albumin, Komorbiditäten (Diabetes, COPD …), Notfall-OP (ja/nein), Disseminierter Tumor (ja/nein), Aszites (ja/nein).

**Folie-10-Beispiel:**
Patient: 74 Jahre, Albumin 2,0 (3 SD unter Durchschnitt), ASA 4, BUN 102 (8 SD über Durchschnitt), Notfall-OP = 1, Aszites = 1 → **P(30-Tage-Mortalität) = 15 %** (erwarteter Wert E).

**Stabilität:** Die VA-Daten zeigen, dass Risikofaktoren von Jahr zu Jahr **bemerkenswert stabil** sind und exzellente prädiktive Validität aufweisen (Folie 11) – Modelle altern nicht schnell.

---

### Anwendung

Beschreiben Sie den Datenerhebungsprozess im NSQIP: Wer erhebt was, über welche Kanäle, und welche Qualitätssicherungsmaßnahmen sind eingebaut?
?
**Drei Datenquellen pro Patient:**
1. **Krankenakte** – Primärquelle für präoperative, intraoperative und initiale postoperative Variablen.
2. **Telefon-Kontakt** mit Patient:in oder Hausarzt – für Ereignisse innerhalb der **30-Tage-Frist** nach Entlassung.
3. **Chirurg** – fachliche Klärung bei unklaren Befunden.

**Zentrale Person: Datenerhebungskraft (DGK)** – speziell geschulte Pflegekraft, die *ausschließlich* der Datenerhebung gewidmet ist (nicht Stationspflege). Eine DGK pro Standort.

**Prozessfluss:** Daten → DGK → Datenfile → **Plausibilitätsfilter** → Abteilungsvergleiche / **Data Warehouse** → Risikoadjustierung + Outcome-Auswertung.

**Qualitätssicherungsmaßnahmen:**

| Element | Funktion |
|---|---|
| Schulung DGK | Standardisierte Anwendung exakter Variablendefinitionen |
| Plausibilitätsfilter | Auffangen von Eingabefehlern |
| **Inter-Rater-Reliability (IR-Reliability)** | Stichprobenartige Doppelerhebung als Auditkennzahl |
| Exakte Definitionen | Jede Variable hat eine operationale Definition (z. B. „Wundinfekt ≤ 30 Tage post-OP") |
| Jährliche Audits | Standortbezogene Datenqualitätsprüfung |
| 30-Tage-Scope | Erfassung auch nach Entlassung |

**Warum Krankenakte ≠ Verrechnungsdaten:** Krankenakte-basiertes NSQIP findet **+61 % mehr Komplikationen**, **+97 % mehr OP-Stelleninfektionen**, **+100 % mehr Harnwegsinfekte** als administrative Daten.

---

Was zeigen die VA-Ergebnisse 1991–2001 und Hall et al. 2009 als Wirksamkeitsbelege für NSQIP? Nennen Sie konkrete Zahlen.
?
**VA-Ergebnisse 1991–2001 (Folie 16):**

Während Volumen und Komplexität der OPs *unverändert* blieben und Risikoprofile der Patienten *unverändert* blieben:
- Postoperative **Mortalität: −27 %**
- Postoperative **Morbidität: −45 %**
- Mediane postoperative **Verweildauer: 9 → 4 Tage** (2 Tage weniger als im privaten Sektor im selben Zeitraum)
- Patientenzufriedenheit verbesserte sich.

→ Fazit der Folie: „Zuverlässige, verwertbare Daten waren von größter Bedeutung."

**Hall et al. *Ann Surg* 2009; 250:363–376 (Folien 20–24):**

Longitudinale Analyse über 3 Jahre (2005–2007), Outcome-Definition: Reduktion der risikoadjustierten O/E-Ratio.

*Bei 118 Spitälern (2006–2007):*
- **66 %** der Kliniken: signifikante **Mortalitätsreduktion** (mittlere O/E-Verbesserung: 0,174; P < 0,05)
- **82 %** der Kliniken: signifikante **Komplikationsraten-Reduktion** (mittlere O/E-Verbesserung: 0,114; P < 0,05)

*Bei 183 Kliniken (2007):*
- Geschätzt **~9.598 vermiedene Komplikationen** (≈ 52 pro Spital)
- **1/5 bis 1/10** aller Komplikationen konnten vermieden werden.

*Robustheit:* Verbesserungen unabhängig von Klinikgröße, Trägertyp (Uni/Schwerpunkt/privat/staatlich), Lage, Bettenanzahl. Auch **Top-Spitäler wurden besser** – spricht gegen Regression-to-the-Mean.

---

Was zeigt die österreichische Beobachtungsstudie (4 Jahre, 8 Kliniken)? Skizzieren Sie die wirtschaftliche Argumentation.
?
**Setting (Folie 26):** 4-jährige Beobachtungsstudie bei einem österreichischen Klinikträger; 8 Kliniken mit je einer chirurgischen Abteilung; risikoadjustiertes Benchmarking + regelmäßige Komplikations­besprechungen.

**Komplikationsraten-Entwicklung (Folie 28):**
- **2015/16 → 2018/19:** 10,24 % → 7,92 % (relative Reduktion ~22,7 %)

**Wirtschaftliche Argumentation:**

Schritt 1 – Komplikationen sind teuer (Folie 27, variable Kosten):
| OP-Typ | nicht-komplikativ | komplikativ | Faktor |
|---|---|---|---|
| Hernie | 251 € | 836 € | 3,3× |
| Galle | 1.371 € | 2.682 € | 2,0× |
| Colon | 2.678 € | 4.464 € | 1,7× |
| Prostata | 2.060 € | 5.040 € | 2,4× |

→ Komplikative Fälle kosten im Schnitt **ca. 3× so viel** wie nicht-komplikative.

Schritt 2 – weniger Komplikationen = kürzere Verweildauer (Folie 29):
- 6.502 Patienten, **−3.349,6 Belagstage**, Tagsatz: **500 €/Belagstag** (Ministeriumsauskunft)
- → Belagskosten-Einsparung: **~1,67 Mio. €**

Schritt 3 – Gesamteinsparung (Folie 30):
- **−1.084.274,7 € pro Jahr** (Gesamtkosten).

**Schlussfolgerung (Folie 31):** Transparenz ermöglicht es, Stärken auszubauen und schwierige Patientengruppen zu identifizieren; datengestützter KVP ist wirtschaftlich nachweisbar wirksam.

---

### Diskussion und Vergleich

Warum reicht eine M&M-Konferenz nicht als Qualitätssicherungs-Instrument, und was leistet NSQIP zusätzlich?
?
**M&M-Konferenz (Morbiditäts- und Mortalitätskonferenz):**
- Diskutiert *Einzelfälle* innerhalb *einer* Abteilung.
- Keine Risikoadjustierung → kaum Vergleichbarkeit.
- Kein systematisches 30-Tage-Follow-up → Ereignisse nach Entlassung fehlen.
- Kein standardisiertes Format → Dokumentation und Vollständigkeit variieren stark.
- Abhängig von Meldebereitschaft und Fehlerkultur der Abteilung.

**NSQIP ergänzt:**
- **Systemisch:** Benchmarking zwischen Häusern, nicht Einzelfall-Diskussion.
- **Risikoadjustiert:** O/E-Ratio macht faire Vergleiche möglich (Alter, ASA, Komorbiditäten).
- **Vollständig:** 30-Tage-Erfassung auch post-Entlassung via Telefon.
- **Datenbasis:** Krankenakte + IR-Reliability + Audit → klinisch valide, nicht nur administrativ.
- **Feedback-Mechanismus:** Halbjahresreport + Best-Practice-Recherche bei Ausreißern.

**Beide ergänzen sich:** M&M für tiefes fallbezogenes Verständnis (Warum ist es passiert?); NSQIP für systemische Trendüberwachung und Benchmarking (Wie gut sind wir im Vergleich?). Entspricht dem Zusammenspiel von Ishikawa/5-Warum (Einzelfall) und NSQIP (Population).

---

Warum ist die Risikoadjustierung der methodische Kernpunkt von NSQIP, und was passiert, wenn sie fehlt?
?
**Ohne Risikoadjustierung:**
- Krankenhäuser, die schwer kranke, alte, multimorbide Patienten behandeln, haben naturgemäß höhere Komplikations- und Mortalitätsraten.
- Eine reine Rangfolge nach absoluter Komplikationsrate bestraft Häuser für ihr Patientenkollektiv, nicht für ihre Qualität.
- Folie 14 belegt: Die Rangliste nach *unadjustierter* Mortalität hat **wenig Ähnlichkeit** mit der nach *adjustierter* Mortalität – Verschiebungen sind drastisch.

**Mit Risikoadjustierung:**
- Das Modell berechnet für jeden Patienten die *erwartete* Ereigniswahrscheinlichkeit auf Basis von ≥13 präoperativen Variablen (Alter, ASA, Albumin, BUN, Notfall-OP, Aszites, …).
- Die O/E-Ratio vergleicht dann: Wie viele Ereignisse hatte die Klinik *verglichen mit dem, was sie bei diesem Patientenkollektiv erwarten durfte*?
- Ergebnis: Kliniken mit komplexen Fällen können fair mit Kliniken mit einfachen Fällen verglichen werden.

**Verbindung zu Confounding (EBM-Vorlesung):** Risikoadjustierung ist die NSQIP-eigene Antwort auf Confounding – Alter und Komorbiditäten wären sonst Confounder, die das Programm nutzlos machen würden. Das logistische Regressionsmodell ist konzeptionell ähnlich wie die Stratifikation oder multivariate Adjustierung in observationalen Studien.

---

Warum ist NSQIP aus BPM-Perspektive relevant, und welche Schnittstellen zu anderen Vorlesungsinhalten gibt es?
?
**NSQIP als BPM-Instrument:**

NSQIP ist das empirische Fundament für prozessbasierte Qualitätsverbesserung in der Chirurgie. Es verbindet mehrere BPM-Konzepte:

| BPM-Konzept | NSQIP-Verbindung |
|---|---|
| **Prozess-KPIs / Kennzahlen** | O/E-Ratio als risikoadjustierte Outcome-Kennzahl |
| **PDCA-Zyklus** | Check (O/E-Report) → Act (KVP-Initiative) → Plan (Best Practice) → Do (Implementierung) |
| **Ishikawa / 5-Warum** | O/E > 1 → Ursachenanalyse auf Abteilungsebene |
| **Value-Based Care (Porter 2006)** | Value = Outcomes/Cost; NSQIP misst Outcomes und reduziert Komplikationskosten → verbessert Value direkt |
| **Komplikation als Outcome** | Davenport et al. NSQIP-Daten: Komplikationen erhöhen Mortalität (18,8× vs. 0,4 %) und Kosten → Reduktion ist BPM-Kernziel |
| **60-30-10 (Braithwaite)** | 30 % suboptimale Versorgung = NSQIP-Handlungsfeld |

**Warum Beobachtungsstudie statt RCT:**
Kein RCT möglich, bei dem eine Klinik randomisiert *kein* Qualitätsprogramm bekommt. Beobachtungsstudien mit konsistenten Effekten über Zeit, Häuser und Länder (VA, Hall et al., Österreich) sind die realistisch erreichbare Evidenzform → Evidenzklasse IIb–III, aber inhaltlich überzeugend.

---

### Mögliche Anschlussfragen des Prüfers

- Welches US-Gesetz hat NSQIP in der VA ausgelöst?
- Was ist die Aufgabe der DGK, und warum ist sie von der Stationspflege getrennt?
- Was bedeutet Inter-Rater-Reliability in diesem Kontext?
- Welche konkreten Prädiktoren nennt die Vorlesung für das Risikoadjustierungsmodell?
- Welche Mortalitätszahl ergibt das Folie-10-Beispiel?
- Wie viele Kliniken und welcher Zeitraum wurden bei Hall et al. analysiert?
- Was kostet ein Belagstag laut Ministeriumsauskunft in der österreichischen Studie?
- Was wäre die Entsprechung der O/E-Ratio in der EBM-Methodik?

---

## Eigene Notizen

*(Hier eigene Ergänzungen und Unsicherheiten eintragen)*
