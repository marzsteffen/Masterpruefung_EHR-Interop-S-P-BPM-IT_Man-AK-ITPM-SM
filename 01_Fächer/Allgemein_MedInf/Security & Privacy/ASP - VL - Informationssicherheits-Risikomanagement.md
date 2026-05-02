---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/09 Informationssicherheits-Risikomanagement/09 Informationssicherheits-Risikomanagement.pdf
datum_vorlesung: 2024-11-13
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Informationssicherheits-Risikomanagement

## Überblick

Neunter und letzter Vorlesungsblock. Systematische Methode zur Verwaltung von Informationssicherheits-Risiken. Aufbau gemäß Big-Picture-Folie (7): Bestimmung des Kontexts, Risikoidentifikation, Risikoanalyse, Risikoevaluierung, Risikobehandlung, Risikokommunikation, Überwachung und Verbesserung. Insgesamt 56 Folien – das längste PDF im Fach.

## Lernziele (laut Vorlesung)

*Im PDF nicht als Lernziele-Liste ausgewiesen.* Aus dem Aufbau: Risiko-Begriff sauber definieren; die Risiko-Trias Asset/Bedrohung/Schwachstelle anwenden; den Risikomanagement-Prozess nach ISO 27005 verstehen; eine Asset-basierte Risikoidentifikation in sechs Schritten durchführen können (BSI 200-2 IT-Grundschutz); qualitative und quantitative Risikobewertungs-Methoden gegenüberstellen; die vier Risikobehandlungs-Strategien (Vermeidung, Reduktion, Transfer, Akzeptanz) anwenden; KPI vs. KRI unterscheiden; Risikoreporting strukturieren.

## Behandelte Konzepte

### Grundlagen
- [[ASP - Risikomanagement - Definition Risiko]]
- [[ASP - Risikomanagement - Grundvoraussetzungen]]
- [[ASP - Risikomanagement - Big Picture]]

### Kontextbestimmung
- [[ASP - Risikomanagement - Kontextbestimmung]]
- [[ASP - Risikomanagement - Risikomatrix]]
- [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]

### Risikoidentifikation
- [[ASP - Risikomanagement - Risikoidentifikation Ansaetze]]
- [[ASP - Risikomanagement - Asset-basierte Identifikation]]
- [[ASP - Risikomanagement - Strukturanalyse und Schutzbedarf]]
- [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]]

### Bewertung und Behandlung
- [[ASP - Risikomanagement - Risikobewertung]]
- [[ASP - Risikomanagement - Risikobehandlung]]

### Überwachung und Kommunikation
- [[ASP - Risikomanagement - Ueberwachung KPI KRI]]
- [[ASP - Risikomanagement - Risikokommunikation]]

## Roter Faden

**Risiko-Begriff (Folie 2):** Duden formuliert ihn negativ („möglicher negativer Ausgang"); ISO 27005:2022 abstrakter („effect of uncertainty on objectives") und neutral – ein Effekt kann positiv oder negativ sein, im Kontext Informationssicherheit aber meist negativ (Note 6 to entry).

**Drei Grundvoraussetzungen (Folie 3):** Ein Risiko entsteht nur, wenn alle drei zugleich erfüllt sind: ein **Asset**, eine **Bedrohung** und eine **Schwachstelle**. Die Folie zeigt das als Venn-Diagramm; die Schnittmenge ist das Risiko. Beispiele Folie 4: Server + Stromausfall + keine USV; Webserver + Hacking + ungeschütztes Netz; ERP + ehemaliger Mitarbeiter + fehlender Rechteentzug.

**Warum Risikomanagement (Folie 6):** systematische Methode für viele und komplexe Risiken. Erlaubt vergleichbare Bewertung, Priorisierung, geregelte Kommunikation, formelle Behandlungsentscheidung, definierte Rollen (Risiko-Eigner, Risikomanager) und regelmäßige Kontrolle.

**Big Picture (Folie 7, ISO 27005-Diagramm):** sieben Schritte, umrahmt von „Communication and Consultation" und „Monitoring and Review":
1. **Bestimmung des Kontexts** (Clause 6).
2. **Risikoidentifikation** (Clause 7.2).
3. **Risikoanalyse** (Clause 7.3).
4. **Risikoevaluierung** (Clause 7.4).
5. **Risikobehandlung** (Clause 8) – mit Decision Points, ob das Assessment ausreicht und ob das Restrisiko akzeptabel ist.
6. **Risikokommunikation** (Clause 10.3).
7. **Überwachung und Verbesserung** (Clause 10.5).

**Kontextbestimmung (Folien 9–15):** Festlegung des Geltungsbereichs (organisatorisch, physisch, technisch), Rollen (Risikomanager, Risiko-Eigner), Bewertungsskalen für Eintrittswahrscheinlichkeit (4-stufig: gering bis sehr hoch; alternativ Eintrittshäufigkeit pro Zeitraum), Schadensklassen (z. B. Beeinträchtigung der körperlichen Unversehrtheit, Imageschaden, finanzieller Schaden), Risikomatrix (Eintrittswahrscheinlichkeit × Auswirkung mit Risikoklassen rot/gelb/grün), Risikoklassen mit Umgangs-Vorgaben (hoch = zwingend behandeln, mittel = behandeln mit GF-Ausnahme, gering = behandeln wenn aufwandsvertretbar) und Risikoakzeptanzkriterien (wer akzeptiert was: Abteilungsleitung / Geschäftsführung / unzulässig).

