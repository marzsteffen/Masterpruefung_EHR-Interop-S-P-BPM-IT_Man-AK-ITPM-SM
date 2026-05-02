---
fach: itpm
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/itpm
---

# ITPM - PF - Aufwandsschätzung Detail

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile
> - Niveau-Konvention: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Themenbereich vertieft die Aufwandsschätzung vollständig: Grundlagen, Cone of Uncertainty, drei Teilbereiche (Größe/Aufwand/Kosten), vier Verfahrensklassen (Delphi, Prozentsatz, Analogie, algorithmisch) plus politische Methoden, Top-down vs. Bottom-up, Drei-Punkt-Schätzung, Function-Point-Methode (5 Hauptfunktionsgruppen), CoCoMo (3 Phasen, Basic-Formeln), sowie Kostenplan und Kostenarten. Quelle: Vorlesungen „Aufwandsschätzung Kosten Personal Controlling" und „Initiierung Strukturierung Requirements".

## Verlinkte Konzepte

- [[ITPM - Aufwandsschätzung - Grundlagen]]
- [[ITPM - Cone of Uncertainty]]
- [[ITPM - Aufwandsschätzung - Schätzverfahren Übersicht]]
- [[ITPM - Aufwandsschätzung - Top-down vs Bottom-up]]
- [[ITPM - Aufwandsschätzung - Delphi-Methode]]
- [[ITPM - Aufwandsschätzung - Prozentsatzmethode]]
- [[ITPM - Aufwandsschätzung - Analogiemethode]]
- [[ITPM - Aufwandsschätzung - Function Point]]
- [[ITPM - Aufwandsschätzung - CoCoMo]]
- [[ITPM - Aufwandsschätzung - Politische Methoden]]
- [[ITPM - Aufwandsschätzung - Drei-Punkt]]
- [[ITPM - Kostenplan]]
- [[ITPM - Kostenarten und Finanzierung]]
- [[ITPM - Projektstrukturplan]]
- [[ITPM - Earned Value Management]]

---

## Karten

### Definition

Was ist Aufwandsschätzung, welche Rolle spielt sie für den Projekterfolg, und welche Best Practices nennt die Vorlesung?
?
**Definition:** „Berechnet im Vorfeld durch Analyse wesentlicher Faktoren die voraussichtlichen Kosten und die Zeit eines Projekts oder Arbeitspakets." Ziel: möglichst genaue Angaben zum Aufwand für Projektplanung oder Angebotserstellung. **Bedeutung:** Erfolg oder Misserfolg ist maßgeblich von der Qualität der Schätzung abhängig; Grundlage für tragfähigen Business Case, Termin-/Meilensteinplanung, Ressourcen, Verträge. **Kosten der Schätzung:** ca. **1–3 % der Projektkosten**. Personalaufwände sind in Software-Projekten meist die teuersten Positionen; PM-Aufwand wird oft als **Aufschlag (ca. 15 %)** auf die Entwicklung berechnet. **Best Practices (Jones 2007):** mehrere Verfahren + mehrere Schätzer; Workshops; erfahrene Spezialisten; in Arbeitsstunden/Punkten schätzen, nicht in Kalendertagen; Faktor für Unvorhersehbares; dokumentieren und nachvollziehbar machen.

Was beschreibt der Cone of Uncertainty, auf welche Untersuchung geht er zurück, und welche Konsequenzen hat er für die Planung?
?
Der Cone of Uncertainty beschreibt die **Abnahme der Schätzunsicherheit** im Projektverlauf. Geht zurück auf **Untersuchungen der NASA**. Eine Schätzung **vor der Anforderungsphase** ist im Durchschnitt mit Unsicherheit von **Faktor 4** belastet: die tatsächlichen Kosten können 4-fach kleiner oder 4-fach größer sein. Die Unsicherheit nimmt stetig ab, erreicht aber erst mit **Projektende 0 %**. **Konsequenzen:** (1) Frühe Schätzungen können nur grobe Näherungen sein. (2) Projektplan sollte die Unsicherheiten widerspiegeln und beinhalten. (3) Schätzungen müssen an Phasenübergängen **regelmäßig aktualisiert** werden. (4) Unsicherheiten können direkt in die Schätzungen einfließen.

