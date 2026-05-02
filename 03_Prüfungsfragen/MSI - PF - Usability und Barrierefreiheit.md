---
fach: msi
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - fach/allgemein/msi
  - typ/pruefungsfrage
  - status/offen
  - flashcards
---

# MSI - PF - Usability und Barrierefreiheit

## Kontext

Kompaktkarte zu Barrierefreiheit im eHealth-Kontext. Basis: §4 BGG (gesetzliche Definition), WCAG 2.1 (vier Prinzipien) und deren Relevanz für CDA-Stylesheets und ELGA-Anwendungen.

## Verlinkte Konzepte

- [[MSI - Barrierefreiheit - Definition und Normen]]
- [[MSI - Barrierefreiheit - WCAG Prinzipien]]

---

## Karten

### Definition

Wie definiert §4 BGG Barrierefreiheit? Für wen gilt eine gesetzliche Verpflichtung in Österreich?

?

**Definition (§4 BGG):** Barrierefrei sind technische Gebrauchsgegenstände, Systeme der Informationsverarbeitung, akustische und visuelle Informationsquellen und Kommunikationseinrichtungen, wenn sie für behinderte Menschen in der allgemein üblichen Weise, **ohne besondere Erschwernis und grundsätzlich ohne fremde Hilfe** zugänglich und nutzbar sind.

**Verpflichtete Akteure** (Folie 62):
- Behörden (e-gov ab 2008)
- Zusteller laut Zustellgesetz
- Verwaltung des Bundes (BGStG)
- Unternehmen, die Güter der Öffentlichkeit anbieten
- Bundesförderungsnehmer (BGStG)

Technische Umsetzungsnorm: **WCAG 2.1** (`https://www.w3.org/TR/WCAG21/`).

---

Welche vier Prinzipien hat WCAG 2.1? Nennen Sie zu jedem Prinzip eine Kernforderung.

?

1. **Wahrnehmbar** – Informationen müssen für alle Benutzer erfassbar sein (Multimodalität, Textalternativen, Kontrast, semantische Auszeichnung).
2. **Bedienbar** – Steuerelemente und Navigation müssen ohne Maus/geräteunabhängig bedienbar sein (Sprunglinks, klare Tab-Reihenfolge, Skalierung).
3. **Verständlich** – Text und Bedienung müssen nachvollziehbar sein (einfache Sprache, keine Popups/bewegte Elemente, einfache Suche, kein horizontales Scrollen).
4. **Robust** – Inhalt muss von assistierenden Technologien (Screenreader) zuverlässig interpretiert werden können (valider Code, eindeutige IDs, Name/Rolle/Wert für alle Elemente).

Merkhilfe: **W–B–V–R** (Wahrnehmbar, Bedienbar, Verständlich, Robust).

---

### Anwendung

Welche WCAG-Prinzipien sind für die Anzeige eines CDA-Befunds im ELGA-Referenzstylesheet besonders kritisch? Begründen Sie.

?

**Wahrnehmbar:** Der Befund muss für sehbehinderte Nutzer (Screenreader) zugänglich sein → semantische Auszeichnung von Tabellen, Überschriften; Textalternativen für Grafiken.

**Verständlich:** Medizinische Inhalte sind fachsprachlich komplex → Abkürzungen erklären, klarer Seitenaufbau, kein horizontales Scrollen. Einfache Sprache für Patientenansicht.

**Robust:** Das Stylesheet erzeugt HTML aus XML → valider, sauberer Code ist Voraussetzung, damit Screenreader und andere Clients den Befund zuverlässig parsen.

**Bedienbar:** Sprunglinks zu langen Befund-Sections; keine zeitbegrenzten Interaktionen.

---

### Diskussion / Vergleich

Was ist der Unterschied zwischen Barrierefreiheit und Usability? Warum kann ein System usable, aber nicht barrierefrei sein?

?

**Usability** = Benutzerfreundlichkeit für die Hauptzielgruppe (typischer Nutzer, keine Behinderung).

**Barrierefreiheit** = Zugänglichkeit für *alle*, einschließlich Menschen mit Behinderung oder chronischer Krankheit.

**Warum trennbar:** Ein System kann intuitiv für 70 % der Bevölkerung bedienbar sein, aber keine Textalternativen für Screenreader haben → barrierefrei ist es nicht. Barrierefreiheit umfasst Usability als Teilmenge, geht aber darüber hinaus.

Bevölkerungsrelevanz: ca. 30 % der österreichischen Bevölkerung sind von Behinderung und/oder chronischer Krankheit betroffen (Folie 59, Quelle: Peter Heumader, JKU, 2016) – eine zu große Gruppe, um sie zu ignorieren.

---

## Mögliche Anschlussfragen des Prüfers

- Welche assistierende Technologie ist für das Prinzip „Bedienbar" besonders relevant? (Screenreader)
- Was versteht WCAG unter „Robust"? Welche Code-Anforderungen ergeben sich?
- Wie hängt das ELGA-Referenzstylesheet mit Barrierefreiheit zusammen?
- Welche Bevölkerungsgruppen profitieren über Menschen mit Behinderung hinaus von Barrierefreiheit? (Ältere, situativ Eingeschränkte, Zeitdruck, kleine Bildschirme)

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
