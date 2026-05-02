---
fach: itpm
typ: pruefungsfrage
status: offen
tags:
  - fach/vertiefung/itpm
  - typ/pruefungsfrage
  - status/offen
  - flashcards
---

# ITPM - PF - Projektsteuerung Detail

Prüfungsfragen-Sammlung zu Projektüberwachung, Projektsteuerung, EVM, Trendanalysen, Teufelsquadrat und 90%-Syndrom.

---

## Definition

Was ist Projektüberwachung, und welche drei Phasen umfasst sie?

?

**Definition (Folie 80):** In der Projektüberwachung werden Sollvorgaben der Projekt- und Systemplanung mit den im Projektablauf erreichten Ist-Werten verglichen und Planabweichungen festgestellt. Bezieht sich auf **Projektgegenstand** und **Projektablauf**.

**Voraussetzungen:**
- Realitätsbezogene, vollständige und prüfbare **Planvorgaben**
- Aktuelle **Ist-Daten**

**Drei Phasen (Folie 81):**
1. **Datenermittlung** – aktuelle Situation im Projekt erfassen
2. **Soll-Ist-Vergleich** – Abweichungen feststellen
3. **Bewertung** – Gründe für Abweichungen ermitteln

**Vier Dimensionen des Soll-Ist-Vergleichs:** Terminkontrolle · Kostenkontrolle · Kapazitätsüberwachung · Leistungsüberwachung

**Abgrenzung:** Überwachung **erkennt** Abweichungen; [[ITPM - Projektsteuerung]] **reagiert** darauf.

Quelle: [[ITPM - Projektüberwachung - Grundlagen]]

---

Was ist das 90%-Syndrom, wann tritt es auf, und wie begegnet man ihm?

?

**Definition:** In einer relativ frühen Projektphase (**30–60 % der Projektlaufzeit**) glaubt man, bereits **90 % des Projektergebnisses** erbracht zu haben.

**Ursachen:**
- Erworbene **Kenntnis des Lösungswegs** → subjektive Vollständigkeitsillusion
- **Unkenntnis** der noch auftretenden Störungen und Restaufwände

**Folge:** Die Umsetzung einer erkannten Lösung erfordert tatsächlich noch erhebliche Aufwände. Subjektive Aufwandseinschätzungen der Mitarbeiter müssen hinterfragt und ggf. deutlich erhöht werden.

**Gegenmaßnahmen:**
- **Objektive Methoden** zur Fortschrittsmessung
- Im einfachsten Fall: **0/100-Methode** – ein Arbeitsergebnis gilt erst nach erfolgter Abnahme als fertig
- Aufwändigere Methoden: Definition einer Metrik (z. B. bestandene Tests, abgenommene Story Points) für laufend erbrachte Ergebnisse

Quelle: [[ITPM - 90% Syndrom]]

---

Wie werden CPI und SPI im Earned Value Management berechnet, und wie sind sie zu interpretieren?

?

Das **Earned Value Management (EVM)** ist die Standardmethode des PMBOK Guide für Projekt-Controlling. Es integriert Zeit, Aufwand und Qualität/Umfang (Magisches Dreieck) in eine gemeinsame Bewertung. Eingeführt **1967 vom US-Verteidigungsministerium**.

**Drei Basiswerte:**

| Größe | Bedeutung |
|---|---|
| **EV** (Earned Value) | Fertigstellungswert |
| **AC** (Actual Cost) | Ist-Kosten |
| **PV** (Planned Value) | Planwert |

**Zwei Indizes:**

| Index | Formel | Interpretation |
|---|---|---|
| **CPI** (Cost Performance Index) | `CPI = EV / AC` | < 1: über Budget · = 1: im Budget · > 1: unter Budget |
| **SPI** (Schedule Performance Index) | `SPI = EV / PV` | < 1: hinter Plan · = 1: im Plan · > 1: vor Plan |

Quelle: [[ITPM - Earned Value Management]]

---

Was ist das Teufelsquadrat nach Sneed, und wie unterscheidet es sich vom Magischen Dreieck?

?

