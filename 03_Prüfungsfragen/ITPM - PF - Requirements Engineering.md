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

# ITPM - PF - Requirements Engineering

Prüfungsfragen-Sammlung zu Requirements Engineering: Grundlagen, Anforderungstypen, Kano-Modell, Erhebung, Dokumentation, Prüfung, Verwaltung und Aufwand.

---

## Definition

Was bedeutet Requirements Engineering, und welche drei Kernaspekte müssen erfüllt sein?

?

**Requirements Engineering (RE)** sorgt dafür, dass im Projekt alle Anforderungen bekannt, verstanden und dokumentiert sind.

**Drei Kernaspekte (Definition laut Vorlesung):**
1. Anforderungen sind **bekannt** und zu einem gewissen Grad **verstanden**
2. Involvierte Stakeholder sind mit allen Anforderungen entsprechend **einverstanden**
3. Anforderungen sind **ausreichend dokumentiert**

**Charakter:** kooperativ, iterativ, inkrementell – nicht alle Anforderungen sind von Beginn an bekannt. Wichtig: Der Teil, der in der **bevorstehenden Iteration** behandelt wird, ist **genauestens bekannt**.

**Relevanz:** 60 % aller Fehler in Softwaresystemen sind auf mangelhafte Requirements zurückzuführen.

Quelle: [[ITPM - Requirements Engineering - Grundlagen]]

---

Welche drei Kategorien von Anforderungen unterscheidet die Vorlesung, und was ist eine Anforderung grundsätzlich?

?

**Definition:** Eine Anforderung ist alles, was ein Produkt **können bzw. leisten muss**. Sie ist zugleich eine **Qualitätseigenschaft**.

**Drei Kategorien:**

| Kategorie | Frage | Beispiel |
|---|---|---|
| **Funktionale Anforderungen** | Was soll das System tun? | Use Cases, Funktionen |
| **Qualitätsanforderungen** | Wie gut, schnell, zuverlässig? | Antwortzeiten, Verfügbarkeit, IT-Sicherheit |
| **Geforderte Randbedingungen** | Welche Vorgaben sind einzuhalten? | Technologien, Compliance |

**Abgrenzung:** Diese Klassifikation nach Inhaltstyp ist **orthogonal** zum Kano-Modell (Klassifikation nach Kundenwirkung) – beide Sichten können kombiniert werden.

Quelle: [[ITPM - Anforderung - Definition]]

---

Was ist das Kano-Modell, und welche drei Anforderungsarten unterscheidet es?

?

Das **Kano-Modell** klassifiziert Anforderungen nach ihrer **Wirkung auf die Kundenzufriedenheit**:

| Art | Beschreibung | Auto-Beispiel (Vorlesung) |
|---|---|---|
| **Basisanforderungen** | Selbstverständlich; werden oft vergessen zu nennen. Fehlen → starke Unzufriedenheit | Auto ist versperrbar |
| **Leistungsanforderungen** | Verlangte Leistung, teilweise Nice-to-Have mit Zusatzkosten; explizit kommuniziert | Metallic-Lackierung |
| **Begeisterungsfaktoren** | Unerwartet; begeistern den Kunden | Keyless-System |

**Verbindung zu Erhebungstechniken:**
- Basisanforderungen → **Beobachtungstechniken** (werden vergessen zu nennen)
- Leistungsanforderungen → **Befragungstechniken**
- Begeisterungsfaktoren → **Kreativitätstechniken**, Prototyping

Quelle: [[ITPM - Kano-Modell - Anforderungsarten]]

---

Welche vier Haupttätigkeiten umfasst die Arbeit eines Requirements Engineers?

?

Laut Vorlesung (Folie 63) hat ein Requirements Engineer **vier Haupttätigkeiten**:

1. **Ermittlung** von Anforderungen (Erhebung)
2. Anforderungen entsprechend **dokumentieren**
3. **Prüfung** der Anforderungen auf Konsistenz und Widerspruchsfreiheit
4. Ergänzung von **Prioritäten und Statusangaben**

