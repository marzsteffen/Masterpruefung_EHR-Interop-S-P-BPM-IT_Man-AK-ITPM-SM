---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Strategie 7 Schritte]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - IT-Strategie - Schritt 3 Applikationsstrategie

> [!info] Kurzdefinition
> Dritter Schritt nach Johanning (2019). Mit Portfolio- und Lebenszyklustheorie wird die Applikationslandschaft analysiert, bewertet und in eine Soll-Applikationsstrategie überführt. Output: Applikations-Roadmap mit drei Handlungsoptionen pro Applikation — behalten, ausmustern, modernisieren.

## Beschreibung

Schritt 3 (Buchkapitel 7) operationalisiert die in Schritt 2 abgeleiteten Handlungsstränge auf Applikationsebene. Hintergrund: Laut HP/Capgemini *Application Landscape Report 2011* halten 85 % der IT-Manager ihr Applikationsportfolio für überarbeitungsbedürftig — viele Kernapplikationen basieren auf veralteten Altanwendungen. Die Strategieoptionen sind **Standardisierung**, **Konsolidierung** oder **Ablösung**.

In der Wartung liegen historisch ca. **80 % des IT-Budgets** (Forrester). Reduzierung der Wartungskosten ist daher ein zentrales strategisches Asset.

## Bestandteile / Aufbau

### Motive für die Erstellung des Applikationsportfolios

- Schatten-Applikationen herausfiltern (Excel/Access ohne IT-Beteiligung entwickelt)
- Insellösungen transparent machen
- Doppel-/Mehrfachnutzung von Daten und Funktionen erkennen
- Heterogene technische Standards aufdecken
- Schnittstellenprobleme und Komplexitätsfallen identifizieren
- Legacy-Applikationen (stark veraltet) erkennen
- Abhängigkeiten zu Personen oder IT-Lieferanten transparent machen

### Compliance-Treiber für die Katalogisierung

- **SOX** (Sarbanes-Oxley)
- **KonTraG** (Gesetz zur Kontrolle und Transparenz im Unternehmensbereich, Deutschland)
- **GoBS** (Grundsätze ordnungsgemäßer DV-Buchführungssysteme)

### Applikationsportfolio nach BCG (auf Applikationen angewendet)

Achsen:
- **X-Achse:** Wichtigkeit der Applikation für den Fachbereich (Unterstützungsprozess ↔ wertschöpfender Prozess)
- **Y-Achse:** Reifegrad der Technologie (alt ↔ neu)
- Kreisgröße: Anzahl Benutzer
- Kreisfarbe: Höhe der Wartungskosten

**Vier Felder + Normstrategien** (nach Ward/Peppard, Hofmann/Schmidt):

| Feld (BCG) | Ward/Peppard | Charakteristik | Normstrategie |
|---|---|---|---|
| Question Marks | **High Potential / Wildcats** | Unklarer Beitrag, risikoreich | Prototypen/Pilotprojekte mit klaren Zeit- und Budgetlimits, **minimal integration**; nur erfolgreiche werden zu Strategic |
| Stars | **Strategic** | Wichtigste Unternehmensapplikationen | **Continuous improvement**, „High Value-Added"; sehr enge Business-IT-Abstimmung |
| Cash Cows | **Key Operational** | Sehr wichtig, Kern-/Management-/Supportprozesse, lange Lebensdauer | **Defensive innovation**, **high quality**, ressourcenschonende Wartung; Erweiterungen nur bei drohenden Wettbewerbsnachteilen |
| Poor Dogs | **Support** | Unterstützung weniger wichtiger Prozesse, Commodity | **Disinvest / Rationalize** — meist an externen Dienstleister abgeben; Eigenbetrieb nur bei Standardsoftware ohne Customization |

### ERP als Sonderfall

ERP-Systeme decken oft den Großteil der Applikationslandschaft ab. Empfehlung: **modulweise** im Portfolio betrachten. Beispiel SAP:
- **FI/CO, HR** → Standardprozesse, Unterstützung → linke Seite (Support/High Potential)
- **WM, JIT/JIS, MM** im produzierenden Umfeld → wertschöpfend, oft mit ABAP-Individualanpassungen → rechte Seite (Cash Cow/Stars)

