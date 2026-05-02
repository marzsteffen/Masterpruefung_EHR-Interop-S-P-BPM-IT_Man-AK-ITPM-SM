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

# SM - ITIL Practice - Release Management

> [!info] Kurzdefinition
> ITIL-4-Practice (Service Management) zum Zur-Verfügung-Stellen neuer und geänderter Services und Funktionen.

## Beschreibung

Folie 81 definiert:

**Zweck:**
> „Das zur Verfügung stellen neuer und geänderter Services und Funktionen."

(Folie 81 wiederholt den Identifikations-Hinweis aus dem Monitoring-Slide — wahrscheinlich Copy-Paste-Fehler im Foliensatz: „Diese Practice identifiziert und priorisiert Infrastruktur, Services, Geschäftsprozesse und Informationssicherheits-Events…" — *passt inhaltlich nicht zu Release Management, im PDF aber so abgedruckt*. Ich übernehme nur die zur Practice passenden Aussagen.)

**Definition Release** (ITIL 4):
> „Eine Version eines Service oder eines anderen Configuration Items oder eine Sammlung von Configuration Items, die zur Verwendung bereitgestellt wird."

Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Zweck | Bereitstellen neuer/geänderter Services und Funktionen |
| Definition Release | Version eines Service / CI(s), zur Verwendung bereitgestellt |

## Beispiel

KIS-Major-Update von Version 7.4 auf 8.0 wird als Release geplant (mehrere CIs: Datenbank, Frontend, Schnittstellen) und zur produktiven Nutzung freigegeben.

## Abgrenzung

- **Release Management vs. Deployment Management**: Deployment ist das technische Ausrollen; Release ist die Verfügbarmachung gegenüber Anwendern. In ITIL 4 sind das *zwei* Practices.
- **Release Management vs. Change Enablement** ([[SM - ITIL Practice - Change Enablement]]): Change Enablement autorisiert Changes; Release stellt das Resultat bereit.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Zweck der Release Management Practice? — Bereitstellung neuer/geänderter Services und Funktionen.

**Definition Release:** Version eines Service oder CIs, zur Verwendung bereitgestellt.

**Diskussionsfrage:** Wie verhält sich Release Management zu agilen/DevOps-Vorgehen, in denen Releases oft ohne separate Practice automatisch ausgerollt werden (CI/CD)? — Spannungsfeld: Klassisches Release ist zeremoniell; DevOps-Releases sind häufig, automatisiert. ITIL 4 betont aber die Unterscheidung zwischen Deployment (technisch) und Release (Verfügbarkeit für Nutzer) — das passt auch zu Feature-Toggles.

**Mögliche Anschlussfragen:**
- Was unterscheidet Release Management und Deployment Management?
- Wie hängt Release mit Change Enablement zusammen?
- Welche Rolle spielt Release Management in einer Cloud-Umgebung (siehe [[SM - ITIL 4 - Cloud Computing Auswirkungen]])?

## Verwandt

- [[SM - ITIL Practice - Change Enablement]]
- [[SM - ITIL Practice - Service Configuration Management]]
- [[SM - ITIL 4 - Service-Wertschöpfungskette]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 81; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
