---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - ITIL 4 Grundprinzipien Detail]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - ITIL 4 Grundprinzip - Dort beginnen wo man steht

> [!info] Kurzdefinition
> Zweites der sieben ITIL-Grundprinzipien („Start Where You Are"). Bei Verbesserungen sollten bereits vorhandene Services und Methoden genutzt werden, statt etwas Neues aus dem Nichts zu bauen. Der aktuelle Zustand muss durch direkte Beobachtung möglichst objektiv bewertet werden — Vorsicht bei Messungen (Goodhart-Gesetz).

## Beschreibung

Folien 92–95 der Courseware. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

### Definition (Folie 92)

> „Bei der Beseitigung alter, erfolgloser Methoden oder Services um etwas Besseres zu erschaffen kann die **Versuchung** groß sein, die Errungenschaften der Vergangenheit vollständig **zu entfernen** und etwas völlig Neues aufzubauen.
> Dies ist selten eine kluge Entscheidung und **meistens unnötig**. Im Gegenteil, es kann **höchst unwirtschaftlich** sein, nicht nur in Bezug auf die Zeit, sondern auch hinsichtlich des Verlusts bereits bestehender Services, Prozesse, Mitarbeiter und Werkzeuge, die von entscheidendem Wert für die Verbesserungsbemühungen sein könnten.
> **Machen Sie keinen Neuanfang**, ohne sich vorher zu überlegen, welche bereits verfügbaren Ressourcen genutzt werden könnten."

### Bewerten Sie, wo Sie sind (Folie 93)

> „Bereits vorhandene Services und Methoden sollten direkt gemessen und/oder beobachtet werden, um deren aktuellen Zustand und zur erneuten Verwendung geeignete Komponenten richtig zu verstehen.
> Entscheidungen über die weiteren Vorgehensweise sollten auf möglichst **genauen Informationen** basieren. Beachten Sie, dass zwischen Berichten und der Realität oft **Diskrepanzen** bestehen.
> **Daten von der Quelle** zu erhalten hilft, Annahmen zu vermeiden."

Empfehlungen:
- Aktivitäten direkt beobachten.
- Dass es keine blöden Fragen gibt.
- Diese unterschiedlichen Rollen müssen Teil der Beobachtungen sein und Informationen aus erster Hand erhalten.

### Die Rolle von Messungen (Folie 94)

> „**Die Verwendung von Messungen** ist bei diesem Prinzip wichtig. Sie sollten das, was beobachtet wird, allerdings unterstützen und nicht ersetzen, da eine übermäßige Abhängigkeit von Datenanalysen und Berichten unbeabsichtigt zu Verzerrungen und Risiken bei der Entscheidungsfindung führen kann.
> Organisationen sollten **eine Reihe von unterschiedlichen Techniken** in Erwägung ziehen, um sich Wissen über die Umgebungen anzueignen, in denen sie arbeiten. Auch wenn manche Dinge nur **durch die Messung** ihrer Auswirkungen verstanden werden können, sollte die **direkte Beobachtung** stets die erste Wahl sein.
> Metriken müssen aussagekräftig sein und sich direkt auf das gewünschte Ergebnis beziehen."

> *„Wenn eine Messung zum Ziel wird, ist sie kein gutes Maß mehr."* — **Goodhart-Gesetz**

### Anwenden des Prinzips (Folie 95)

> Ein umfassendes Verständnis des aktuellen Status von Services und Methoden ist wichtig bei der Auswahl der Elemente, die erneut verwendet, geändert oder auf erweitert werden sollen.
> Beachten Sie diese Empfehlungen:
> - Sehen Sie, so objektiv wie möglich **was da ist**, und verwenden Sie das gewünschte Endergebnis als **Ausgangspunkt**.
> - Wenn Beispiele für **erfolgreiche** Practices oder Services **gefunden** werden, **ermitteln** Sie, ob und wie sie **wiederholt** werden können, um den **gewünschten Status** zu erreichen.
> - Nutzen Sie Ihre **Risikomanagement-Fachkenntnisse**.
> - Seien Sie sich bewusst, dass **manchmal keine** der vorhandenen Ressourcen wiederverwendet werden kann.

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Anti-Reflex | Nicht alles wegwerfen und neu bauen — meist unwirtschaftlich |
| Wiederverwendung | Vorhandene Services, Prozesse, Mitarbeiter, Werkzeuge prüfen |
| Direkte Beobachtung | Erste Wahl, vor Berichten und reinen Datenanalysen |
| Messungen | Unterstützen, nicht ersetzen die Beobachtung |
| Goodhart-Gesetz | Vorsicht: Messung-zum-Ziel-Effekt |
| Risk Management | Ist Teil der Bewertung |
| Ehrlichkeit | Manchmal ist tatsächlich nichts wiederverwendbar |

## Beispiel

Krankenhaus-IT plant Modernisierung des Service Desks:
- **Falsch:** „Wir kaufen ein neues Tool und beginnen bei null."
- **Richtig:** Direkt beobachten, wie der Service Desk arbeitet (eine Schicht mitlaufen). Vorhandene KEDB, Klassifizierungssystem, Skripte prüfen. Was funktioniert? Was lässt sich erweitern?
- **Goodhart-Risiko:** Wenn KPI „99 % Tickets in 1h beantwortet" zum Ziel wird, antworten Mitarbeiter unverbindlich („Wir prüfen das"), um die Messung zu erreichen — Wert geht verloren.

## Abgrenzung

- **Dort beginnen, wo man steht vs. CSI-Schritt 2 „Wo stehen wir gerade?"** (siehe [[SM - ITIL Continual Improvement - Modell]]): Eng verwandt — Schritt 2 operationalisiert dieses Prinzip im CSI-Modell.
- **Dort beginnen vs. Greenfield/Brownfield**: Greenfield = bei null beginnen; Brownfield = auf Vorhandenem aufbauen. ITIL bevorzugt klar Brownfield, sofern sinnvoll.
- **Direkte Beobachtung vs. Audit/Reporting**: Audit/Reporting können Berichts-Diskrepanzen enthalten; direkte Beobachtung ist robuster.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet „Dort beginnen, wo man steht"? — Vor jeder Veränderung den Ist-Zustand objektiv erfassen, Vorhandenes prüfen, nicht reflexhaft alles neu bauen.

**Anwendungsfrage:** Welche Vorgehensweisen unterstützen dieses Prinzip? — Direkte Beobachtung, Daten von der Quelle, vielfältige Techniken, Risk Management, ehrliche Anerkennung von Nicht-Wiederverwendbarkeit.

**Diskussionsfrage:** Was ist das Goodhart-Gesetz und wie ist es relevant? — „Wenn eine Messung zum Ziel wird, ist sie kein gutes Maß mehr." Konsequenz: Metriken so wählen, dass sie nicht primär als Steuerungsanreiz wirken, sondern als Indikator. Krankenhaus-Beispiel: Lösungszeiten als KPI können dazu führen, dass Tickets prematur geschlossen werden.

**Mögliche Anschlussfragen:**
- Welche Rolle hat direkte Beobachtung gegenüber Berichten?
- Wie verhält sich dieses Prinzip zur GAP-Analyse?
- In welchem CSI-Schritt ist es zentral verankert? — Schritt 2.

## Verwandt

- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 - Prinzip Interaktion und Relevanz]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - CMMI - Reifegradmodell]]

## Quelle

- Vorlesung: [[SM - VL - ITIL 4 Grundprinzipien Detail]]
- Folien/Seitenangabe: Courseware-Folien 92–95; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
