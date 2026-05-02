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

# SM - PF - ITIL V3 vs ITIL 4

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Vergleichskarten zwischen ITIL V3 (Service Lifecycle, Van Haren Publishing 2008) und ITIL 4 (Service Value System, Axelos / Van Haren Publishing 2019). Der Vault enthält parallel V3- und ITIL-4-Konzeptnotes — diese Note verbindet beide Welten und fokussiert auf prüfungsrelevante Unterschiede: Strukturmodell (Lifecycle vs. SVS), Prozess-zu-Practice-Übergang, veränderte Definitionen und Migrationsmotivation. Relevant für SM (Servicemanagement, FH JOANNEUM eHealth).

## Verlinkte Konzepte

- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - ITIL V3 - Service Operation]]
- [[SM - ITIL V3 Practice - Incident Management]]
- [[SM - ITIL V3 Practice - Problem Management]]
- [[SM - ITIL V3 Practice - Event Management]]
- [[SM - ITIL V3 Practice - Request Fulfillment]]
- [[SM - ITIL V3 Practice - Access Management]]
- [[SM - ITIL 4 - Service Value System]]
- [[SM - ITIL 4 - Management Practices Übersicht]]
- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL Practice - Problem Management]]
- [[SM - ITIL Practice - Monitoring and Event Management]]
- [[SM - ITIL Practice - Service Request Management]]
- [[SM - ITIL Practice - Change Enablement]]
- [[SM - ITIL Practice - Service Desk]]

---

## Karten

### Definition

Was sind die fünf Phasen des ITIL V3 Servicelebenszyklus, und welche Prozesse enthält Service Operation?

?

**Fünf Phasen (Folie 32):**
1. Service Strategy
2. Service Design
3. Service Transition
4. Service Operation
5. Continual Service Improvement (CSI)

**Service Operation Prozesse (Folie 32):**
- Event Management
- Incident Management
- Problem Management
- Request Fulfilment
- Access Management

*Hinweis:* Access Management erscheint im Foliensatz doppelt — einmal unter Service Transition und einmal unter Service Operation (Aufbau vs. Tagesgeschäft).

---

Was ist der grundlegende strukturelle Unterschied zwischen dem ITIL V3 Servicelebenszyklus und dem ITIL 4 Service Value System (SVS)?

?

**ITIL V3 — Servicelebenszyklus:**
- Lineares / zyklisches Modell mit 5 aufeinanderfolgenden Phasen
- Jede Phase hat definierte Prozesse → sequenzielles Denken
- Starre Phasengrenzen: Service Strategy → Design → Transition → Operation → CSI

**ITIL 4 — Service Value System (SVS):**
- Nicht-lineares Gesamtmodell aus 5 Komponenten: Guiding Principles, Governance, Service Value Chain, Practices, Continual Improvement
- Kein Lifecycle — stattdessen flexible Wertschöpfungsströme (Value Streams), die beliebige Kombinationen von SVS-Aktivitäten durchlaufen
- Alle 5 Komponenten wirken gleichzeitig und kontinuierlich zusammen

**Kernunterschied:** V3 denkt in Phasen und Prozessen; ITIL 4 denkt in Wertströmen und Practices.

---

Was ist ein „Prozess" in ITIL V3, und wie unterscheidet er sich von einer „Practice" in ITIL 4?

?

**ITIL V3 — Prozess:**
- Definierte Abfolge von Aktivitäten mit messbaren Inputs und Outputs
- Beispiel: V3 Incident Management hat **9 formale Prozessschritte** (Identification → Logging → Categorization → Prioritization → Initial Diagnosis → Escalation → Investigation → Resolution → Closure)
- Sehr präskriptiv: jeder Schritt ist vorgegeben