Welche vier Hauptverfahren der Aufwandsschätzung gibt es, und welche zusätzlichen Methoden nennt die Vorlesung?
?
| Verfahren | Beispiel |
|---|---|
| **Expertenbefragung** | Delphi-Methode (Standard- und Breitband-Delphi) |
| **Kennzahlverfahren** | Prozentsatzmethode |
| **Vergleichsmethoden** | Analogiemethode |
| **Algorithmische Verfahren** | Function-Point-Methode, CoCoMo |
**Zusätzlich:** Politische Methoden (**Pricing-to-win**, **Max-Budget**) – keine Schätzverfahren im engeren Sinne; das Budget bestimmt den Aufwand, nicht umgekehrt. Wichtig: In der Praxis werden mehrere Verfahren **kombiniert**; Einzelmethoden erhöhen das Fehlerrisiko.

Wie lautet die Formel der Drei-Punkt-Schätzung, und wozu dienen die drei Werte?
?
**Drei Werte:** tO = optimistische Zeit (Minimum), tW = wahrscheinliche Zeit (Normalfall), tP = pessimistische Zeit (Maximum). **Formel:** `t = (tO + 4·tW + tP) / 6`. Die wahrscheinliche Zeit wird **vierfach gewichtet**, weil sie den realistischsten Wert repräsentiert (Beta-Verteilung). Ziel: Unsicherheit explizit machen und in die Schätzung einbeziehen. **Beispiel (Standardlehrbuch, nicht Vorlesung):** tO = 4, tW = 7, tP = 12 → t = (4 + 28 + 12) / 6 = 44/6 ≈ 7,33 Tage. Verbindung: Drei-Punkt eignet sich für die Schätzung einzelner Arbeitspakete im Ablauf-/Terminplan; die Cone-of-Uncertainty-Logik ist implizit enthalten (Bandbreite tO–tP).

Welche fünf Hauptfunktionsgruppen und welche drei Komplexitätsgruppen hat die Function-Point-Methode?
?
**Fünf Hauptfunktionsgruppen:** (1) Externe Inputs, (2) Externe Outputs, (3) Interne Dateien, (4) Externe Abfragen, (5) Externe Schnittstellen. **Drei Komplexitätsgruppen:** Niedrig, Mittel, Hoch. **Berechnungsweg:** Funktionen ermitteln → in Hauptfunktionsgruppen einordnen → Komplexität bewerten → Function Points per Tabelle → Aufwand per Tabelle. **Charakteristik:** funktionalitätsbasiert, **sprachunabhängig** (unabhängig von der Implementierungssprache). Konkrete Tabellenwerte sind **im Vorlesungs-PDF nicht enthalten**.

Welche drei Phasen hat CoCoMo, auf welcher Größe basiert es, und wie lauten die Basic-CoCoMo-Formeln?
?
**CoCoMo** (Constructive Cost Model) = algorithmisches Verfahren für Softwareentwicklung; Basis: **LOC (Lines of Code) / KDSI (Kilo Delivered Source Instructions)**. **Drei Phasen:** (1) **Basic CoCoMo** – Formeln: `Aufwand [PM] = A × Größe[KDSI]^B` / `Dauer [Monate] = C × Aufwand^D`. (2) **Intermediate CoCoMo** – 15 Kostentreiber (K1–K15) multiplizieren den Basic-Aufwand; im PDF nicht einzeln aufgeführt. (3) **Detailed CoCoMo** – wie Intermediate, aber mit verfeinerter Aufgabenliste. **Basic-CoCoMo-Projekttypen:** Organic (A=2,4; B=1,05; C=2,5; D=0,38) / Semi-detached (A=3,0; B=1,12; C=2,5; D=0,35) / Embedded (A=3,6; B=1,20; C=2,5; D=0,32).

### Anwendung

Ein Projekt wird als „Semi-detached" eingestuft und hat 50 KDSI. Berechnen Sie nach Basic CoCoMo Aufwand und Dauer.
?
**Gegeben:** Projekttyp Semi-detached → A=3,0; B=1,12; C=2,5; D=0,35. Größe = 50 KDSI. **Aufwand:** `3,0 × 50^1,12 = 3,0 × 79,9 ≈ 240 Personenmonate`. **Dauer:** `2,5 × 240^0,35 = 2,5 × 6,82 ≈ 17 Monate`. Die 15 Kostentreiber des Intermediate CoCoMo würden diesen Wert mit einem Multiplikations-Faktor anpassen (im PDF nicht einzeln definiert). **Hinweis:** LOC-Schätzungen sind schwierig für moderne Frameworks; die Ergebnisse sind Richtwerte, keine Garantien. Das Verfahren ist eher für große, klar abgegrenzte Softwareprojekte geeignet.

