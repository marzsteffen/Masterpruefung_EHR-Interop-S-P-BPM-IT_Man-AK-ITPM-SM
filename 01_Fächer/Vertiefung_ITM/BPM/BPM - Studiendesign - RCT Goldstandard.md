---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Evidenzbasierte Medizin]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - Studiendesign - RCT als Goldstandard

> [!info] Kurzdefinition
> Der **Randomised Controlled Trial (RCT)** ist der **Goldstandard** experimenteller medizinischer Forschung. Drei Qualitätsmerkmale definieren ihn: **Kontrollgruppe**, **Randomisierung**, **Verblindung**. Hinzu kommt die **statistische Auswertung** mit kontrollierter Irrtums­wahrscheinlichkeit.

## Beschreibung

Folien 32, 38, 40–42.

### Experimentelle Designs (Folie 33, wörtlich)

> Experimentelle Forschungsdesigns prüfen eine Hypothese, indem sie die unabhängige Variable gezielt manipulieren und den Einfluss von Störgrößen durch Konstanthaltung der Versuchs­bedingungen, Elimination, Randomisierung oder Parallelisierung kontrollieren.

### Wie wird Wirksamkeit nachgewiesen? (Folie 38)

Um die Wirksamkeit einer Intervention festzustellen, braucht man:
- eine **Interventionsgruppe** und eine **Kontrollgruppe**,
- eine **Gruppenzuordnung nach dem Zufallsprinzip**.

> Ausschließlich randomisierte Vergleichsstudien gewährleisten, dass sich die beiden Gruppen nur hinsichtlich der Intervention unterscheiden und somit ein Effekt der Intervention zuzuschreiben ist. Nicht randomisierte Studien überschätzen oft die Wirksamkeit einer Intervention.

### Drei Qualitätsmerkmale (Folie 40)

| Merkmal | Funktion |
|---|---|
| **Kontrollgruppe** | Vergleichsmaßstab; ohne Kontrolle keine Effektaussage. |
| **Randomisierung** | Zufällige Zuordnung der Beobachtungs­einheiten auf Gruppen → Confounder-Kontrolle (auch unbekannte). |
| **Verblindung** | Schutz vor Bias durch Erwartungs­änderung von Patient:in (einfach blind), Behandelnden (doppelblind) oder Auswertenden (dreifach blind). Im PDF benannt, nicht ausführlich definiert. |

Plus: **Statistische Auswertung** mit Irrtumswahrscheinlichkeit (p-Werte, Konfidenzintervalle).

### Goldstandard

> „Golden Standard": Randomisierte, kontrollierte und doppelblinde Studie (Randomised Controlled Trial – RCT).

### Wirksamkeit der Randomisierung (Folie 42)

Beispiel **Ioannidis et al. 2001**: Auswahl von 45 Themenbereichen, in denen sowohl nicht-randomisierte als auch randomisierte Studien existierten (gesamt 408 inkludierte Studien). Behandlungseffekt bei nicht-randomisierten Studien „überzufällig" größer:

- Bei **60 %** wurde der Effekt **um 50 % überschätzt**.
- Bei **einem Drittel** wurde der Effekt **um mehr als 200 % überschätzt**.

→ Belegt empirisch, warum Randomisierung methodisch unverzichtbar ist.

### Randomisierung als Confounder-Kontrolle (Folie 41)

> Einzige Methode um Effekte von Störgrößen, welche unbekannt sind oder nicht durch Blockierung eliminiert werden können, auszuschalten.

## Bestandteile / Aufbau

```
RCT-Goldstandard
├── Kontrollgruppe          (gegen "vorher/nachher" allein)
├── Randomisierung          (gegen Confounder)
├── Verblindung (doppelblind)  (gegen Bias)
└── Statistische Auswertung (gegen Zufall)
```

Damit adressiert das RCT-Design **alle drei nicht-kausalen Erklärungen** einer Assoziation aus [[BPM - EBM - Ursachen einer Assoziation]] (Bias, Confounding, Zufall).

## Beispiel

Hypothese: „Mesh-Reparatur ist besser als Naht-Reparatur bei Inguinalhernie." 
- Kontrollgruppe: Naht-Reparatur.
- Randomisierung: Patient:innen werden zufällig zugeteilt.
- Doppelblindung: bei chirurgischen Studien schwer (Operateur:in weiß, was sie tut), aber Outcome-Bewerter:innen können verblindet werden.
- Auswertung: Konfidenz­intervall für die Differenz der Rezidivraten.

→ Ergibt eine Klasse-Ib-Studie ([[BPM - Evidenzklassen - AHRQ]]).

## Abgrenzung

- **RCT ≠ Beobachtungsstudie.** Beobachtung erfolgt ohne Manipulation (Kohorten, Fall-Kontroll, Querschnitt) – RCT manipuliert die unabhängige Variable.
- **RCT ≠ Quasi-Experiment.** Quasi-Experimente haben Kontrollgruppe ohne Randomisierung – methodisch schwächer.
- **Goldstandard ≠ einzig zulässige Studienform.** Manche Fragestellungen lassen sich ethisch oder logistisch nicht im RCT untersuchen (z. B. Wirkung des Rauchens auf Lungenkrebs – RCT wäre unethisch). Dann gilt: Beobachtungsstudie + Risikoadjustierung + Kausalitäts­kriterien.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche drei Qualitätsmerkmale machen den RCT zum Goldstandard?"

**Anwendungsfrage:** „Was zeigt Ioannidis et al. 2001, und was lernen wir daraus für Pfade?" – Nicht-randomisierte Studien überschätzen Effekte; Pfade dürfen nur auf solider, am besten RCT-basierter Evidenz aufbauen.

**Diskussionsfrage:** Wann ist RCT *nicht* der richtige Studientyp? – chirurgische Innovationen mit langer Lernkurve; ethisch problematische Eingriffe (Schein-OP); seltene Erkrankungen (zu wenig Probanden); Implementierungs-Fragen (wo Beobachtungsstudie und Process Mining geeigneter sind).

**Mögliche Anschlussfragen:**
- Welche drei Bedrohungen werden durch die drei Qualitätsmerkmale jeweils adressiert?
- Was ist der Unterschied zwischen einfacher und doppelter Verblindung?
- Wie groß war die Effekt-Überschätzung in Ioannidis 2001?

## Verwandt

- [[BPM - EBM - Ursachen einer Assoziation]]
- [[BPM - Confounder-Kontrolle - Methoden]]
- [[BPM - Bias - Definition]]
- [[BPM - Evidenzklassen - AHRQ]]
- [[BPM - Studiendesign - Endpunkt]]
- [[BPM - Validitaet - Interne vs Externe]]

## Quelle

- Vorlesung: [[BPM - VL - Evidenzbasierte Medizin]]
- Folien/Seitenangabe: Folien 32, 33, 38, 40–42
- Externe Quelle laut Folien: Ioannidis JPA et al. (2001) – Effekt-Überschätzung in nicht-randomisierten Studien.
