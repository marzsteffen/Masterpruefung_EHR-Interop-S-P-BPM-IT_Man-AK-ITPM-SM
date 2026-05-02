---
fach: sm
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/sm
---

# SM - PF - Continual Improvement

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Karten zum Continual Service Improvement (CSI) Modell: 6+1 Schritte, Hilfsmethoden, Guiding Principles-Bezug und Abgrenzung zu verwandten Konzepten. Quelle: Folien 107–122 (ITIL 4 Foundation Courseware, Axelos / Van Haren Publishing 2019). Relevant für SM (Servicemanagement, FH JOANNEUM eHealth).

## Verlinkte Konzepte

- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - ITIL 4 - Service Value System]]
- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - SWOT-Analyse]]
- [[SM - CMMI - Reifegradmodell]]
- [[SM - ITIL V3 - Servicelebenszyklus]]

---

## Karten

### Definition

Nennen Sie die 6+1 Schritte des CSI-Modells mit den zugehörigen Leitfragen.

?

**Das CSI-Modell (Folie 110):**

| Schritt | Leitfrage | Aktivität |
|---|---|---|
| 1 | Was ist unsere Vision? | Business Vision, Mission und Ziele definieren |
| 2 | Wo stehen wir gerade? | Current State Assessment durchführen |
| 3 | Wo wollen wir hin? | Messbare Ziele mit CSFs und KPIs festlegen |
| 4 | Wie kommen wir dort hin? | Verbesserungsplan (iterativ) definieren |
| 5 | Aktiv werden | Verbesserungsaktionen ausführen |
| 6 | Sind wir angekommen? | KPIs und Zielerreichung evaluieren |
| (Klammer) | Wie halten wir unsere Services in Schwung? | Kontinuierliche Kontinuität sicherstellen |

**Merkhilfe:** Vision → Ist → Soll → Plan → Aktion → Evaluation (+ Kontinuität als permanente Rahmenfrage).

---

Warum ist Continual Improvement in ITIL 4 notwendig — welche drei Begründungen nennt die Vorlesung?

?

**Warum CSI? (Folie 107):**

1. **Geschäftsumfeld und Kundenanforderungen ändern sich ständig** — der Service Provider muss sich kontinuierlich anpassen, sonst verliert er den Bezug zu aktuellen Bedürfnissen.

2. **Technologie ändert sich ständig** — ohne Anpassung sind Services schnell veraltet und wettbewerbsunfähig.

3. **Services müssen kontinuierlich auf Verbesserungsmöglichkeiten geprüft werden** — andernfalls verlieren sie an Wert für den Kunden.

**ITIL-4-Strukturelle Verortung:** Continual Improvement ist sowohl eine der fünf SVS-Komponenten (neben Guiding Principles, Governance, SVC und Practices) als auch eine eigenständige **General Management Practice**.

---

Welche Methoden und Techniken nennt der Foliensatz als Hilfsmittel für CSI?

?

**Methoden für Continual Improvement (Folie 109):**
- **Balanced Scorecard** — ausgewogene Leistungsmessung über mehrere Perspektiven
- **Lean-Management** — Reduzierung von Verschwendung
- **Multi-Phasen-Projekte** — strukturierte Umsetzung komplexer Verbesserungen
- **Reifegrad-Assessments** (z. B. CMMI) — Bewertung des aktuellen Prozessreifegrads
- **DevOps** — Verbesserung durch enge Dev/Ops-Zusammenarbeit
- **SWOT-Analyse** — Stärken, Schwächen, Chancen, Risiken (Hilfsmethode in Schritt 3)
- **Continual Service Improvement Modell** (das 6+1-Schritte-Modell selbst)
- **Inkrementelle agile Verbesserung** — iteratives Vorgehen in kleinen Schritten

---

Was ist eine GAP-Analyse im CSI-Kontext, und wie sieht ein Beispiel aus Schritt 3 aus?

?

**GAP-Analyse (Folie 114–115):**
Identifikation und Priorisierung von Verbesserungsmöglichkeiten durch Vergleich von Desired State und Current State.

