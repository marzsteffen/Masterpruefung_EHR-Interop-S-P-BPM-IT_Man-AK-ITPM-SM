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

# BPM - Confounder-Kontrolle - Methoden

> [!info] Kurzdefinition
> **Vier Methoden** zur Kontrolle von Confoundern in Studien: **Randomisierung**, **Restriktion**, **Matching**, **Stratifikation**. Jede hat eigene Vor- und Nachteile; Randomisierung ist die wirksamste, weil sie auch unbekannte Confounder kontrolliert.

## Beschreibung

Folien 25–30.

### 1. Randomisierung (Folien 25–26)

- **Randomisierung ist die optimale Methode, Confounder zu kontrollieren.**
- Bekannte (messbare) *und* unbekannte (nicht-messbare) Einflussfaktoren werden zwischen Kontroll- und Interventionsgruppe verteilt.
- Unsicherheit, ob beobachtete Zusammenhänge beeinflusst wurden, verringert sich.
- Die Wahrscheinlichkeit, dass alle Einflussfaktoren gut ausbalanciert sind, **steigt mit der Sample-Größe**.
- Vorteil ggü. willkürlicher Zuteilung: Der potenzielle Einfluss subjektiver Auswahl ist geringer.
- Faustregel: Ab ~200 Teilnehmer:innen ist die Chance auf gute Balance hoch.

→ Randomisierung ist Bestandteil der RCT (siehe [[BPM - Studiendesign - RCT Goldstandard]]).

### 2. Restriktion (Folien 27–28)

- Bei observationalen Studien einsetzbar.
- Einfach durchzuführen und zu verstehen.
- **Anpassung der Einschluss­kriterien** schränkt die Studienpopulation ein und eliminiert so den Einfluss bekannter Störfaktoren.
- Beispiel: Einschluss nur von Nichtrauchern unter 60 Jahren → Einfluss von Rauchen und hohem Alter eliminiert.

**Nachteile:**
- **Externe Validität sinkt** (Generalisierbarkeit), Vgl. [[BPM - Validitaet - Interne vs Externe]].
- Anzahl geeigneter Kandidat:innen für die Studie wird reduziert.
- Restringierte Variablen können nicht mehr untersucht werden.
- → **Nur bei von vornherein bekannten starken Einflussfaktoren einsetzen.**
- **CAVE**: Nicht alle Confounder sind bekannt.

### 3. Matching (Folie 29)

- „Paarbildung": Fälle und Kontrollen werden in passende Zweiergruppen eingeteilt, bezogen auf einen bestimmten Confounder.
- **Vorteil**: Einzelne Confounder können komplett ausgeschaltet werden.
- **Nachteile**:
  - **Overmatching-Gefahr** (zu enges Matching eliminiert auch echte Effekte).
  - Die Studienpopulation entspricht nicht mehr der realen Situation.

### 4. Stratifikation (Folie 30)

- Analyse des Effekts in einzelnen **Schichten der Confounder-Variable**.
- **Vorteile**:
  - Intensiver Überblick über die Daten.
  - Eignet sich auch zur Identifikation von **Effekt­modulation** (Interaktion).
- **Nachteil**:
  - Impraktikabel zur Untersuchung multifaktoriell bedingter Problem­stellungen, bei denen viele potenzielle Confounder oder Risikofaktoren berücksichtigt werden müssen.

### Vergleichstabelle

| Methode | Zeitpunkt | Bekannte Confounder | Unbekannte Confounder | Externe Validität |
|---|---|---|---|---|
| **Randomisierung** | a priori (Studiendesign) | ✓ | ✓ | hoch |
| **Restriktion** | a priori | ✓ (eliminiert) | ✗ | sinkt deutlich |
| **Matching** | a priori | ✓ (kontrolliert) | ✗ | sinkt |
| **Stratifikation** | a posteriori (Analyse) | ✓ (kontrolliert) | ✗ | erhalten |

## Bestandteile / Aufbau

```
Confounder erkannt → Methodenwahl:
  ├── RCT möglich → RANDOMISIERUNG (1. Wahl)
  └── observational  
        ├── starker bekannter Confounder → RESTRIKTION (Einschlusskrit.)
        ├── einzelner Confounder, paargenau → MATCHING
        └── mehrere bekannte Confounder, Subgruppen-Effekte → STRATIFIKATION
```

In der Praxis kombiniert: Ein RCT plus multivariate Regression in der Analyse, z. B.

## Beispiel

NSQIP arbeitet mit observationalen Daten – kein RCT möglich. Zur Confounder-Kontrolle:
- **Restriktion** ist begrenzt einsetzbar (würde Generalisierbarkeit verlieren).
- **Matching** und **Stratifikation** kommen in einzelnen Auswertungen vor.
- Hauptmethode: **multivariate Regression** mit Risikofaktoren als Covariaten – diese Form der „statistischen Adjustierung" wird in der Folien-Reihe nicht als eigene 5. Methode benannt, ergibt sich aber implizit aus der Risikoadjustierung (siehe [[BPM - NSQIP - Risikoadjustierung]] und [[BPM - NSQIP - O-E-Ratio]]).

## Abgrenzung

- **Randomisierung ≠ willkürliche Zuteilung.** Willkür hat den Bias der zuteilenden Person; Randomisierung ist statistisch unparteiisch.
- **Restriktion ≠ Einschluss­krit­erien generell.** Restriktion ist die *gezielte* Eliminierung eines bekannten Confounders; reguläre Ein-/Ausschlusskriterien dienen zusätzlich der Sicherheit, Praktikabilität, Indikation.
- **Matching ≠ Stratifikation.** Matching ist 1:1 (oder n:1) auf Probandenebene; Stratifikation ist die analytische Schichtung *nach* der Studie.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche vier Methoden zur Kontrolle von Confoundern lehrt die Vorlesung?"

**Anwendungsfrage:** „Welche Methode wählen Sie, wenn Sie observational forschen und einen einzelnen, sehr starken Confounder kontrollieren wollen?" – Matching oder Restriktion, je nach Ziel.

**Diskussionsfrage:** Warum kontrolliert nur Randomisierung *unbekannte* Confounder? – Randomisierung verteilt zufällig, also auch Faktoren, die der/die Forscher:in gar nicht kennt. Die anderen drei Methoden setzen Vorwissen über den Confounder voraus.

**Mögliche Anschlussfragen:**
- Was ist Overmatching?
- Wann ist Restriktion sinnvoll, wann gefährlich?
- Wie hängt Stratifikation mit Effektmodulation zusammen?

## Verwandt

- [[BPM - Confounder - Definition]]
- [[BPM - Bias - Definition]]
- [[BPM - Studiendesign - RCT Goldstandard]]
- [[BPM - Validitaet - Interne vs Externe]]
- [[BPM - NSQIP - Risikoadjustierung]]

## Quelle

- Vorlesung: [[BPM - VL - Evidenzbasierte Medizin]]
- Folien/Seitenangabe: Folien 25–30
