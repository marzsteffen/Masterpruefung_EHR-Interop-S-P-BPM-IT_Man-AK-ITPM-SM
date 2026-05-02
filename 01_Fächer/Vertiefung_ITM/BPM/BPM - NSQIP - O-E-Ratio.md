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

# BPM - NSQIP - O/E-Ratio (Observed vs. Expected)

> [!info] Kurzdefinition
> Die **O/E-Ratio** (Observed-vs-Expected-Ratio) ist die zentrale Steuerungs­kennzahl von NSQIP. **O** = Anzahl beobachteter postoperativer Ereignisse, **E** = Anzahl erwarteter Ereignisse aus dem Risikoadjustierungs­modell. **O/E < 1** = besser als erwartet, **O/E > 1** = schlechter als erwartet.

## Beschreibung

Folie 12 (Definition) und Folie 14 (Wirkung der Adjustierung).

### Definition

Die Folie nutzt eine Golfplatz-Analogie:

> Stellen Sie sich ein O/E-Verhältnis als Par auf einem Golfplatz vor – die erwartete Punktzahl. Ein O/E-Verhältnis ist ein mathematisches Konstrukt, das das risikoadjustierte Ergebnis für einen bestimmten Klinik-Standort genau anzeigt.

| Größe | Bedeutung |
|---|---|
| **O** | Gesamtzahl der **beobachteten** postoperativen Ereignisse (Todesfälle oder Komplikationen) |
| **E** | Anzahl der **erwarteten** Ereignisse, basierend auf präoperativem Risiko und anderen Faktoren in einer bestimmten Patientenpopulation |

### Interpretation

- **O/E < 1** → Klinik-Standort erbringt eine **bessere Leistung als erwartet** (besser als Par).
- **O/E > 1** → Klinik-Standort hat einen **signifikanten Überschuss an unerwünschten Ereignissen** (schlechter als Par).
- **O/E = 1** → erwartungsgerechte Leistung.

### Wirkung der Risikoadjustierung auf Rangfolgen (Folie 14)

Die Folie zeigt explizit: Die Rangliste der Krankenhäuser nach **unadjustierter** 30-Tage-Mortalität hat wenig Ähnlichkeit mit der Rangliste nach **adjustierter** Mortalität. Verschiebungen sind drastisch – Häuser, die unadjustiert gut wirken, können adjustiert mittelmäßig oder schlecht sein und umgekehrt.

> „Risikoadjustierung hat einen tiefgreifenden Einfluss auf die tatsächliche Leistung eines medizinischen Zentrums – im Vergleich zu anderen."

### Statistische Ausreißer

Folie 13 markiert in der „General Surgery O/E Ratios for Morbidity"-Darstellung **statistisch signifikante Ausreißer nach unten** mit „#" – das ist der Punkt, wo Best-Practice-Recherche und KVP-Ansatz im Programm konkret werden.

### Halbjahresreport (Folie 17)

Risk-adjusted semiannual NSQIP report für alle Komplikationen über alle Spitäler – jedes Spital wird mit Pfeil in der Gesamtgruppe verortet, wodurch die eigene Position im Benchmark sichtbar wird.

## Bestandteile / Aufbau

```
O = Σ beobachtete Ereignisse
E = Σ erwartete Ereignisse (aus Risikoadjustierungs-Modell)
─────────────────────────────────
O/E = O / E

   < 1 → besser als erwartet
   = 1 → erwartungsgerecht
   > 1 → schlechter als erwartet
```

## Beispiel

Klinik mit 100 Hernien-OPs. 5 Komplikationen beobachtet (O = 5). Aus Risikoadjustierungsmodell: 7 Komplikationen erwartet (E = 7). → O/E = 5/7 ≈ 0,71 → besser als erwartet.

Bei 9 beobachteten Komplikationen wäre O/E = 9/7 ≈ 1,29 → schlechter als erwartet → Trigger für Ursachenanalyse (vgl. [[BPM - Methode - Ishikawa 7M]]).

## Abgrenzung

- **O/E ≠ absolute Komplikationsrate.** Die absolute Rate (z. B. 5 %) sagt ohne Casemix-Bezug wenig aus.
- **O/E ≠ SMR** (Standardized Mortality Ratio) im engeren Sinne, ist aber eng verwandt – SMR ist eine spezifische Form der O/E-Ratio für Mortalität.
- **O/E < 1 ist nicht automatisch „gut".** Das Modell kann Variablen übersehen, die in einem speziellen Klinik-Profil das Risiko unterschätzen lassen. Statistische Signifikanz (Konfidenz­intervalle) ist mitzubedenken.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was ist die O/E-Ratio im NSQIP-Kontext, und wie interpretiert man sie?"

**Anwendungsfrage:** „Eine Klinik hat O/E = 1,4 für postoperative Pneumonien. Was bedeutet das, und welche Maßnahme ergibt sich?" – 40 % mehr Pneumonien als erwartet → Ursachenanalyse, evtl. Anlehnung an Best-Practice-Studien wie [[BPM - Paper - The Power of NSQIP Pneumonia]].

**Diskussionsfrage:** Warum ist die Golfplatz-Analogie didaktisch wirksam? – Sie macht das Konzept der „erwartungsbereinigten" Leistung intuitiv: Es ist nicht peinlich, ein Par-72-Loch in 72 Schlägen zu beenden – peinlich ist nur, schlechter als der Par zu sein.

**Mögliche Anschlussfragen:**
- Was bedeutet O/E < 1 genau?
- Wie verändern Risikoadjustierungen die Rangfolge?
- Wann ist eine O/E-Ratio statistisch signifikant?
- Wie wird der „Ausreißer nach unten" gefunden und genutzt?

## Verwandt

- [[BPM - NSQIP - Risikoadjustierung]]
- [[BPM - NSQIP - Programm]]
- [[BPM - NSQIP - Wirksamkeit Hall et al]]
- [[BPM - Methode - Ishikawa 7M]]
- [[BPM - Prozess-Kennzahlen]]

## Quelle

- Vorlesung: [[BPM - VL - ACS-NSQIP]]
- Folien/Seitenangabe: Folien 12 (Definition), 13 (Ausreißer), 14 (Verschiebung der Rangliste), 17 (Halbjahresreport)
