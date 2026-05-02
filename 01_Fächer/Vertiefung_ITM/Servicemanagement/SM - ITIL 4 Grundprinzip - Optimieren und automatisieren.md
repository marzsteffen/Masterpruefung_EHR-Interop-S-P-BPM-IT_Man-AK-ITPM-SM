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

# SM - ITIL 4 Grundprinzip - Optimieren und automatisieren

> [!info] Kurzdefinition
> Siebtes der sieben ITIL-Grundprinzipien („Optimize and Automate"). Organisationen sollen den Wert ihrer Aktivitäten maximieren — durch Optimierung *vor* Automatisierung. Standardisierung unterstützt Automatisierung. Das Vier-Dimensionen-Modell hilft bei der ganzheitlichen Sicht; Automatisierung darf nicht ohne menschlichen Eingriff erfolgen.

## Beschreibung

Folien 112–115 der Courseware. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

### Definition (Folie 112)

> „Organisationen müssen den **Wert** der durch ihre personellen und technischen Ressourcen ausgeführten **Aktivitäten maximieren**.
> Das **Vier-Dimensionen-Modell** bietet eine ganzheitliche Sicht auf die verschiedenen Einschränkungen, Ressourcentypen und andere Bereiche, die bei der Gestaltung, Verwaltung oder dem Betrieb einer Organisation berücksichtigt werden sollten.
> Technologie kann Organisationen bei der Erweiterung unterstützen, nichtsdestotrotz sollte man sich **nicht auf eine Technologie ohne die Möglichkeit menschlichen Eingreifens verlassen**.
> Bevor sie effektiv automatisiert werden können, sollten Aktivitäten **optimiert** werden. Optimierung bedeutet, etwas innerhalb eines fest gesetzten Rahmens so effektiv und nützlich zu machen wie nötig."

### Der Weg zur Optimierung (Folie 113)

> „Es gibt viele Möglichkeiten, wie Practices und Services optimiert werden können.
> Die Practices **‚Continual Improvement'** und **‚Measurement and Reporting'** sind dafür unerlässlich. Die spezifischen Practices können sich auf Leitlinien von ITIL, Lean, DevOps, Kanban und anderen Quellen stützen. Unabhängig von den spezifischen Techniken folgt der Weg zur Optimierung diesen allgemeinen **Schritten**:
>
> 1. **Den Kontext verstehen**, in dem die vorgeschlagene Optimierung erfolgt, und sich entsprechend abstimmen.
> 2. **Den aktuellen Zustand** der vorgeschlagenen Optimierung **bewerten**.
> 3. Darauf einigen, was der **zukünftige Zustand und die Prioritäten der Organisation** sein sollten, wobei der Schwerpunkt auf Vereinfachung und Wertschöpfung liegt.
> 4. Sicherstellen, dass für die Optimierung **ein angemessenes Maß an Engagement und Unterstützung der Stakeholder** vorhanden ist.
> 5. **Verbesserungen auf iterative Weise ausführen.** Verwenden Sie Messgrößen und anderes Feedback, um den Fortschritt zu überprüfen, den Kurs zu halten und den Ansatz zur Optimierung bei Bedarf anzupassen.
> 6. **Die Auswirkungen der Optimierung fortlaufend überwachen.** Dies erleichtert es, Möglichkeiten zur Verbesserung der Arbeitsmethoden zu identifizieren."

### Automatisierung verwenden (Folie 114)

> „Unter Automatisierung versteht man typischerweise den **Einsatz von Technologie**, um einen Schritt oder eine Reihe von Schritten korrekt und kontinuierlich mit begrenztem oder keinem menschlichen Eingreifen auszuführen.
> So beispielsweise in Organisationen, denen es um eine **kontinuierliche Weiterentwicklung** geht, durch **Live-Tests** und häufig **automatische Prüfungen**, die in jeder Umgebung vorkommen.
> In ihrer einfachsten Form könnte Automatisierung jedoch auch Standardisierung und Rationalisierung **manueller Tätigkeiten** bedeuten. Effizienz lässt sich erheblich steigern, indem man den Bedarf an **menschlicher Beteiligung verringert**, um jeden Teil eines Prozesses zu stoppen und zu bewerten.
> Gelegenheiten zur Automatisierung lassen sich im gesamten Unternehmen finden. **Standards und wiederkehrende Aufgaben** zu automatisieren kann dazu beitragen, der Organisation **Kosten** einzusparen, menschliche **Fehler** zu reduzieren und die **Mitarbeitererfahrung** zu verbessern."

### Anwenden des Prinzips (Folie 115)

- **Vereinfachen und/oder optimieren Sie Vorgänge, bevor Sie automatisieren.** Nehmen Sie sich Zeit, die standardmässigen und wiederkehrenden Prozesse so weit wie möglich abzubilden und zu rationalisieren (zu optimieren). Dann können Sie mit der Automatisierung beginnen.
- **Definieren Sie Ihre Messgrössen.** Verwenden Sie dieselben Messgrössen, um die Baseline zu definieren und die erreichten Ergebnisse zu messen. Stellen Sie sicher, dass die Messgrössen ergebnis- und wertorientiert sind.
- **Beachten Sie auch die anderen Grundprinzipien, wenn Sie dieses anwenden:**
  - **Iterative Weiterentwicklung mit Feedback.** Iterative Optimierung und Automatisierung machen Fortschritte sichtbar und erhöhen das Buy-In der Stakeholder.
  - **Auf Einfachheit und Praktikabilität achten.** Die Dinge können einfach sein, aber nicht optimiert. Verwenden Sie also die Prinzipien zusammen.
  - **Wertorientierung.** Die Auswahl, was wie optimiert und automatisiert werden könnte, sollte auf dem bestmöglichen Wert basieren.
  - **Dort beginnen, wo man steht.** Nutzen Sie bereits Vorhandenes, aber nicht oder unzureichend genutztes, um Optimierungs- und Automatisierungsmöglichkeiten schnell und wirtschaftlich umzusetzen.

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Wert maximieren | Personelle und technische Ressourcen |
| Vier-Dimensionen-Sicht | Ganzheitlich design, manage, operate |
| Mensch im Loop | Keine Technologie ohne menschlichen Eingriff |
| Erst optimieren, dann automatisieren | Reihenfolge entscheidend |
| Optimierungs-Schritte (6) | Kontext → Ist → Soll → Engagement → iterativ → überwachen |
| Standardisierung | Voraussetzung für Automatisierung |
| Anwendung anderer Prinzipien | Iterativ + Feedback, Einfachheit, Wert, Dort beginnen |

## Beispiel

Krankenhaus-IT führt KI-gestützte Ticket-Klassifizierung ein (siehe [[SM - Fallstudie - KI Incident Management]]):

1. **Kontext verstehen:** 46.000 Tickets/Jahr, manueller Klassifizierungsaufwand am 1st Level zu hoch.
2. **Ist-Zustand:** Klassifikation dauert ø 2 Min. pro Ticket; Fehlklassifikationsrate 15 %.
3. **Soll-Zustand:** ø 30 Sek., Fehlklassifikation < 5 %.
4. **Engagement:** Service Desk, Datenschutz, Pflege/Ärzte als Stakeholder einbinden.
5. **Iterativ:** Pilot mit 1 Applikationsklasse, Feedback, Modell-Verbesserung, Skalierung.
6. **Überwachen:** Monatlich messen, Modell nachtrainieren.

Vorher *nicht* automatisieren (z. B. Tickets ohne Optimierung in eine schlechte KI werfen) — sonst Verschwendung in Hochgeschwindigkeit.

## Abgrenzung

- **Optimieren ≠ Automatisieren**: Optimierung kann auch ohne Automatisierung erfolgen (z. B. Prozessvereinfachung). Automatisierung ohne vorherige Optimierung ist gefährlich.
- **Standardisierung vs. Automatisierung**: Standardisierung schafft die Voraussetzung; Automatisierung ist die Ausführung mittels Technologie.
- **Mensch im Loop vs. Vollautomatisierung**: ITIL 4 fordert explizit menschlichen Eingriff als Möglichkeit — keine vollständige Black-Box.
- **Beziehung zu CSI** (siehe [[SM - ITIL Continual Improvement - Modell]]): Die 6 Optimierungs-Schritte sind eng verwandt mit dem CSI-Modell (Vision/Ist/Soll/Plan/Aktiv/Evaluation).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet „Optimieren und automatisieren"? — Wert maximieren durch Optimierung vor Automatisierung; Standardisierung als Voraussetzung; Vier-Dimensionen-Modell als Designhilfe; Mensch muss eingreifen können.

**Anwendungsfrage:** Welche 6 Schritte hat der „Weg zur Optimierung"? — Kontext verstehen → Ist bewerten → Soll einigen → Engagement sichern → iterativ ausführen → Auswirkungen überwachen.

**Diskussionsfrage:** Warum darf nicht ohne Optimierung automatisiert werden? — Automatisierte Verschwendung skaliert die Probleme statt sie zu lösen. Ein schlechter Prozess wird durch Automatisierung schneller, nicht besser.

**Mögliche Anschlussfragen:**
- Welche Practices sind für Optimierung unerlässlich? — Continual Improvement und Measurement and Reporting.
- Welche anderen Frameworks/Methoden werden als Quellen genannt? — ITIL, Lean, DevOps, Kanban.
- Welche Vorteile bringt Automatisierung typischerweise? — Kosten, Fehlerreduktion, bessere Mitarbeitererfahrung.
- Welche anderen Grundprinzipien sind bei Anwendung dieses Prinzips zu beachten? — Iterative Weiterentwicklung mit Feedback, Auf Einfachheit achten, Wertorientierung, Dort beginnen.

## Verwandt

- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 - Prinzip Interaktion und Relevanz]]
- [[SM - ITIL 4 - Four Dimensions]]
- [[SM - ITIL 4 Grundprinzip - Iterative Weiterentwicklung mit Feedback]]
- [[SM - ITIL 4 Grundprinzip - Auf Einfachheit und Praktikabilität achten]]
- [[SM - ITIL 4 Grundprinzip - Wertorientierung]]
- [[SM - ITIL 4 Grundprinzip - Dort beginnen wo man steht]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - Fallstudie - KI Incident Management]]

## Quelle

- Vorlesung: [[SM - VL - ITIL 4 Grundprinzipien Detail]]
- Folien/Seitenangabe: Courseware-Folien 112–115; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
