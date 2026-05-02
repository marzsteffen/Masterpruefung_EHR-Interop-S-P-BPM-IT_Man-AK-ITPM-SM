---
typ: konzept
status: offen
faecher: [bpm, itm-ak, sm, itpm]
quellen:
  - "[[BPM - PDCA-Zyklus]]"
  - "[[BPM - Grundprinzip - Kontinuierliche Verbesserung]]"
  - "[[BPM - Fehlerkultur - Deming]]"
  - "[[BPM - Bewusstseinskreis]]"
  - "[[ITM-AK - PDCA-Zyklus]]"
  - "[[ITM-AK - ISO 9001-2015]]"
  - "[[ITM-AK - Toyota Kata - Verbesserungs-Kata]]"
  - "[[SM - ITIL Continual Improvement - Modell]]"
  - "[[SM - CMMI - Reifegradmodell]]"
  - "[[ITPM - Vorgehensmodelle - Klassisch vs Agile]]"
  - "[[ITPM - Scrum - Empirische Prozesssteuerung]]"
tags:
  - typ/konzept
  - status/offen
  - cross-fach
  - fach/vertiefung/bpm
  - fach/vertiefung/itm-ak
  - fach/vertiefung/sm
  - fach/vertiefung/itpm
---

# Cross - PDCA-Zyklus quer durch die Disziplinen

> [!info] Kurzdefinition
> Der PDCA-Zyklus erscheint in vier Fächern, dreimal explizit (BPM, ITM-AK, SM in Form des CSI-Modells) und einmal als gespaltene Sicht (ITPM: klassisch-deterministisch *ohne* PDCA, agil-empirisch *mit* PDCA-äquivalenter Inspect-&-Adapt-Logik). Die Brücke zeigt, dass alle vier denselben iterativen Roten Faden tragen — und wo die Implementierung sich unterscheidet (4 Phasen vs. 6+1 Schritte vs. 4 Scrum-Ereignisse). ITPM-Wasserfall ist die produktive Kontrast-Sicht.

## Sicht aus Fach BPM

BPM behandelt PDCA als **Standardmethode des kontinuierlichen Verbesserungsprozesses** mit kultureller Voraussetzung.

**PDCA-Zyklus** (siehe [[BPM - PDCA-Zyklus]], Folie 36):

| Schritt | Inhalt (wörtlich aus Folie 36) |
|---|---|
| Plan | Lösung planen, Verbesserungen planen |
| Do | Lösung realisieren / umsetzen |
| Check | Ergebnisse und den Plan bewerten |
| Act | Verbesserung standardisieren und danach handeln |

- Auch „Deming-Kreis" genannt — nach W. Edwards Deming.
- Schleife, nicht Einzeldurchlauf: nach Act beginnt der nächste Plan.
- Maßnahmenplan-Beispiel auf Folie 149: konkrete Mapping-Anwendung Limonadenstand / verbesserter Prozess.

**Kontinuierliche Verbesserung als Grundprinzip** (siehe [[BPM - Grundprinzip - Kontinuierliche Verbesserung]], Folien 31–35):

