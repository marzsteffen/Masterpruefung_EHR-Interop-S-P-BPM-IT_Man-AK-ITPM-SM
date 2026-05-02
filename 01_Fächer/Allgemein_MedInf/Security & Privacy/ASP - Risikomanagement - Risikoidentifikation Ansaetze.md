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

# ASP - Risikomanagement - Risikoidentifikation: Ereignis-basiert vs. Asset-basiert

> [!info] Kurzdefinition
> Zwei methodische Ansätze zur Identifikation von Risiken: ereignis-basiert (top-down, übergeordnete Szenarien) oder asset-basiert (bottom-up, einzelne Assets). Beide leiten in dieselbe Risikobewertung und -behandlung über.

## Beschreibung

Folie 17 stellt die zwei Ansätze gegenüber.

### Ereignis-basierter Ansatz (Top-Down)
- Ausgangspunkt: ein **Ereignis** (übergeordnetes oder strategisches Szenario mit Auswirkung auf Prozesse).
- Beispiel: „Pandemie", „großflächiger Cyberangriff", „Standort-Ausfall durch Feuer".
- Sicht: **Top-Down.**
- Eignet sich für **strategische Szenarien**, die mehrere Assets gleichzeitig betreffen.

### Asset-basierter Ansatz (Bottom-Up)
- Ausgangspunkt: ein **Asset / eine Asset-Gruppe**.
- Pro Asset werden Bedrohungen und Schwachstellen ermittelt → ergibt das Risiko.
- Sicht: **Bottom-Up.**
- Untersuchung von Assets im Detail.
- **Ermöglicht spezifische Risikobehandlung auf detaillierter Ebene.**

### Ablauf (Folie 17, beide Ansätze)
Nach der Identifikation: gleiche Schritte für beide Ansätze:
- Risikobewertung
- Risikobehandlung
- Maßnahmen

## Bestandteile / Aufbau

| Aspekt | Ereignis-basiert | Asset-basiert |
|---|---|---|
| Sicht | Top-Down | Bottom-Up |
| Startpunkt | strategisches Szenario | einzelnes Asset |
| Detaillierungsgrad | grob, übergreifend | fein, asset-spezifisch |
| Stärke | erkennt Querschnitts-Szenarien | erkennt asset-spezifische Schwachstellen |
| Schwäche | übersieht ggf. Detail-Lücken | übersieht ggf. übergreifende Szenarien |
| Einsatz | strategische Planung, BCM | operative IT-Sicherheit, IT-Grundschutz |

## Beispiel

- Ereignis-basiert: „Was passiert mit unserem Krankenhaus, wenn eine Pandemie ausbricht?" → Liste von Auswirkungen auf alle Prozesse.
- Asset-basiert: „Welche Risiken hat unser zentrales KIS?" → Liste von Bedrohungen und Schwachstellen für das KIS allein.

## Abgrenzung

- **Beide Ansätze schließen einander nicht aus.** In der Praxis werden sie kombiniert: ereignis-basiert für strategische Sicht, asset-basiert für operative Details.
- **Asset-basiert ist im PDF detailliert** in 6 Schritten (siehe [[ASP - Risikomanagement - Asset-basierte Identifikation]]). Ereignis-basiert wird nur konzeptuell gegenübergestellt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche zwei Ansätze zur Risikoidentifikation gibt es, und worin unterscheiden sie sich?

**Anwendungsfrage:** Welcher Ansatz ist für ein Krankenhaus zur Pandemie-Vorsorge sinnvoller? Welcher für eine IT-Sicherheits-Risikoanalyse pro System?

**Diskussionsfrage:** Welche systematischen Lücken hat jeder der beiden Ansätze allein? Warum kombiniert man sie? (Beide haben blinde Flecken; Top-Down übersieht spezifische technische Schwachstellen, Bottom-Up übersieht systemübergreifende Szenarien.)

**Mögliche Anschlussfragen:**
- Welche 6 Schritte umfasst die asset-basierte Identifikation? ([[ASP - Risikomanagement - Asset-basierte Identifikation]])
- Wie hängt der ereignis-basierte Ansatz mit der BCM-BIA zusammen? ([[ASP - BCM - Business Impact Analyse]])
- Welche Methode passt besser zur ISO 27005?

## Verwandt

- [[ASP - Risikomanagement - Asset-basierte Identifikation]]
- [[ASP - Risikomanagement - Big Picture]]
- [[ASP - Risikomanagement - Grundvoraussetzungen]]
- [[ASP - BCM - Business Impact Analyse]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folie 17
