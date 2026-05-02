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

# SM - PF - Service Value Chain

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Karten zur Service-Wertschöpfungskette (Service Value Chain, SVC) als zentralem Element des ITIL 4 Service Value System — sechs Aktivitäten, Diagramm-Struktur, Servicewertströme und Abgrenzung zu V3-Lifecycle und Practices. Relevant für SM (Servicemanagement, FH JOANNEUM eHealth). Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019), Folien 51 und 70–78.

## Verlinkte Konzepte

- [[SM - ITIL 4 - Service-Wertschöpfungskette]]
- [[SM - ITIL 4 - Wertstrom Definition]]
- [[SM - ITIL 4 - Service Value System]]
- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - ITIL 4 - Management Practices Übersicht]]
- [[SM - ITIL 4 - Sieben Grundprinzipien]]

---

## Karten

### Definition

Nennen und erläutern Sie die sechs Aktivitäten der Service-Wertschöpfungskette (SVC) mit ihren Zwecken.

?

**Zweck der SVC (Folie 70):** Betriebsmodell, das die zentralen Aktivitäten beschreibt, um auf Nachfrage zu reagieren und die Realisierung von Wert durch Schaffung und Management von Produkten und Services zu unterstützen.

| # | Aktivität | Zweck |
|---|---|---|
| 1 | **Planung (Plan)** | Gemeinsames Verständnis von Vision, Ist-Stand und Verbesserungsmöglichkeiten über alle vier Dimensionen und alle Services sicherstellen |
| 2 | **Verbesserung (Improve)** | Kontinuierliche Verbesserung von Produkten, Services und Practices über alle Aktivitäten und die vier Dimensionen hinweg sicherstellen |
| 3 | **Engagement (Engage)** | Stakeholder-Bedürfnisse verstehen, Transparenz und kontinuierliches Engagement fördern; alle Interaktionen mit Parteien außerhalb der Wertschöpfungskette laufen über Engagement |
| 4 | **Design und Transition (Design and Transition)** | Sicherstellen, dass Produkte und Services die Erwartungen der Stakeholder an Qualität, Kosten und Time-to-Market erfüllen |
| 5 | **Erhalten und Erstellen (Obtain/Build)** | Sicherstellen, dass Servicekomponenten verfügbar sind, wann und wo sie benötigt werden, gemäß vereinbarter Spezifikation |
| 6 | **Bereitstellung und Support (Deliver and Support)** | Sicherstellen, dass Services gemäß vereinbarter Spezifikation und Stakeholder-Erwartungen bereitgestellt und unterstützt werden |

---

Beschreiben Sie die Diagramm-Struktur der SVC (Folie 71). Warum stehen Plan und Improve außen?

?

**Diagramm-Fluss (Folie 71):**
```
Demand  →  Engage  →  Design and Transition  →  Products
                   →  Obtain / Build          →  and
                   →  Deliver and Support     →  Services  →  Value
```
Eingerahmt von **Plan** (oben, horizontal über alle Aktivitäten) und **Improve** (unten, horizontal über alle Aktivitäten).

**Warum außen / als Rahmen:**
- **Plan** und **Improve** sind **Querschnittsaktivitäten** — sie wirken nicht in einem bestimmten Schritt im Fluss, sondern kontinuierlich über alle anderen Aktivitäten hinweg.
- Plan setzt die Richtung für alle Aktivitäten; Improve bewertet und optimiert sie laufend.
- Sie sind immer aktiv — unabhängig davon, welche konkrete Kombination von Engage / Design / Obtain / Deliver gerade genutzt wird.

---

Was ist ein Wertstrom (Value Stream) in ITIL 4, und wie unterscheidet er sich von der Service-Wertschöpfungskette?

?

**Definition Wertstrom (Folie 51):**
> „Eine Reihe von Schritten, die eine Organisation unternimmt, um Produkte und Services für Konsumenten zu entwickeln und bereitzustellen — eine Kombination der Wertschöpfungsaktivitäten einer Organisation."

**Wertstrom vs. SVC:**
| | Service-Wertschöpfungskette (SVC) | Wertstrom |
|---|---|---|
| Charakter | Generische Vorlage mit 6 Aktivitäten | Konkrete, szenariospezifische Kombination |
| Ebene | Modell / Framework | Praxis / Ausführung |
| Inhalt | 6 Aktivitäten, immer dieselben | Beliebige Teilmenge + passende Practices |
| Wiederverwendung | Einmalig definiert | Für jedes Szenario neu zusammengesetzt |

Folie 72: „Servicewertströme sind spezifische Kombinationen von Aktivitäten und Practices."

---

Was sind laut Folie 72 generische Practices, die in vielen verschiedenen Wertströmen als Unterstützung verwendet werden können?

