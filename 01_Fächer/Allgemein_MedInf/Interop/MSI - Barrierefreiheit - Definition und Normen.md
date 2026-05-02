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

# MSI - Barrierefreiheit - Definition und Normen

> [!info] Kurzdefinition
> Barrierefreiheit ist die Eigenschaft technischer Gebrauchsgegenstände, Informationssysteme, akustischer/visueller Informationsquellen und Kommunikationseinrichtungen, ohne besondere Erschwernis und grundsätzlich ohne fremde Hilfe zugänglich und nutzbar zu sein (§4 BGG). Maßgebliche technische Norm: **WCAG 2.1**. Verpflichtungen für Behörden, Bundesverwaltung, kommerzielle Anbieter öffentlicher Güter und Bundesförderungs­nehmer.

## Beschreibung

Folie 60 (Definition):

> „Barrierefrei sind […] technische Gebrauchsgegenstände, Systeme der Informationsverarbeitung, akustische und visuelle Informationsquellen und Kommunikationseinrichtungen […], wenn sie für behinderte Menschen in der allgemein üblichen Weise, ohne besondere Erschwernis und grundsätzlich ohne fremde Hilfe zugänglich und nutzbar sind." *(§4 BGG)*

Folie 59 zur Bevölkerungs­statistik (ca. 8 Mio. Österreich, Quelle laut Folie: Peter Heumader, JKU, 9.6.2016):
- 70,2 % ohne Behinderung bzw. chronische Krankheit.
- 6,7 % von Behinderung betroffen.
- 10,8 % von chronischer Krankheit betroffen.
- 12,3 % sowohl von Behinderung als auch chronischer Krankheit betroffen.

Insgesamt also rund 30 % der Bevölkerung mit Behinderung und/oder chronischer Krankheit.

Folie 61 vergleicht Buch vs. IT-Anwendung:
- **Inhalt**: Blinde Menschen können den Inhalt nicht erfassen.
- **Steuerung**: Körperlich behinderte Menschen können evtl. die Seiten nicht umblättern.
- **Darstellung**: Kognitiv beeinträchtigte Personen können den Text nicht verstehen.
- → IT kann das **besser**, FALLS man die Barrierefreiheit mitbedenkt.

Folie 62 (Normen und Vorschriften):
- **Web Content Accessibility Guidelines (WCAG) 2.1** – `https://www.w3.org/TR/WCAG21/`.
- Verpflichtung zur barrierefreien Website:
  - Behörden (e-gov ab 2008).
  - Zusteller laut e-gov (Zustellgesetz).
  - Verwaltung des Bundes (BGStG / e-gov).
  - Unternehmen, die Güter verkaufen, „die der Öffentlichkeit zur Verfügung stehen".
  - Förderungsnehmer von Bundesförderungen (BGStG).

Folie 68 (IT-Systeme für alle): adressiert sind 30 % behinderte und/oder chronisch Kranke (sehbehindert, motorisch behindert, gehörlos/hörbehindert, kognitive Behinderungen / Lerneinschränkung), ältere Menschen, Menschen in besonderen Situationen (fachfremd, kleine Bildschirme, Arbeit unter Zeitdruck). Mittel: **Audits**. Ressource: `https://www.gesundheit.gv.at/ueber-uns/barrierefreiheit`.

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Gesetzliche Definition | §4 BGG |
| Technische Norm | WCAG 2.1 |
| Pflichtige Akteure | Behörden, Bundesverwaltung, kommerzielle Verkäufer öffentlicher Güter, Bundesförderungs­nehmer |
| Zielgruppe | ~30 % der Bevölkerung mit Behinderung/chronischer Krankheit + ältere Menschen + situativ Eingeschränkte |
| Werkzeug | Audits |

## Beispiel

Im PDF nicht in Form einer Fallstudie ausgeführt. Die Folien 28 + 29 referenzieren das ELGA-Referenzstylesheet und CDA2PDF als Maßnahmen, die Barrierefreiheit unterstützen.

## Abgrenzung

- **Barrierefreiheit ≠ Usability**: Usability ist Benutzer­freundlichkeit für die Hauptzielgruppe; Barrierefreiheit fordert Zugang für alle. Barrierefreiheit umfasst Usability als Teilmenge.
- **WCAG ≠ EN 301 549**: WCAG fokussiert Web-Inhalte; EN 301 549 ist die EU-Norm für IKT-Beschaffung (im PDF nicht erwähnt).
- **§4 BGG (Bundes-Behindertengleichstellungsgesetz)** ≠ **BGStG (Bundes-Behindertengleichstellungs­gesetz / Anwendungsgesetz)**: BGG definiert Barrierefreiheit, BGStG regelt Verpflichtungen.

## Prüfungsrelevanz

**Mittel** (im Vergleich zu CDA-Kerninhalten geringer, aber im Diskursfeld eHealth wichtig).

**Typische Definitionsfrage:** Wie definiert §4 BGG Barrierefreiheit?

**Anwendungsfrage:** Welche Akteure sind in Österreich gesetzlich zur barrierefreien Website verpflichtet?

**Diskussionsfrage:** Welche Verbindung gibt es zwischen Barrierefreiheit und Usability eines CDA-Stylesheets?

**Mögliche Anschlussfragen:**
- Welche vier Prinzipien hat WCAG 2.1? → [[MSI - Barrierefreiheit - WCAG Prinzipien]]
- Welcher Anteil der Bevölkerung ist von Behinderung/chronischer Krankheit betroffen?
- Welche Hilfen bietet `https://www.gesundheit.gv.at/ueber-uns/barrierefreiheit`?

## Verwandt

- [[MSI - Barrierefreiheit - WCAG Prinzipien]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]] (Stylesheet als Mittel zur barrierefreien Anzeige)
- [[MSI - HL7 CDA - Eigenschaften]] (Lesbarkeit / human readability)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 59, 60, 61, 62, 68 (Quelle Statistik: Peter Heumader, JKU, 9.6.2016)