**Abgrenzung Requirements Engineer vs. Projektleiter:**
- RE: Ermittelt, spezifiziert, prüft, verwaltet Anforderungen + erhebt Stakeholder
- PL: Definiert Ziele + Produktvision, plant RE-Aufwände, steuert den RE-Prozess, verantwortet Stakeholder-Relationship-Management

**Grundsatz:** Die Projektziele sind für den RE eine treibende Kraft. Anforderungen müssen **präzise, widerspruchsfrei und vollständig** erfasst werden.

Quelle: [[ITPM - Requirements Engineer - Rolle]], [[ITPM - Requirements Engineering - Grundlagen]]

---

Was ist das Lastenheft, wer erstellt es, und welche Pflichtinhalte gehören hinein?

?

Das **Lastenheft** (User Requirements Specification) ist eine Zusammenstellung aller Anforderungen des **Auftraggebers** in Bezug auf den Liefer- und Leistungsumfang – aus **Anwendersicht**.

**Pflichtinhalte (Vorlesung Folie 23):**
- Beschreibung der Ausgangssituation
- Aufgabenstellung
- Schnittstellen
- Anforderungen an die Systemtechnik
- Anforderungen an den Betrieb
- Anforderungen für die Inbetriebnahme
- Anforderungen an die Qualität
- Anforderungen an die IT-Sicherheit

**Abgrenzung Lastenheft vs. Pflichtenheft:**
- **Lastenheft** = Auftraggeber, Anwendersicht: „Was soll erreicht werden?"
- **Pflichtenheft** = Auftragnehmer, Lösungssicht: „Wie soll es realisiert werden?"
- Beide sollten **dieselbe Inhaltsstruktur** haben → leichterer Abgleich.

Sollte **sehr früh** im Projekt erstellt werden.

Quelle: [[ITPM - Lastenheft]]

---

## Anwendung

Welche sechs Gruppen von Erhebungstechniken kennt die Vorlesung, und welche passt zu welcher Kano-Anforderungsart?

?

**6 Gruppen laut Vorlesung (Folien 65–66):**

| Technik | Anwendung | Kano-Passung |
|---|---|---|
| **Befragung** (Interview, Fragebogen) | Explizit kommunizierbare Anforderungen; Interview-Dreistufenplan: Fragen → Zuhören → Mit eigenen Worten wiederholen | Leistungsanforderungen |
| **Feldbeobachtung** | Beobachtung bei der Arbeit mit kurzen Zwischenfragen | Basisanforderungen |
| **Apprenticing** | Arbeitsablauf beobachten + selbst ausprobieren, ob alles richtig erfasst wurde | Basisanforderungen |
| **Vergangenheitsorientiert** | Dokumentenanalyse von Altsystemen → Problemthemen identifizieren | Alle Arten |
| **Simulation / Prototyping** | Im PDF nur als Begriff genannt | Begeisterungsfaktoren |
| **Kreativitätstechniken** (Brainstorming) | Sammeln → Strukturieren → Bewerten; mit- und vorausdenken | Begeisterungsfaktoren |

**Werkzeuge:** Mindmaps (Strukturierung), Audio-/Videoaufzeichnungen (zeitlich begrenzte Stakeholder).

Quelle: [[ITPM - RE - Erhebungstechniken]]

---

Welche drei Dokumentationswege gibt es im RE, und welche UML-Diagrammtypen werden für welche Fragestellung eingesetzt?

?

**Drei Dokumentationswege (Folie 67):**

| Weg | Ziel | Methoden |
|---|---|---|
| **Schreiben** | Präzise, detaillierte Spezifikation | Textuelle Anforderungen |
| **Malen** | Überblick schaffen | UML, BPMN |
| **Vorzeigen** | Verständnis prüfen, erste Tests | Prototypen |

**UML-Diagrammtypen und ihre Fragestellung:**

| Diagramm | Einsatz |
|---|---|
| **Use-Case-Modellierung** | Überblick Systemfunktionalität; Akteure (Strichmännchen) + Abläufe (Ellipsen) |
| **Aktivitätsdiagramm** (inkl. BPMN) | Schritt-für-Schritt-Abläufe mit Verzweigungen und Wiederholungen |
| **Zustandsdiagramm** | Nicht-lineare Abläufe mit internen/externen Ereignissen; Systemzustände |
| **Sequenzdiagramm** | Schritt-für-Schritt in einem konkreten Fall; Nachrichten zwischen Objekten |

