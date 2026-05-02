---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - SWOT-Analyse

> [!info] Kurzdefinition
> Die SWOT-Analyse ist ein strategisches Tool zur Bewertung der internen Stärken (Strengths) und Schwächen (Weaknesses) sowie der externen Chancen (Opportunities) und Risiken (Threats) eines Unternehmens. Im Foliensatz wird sie als Hilfsmethode bei CSI-Schritt 3 („Wo wollen wir hin?") eingeführt — am Beispiel Tesla.

## Beschreibung

Die SWOT-Analyse wird in den Folien 116–117 mit dem Beispiel Tesla illustriert. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019) — Eingebettet in das CSI-Kapitel, daher als Hilfsmethode bei CSI-Schritt 3 zu verstehen.

**Vier Quadranten** (Folie 116):

|  | Intern | Intern |
|---|---|---|
| | **S — Strengths (Stärken)** | **W — Weaknesses (Schwächen)** |
| Tesla-Beispiele | Starke Marke und Marktführer im Bereich der E-Autos · Akkukapazität · Reichweite der Autos · Ladeinfrastruktur | Fehlendes Händlernetz · Servicequalität · Produktionsprobleme und Lieferprobleme · Elon Musk als Führungsfigur |
|  | **O — Opportunities (Chancen)** | **T — Threats (Risiken)** |
|  | Markt für E-Autos wird stark wachsen · Steigendes Umweltbewusstsein bei Konsumenten · Loyale Fanbase | Investoren: Tesla verdient zu wenig Geld · Öffentliche Wahrnehmung von Reichweite und Akkukapazität falsch · Fehlende Recyclingstrategien für Batterien |

**Strategische Kombinationen** (Folie 117):

- **S–O (Stärken in Kombination mit Chancen):** Ausbau der Ladeinfrastruktur, um stark wachsenden Markt zu nutzen · Forschung im Bereich umweltfreundlicher Technologien · Akkukapazität und Reichweite stärker kommunizieren.
- **W–O (Schwächen in Kombination mit Chancen):** Kooperationen mit Servicepartnern · Verbesserung der Produktions-/Distributionsprozesse, um steigende Nachfrage bewältigen zu können.
- **S–T (Stärken in Kombination mit Risiken):** Lösung des Recycling-Problems · Entwicklung umweltfreundlicherer Batterien · Erhöhung der Reichweite · Starke Marke nutzen, um öffentliche Wahrnehmung zu verbessern.
- **W–T (Schwächen in Kombination mit Risiken):** Rasch in die Gewinnzone kommen, um Investoren zu beruhigen · Führungsstil ändern, um hoher Fluktuation entgegenzutreten.

## Bestandteile / Aufbau

| Quadrant | Inhalt |
|---|---|
| Stärken (intern) | Vorteile, die das Unternehmen hat |
| Schwächen (intern) | Schwachpunkte des Unternehmens |
| Chancen (extern) | Marktentwicklungen, die genutzt werden können |
| Risiken (extern) | Externe Bedrohungen |

**Strategische Kombinationen:**
- **SO** — wie Stärken nutzen, um Chancen zu ergreifen?
- **WO** — wie Schwächen abbauen, um Chancen zu ergreifen?
- **ST** — wie Stärken nutzen, um Risiken abzufangen?
- **WT** — wie Schwächen abbauen, um Risiken zu reduzieren?

## Beispiel

Tesla-Beispiel oben (laut Folien 116–117). Aus Krankenhaus-IT-Sicht (eigenes Beispiel, *im PDF nicht ausgearbeitet*):

| Quadrant | Beispiel |
|---|---|
| Stärken | Eigene FHIR-Kompetenz, gute Vernetzung zur Pflege, modernes KIS |
| Schwächen | Personalengpass, veraltete Cybersecurity, kein Self-Service |
| Chancen | ELGA-Verpflichtung, Telemedizin-Markt, Digitalisierungsförderung |
| Risiken | Cyberangriff, Fachkräftemangel, regulatorische Verschärfungen (DSGVO) |

## Abgrenzung

- **SWOT vs. PESTEL** (siehe [[SM - PESTEL-Analyse]]): PESTEL ist Makroumfeld-Analyse; SWOT ist konkret unternehmensbezogen. PESTEL-Outputs liefern oft Inputs für O/T in der SWOT.
- **SWOT vs. GAP-Analyse**: GAP-Analyse vergleicht Soll vs. Ist konkret; SWOT ist breitere strategische Analyse.
- **SWOT in CSI**: Wird in Schritt 3 („Wo wollen wir hin?") als Hilfsmethode eingesetzt — siehe [[SM - ITIL Continual Improvement - Modell]].

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet SWOT? — Strengths/Stärken (intern), Weaknesses/Schwächen (intern), Opportunities/Chancen (extern), Threats/Risiken (extern).

**Anwendungsfrage:** Skizzieren Sie eine SWOT-Analyse für ein Krankenhaus-IT-Vorhaben „Telemedizin-Plattform einführen". Welche Strategien folgen aus den vier Kombinationen (SO, WO, ST, WT)?

**Diskussionsfrage:** Welche typischen Fehler werden bei einer SWOT gemacht? — Verwechselung intern/extern (z. B. „Marktwachstum" als Stärke); zu allgemein formuliert; keine Ableitung strategischer Konsequenzen aus den Kombinationen.

**Mögliche Anschlussfragen:**
- Wie hängen SWOT und PESTEL zusammen?
- Wie lassen sich Outputs der SWOT in CSI-Aktionen überführen? — Über Schritt 4 (Verbesserungsplan).
- Welche der vier Strategien (SO, WO, ST, WT) ist defensiv, welche offensiv? — SO offensiv (Wachstum), WT defensiv (Schadensbegrenzung), WO und ST sind „Brückenstrategien".

## Verwandt

- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - PESTEL-Analyse]]
- [[SM - CMMI - Reifegradmodell]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 116–117 (Tesla-Beispiel als Exkurs in CSI-Schritt 3); Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
