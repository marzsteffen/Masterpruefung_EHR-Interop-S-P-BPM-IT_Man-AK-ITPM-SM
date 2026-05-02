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

# SM - IT-Strategie - Schritt 1 IST-Analyse

> [!info] Kurzdefinition
> Erster Schritt im 7-Schritte-Modell von Johanning (2019). Interne Analyse der IT entlang von **vier Kategorien** mit insgesamt **18 Untersuchungsfeldern**: IT-Prozesse, IT-Governance/Organisation/Mitarbeiter, Technologie und Finanzen. Output: Reifegrad-Netzdiagramm und Handlungsfelder als Grundlage für die weiteren Schritte.

## Beschreibung

Schritt 1 (Buchkapitel 5) liefert die Ausgangslage. Johanning betont:

> „Wer etwas verbessern will, muss die Ausgangslage kennen."

Die Ist-Analyse orientiert sich nicht 1:1 an CMM(I) oder anderen Reifegradmodellen, sondern extrahiert im Sinne eines besseren **IT-Business-Alignments** die für die IT-Strategie relevanten Bewertungsfelder.

## Bestandteile / Aufbau

### Vier Untersuchungskategorien mit 18 Feldern

| Kategorie | Untersuchungsfeld | Inhalt |
|---|---|---|
| **IT-Prozesse** | Projektmanagement | Wie gut werden Projekte geführt? Standards? |
|  | Demand Management | Reibungslose Zusammenarbeit IT ↔ Fachbereich |
|  | Supply Management | Technischer Kern der IT-Organisation |
|  | Service Management | Reifegrad der ITIL-Prozesse in Operations |
|  | Quality Assurance / Quality Management | Qualitätsdefinitionen, Reporting, Monitoring |
| **IT-Governance, IT-Organisation, IT-Mitarbeiter** | IT-Governance-Strukturen | COBIT-Standards, Verzahnung Corporate ↔ IT-Governance |
|  | Sourcing-Strategie | Zusammenarbeit mit externen Lieferanten |
|  | Rollen und Verantwortlichkeiten | Klare Linien-/Projektzuständigkeiten |
|  | Business-IT-Alignment | Verzahnung Fachbereich ↔ IT |
|  | Mitarbeiterentwicklung | Fachliche und Soft-Skill-Weiterqualifizierung |
| **Technologie** | Architekturmanagement | Bebauungsplan für Applikationslandschaft |
|  | IT-Sicherheit & Disaster Recovery Management | Schutz, Notfallplan, Verfügbarkeit |
|  | IT-Infrastruktur und Betrieb | Reibungsloser Betrieb |
|  | Stammdatenmanagement | Datenqualität, Pflegeprozesse |
|  | Softwareentwicklung | Vorgehensmodelle, Lasten-/Pflichtenhefte, Customizing |
| **Finanzen** | Optimale Kostenstrukturen | Kostenarten, Kostenstellen, Kostenträger |
|  | IT-Controlling | KPIs, BSC, Reporting |
|  | Compliance | COBIT, Lizenzmanagement, GDPdU, Datenschutz |

### Methodik (Fragebogen + Auswertung)

1. **Inputs:** Prozesshandbücher, IT-Organigramme, Sourcing-Konzepte, Architekturskizzen, Netzwerkstruktur, Sicherheitskonzepte, Notfallpläne, Schulungsunterlagen, Lasten-/Pflichtenhefte etc.
2. **Beteiligte:** unter Leitung des Projektleiters/CIO, in größeren Projekten neutraler Dritter (auf IT-Strategie spezialisierter Berater); Abgleich mit Vorgesetztem (Geschäftsführung/Vorstand) obligatorisch.
3. **Erhebung:** strukturierte Interviews + Recherchen.
4. **Fragebogen-Aufbau:** pro Untersuchungsfeld 5 Fragen mit je 3 Antworten (Punkte: 0 / 5 / 10).
5. **Bewertung pro Fragebogen:** Punktezahl in Reifegrad 1–5 übersetzt:
   - 0–10 Punkte → 1
   - 11–20 Punkte → 2
   - 21–30 Punkte → 3
   - 31–40 Punkte → 4
   - 41–50 Punkte → 5
6. **Output:** Übertragung in **Netzdiagramm** mit allen 18 Feldern als Achsen.
7. **Ableitung der Handlungsfelder:** Alle Bereiche mit Bewertung **≤ 2** sind Handlungsfeld und werden in den Schritten 2–7 weiter ausgearbeitet. Bewertung 1 = sehr dringend; 2 = dringlich.

