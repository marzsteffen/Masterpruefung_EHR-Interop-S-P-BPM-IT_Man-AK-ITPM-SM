---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - ITSM Einführung Text]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - Service-Level - Utility vs Warranty

> [!info] Kurzdefinition
> Utility (Nutzen) bezeichnet *was* ein Service tut — die bereitgestellte Funktionalität. Warranty (Gewähr) bezeichnet *wie* der Kunde den Nutzen geliefert bekommt — die qualitätsbezogenen Anforderungen wie Verfügbarkeit, Zuverlässigkeit, Sicherheit. Diese Anforderungen werden auch als Service-Levels bezeichnet.

## Beschreibung

Allweyer beschreibt für die Verwendbarkeit eines Service zwei maßgebliche Aspekte (vgl. [BeZi15]):

- **Utility (Nutzen):** Die bereitgestellte Funktionalität. Das, *was* der Service tut.
- **Warranty (Gewähr):** Die Zusicherung, dass der Service den vereinbarten Anforderungen entspricht — z. B. hinsichtlich Verfügbarkeit, Zuverlässigkeit oder Sicherheit. Das, *wie* der Kunde den Nutzen geliefert bekommt. Diese qualitätsbezogenen Anforderungen werden als **Service-Levels** bezeichnet.

Beide Aspekte zusammen bestimmen, ob ein Service für den Kunden tatsächlich brauchbar ist. Ein Service mit voller Utility, aber ohne Warranty (z. B. funktional korrekt, aber nur sporadisch verfügbar) liefert dem Kunden keinen verlässlichen Nutzen.

## Bestandteile / Aufbau

| Aspekt | Frage | Beispielinhalte |
|---|---|---|
| Utility | Was tut der Service? | Funktion „CRM-Zugriff", „E-Mail-Postfach mit 5 GB", „Hotline-Erreichbarkeit" |
| Warranty | Wie verlässlich? | Verfügbarkeit, Zuverlässigkeit, Sicherheit, Performance, Kontinuität |

Die Warranty-Anforderungen werden in Service-Levels operationalisiert (z. B. „99,5 % Verfügbarkeit pro Monat") und in einem SLA festgehalten (siehe [[SM - SLA - Definition und Inhalte]]).

## Beispiel

Allweyer nennt Verfügbarkeit, Zuverlässigkeit und Sicherheit als typische Warranty-Aspekte. Konkretes Beispiel im Text: 99,5 % monatliche Verfügbarkeit als Service-Level.

## Abgrenzung

- **Utility ≠ Warranty:** Beide werden gemeinsam vereinbart, sind aber unterschiedliche Designdimensionen. Ein Service kann denselben Funktionsumfang (Utility) mit unterschiedlichen Qualitätsstufen (Warranty) anbieten — z. B. Standard-Support vs. Premium-Support.
- **Service-Level vs. SLA:** Service-Level ist die einzelne Qualitätszusage; das SLA ist das Vertragsdokument, das die Service-Levels schriftlich festhält.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeuten Utility und Warranty? — Utility = was der Service tut (Funktionalität); Warranty = wie verlässlich er das tut (Verfügbarkeit, Zuverlässigkeit, Sicherheit).

**Anwendungsfrage:** Ordnen Sie für einen konkreten Service Eigenschaften zu Utility oder Warranty zu (z. B. „CRM-Zugriff für Vertriebsmitarbeiter" → Utility; „99,9 % Verfügbarkeit Mo–Fr 8–18 Uhr" → Warranty).

**Diskussionsfrage:** Warum reicht eine Definition über die Funktionalität allein (Utility) nicht aus? Welche Konsequenz hat das fürs Service-Design — und welche Inhalte landen dann zwingend im SLA?

**Mögliche Anschlussfragen:**
- Wie verhalten sich Utility und Warranty zu den typischen SLA-Inhalten?
- Können Standard-SLAs unterschiedliche Warranty-Stufen anbieten (Premium-Support)?
- Wie hängt das mit der Risikoverteilung beim Anbieter zusammen ([[SM - IT-Service - Definition]])?

## Verwandt

- [[SM - IT-Service - Definition]]
- [[SM - SLA - Definition und Inhalte]]
- [[SM - Service-Katalog - Definition und Aufbau]]

## Quelle

- Vorlesung: [[SM - VL - ITSM Einführung Text]]
- Folien/Seitenangabe: Buchseite 129–130 (Allweyer, Kap. 8.2 „Service-Levels"); Quellenverweis [BeZi15]

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
