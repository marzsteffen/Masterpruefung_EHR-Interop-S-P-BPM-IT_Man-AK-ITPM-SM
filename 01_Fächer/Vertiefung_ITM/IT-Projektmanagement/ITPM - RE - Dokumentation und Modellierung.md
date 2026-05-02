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

# ITPM - RE - Dokumentation und Modellierung

> [!info] Kurzdefinition
> Anforderungen können auf drei Wegen dokumentiert werden: **Schreiben** (textlich), **Malen** (grafisch via UML/BPMN) und **Vorzeigen** (Prototyping). Modellierungssprachen: Use-Case-Modellierung, UML-Aktivitätsdiagramm, Zustandsdiagramm, UML-Sequenzdiagramm. Requirements-Dokumente folgen einer Standardgliederung.

## Beschreibung

### Drei Dokumentationswege (Folie 67)

| Weg | Funktion | Methoden |
|---|---|---|
| **Schreiben** | Anforderungen auf Papier bringen, präzise und im Detail. | Textuelle Spezifikation. |
| **Malen** | Guten Überblick schaffen via grafischer Darstellung. | UML, BPMN. |
| **Vorzeigen** | Prüfen, ob alles richtig verstanden wurde; erste Tests. | Prototypen. |

### Modellierungstypen

#### Use-Case-Modellierung (Folie 68)

- Gewünschte Abläufe als **Ellipsen**.
- Auslöser als **Strichmännchen** (Akteure).
- Soll einen **Überblick über die Systemfunktionalität** geben.

#### UML-Aktivitätsdiagramme (Folie 69)

- Zählen auch **BPMN-Modelle** dazu.
- Beschreiben Abläufe **Schritt für Schritt**.
- Bilden auch **Verzweigungen** und **Wiederholungen** ab.

#### Zustandsdiagramme (Folie 70)

- Eingesetzt, wenn der Ablauf **nicht linear** abbildbar ist und durch interne und externe Ereignisse gestört werden kann.
- Beschreiben, in welchem **Zustand** sich das System befinden kann.
- Bilden ab, welche Funktionen in bestimmten Zuständen ausgeführt werden sollen.

#### UML-Sequenzdiagramm (Folie 71)

- **Schritt für Schritt** modelliert, was ein System in einem **konkreten Fall** als nächstes tun soll.

### Gliederung von Requirements-Dokumenten (Folie 72)

Folgende Kapitel sollten enthalten sein:

- Die **Projektziele**
- **Abgrenzung** des zu entwickelnden Systems von seiner Umgebung (Kenntnis über Grenze und externe Schnittstellen)
- Die **drei Arten von Anforderungen**: funktionale, Qualitätsanforderungen, Randbedingungen
- Ein **Glossar** (gute Begriffsdefinitionen sind essenzieller Bestandteil)
- Ein **Abkürzungsverzeichnis**

## Beispiel

*Im PDF nicht durch konkretes Diagramm-Beispiel mit Inhalt illustriert.* Schaubilder ohne textuelle Erläuterung.

## Abgrenzung

- **Schreiben** vs. **Malen**: Text liefert Detail, Grafik liefert Überblick. Beide ergänzen sich.
- **Use Case** ≠ **User Story** ([[ITPM - Agile - User Story]]): Use Case ist detailliert mit Akteuren und Ablauf; User Story ist kurz im Format „Als …".
- **UML-Aktivitätsdiagramm** und **BPMN** überlappen funktional, kommen aber aus unterschiedlichen Communities (Software vs. Business Process).
- **Zustandsdiagramm** ist State-Machine-orientiert; **Sequenzdiagramm** ist Nachrichten-/Interaktionsorientiert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Dokumentationswege gibt es im RE? Welche UML-Diagrammtypen werden für welche Fragestellung eingesetzt?

**Anwendungsfrage:** Sie modellieren ein Patientenportal: Welches Diagramm wählen Sie für (a) den Login-Ablauf, (b) die Zustände einer Terminbuchung, (c) den Use Case „Befund einsehen"?

**Diskussionsfrage:** Wann ist welche Dokumentationsform übertrieben, wann unzureichend? Wie verhält sich der Aufwand zur Komplexität?

**Mögliche Anschlussfragen:**
- Welche Gemeinsamkeiten/Unterschiede haben UML-Aktivitätsdiagramm und BPMN?
- Welche Rolle spielen Glossar und Abkürzungsverzeichnis – warum nicht im Anhang?
- Verbindung zum BPM-Fach ([[BPM - MOC]])?

## Verwandt

- [[ITPM - Requirements Engineering - Grundlagen]]
- [[ITPM - RE - Erhebungstechniken]]
- [[ITPM - Anforderung - Definition]]
- [[ITPM - Lastenheft]]
- [[ITPM - Pflichtenheft]]
- [[ITPM - Agile - User Story]]
- [[BPM - MOC]]

## Quelle

- Vorlesung: [[ITPM - VL - Initiierung Strukturierung Requirements]]
- Folien/Seitenangabe: 67–72
