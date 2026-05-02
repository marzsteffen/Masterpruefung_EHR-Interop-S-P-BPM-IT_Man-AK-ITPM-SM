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

# BPM - Confounder - Definition

> [!info] Kurzdefinition
> Ein **Confounder (Störfaktor)** ist eine dritte Variable, die *sowohl* Risikofaktor für den untersuchten Effekt ist *als auch* mit dem untersuchten Risikofaktor assoziiert ist – ohne dessen Folge zu sein. Confounder erzeugen eine **wahre, aber irreführende Assoziation**.

## Beschreibung

Folien 17, 23–24.

### Drei Kriterien (Folie 23)

Ein Faktor ist ein Confounder, wenn er gleichzeitig:

1. **einen Risikofaktor für den zu untersuchenden Effekt darstellt**,
2. **mit dem zu untersuchenden Risikofaktor assoziiert ist**, und
3. **mit dem zu untersuchenden Risikofaktor assoziiert ist, ohne dessen Folge zu sein** (also nicht in der Kausalkette zwischen Risikofaktor und Effekt liegt).

### Abgrenzung Bias ↔ Confounder (Folie 17, wörtlich)

> „BIAS CREATES AN ASSOCIATION THAT IS NOT TRUE BUT CONFOUNDER DESCRIBES AN ASSOCIATION THAT IS TRUE; BUT POTENTIALLY MISLEADING."

### Beispiel: Hüft-Total-Endoprothese (HTEP) und erhöhte Mortalität bei OP-Verzögerung (Folie 24)

Beobachtung: Patient:innen mit langem Warten auf HTEP haben höhere Mortalität.

| Variable | Rolle |
|---|---|
| **Untersuchter Risikofaktor** | langes Warten auf HTEP-OP |
| **Effekt** | hohe Mortalität |
| **Confounder** | Alter und schlechter Allgemeinzustand |

Logik: Alte und kranke Patient:innen müssen vor der OP **erst stabilisiert werden** → das verzögert die OP. Gleichzeitig verursachen Alter und Allgemeinzustand selbst eine erhöhte Mortalität. Die Beobachtung „Verzögerung → Mortalität" ist *wahr*, aber nicht *kausal*: nicht die Verzögerung tötet, sondern der Allgemeinzustand.

```
Alte und kranke Patient:innen
   │
   ├──→ Langes Warten auf HTEP (sie müssen stabilisiert werden)
   │
   └──→ Mortalität hoch
```

→ Würde man auf Basis dieser Beobachtung „schneller operieren" als Maßnahme, würde die Mortalität *nicht* sinken, weil der wahre Treiber unverändert bleibt.

### Methodische Konsequenz

Confounding kann **in der Analyse berücksichtigt werden** (Folie 23), z. B. durch:
- **Randomisierung** (siehe [[BPM - Confounder-Kontrolle - Methoden]]) – beste Methode, weil sie auch unbekannte Confounder kontrolliert.
- **Restriktion** (Einschluss­kriterien einengen).
- **Matching** (Paarbildung).
- **Stratifikation** (Analyse pro Subgruppe).
- Multivariate statistische Modelle (Regression mit Confounder als Covariate).

## Bestandteile / Aufbau

Confounding hat *drei* notwendige Bedingungen – fehlt eine, ist die Variable kein Confounder, sondern z. B. ein Effekt-Modulator oder ein Mediator.

```
RISIKOFAKTOR ───────→ EFFEKT
       ↑                ↑
       │                │
       └─── Confounder ─┘
```

## Beispiel

NSQIP nutzt Risikoadjustierung exakt, um Confounder zu kontrollieren: Alter, Komorbiditäten, ASA, BMI, Albumin etc. werden in das Erwartungs­modell aufgenommen, sodass die O/E-Ratio (siehe [[BPM - NSQIP - O-E-Ratio]]) eine fairere Vergleichbarkeit zwischen Krankenhäusern liefert.

## Abgrenzung

- **Confounder ≠ Mediator.** Mediator liegt *in der Kausalkette* zwischen Risikofaktor und Effekt; Confounder liegt *außerhalb*. Beispiel Mediator: Rauchen (Risikofaktor) → Atherosklerose (Mediator) → Herzinfarkt (Effekt). Atherosklerose darf nicht als „Confounder" kontrolliert werden, sonst verschwindet der echte Effekt.
- **Confounder ≠ Bias.** Confounder = wahre Drittvariable; Bias = systematischer Fehler in Daten oder Methode (vgl. [[BPM - Bias - Definition]]).
- **Confounder ≠ Effektmodulator.** Effektmodulator (= Interaktion) verändert die *Stärke* des Effekts in Subgruppen, ist aber nicht selbst Risikofaktor + assoziiert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche drei Kriterien definieren einen Confounder?"

**Anwendungsfrage:** „Erläutern Sie das HTEP-Beispiel der Vorlesung." – Alter und Allgemein­zustand als Confounder, der die scheinbare Kausalität zwischen Verzögerung und Mortalität erklärt.

**Diskussionsfrage:** Warum ist ein Confounder gefährlicher als ein offensichtlicher Bias? – Bias kann oft im Studiendesign erkannt werden; Confounding ist „eine wahre Beobachtung mit falscher Schluss­folgerung" – schwer zu durchschauen ohne explizite Modellierung.

**Mögliche Anschlussfragen:**
- Wie kontrolliert man Confounding in einer RCT?
- Wie unterscheidet sich Confounder vom Mediator?
- Was ist im HTEP-Beispiel der Confounder?

## Verwandt

- [[BPM - Bias - Definition]]
- [[BPM - EBM - Ursachen einer Assoziation]]
- [[BPM - Confounder-Kontrolle - Methoden]]
- [[BPM - Studiendesign - RCT Goldstandard]]
- [[BPM - NSQIP - Risikoadjustierung]]
- [[BPM - NSQIP - O-E-Ratio]]

## Quelle

- Vorlesung: [[BPM - VL - Evidenzbasierte Medizin]]
- Folien/Seitenangabe: Folien 17, 23–24
