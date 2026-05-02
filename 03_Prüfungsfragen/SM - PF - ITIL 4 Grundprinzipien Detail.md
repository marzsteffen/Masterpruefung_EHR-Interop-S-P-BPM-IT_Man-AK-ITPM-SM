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

# SM - PF - ITIL 4 Grundprinzipien Detail

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Detail-Karten zu allen sieben ITIL 4-Grundprinzipien (Courseware-Folien 88–115), zur Interaktion der Prinzipien (Folie 81) sowie zum Vergleich mit dem Agilen Manifest (Folie 87). Die Überblicks-Karten (alle 7 Prinzipien benennen, SVS-Einordnung) befinden sich in [[SM - PF - ITIL 4 Grundlagen]]. Relevant für SM (Servicemanagement, FH JOANNEUM eHealth). Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Verlinkte Konzepte

- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 Grundprinzip - Wertorientierung]]
- [[SM - ITIL 4 Grundprinzip - Dort beginnen wo man steht]]
- [[SM - ITIL 4 Grundprinzip - Iterative Weiterentwicklung mit Feedback]]
- [[SM - ITIL 4 Grundprinzip - Zusammenarbeit und Transparenz fördern]]
- [[SM - ITIL 4 Grundprinzip - Ganzheitlich denken und arbeiten]]
- [[SM - ITIL 4 Grundprinzip - Auf Einfachheit und Praktikabilität achten]]
- [[SM - ITIL 4 Grundprinzip - Optimieren und automatisieren]]
- [[SM - ITIL 4 - Prinzip Interaktion und Relevanz]]
- [[SM - ITIL 4 - Vergleich Grundprinzipien vs Agile Manifest]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - Fallstudie - KI Incident Management]]

---

## Karten

### Definition

Was ist der erste Schritt des Grundprinzips „Wertorientierung", und was unterscheidet CX von UX?

?

**Erster Schritt (Folie 69/91):** In jeder Situation bestimmen, **wer der Service-Consumer ist** — und wer die Stakeholder sind. Nicht nur Kunden, sondern alle Gruppen, die Nutzen ziehen.
**Formen von Wert (Folie 89):** Umsatz, Kundentreue, niedrigere Kosten, Wachstumschancen, Produktivitätssteigerung, Risikoreduzierung, neue Märkte, Wettbewerbsfähigkeit. Wert verändert sich über die Zeit.
**CX vs. UX (Folie 90):**
- *Customer Experience (CX):* Gesamtheit der Interaktionen eines **Kunden** mit der Organisation und ihren Produkten — subjektiv und objektiv.
- *User Experience (UX):* Gesamtheit der Interaktionen eines **Anwenders** mit dem Service.
Im Krankenhaus: Pflegekraft = UX-Adressat; Pflegeleitung = CX-Adressat.

---

Was besagt das Goodhart-Gesetz im Kontext von „Dort beginnen, wo man steht", und welche Methode hat Vorrang?

?

**Goodhart-Gesetz (Folie 94):** „Wenn eine Messung zum Ziel wird, ist sie kein gutes Maß mehr." Wird z. B. „Ticket-Lösungszeit < 1h" zum primären KPI, beantworten Mitarbeiter Tickets unverbindlich, um die Metrik zu erfüllen — ohne echten Wert zu liefern.
**Konsequenz:** Metriken sollten Beobachtung unterstützen, nicht ersetzen. Aussagekräftige Metriken mit direktem Ergebnisbezug wählen.
**Methoden-Priorität:** **Direkte Beobachtung** ist die erste Wahl. Berichte und reine Datenanalysen können Diskrepanzen zur Realität enthalten. Daten von der Quelle holen vermeidet Annahmen.

---

Was ist eine Feedbackschleife laut ITIL 4, und welche fünf Feedbackquellen nennt die Courseware?

?

