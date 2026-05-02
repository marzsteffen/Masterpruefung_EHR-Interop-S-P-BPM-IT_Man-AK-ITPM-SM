---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Aufwandsschätzung - Grundlagen

> [!info] Kurzdefinition
> Die Aufwandsschätzung berechnet im Vorfeld durch Analyse wesentlicher Faktoren die voraussichtlichen Kosten und die Zeit eines Projekts oder Arbeitspakets. Sie liefert Schätzwerte für Termine, Aufwand und Budget und ist Erfolgsgrundlage für Projekte.

## Beschreibung

**Definition (Folie 8):**
Die Aufwandsschätzung berechnet im Vorfeld die voraussichtlichen **Kosten** und die **Zeit** eines Projekts oder Arbeitspakets durch Analyse wesentlicher Faktoren. Sie versucht – unter Zugrundelegung existierender Projektunterlagen – möglichst genaue Angaben zum benötigten Aufwand zu machen, um den Projektablauf zu planen oder ein Angebot zu erstellen.

**Warum wichtig (Folien 10–12):**

- Erfolg oder Misserfolg eines Projekts ist maßgeblich von der **Qualität der Aufwandsschätzung** abhängig.
- Grundlage für die Erstellung eines tragfähigen **Business Cases**.
- Erstellt Grundlagen für: Termin-/Meilensteinplanung, Ressourcen, Entscheidung über Alternativen, Verträge.
- **Daher: Schätzung eines Projekts so früh wie möglich!**

**Spezifika in Software-Projekten (Folie 12):**

- **Personalaufwände sind meist die teuersten Aufwände.**
- Im Vordergrund: Schätzung des **Personalaufwands in der Entwicklung**, weniger Schulung/Wartung.
- Oft wird direkt die reine Entwicklung geschätzt; Projektmanagement, Testen etc. durch **Aufschlag** berücksichtigt (z. B. PM ca. **15 %**).
- In der Kalkulation oft nur **Personalaufwände** als direkte Kosten.

## Bestandteile / Aufbau

### Probleme beim Schätzen (Folien 15–17)

