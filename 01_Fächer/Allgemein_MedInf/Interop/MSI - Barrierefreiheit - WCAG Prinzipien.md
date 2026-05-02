---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Barrierefreiheit - WCAG Prinzipien

> [!info] Kurzdefinition
> Vier Prinzipien der Barrierefreiheit (WCAG 2.1): **Wahrnehmbar**, **Bedienbar**, **Verständlich**, **Robust**. Ziel: IT-Systeme, die für *alle* da sind.

## Beschreibung

Folie 63 listet die vier Prinzipien:

1. **Wahrnehmbar** – Informationen und Steuerelemente der Benutzerschnittstelle müssen so darstellbar sein, dass sie alle Benutzer wahrnehmen können.
2. **Bedienbar** – Steuerelemente der Benutzerschnittstelle und Navigation müssen bedienbar sein.
3. **Verständlich** – Sowohl die Informationen als auch die Bedienung der Benutzerschnittstelle müssen verständlich sein.
4. **Robust** – Der Inhalt muss so robust sein, damit er von verschiedensten Benutzerklienten inkl. assistierender Technologien verlässlich interpretiert werden kann.

Ziel: **IT-Systeme, die für ALLE da sind.**

Folien 64–67 vertiefen die Prinzipien:

**Prinzip 1: Wahrnehmbar (Folie 64)**
- Inhalt muss für alle wahrnehmbar sein.
- **Multimodalität** der Inhalte, da rein auditiver oder rein visueller Inhalt nicht für alle wahrgenommen werden kann.
- Textalternativen bieten:
  - Ersatzinhalte, etwa Audiobeschreibung.
  - Gebärdensprache-Videos.
- Semantische Auszeichnung (z. B. bei Formularen, Tabellenzeilen/spalten).
- Kontrast, Farbe.

**Prinzip 2: Bedienbar (Folie 65)**
- Geräte-unabhängige Bedienung, etwa ohne Maus.
- Barrierefreie Navigation:
  - Auszeichnung der Navigationselemente.
  - Sprunglinks.
  - Klarer Seitenaufbau, logische Tab-Reihenfolge (etwa für Screenreader wichtig).
  - Links kennzeichnen.
- Skalierung.
- Wahrnehmbarkeit und Bedienbarkeit u. a. wichtig für Screenreader (Demo-Video laut Folie: „Screen Reader Demo for Digital Accessibility – YouTube").

**Prinzip 3: Verständlich (Folie 66)**
- Lesbarer und verständlicher Text:
  - Einfache Sprache (siehe `https://lebenshilfe.at/wp-content/uploads/Infoblatt_Einfache-Sprache-1.pdf`).
  - Auszeichnung von Sprache, z. B. bei mehrsprachigen Dokumenten.
  - Abkürzungen und Akronyme kennzeichnen und erklären.
  - Glossare für nicht gebräuchliche Begriffe.
- Allgemeine Usability-Richtlinien:
  - Das Menü am besten auf der linken Seite positionieren.
  - Eine Möglichkeit zur Vergrößerung des Textes anbieten (Link oder Schaltfläche).
  - Keine Pop-Up-Fenster verwenden.
  - Keine sich bewegenden Elemente verwenden.
  - Eine einfache Suche anbieten.
  - Dafür sorgen, dass kein horizontales Scrollen nötig ist.
  - Vertikales Scrollen vermeiden! (Alternativ: Sprunglinks anbieten.)

**Prinzip 4: Robust (Folie 67)**
- „Sauberer" Code für assistierende Technologien:
  - Auszeichnung von Sprache.
  - Valider Code, etwa XML, HTML.
  - Eindeutige IDs.
  - Alle Elemente besitzen Name, Rolle, Wert.

## Bestandteile / Aufbau

| Prinzip | Kern-Forderung | Schlüssel-Praktiken |
|---|---|---|
| Wahrnehmbar | für alle erfassbar | Multimodalität, Textalternativen, Kontrast, semantische Auszeichnung |
| Bedienbar | für alle steuerbar | geräte-unabhängige Bedienung, klare Navigation, Sprunglinks, Skalierung |
| Verständlich | für alle nachvollziehbar | einfache Sprache, kein bewegter Inhalt, einfache Suche, kein horizontales Scrollen |
| Robust | für assistierende Technologien parsbar | valider Code, eindeutige IDs, Name/Rolle/Wert |

## Beispiel

Im PDF nicht als zusammenhängendes Beispiel ausgeführt; einzelne Praktiken in den Prinzip-Folien. Implizit: Das ELGA-Referenzstylesheet (Folie 28) muss diese Prinzipien beachten – z. B. Sprunglinks, klar strukturierte Sections, Tabelle mit semantischer Auszeichnung in der Lab-Anzeige (Folie 28).

## Abgrenzung

- **WCAG-Prinzipien ≠ einzelne Erfolgskriterien**: Die Prinzipien gliedern WCAG; darunter liegen Richtlinien und konkrete Erfolgskriterien (Levels A, AA, AAA). Diese Detailhierarchie wird im Vorlesungs-PDF nicht ausgearbeitet.
- **„Robust" ≠ „Skalierbar"**: Robust meint Interpretierbarkeit durch verschiedene Clients, nicht Performance.
- **„Verständlich" ≠ „Schön"**: Verständlich ist klar/eindeutig, nicht ästhetisch.

## Prüfungsrelevanz

**Mittel.** Wenn Prüfungsfragen zu Barrierefreiheit gestellt werden, sind die vier Prinzipien typische Einstiegsfragen.

**Typische Definitionsfrage:** Welche vier Prinzipien hat WCAG 2.1?

**Anwendungsfrage:** Geben Sie pro Prinzip ein konkretes Beispiel für eine ELGA-Anwendung.

**Diskussionsfrage:** Welche Prinzipien sind für die Anzeige eines CDA-Befunds besonders kritisch? (Wahrnehmbar + Verständlich + Robust.)

**Mögliche Anschlussfragen:**
- Welche Praktiken adressiert „Wahrnehmbar"?
- Was ist der Unterschied zwischen „Bedienbar" und „Robust"?
- Wie hängen WCAG und §4 BGG zusammen? → [[MSI - Barrierefreiheit - Definition und Normen]]

## Verwandt

- [[MSI - Barrierefreiheit - Definition und Normen]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]] (Anzeige & Druck)
- [[MSI - HL7 CDA - Eigenschaften]] (Lesbarkeit)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 63, 64, 65, 66, 67
- Externe Originalquelle: WCAG 2.1, `https://www.w3.org/TR/WCAG21/`.
