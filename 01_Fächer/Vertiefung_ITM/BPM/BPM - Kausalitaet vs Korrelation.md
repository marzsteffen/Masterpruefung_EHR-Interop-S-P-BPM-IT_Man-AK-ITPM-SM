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

# BPM - Kausalität vs. Korrelation

> [!info] Kurzdefinition
> **Kausalität** beschreibt eine *Ursache-Wirkungs-Beziehung* (A bewirkt B). **Korrelation** beschreibt nur eine *statistische Wechselbeziehung* zwischen zwei Größen, die nicht kausal sein muss. „Korrelation impliziert keine Kausalität."

## Beschreibung

Folien 11–16.

### Kausalität (Folie 11)

> Kausalität (von lateinisch causa, „Ursache", und causalis, „ursächlich, kausal") ist die Beziehung zwischen Ursache und Wirkung. Demnach ist A die Ursache für die Wirkung B, wenn B von A herbeigeführt wird.

#### Drei Kausalitäts-Kriterien (Folie 11)

1. **Die „Ursache" und die „Wirkung" hängen zusammen** (Korrelation als notwendige, aber nicht hinreichende Bedingung).
2. **Die „Ursache" geht der „Wirkung" rechtzeitig voraus** (Zeitlichkeit).
3. **Es gibt keine plausiblen alternativen Erklärungen** für den beobachteten Effekt (Ausschluss von Bias, Confounding, Zufall – vgl. [[BPM - EBM - Ursachen einer Assoziation]]).

### Korrelation (Folien 12–14)

> Eine Korrelation beschreibt eine Beziehung zwischen zwei oder mehreren Merkmalen, Ereignissen, Zuständen oder Funktionen. Die Beziehung muss keine kausale Beziehung sein.

#### Eigenschaften

- **Stärke**: Maßzahlen liegen meist zwischen 0 (kein Zusammenhang) und 1 (starker Zusammenhang). Beispiel der Folie: Haar- und Augenfarbe von Studierenden ergibt einen korrigierten Kontingenzkoeffizienten von 0,55 → mittelstarker Zusammenhang.
- **Richtung**: positive Korrelation („mehr → mehr"; Beispiel: „mehr Futter, dickere Kühe") vs. negative / Antikorrelation („mehr → weniger"; Beispiel: „mehr gefahrene Strecke, weniger Treibstoff").
- **Sättigungsgrenzen**: Beispiel: mehr Gas → schneller, aber nicht über die technische Höchstgeschwindigkeit. In vielen wirtschaftlichen Korrelationen: steigende Grenzkosten, sinkender Grenznutzen.

### Korrelation vs. Kausalität – Beispiele (Folie 16)

| Beobachtung | Schein-Kausalität | Wahre Erklärung |
|---|---|---|
| Mehr Feuerwehrleute im Einsatz → mehr Brandschäden | „Feuerwehr verursacht Schäden" | Gemeinsame Ursache: **Größe des Brandes** (Confounder) |
| Längere Verweildauer im Krankenhaus → schlechterer Gesundheitszustand danach | „Krankenhaus macht krank" | Gemeinsame Ursache: **Schwere der Erkrankung** |

→ Beide Beispiele illustrieren Confounding (siehe [[BPM - Confounder - Definition]]).

## Bestandteile / Aufbau

| Größe | Korrelation | Kausalität |
|---|---|---|
| Notwendig | ja (Statistik) | ja (Korrelation) |
| Hinreichend | nein | nein – auch zeitliche Reihenfolge + Ausschluss Alternativen |
| Erklärt | Wechselbeziehung | Ursache-Wirkungs-Pfad |
| Aussage über Intervention | unsicher | begründet |

## Beispiel

NSQIP-Studie zeigt: Krankenhäuser mit hoher Komplikationsrate haben hohe Kosten. **Korrelation** offensichtlich. **Kausalität?** Mehrere mögliche Erklärungen:
- Komplikationen verursachen Kosten (kausal, plausibel; Davenport et al., siehe [[BPM - Komplikation - Definition]]).
- Hohe Kosten verursachen Komplikationen (umgekehrt – unplausibel).
- Beide werden durch die Patient:innen-Komplexität verursacht (Confounding).

Risikoadjustierung kontrolliert das Confounding und macht die kausale Aussage „Komplikationen → Kosten" tragfähiger.

## Abgrenzung

- **Korrelation ist notwendig, aber nicht hinreichend für Kausalität.** Ohne Korrelation keine Kausalität – ohne weitere Kriterien aber auch keine Kausalität.
- **Kausalität ≠ Determinismus.** Auch wenn A B bewirkt, kann der Effekt probabilistisch sein (z. B. Rauchen verursacht Lungenkrebs nicht in 100 % der Fälle, ist aber kausal).
- **Reverse Causation** (umgekehrte Kausalität) – im PDF nicht als eigener Begriff genannt, aber implizit im 2. Kausalitäts­kriterium (zeitliche Reihenfolge).

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche drei Kriterien müssen für Kausalität erfüllt sein?"

**Anwendungsfrage:** „Geben Sie ein klinisches Beispiel für eine starke Korrelation, die keine Kausalität ist." – Verweildauer/Mortalität (Confounder Schwere); langes Warten auf Hüft-OP/erhöhte Mortalität (siehe HTEP-Beispiel in [[BPM - Confounder - Definition]]).

**Diskussionsfrage:** Wie sichern wir den Übergang von Korrelation zu Kausalität in der medizinischen Forschung? – RCT als Goldstandard; bei Beobachtungsstudien Kausalitäts­kriterien nach Bradford-Hill (im PDF nicht erwähnt; bei Bedarf im mündlichen Gespräch).

**Mögliche Anschlussfragen:**
- Was bedeutet positive vs. negative Korrelation?
- Was ist eine Sättigungsgrenze?
- Wie hängt das mit Confounding zusammen?

## Verwandt

- [[BPM - EBM - Ursachen einer Assoziation]]
- [[BPM - Confounder - Definition]]
- [[BPM - Bias - Definition]]
- [[BPM - Studiendesign - RCT Goldstandard]]

## Quelle

- Vorlesung: [[BPM - VL - Evidenzbasierte Medizin]]
- Folien/Seitenangabe: Folien 11–16
- Externe Quelle laut Folien: Wikipedia