**Pflichtinhalte eines Requirements-Dokuments:** Projektziele, Abgrenzung, drei Anforderungsarten, **Glossar**, Abkürzungsverzeichnis.

Quelle: [[ITPM - RE - Dokumentation und Modellierung]]

---

Welche drei Methoden der Anforderungsprüfung gibt es, und wann sollte geprüft werden?

?

**Was wird geprüft?**
- **Form:** Entspricht das Dokument Unternehmensstandards? Inhaltsverzeichnis vorhanden? Scope abgegrenzt? Use Cases mit Akteur + Name?
- **Inhalt:** Korrektheit, Vollständigkeit, Verständlichkeit.

**Wann prüfen?**

| Zeitpunkt | Bewertung |
|---|---|
| **Ständig** (beim Erheben + Dokumentieren) | **Beste Variante** – Fehler sofort erkannt |
| **Zu Meilensteinen** | Pragmatischer Mittelweg |
| **Am Ende des RE** | **Risikoreichste** – Änderungen kommen spät |

**Drei Methoden (Folie 77):**

| Methode | Ablauf |
|---|---|
| **Review / Gutachten** | Dokument an Prüfer → Stellungnahme → Nachbesprechung |
| **Inspektion** | Dokument an Gruppe → vorab prüfen → gemeinsamer Termin → Mängel dokumentieren |
| **Walkthrough** | Ersteller führt Prüfer durch das Dokument → Mängel dokumentieren → beheben → Freigabe |

**Beteiligte:** Auftraggeber, Endanwender, Abnehmer des Dokuments (Architekten/Designer für Machbarkeit).

Quelle: [[ITPM - RE - Anforderungsprüfung]]

---

Welche Attribute hat eine verwaltete Anforderung, und nach welchen Kriterien wird sie priorisiert?

?

**Pflichtattribute einer Anforderung (Folie 78):**
- **Eindeutige ID**
- **Name**
- **Begründung**
- **Abnahmekriterien**
- **Beteiligte Personen** (z. B. Ersteller)
- **Status:** erfasst → geprüft → freigegeben

**Priorisierungskriterien:**
1. **Wert für den Kunden**
2. **Wert für Firma / Geschäft**
3. **Time to Market**
4. **Risiko und Aufwand**

**Weitere Aspekte (Folie 79):**
- **Abhängigkeiten** zwischen Anforderungen abbilden
- **Versionsverwaltung** – Anforderungen können sich ändern

**Hinweis:** Die Statusmenge (erfasst/geprüft/freigegeben) ist im PDF eng gefasst; reale Tools haben oft mehr Statusstufen.

Quelle: [[ITPM - RE - Anforderungsverwaltung]]

---

Wie verteilt sich der Aufwand in einem mittelgroßen Projekt, und welche Arbeiten sind in den ersten 1–5 % des Aufwands zu priorisieren?

?

**Aufwandsverteilung (Folie 82):**

| Bereich | Anteil |
|---|---|
| Requirements | 22,5 % |
| Architektur / Design | 22,5 % |
| Codierung / Unit-Test | 22,5 % |
| Integration / Abnahmetest | 22,5 % |
| Management | 10 % |

*Basis: je ¼ auf die vier Entwicklungsbereiche; Management-Anteil ~10 % → jeweils 22,5 % für die übrigen.*

**Frühe Aufgaben in 1–5 % des Gesamtaufwands (Folie 84):**
1. **Ziele definieren**
2. **Stakeholder erheben** (Suchprozess: Know-how → Rolle → Person)
3. **Funktionale Anforderungen in Use Cases zerlegen** – je 2–4 Sätze → 80–90 % der Anwendungsfälle gefunden
4. **15–30 wichtigste Begriffe** für das Glossar definieren
5. **Offensichtliche nicht-funktionale Anforderungen**, wichtigste Qualitätsanforderungen, härteste Randbedingungen identifizieren

