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

# SM - PF - ITIL 4 Grundlagen

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Themenbereich deckt die konzeptionellen Grundlagen von ITIL 4 ab: die Entwicklung von ITIL 3 zu ITIL 4, das Service Value System (SVS) mit seinen fünf Komponenten, die Vier Dimensionen als Designperspektiven sowie die Sieben Grundprinzipien als universelle Leitlinien. Relevant für SM (Servicemanagement, FH JOANNEUM eHealth). Einzel-Prinzip-Karten befinden sich in [[SM - PF - ITIL 4 Grundprinzipien Detail]].

## Verlinkte Konzepte

- [[SM - ITIL - Überblick]]
- [[SM - ITIL 4 - Service Value System]]
- [[SM - ITIL 4 - Four Dimensions]]
- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 - Service-Wertschöpfungskette]]
- [[SM - ITIL 4 - Wertstrom Definition]]
- [[SM - ITIL 4 - Organisatorische Agilität und Resilienz]]
- [[SM - ITIL 4 - Dimension Organisationen und Menschen]]
- [[SM - ITIL 4 - Dimension Informationen und Technologie]]
- [[SM - ITIL 4 - Dimension Partner und Lieferanten]]
- [[SM - ITIL 4 - Dimension Wertströme und Prozesse]]
- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - IT-Servicemanagement - Definition Leutgeb]]

---

## Karten

### Definition

Was ist ITIL, und welche zwei Versionen unterscheidet die Vorlesung?

?

ITIL (IT Infrastructure Library) ist ein Referenzmodell für den Aufbau und die Gestaltung des IT-Servicemanagements — das am weitesten verbreitete Rahmenwerk für IT-Management, dessen Inhalte als „Best Practice" gelten. Ursprünglich in den 1980er-Jahren von der britischen Regierung herausgegeben.
**ITIL 3:** detailliert beschriebene Prozesse; wurde als zu umfangreich, bürokratisch und unflexibel kritisiert; starre Prozesse passten schlecht zu Agile und DevOps.
**ITIL 4:** 34 Practices (Praktiken); flexibler, agil-kompatibler, adressiert genau die ITIL-3-Schwächen.
Wichtig: Ohne Versionsnummer sind Aussagen zu „ITIL" im Prüfungsgespräch unklar.

---

Was sind die fünf Komponenten des ITIL 4 Service Value System (SVS)?

?

Das SVS nimmt Inputs auf und liefert Outputs:
**Inputs:** Opportunity (Optionen zur Wertschöpfung) und Demand (konkrete Anforderungen).
**Outputs:** Ziele und Wert.
**Fünf Komponenten:**
1. **Grundprinzipien** — universelle Empfehlungen, situationsunabhängig
2. **Governance** — Mittel zur Führung und Steuerung der Organisation
3. **Service-Wertschöpfungskette** — miteinander verbundene Aktivitäten zur Wertlieferung
4. **Practices** — Organisationsressourcen zur Erreichung von Zielen
5. **Continual Improvement** — wiederkehrende Aktivität auf allen Ebenen

---

Welche vier Dimensionen kennt ITIL 4, und was ist ihre Funktion?

?

Die Vier Dimensionen sind die Designperspektiven, aus denen Produkte und Services betrachtet werden müssen, um Wert zu erzeugen:
1. **Organisationen und Menschen** — Kultur, Kapazitäten, Kompetenzen, Rollen, Motivation
2. **Informationen und Technologie** — Wissensdatenbanken, Workflow-Systeme, Kommunikation, Sicherheit und Compliance
3. **Partner und Lieferanten** — Abhängigkeiten, Beteiligung an Services (Entwurf, Betrieb, Support)
4. **Wertströme und Prozesse** — Aktivitäten, Koordination, effektive und effiziente Wertschöpfung
**Außenring:** PESTEL-Faktoren (Politik, Gesellschaft, Wirtschaft, Technologie, Umwelt, Recht) als externe Einflussfaktoren auf alle vier Dimensionen.

---

Nenne alle Sieben Grundprinzipien von ITIL 4 (deutsch und englisch) und ihren gemeinsamen Charakter.

?

