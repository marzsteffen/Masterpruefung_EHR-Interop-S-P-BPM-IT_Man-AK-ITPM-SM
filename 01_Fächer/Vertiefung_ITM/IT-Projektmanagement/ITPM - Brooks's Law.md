---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Brooks's Law

> [!info] Kurzdefinition
> Brooks's Law: „Adding manpower to a late software project makes it later." Mehr Personal in einem späten Softwareprojekt verzögert es zusätzlich – wegen Trainingsaufwand und steigendem Kommunikationsaufwand. Für jedes Projekt gibt es eine **optimale Mitarbeiteranzahl** im Verhältnis zur minimalen Projektdauer.

## Beschreibung

Aus Folien 73–74:

- Beobachtung über das Management von Softwareprojekten von **Fred Brooks**, geprägt 1975 in seinem Buch **„The Mythical Man-Month"**.
- Aussage: „Das Hinzufügen von Arbeitskräften zu einem späten Softwareprojekt macht es noch später."

**Ursachen für die Verzögerung:**

- **Erhöhter Trainingsaufwand** für die neuen Mitarbeiter.
- **Steigender Kommunikationsaufwand** (mehr Personen → mehr Kommunikationsverbindungen).

## Bestandteile / Aufbau

- Für jedes Projekt existiert eine **optimale Mitarbeiteranzahl** im Verhältnis zur minimalen Projektdauer.
- Mehr Mitarbeiter ≠ proportional weniger Zeit – im Gegenteil, ab einer Schwelle steigt die Projektdauer wieder.

Mathematischer Hintergrund (Standardlehrbuch, im PDF nicht ausgeführt): Bei n Mitarbeitern gibt es **n × (n–1) / 2** Kommunikationspaare.

## Beispiel

*Im PDF nicht durch konkretes Beispiel illustriert; nur Schaubild zur Wirkung mit Kurve „Optimum + Verschlechterung bei mehr Personal".*

## Abgrenzung

- Brooks's Law gilt insbesondere für **Software-Projekte**, weniger für rein körperliche Tätigkeiten.
- **Counter-Pattern:** Bei sehr früher Projektphase und gut modularisierten Aufgaben kann zusätzliches Personal sinnvoll sein.
- Beziehung zu **Teamgröße** ([[ITPM - Projektteam - Bildung]]): Optimale Teamgröße 5–7 Personen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was besagt Brooks's Law, und wer hat es formuliert?

**Anwendungsfrage:** Ihr Projekt liegt 4 Wochen hinter dem Plan. Sollen Sie 3 weitere Entwickler dazunehmen? Diskutieren Sie.

**Diskussionsfrage:** Welche Ausnahmen / Grenzen hat Brooks's Law? In welchen Projekttypen gilt es weniger?

**Mögliche Anschlussfragen:**
- Welcher Buchtitel wird in der Vorlesung zitiert (The Mythical Man-Month)?
- Wie verhält sich Brooks's Law zur Personenmonat-Definition?
- Welche Konsequenz für die Personalplanung in der Frühphase?

## Verwandt

- [[ITPM - Personalplanung - Grundlagen]]
- [[ITPM - Projektteam - Bildung]]
- [[ITPM - Personenmonat - Zeitumrechnung]]
- [[ITPM - Projektkommunikation - Grundlagen]]

## Quelle

- Vorlesung: [[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]
- Folien/Seitenangabe: 73–74