### Applikationslebenszyklus (nach Heinrich)

Sechs Phasen mit charakteristischer Kosten/Nutzen-Kurve:

| Phase | Inhalt | Kosten/Nutzen |
|---|---|---|
| 1. Entwicklung | Ideenfindung, Software-Entwicklung (auch Customizing nach Einkauf!) | Höchste Kosten, kein Nutzen |
| 2. Systemeinführung | Schrittweise Einführung, Tests, Fehler beseitigen | Wachsende Nutzung |
| 3. Wachstum | Alle Tests abgeschlossen, alle Funktionen produktiv | Nutzung nimmt zu |
| 4. Sättigung/Reife | Höhepunkt der Nutzung | Nutzen am höchsten |
| 5. Rückgang | Nutzung nimmt ab (System nicht mehr aktuell, Aufgaben gehen zurück) | Sinkender Nutzen |
| 6. Abschaffung | Ablösung-Entscheidung, ggf. remanente Lizenzkosten/Umstellungskosten | Nur Restkosten |

Anmerkung: Technische Applikationen (z. B. Produktionssteuerung) haben längere Lebenszyklen als kommerzielle (z. B. ERP), die oft durch gesetzliche Änderungen kürzer leben.

### Bewertungskriterien für Applikationen

Bewertung mit Schulnoten **1–6**:

| Kriterium | Inhalt |
|---|---|
| Wartungskosten | Zu hoch / niedrig / marktgerecht? Benchmarks heranziehen. |
| Akzeptanz bei Anwendern | Usability, Bedienerfreundlichkeit, „Geredet wird über…" |
| Reifegrad der Prozessabbildung | Wie vollständig deckt die Applikation den Prozess ab? |
| Wahrscheinlichkeit kurzfristiger Prozessänderungen | Sich anbahnende Veränderungen in den nächsten 3 Jahren |
| Reifegrad der Technologie und Lock-In-Gefahr | Zukunftsfähigkeit der Plattform; Verfügbarkeit von Entwicklern |

### Drei Handlungsoptionen

| Option | Inhalt |
|---|---|
| **Behalten** | Kein Handlungsbedarf |
| **Ausmustern** | Wegwerfen und ggf. ersetzen oder Funktionalität in eine bestehende Applikation integrieren |
| **Modernisieren** | Auf neuen technologischen Stand bringen — z. B. Web-Enable, Integration Legacy mit neuen Technologien, Re-Host, Wegwerfen und Neuschreiben |

### Applikations-Roadmap

Zeitstrahl mit allen Änderungen, Ergänzungen und Neuanschaffungen — Grundlage für die spätere Ressourcenplanung (Kapital, Mitarbeiter, Know-how) und das IT-Projektportfolio in [[SM - IT-Strategie - Schritt 6 Umsetzung Roadmap Budget Projektportfolio]].

## Beispiel

Buch-Beispiel Produktio weltweit GmbH (gekürzt):

| Applikation | Bewertung | Handlung |
|---|---|---|
| SAP FI | 3/4/4/Ja-SEPA/3 | **Modernisieren** — Standardisierung, SEPA, Auslandsstandorte integrieren |
| SAP CO | 3/3/4/Nein/3 | **Modernisieren** — DB-Rechnungen direkt in CO |
| SAP HCM | 3/4/5/Ja/3 | **Modernisieren** — Standardisierung Personalprozesse, Zeitwirtschaft |
| SAP WM/SD | 3/2/2/Nein/3 | **Behalten** |
| MES Siemens | 5/3/3/Nein/5 | **Modernisieren/Ausmustern** — Schnittstelle zu SAP, Neuausschreibung |
| Salesforce | 2/2/3/Nein/2 | **Behalten** |
| MS Access „OldStyle" | 4/3/4/Nein/3 | **Ausmustern** — Schatten-IT, Legacy |
| MS Access „Lieferantendaten" | 4/2/4/Nein/3 | **Ausmustern** — in ERP integrieren |