**Feedbackschleife (Folie 97):** Eine Situation, in der ein Teil des **Outputs** einer Aktivität als neuer **Input** derselben oder einer nachgelagerten Aktivität verwendet wird. Feedback muss in der Wertschöpfungskette aktiv gesammelt werden.
**Fünf Feedbackquellen:**
1. Endanwender- und Kundenwahrnehmung des geschaffenen Werts
2. Effizienz und Effektivität von Wertschöpfungskettenaktivitäten
3. Effektivität von Service-Governance und Managementkontrollen
4. Schnittstellen zwischen Organisation und Netzwerk von Partnern und Lieferanten
5. Nachfrage nach Produkten und Services
Timing: Feedback **vor, während und nach** jeder Iteration einholen.

---

Was bedeutet „Zusammenarbeit ≠ Konsens", und welche Stakeholder-Gruppen nennt die Courseware?

?

**Zusammenarbeit ≠ Konsens (Folie 106):** Zusammenarbeit erfordert Information, Verständnis und Vertrauen — aber **kein Konsens** ist notwendig. Entscheidungen können und müssen auch ohne Einstimmigkeit getroffen werden.
**Stakeholder-Gruppen (Folien 102–103):**
- **Kunden** — erste und offensichtlichste Gruppe
- **Entwickler** — arbeiten mit operativen Teams zusammen
- **Lieferanten** — definieren Anforderungen und entwickeln Lösungsideen
- **Relationship-Manager** — verstehen Anforderungen und Prioritäten der Konsumenten
- **Interne und externe Lieferanten** — prüfen gemeinsame Prozesse, identifizieren Optimierungspotenziale
**Silos:** entstehen durch Verhalten *und* strukturelle Ursachen — das Prinzip „Ganzheitlich denken" hilft, sie abzubauen.

---

Welche sechs Schritte umfasst der „Weg zur Optimierung" bei „Optimieren und automatisieren"?

?

Laut Folie 113 (ITIL 4 Foundation Courseware):
1. **Den Kontext verstehen**, in dem die Optimierung erfolgt, und abstimmen
2. **Den aktuellen Zustand** der vorgeschlagenen Optimierung bewerten
3. Auf **zukünftigen Zustand und Prioritäten** einigen (Schwerpunkt: Vereinfachung und Wertschöpfung)
4. **Engagement und Unterstützung der Stakeholder** sicherstellen
5. **Verbesserungen iterativ ausführen** — Messgrößen und Feedback zur Kurskorrektur nutzen
6. **Auswirkungen der Optimierung fortlaufend überwachen** — Verbesserungsmöglichkeiten identifizieren
*Mnemonik:* Kontext → Ist → Soll → Engagement → Iterativ → Überwachen

---

### Anwendung

Wenden Sie das Prinzip „Wertorientierung" auf einen Krankenhaus-IT-Service an: Welche Fragen müssen beantwortet werden?

?

**Service-Beispiel:** Mobiler KIS-Zugang für Pflegekräfte.
**Wer ist der Service-Consumer?** Pflegekraft am Bett.
**Wer sind die Stakeholder?** Pflegekraft (UX), Pflegeleitung (CX), IT-Abteilung, Datenschutzbeauftragter, Patient (mittelbar).
**Warum/Wobei/Wie?** Pflegekraft will am Bett dokumentieren (Outcome); Service hilft, Wegezeiten und Fehler zu reduzieren.
**Wert (Folie 89):** Produktivitätssteigerung (weniger Wegezeiten), Risikoreduzierung (höhere Datenqualität), verringerte negative Auswirkungen (weniger Fehler).
**CX/UX:** Tablet-UX ist entscheidend — ohne gute Bedienbarkeit wird der Service nicht akzeptiert.
**Kontinuität:** Regelmäßig Feedback einholen, nicht nur bei Einführung.

---

Eine Krankenhaus-IT-Abteilung plant, ihren Service Desk neu aufzusetzen. Wie wenden Sie „Dort beginnen, wo man steht" korrekt an?

?