### Beispiel Produktio weltweit GmbH (Buch-Beispiel)

Auswertung im Buch: 8 Handlungsfelder identifiziert (Demand Management, Service Management, IT-Governance-Strukturen, Sourcing-Strategie, Rollen & Verantwortlichkeiten, IT-Controlling, Compliance, Projektmanagement). Die ursprüngliche Scope-Definition des Projektes wurde dadurch um diese 8 Felder erweitert.

## Beispiel

*Im Buch wird der Fragebogen exemplarisch für IT-Prozess „Projektmanagement" und „Demand Management" durchgespielt.* Beispielfragen aus Projektmanagement (Auszug):

- „Wie oft sind in den vergangenen fünf Jahren IT-Projekte gescheitert (im Sinne von Budget- oder Terminüberschreitungen)?" → Mehr als 50 % [0] · Max. 10 % [5] · Gar nicht [10]
- „Gibt es ein eigenes Project-Management-Office? Findet eine ständige Weiterbildung aller Mitarbeiter zu Projektmanagementthemen statt?" → Nein [0] · Ja, aber noch nicht etabliert [5] · Ja, voll funktionsfähig und leistet gute Unterstützung [10]

(Der Fragebogen umfasst pro Feld 5 Fragen — siehe Buchkapitel oder PDF-Arbeitsblätter 4.6–4.23.)

## Abgrenzung

- **IST-Analyse vs. SWOT** (siehe [[SM - SWOT-Analyse]]): IST-Analyse ist die *Innensicht*, SWOT verbindet Innen- und Außensicht. Beide ergänzen sich; SWOT folgt nach IST-Analyse.
- **IST-Analyse vs. CMMI/COBIT-Fähigkeitsstufen** (siehe [[SM - CMMI - Reifegradmodell]] und [[SM - COBIT 2019 - Fähigkeitsstufen]]): Strukturell ähnlich (1–5-stufige Bewertung); Johannings IST-Analyse ist aber breiter (18 Felder) und IT-Strategie-fokussiert.
- **IST-Analyse vs. CSI-Schritt 2 „Wo stehen wir gerade?"** (siehe [[SM - ITIL Continual Improvement - Modell]]): Inhaltlich verwandt — beides Standortbestimmung. CSI ist Service-fokussiert, IST-Analyse strategie-fokussiert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Untersuchungskategorien hat Schritt 1 nach Johanning? — IT-Prozesse, IT-Governance/Organisation/Mitarbeiter, Technologie, Finanzen.

**Anwendungsfrage:** Welche 18 Untersuchungsfelder gibt es? Wie wird das Ergebnis ausgewertet (Punktzahl → Reifegrad → Netzdiagramm → Handlungsfelder)?

**Diskussionsfrage:** Wie wird ein „Handlungsfeld" definiert? — Bereich mit Bewertung ≤ 2 im Reifegrad-Modell (Punktzahl ≤ 20).

**Mögliche Anschlussfragen:**
- Warum 5 Fragen pro Feld mit 0/5/10-Punkte-Antworten?
- Wer ist im Idealfall der Erheber? — Projektleiter, CIO, ggf. neutraler Dritter; Abgleich mit Geschäftsführung obligatorisch.
- Welche Eingangsdokumente sind hilfreich? — Prozesshandbücher, Organigramme, Architekturskizzen, Sourcing-Konzepte, Sicherheitskonzepte, Notfallpläne, Lasten-/Pflichtenhefte etc.
- Wie integriert sich Schritt 1 in den Gesamtstrategie-Erarbeitungsprozess?
- Welche Beziehung besteht zu COBIT (in Frage 1 zu IT-Governance-Strukturen explizit referenziert)?

## Verwandt

- [[SM - VL - IT-Strategie 7 Schritte]]
- [[SM - IT-Strategie - 7 Schritte nach Johanning]]
- [[SM - IT-Strategie - Definition]]
- [[SM - CMMI - Reifegradmodell]]
- [[SM - COBIT 2019 - Fähigkeitsstufen]]
- [[SM - SWOT-Analyse]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - IT-Strategie - Schritt 2 Herausforderungen und IT-Vision]] *(folgt)*

## Quelle

- Vorlesung: [[SM - VL - IT-Strategie 7 Schritte]]
- PDF: `Folien/Servicemanagement/Folien/IT-Strategie/Schritt 1 IST-Analyse.pdf` (32 Seiten = Johanning Kap. 5, S. 67–98)
- Quelle: Johanning, V. (2019). *IT-Strategie.* Wiesbaden: Springer Fachmedien

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