Die Applikations-Roadmap legt Maßnahmen über mehrere Jahre fest — z. B. 2014: SAP FI/CO Auslandsstandorte + SEPA + DMS-Einführung; 2015: SAP HCM Erweiterungen + MES-Ausschreibung; 2016: SAP-MES-Schnittstelle; 2017: Roll-out an allen Auslandsstandorten.

## Abgrenzung

- **Applikationsportfolio vs. UN-Produktportfolio (Schritt 2)**: Beide nutzen die BCG-Logik, aber auf unterschiedliche Objekte angewendet. Schritt 2 = Produkte/SGEs des Unternehmens; Schritt 3 = IT-Applikationen.
- **Applikationslebenszyklus vs. Servicelebenszyklus** (siehe [[SM - ITIL V3 - Servicelebenszyklus]]): Servicelebenszyklus (V3) ist ein generisches ITSM-Modell; Applikationslebenszyklus folgt Produktlebenszyklus-Logik mit konkreten 6 Phasen pro einzelner Applikation.
- **Modernisieren vs. Ausmustern**: Modernisierung verlängert die Lebensdauer (Web-Enable, Re-Host, Refactoring); Ausmustern beendet sie.
- **Applikationsstrategie vs. Sourcing-Strategie**: Schritt 3 entscheidet *was* mit Applikationen geschieht; [[SM - IT-Strategie - Schritt 4 Sourcing-Strategie]] entscheidet *wer* sie betreibt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Felder und Normstrategien hat das Applikationsportfolio nach Ward/Peppard? — High Potential (Pilotprojekte, minimal integration), Strategic (continuous improvement), Key Operational (defensive innovation, high quality), Support (disinvest/rationalize).

**Anwendungsfrage:** Wie viele Phasen hat der Applikationslebenszyklus nach Heinrich? — 6: Entwicklung, Systemeinführung, Wachstum, Sättigung/Reife, Rückgang, Abschaffung.

**Diskussionsfrage:** Warum gilt für Cash-Cow-Applikationen die Devise „defensive innovation"? — Kosteneffektivität geht vor Innovation; Wartung wird mit zunehmendem Alter teuer. Ressourcen werden für strategische Applikationen freigehalten.

**Mögliche Anschlussfragen:**
- Welche fünf Bewertungskriterien werden für Applikationen verwendet?
- Welche drei Handlungsoptionen gibt es pro Applikation?
- Wie geht man mit ERP-Systemen im Portfolio um? — Modulweise betrachten.
- Was ist eine Schatten-Applikation und warum ist sie problematisch?
- Welche Compliance-Treiber gibt es (SOX, KonTraG, GoBS)?
- Welcher Anteil des IT-Budgets fließt typischerweise in Wartung? — 80 % (Forrester).

## Verwandt

- [[SM - VL - IT-Strategie 7 Schritte]]
- [[SM - IT-Strategie - Schritt 1 IST-Analyse]]
- [[SM - IT-Strategie - Schritt 2 Herausforderungen und IT-Vision]]
- [[SM - IT-Strategie - Schritt 4 Sourcing-Strategie]]
- [[SM - IT-Strategie - Schritt 6 Umsetzung Roadmap Budget Projektportfolio]]
- [[SM - ITIL V3 - Servicelebenszyklus]]
- [[SM - ITIL Practice - Service Configuration Management]]

## Quelle

- Vorlesung: [[SM - VL - IT-Strategie 7 Schritte]]
- PDF: `Folien/Servicemanagement/Folien/IT-Strategie/Schritt 3.pdf` (29 Seiten = Johanning Kap. 7, S. 127–155)
- Quelle: Johanning, V. (2019). *IT-Strategie.* Wiesbaden: Springer Fachmedien
- Im PDF zitiert: Ward/Peppard [39], Hofmann/Schmidt [25/24], Heinrich [22], HP/Capgemini Application Landscape Report [13/14], Forrester [16]

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