Wie funktioniert die Delphi-Methode (Standard vs. Breitband), und für welche Projekte ist sie geeignet?
?
**Delphi = Expertenbefragung durch strukturierte Mehrfachbefragung** (entwickelt von RAND-Corporation / O. Helmer). Geeignet für **große Projekte** (hoher Aufwand). **Standard-Delphi:** (1) PL schildert Vorhaben, Formular ausgeben. (2) Experten füllen **getrennt** aus – keine Diskussion untereinander. (3) PL analysiert, erstellt neues Formular mit Ausreißer-Kommentaren. (4) Experten überarbeiten selbständig. (5) Wiederholen bis Annäherung. (6) **Durchschnittswert** = Ergebnis. **Breitband-Delphi:** Zusätzlich **gemeinsame Sitzungen** (Kick-off + zwischen Runden) zur Diskussion der Ausreißer – schnellere Konvergenz, aber Anonymität eingeschränkt. **Hauptvorteil Anonymität:** Meinungsänderung ohne Gesichtsverlust möglich; kein Konformitätsdruck; besonders wertvoll bei **innovativen Vorhaben**. Nachteil: Großer Zeitbedarf.

Wie wird die Prozentsatzmethode nach Hewlett-Packard angewendet, und welches Risiko hat sie?
?
**Prozentsatzmethode:** keine eigenständige Methode – Detailschätzung **einer Phase** mit anderer Methode, Hochrechnung auf den Gesamtaufwand via erfahrungsbasierter Prozentverteilung. **HP-Verteilung (Folie 36):** Analyse 18 % / Entwurf 19 % / Implementierung 34 % / Test 29 %. **Anwendungsbeispiel:** Implementierungsaufwand geschätzt = 800 PT → Gesamtaufwand = 800 / 0,34 ≈ 2350 PT. **Voraussetzung:** Erfahrungswerte aus abgeschlossenen vergleichbaren Projekten. **Vorteile:** zeitsparend, oft überraschend genau. **Risiko:** Fehler in der Detailschätzung werden **multipliziert** – ein 10 %-Fehler in der Implementierungsschätzung ergibt 10 % Fehler im gesamten Projekt.

Welche Eckpunkte hat ein Kostenplan, und wann darf das Budget geändert werden?
?
**Eckpunkte (Folie 56):** phasenorientiert vorgehen; Änderungen berücksichtigen; mehrere Personen beteiligen; vorsichtig bewerten; Genauigkeit nicht übertreiben; Folgekosten (Wartung) berücksichtigen; sonstige Kosten (Admin, Meetings, Wartezeiten); **Risikozuschlag 15 %**; **Gewinnzuschlag 15 %**. **Budget darf geändert werden bei:** (1) Änderung des **Leistungsumfangs**. (2) Neue Kostenschätzung liefert **realistischere Werte**. (3) Plankosten für konkrete Aufgabe reichen nicht aus und können durch andere Minderkosten **nicht aufgefangen** werden. Grundsatz: Kosten lassen sich in **frühen Projektphasen** noch stark beeinflussen – spätes Eingreifen ist wirkungslos; nicht hoffen, in späten Phasen noch zu sparen.

Was sind die drei Kostengruppen und welche Finanzierungsformen gibt es?
?
**Drei Kostengruppen:** Fixkosten, variable Kosten, Gemeinkosten. **Kostenarten:** Personalkosten (Ingenieurs-/Sachbearbeiterstunden, Fremdpersonal), Maschinenkosten, Montagekosten, Vorhaltezeiten, Materialkosten, Lizenzkosten, Werkzeugkosten, IT/Verwaltung, Reisekosten, Vertriebskosten. **Formel:** `Aufwand = Aufwandsmenge × Kostensatz`. **Drei Finanzierungsformen:** (1) **Vorauszahlung** – Auftraggeber stellt vollständige Mittel zu Projektbeginn. (2) **Vorausgehende phasenbezogene Zahlungen** – Mittel vor jeder Phase, sodass Kosten zu jedem Zeitpunkt gedeckt. (3) **Phasenbezogene gemischte Finanzierung** – Mittel decken Kosten zu „vielen", aber nicht allen Zeitpunkten. Grundsatz: Projektkosten sollen vollständig vom Auftraggeber getragen werden; positiver Ertrag ist zusätzliches Ziel.

