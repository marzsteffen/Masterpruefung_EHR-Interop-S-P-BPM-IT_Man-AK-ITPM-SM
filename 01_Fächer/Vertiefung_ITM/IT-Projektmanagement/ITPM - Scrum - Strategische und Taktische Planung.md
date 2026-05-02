---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Werkzeuge 02 Agiles PM]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Scrum - Strategische und Taktische Planung

> [!info] Kurzdefinition
> Scrum unterscheidet zwei Planungsebenen: die **strategische Planung** (von der Produktidee über Vision, Backlog und Schätzung bis zum Releaseplan) und die **taktische Planung** (Sprint-Planning für den konkreten Sprint). Ergebnis der strategischen Planung: Klarheit über Inhalt und Kostenrahmen. Ergebnis der taktischen Planung: Sprint Goal + Sprint Backlog.

## Beschreibung

Die Vorlesung strukturiert den gesamten Scrum-Prozess in zwei Planungsebenen.

## Bestandteile / Aufbau

### Strategische Planung (Folien 33–48)

| Phase | Inhalt |
|---|---|
| **Discoveryphase** | Eine Person (Kunde) kommt mit einer Produktidee zum Product Owner. Idee wird zwischen den beiden, eventuell mit Entwicklungsteam, besprochen. **Ergebnis: eine Produktvision.** |
| **Produktvision** | Beschreibt zukünftiges Produkt in kurzer Form. Klar, präzise, detailreich ohne spezifisch zu sein. PO definiert, dann Abstimmung mit Team. Methoden: Freewriting, Elevator Pitch, Product Vision Board. |
| **Product Backlog** | PO definiert mit/ohne Team die Produktfunktionalitäten. PBIs / User Stories entstehen. Hilfsmittel: Mindmap, Story Cards. |
| **Reihung des Backlogs** | Festlegung der Reihenfolge anhand finanziellem Gewinn und Funktionalität. Methoden: MusCoW, 1000 Pingpong-Bälle. |
| **Schätzung** | Schätzung der Backlog Items (Größe, nicht Aufwand). Notwendige Infos: Referenz-Item, Maßeinheit (Story Points), Skala (Fibonacci). Methoden: Planning Poker, Magic Estimation. |
| **Releaseplanung** | Wann ist welche Funktionalität fertig? Basis: Größe der Items, Priorisierung, Velocity (Kapazität pro Sprint). Achten auf Velocity-Schwankung (besonders zu Beginn) und Jahreszeit (Urlaub, Feiertage). |

**Ergebnis der strategischen Planung:**
- Team weiß, was auf sie zukommt.
- Product Owner weiß, welche Kosten ungefähr zu erwarten sind.
- Anschließend beginnen die **Sprints** (zeitlich abgegrenzte Etappen).

Outputs der Sprints heißen: **Produktinkrement, Potential Shippable Business Functionality** oder **Potential Shippable Code**.

### Taktische Planung (Folien 49–50)

Beginnt mit dem **Sprint Planning Meeting 1**:

- **Teilnehmer:** PO, Entwicklungsteam, Management, Anwender.
- **Sprint Goal** wird definiert.
- Auswahl der Product Backlog Items, die im Sprint abgearbeitet werden = **Selected Product Backlog**.
- **Ergebnis:** Jeder weiß, was am Ende des Sprints herauskommen muss; **Commitment** durch Team.

Anschließend **Sprint Planning Meeting 2**:

- *Wie* werden Anforderungen umgesetzt? (Designworkshop)
- Skizzen und Architektur werden festgelegt.
- Liste mit Aufgaben pro PBI → **Sprint Backlog**.

## Beispiel

Übungsaufgaben aus der Vorlesung führen schrittweise durch beide Planungsebenen am Beispiel „Büro/Arbeitszimmer einrichten":
- Product Vision Board (Folien 37–38)
- User Stories (Folien 41)
- Backlog-Reihung (Folie 43)
- Sprint Backlog (Folie 51)

## Abgrenzung

- **Strategische Planung** ist eine Aktivität des **Product Owners** mit Team-Beteiligung; sie wird **kontinuierlich gepflegt** (Backlog Refinement).
- **Taktische Planung** findet in jedem Sprint Planning statt – also pro Sprint einmal.
- Klassisches PM macht **eine umfassende Planung vorab**; Scrum **trennt** strategische und taktische Planung in unterschiedliche Häufigkeit und Detailtiefe.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche zwei Planungsebenen kennt Scrum, und welches Output hat jede?

**Anwendungsfrage:** Sie übernehmen ein neues Patientenportal-Projekt – durchlaufen Sie die strategische Planung von Vision bis Releaseplan in 5 Schritten.

**Diskussionsfrage:** Welche Vorteile hat die Trennung in strategisch + taktisch gegenüber einer einzelnen Vorab-Großplanung im Wasserfall?

**Mögliche Anschlussfragen:**
- Welche Methoden gehören in welche Planungsebene?
- Wie hängen Velocity und Releaseplan zusammen?
- Wo ist die Grenze: ab wann müssen Anforderungen in den Sprint, ab wann bleiben sie im Backlog?

## Verwandt

- [[ITPM - Scrum - Grundlagen]]
- [[ITPM - Scrum - Artefakte]]
- [[ITPM - Scrum - Backlog Priorisierung]]
- [[ITPM - Scrum - Sprint]]
- [[ITPM - Scrum - Meetings]]
- [[ITPM - Agile - Story Points]]
- [[ITPM - Agile - Planning Poker]]

## Quelle

- Vorlesung: [[ITPM - VL - Werkzeuge 02 Agiles PM]]
- Folien/Seitenangabe: 33–50