**ITIL 4 — Practice:**
- „Eine Reihe von Organisationsressourcen, die zur Durchführung von Aufgaben oder zur Erreichung eines Ziels bestimmt sind" — umfasst Menschen, Prozesse, Werkzeuge, Information (alle 4 Dimensionen)
- Weniger präskriptiv: definiert Zweck und Ergebnis, nicht jeden Einzelschritt
- Beispiel: ITIL 4 Incident Management definiert eine **Lösungs-Hierarchie** (Selbsthilfe → Service Desk → Support-Team → Lieferanten → temporäres Team → Notfallpläne), keine starren 9 Schritte

**Kernunterschied:** Prozess = WIE (Schritt für Schritt); Practice = WAS und WOMIT (Ressourcen + Ziel), flexibles WIE.

---

Wie war Access Management in ITIL V3 positioniert, und was entspricht ihm in ITIL 4?

?

**ITIL V3 — Access Management:**
- Eigenständiger Prozess in **Service Operation** (5 Schritte: Anfrage → Verifizierung → Rechte bereitstellen → Protokollieren → Rechte entziehen/anpassen)
- Im Foliensatz doppelt aufgeführt: auch unter **Service Transition** — dort vermutlich Erstaufbau, in Operation der laufende Betrieb
- Zweck: Zugriff auf Services nur für autorisierte Nutzer gewähren

**ITIL 4:**
- Kein direktes 1:1-Pendant
- Access Management ist in ITIL 4 **in die Information Security Management Practice** (General Management) integriert
- ITIL 4 betrachtet Zugriffsrechte als Teil des umfassenderen Sicherheitsmanagements, nicht als isolierten Betriebsprozess

---

Welche V3-Prozesse haben kein direktes 1:1-Pendant in ITIL 4 — und warum?

?

**Access Management (V3)** → subsumiert in **Information Security Management (ITIL 4)**:
Zugriffsrechte sind in ITIL 4 ein Aspekt des Sicherheitsmanagements, kein eigenständiger Prozess mehr.

**Request Fulfilment (V3, 4 Schritte)** → **Service Request Management (ITIL 4)**:
Umbenennung und inhaltliche Erweiterung — ITIL 4 definiert 5 Request-Typen (Informationen, Bereitstellung, Zugang, Feedback, Ausnahmen) statt eines linearen 4-Schritt-Prozesses.

**Change Management (V3)** → **Change Enablement (ITIL 4)**:
Umbenennung ist bewusst: „Enablement" statt „Management" signalisiert, dass Changes unterstützt werden sollen, nicht bürokratisch kontrolliert.

**Service Desk (V3 = Funktion)** → **Service Desk (ITIL 4 = eigene Practice)**:
In V3 war Service Desk eine Funktion (kein Prozess); ITIL 4 erhebt es zur vollwertigen Practice.

---

### Anwendung

Ordnen Sie diese V3-Prozesse den am nächsten liegenden ITIL 4-Practices zu.

?

| ITIL V3 Prozess | ITIL 4 Practice | Änderung |
|---|---|---|
| Event Management | Monitoring and Event Management | Präzisere Event-Definition; IS-Events explizit |
| Incident Management | Incident Management | 9 Schritte → Lösungs-Hierarchie; weniger präskriptiv |
| Problem Management | Problem Management | 10 Schritte → 3 Phasen; Definitionen klarer |
| Request Fulfilment | Service Request Management | 4 Schritte → 5 Request-Typen |
| Access Management | Information Security Management | Kein Pendant — subsumiert |
| Change Management | Change Enablement | Umbenennung; Botschaft: enablement statt Kontrolle |
| Service Desk (Funktion) | Service Desk (Practice) | Aufgewertet zur eigenen Practice |

---

KIS-Incident im Krankenhaus: Wie unterscheiden sich der V3- und der ITIL-4-Ablauf konkret?

?

**ITIL V3 — 9 formale Prozessschritte:**
1. Identification
2. Logging
3. Categorization
4. Prioritization
5. Initial Diagnosis
6. Escalation (functional/hierarchical)
7. Investigation and Diagnosis
8. Resolution and Recovery
9. Incident Closure

