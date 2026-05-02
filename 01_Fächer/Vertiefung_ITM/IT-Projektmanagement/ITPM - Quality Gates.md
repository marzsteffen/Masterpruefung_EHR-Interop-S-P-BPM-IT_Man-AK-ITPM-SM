---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Qualitätsmanagement]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Quality Gates

> [!info] Kurzdefinition
> Quality Gates sind definierte Kontrollpunkte an Phasenübergängen eines Projekts. An jedem Gate werden vorab festgelegte Qualitätskriterien geprüft; nur bei Erfüllung darf in die nächste Phase übergegangen werden. Sie sind ein wichtiges Hilfsmittel im Qualitätsmanagement.

## Beschreibung

Quality Gates werden in der Vorlesung als **Übungsaufgabe** (Folie 44) eingeführt:

> „Sogenannte ‚Quality Gates' sind ein wichtiges Hilfsmittel im Rahmen des Qualitätsmanagements in Projekten."

Konkrete Inhalte zu Quality Gates werden im PDF **nicht ausgearbeitet** – die Vorlesung verlangt eine eigene Literaturrecherche und Ausarbeitung als max. 2-A4-Seiten-Dokument zu folgenden Fragen:

- **Was sind Quality Gates?**
- **Wie werden sie verwendet?**
- **Definieren Sie für Ihr Projekt die wichtigsten Quality Gates.**

> ⚠️ Die folgenden Inhalte stammen aus Standardlehrbuch-Wissen und sind als „Ergänzung außerhalb der Vorlesung" zu verstehen.

## Bestandteile / Aufbau

> *Die folgenden Beschreibungen sind nicht aus dem PDF, sondern Standardlehrbuch-Wissen zur Vorbereitung der Übungsaufgabe.*

### Definition (Standardlehrbuch)

Ein Quality Gate ist ein **definierter Kontrollpunkt** im Projektablauf, der zwischen zwei Phasen liegt und vorgibt, welche Kriterien erfüllt sein müssen, damit das Projekt in die nächste Phase übergehen darf.

### Typische Eigenschaften

- **Verbindlich:** Übergang erst nach erfolgreicher Prüfung.
- **Vorab definiert:** Kriterien werden vor Projektstart festgelegt.
- **Kontrolliert:** Entscheidung durch ein Gremium (Lenkungsausschuss, QS-Verantwortlicher, Projektleiter).
- **Dokumentiert:** Ergebnisse werden formal festgehalten (Freigabe oder Nacharbeit).

### Typische Quality Gates in einem klassischen Projekt

| Gate | Phasenübergang | Beispielkriterien |
|---|---|---|
| **G0 – Projektfreigabe** | Initiierung → Planung | Projektantrag genehmigt, Sponsor benannt |
| **G1 – Anforderungsfreigabe** | Planung → Konzept | Lastenheft freigegeben, Anforderungen vollständig |
| **G2 – Designfreigabe** | Konzept → Realisierung | Pflichtenheft freigegeben, Architektur reviewed |
| **G3 – Testfreigabe** | Realisierung → Test | Code-Reviews abgeschlossen, Komponentenstest grün |
| **G4 – Abnahme** | Test → Inbetriebnahme | Abnahmetest bestanden, Schulungen abgeschlossen |
| **G5 – Projektabschluss** | Betrieb → Abschluss | Lessons Learned dokumentiert, Übergabe erfolgt |

## Beispiel

Übungsaufgabe der Vorlesung (Folie 44): Definition der wichtigsten Quality Gates für das eigene Projekt – Deadline 27.06.2025, Abgabe über Moodle, Präsentation in der nächsten LV.

## Abgrenzung

- **Quality Gate** ≠ **Meilenstein** ([[ITPM - Meilenstein]]): Meilensteine sind Zeitpunkte ohne zwingende Kriterien; Quality Gates sind kriterienbasierte Entscheidungspunkte.
- **Quality Gate** ≠ **Phasenende:** Phasenende ist temporal, Gate ist qualitativ.
- Verbindung zu **QS-Phasen** ([[ITPM - QS - Phasen]]) – die phasenbezogenen QS-Fragen werden an Quality Gates formell überprüft.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Quality Gate, und wie unterscheidet es sich von einem Meilenstein?

**Anwendungsfrage:** Definieren Sie für ein KIS-Migrationsprojekt vier Quality Gates mit je drei Kriterien.

**Diskussionsfrage:** Welche Risiken bestehen, wenn Quality Gates rein formell durchlaufen werden („Stempel-QG"), ohne echte Prüfung?

**Mögliche Anschlussfragen:**
- Wer entscheidet über die Freigabe eines Quality Gates?
- Wie verhalten sich Quality Gates zu agilen Sprint Reviews?
- Welche Verbindung zur Verifikation/Validierung?
- Wie verhält sich die Definition of Done zum Quality Gate?

## Verwandt

- [[ITPM - QS - Plan]]
- [[ITPM - QS - Phasen]]
- [[ITPM - QS - Organisation]]
- [[ITPM - Meilenstein]]
- [[ITPM - QS - Testen Verifikation Validierung]]
- [[ITPM - Agile - Definition of Done]]

## Quelle

- Vorlesung: [[ITPM - VL - Qualitätsmanagement]]
- Folien/Seitenangabe: 44 (nur als Übungsaufgabe; Inhalt im PDF nicht ausgeführt)

## Ergänzung außerhalb der Vorlesung

Die obige inhaltliche Beschreibung (Definition, Eigenschaften, typische Gates G0–G5) ist **Standardlehrbuch-Wissen** und stammt **nicht aus dem PDF**. Die Vorlesung selbst lässt Quality Gates als Übungsaufgabe offen. Bitte vor mündlicher Prüfung die eigene Ausarbeitung mit dieser Note abgleichen und ggf. ergänzen.