?

Folie 72 nennt als Beispiele für generische, szenarioübergreifende Practices:
- **Geschäftsanalyse**
- **Entwicklung**
- **Testen**
- **Release und Rollout**
- **Unterstützung**

Diese Practices tauchen in vielen Wertströmen auf, weil sie grundlegende Tätigkeiten der Wertschöpfung abdecken — unabhängig davon, welcher konkrete Service oder welches Szenario bearbeitet wird.

---

### Anwendung

Skizzieren Sie einen konkreten Wertstrom für die Einführung eines mobilen KIS-Zugangs im Krankenhaus — welche SVC-Aktivitäten in welcher Reihenfolge?

?

**Szenario:** Krankenhaus führt mobilen KIS-Zugang (Tablets für Pflegekräfte) ein.

| SVC-Aktivität | Konkrete Inhalte |
|---|---|
| **Plan** | Vision „mobile Pflegekraft 2027" definieren; alle vier Dimensionen abstimmen (Technologie, Organisation, Partner, Informationen) |
| **Engage** | Pflegeleitung, Datenschutzbeauftragten, Betriebsrat, KIS-Hersteller und Cloud-Anbieter einbinden; Anforderungen klären |
| **Design and Transition** | Lösung entwerfen (MDM, Sicherheitskonzept, Netzwerkinfrastruktur); Pilotphase planen; Schulungen entwickeln |
| **Obtain/Build** | Tablets beschaffen; MDM-Software konfigurieren; KIS-App ausrollen und testen |
| **Deliver and Support** | Rollout auf allen Stationen; Anwender-Support (Service Desk); Garantie- und Update-Management |
| **Improve** | Lessons Learned aus dem Piloten einbeziehen; laufende NPS-Erhebung; Optimierungsvorschläge priorisieren |

*Plan und Improve sind Querschnittsaktivitäten — sie begleiten den gesamten Wertstrom.*

---

Welche SVC-Aktivitäten sind bei einem Major Incident (KIS-Totalausfall) primär betroffen — und welche Practices unterstützen sie?

?

| SVC-Aktivität | Relevanz beim Major Incident | Unterstützende Practice(s) |
|---|---|---|
| **Engage** | Kommunikation mit Pflegedirektion, Ärzten, ggf. Medienverteiler; Stakeholder über Status informieren | Service Desk (SPOC), Service Level Management |
| **Deliver and Support** | Incident-Bearbeitung, Eskalation, Wiederherstellung; das ist der Kern | Incident Management, Monitoring and Event Management |
| **Improve** | Post-Incident-Review; Root Cause → Problem Management → Change | Problem Management, Continual Improvement |
| **Plan** | Major-Incident-Eskalationspfade und Notfallpläne müssen vorab definiert sein | Change Enablement, Service Configuration Management |

**Obtain/Build** und **Design and Transition** sind im Incident selbst weniger aktiv — aber nach der Lösung (Infrastruktur-Patch, neue Komponente) wieder relevant.

---

Zeigen Sie am Beispiel eines neuen FHIR-Schnittstellenprojekts, wie alle sechs SVC-Aktivitäten iterativ und nicht-linear ablaufen können.

?

**Szenario:** Krankenhaus entwickelt eine neue FHIR-Schnittstelle zwischen KIS und Laborsystem.

**Iterativer, nicht-linearer Ablauf:**
1. **Engage** — Anforderungen mit Laborärzte und KIS-Hersteller klären
2. **Design and Transition** — FHIR-Ressourcen-Mapping entwerfen (Iteration 1: nur Laborbefunde)
3. **Obtain/Build** — FHIR-Adapter entwickeln und im Testsystem deployen
4. **Deliver and Support** — Testbetrieb auf einer Pilotstation
5. **Improve** — Feedback: Parsing-Fehler bei bestimmten Laborcodes → zurück zu **Design and Transition**
6. **Obtain/Build** — Fehlerkorrektur
7. **Deliver and Support** — Roll-out auf alle Stationen
8. **Improve** — kontinuierlich: neue FHIR-Ressourcen in späteren Iterationen

**Plan** und **Improve** begleiten alle Schritte durchgehend.

**ITIL-4-Pointe:** V3 würde diesen Ablauf in Phasen pressen (Design → Transition → Operation); ITIL 4 erlaubt das Zurückspringen explizit — der Wertstrom wird nicht-linear durchlaufen.

---

### Diskussion

Wie unterscheidet sich die SVC vom ITIL V3 Servicelebenszyklus — und welche konkreten Nachteile des V3-Modells löst die SVC?

?

