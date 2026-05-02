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

# ITPM - Ablauf- und Terminplan

> [!info] Kurzdefinition
> Der Ablauf- und Terminplan sortiert alle Arbeitspakete in ihre Ausführungsreihenfolge und legt die geplanten Ausführungstermine fest. Er beruht auf Anordnungsbeziehungen (Abhängigkeiten), Vor-/Rückwärtsrechnung sowie Pufferzeiten und liefert die Basis für Gantt-Diagramme und Terminlisten.

## Beschreibung

**Aufgabe (Folie 45):**

- Sortiert alle Arbeiten und Arbeitspakete in ihre **Ausführungsreihenfolge**.
- Legt die **geplanten Ausführungstermine** fest.

**Leitfragen für den Ablauf:**
- Welche Arbeitspakete können **unabhängig** voneinander ausgeführt werden?
- Welche AP sind **unmittelbare Voraussetzung**?
- Welche AP können **unmittelbar folgen**?
- Welche Aktivitäten gehen **parallel**?

## Bestandteile / Aufbau

### Liste von Aktivitäten (Folie 46)

- Wenn der PSP noch zu grob ist, werden Arbeitspakete in **Vorgänge** zerlegt.
- Ein **Vorgang** ist die kleinste, planbare Aktivitäteneinheit.

### Anordnungsbeziehungen (Folie 47)

- Abhängigkeiten werden **identifiziert**.
- Es wird geprüft, was **parallel** stattfinden kann.
- **Darstellung:** Aktivitäten grafisch im **Netzplan** – parallel oder hintereinander.

### Aufwandsschätzung (Folie 48)

Jede Aktivität bekommt eine geschätzte **Zeitdauer**. Methode: **Drei-Punkt-Schätzung** – siehe [[ITPM - Aufwandsschätzung - Drei-Punkt]].

### Terminplan & Zeitrechnungen (Folie 49)

- **Vorwärtsrechnung:** frühestmöglicher Start- und Endtermin aller Aktivitäten.
- **Rückwärtsrechnung:** spätester zulässiger Start- und Endtermin jeder Aktivität.
- Aus den Zeitdauerwerten und Abhängigkeiten ergibt sich für alle Aktivitäten der späteste Start-/Endtermin.

### Pufferzeiten, kritischer Weg, Meilensteine, Fixtermine

Detail in eigenen Notes:
- [[ITPM - Pufferzeiten]]
- [[ITPM - Kritischer Weg]]
- [[ITPM - Meilenstein]]

**Projektkalender und Fixtermine (Folie 52):**
- Zeitdauer wird auf den Kalender eingetragen; Wochenenden und Feiertage werden hier ergänzt.
- **Fixtermine** sind Zeitpunkte, an denen Aktivitäten fertig sein müssen. Eventuell Umplanung, parallele Ausführung oder zusätzliche Ressourcen.

### Darstellung

- **Balkenplantechnik (Gantt-Diagramm):** siehe [[ITPM - Gantt-Diagramm]].
- **Terminliste (Folie 55):** Vorgangsnummer, Beschreibung, geschätzte Dauer, geplanter Start-/Endtermin – hilft bei der Überwachung des Projektfortschritts.

## Beispiel

Übungsaufgabe der Vorlesung (Folie 58): Ablauf- und Terminplan für das eigene Projekt erstellen.

## Abgrenzung

- **Ablauf-/Terminplan** zeigt **wann** und in welcher Reihenfolge gearbeitet wird; **PSP** zeigt **was** zu tun ist (siehe [[ITPM - Projektstrukturplan]]).
- **Netzplan** ≠ **Gantt**: Netzplan zeigt Abhängigkeiten als Graph, Gantt als Zeitbalken.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Schritte umfasst die Erstellung eines Ablauf- und Terminplans (Aktivitätenliste, Anordnungsbeziehungen, Schätzung, Terminrechnung, Darstellung)?

**Anwendungsfrage:** Was ist der Unterschied zwischen Vorwärts- und Rückwärtsrechnung, und wofür dient jede?

**Diskussionsfrage:** Wann wird ein zu detaillierter Ablauf-/Terminplan zum Hindernis? Wann zu grob?

**Mögliche Anschlussfragen:**
- Welche Software-Werkzeuge eignen sich (MS Project, Primavera, Smartsheet)? *(im PDF nicht definiert)*
- Wie verhält sich der Ablauf-/Terminplan zum Sprint-Plan in Scrum?

## Verwandt

- [[ITPM - Projektstrukturplan]]
- [[ITPM - Aufwandsschätzung - Drei-Punkt]]
- [[ITPM - Pufferzeiten]]
- [[ITPM - Kritischer Weg]]
- [[ITPM - Meilenstein]]
- [[ITPM - Gantt-Diagramm]]
- [[ITPM - DIN 69900 - Netzplantechnik]]

## Quelle

- Vorlesung: [[ITPM - VL - Initiierung Strukturierung Requirements]]
- Folien/Seitenangabe: 45–55