**Beispiel aus Folie 115 — Verbesserungspotenzial „Erhöhung Kundenzufriedenheit":**

| Dimension | Desired State | Current State | Action Steps |
|---|---|---|---|
| Zufriedenheit | 99 % | unbekannt | Aktuelle Zufriedenheit erheben |
| Lösungszeit | 3 Tage | 6 Tage | Eskalationsprozess adaptieren; Helpdesk-MA einschulen |

**Im CSI-Modell:** GAP-Analyse ist zentrales Werkzeug in **Schritt 3 (Wo wollen wir hin?)** — sie überbrückt Ist-Zustand (Schritt 2) und Soll-Zustand (Schritt 3) und erzeugt konkrete Action Steps für Schritt 4.

---

### Anwendung

Wenden Sie alle sechs CSI-Schritte auf die Initiative „Pflegekraft-Zufriedenheit mit IT erhöhen" an.

?

**Krankenhaus-CSI-Anwendung:**

| Schritt | Konkreter Inhalt |
|---|---|
| **1 Vision** | „Pflegekraft als zufriedener IT-Service-Konsument; IT als verlässlicher Partner im Klinikalltag." |
| **2 Ist** | Zufriedenheit derzeit unbekannt; mittlere Ticket-Lösungszeit 6 Tage; hohe Eskalationsrate bei KIS-Problemen. |
| **3 Soll** | 99 % Kundenzufriedenheit; Lösungszeit ≤ 3 Tage; keine Eskalation wegen fehlender Schulung. KPI: Monatliche Kurzbefragung + Ticket-Auswertung. |
| **4 Plan** | Eskalationsprozess überarbeiten; Helpdesk-Schulungsplan erstellen; Zufriedenheitsumfrage aufsetzen; Zeitrahmen 3 Monate. |
| **5 Aktion** | Schulungen durchführen; neuen Eskalationspfad kommunizieren; Umfragen monatlich senden. Change Enablement für Prozessänderung nutzen. |
| **6 Evaluation** | Nach 6 Monaten KPIs messen: Zufriedenheitsscore, Lösungszeit, Eskalationsrate. Ziele erreicht? Nächste Iteration planen. |
| **(Kontinuität)** | Quartalsweise Review-Meeting; CSI-Zyklus läuft dauerhaft weiter. |

---

Ordnen Sie den drei ITIL-4-Guiding-Principles dem passenden CSI-Schritt zu: „Wo anfangen", „Feedback geben" und „Ganzheitlich denken".

?

**Guiding Principles im CSI-Modell (vgl. Folie 122):**

| Guiding Principle | Zugehöriger CSI-Schritt | Begründung |
|---|---|---|
| **Dort anfangen, wo man ist** | **Schritt 2 — Ist-Zustand** | Kein Re-Start von null; bestehende Assessments, Daten und Fähigkeiten nutzen. Schritt 2 baut auf dem, was schon da ist. |
| **Feedback einholen und weiterentwickeln** | **Schritt 6 — Evaluation + Klammer** | KPIs messen, Ergebnisse bewerten, nächste Iteration vorbereiten. Das Feedback aus Schritt 6 speist Schritt 1 der nächsten Runde. |
| **Ganzheitlich denken und arbeiten** | **Schritt 3/4 — Soll + Plan** | Verbesserungsmaßnahmen dürfen nicht isoliert optimiert werden; alle vier Dimensionen (People, Process, Technology, Partners) müssen im Plan berücksichtigt sein. |

*Hinweis: Der Foliensatz zeigt eine vollständige Zuordnungstabelle aller 7 Grundprinzipien zu CSI-Schritten auf Folie 122.*

---

Welche vier ITIL-Practices werden in Schritt 5 des CSI-Modells explizit als wichtig genannt — und warum?

?

**Schritt 5 — Aktiv werden (Folie 120):**

Für diesen Schritt sollen folgende Practices verstanden und eingesetzt werden:

| Practice | Relevanz in Schritt 5 |
|---|---|
| **Change Enablement** | Verbesserungsmaßnahmen sind oft Changes — sie müssen autorisiert, bewertet und gesteuert werden |
| **Measurement and Reporting** | Wirksamkeit der Maßnahmen muss gemessen und berichtet werden |
| **Risk Management** | Umsetzungsrisiken der Verbesserungsmaßnahmen identifizieren und steuern |
| **Continual Improvement** | Die Practice selbst — strukturiertes Vorgehen nach dem CSI-Modell |

**Prüfungsrelevanz:** Diese vier Practices zeigen, dass CSI kein isolierter Prozess ist, sondern in das Gesamtgefüge der ITIL-4-Practices eingebettet ist.

---

### Diskussion

Warum ist Schritt 2 des CSI-Modells (Ist-Zustand erheben) der kritischste Schritt — und was passiert, wenn man ihn überspringt?

?

**Kritik von Schritt 2 aus dem Foliensatz:**
> „Ohne diesen Schritt fehlt die grundlegende Messlinie zur Zielerreichung — *Startpunkt muss bekannt sein!*"

**Was passiert ohne Schritt 2:**

1. **Keine Baseline → keine Messung:** Wenn der Ist-Zustand unbekannt ist, kann nach der Verbesserungsmaßnahme nicht festgestellt werden, ob Fortschritt erzielt wurde. KPIs in Schritt 6 sind sinnlos ohne Referenzpunkt.

2. **Ressourcenverschwendung:** Maßnahmen werden definiert, ohne zu wissen, welche Probleme real existieren — Gefahr, am eigentlichen Problem vorbeizuarbeiten.

3. **GAP-Analyse unmöglich:** Eine sinnvolle GAP-Analyse (Schritt 3) braucht beide Pole: Desired State und Current State. Ohne Current State fehlt eine Hälfte.

4. **Organisationales Lernen unmöglich:** Die Organisation kann nicht aus Erfahrung lernen, wenn sie den Ausgangspunkt ihrer Verbesserungsinitiativen nicht kennt.

**Krankenhaus-Beispiel:** Initiative „Ticketbearbeitung beschleunigen" ohne vorherige Messung der aktuellen Lösungszeit → nach 6 Monaten: „Wir glauben, dass es besser ist" — aber kein Nachweis möglich. IT-Controlling und Geschäftsführung akzeptieren das nicht.

---

Wie hängen CSI und Problem Management zusammen — und wo überschneiden sich beide Practices?

?

**Parallelen:**
- Problem Management identifiziert wiederkehrende Incidents (Muster) → erzeugt Known Errors → Change Requests
- CSI identifiziert Servicelücken (GAP) → erzeugt Verbesserungspläne → Change Requests
- Beide nutzen **Trendanalysen**, um systematische Schwächen zu finden

**Zusammenspiel:**
- Problem Management liefert **Inputdaten** für CSI Schritt 2 (Ist-Analyse): welche Probleme traten wie oft auf?
- CSI Schritt 3 kann Problemlösung als Verbesserungsziel aufnehmen: „Häufigkeit von DB-Incidents auf null reduzieren"
- Schritt 5 (Aktiv werden) nutzt Change Enablement — das ist auch der Output von Problem Managements Error Control

**Wesentlicher Unterschied:**
- Problem Management: reaktiv/proaktiv auf konkrete Incidents bezogen; Ziel = Ursache beheben
- CSI: strategisch; Ziel = gesamtheitliche Verbesserung von Services, Processes, Practices — nicht nur Incident-getrieben

---

## Mögliche Anschlussfragen des Prüfers

- Was ist der Unterschied zwischen CSI als SVS-Komponente und Continual Improvement als Practice?
- Welche Methode ist in Schritt 2 besonders geeignet, um den Reifegrad von IT-Prozessen zu messen?
- Wie verhält sich das CSI-Modell zum PDCA-Zyklus (Deming)?
- Was sind CSFs und KPIs — und wie hängen beide zusammen?
- Warum ist „inkrementelle agile Verbesserung" als Methode für CSI besonders geeignet?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