Das **Teufelsquadrat nach Sneed** erweitert das [[ITPM - Projektsteuerung - Magisches Dreieck]] um eine vierte Dimension und visualisiert den Zielkonflikt geometrisch: Die **Fläche des Quadrats bleibt konstant** – jede Änderung einer Größe muss durch andere Größen kompensiert werden.

**Vier Steuerungsgrößen:**
1. **Kosten**
2. **Qualität**
3. **Zeit**
4. **Inhalt / Umfang**

**Unterschied zum Magischen Dreieck:**
- Magisches Dreieck: **3 Dimensionen** (Zeit, Kosten, Qualität/Umfang) – Qualität und Umfang zusammengefasst
- Teufelsquadrat: **4 Dimensionen** – Qualität (Code-Qualität, Zuverlässigkeit) und Umfang (Funktionsumfang) explizit getrennt, weil sie in der Praxis **unterschiedlich verhandelt** werden

**Kernaussage (Vorlesung):** „Je mehr der verbleibenden Größen unantastbar sind, desto geringer ist der Handlungsspielraum für den Projektleiter."

Quelle: [[ITPM - Projektsteuerung - Teufelsquadrat]]

---

Was ist die Meilensteintrendanalyse (MTA), und welche Verlaufsmuster gibt es?

?

Die **Meilensteintrendanalyse (MTA)** verfolgt geplante Meilensteintermine über die Projektlaufzeit hinweg. Sie zeigt Verschiebungen früh genug, um Korrekturmaßnahmen zu ermöglichen.

**Aufbau:**
- **X-Achse:** Berichtszeitpunkte (z. B. monatlich)
- **Y-Achse:** geplante Meilensteintermine
- Pro Meilenstein wird zu jedem Berichtspunkt der **dann erwartete Endtermin** eingetragen und verbunden

**Verlaufsmuster:**

| Verlauf | Bedeutung |
|---|---|
| **Waagrecht** | Meilenstein hält den geplanten Termin |
| **Steigend** | Meilenstein verschiebt sich (Verzug) |
| **Fallend** | Meilenstein wird vorgezogen (selten) |

**Abgrenzung:**
- MTA → verfolgt **Termine** (zeitliche Dimension)
- [[ITPM - Kostentrendanalyse]] → verfolgt **Kosten/Aufwände**
- [[ITPM - Agile - Burn-Down-Chart]] → storypoint-basiert, agil

Quelle: [[ITPM - Meilensteintrendanalyse]]

---

## Anwendung

Welche typischen Ursachen für Kostenüberschreitungen nennt die Vorlesung, und wie unterscheiden Sie „echte" von „bewussten" Überschreitungen?

?

**6 Ursachen für Kostenüberschreitungen (Folie 84):**
1. **Ungenaue Projektabgrenzung** – unnötige Arbeiten werden erledigt
2. **Management-Entscheidung, zu tief anzubieten** (Pricing-to-win, Max-Budget → [[ITPM - Aufwandsschätzung - Politische Methoden]])
3. **Unkontrollierte Änderungen** – nachträglich wird ein „Rolls-Royce" verlangt
4. **Aufholen zeitlicher Verzögerungen** – Überstunden treiben Kosten
5. **Unvorhersehbare technische Schwierigkeiten**
6. **Abrechnung projektfremder Kosten**

**„Echte" vs. „bewusste" Überschreitungen:**

| Typ | Ursache | Reaktion |
|---|---|---|
| **Technisch/echt** | Komplexität unterschätzt, Fehlqualifikation, unvorhersehbare Probleme | Nachschätzung, Scope-Anpassung, Ressourcen prüfen |
| **Bewusst/politisch** | Pricing-to-win, zu tiefes Angebot in Akquisephase | Eskalation, Change Request, Risikoklärung |

**Präventiv:** Risikozuschlag von 15 % im Kostenplan sichert gegen unvorhersehbare Kosten ab.

Quelle: [[ITPM - Kostenüberwachung]]

---

Was unterscheidet Kapazitätsüberwachung und Leistungsüberwachung, und welche Ursachen für Abweichungen nennt die Vorlesung?

?