**Falsch (Greenfield-Reflex):** „Wir kaufen ein neues Tool und starten von null." — Laut Folie 92 meist unwirtschaftlich: Verlust vorhandener Prozesse, Mitarbeiter-Know-how und bewährter Strukturen.
**Richtig:**
1. Service-Desk-Alltag **direkt beobachten** (eine Schicht mitlaufen; Folie 93).
2. Bestehende Known Error Database (KEDB), Klassifizierungssystem und Skripte prüfen — was ist wiederverwendbar?
3. **Daten von der Quelle** holen, statt nur Berichte lesen.
4. Erfolgreiche Practices identifizieren und prüfen, ob sie reproduzierbar sind.
5. Ehrlich anerkennen, wenn tatsächlich nichts wiederverwendbar ist (Folie 95).
**Goodhart-Risiko:** KPI „Tickets in 1h gelöst" nicht als alleinige Steuerungsgröße.

---

Wie wenden Sie „Iterative Weiterentwicklung mit Feedback" bei der Einführung einer Telemedizin-Plattform in einem Krankenhaus an?

?

**MVP-Ansatz (Folie 99):** Nicht die komplette Plattform in 12 Monaten entwickeln — stattdessen:
1. **Schritt 1 (MVP):** Pilot in Kardiologie mit 5 Patienten, einfache Video-Konsultation.
2. **Feedback (vor/während/nach Iteration):** Patienten haben Login-Probleme; Ärzte wollen KIS-Schnittstelle.
3. **Schritt 2:** Login vereinfachen + KIS-Anbindung umsetzen.
4. **Schritt 3:** Skalierung auf weitere Fachbereiche.
**Warum:** „Schnell ≠ unvollständig" (Folie 99) — MVP ermöglicht maximales Lernen mit minimalem Aufwand. Das Gesamtprogramm wird bei jedem Schritt neu bewertet.
**Risiko ohne Iteration:** Wasserfall-Entwicklung → Anforderungen veraltet, Akzeptanz unklar bei Auslieferung.

---

Ein Krankenhaus-IT-Leiter möchte einen Change-Request-Prozess vereinfachen. Welche Zielkonflikte treten typischerweise auf, und wie löst ITIL 4 sie?

?

**Typischer Zielkonflikt (Folie 110):** Management möchte umfangreiche Datenmenge für Entscheidungen; Mitarbeiter wollen einfache Records mit minimaler Dateneingabe.
**ITIL-4-Lösung:**
- Services nur Daten generieren lassen, die echten Entscheidungswert bieten.
- Records vereinfachen und nach Möglichkeit automatisieren.
- Ausnahmen-Regelung (Folie 109): allgemeine Regeln für Ausnahmen aufstellen, nicht jeden Sonderfall einzeln abbilden.
**Krankenhaus-Praxis:** Standard-Changes vorautorisieren (kein Komitee); Normal-Changes mit definiertem CAB; Notfall-Changes beschleunigt. Jeder Prozessschritt auf Wertbeitrag geprüft — nicht-wertschöpfende Schritte entfernen.

---

Wenden Sie die 6 Optimierungsschritte auf die KI-gestützte Ticket-Klassifizierung im Krankenhaus an.

?

**Aus [[SM - Fallstudie - KI Incident Management]]:**
1. **Kontext:** 46.000 Tickets/Jahr; manueller Klassifizierungsaufwand am 1st Level zu hoch.
2. **Ist-Zustand:** ø 2 Min. Klassifizierung; 15 % Fehlklassifikationsrate.
3. **Soll-Zustand:** ø 30 Sek.; Fehlrate < 5 %.
4. **Engagement:** Service Desk, Datenschutz, Pflege/Ärzte als Stakeholder einbinden.
5. **Iterativ:** Pilot mit einer Applikationsklasse → Feedback → Modell verbessern → Skalierung.
6. **Überwachen:** Monatliche Messung; Modell bei Drift nachtrainieren.
**Reihenfolge:** Erst Klassifizierungsprozess **optimieren** (ggf. reduzieren, vereinfachen), dann KI-Automatisierung — nie umgekehrt (automatisierte Verschwendung skaliert Probleme).