**ITIL V3 — Servicelebenszyklus:**
- 5 sequenzielle Phasen: Strategy → Design → Transition → Operation → CSI
- Jede Phase hat Prozesse; Phasengrenzen sind real organisatorisch
- CSI als „Nachpflege" am Ende des Zyklus

**ITIL 4 — Service Value Chain:**
- 6 Aktivitäten, nicht-linear; beliebige Kombinationen in Wertströmen möglich
- Improve ist kein Ende-Schritt, sondern permanente Querschnittsaktivität
- Engage als explizite Stakeholder-Brücke in jeder Phase des Wertstroms

**Konkrete V3-Probleme, die die SVC löst:**

| V3-Problem | SVC-Lösung |
|---|---|
| Rücksprünge zwischen Phasen schwer explizit gemacht | Wertströme können Aktivitäten mehrfach und in beliebiger Reihenfolge nutzen |
| CSI als Nachpflege, nicht kontinuierlich | Improve wirkt permanent über alle Aktivitäten hinweg |
| Stakeholder-Engagement implizit | Engage als eigene Aktivität — Außenkommunikation explizit verankert |
| Phasen-Silos fördern Übergabeprobleme | Kein Lifecycle-Silo; alle Aktivitäten sind jederzeit zugänglich |

---

Warum ist die Strukturierung eines IT-Service-Portfolios nach Wertströmen besser als nach Technologien oder Abteilungen?

?

**Technologie-/Abteilungsorientierung (klassisch):**
- Portfolio: Netzwerk, Server, Datenbanken, Applikationen — technologisch gegliedert
- Problem: Kundenperspektive fehlt; welchen Wert liefert „Datenbankinfrastruktur" für die Pflegekraft?
- Abteilungen verteidigen Silos; Verantwortung für End-to-End-Outcomes unklar

**Wertstrom-Orientierung (ITIL 4):**
- Portfolio: „KIS-Zugang", „Laborbefunde abrufen", „Entlassbrief erstellen" — wertstrom-gegliedert
- Jeder Wertstrom hat klaren Outcome und Stakeholder
- Wertstromoptimierung macht Verschwendung sichtbar (Lean-Prinzip); Engpässe werden outcome-orientiert behoben
- Continual Improvement kann pro Wertstrom gemessen werden (Durchlaufzeit, Fehlerquote, Kundenzufriedenheit)

**Krankenhaus-Beispiel:** Ein Wertstrom „Notaufnahme-Dokumentation" umfasst KIS, PACS, Laborsystem — technologisch verschiedene Komponenten, aber ein klarer Wert für den Notarzt. Die wertstrom-orientierte Sicht macht den gesamten Outcome-Pfad verantwortlich, nicht einzelne Technologie-Silos.

---

Wie hängen die sechs SVC-Aktivitäten mit den 34 ITIL 4-Practices zusammen — und was ist die Rolle der Practices in einem Wertstrom?

?

**Verhältnis SVC ↔ Practices:**
- SVC-Aktivitäten sind **generische Wertschöpfungsschritte** — sie beschreiben das WAS (Zweck), nicht das WIE
- Practices liefern die **konkreten Ressourcen** (Menschen, Prozesse, Werkzeuge, Information) für das WIE
- Ein Wertstrom kombiniert SVC-Aktivitäten + passende Practices für ein spezifisches Szenario

**Beispiel-Mapping:**

| SVC-Aktivität | Typisch genutzte Practices |
|---|---|
| Engage | Service Desk, Service Level Management, Business Analysis |
| Design and Transition | Change Enablement, Release Management, Service Configuration Management |
| Obtain/Build | Software Development, Infrastructure and Platform Management |
| Deliver and Support | Incident Management, Monitoring and Event Management, Service Request Management |
| Improve | Continual Improvement, Problem Management, Knowledge Management |
| Plan | Architecture Management, Strategy Management, Risk Management |

**Wichtige Einschränkung:** Practices können in mehreren Aktivitäten genutzt werden — z. B. Service Configuration Management in Deliver and Support (CMDB-Abfrage bei Incidents) und in Design and Transition (neue CIs anlegen). Die 34 Practices sind keine 1:1-Zuordnung zu SVC-Aktivitäten.

---

## Mögliche Anschlussfragen des Prüfers

- Was ist der Unterschied zwischen Wertstrom und Service-Wertschöpfungskette in einem Satz?
- Warum sind Plan und Improve im SVC-Diagramm als Außenring / horizontale Querbalken dargestellt?
- Welche SVC-Aktivität ist explizit für die Stakeholder-Kommunikation zuständig?
- Wie kann Lean Value Stream Mapping mit der ITIL 4 SVC kombiniert werden?
- Was ist der Unterschied zwischen SVC-Aktivität „Design and Transition" und der V3-Phase „Service Design"?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
