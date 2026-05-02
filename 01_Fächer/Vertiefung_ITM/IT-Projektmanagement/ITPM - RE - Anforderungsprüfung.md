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

# ITPM - RE - Anforderungsprüfung

> [!info] Kurzdefinition
> Anforderungsprüfung umfasst die Prüfung von **Form** (Aufbau, Vollständigkeit der Struktur) und **Inhalt** (Korrektheit, Verständlichkeit). Sie sollte **ständig** stattfinden, alternativ an Meilensteinen oder am Ende. Methoden: Reviews, Inspektionen, Walkthroughs.

## Beschreibung

### Was wird geprüft? (Folie 74)

**Form:**
- Entspricht das Dokument den Vorgaben des Unternehmens?
- Ist ein Inhaltsverzeichnis vorhanden?
- Beispielfragen:
  - Sind die Ziele bzw. die Vision des Projekts explizit?
  - Ist der Scope vom Kontext klar abgegrenzt?
  - Haben alle Use-Cases einen Akteur und einen Namen?
  - Sind in einem etwaigen Datenmodell alle Beziehungen bekannt?

**Inhalt:**
- Prüfung auf inhaltliche **Korrektheit** und **Vollständigkeit**.
- Macht alles Sinn und ist es verständlich?

### Wann sollte man prüfen? (Folie 75)

| Zeitpunkt | Bewertung |
|---|---|
| **Ständig** (beim Erheben und Dokumentieren) | **Beste Variante** – Fehler werden sofort bemerkt. |
| **Zu bestimmten Meilensteinen** | Pragmatischer Mittelweg. |
| **Am Ende des Requirements** | **Risikoreichste Prüfung** – Probleme/Änderungen kommen spät. |

### Wer sollte beteiligt sein? (Folie 76)

- **Auftraggeber**
- **Endanwender**
- **Abnehmer des Dokuments** (Softwarearchitekten oder Designer, die Machbarkeit und Risiken einschätzen)

### Wie sollte geprüft werden? (Folie 77)

| Methode | Ablauf |
|---|---|
| **Gutachten / Stellungnahme / Reviews** | Dokument an einen geeigneten Prüfer; dieser verfasst eine Stellungnahme; danach Nachbesprechung und weitere Schritte. |
| **Inspektionen** | Dokument an Gruppe von Lesern; vorab Prüfung; gemeinsamer Termin; Mängel dokumentieren und Vorgehensweise festlegen. |
| **Walkthroughs** | Ersteller führt Prüfer inhaltlich durch das Dokument (z. B. anhand Use Cases); Daten und Qualitätsanforderungen werden parallel besprochen; Mängel dokumentieren, beheben, anschließend Freigabe. |

## Bestandteile / Aufbau

Drei Dimensionen der Prüfung: **Was** (Form/Inhalt), **wann** (ständig/Meilenstein/Ende), **wer/wie** (Reviews/Inspektionen/Walkthroughs).

## Beispiel

*Im PDF nicht durch konkretes Prüfungsbeispiel illustriert.*

## Abgrenzung

- **Review** ist meist asynchron (Stellungnahme).
- **Inspektion** ist halbsynchron (vorab + Termin).
- **Walkthrough** ist synchron (Ersteller führt durch).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Methoden zur Anforderungsprüfung kennt die Vorlesung? Wie unterscheiden sie sich im Ablauf?

**Anwendungsfrage:** Welche Prüfungs-Methode wählen Sie für ein 200-seitiges Lastenheft mit komplexen Use Cases?

**Diskussionsfrage:** Warum ist „ständige Prüfung" theoretisch am besten, aber in der Praxis schwer durchhaltbar?

**Mögliche Anschlussfragen:**
- Wer freigibt das Requirements-Dokument am Ende?
- Wie verhält sich Anforderungsprüfung zur Sprint Review im agilen Kontext?
- Welche Rolle spielen Tools (z. B. Jira, Azure DevOps, DOORS)? *(im PDF nicht definiert)*

## Verwandt

- [[ITPM - Requirements Engineering - Grundlagen]]
- [[ITPM - RE - Anforderungsverwaltung]]
- [[ITPM - Anforderung - Definition]]
- [[ITPM - RE - Dokumentation und Modellierung]]
- [[ITPM - Pflichtenheft]]

## Quelle

- Vorlesung: [[ITPM - VL - Initiierung Strukturierung Requirements]]
- Folien/Seitenangabe: 74–77