→ Jeder Schritt ist formell definiert; strikte Reihenfolge.

**ITIL 4 — Lösungs-Hierarchie:**
1. Anwender (Selbsthilfe)
2. Service Desk (1st Level)
3. Support-Team (nach Kategorie)
4. Lieferanten / Partner
5. Temporäres Team (Major Incidents)
6. Notfallwiederherstellungspläne

→ ITIL 4 beschreibt Eskalationsstufen, keine starren Schritte. Das Ergebnis (Wiederherstellung) ist zentral, nicht der Prozessweg.

**Praxis-Unterschied:** Ein agiles IT-Team im Krankenhaus, das Tickets direkt im Slack behandelt, verletzt formal ITIL V3 (kein Logging-Schritt); in ITIL 4 ist Flexibilität im WIE explizit erlaubt, solange das Ziel erreicht wird.

---

Problem Management: Wie unterscheiden sich die V3- und ITIL-4-Strukturen, und was bringt die ITIL-4-Begriffstrias?

?

**ITIL V3 — Problem Management (10 Schritte):**
1. Problem Detection
2. Problem Logging
3. Categorization
4. Prioritization
5. Investigation and Diagnosis (inkl. Known-Error-Unterprozess: Raise Known Error → Workaround → Request for Change)
6. Raise Known Error Record
7. Workaround
8. Raise RFC (Request for Change)
9. Resolution
10. Closure
→ Plus: Major Problem Review als eigenständiger Unterprozess

**ITIL 4 — Problem Management (3 Phasen):**
1. Problemidentifizierung (Trendanalysen, Muster)
2. Problemsteuerung / Problem Control (Ursachenanalyse, Workarounds, Known Errors dokumentieren)
3. Fehlersteuerung / Error Control (Known Errors managen, dauerhafte Lösung, ggf. Change Request)

**Vorteil der ITIL-4-Begriffstrias:**
- **Problem** = Ursache / mögliche Ursache von Incidents (klare Definition)
- **Workaround** = Lösung, die Auswirkungen reduziert, ohne vollständige Lösung
- **Known Error** = Problem, das analysiert, aber noch nicht gelöst wurde
→ In V3 waren diese Begriffe weniger trennscharf definiert.

---

### Diskussion

Warum wurde ITIL V3 von ITIL 4 abgelöst — was waren die Hauptkritikpunkte an V3?

?

**Hauptkritikpunkte an ITIL V3:**

1. **Zu starr für Agile/DevOps:** Die 9- und 10-Schritt-Prozesse passen schlecht in iterative Entwicklungszyklen. Agile Teams empfanden V3 als bürokratisch.

2. **Lifecycle-Denken vs. kontinuierliche Lieferung:** V3s Phasenmodell (Strategy → Design → Transition → Operation) impliziert sequenzielle, große Releases — im Widerspruch zu CI/CD-Pipelines.

3. **Prozess-Silos:** V3-Prozesse waren oft isoliert organisiert; Querverbindungen zwischen Prozessen wurden nicht systematisch adressiert.

4. **Kein explizites Wertfokus:** ITIL 4 stellt „Co-creating Value" ins Zentrum; V3 fokussierte auf Service-Lieferung, nicht auf gemeinsame Wertschöpfung mit dem Kunden.

5. **Fehlende Integrationsbrücken:** Zu Agile, DevOps, Lean gab es in V3 keine expliziten Verbindungen — ITIL 4 adressiert dies direkt (Guiding Principles, SVS).

**ITIL 4-Antwort:** 34 Practices statt Prozesse, 7 Guiding Principles, SVS als Gesamtrahmen, explizite Kompatibilität mit Agile und DevOps.

---

Vergleichen Sie die Event-Definition in ITIL V3 und ITIL 4. Warum ist die ITIL-4-Definition präziser?

?