---

### Diskussion

Ordnen Sie die vier Werte des Agilen Manifests den ITIL 4-Grundprinzipien zu (laut Folie 87).

?

| Agile Manifest | ITIL 4-Grundprinzipien |
|---|---|
| **Mensch und Interaktionen** über Prozesse und Werkzeuge | Auf Einfachheit und Praktikabilität achten · Dort beginnen, wo man steht |
| **Funktionierende Software** über umfassende Dokumentation | Wertorientierung · Ganzheitlich denken und arbeiten |
| **Mitwirkung des Kunden** über Vertragsverhandlungen | Wertorientierung · Zusammenarbeit und Transparenz fördern |
| **Auf Veränderung reagieren** über Planverfolgung | Iterative Weiterentwicklung mit Feedback · Auf Einfachheit und Praktikabilität achten |

**Hinweis:** Das siebte Prinzip „Optimieren und automatisieren" ist in der Folie-87-Tabelle **nicht explizit zugeordnet** (im PDF nicht zugeordnet).

---

Sind ITIL 4 und Agile kompatibel? Welche ITIL-Practices profitieren laut Courseware besonders von Agile?

?

**Kompatibilität:** Ja — ITIL 4 wurde explizit als Brücke zu Agile/DevOps konzipiert (im Gegensatz zu ITIL V3, das dafür kritisiert wurde). Folie 84: „ITIL kann Agile-Teams ergänzen durch effektivere, schnellere und stabilere Bereitstellung."
**Practices, die von Agile profitieren (Folie 84):**
- Continual Improvement
- Problem Management
- Change Enablement
- Release Management
- Deployment Management
**Spannungsfeld:** ITIL bringt Stabilität (Change Governance, SLAs); Agile bringt Geschwindigkeit. Bei klarer Rollenaufteilung (DevOps-Pipeline mit ITIL-Gates) komplementär. Bei rein zeremonieller ITIL-Umsetzung entstehen Reibung und Bürokratie.

---

Welche Agile-Rollen entsprechen laut Courseware welchen ITSM-Rollen?

?

Laut Folie 86 (ITIL 4 Foundation Courseware):

| Agile-Rolle | ITSM-Rolle |
|---|---|
| Produktmanager / Produkteigentümer | **Service-Eigentümer** |
| Scrum-Master | **Change Manager** |
| Scrum-Master (Retrospektiven) | **Kontinuierliche Verbesserung** (Continual Improvement) |

Hintergrund: Scrum-Master führen bereits Retrospektiven durch und sorgen für Lessons Learned — das ist Kerntätigkeit des Continual Improvement. Produkteigentümer verantworten Outcomes und Backlogs — analog zur Service-Owner-Rolle.

---

Warum darf nicht ohne vorherige Optimierung automatisiert werden? Was ist die Reihenfolge laut ITIL 4?

?

**Reihenfolge (Folie 115):** Erst Standardisieren → Optimieren → dann Automatisieren.
**Begründung:** Wird ein schlechter Prozess automatisiert, skaliert man seine Probleme statt sie zu lösen — automatisierte Verschwendung läuft schneller, aber nicht besser.
**Voraussetzung für Automatisierung:** Standardisierung. Wiederkehrende, standardisierte Aufgaben lassen sich automatisieren; Ausnahmen und Sonderfälle zuerst durch Prozess-Design reduzieren.
**Mensch im Loop (Folie 112):** ITIL 4 fordert explizit, dass Technologie **ohne die Möglichkeit menschlichen Eingreifens** nicht verwendet werden soll — keine vollständige Black-Box-Automatisierung.
**Vorteile nach Optimierung+Automatisierung:** Kosteneinsparung, Fehlerreduktion, bessere Mitarbeitererfahrung.

---

Welche vier anderen Grundprinzipien müssen laut Courseware bei der Anwendung von „Optimieren und automatisieren" zusätzlich beachtet werden?

?

Laut Folie 115 (ITIL 4 Foundation Courseware):

