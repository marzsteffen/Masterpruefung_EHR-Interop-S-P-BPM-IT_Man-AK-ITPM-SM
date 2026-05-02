---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Einfuehrung und Motivation]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - DSGVO - Grundsätze für die Verarbeitung personenbezogener Daten

> [!info] Kurzdefinition
> Vier in der Vorlesung genannte Grundsätze der DSGVO für die Verarbeitung personenbezogener Daten: Zweckbindung, Datenminimierung, Speicherbegrenzung, Integrität und Vertraulichkeit.

## Beschreibung

Folie 16 nennt die Datenschutzgrundverordnung (DSGVO) als zentrales europäisches Datenschutz-Regelwerk und benennt vier Grundsätze für die Verarbeitung personenbezogener Daten.

**Ziel der DSGVO** (laut Folie): Schutz der personenbezogenen und sensiblen Daten.

**Geltungsbereich:** Gilt für alle Unternehmen, die Daten von EU-Bürgern verarbeiten – unabhängig vom Standort.

**Grundsätze (laut Folie 16):**
- **Zweckbindung:** Daten dürfen nur für den festgelegten Zweck erhoben und verwendet werden.
- **Datenminimierung:** Es sollen nur die für den Zweck notwendigen Daten erhoben werden.
- **Speicherbegrenzung:** Daten dürfen nur so lange gespeichert werden, wie es für den Zweck notwendig ist.
- **Integrität und Vertraulichkeit:** Angemessene Sicherheit der Daten muss gewährleistet sein.

**Im PDF nicht enthalten** (zur Information – nicht in der Note ergänzen): die DSGVO Art. 5 enthält darüber hinaus die Grundsätze „Rechtmäßigkeit, Verarbeitung nach Treu und Glauben, Transparenz" und „Richtigkeit", sowie als zusätzliches Prinzip „Rechenschaftspflicht" (Accountability). Diese werden in dieser Vorlesung *nicht* aufgeführt.

## Bestandteile / Aufbau

| Grundsatz | Kerngedanke |
|---|---|
| Zweckbindung | Daten nur für festgelegten Zweck verwenden |
| Datenminimierung | Nur notwendige Daten erheben |
| Speicherbegrenzung | Nur so lange speichern wie nötig |
| Integrität und Vertraulichkeit | Angemessene Sicherheit gewährleisten |

## Beispiel

*Kein konkretes Beispiel im PDF.* Üblicher eHealth-Bezug: Eine Praxis darf für die Terminvereinbarung Name, Geburtsdatum und Telefonnummer erheben (Datenminimierung) und nicht zusätzlich SVNR und Anschrift, wenn diese für den Zweck nicht erforderlich sind.

## Abgrenzung

- Die DSGVO-Version oder Artikel-Bezüge (z. B. „Art. 5 Abs. 1") sind in der Vorlesung *nicht* angegeben. **DSGVO-Version im PDF nicht spezifiziert** (in der Praxis: Verordnung (EU) 2016/679, anwendbar seit 25.05.2018).
- Die Vorlesung nennt explizit nur diese vier Grundsätze, nicht alle aus Art. 5 DSGVO. Bei einer Prüfungsantwort kann das relevant sein.
- „Integrität und Vertraulichkeit" als Grundsatz adressiert primär die [[ASP - Informationssicherheit - CIA-Triade]] – ist aber nicht mit „Privatsphäre" identisch.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Grundsätze nennt die DSGVO für die Verarbeitung personenbezogener Daten (laut Vorlesung)?

**Anwendungsfrage:** Welcher Grundsatz ist verletzt, wenn in einer eHealth-App die Geräte-IMEI für eine reine Login-Funktionalität gespeichert wird? (Datenminimierung.)

**Diskussionsfrage:** Wie unterscheidet sich der Grundsatz „Integrität und Vertraulichkeit" von [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]? Welcher Grundsatz adressiert direkt das Schutzziel Privatsphäre? (Antwort: Zweckbindung – Privatsphäre ist „zweckgemäße Verwendung".)

**Mögliche Anschlussfragen:**
- Wie wirkt sich der Grundsatz Speicherbegrenzung auf Backup-Strategien aus?
- Welche technischen Maßnahmen unterstützen Datenminimierung? (Pseudonymisierung, Anonymisierung – Letztere ist im PDF dieser Vorlesung *nicht* genannt.)
- Welchen Bezug hat der Grundsatz „Integrität und Vertraulichkeit" zur CIA-Triade?

## Verwandt

- [[ASP - DSGVO - Privacy by Design]]
- [[ASP - DSGVO - Privacy by Default]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]
- [[ASP - Informationssicherheit - CIA-Triade]]
- [[EHR - Einwilligung - Patient Consent]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 16
