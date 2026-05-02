---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - ACS-NSQIP]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - NSQIP - Risikoadjustierung

> [!info] Kurzdefinition
> **Risikoadjustierung** im NSQIP berechnet aus präoperativen Patientenfaktoren die *erwartete* Wahrscheinlichkeit eines unerwünschten Ereignisses (Mortalität, Komplikation). Damit lassen sich Krankenhäuser fair vergleichen, unabhängig vom Schweregrad der Patientenpopulation.

## Beschreibung

Folien 8–11.

### Warum Risikoadjustierung?

Folie 8: „Fairness mit Risikoadjustierung" – Krankenhäuser, die schwer kranke Patienten behandeln, hätten ohne Adjustierung schlechte Outcomes. Ein 75-jähriger multimorbider Patient hat *erwartungsgemäß* höhere Mortalitäts­wahrscheinlichkeit als ein gesunder 21-Jähriger; das Krankenhaus, das ihn behandelt, soll dafür nicht bestraft werden.

### Methodik: Stepwise-in/-out-Analyse (Folie 9)

Aus einem Pool potenzieller Prädiktoren werden statistisch die signifikanten ausgewählt. Aus den Folien benannte Prädiktor-Variablen:

- **Alter**
- **Geschlecht**
- **ASA-Klassifikation** (American Society of Anesthesiologists; im PDF nicht weiter erläutert)
- **BMI**
- **Anzahl weiße Blutkörperchen**
- **BUN** (Blood Urea Nitrogen / Harnstoff)
- **Hämatokrit**
- **Thrombozyten**
- **Albumin**
- **Komorbiditäten** (Diabetes, COPD, …)
- **Notfall-OP** (ja/nein)
- **Disseminierter Tumor** (ja/nein)
- **Aszites** (ja/nein)

### Ergebnis: Wahrscheinlichkeit eines Ereignisses

Folie 10 zeigt ein konkretes Beispiel:

Patient 74 Jahre, Albumin = 2.0 (3 SD unter Durchschnitt), ASA = 4, BUN = 102 (8 SD über Durchschnitt), Disseminierter Tumor = 0, Aszites = 1, Alter = 74, Notfall = 1.

→ **P(Tod) = 15 %** (Wahrscheinlichkeit der 30-Tage-Mortalität)

Diese „erwartete" Wahrscheinlichkeit fließt als **E (expected)** in die O/E-Ratio ein (siehe [[BPM - NSQIP - O-E-Ratio]]).

### Stabilität der Prädiktoren (Folie 11)

> Die Daten der VA haben statistisch gezeigt, dass Risikofaktoren von Jahr zu Jahr bemerkenswert stabil sind und eine ausgezeichnete prädiktive Validität aufweisen.

→ Die Modelle altern nicht schnell; Re-Kalibrierung ist möglich, aber nicht jährlich nötig.

## Bestandteile / Aufbau

```
Präoperative Variablen (≥ 13 Prädiktoren)
            │
            ▼
Stepwise-in/-out Selektion
            │
            ▼
Logistisches Regressionsmodell  →  P(Ereignis)
            │
            ▼
"Erwartetes" Outcome (E)
            │
            ▼
O/E-Ratio (Vergleich mit beobachtetem Outcome O)
```

## Beispiel

Krankenhaus A operiert vor allem ältere multimorbide Patient:innen, KH B vor allem junge gesunde. Ohne Adjustierung hätte A eine höhere Komplikationsrate – wirkt also schlechter. Mit Adjustierung wird die *erwartete* Komplikationsrate für die jeweiligen Patientenkollektive berechnet; bei A liegt sie höher als bei B. Die O/E-Ratio bringt beide auf vergleichbares Niveau.

## Abgrenzung

- **Risikoadjustierung ≠ Casemix-Adjustierung.** Casemix bezieht sich auf die Komplexität der OPs; Risikoadjustierung bezieht sich auf die Patient:innen-Eigenschaften. NSQIP nutzt **beides**.
- **Risikoadjustierung ≠ subjektives „die haben halt schwerere Fälle"-Argument.** Risikoadjustierung ist ein statistisch validiertes Modell, keine Entschuldigung.
- **ASA-Klassifikation** ist ein Eingabe­wert, kein Outcome – sie wird vom Anästhesisten präoperativ vergeben (im PDF nicht detailliert).

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was ist Risikoadjustierung im NSQIP-Kontext, und welche Variablen verwendet sie?"

**Anwendungsfrage:** „Berechnen Sie aus dem Beispielpatienten der Folie 10 die erwartete 30-Tage-Mortalität." – Antwort: 15 % (aus dem Modell).

**Diskussionsfrage:** Wenn Risikoadjustierung so wichtig ist – warum machen es nicht alle Qualitätsprogramme? – Aufwand der Datenerhebung, statistische Expertise, Modellpflege, Akzeptanz in der Klinik. Bezug zu [[BPM - NSQIP - Datenerhebung]].

**Mögliche Anschlussfragen:**
- Was ist Stepwise-in/-out?
- Wie alt sind die NSQIP-Modelle?
- Was bedeutet ASA?
- Wie hängt das Modell mit der O/E-Ratio zusammen?

## Verwandt

- [[BPM - NSQIP - Programm]]
- [[BPM - NSQIP - Datenerhebung]]
- [[BPM - NSQIP - O-E-Ratio]]
- [[BPM - Komplikation - Definition]]
- [[BPM - Methode - FMEA]]

## Quelle

- Vorlesung: [[BPM - VL - ACS-NSQIP]]
- Folien/Seitenangabe: Folien 8–11
- Folie 8 zitiert Shukri et al. Arch Surg 2002;137:20–27.