Quelle: [[ITPM - RE - Aufwand und Kostenschätzung]]

---

## Diskussion

„60 % aller Fehler in Softwaresystemen sind auf mangelhafte Requirements zurückzuführen." Welche Konsequenzen hat das für die Projektplanung?

?

**Aussage der Vorlesung (Folie 62):** 60 % aller Fehler entstehen durch mangelhaftes RE. Wenn das Verständnis für Anforderungen unzureichend ist, wird die Software nicht so aussehen, wie sie soll; schlecht definierte Anforderungen können unterschiedlich interpretiert werden.

**Konsequenzen für die Projektplanung:**

1. **RE ist keine optionale Phase** – Unterschätzung rächt sich in Fehlerkosten und Nacharbeiten (Fehler-Kosten-Eskalation: in der Anforderungsphase billiger zu beheben als in der Abnahme)
2. **Investition in RE zahlt sich aus:** ca. 22,5 % des Gesamtaufwands für Requirements sind angemessen und kein Overhead
3. **Frühzeitige Prüfung ist Pflicht:** ständige Prüfung besser als Batch-Review am Ende
4. **Stakeholder aktiv einbinden** – Anforderungen, die nicht kommuniziert wurden, fehlen im Lastenheft → regelmäßige Reviews mit Auftraggeber und Endanwendern

**Kritische Gegenposition:**
- Die 60 %-Zahl ist empirisch schwer zu verifizieren und hängt stark vom Projekttyp ab
- In agilen Projekten werden Fehler durch kontinuierliches Feedback früher entdeckt – aber das setzt voraus, dass RE iterativ stattfindet

Quelle: [[ITPM - Requirements Engineering - Grundlagen]]

---

Warum müssen Basisanforderungen besonders sorgfältig erhoben werden, obwohl sie „selbstverständlich" wirken?

?

**Problem:** Basisanforderungen werden vom Kunden selten explizit genannt, weil sie als selbstverständlich vorausgesetzt werden. In Interviews und Fragebögen (Befragungstechniken) tauchen sie kaum auf.

**Konsequenz bei Fehlen:** Starke Unzufriedenheit – obwohl das Feature nie aktiv verlangt wurde, ist sein Fehlen ein K.O.-Kriterium.

**Beispiel (Vorlesung):** Ein Auto ist versperrbar – kein Käufer würde das im Verkaufsgespräch als Anforderung nennen; fehlt es, ist das Produkt unbrauchbar.

**Erhebungsstrategie für Basisanforderungen:**
- **Feldbeobachtung:** Benutzer bei der Arbeit beobachten – was tun sie, ohne darüber nachzudenken?
- **Apprenticing:** Selbst ausprobieren, was die Stakeholder täglich tun

**eHealth-Beispiel:** Patientenportal – „Login funktioniert auf Mobilgeräten" wird niemand explizit nennen, aber fehlt es, ist das System unbrauchbar.

**Zeitdimension:** Begeisterungsfaktoren werden über Zeit zu Basisanforderungen (z. B. Kamera im Smartphone war 2003 Begeisterungsfaktor, heute Basisanforderung) → RE muss Marktkontext berücksichtigen.

Quelle: [[ITPM - Kano-Modell - Anforderungsarten]]

---

Vergleichen Sie klassisches RE (Lastenheft/Pflichtenheft) mit agilem RE (Backlog/User Stories). Wo sind die Grenzen beider Ansätze?

?

| Dimension | Klassisches RE | Agiles RE |
|---|---|---|
| **Zeitpunkt** | Weitgehend vor Realisierung abgeschlossen | Kontinuierlich, iterativ |
| **Hauptdokument** | Lastenheft → Pflichtenheft | Product Backlog (User Stories, Epics) |
| **Vollständigkeit** | Anspruch: vollständig vor Umsetzung | Bewusst unvollständig; Detaillierung im Refinement |
| **Änderungsmanagement** | Formal über Change Requests | Sprint-Backlog-Anpassung, Sprint-Goal-Schutz |
| **Stakeholder-Einbindung** | Intensiv in RE-Phase, danach reduziert | Kontinuierlich (Sprint Review, Backlog Refinement) |