Worin unterscheiden sich Top-down und Bottom-up als Schätzstrategien, und welches Risiko hat jede?
?
**Top-down:** Aufwand für das **gesamte Projekt** aus allgemeiner Funktionalität schätzen, dann auf Teilfunktionen aufteilen. Basis: logische Funktionen, nicht Komponenten. **Gefahr:** geht nicht genug auf wichtige Details ein. Geeignet für **frühe Projektphasen**, Grobschätzung. **Bottom-up:** Aufwand für **jede Komponente** einzeln bestimmen; Gesamtaufwand = Summe. **Gefahr:** projektübergreifende Aktivitäten (PM, QS, Koordination) werden vergessen. Geeignet für **detaillierte Planung** mit ausgearbeitetem Pflichtenheft. **Best Practice:** kombinieren – Top-down für erste Orientierung, Bottom-up zur Validierung; bei starker Abweichung: Ursache analysieren, nicht einfach mitteln. Verbindung: Auch bei der PSP-Erstellung gibt es Top-down vs. Bottom-up als Strukturierungsrichtung.

### Diskussion

„Eine Schätzung ist nicht mit Verhandeln zu verwechseln" – wie reagieren Sie, wenn ein Auftraggeber den Aufwand halbieren möchte?
?
Kernsatz aus der Vorlesung (Folie 25): „Eine Schätzung kann nur reduziert werden, wenn Leistungsumfang oder Qualität reduziert wird." **Konsequente Haltung:** (1) Aufwandsreduktion ist nur möglich durch **Scope-Reduktion** (weniger Features), **Qualitätsreduktion** (weniger Tests, weniger Dokumentation) oder **Risikoerhöhung** (Puffer streichen). (2) Der Auftraggeber muss die Konsequenz **explizit akzeptieren und dokumentieren**. (3) Magisches Dreieck / Teufelsquadrat: Wer eine Variable erzwingt, beeinflusst die anderen – das ist kein Verhandlungsspielraum, sondern eine physikalische Konsequenz. **Typischer Praxisdruck:** Erwartungshaltung des Auftraggebers (Eisberg-Modell); politische Methoden (Pricing-to-win) verführen, dennoch nachzugeben. **Gegenmaßnahme:** Schätzung transparent dokumentieren und Annahmen sichtbar machen; geänderte Annahmen bei Neuschätzung explizit protokollieren.

Welche Faktoren beeinflussen die Schätzqualität in IT-Projekten, und welche sind im Health-IT-Kontext besonders ausgeprägt?
?
**Produktfaktoren:** Funktionale/nicht-funktionale Anforderungen, Anwendungsart, Qualität/Stabilität, **Zertifizierbarkeit**, Sicherheit, Dokumentationsumfang. **Prozessfaktoren:** gewähltes Prozessmodell (klassisch vs. agil). **Projektfaktoren:** Organisationsrahmen, Soft-/Hardwareumgebung, Werkzeuge, Stabilität. **Personenfaktoren:** Personalausstattung, Qualifikation, Unternehmenskultur, Führungsstil. **Typische Schätzfehlerquellen:** unterschiedliche Mitarbeitererfahrung; wechselnde Technologiestacks von Projekt zu Projekt; Teamgröße; Motivation; verteilte Teams. **Health-IT spezifisch:** Regulatorische Anforderungen (MDR, DSGVO, AMNOG) erhöhen den Dokumentations- und Validierungsaufwand erheblich – werden in frühen Schätzungen oft unterschätzt. Zertifizierbarkeit ist als Einflussfaktor in regulierten Umgebungen dominant.

Vergleichen Sie Delphi-Methode und Planning Poker entlang von Anonymität, Aufwand und Zielgruppe.
?
| Merkmal | Delphi-Methode | Planning Poker |
|---|---|---|
| **Anonymität** | vollständig (Standard) / eingeschränkt (Breitband) | nein; verdeckt erst aufgedeckt |
| **Aufwand** | hoch (mehrere Runden, schriftlich) | gering (integriert in Sprint Workflow) |
| **Iterationen** | mehrfach bis Annäherung | 2–3 Runden bis Konsens |
| **Zielgruppe** | große, kritische Projekte | agile Teams, Sprint-Planung |
| **Basis** | externe Experten, getrennt | Entwicklungsteam, gemeinsam |
| **Ergebnis** | Durchschnittswert der letzten Runde | Konsens des Teams |
Gemeinsamkeit: Beide reduzieren **Verzerrungseffekte** (Anchoring, Konformitätsdruck) durch Trennung der Erstschätzungen. Planning Poker ist eine **Light-Variante** von Breitband-Delphi für agile Kontexte.

