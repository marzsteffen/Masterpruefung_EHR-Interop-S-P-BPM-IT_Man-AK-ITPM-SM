---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Semantik Theorie]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologie - Anforderungen

> [!info] Kurzdefinition
> Liste aus der Vorlesung mit den Anforderungen an Ordnungssysteme/Terminologien: vollständig, disjunkt, klar systematisch, beliebige Sprachvarianten/Synonyme, Kompositions-Grammatik, maschineninter­pretierbar, übertragbar ohne Bedeutungsverlust.

## Beschreibung

Folie 11 listet die Anforderungen an Ordnungssysteme:

- **Vollständig**
  - Alle Begriffe der Konzeptdomäne müssen enthalten sein.
  - z. B. ICD-10 muss alle Krankheitsbilder abdecken.
- **Disjunktheit**
  - Eindeutige Konzepte.
  - Keine Überschneidung, keine Redundanzen.
  - Achtung bei Synonymen und Homonymen.
  - Diskussionsfrage in der Folie: „Warum ist ein Konzept ‚Sonstiges' so problematisch?" – verweist auf Cimino's „Rejection of Not Elsewhere Classified".
- **Klare Systematik des Ordnungssystems**
  - Konsistent, widerspruchsfrei.
  - Anerkannt und transparent.
- **Beliebige Sprachvarianten und Synonyme.**
- **Kompositions-Grammatik → „Sprache"** (Bezug zur Postkoordination).
- **Maschineninterpretierbar, übertragbar ohne Bedeutungsverlust.**

(Folie 12 trägt die Überschrift „Anforderungen an Ordnungssysteme 2/2", war aber im gelieferten PDF-Auszug nicht in der ersten Häfte sichtbar – die obige Liste stammt vollständig aus Folie 11. Falls Folie 12 zusätzliche Anforderungen enthält, die später noch sichtbar werden, sollte diese Note ergänzt werden.)

## Bestandteile / Aufbau

| Anforderung | Bedeutung |
|---|---|
| Vollständigkeit | Konzeptdomäne abdeckend |
| Disjunktheit | Keine Überschneidungen, keine Redundanz |
| Klare Systematik | Konsistent, widerspruchsfrei, anerkannt |
| Sprachvarianten/Synonyme | Mehrere Bezeichnungen pro Konzept zulassen |
| Kompositions-Grammatik | Fähigkeit zur Postkoordination |
| Maschineninterpretierbarkeit | Codes übertragbar ohne Bedeutungsverlust |

## Beispiel

Das „Sonstiges"-Beispiel der Folie verweist auf das Problem nicht-disjunkter Ordnungssysteme: Wenn ein Pendant zur „Sonstiges"-Kategorie existiert, ist die Klassifikation zwar formal vollständig, aber unbrauchbar zur eindeutigen Codierung – dieselben Befunde landen mit unterschiedlicher Wahrscheinlichkeit in „Sonstiges", abhängig vom Codierer.

## Abgrenzung

- Diese Liste überlappt **stark** mit Cimino's Desiderata, ist aber nicht identisch: die Vorlesungs-Anforderungen sind kompakter und gehen direkt auf die Praxis-Sicht der Codierung ein. Cimino formuliert die Anforderungen detaillierter und benennt explizit „Concept Permanence", „Polyhierarchy", „Formal Definition" etc.
- **Anforderungen ≠ Konformität.** Eine reale Terminologie erfüllt die Anforderungen typischerweise nur teilweise; Disjunktheit und Vollständigkeit sind in der Praxis oft Spannungs­felder.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche sechs Anforderungen an ein Ordnungssystem nennt die Vorlesung?

**Anwendungsfrage:** Bewerten Sie ICD-10 anhand dieser Anforderungen – welche werden gut erfüllt, welche schwächer?

**Diskussionsfrage:** Warum ist ein Konzept „Sonstiges" so problematisch? (Antwort: bricht Disjunktheit und macht Aggregation/Vergleich unzuverlässig; Cimino verlangt explizit dessen Vermeidung.)

**Mögliche Anschlussfragen:**
- Wie verhält sich „Kompositions-Grammatik" zur Postkoordination in SNOMED CT? → [[MSI - Terminologie - Präkoordination vs Postkoordination]]
- Welche Cimino-Desiderata adressieren dieselben Punkte mit anderen Worten?
- Wann ist Vollständigkeit unrealistisch?

## Verwandt

- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Vokabular und kontrolliertes Vokabular]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 11 (Folie 12 „Anforderungen 2/2" war im PDF-Auszug noch nicht sichtbar – ggf. Ergänzung notwendig)
