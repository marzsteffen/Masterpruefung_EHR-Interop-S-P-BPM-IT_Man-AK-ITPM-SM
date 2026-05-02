---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Initiierung Strukturierung Requirements]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - RE - Anforderungsverwaltung

> [!info] Kurzdefinition
> Anforderungen werden über Lebenszyklus hinweg verwaltet: ID, Name, Begründung, Abnahmekriterien, beteiligte Personen, Status, Priorität, Abhängigkeiten und Versionierung. Die Verwaltung sichert Nachvollziehbarkeit, Änderungsfähigkeit und Konsistenz.

## Beschreibung

Die Vorlesung führt die Verwaltungsattribute auf den Folien 78–79 ein.

## Bestandteile / Aufbau

### Pflichtattribute pro Anforderung (Folie 78)

- **Eindeutige ID** zur Identifizierung.
- **Name** der Anforderung.
- **Begründung** für die Anforderung.
- **Abnahmekriterien** für die Anforderung.
- **Personen**, die mit der Anforderung zu tun haben (z. B. Wer hat die Anforderung erstellt?).
- **Status:** erfasst, geprüft, freigegeben.

### Priorisierung (Folie 78)

Festlegung der Priorität durch:

- **Wert für den Kunden**
- **Wert für Firma / Geschäft**
- **Time to Market**
- **Risiko und Aufwand**

### Weitere Verwaltungsaspekte (Folie 79)

- **Abhängigkeiten von Anforderungen** – Abbildung, wenn eine Anforderung von einer anderen abhängt.
- **Versionsverwaltung** – Anforderungen können sich in einem gewissen Maß ändern.

## Beispiel

*Im PDF nicht durch ein konkretes Anforderungs-Datenblatt illustriert.*

## Abgrenzung

- **Anforderungsverwaltung** ≠ **Anforderungsprüfung** ([[ITPM - RE - Anforderungsprüfung]]): Verwaltung ist der laufende Prozess, Prüfung ist der Qualitätsschritt.
- Die Statusmenge (erfasst → geprüft → freigegeben) ist im PDF eng gefasst; reale Tools haben oft mehr Status (z. B. „in Umsetzung", „abgenommen").

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Attribute hat eine verwaltete Anforderung mindestens?

**Anwendungsfrage:** Wie priorisieren Sie eine Anforderung mit hohem Kundenwert, niedrigem Geschäftswert, hohem Risiko?

**Diskussionsfrage:** Warum braucht es Versionsverwaltung für Anforderungen, obwohl sie „nur" Spezifikation sind?

**Mögliche Anschlussfragen:**
- Wie verhalten sich diese Attribute zu User-Story-Feldern in Jira?
- Welche Werkzeuge unterstützen Requirements-Management (DOORS, Polarion, Jira, etc.)? *(im PDF nicht definiert)*
- Welche Rolle spielen Abhängigkeiten beim Backlog-Refinement?

## Verwandt

- [[ITPM - Requirements Engineering - Grundlagen]]
- [[ITPM - RE - Anforderungsprüfung]]
- [[ITPM - Anforderung - Definition]]
- [[ITPM - Scrum - Backlog Priorisierung]]
- [[ITPM - Lastenheft]]
- [[ITPM - Pflichtenheft]]

## Quelle

- Vorlesung: [[ITPM - VL - Initiierung Strukturierung Requirements]]
- Folien/Seitenangabe: 78–79