**ITIL V3 — Event:**
> „Ein Ereignis welches die IT-Infrastruktur beeinflusst."

**ITIL 4 — Event:**
> „Jede Statusänderung, die für das Management eines Service oder eines anderen Configuration Items (CI) von Bedeutung ist. Events werden normalerweise durch Benachrichtigungen erkannt, die von einem IT Service, CI oder Monitoring-Tool erstellt werden."

**Warum präziser:**

1. **Statusänderung statt Ereignis:** ITIL 4 definiert konkret, was ein Event auslöst (Statusänderung), V3 bleibt vage.

2. **CI-Bezug explizit:** ITIL 4 verankert Events im Configuration-Item-Kontext — Events sind relevant für das Management von CIs, nicht beliebiger Infrastruktur.

3. **Erkennungsquelle benannt:** ITIL 4 nennt Service, CI, Monitoring-Tool als Quellen — praktisch wichtig für Architekturentscheidungen (welche Tools müssen Events erzeugen?).

4. **Informationssicherheits-Events integriert:** ITIL 4 Monitoring and Event Management schließt IS-Events explizit ein — V3 Event Management hatte keinen expliziten Sicherheitsfokus.

---

Was hat sich beim Übergang von ITIL V3 Change Management zu ITIL 4 Change Enablement geändert — und warum ist der neue Name bedeutsam?

?

**Inhaltliche Änderungen:**

| Aspekt | V3 Change Management | ITIL 4 Change Enablement |
|---|---|---|
| Name-Botschaft | Kontrolle und Verwaltung | Ermöglichung und Unterstützung |
| Change-Arten | Standard / Normal / Emergency | Standard / Normal / Notfall (identisch, andere Akzente) |
| Change Autorität | Change Advisory Board (CAB) | Change Autorität (flexibler, je Change-Typ unterschiedlich) |
| Abgrenzung | Nicht explizit vs. OCM | Explizit abgegrenzt von Organizational Change Management |
| Fokus | Risikominimierung durch Genehmigung | Maximierung erfolgreicher Changes |

**Warum der neue Name bedeutsam:**
- „Management" = bürokratische Kontrolle → wurde als Engpass wahrgenommen
- „Enablement" = Unterstützung → signalisiert: Changes sollen ermöglicht, nicht aufgehalten werden
- Dies adressiert direkt die V3-Kritik: CABs galten oft als „Change-Blocker", nicht als Enabler

**Für die Prüfung:** Die Umbenennung ist kein Zufall — ITIL 4 will kommunizieren, dass Change Enablement den Geschäftswert von Änderungen sichert, nicht nur Risiken verwaltet.

---

Wie veränderte sich die Position des Service Desk von ITIL V3 zu ITIL 4 — und was bedeutet diese Aufwertung?

?

**ITIL V3 — Service Desk als Funktion:**
- Service Desk war eine der vier **Functions** in Service Operation (neben IT Operations Management, Technical Management, Application Management)
- Functions in V3 = Organisationseinheiten, keine Prozesse
- Service Desk führte andere Prozesse aus (Incident Management, Request Fulfilment), hatte aber keinen eigenen definierten Prozess

**ITIL 4 — Service Desk als eigenständige Practice:**
- Service Desk ist eine von 17 **Service Management Practices**
- Hat einen eigenen Zweck: Single Point of Contact (SPOC) zwischen Service Provider und allen Anwendern
- Hat eigene Verantwortlichkeiten: erfassen, klassifizieren, zuweisen, beantworten, eskalieren
- Explizit: großer Einfluss auf User Experience — Wahrnehmung des gesamten IT-Providers hängt am Service Desk

**Was die Aufwertung bedeutet:**
1. Service Desk wird nicht mehr nur als Empfangsstelle behandelt, sondern als strategische Practice mit eigenem Wertbeitrag
2. UX-Aspekt wird explizit in die Practice-Definition integriert
3. Kompatibilität mit modernen Servicemodellen (Omnichannel, Self-Service-Portale)

