---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Informationssicherheits-Risikomanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Risikomanagement - Risikobewertung (Qualitativ vs. Quantitativ)

> [!info] Kurzdefinition
> Risikobewertung zerlegt das Risiko in Eintrittswahrscheinlichkeit und Auswirkung und kombiniert beide. Zwei Methodengruppen: qualitativ (Ordinalskalen, Matrizen) und quantitativ (metrische Skalen, finanzieller Schaden × Frequenz pro Jahr, Konfidenzintervalle).

## Beschreibung

### Analyse eines Risikos (Folie 37)

**Drei-Schritt-Vorgehen:**
1. **Zerlegung** des Risikos.
2. **Bewertung der einzelnen Faktoren.**
3. **Berechnung des Risikos.**

**Risiko-Zerlegung:**
```
Risiko = Ungewissheit × (negative) Auswirkung
       = "Passiert es, und wie oft?" × "Welcher Schaden entsteht, wenn es passiert?"
```

Vorteile der Zerlegung:
- Leichtere Einschätzung.
- Ableitung aus vorhandenen Daten möglich.
- Weitere Zerlegung möglich (z. B. Wahrscheinlichkeit in Ereigniseintritt × Folgewahrscheinlichkeit).

### Qualitative Methoden (Folien 38–39)

- Faktoren auf **Ordinalskalen**.
- Beispiel-Skalen: verbal („niedrig"/„mittel"/„hoch") oder Farben (grün/gelb/rot).
- Berechnung über Matrizen oder einfache „Formeln" wie „Risiko = Auswirkung × Wahrscheinlichkeit".
- Eignen sich zur Einschätzung **schwer quantifizierbarer Risiken**.

**Vorteile:** Intuitiv verständlich; leicht zu erklären; hoher Bekanntheitsgrad; bessere Bewertung schwer quantifizierbarer Risiken; Interviews/Fokusgruppen/Expertenbewertungen ermöglichen die Einbeziehung persönlicher Erfahrungen.

**Nachteile:** Verwendung fehlerhafter Matrizen; anfällig für Fehler in der Festlegung der Kategorien/Wertebereiche; wenig Aussagekraft, wenn sich Risiken das gleiche Feld teilen; keine empirische Basis.

### Quantitative Methoden (Folien 40–43)

- Faktoren auf **metrischen Skalen**.
- Beispiel: Eintrittswahrscheinlichkeit in Prozent oder Häufigkeit pro Jahr; Schaden in Euro pro Vorfall.
- **Fokus:** Berechnung von **finanziellen Schäden**.
- Möglicher Vergleich von **Kosten und Nutzen** von Sicherheitsmaßnahmen (einfachere Messbarkeit der Effektivität, einfachere Priorisierung).
- Berücksichtigung statistischer Daten und historischer Trends.
- Werkzeuge: z. B. **CRISAM**.
- **Konfidenzintervalle** zur Abbildung von Unsicherheiten („90 % Konfidenzniveau – der Schaden wird zwischen 5.000 und 70.000 Euro liegen").

**Vorteile:** belastbare Ergebnisse, saubere Differenzierung auch bei kleinen Unterschieden, kontrollierte Subjektivität, ermöglicht Ableitung sinnvoller Investitionen, Erwartungswerte = Rückstellungen, kann Verteilungsfunktionen abbilden.

**Nachteile:** höhere Komplexität (statistische Methoden) erfordert Werkzeuge, nicht mehr im Kopf oder auf Papier abbildbar; erklärungs- und verständnisbedürftig.

### Beispielabschätzung quantitativ (Folie 42)

| Bedrohung | Schaden | Frequenz/Jahr | Schaden/Ereignis | Schaden/Jahr |
|---|---|---|---|---|
| DDoS-Angriff | Verfügbarkeit | 1,50 | 15.000 € | 22.500 € |
| SQL-Injection | Data Breach | 0,40 | 60.000 € | 24.000 € |
| Bösartiger Insider | Data Breach | 0,10 | 150.000 € | 15.000 € |
| Brand im RZ | Datenverlust, Verfügbarkeit | 0,05 | 250.000 € | 12.500 € |
| Fehler im Algorithmus | Kundenzufriedenheit | 0,20 | 100.000 € | 20.000 € |

## Bestandteile / Aufbau

| Aspekt | Qualitativ | Quantitativ |
|---|---|---|
| Skala | Ordinal (verbal/farbig) | metrisch (Prozent, Euro) |
| Berechnung | Matrix oder einfache Formel | Erwartungswert × Schaden |
| Tooling | Papier/Tabelle | Tools wie CRISAM |
| Stärke | intuitiv, schwer quantifizierbare Risiken | belastbar, Kosten-Nutzen |
| Schwäche | subjektiv, unscharf | komplex, erklärungsbedürftig |

## Beispiel

Aus Folie 42: DDoS-Angriff: Frequenz 1,5 pro Jahr, Schaden 15.000 € pro Ereignis → erwarteter Jahresschaden 22.500 €. Diese Zahl lässt sich gegen die Kosten einer DDoS-Schutz-Maßnahme abwägen.

## Abgrenzung

- **Qualitative ↔ Quantitative Methoden** schließen einander nicht aus. In der Praxis werden sie oft kombiniert (z. B. qualitativ in der Erstbewertung, quantitativ für die wichtigsten Risiken).
- **Risikobewertung ≠ Risikoevaluierung:** Bewertung berechnet die Höhe; Evaluierung vergleicht mit Akzeptanzkriterien (siehe [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie wird ein Risiko zerlegt und bewertet? Welche zwei Methodengruppen gibt es?

**Anwendungsfrage:** Berechnen Sie den erwarteten Jahresschaden für einen Vorfall mit Frequenz 0,4/Jahr und Schaden 60.000 €. (= 24.000 €.) Welche Methode (qualitativ/quantitativ) eignet sich besser für ein Krankenhaus, und warum?

**Diskussionsfrage:** Welche Schwächen hat eine rein quantitative Methode bei Risiken für Leib und Leben? (Wert eines Menschenlebens lässt sich kaum sinnvoll monetarisieren; ethische Fragen.) Welche Trade-offs entstehen zwischen den Methoden?

**Mögliche Anschlussfragen:**
- Was sind Konfidenzintervalle, und welche Aussage treffen sie?
- Welches Tool wird in der Vorlesung als Beispiel genannt? (CRISAM.)
- Wie hängt die Risikobewertung mit der Risikomatrix zusammen?

## Verwandt

- [[ASP - Risikomanagement - Risikomatrix]]
- [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]
- [[ASP - Risikomanagement - Risikobehandlung]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 37–43