- KVP-Methode = PDCA.
- Mathematisches Argument: 1,01³⁶⁵ = 37,78 (1 % Verbesserung pro Tag → 37× besser im Jahr).
- KVP ist *Denkweise*, nicht einmaliges Projekt.
- Bezug zu ISO 9001 Abschnitt 8.5.1 (Steuerung „unter beherrschten Bedingungen").

**Fehlerkultur als Voraussetzung** (siehe [[BPM - Fehlerkultur - Deming]], Folien 37–38):

- Demings Punkt 8: „Schaffe die Angst ab."
- Gesunde Fehlerkultur: offene Kommunikation, sachliche Ursachenanalyse, Fehler als Lernchancen.
- Bezug zu „To Err Is Human" (IOM 2000): Paradigmenwechsel von individueller Schuld zu Systemansatz.

**Bewusstseinskreis als Vor-PDCA-Stufe** (siehe [[BPM - Bewusstseinskreis]], Folie 147):

- Vier Stufen: **Bewusstsein → Wissen → Verstehen → Anwenden**.
- Sequenziell, nicht zyklisch.
- Voraussetzung für die wirksame Anwendung des PDCA-Kreises.
- Eingebettet in Schritt 4 (Realisierung) der 4-Schritte-Methode.

## Sicht aus Fach ITM-AK

ITM-AK behandelt PDCA als **methodische Klammer der ISO 9001:2015** plus Toyota Kata als verwandte Variante.

**PDCA-Zyklus** (siehe [[ITM-AK - PDCA-Zyklus]], Folie 6):

- Vier Phasen Plan / Do / Check / Act, klassisches Diagramm aus ResearchGate-Quelle.
- ISO-9001:2015-Hauptkapitel-Zuordnung:

| Phase | ISO-9001-Klauseln |
|---|---|
| Plan | Klausel 6 (Planung) |
| Do | Klauseln 7 (Unterstützung) + 8 (Betrieb) |
| Check | Klausel 9 (Leistungsbewertung) |
| Act | Klausel 10 (Verbesserung) |

- Klauseln 4 (Kontext) und 5 (Führung) bilden den **Rahmen**, in dem PDCA läuft. „Leadership (5)" steht im Diagramm-Zentrum.

**Diskussions-Aussage aus dem Note** (zitatpflichtig wegen der Cross-Pointe):

- „Warum ist PDCA in der Praxis trotz Einfachheit oft schwer durchzuhalten?
  - Druck zu kurzfristigen Ergebnissen schneidet Check und Act ab.
  - Datenmangel macht Check schwierig.
  - Lernen aus Fehlern erfordert Kultur, die nicht überall vorhanden ist."

**Toyota Kata als PDCA-Variante** (siehe [[ITM-AK - Toyota Kata - Verbesserungs-Kata]], Folien 17–19):

- Stufenweise Annäherung an Vision: Aktuelle Situation → Zielstufe (was) → Umsetzung (wie) → Vision.
- Bei Problemen: Root-Cause-Analyse als Schleife.
- Kata-Note grenzt explizit ab: „Toyota Kata ≠ PDCA: PDCA ist generischer; Kata strukturiert PDCA-ähnliches Denken durch eine Vision-Zielstufe-Logik und disziplinierte Coaching-Routinen."

## Sicht aus Fach SM

SM behandelt PDCA **nicht direkt** als Begriff, sondern als das **ITIL Continual Improvement-Modell (CSI)** mit feinerer Schritt-Zerlegung.

**ITIL CSI-Modell** (siehe [[SM - ITIL Continual Improvement - Modell]], Folien 107–122):

Sechs Schritte plus Klammer-Frage:

1. Was ist unsere Vision?
2. Wo stehen wir gerade? (Current-State-Assessment — *„Startpunkt muss bekannt sein!"*)
3. Wo wollen wir hin? (mit GAP-Analyse, KPIs, SWOT)
4. Wie kommen wir dort hin? (Plan, iterativ)
5. Aktiv werden (Change Management, Measurement und Reporting, Risk Management, Continual Improvement)
6. Sind wir angekommen? (KPIs evaluieren, Change Management)
+ Klammer: Wie halten wir unsere Services in Schwung?

**PDCA-Mapping zum CSI-Modell** (Synthese, in den Notes nicht explizit gemappt):

| PDCA | CSI-Schritt |
|---|---|
| Plan | 1–4 (Vision → Ist → Soll → Wie) |
| Do | 5 (Aktiv werden) |
| Check | 6 (Sind wir angekommen?) |
| Act | Klammer (Schwung halten) → zurück zu 1 |

**CSI-Modell vs. PDCA — explizite Aussage aus dem Note**: „Beide sind iterative Verbesserungsmodelle; CSI ist ITIL-spezifisch und expliziter (6+1 Schritte mit klaren Fragen)."

**CMMI als Reifegrad-Bewertung** (siehe [[SM - CMMI - Reifegradmodell]]):

- Stufen 1–5: Initial / Gemanagt / Definiert / Quantitativ gemanagt / Optimierend.
- Wird in CSI Schritt 2 als Hilfsmethode genutzt — Reifegrad ist *Bewertung*, nicht *Verbesserung* (siehe Brücke 9 [[Cross - Qualitaetsmanagement]]).

## Sicht aus Fach ITPM (Kontrast-Sicht)

ITPM hat **keinen dedizierten PDCA-Note**. Iteration läuft entweder gar nicht (klassisch) oder unter anderem Begriff (agile/Scrum: Empirische Prozesssteuerung).

**Klassisch — kein PDCA** (siehe [[ITPM - Vorgehensmodelle - Klassisch vs Agile]], Folien 66–68):

- Wasserfallmodell: lange Anforderungserfassung → sequentielle Phasen → Auslieferung am Ende → Kunden-Feedback erst danach.
- „Viel Planung, oft für lange Zeiträume detailliert."
- Phasen sind sequenziell; nach Abschluss einer Phase kein Rückgriff zur Verbesserung.

→ Klassisches IT-Projektmanagement ist explizit **nicht PDCA-orientiert**, sondern phasenmodelliert.

**Agile/Scrum — PDCA-äquivalent** (siehe [[ITPM - Scrum - Empirische Prozesssteuerung]], Folie 22):

- Empirische Prozesssteuerung als theoretische Basis von Scrum.
- **Inspect & Adapt**-Prinzip: Prozess wird empirisch beobachtet und kontinuierlich angepasst — funktional identisch zum PDCA-Kreis.
- Drei Säulen: **Transparenz, Überprüfung, Anpassung**.
- Vier Anpassungs-Ereignisse: **Sprint Planning, Daily Scrum, Sprint Review, Sprint Retrospektive**.
- Note grenzt explizit ab: „Empirische vs. deterministische Prozesssteuerung: Klassisches PM ist deterministisch (Plan vorab), Scrum ist empirisch (Anpassung anhand von Beobachtungen)."

**ITPM-Mapping zum PDCA-Kreis** (Synthese, in den Notes nicht explizit gemappt):

| PDCA | Scrum-Ereignis |
|---|---|
| Plan | Sprint Planning |
| Do | Sprint-Ausführung |
| Check | Sprint Review |
| Act | Sprint Retrospektive |

## Gemeinsamkeiten

| Aussage | Wo |
|---|---|
| Iterativer Kreis als Roter Faden | BPM, ITM-AK, SM-CSI, ITPM-Scrum |
| Prinzip „Erst messen, dann verbessern" | BPM Check-Phase, SM CSI Schritt 2/6, ITPM Sprint Review |
| Standardisierung als Abschluss eines Zyklus | BPM Act, ITM-AK Klausel 10, SM CSI-Klammer, ITPM Definition of Done |
| Kulturelle Voraussetzung: Lernen aus Fehlern | BPM Fehlerkultur, ITM-AK Diskussion „Lernen aus Fehlern erfordert Kultur", ITPM Empirische Prozesssteuerung „setzt Vertrauen voraus" |
| Anti-Pattern: Plan abbrechen vor Check/Act | BPM Diskussion (schwierigste Stelle ist Übergang Check→Act), ITM-AK Diskussion (Druck zu kurzfristigen Ergebnissen schneidet Check und Act ab) |

## Unterschiede / Konflikte / unterschiedliche Schwerpunkte

**1. Vier Phasen vs. 6+1 Schritte vs. 4 Scrum-Ereignisse vs. 7 ISO-9001-Klauseln.**

Dasselbe Konzept, vier verschiedene Granularitäten:

| Implementierung | Granularität | Quelle |
|---|---|---|
| BPM PDCA | 4 Phasen | Folie 36 |
| ITM-AK ISO 9001 | 7 Hauptkapitel mit PDCA-Zuordnung | Folie 6 + 11 |
| SM CSI | 6 Schritte + Klammer | Folien 107–122 |
| ITPM Scrum | 4 Ereignisse + 3 Säulen | Folie 22 |

Wer in der Prüfung mit „der" PDCA-Zyklus argumentiert, muss die Granularität nennen. „PDCA in BPM" ist die 4-Phasen-Version; „PDCA in SM" ist das 6+1-Schritte-Modell; „PDCA in ITPM" ist die Empirische Prozesssteuerung mit vier Sprint-Ereignissen.

**2. Vokabular-Konflikt: PDCA vs. CSI vs. Inspect-&-Adapt vs. KVP.**

Vier verschiedene Wörter, dasselbe Grundprinzip:

- BPM: PDCA-Zyklus / Deming-Kreis / KVP.
- ITM-AK: PDCA-Zyklus / kontinuierliche Verbesserung.
- SM: Continual Service Improvement (CSI) / Continual Improvement Practice.
- ITPM: Empirische Prozesssteuerung / Inspect & Adapt.

In der Prüfung: bei Diskussion mehrerer Fächer die Vokabular-Trennung klar markieren („in BPM-Sprech ist das der PDCA-Zyklus; in ITIL-Sprech wird er als CSI-Modell ausdifferenziert"); nicht beliebig zwischen den Begriffen wechseln.

**3. ITPM-Wasserfall ist die einzige Stelle ohne PDCA.**

ITPM ist das einzige Fach, das eine *anti-iterative Logik* explizit beschreibt (Wasserfallmodell, V-Modell, Phasenmodelle). Die Vorlesung relativiert das aber selbst: in der Spezifitäts-Skala von „Wasserfall" bis „Agile" sieht ITPM eine Kontinuum-Struktur. Der Wasserfall ist nicht „falsch", sondern für andere Komplexitäts-Klassen geeignet (Stacey-Matrix-Bezug).

Saubere Cross-Aussage: Klassisches PM und PDCA sind keine direkten Gegner. Sie adressieren unterschiedliche Komplexitäten — PDCA passt für Verbesserung wiederkehrender Prozesse, Wasserfall passt für einmalige, gut spezifizierbare Vorhaben.

**4. Voraussetzungs-Schichten (Bewusstseinskreis nur in BPM).**

BPM ist das einzige Fach, das eine *Vor-PDCA-Stufe* explizit benennt: der Bewusstseinskreis (Bewusstsein → Wissen → Verstehen → Anwenden) ist Voraussetzung für die wirksame Anwendung des PDCA. ITM-AK, SM und ITPM thematisieren keine entsprechende Vorbedingung. Wer „Was muss erfüllt sein, damit PDCA wirkt?" beantworten muss, antwortet aus BPM.

**5. Toyota Kata vs. PDCA — eine ITM-AK-spezifische Verfeinerung.**

Toyota Kata erscheint nur in ITM-AK. Die Note grenzt explizit ab: „Toyota Kata ≠ PDCA: PDCA ist generischer; Kata strukturiert PDCA-ähnliches Denken durch eine Vision-Zielstufe-Logik und disziplinierte Coaching-Routinen." Kata ist also *PDCA mit Vision-Anker* — die Variante, die Vision-Bezug und Coaching-Disziplin in den Zyklus einbaut.

**6. Ressort der Iteration: Prozess vs. Produkt vs. Service.**

Iteriert wird je Fach über etwas anderes:

| Fach | Was wird iteriert? |
|---|---|
| BPM | Geschäftsprozess (klinischer Pfad, OP-Routine, Hygiene-Standard) |
| ITM-AK | Qualitätsmanagement-System / IT-Infrastruktur |
| SM | IT-Service (Incident-Prozess, Service Desk, Provisioning) |
| ITPM-Scrum | Software-Produkt (Inkrement) |

Konsequenz: dasselbe Werkzeug, andere Anwendungs-Domäne. Wer „PDCA für Software-Entwicklung" beantwortet, antwortet aus ITPM-Scrum (Empirische Prozesssteuerung). Wer „PDCA für klinische Prozesse" beantwortet, antwortet aus BPM. Wer „PDCA für IT-Services" beantwortet, antwortet aus SM-CSI.

**7. ITPM-Sprint-Retrospektive ↔ PDCA-Act — wo bleibt die Standardisierung?**

In BPM wird Act explizit als „Verbesserung standardisieren" beschrieben. In ITPM-Scrum entspricht das funktional der Sprint Retrospektive — die aber nicht primär standardisiert, sondern reflektiert und nächste Verbesserungen plant. Das ist ein subtiler Unterschied: BPM-PDCA betont Standardisierung als Abschluss, Scrum-Retrospektive betont kontinuierliches Lernen ohne fixierten Endpunkt. Beide sind iterativ; nur der „Abschluss-Charakter" einer Iteration ist unterschiedlich.

## Synthese für die mündliche Prüfung

**Diskussions-Achse 1: „Wo erscheint PDCA in der Vertiefung?"**

Sauberer Antwort-Aufbau:

1. **BPM**: PDCA-Zyklus als Standardmethode des KVP, mit Bewusstseinskreis als Vorbedingung und Fehlerkultur (Demings Punkt 8) als kultureller Voraussetzung.
2. **ITM-AK**: PDCA als methodische Klammer der ISO 9001:2015, mit konkreter Klausel-Zuordnung. Toyota Kata als PDCA-Variante mit Vision-Bezug.
3. **SM**: PDCA als ITIL CSI-Modell mit feinerer 6+1-Schritte-Granularität. CMMI als ergänzendes Bewertungsinstrument für Schritt 2.
4. **ITPM**: PDCA *nicht* im klassischen Vorgehen (Wasserfall), aber als Empirische Prozesssteuerung in Scrum mit den vier Anpassungs-Ereignissen.

**Diskussions-Achse 2: „Warum scheitert PDCA in der Praxis?"**

Antwort kombiniert ITM-AK-Diskussion und BPM-Fehlerkultur:

- ITM-AK-Note: „Druck zu kurzfristigen Ergebnissen schneidet Check und Act ab. Datenmangel macht Check schwierig. Lernen aus Fehlern erfordert Kultur, die nicht überall vorhanden ist."
- BPM-Fehlerkultur: ohne offene Kommunikation und sachliche Ursachenanalyse bleiben Fehler verborgen → kein Lerngewinn → Verbesserung unmöglich.
- BPM-Bewusstseinskreis: ohne abgeschlossenen Bewusstseinskreis ist die wirksame Anwendung des PDCA-Kreises nicht möglich.

Die saubere Synthese: PDCA ist methodisch trivial, kulturell und organisatorisch anspruchsvoll. Die Methode versagt nicht an der Methode, sondern an Datenverfügbarkeit (Check), Disziplin (Act) und Fehlerkultur (gesamter Zyklus).

**Diskussions-Achse 3: „Klassisch oder agil — wo passt PDCA?"**

Antwort aus ITPM:

- Klassisches PM (Wasserfall) ist deterministisch → kein PDCA.
- Agiles PM (Scrum) ist empirisch → PDCA-äquivalent über Empirische Prozesssteuerung.
- Auswahl-Kriterium: Stacey-Matrix-Komplexität. PDCA passt, wo Anforderungen unklar oder veränderlich sind und Lernen während der Umsetzung nötig ist.

Cross-Anschluss zu BPM/SM: Auch klinische Prozesse und IT-Services sind „komplexe Systeme" im Stacey-Sinne — daher der allgemein PDCA-orientierte Charakter dieser Fächer.

**Diskussions-Achse 4: „Welche PDCA-Variante hat welchen Nutzen?"**

| Wer es braucht | Modell | Stärke |
|---|---|---|
| Klinische Prozesse | BPM PDCA + Bewusstseinskreis | Kulturelle Voraussetzung explizit |
| QM-Systeme nach ISO | ITM-AK ISO 9001 PDCA | Norm-konformer Aufbau |
| IT-Services | SM CSI 6+1 | Feine Schritt-Granularität, KPI-Anker |
| Software-Entwicklung | ITPM Scrum / Empirische Prozesssteuerung | Time-Boxing, Inspect-&-Adapt-Disziplin |
| Strategische Verbesserung mit Vision | ITM-AK Toyota Kata | Vision-Anker, Coaching-Routine |

**Anschlussfragen, die ohne Cross-Fach-Verständnis schwer zu beantworten sind:**

- „Wo ist Plan im ITIL CSI-Modell?" — bei den Schritten 1 bis 4. Aus SM-CSI mit PDCA-Mapping.
- „Wo ist Act in der Sprint-Retrospektive?" — funktional ja, aber mit anderem Charakter (kein „Standardisieren", sondern „Lernen für nächsten Sprint"). Aus ITPM-BPM-Vergleich.
- „Welche ISO-9001-Klausel entspricht BPM-Check?" — Klausel 9 (Leistungsbewertung). Aus ITM-AK-PDCA-Mapping.
- „Was muss erfüllt sein, damit PDCA in einer Klinik wirkt?" — abgeschlossener Bewusstseinskreis (BPM) + gesunde Fehlerkultur (BPM Demings-Punkt-8) + Datenverfügbarkeit (ITM-AK-Diskussion).
- „Warum ist Toyota Kata nicht einfach PDCA?" — Kata baut Vision-Anker und Coaching-Disziplin ein, PDCA ist generisch. Aus ITM-AK Kata-Note.
- „Wie erkennt man, dass eine PDCA-Implementierung Theater ist?" — wenn nur Plan und Do durchlaufen werden, Check und Act nicht. Cross-Synthese aus ITM-AK-Diskussion und BPM-Diskussionsfrage.

## Verwandt

**BPM:**
- [[BPM - PDCA-Zyklus]]
- [[BPM - Grundprinzip - Kontinuierliche Verbesserung]]
- [[BPM - Fehlerkultur - Deming]]
- [[BPM - Bewusstseinskreis]]
- [[BPM - Phase 2 - 4-Schritte-Methode]]
- [[BPM - Methode - Ishikawa 7M]]
- [[BPM - Methode - 5-Warum]]
- [[BPM - Diagram - PDCA und Bewusstseinskreis]]

**ITM-AK:**
- [[ITM-AK - PDCA-Zyklus]]
- [[ITM-AK - ISO 9001-2015]]
- [[ITM-AK - Toyota Kata - Verbesserungs-Kata]]
- [[ITM-AK - Qualität - Donabedian-Dimensionen]]

**SM:**
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - CMMI - Reifegradmodell]]
- [[SM - SWOT-Analyse]]

**ITPM:**
- [[ITPM - Vorgehensmodelle - Klassisch vs Agile]]
- [[ITPM - Scrum - Empirische Prozesssteuerung]]
- [[ITPM - Scrum - Meetings]]
- [[ITPM - Stacey Matrix - Komplexitätseinordnung]]
- [[ITPM - Wasserfallmodell]]
- [[ITPM - Diagram - Vorgehensmodelle Vergleich]]
- [[ITPM - Diagram - Scrum Zyklus]]

**Andere Brücken:**
- [[Cross - Qualitaetsmanagement]] (PDCA als gemeinsamer Roter Faden der drei QM-Sichten)

**MOCs:**
- [[BPM - MOC]]
- [[ITM-AK - MOC]]
- [[SM - MOC]]
- [[ITPM - MOC]]

## Quelle

Cross-Fach-Synthese aus den oben gelisteten BPM-, ITM-AK-, SM- und ITPM-Konzept-Notes.

**Wichtige Quellen-Beobachtungen:**

- BPM-PDCA-Note nennt „Deming-Kreis" als Synonym; ITM-AK-PDCA-Note nicht.
- ITM-AK-PDCA-Note macht das ISO-9001-Mapping konkret (Klauseln 6/7/8/9/10); BPM-PDCA-Note nicht.
- SM-Vorlesung nutzt das Wort „PDCA" nicht direkt — verwendet stattdessen „Continual Service Improvement". Das Mapping CSI ↔ PDCA ist Synthese, nicht direkt aus dem Vault zitiert.
- ITPM-Scrum-Empirische-Prozesssteuerung-Note macht das Mapping Inspect-&-Adapt ↔ PDCA *nicht* explizit. Auch dieses Mapping ist Synthese.
- BPM-Bewusstseinskreis als Vor-PDCA-Stufe ist BPM-spezifisch — keine andere Vorlesung im Vault.

**Fach-Zuordnung der Quellen:**

| Note | Fach |
|---|---|
| BPM - PDCA-Zyklus / Grundprinzip - Kontinuierliche Verbesserung / Fehlerkultur - Deming / Bewusstseinskreis | BPM |
| ITM-AK - PDCA-Zyklus / ISO 9001-2015 / Toyota Kata - Verbesserungs-Kata | ITM-AK |
| SM - ITIL Continual Improvement - Modell / CMMI - Reifegradmodell | SM |
| ITPM - Vorgehensmodelle - Klassisch vs Agile / Scrum - Empirische Prozesssteuerung | ITPM |