**Grenzen klassisch:**
- Anforderungen ändern sich während der Umsetzung → teuer
- Vollständigkeit kaum erreichbar → false sense of security
- Lange Vorlaufzeit vor erstem Feedback

**Grenzen agil:**
- In regulierten Umgebungen (Medizintechnik, MDR) ist Vollständigkeitsdoku verpflichtend → Backlog allein reicht nicht
- Technisch komplexe Systeme (z. B. KIS-Kern) brauchen stabile Architekturentscheidungen, die iteratives RE erschweren

**Fazit:** Die Vorlesung empfiehlt **kooperatives, iteratives, inkrementelles RE** – kein Widerspruch zu klassischen Dokumenten, solange die Kernprinzipien (bekannt, einverstanden, dokumentiert) eingehalten werden.

Quelle: [[ITPM - Requirements Engineering - Grundlagen]], [[ITPM - Lastenheft]]

---

Im agilen Kontext fallen Requirements Engineer und Product Owner oft zusammen. Ist das sinnvoll?

?

**Argument dafür (Zusammenführung):**
- Der PO ist ohnehin für Backlog-Priorisierung und Anforderungsklarheit zuständig
- In kleinen Teams ist eine dedizierte RE-Rolle oft nicht finanzierbar
- Kurze Feedbackschleifen (Sprint Review) ersetzen formale RE-Prüfprozesse teilweise
- Kontinuierliche Stakeholder-Einbindung reduziert Missverständnisse

**Argument dagegen (Trennung):**
- Der PO muss gleichzeitig strategische Vision vertreten UND technische Anforderungen präzise spezifizieren – das ist eine Doppelbelastung
- RE erfordert andere Skills als Backlog-Management (Modellierung, UML, Konsistenzprüfung)
- In regulierten Umgebungen (eHealth, MDR) braucht Anforderungsdokumentation formale Gründlichkeit, die der PO unter Sprint-Druck nicht leisten kann
- Interessenkonflikt: PO priorisiert für den Business Value; RE-Integrität erfordert vollständige Abdeckung auch „unattraktiver" Anforderungen

**Fazit:** Zusammenführung ist pragmatisch vertretbar in kleinen Projekten mit geringer regulatorischer Anforderung; in Health-IT-Kontexten ist eine zumindest teilweise Trennung der Verantwortlichkeiten empfehlenswert.

Quelle: [[ITPM - Requirements Engineer - Rolle]]

---

Welche Probleme entstehen, wenn Anforderungshierarchie-Ebenen übersprungen werden (z. B. direkt von Business Vision zu Component Requirements)?

?

**Die vier Ebenen laut Vorlesung:**
1. **Business Vision** – Was will der Kunde erreichen? Rechtfertigt die Investition.
2. **Stakeholder / Kundenanforderungen** – Fachliche Anforderungen (Quality in Use)
3. **System- / Software Requirements** – Technische Produktanforderungen (Product Quality)
4. **Component Requirements** – Einzelne Komponenten

**Probleme beim Überspringen von Ebenen:**

*Von Vision direkt zu Components:*
- Lösung wird vor vollständigem Problemverständnis definiert
- Technische Details beeinflussen fachliche Anforderungen → **Solution Bias**
- Stakeholder können Component Requirements nicht validieren – sie kennen keine Systemarchitektur

*Von Stakeholder Requirements direkt zu Components:*
- System-Level-Architekturentscheidungen fehlen → inkonsistente Komponentenentwicklung
- Fehlende Schnittstellendefinitionen zwischen Komponenten

*Von Vision direkt zu Stakeholder Requirements (Ebene 1 überspringen):*
- Anforderungen haben keine gemeinsame Richtung → verschiedene Stakeholder definieren in unterschiedliche Richtungen
- Geschäftlicher Nutzen bleibt unklar → Investitionsentscheidung nicht nachvollziehbar

**Fazit:** Jede Ebene dient als Validierungsanker für die nächste. Der iterative Abstieg ist kein bürokratischer Overhead, sondern strukturelle Fehlervermeidung.

Quelle: [[ITPM - QM - Hierarchische Anforderungsdoku]]