- IT-Projekte oft einzigartig → Wiederholbarkeit fragwürdig.
- Schätzungen schon **früh** notwendig (Vertrag, Pflichtenheft) → unsichere Informationen.
- Schätzungen sind von Natur aus **ungenau**; **wiederholtes Schätzen** an Phasenübergängen erforderlich.
- **Zielkonflikt** des Schätzverfahrens: Prognosegenauigkeit vs. rasche Durchführbarkeit vs. geringer Bearbeitungsaufwand.
- **Erwartungshaltung** des Auftraggebers (terminliche Vorstellungen, Forderungen) – Eisberg-Modell.
- **Überprüfbarkeit** wird oft nicht durchgeführt; schlechtes PM kann Schätzung ad absurdum führen.
- **Einflussfaktoren** vielfältig (Komplexität, Methoden, Werkzeuge, Definitionen wie „Was ist ein Personenmonat?").

### Gründe für unrealistische Schätzung (Folie 14)

- Unterschiedliche Erfahrung der Mitarbeiter
- Wechselnde Prozesse, Tools, Sprachen, Plattformen, Frameworks von Projekt zu Projekt
- Größe der Projektteams
- Motivation der Teammitglieder
- Verteilung der Teams über mehrere Standorte/Kontinente

### Einflussfaktoren in der Literatur (Folie 22)

- **Produkt:** Funktionale/nicht-funktionale Anforderungen, Art der Anwendung, Qualität und Stabilität, Zertifizierbarkeit, Sicherheit, Dokumentationsumfang.
- **Prozess:** gewähltes Prozessmodell.
- **Projekt:** Organisatorische Rahmenbedingungen, Soft-/Hardwareumgebung, Werkzeuge, Stabilität.
- **Personen:** Personalausstattung, Qualifikation, Unternehmenskultur, Führungsstil, künftige Nutzer.

### Anforderungen an Schätzverfahren (Folien 20–21)

- **Ergebnisqualität:** Genauigkeit, Objektivität, Nachvollziehbarkeit, Bewertbarkeit, Anpassbarkeit, Übertragbarkeit.
- **Effizienz:** schnelle Verfügbarkeit, leichte Erlernbarkeit, adäquater Zeitaufwand, IT-Unterstützung.
- **Unterstützung des Projektmanagements:** frühzeitige Abschätzung, Strukturierung, Wiederholbarkeit, Sensitivitätsanalyse.

### Kosten von Schätzverfahren (Folie 23)

- **1–3 % der Projektkosten** für eine gute Schätzung.
- Schätzkosten Teil der Angebotskosten.
- Typische Verteilung Angebotskosten:
  - 30–50 % Angebotsvorbereitung
  - 20–30 % Schätzung
  - 30–40 % Ausformulierung des Angebots

### Ablauf einer Schätzung (Folien 24–25)

```
Projektumfang & Meilensteine festlegen → PSP erstellen →
Größenschätzung → Aufwandsschätzung → Kostenschätzung →
Aktivitätenzeitplan → Kostenplanung → Planung abstimmen & freigeben
```

- Schätzung ist gleichbedeutend mit dem **Umgang mit Unsicherheiten**; Risikomanagement ist wesentlicher Bestandteil.
- **Idealfall:** ausgearbeitetes Pflichtenheft als Grundlage.
- **Eine Schätzung ist nicht mit Verhandeln zu verwechseln.** Eine Schätzung kann nur reduziert werden, wenn Leistungsumfang oder Qualität reduziert wird.

### Best Practices (Folien 50–52)

- Mehrere Schätzverfahren, mehrere Schätzer.
- **Workshops** mit Team und Kunden.
- **Erfahrene Spezialisten** in Analyse und Schätzungen einbeziehen.
- **Schätzung in Punkten oder Arbeitsstunden, nicht in Kalendertagen.**
- Faktor für Unvorhersehbares einplanen.
- Schätzung **dokumentieren** und Kalkulation nachvollziehbar machen.
- Auszug aus Jones (2007): „Be accurate. Be conservative. Base the estimate on solid historical data. Include quality. Be prepared to defend the assumptions of your estimate."

## Beispiel

*Im PDF nicht durch konkretes Praxisbeispiel illustriert.*

## Abgrenzung

- **Schätzung** ≠ **Verhandlung** (Folie 25).
- **Aufwandsschätzung** ≠ **Größenschätzung** ≠ **Kostenschätzung** – Größe ist die Voraussetzung für Aufwand, Aufwand für Kosten (siehe Detail-Note [[ITPM - Aufwandsschätzung - Schätzverfahren Übersicht]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Aufwandsschätzung, und welche Rolle spielt sie für den Projekterfolg?

**Anwendungsfrage:** Sie sollen für ein KIS-Migrationsprojekt eine erste Aufwandsschätzung erstellen – welche Schritte gehen Sie konkret durch?

**Diskussionsfrage:** „Schätzung ist nicht Verhandeln" – wie reagieren Sie, wenn ein Auftraggeber den Aufwand auf die Hälfte drücken möchte?

**Mögliche Anschlussfragen:**
- Welche Best Practices nennen Sie?
- Wie verteilen sich die Angebotskosten?
- Welche Einflussfaktoren spielen eine besondere Rolle in Health-IT?

## Verwandt

- [[ITPM - Cone of Uncertainty]]
- [[ITPM - Aufwandsschätzung - Schätzverfahren Übersicht]]
- [[ITPM - Aufwandsschätzung - Top-down vs Bottom-up]]
- [[ITPM - Aufwandsschätzung - Drei-Punkt]]
- [[ITPM - Projektstrukturplan]]
- [[ITPM - Pflichtenheft]]
- [[ITPM - Kostenplan]]

## Quelle

- Vorlesung: [[ITPM - VL - Aufwandsschätzung Kosten Personal Controlling]]
- Folien/Seitenangabe: 8–25, 50–52