---

Ist ITIL 4 „besser" als ITIL V3? Diskutieren Sie — und wann könnte V3 noch sinnvoll sein.

?

**Argumente für ITIL 4 (gegenüber V3):**
- Explizite Agile/DevOps-Kompatibilität; 7 Guiding Principles passen zu modernen Arbeitsweisen
- Practices statt Prozesse: mehr Flexibilität im WIE, Fokus auf Ergebnis
- Präzisere Definitionen (Event, Problem, Workaround, Known Error)
- Co-creating Value als zentrales Konzept: Kundenperspektive stärker verankert
- Change Enablement-Philosophie: weniger Bürokratie, mehr Ermöglichung

**Argumente, wann V3 noch sinnvoll sein kann:**
- Sehr detaillierte, schritt-für-schritt-orientierte Organisationen (z. B. regulierte Branchen mit dokumentierten Prozessaudits) schätzen die V3-Präskriptivität
- Bestehende ITIL-V3-Zertifizierungen und -Tools sind im Einsatz; Migration kostet Zeit und Geld
- V3-Prozessdokumentation kann in ITIL 4-Practices überführt werden — V3 und ITIL 4 sind nicht inkompatibel, sondern komplementär

**Prüfungsrelevante Antwort:** ITIL 4 ist nicht besser, sondern **kontextuell geeigneter für moderne, agile Organisationen**. Für klassisch-strukturierte IT-Abteilungen in streng regulierten Umgebungen bietet V3's Präskriptivität Vorteile. Die meisten Organisationen migrieren schrittweise.

---

Warum erscheint Access Management im ITIL V3 Foliensatz doppelt — unter Service Transition und Service Operation — und was sagt das über die Grenzen des Lifecycle-Modells?

?

**Doppellistung im Foliensatz (Folie 32):**
Access Management erscheint sowohl unter **Service Transition** als auch unter **Service Operation**.

**Mögliche Erklärung:**
- **Service Transition**: Aufbau von Zugriffsrechten beim erstmaligen Bereitstellen eines Services (z. B. initiale Rollendefinitionen, Berechtigungskonzepte erstellen)
- **Service Operation**: Laufende Vergabe, Anpassung und Entzug von Zugriffsrechten im Tagesgeschäft

**Was das über das Lifecycle-Modell aussagt:**
Das Lifecycle-Modell erzwingt eine Phasenzuordnung — aber manche Aktivitäten gehören inhaltlich zu mehreren Phasen. Diese Doppellistung zeigt:
1. **Künstliche Phasengrenzen:** Real ist Access Management ein kontinuierlicher Prozess, keine Transition-oder-Operation-Entscheidung
2. **Schwäche des Lifecycle-Ansatzes:** ITIL 4 löst dieses Problem mit dem SVS — Practices wirken phasenübergreifend und kontinuierlich, ohne Lifecycle-Grenzen
3. **In ITIL 4** ist das Problem gelöst: Information Security Management ist eine Practice, die in jedem Value Stream eingesetzt werden kann, ohne Lifecycle-Zuordnung

---

## Mögliche Anschlussfragen des Prüfers

- Was ist der Unterschied zwischen einem ITIL V3 „Prozess" und einer ITIL 4 „Practice" in einem Satz?
- Welche ITIL-4-Practice entspricht dem V3-Prozess „Request Fulfilment" — und was hat sich inhaltlich verändert?
- Warum heißt es in ITIL 4 „Change Enablement" und nicht mehr „Change Management"?
- Nennen Sie drei Guiding Principles, die direkt auf Kritikpunkte an ITIL V3 antworten.
- Kann man ITIL V3 und ITIL 4 parallel betreiben? Welche Risiken gibt es?
- Warum ist die ITIL-4-Event-Definition für Cloud-Umgebungen besser geeignet?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