| Dimension | Kapazitätsüberwachung | Leistungsüberwachung |
|---|---|---|
| **Fragestellung** | Wie viel Personal ist gebunden? | Wie gut/viel wurde geleistet? |
| **Vergleich** | Geplante vs. tatsächlich benötigte Kapazitäten | Geplante vs. erreichte Qualität/Quantität |
| **Methoden** | Kapazitätsplanung, Stunden-Soll-Ist | Besprechungen während AP-Bearbeitung; Reviews nach AP-Ende |

**Ursachen für Kapazitätsabweichungen (Folie 85):**
- Mitarbeiter sind **falsch qualifiziert** oder eingesetzt
- Mitarbeiter werden **zu früh fertig** (Parkinson's Law-Effekt)
- Mitarbeiter werden in **andere Projekte abgezogen**
- Mitarbeiter **finden kein Ende**

**Grundsatz Kapazitätssteuerung:** Mitarbeiter **so spät wie möglich** einsetzen und **so früh wie möglich** herausnehmen.

**Voraussetzung Leistungsüberwachung:** Nur produktiv, wenn ein **vernünftiges Fehlerklima** etabliert ist. Leistungsüberwachung muss sowohl **durchgeführt** als auch vom Team **akzeptiert** werden.

Quelle: [[ITPM - Kapazitätsüberwachung]], [[ITPM - Leistungsüberwachung]]

---

Was ist Projektsteuerung, und welche aktiven Steuerungselemente kennt die Vorlesung?

?

**Definition (Folie 87–88):** Projektsteuerung beinhaltet alle projektinternen Aktivitäten des Projektleiters, die erforderlich sind, um das geplante Projekt im Rahmen der Planungswerte abzuwickeln.

**Grundprinzip:** Planung ist zukunftsgerichtet und nimmt den Verlauf nur theoretisch vorweg. Nur durch aktive, wirkungsvolle Steuerung kann mit dem Erreichen des Projektziels gerechnet werden.

**Aktive Steuerungselemente (Folie 88):**
- **Formale Freigabe** von Arbeitspaketen
- **Eingreifen bei Abweichungen**
- **Sammeln von Informationen** – auch über informelle Kommunikation
- **Laufende Anpassung der Pläne** bei: neuen Erkenntnissen, Rahmenbedingungsänderungen, Kosten-/Terminüberschreitungen
- **Verzahnung von Systemführung und Projektführung:**
  - **Systemführung** = technische Entwicklung, Variantenauswahl
  - **Projektführung** = Mitteleinsatz, Termin-/Kostenplanung

**Steuerungs-/Überwachungs-Schleife:**
`Planung (SOLL) → Durchführung → Überwachung → Abweichung → Steuerung → neue SOLL → ...`

Quelle: [[ITPM - Projektsteuerung]]

---

Wie funktioniert Terminüberwachung, und welche besonderen Risiken gibt es?

?

**Terminüberwachung (Folie 82)** vergleicht:
- Geplante Meilensteine / Aufgabenenden mit **tatsächlichen Terminen**
- **Prozentuale Fertigstellungsgrade** – Vorsicht: **90%-Syndrom!**
- **Trendanalysen:** fallend, waagrecht, ansteigend

**Besondere Risiken:**
- **90%-Syndrom:** Mitarbeiter melden 90 % Fertigstellung, obwohl tatsächlich erst ~50 % erreicht – eine **klare, objektive Definition von Fertigstellung** ist zwingend (→ 0/100-Methode als Gegenmaßnahme)
- **Externe Faktoren:** Lieferzeiten von Zulieferern, Wartezeiten, fehlende Beistellungen

**Werkzeuge:**
- **Meilensteintrendanalyse** (MTA): verfolgt Terminentwicklung über Berichtszeitraum
- Soll-Ist-Terminvergleich
- Kritischer Weg ([[ITPM - Kritischer Weg]]): zeigt terminlich kritische Aufgabenketten

Quelle: [[ITPM - Terminüberwachung]]

---

## Diskussion

EVM gilt als mächtiges Controlling-Werkzeug – welche Schwächen hat es in IT-Projekten?

?

**Stärken von EVM:**
- Integriert Zeit, Kosten und Umfang in einem Modell → frühzeitige Trendprognose
- PMBOK-Standard → international etabliert und anerkannt
- CPI und SPI liefern objektive Kennzahlen für Steering-Committee-Berichte

**Schwächen in IT-Projekten:**

1. **Anforderungsinstabilität:** EVM setzt voraus, dass der Umfang (PV) zu Projektbeginn klar definiert ist → in Projekten mit volatilen Anforderungen liefert EV keine verlässliche Basis
2. **Schwierige EV-Messung:** Fertigstellungsgrade für Software sind notorisch subjektiv → 90%-Syndrom verfälscht den Earned Value
3. **Planqualität als Voraussetzung:** Unrealistische Planvorgaben → alle EVM-Kennzahlen führen in die falsche Richtung
4. **Keine Qualitätsaussage:** CPI/SPI sagen nichts über Code-Qualität, Testtiefe oder technische Schulden aus
5. **Agile Inkompatibilität:** Backlog-getriebene Entwicklung hat variablen Scope → klassischer PV nicht sinnvoll anwendbar; Velocity + Burn-Down ersetzen EVM in reinen Scrum-Projekten

**Fazit:** EVM ist in klassisch-plangetriebenen IT-Projekten mit stabilem Scope valide. In hybriden oder agilen Projekten braucht es ergänzende oder alternative Metriken.

Quelle: [[ITPM - Earned Value Management]]

---

Welche Dimension des Teufelsquadrats wird in IT-Projekten typischerweise geopfert, wenn drei Größen festgeschrieben sind?

?

**Ausgangslage:** Im Teufelsquadrat gilt die Fläche als konstant – wenn Zeit, Kosten und Inhalt fix sind, muss **Qualität** nachgeben.

**Empirische Beobachtung in IT-Projekten:**

*Am häufigsten geopfert: **Qualität** (Code-Qualität, Testtiefe, Dokumentation)*
- Gründe: Qualitätsmängel sind kurzfristig weniger sichtbar als Terminverzüge
- Konsequenz: Technische Schulden, spätere Mehrkosten im Betrieb
- Aus Teufelsquadrat-Sicht: Qualitätsverlust ist oft der „unsichtbarste" Kompromiss

*Zweithäufig: **Inhalt** (Scope)*
- In agilen Projekten ist Scope-Reduktion explizit das bevorzugte Mittel (fixe Zeit + fixe Kosten, variabler Umfang)
- Klassisch: Change Requests schützen den Inhalt formal, aber informell wird „descoped"

**Problematik festgeschriebener Größen:**
- „Die beste Steuerung funktioniert nur, wenn noch Handlungsspielraum vorhanden ist"
- Wenn alle vier Größen vertraglich fixiert sind, ist der Projektleiter handlungsunfähig → Risikoklärung in der Angebotsphase ist entscheidend

**Fazit:** Qualität als Puffer ist kurzfristig verlockend, langfristig teuer. In regulierten Umgebungen (eHealth, MDR) ist Qualitätsreduktion oft nicht zulässig → Scope oder Zeit müssen dann wirklich verhandelbar sein.

Quelle: [[ITPM - Projektsteuerung - Teufelsquadrat]]

---

Welche Vor- und Nachteile hat die 0/100-Methode zur Fertigstellungsmessung gegenüber der Prozentsatz-Methode?

?

**0/100-Methode:** Ein Arbeitsergebnis gilt erst nach erfolgter **Abnahme** als fertig (100 %); bis dahin ist es 0 % fertig.

**Vorteile:**
- Vollständig **objektiv** – kein Raum für subjektive 90%-Schätzungen
- Verhindert das **90%-Syndrom** strukturell
- Klarer Abnahme-/Qualitätsprozess erzwungen
- Einfach messbar und nachvollziehbar (binär)

**Nachteile:**
- **Sehr konservativ** bei langen Arbeitspaketen – ein 3-Monats-AP steht monatelang bei 0 %
- **Keine Frühwarnung** bei intern schleichendem Verzug
- Schlechter geeignet für **Reporting an Stakeholder**, die Zwischenstände erwarten
- Kann **Demotivation** erzeugen, wenn Fortschritt erst spät sichtbar wird

**Prozentsatz-Methode:**
- Erlaubt **Zwischenstände** (z. B. 30 %, 60 %, 80 %)
- Anfällig für das **90%-Syndrom**: Mitarbeiter überschätzen systematisch ihren Fortschritt

**Kompromiss:** Aufwändigere Methoden definieren eine **Metrik** für laufend erbrachte Teilleistungen (z. B. bestandene Unit-Tests, abgenommene Story Points) – objektiver als Prozentsatz, granularer als 0/100.

Quelle: [[ITPM - 90% Syndrom]]

---

Warum ist „Fehlerklima" eine Voraussetzung für funktionierende Leistungsüberwachung – und was passiert, wenn es fehlt?

?

**Aussage der Vorlesung (Folie 86):** Leistungsüberwachung ist auf Dauer nur dann produktiv, wenn ein **vernünftiges Fehlerklima** installiert ist. Sie muss sowohl durchgeführt als auch **akzeptiert** werden.

**Was ist ein vernünftiges Fehlerklima?**
- Fehler werden als **Lernchance** betrachtet, nicht als Versagen
- Mitarbeiter können **Probleme offen melden** ohne Angst vor Sanktionen
- Überwachung dient der Entwicklung, nicht der Kontrolle

**Was passiert ohne Fehlerklima:**
- Mitarbeiter **schönen Statusberichte** → falsche IST-Daten → Überwachung liefert falsche Signale
- **90%-Syndrom** verstärkt sich: Probleme werden so lange wie möglich verborgen
- Fehlende Eskalation: Probleme werden nicht gemeldet, bis sie eskalieren
- Projektleiter verliert **Informationsqualität** – Steuerungsentscheidungen auf falscher Basis

**Verbindung zur Personalentwicklung:** Die Vorlesung betont, dass Leistungsüberwachung in personalintensiven Branchen (z. B. Software) **unternehmenskritisch** für die Personalentwicklung ist – nicht nur für Projektziele.

**Konsequenz:** Fehlerkultur ist keine Soft-Skill-Frage, sondern ein **strukturelles PM-Werkzeug** – ohne sie ist quantitative Überwachung wertlos.

Quelle: [[ITPM - Leistungsüberwachung]]

---

Welche Vorteile bieten MTA und KTA zusammen gegenüber EVM allein?

?

**MTA + KTA kombiniert:**

| Werkzeug | Stärke | Schwäche |
|---|---|---|
| **MTA** | Zeigt Termintrends über Zeit (Verschiebungen früh erkennbar) | Keine Kostenaussage |
| **KTA** | Zeigt Aufwandstrends über Zeit (Schätzungsänderungen sichtbar) | Keine Terminaussage |
| **EVM** | Integriert Termin + Kosten in CPI/SPI; ermöglicht Prognose | Setzt guten Ausgangsplan voraus; schwarze Box für Nicht-Controller |

**Vorteile MTA + KTA gegenüber EVM:**

1. **Einfacher verständlich:** Geschäftsführung und Lenkungsausschuss verstehen Trendverläufe ohne EVM-Vorkenntnisse
2. **Dimensionentrennung:** Zeit- und Kostentrends können unabhängig analysiert werden – eine Meilensteinkrise muss keine Kostenkrise sein
3. **Kein vollständiger Ausgangsplan nötig:** MTA/KTA funktionieren auch bei iterativer Planung, EVM setzt fixen PV voraus
4. **Frühwarnsignal:** Beide zeigen Trends über mehrere Berichtspunkte → Tendenzen sichtbar, bevor sie zu Eskalationen werden

**Fazit:** MTA + KTA sind pragmatische, kommunizierbare Werkzeuge für die laufende Projektkommunikation. EVM ist präziser und prognoseorientierter, aber voraussetzungsreicher. In der Praxis werden sie oft kombiniert eingesetzt.

Quelle: [[ITPM - Meilensteintrendanalyse]], [[ITPM - Kostentrendanalyse]], [[ITPM - Earned Value Management]]