**Risikoidentifikation (Folien 17–29):** Zwei Ansätze. **Ereignis-basiert** (top-down, übergeordnete strategische Szenarien) vs. **Asset-basiert** (bottom-up, einzelne Assets, ermöglicht spezifische Risikobehandlung). Die Vorlesung zeigt den Asset-basierten Ansatz in 6 Schritten:
1. Strukturanalyse und Schutzbedarfsfeststellung.
2. IT-Grundschutz-Modellierung gemäß **BSI 200-2** (Prozess-Bausteine ISMS, ORP, CON, OPS; System-Bausteine APP, SYS, IND, NET, INF).
3. Erstellung einer Gefährdungsübersicht (elementare + spezifische + zusätzliche Gefährdungen).
4. Erstellung einer Anforderungsübersicht (Soll-Ist-Vergleich Schutzmaßnahmen pro Baustein).
5. Schwachstellenanalyse.
6. Erstellung einer Risikoliste (Wer + tut was + gegen wen + mit welcher Auswirkung).

**Risikobewertung (Folien 31–37):** Risiko = Eintrittswahrscheinlichkeit × Auswirkung. Zwei Methodengruppen. **Qualitativ** (Ordinalskalen, Matrizen, intuitiv, gut für schwer quantifizierbare Risiken; Schwächen: subjektiv, Matrix-Fehler). **Quantitativ** (metrische Skalen, finanzielle Schadenshöhe × Frequenz pro Jahr, ermöglicht Kosten-Nutzen-Vergleich, Konfidenzintervalle für Unsicherheit; höhere Komplexität, Werkzeuge wie CRISAM erforderlich).

**Risikobehandlung (Folien 39–41):** Vier Strategien:
1. **Vermeidung** (Tätigkeit/Prozess wird nicht durchgeführt → Risiko eliminiert).
2. **Reduktion** (risikoreduzierende Maßnahmen).
3. **Transfer** (Verantwortung verlagern, z. B. Versicherung).
4. **Akzeptanz** (Restrisiko in Kauf nehmen).

Risikobehandlungsplan-Tabelle: Risiko, Strategie, konkrete Maßnahme, Umsetzungsfrist, Verantwortlicher, Kosten, Auswirkung auf Risiko, Restrisiko.

**Überwachung und Verbesserung (Folien 43–45):** Kontinuierliche Verbesserung des Prozesses. **KPI** = Erfolg/Effektivität messen. **KRI** = potenzielle Risiken überwachen. Schwellwerte definieren, ab denen automatisch Maßnahmen ausgelöst werden.

**Risikokommunikation (Folien 47–49):** Risikobericht ermöglicht Steuerung, Priorisierung, Transparenz und ist vertrauensbildend für Stakeholder. Frequenz hängt von Größe, Komplexität, Risikolage ab – mindestens jährlich, bei großen Unternehmen quartalsweise. Formate: schriftliche Berichte, Dashboards, Präsentationen, Meetings.

## Zentrale Aussagen / Take-aways

- **Risiko-Trias:** Asset + Bedrohung + Schwachstelle. Alle drei nötig, sonst kein Risiko.
- **ISO 27005:2022:** „effect of uncertainty on objectives" – formal neutral; in der Praxis negativ.
- **7-Schritte-Prozess (Big Picture):** Kontext, Identifikation, Analyse, Evaluierung, Behandlung, Kommunikation, Überwachung.
- **Risikomatrix** mit Eintrittswahrscheinlichkeit × Auswirkung; Anzahl Klassen (3×3 vs. 4×4) bestimmt Granularität.
- **Asset-basierte Identifikation in 6 Schritten** über BSI 200-2 IT-Grundschutz-Methodik.
- **Risiko = Eintrittswahrscheinlichkeit × Auswirkung.**
- **Vier Behandlungsstrategien:** Vermeidung, Reduktion, Transfer, Akzeptanz.
- **KPI ≠ KRI:** KPI misst Performance, KRI misst Risiko-Indikatoren.
- **Risikobericht** mind. jährlich; Quartalsweise bei großen Unternehmen.

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Business Continuity Management]] (BCM-Risikoanalyse als Spezialfall)
- [[ASP - VL - Einfuehrung und Motivation]] (Schutzziele, CIA-Triade, DSGVO)
- [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (Bausteine zur Risikoreduktion)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/09 Informationssicherheits-Risikomanagement/09 Informationssicherheits-Risikomanagement.pdf`
- Folienanzahl: 56
- Vortragender: Dr. Kevin Theuermann
- Datum laut Vorlesungsplan (Kapitel 01, Folie 4): 13.11.2024