1. Wertorientierung — *Focus on Value*
2. Dort beginnen, wo man steht — *Start Where You Are*
3. Iterative Weiterentwicklung mit Feedback — *Progress Iteratively with Feedback*
4. Zusammenarbeit und Transparenz fördern — *Collaborate and Promote Visibility*
5. Ganzheitlich denken und arbeiten — *Think and Work Holistically*
6. Auf Einfachheit und Praktikabilität achten — *Keep it Simple and Practical*
7. Optimieren und automatisieren — *Optimize and Automate*
**Charakter:** Universelle Empfehlungen — gelten in *allen* Situationen, unabhängig von Änderungen in Zielen, Strategien oder Führungsstrukturen. Keine spezifischen Aktionen, keine Prozesse. Typischerweise werden mehrere Prinzipien gleichzeitig angewendet.

---

### Anwendung

Ordnen Sie ein Krankenhaus-Szenario den Inputs, Komponenten und Outputs des SVS zu.

?

**Szenario:** Pflegekräfte benötigen mobilen Zugang zum Krankenhausinformationssystem (KIS).
**Demand:** konkrete Anforderung der Pflegekräfte nach mobilem KIS-Zugang.
**Opportunity:** Möglichkeit, Tablets einzuführen und den Pflegeprozess zu optimieren.
**Im SVS:**
- *Governance:* setzt Datenschutz- und Sicherheitsrahmen (DSGVO, Krankenhausrichtlinien)
- *Wertschöpfungskette:* realisiert den Service (Design → Entwicklung → Betrieb)
- *Practices:* Service Configuration Management, Incident Management, Information Security Management
- *Continual Improvement:* iterative Verbesserung basierend auf Nutzerfeedback
**Output:** produktive Tablet-Lösung mit messbarem Mehrwert für den Pflegeprozess.

---

Welche der Vier ITIL 4-Dimensionen ist im Krankenhaus-Kontext laut Vorlesung oft unterentwickelt, und warum?

?

Dimension 1: **Organisationen und Menschen** (Folie 28). Krankenhäuser sind traditionell medizinisch-hierarchisch organisiert; die IT wird häufig als technische Infrastruktur gesehen, nicht als service-orientierter Partner. Rollen, Verantwortlichkeiten und die Service-Haltung der IT-Mitarbeitenden entsprechen oft nicht dem ITSM-Modell. Kultureller Wandel zur Service-Orientierung ist eine der zentralen Herausforderungen.

---

Welches ITIL 4-Grundprinzip empfiehlt, Aufgaben in kleinere Schritte zu unterteilen? Wie hängt es mit einem anderen Prinzip zusammen?

?

**Iterative Weiterentwicklung mit Feedback** (*Progress Iteratively with Feedback*, Prinzip 3). Laut Folie 68 ist dies die korrekte Antwort (Antwort C).
**Verbindung zu Prinzip 5 — Ganzheitlich denken und arbeiten:** Iteration ohne Systemsicht riskiert lokale Optimierungen. Ganzheitliches Denken hält die Gesamtperspektive aufrecht. Beide Prinzipien müssen balanciert werden: Iteration liefert schnelle Lernzyklen; Systemsicht verhindert suboptimale Teiloptimierungen.

---

Wie begründen Sie das Prinzip „Dort beginnen, wo man steht" bei einer ITSM-Einführung in einem Krankenhaus?

?

Das Prinzip warnt davor, bestehende Prozesse und Ressourcen zu ignorieren: Vor dem Aufbau neuer Systeme (z. B. ein ITSM-Tool) muss der **aktuelle Zustand so objektiv wie möglich gemessen** werden.
**Im Krankenhaus:** Bestehende Ticketing-Workflows, informelle Supportprozesse und vorhandene Monitoring-Systeme analysieren, bevor komplett neu aufgebaut wird — Wiederverwendbares erkennen, Ressourcen schonen und Akzeptanzprobleme durch unnötige Brüche vermeiden.

---

### Diskussion

Warum ersetzt ITIL 4 den V3-Servicelebenszyklus durch das SVS? Was ist der zentrale strukturelle Unterschied?

?

**ITIL V3-Kritik:** Zu starr, bürokratisch, unflexibel; der lineare 5-Phasen-Lebenszyklus (Strategy → Design → Transition → Operation → CSI) implizierte eine Sequenzierung, die der Praxis widersprach und schlecht zu Agile und DevOps passte.
**SVS als Antwort:** Nicht-lineares System. Die Service-Wertschöpfungskette ist das zentrale Element, aber nur *eine* von fünf Komponenten. Wertströme können flexibel kombiniert werden. Das SVS betont Zusammenwirken statt Sequenzierung, ist agil-kompatibel und erlaubt parallele Aktivitäten.