Function Point vs. CoCoMo – welches Verfahren passt wann, und was sind die kritischen Grenzen jedes Ansatzes?
?
| | Function Point | CoCoMo |
|---|---|---|
| **Basis** | Funktionalität (Inputs, Outputs, Dateien, Abfragen, Schnittstellen) | LOC / KDSI |
| **Sprachabhängigkeit** | **unabhängig** | abhängig (LOC-Schätzung vorher nötig) |
| **Frühest einsetzbar** | ja, wenn Anforderungen klar | erst nach LOC-Schätzung |
| **Kritische Grenze** | Tabellenwerte extern, Komplexitätsbewertung subjektiv | LOC schwer schätzbar bei modernen Frameworks; CoCoMo passt schlecht zu High-Level-Sprachen |
| **Vorteil** | kundennahe, nachvollziehbar | explizite Formeln, reproduzierbar |
Fazit: Function Point für **frühe Phase**, wenn Anforderungen in Funktionen formulierbar; CoCoMo für **große Embedded-Projekte** mit gut schätzbarer Codegröße. Beide sind **algorithmisch** und setzen belastbare Eingangsdaten voraus – ohne diese liefern sie falsche Präzision.

Wann ist Pricing-to-win betriebswirtschaftlich gerechtfertigt – und welche Risiken entstehen für Auftragnehmer und Auftraggeber?
?
**Pricing-to-win:** Aufwand wird durch das Budget des Auftraggebers bestimmt, nicht durch die Projektfunktionalität; nur so viel Aufwand, dass noch Gewinn gemacht wird. **Betriebswirtschaftlich gerechtfertigt bei:** strategischen Projekten (Erstprojekt beim attraktiven Kunden, Verdrängungswettbewerb, Kostenbeitragsituationen); Ziel: Markt gewinnen und später Margen holen. **Risiken für den Auftragnehmer:** (1) Dauerhafter Verlust bei schlechter Kalkulation. (2) Qualitätseinsparungen, die zu Nacharbeitskosten führen. (3) Scope-Creep ohne Zusatzvergütung. **Risiken für den Auftraggeber:** (1) Qualitätsmangel, wenn Auftragnehmer schneidet. (2) Abhängigkeit, wenn Auftragnehmer nach Einstiegsphase Konditionen anhebt. (3) Projektverzögerung durch Unterbesetzung. **Max-Budget** ist die „harte Variante": Aufwand = verfügbares Budget, unabhängig vom Realaufwand.

Warum schlagen Best Practices mehrere Schätzverfahren vor – und was tut man, wenn zwei Verfahren zu sehr unterschiedlichen Ergebnissen führen?
?
**Begründung für Methodenkombination:** Jedes Verfahren hat eigene Schwächen (Delphi: subjektiv; Analogie: nur bei Vorprojekten; FP: Tabellen extern; CoCoMo: LOC-Abhängigkeit; Prozentsatz: Fehlermultiplikation). Unterschiedliche Verfahren beleuchten unterschiedliche Aspekte → Kreuzvalidierung erhöht Konfidenz. Mehrere Schätzer reduzieren individuelle Verzerrungen. **Bei stark abweichenden Ergebnissen:** (1) Annahmen beider Schätzungen explizit vergleichen – oft liegt die Abweichung in unterschiedlichen Scope-Definitionen. (2) Einflussfaktoren (Produkt/Prozess/Projekt/Person) gezielt hinterfragen. (3) Breitband-Delphi nutzen, um die Ausreißer zu diskutieren. (4) Drei-Punkt-Methode: Abweichung als tO und tP verwenden → gewichtetes Mittel. Grundsatz: Starke Abweichung ist kein Fehler, sondern ein Signal für **hohe Unsicherheit** → in den Projektplan einfließen lassen.

---

## Mögliche Anschlussfragen des Prüfers

- Wie hoch sind Risiko- und Gewinnzuschlag im Kostenplan, und warum genau diese Größe?
- Wann ist Bottom-up-Schätzung unmöglich – und was tut man in diesem Fall?
- Welche Rolle spielt die Cost Data Base bei Analogie- und Prozentsatzmethode?
- Wie verhält sich die Aufwandsschätzung zum Earned Value Management (Soll-Ist-Vergleich)?
- Wie ändert sich die Schätzstrategie von Wasserfall zu Scrum?
- Intermediate CoCoMo: Welche Kategorien von Kostentreibern gibt es? *(im PDF nicht aufgeführt)*
- Wie wirkt sich eine Unterschätzung um 30 % auf Risikozuschlag, Gewinn und Projekterfolg aus?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
