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

# SM - 5 Phasen - serviceorientierte IT-Organisation

> [!info] Kurzdefinition
> Modell der USU GmbH (2018) zur Entwicklung einer serviceorientierten IT-Organisation in fünf Phasen: Klärung der Ziele und Strategie → Aufbau eines Servicekatalogs → Definieren von Service Level Agreements → Service Monitoring und Reporting → Review und Optimierung.

## Beschreibung

Folie 29 zeigt das Modell als Pfeilkette mit fünf Phasen. Jede Phase ist Voraussetzung für die nächste; die fünfte schließt den Kreis (Review und Optimierung führt zurück in die Strategie und in nachfolgende Iterationen — analog zum CSI-Modell, siehe [[SM - ITIL Continual Improvement - Modell]]).

Im Foliensatz steht jede Phase nur als Beschriftung (Pfeilbeschriftung); zusätzliche Details sind dort *nicht angegeben.*

## Bestandteile / Aufbau

| Phase | Bezeichnung | Inhalt |
|---|---|---|
| 1 | Klärung der Ziele und Strategie | Ausrichtung der IT auf Unternehmensziele |
| 2 | Aufbau eines Servicekatalogs | Definition und Strukturierung der angebotenen Services (siehe [[SM - IT-Service-Katalog - Sichten und Strukturierung]]) |
| 3 | Definieren von Service Level Agreements | Vertragliche Festlegung der Service-Levels (siehe [[SM - SLA - Definition und Inhalte]]) |
| 4 | Service Monitoring und Reporting | Messung und Berichterstattung |
| 5 | Review und Optimierung | Bewertung und kontinuierliche Verbesserung |

Diese fünf Phasen entsprechen weitgehend dem Lebenszyklus eines Service: erst Strategie, dann Definition, dann Vereinbarung, dann Betrieb mit Messung, dann Verbesserung. Sie sind ein praktisches Roadmap-Modell für Krankenhaus-IT-Abteilungen, die sich serviceorientiert aufstellen wollen.

## Beispiel

Anwendung auf eine Krankenhaus-IT (laut Foliensatz nicht ausgearbeitet, aber sinnvoll):

1. **Strategie:** „Krankenhaus-IT wird interner Dienstleister mit messbarem Mehrwert."
2. **Servicekatalog:** Aufstellung aller IT-Services (KIS-Zugang, RIS-Zugang, Mailservice, Notfall-Support, …).
3. **SLAs:** 99,5 % Verfügbarkeit für KIS während der Servicezeiten; 24×7-Support für Notfall-Services.
4. **Monitoring/Reporting:** Monatliche Berichte an Geschäftsleitung und Fachabteilungen.
5. **Review/Optimierung:** Jährliche SLA-Reviews; Anpassung an neue medizinische Anforderungen (z. B. Telemedizin).

## Abgrenzung

- **5 Phasen vs. ITIL V3 Servicelebenszyklus** (siehe [[SM - ITIL V3 - Servicelebenszyklus]]): Der V3-Lifecycle hat ebenfalls fünf Phasen (Strategy/Design/Transition/Operation/CSI), die aber tiefer in die ITIL-Logik eingebettet sind. Das USU-Modell ist eine vereinfachte Roadmap, kein Referenzmodell.
- **5 Phasen vs. Krankenhaus-Kernprozesse** (siehe [[SM - ITSM im Gesundheitswesen - Krankenhaus-Architektur]]): Das Krankenhaus hat ebenfalls fünf Kernprozesse (Aufnahme/Anamnese/Diagnostik/Therapie/Entlassung) — Verwechslungsgefahr! Beide sind unabhängige 5-Phasen-Modelle.
- **5 Phasen vs. CSI-Modell** (siehe [[SM - ITIL Continual Improvement - Modell]]): CSI hat sechs (+1) Schritte mit anderem Fokus (Verbesserungsschleife). 5-Phasen-Modell ist eher Aufbauleitfaden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche fünf Phasen umfasst die Entwicklung einer serviceorientierten IT-Organisation laut USU? — Strategie/Ziele → Servicekatalog → SLAs → Monitoring/Reporting → Review/Optimierung.

**Anwendungsfrage:** In welcher Phase befindet sich eine Krankenhaus-IT-Abteilung, die zwar einen Servicekatalog hat, aber keine SLAs vereinbart? — Zwischen Phase 2 und 3.

**Diskussionsfrage:** Was passiert, wenn eine Phase übersprungen wird, z. B. SLAs ohne klaren Servicekatalog? — Folge: SLAs werden auf nicht definierte Services bezogen, Messgrößen sind unklar, Streitigkeiten programmiert. Vergleichbar mit ITIL-4-SLM-Anforderung „SLAs müssen sich auf einen definierten Service im Servicekatalog beziehen" (siehe [[SM - ITIL Practice - Service Level Management]]).

**Mögliche Anschlussfragen:**
- Wie hängt das 5-Phasen-Modell mit dem ITIL-V3-Lifecycle zusammen?
- Wie wird die fünfte Phase „Review und Optimierung" konkret umgesetzt? — Verbindung zu CSI-Modell.
- Welche Rolle spielt das Tooling in jeder Phase?

## Verwandt

- [[SM - IT-Service-Katalog - Sichten und Strukturierung]]
- [[SM - SLA - Definition und Inhalte]]
- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - ITSM im Gesundheitswesen - Krankenhaus-Architektur]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 29; Quelle: USU GmbH 2018

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