---

Was ist der Unterschied zwischen Grundprinzipien, Practices und der Service-Wertschöpfungskette?

?

| Element | Was ist es? | Funktion im SVS |
|---|---|---|
| **Grundprinzipien** | Universelle Haltungen/Empfehlungen | Leiten *wie* gearbeitet wird |
| **Service-Wertschöpfungskette** | 6 miteinander verbundene Aktivitäten | Beschreibt *womit* Wert erzeugt wird |
| **Practices** | Organisationsressourcen (Tools, Skills, Prozesse) | Definieren *was* konkret getan wird (z. B. Incident Management) |

Alle drei sind Komponenten des SVS, aber auf unterschiedlichen Abstraktionsebenen. Grundprinzipien sind die „Philosophie", die Wertschöpfungskette ist die „Maschinerie", Practices sind die „Werkzeuge".

---

Was ist der Unterschied zwischen den Vier Dimensionen und der EBEL-Trias (Menschen, Prozesse, IT)?

?

Die **EBEL-Trias** (ITIL V3-Vorgänger) kennt drei Säulen: Menschen, Prozesse, IT.
**ITIL 4** erweitert auf Vier Dimensionen:
- Dimension 1 (Organisationen und Menschen) ≈ "Menschen" + Kultur, Kompetenzen, Motivation
- Dimension 4 (Wertströme und Prozesse) ≈ "Prozesse" + Wertströme, Koordination
- Dimension 2 (Informationen und Technologie) ≈ "IT" + explizit Informationen, Daten, Wissen
- **Neu: Dimension 3 — Partner und Lieferanten** — explizite Anerkennung externer Abhängigkeiten, Outsourcing-Realitäten und Cloud-Nutzung, die V3 implizit ließ.

---

Welche Spannung kann zwischen „Ganzheitlich denken" und „Auf Einfachheit achten" entstehen? Wie wird sie aufgelöst?

?

**Spannung:** Ganzheitliches Denken verlangt, alle vier Dimensionen und Stakeholder zu berücksichtigen — das kann zu Komplexität führen. „Einfachheit" verlangt, Unnötiges zu stoppen und Prozesse/Services zu entschlacken.
**Auflösung:** Beide Prinzipien wirken zusammen, nicht gegeneinander. Ganzheitlichkeit verhindert blinde Flecken (z. B. wird Dimension 1 ignoriert, scheitert beste Technologie an fehlendem Change Management). Einfachheit verhindert Overengineering. Die Balance: systemisches Denken anwenden, aber nur so viel Komplexität zulassen, wie für den Wert notwendig ist.

---

Warum gilt ITIL als „Best Practice"-Rahmenwerk und nicht als normativer Standard? Welche Konsequenz hat das?

?

**Best Practice:** Aus der Praxis heraus entwickelt und vielfach bewährt — keine externe Auditierungspflicht, keine Zertifizierungspflicht für die *Organisation* (nur für Einzelpersonen optional).
**Konsequenz:** Unternehmen können ITIL selektiv und angepasst adoptieren; kein verpflichtender Compliance-Nachweis.
**Vergleich:**
- **ISO/IEC 20000-1:2018:** normativer Standard, auditierbar, Zertifizierung möglich/verpflichtend
- **COBIT 2019:** Governance-Rahmenwerk mit Steuerungs- und Audit-Charakter
ITIL ist das flexibelste und am weitesten verbreitete der drei — aber auch das unverbindlichste.

---

## Mögliche Anschlussfragen des Prüfers

- Was unterscheidet ITIL von COBIT 2019 und ISO/IEC 20000-1:2018 hinsichtlich Verbindlichkeit und Fokus?
- Wie viele Practices hat ITIL 4, und in welche Kategorien sind sie eingeteilt?
- Was ist ein Wertstrom (Value Stream) im Sinne von ITIL 4?
- Wie hängen die Sieben Grundprinzipien mit dem CSI-Modell zusammen?
- Welcher erste Schritt ist beim Prinzip „Wertorientierung" laut Folie 69 vorgeschrieben?
- Wie würden Sie das SVS auf die Einführung eines neuen KIS-Moduls in einem Krankenhaus anwenden?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