1. **Iterative Weiterentwicklung mit Feedback** — iterative Optimierung und Automatisierung machen Fortschritte sichtbar und erhöhen das Stakeholder-Buy-In.
2. **Auf Einfachheit und Praktikabilität achten** — Dinge können einfach sein, aber nicht optimiert. Prinzipien zusammen anwenden.
3. **Wertorientierung** — die Auswahl, was wie optimiert/automatisiert wird, auf dem bestmöglichen Wert für Konsumenten basieren.
4. **Dort beginnen, wo man steht** — bereits Vorhandenes, aber unzureichend Genutztes nutzen, um Optimierungs- und Automatisierungsmöglichkeiten schnell und wirtschaftlich umzusetzen.

Dies illustriert das übergeordnete Prinzip: Die sieben Grundprinzipien wirken als **Netzwerk**, nicht als unabhängige Liste.

---

Welche Risiken entstehen, wenn eine Organisation nur ein oder zwei Grundprinzipien anwendet?

?

**Grundregel (Folie 81):** Die Grundprinzipien interagieren miteinander und sind voneinander abhängig. Organisationen sollen alle prüfen und gemeinsam einsetzen.
**Beispiele für isolierte Anwendung:**
- **Nur „Optimieren und automatisieren"** ohne Wertorientierung → Effizienzgewinne ohne Kundennutzen; ohne „Dort beginnen" → Automatisierung von Neuem statt Vorhandenem.
- **Nur „Iterative Weiterentwicklung"** ohne „Ganzheitlich denken" → lokale Optimierungen ohne Systemsicht; blinde Flecken in anderen Dimensionen.
- **Nur „Einfachheit"** ohne „Ganzheitlich denken" → Prozesse zu vereinfacht, wichtige Dimensionen (Partner, Informationen) ausgeblendet.
**Fazit:** Kein Prinzip ist hierarchisch übergeordnet — alle sind situationsspezifisch relevant und kohärent anzuwenden.

---

Wie balanciert man die Prinzipien „Ganzheitlich denken" und „Auf Einfachheit achten" in einem komplexen Krankenhaus-IT-Projekt?

?

**Spannungsfeld:** Ganzheitlichkeit verlangt, alle vier Dimensionen und Stakeholder zu berücksichtigen — das erzeugt Komplexität. Einfachheit verlangt, unnötige Schritte zu eliminieren — das droht Dimensionen auszublenden.
**Auflösung (Folie 108 + 109-111):**
- *Ganzheitlich denken:* Komplexitätsbewusstsein — unterschiedliche Heuristiken für einfache vs. komplexe Systeme. In komplexen Systemen (z. B. KIS-Migration) Änderungsauswirkungen auf andere Elemente analysieren und einplanen.
- *Einfachheit:* Nur so viele Schritte wie absolut nötig. Nicht jeden Sonderfall einzeln abbilden — allgemeine Ausnahmenregeln aufstellen.
- **Balance:** Systemisch denken, aber gezielt vereinfachen. Ganzheitlichkeit verhindert blinde Flecken; Einfachheit verhindert Overengineering. Beispiel: alle vier Dimensionen prüfen, aber für jede nur die relevanten Aspekte designen, nicht alles.

---

## Mögliche Anschlussfragen des Prüfers

- Welchen ersten Schritt verlangt Wertorientierung laut Folie 69? (Service-Consumer bestimmen)
- Was ist Goodhart-Gesetz, und welches Prinzip macht es relevant?
- Welche Vorteile bietet zeitgesteuertes, iteratives Arbeiten mit Feedbackschleifen (Folie 98)?
- Was ist DevOps, und wie unterscheidet es sich von Agile?
- Welches Prinzip ist in der Agile-Manifest-Tabelle **nicht** explizit zugeordnet?
- Wie hängen die Sieben Grundprinzipien mit dem CSI-Modell zusammen (Folie 122 Hauptfoliensatz)?
- Welche Practices sind laut Courseware für Optimierung unerlässlich?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
