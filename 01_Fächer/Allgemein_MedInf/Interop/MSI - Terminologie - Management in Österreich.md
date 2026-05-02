---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Terminologien Anwendung]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologie - Management in Österreich

> [!info] Kurzdefinition
> Lebenszyklus-Aufgaben rund um Terminologien in einem nationalen eHealth-System: Suche, Auswahl, Value-Set-Erstellung, Übersetzen, Mappen, neue Codes einbringen, Wartung, Verteilung, Lizenz-Management, Zusammenspiel mit Anzeige und Validierung.

## Beschreibung

Folie 17 listet die Terminologie-Management-Aufgaben in Österreich:

- **Suche nach geeigneten Terminologien und Abstimmung mit Fachexperten/Arbeitsgruppen.**
  - LOINC, SNOMED, HL7 … oder eine eigene Terminologie?
  - Terminologische Analyse auf Synonyme, Homonyme … (siehe [[MSI - Begriff - Synonyme Homonyme Eponyme]]).
- **Value Set Erstellung.**
  - Subsets erstellen, Festlegung von Anzeigetexten.
- **Übersetzen und Mappen.**
- **Einbringen neuer Codes** (z. B. LOINC, SNOMED).
- **Wartung von Terminologien.**
- **Verteilung von Terminologien.**
- **Lizenz-Management.**
- **Zusammenspiel mit Anzeige von Befunden** (Stylesheet) **und Validierung** (Schematron, Online-Validator).

## Bestandteile / Aufbau

Lebenszyklus eines Value Sets/einer Terminologie im nationalen Kontext:

1. **Erhebung des Bedarfs** (Fachexperten/Arbeitsgruppen).
2. **Auswahl der Quell-Terminologie** (SNOMED CT, LOINC, lokal entwickelt).
3. **Terminologische Analyse** (Synonyme, Homonyme).
4. **Value Set Definition** (Subset + Anzeigetexte).
5. **Übersetzung & Mapping** (z. B. EN → DE, lokal → international).
6. **Code-Einbringung** (Antrag bei Quell-Pflegestelle, falls neuer Code nötig).
7. **Wartung und Versionierung.**
8. **Verteilung an Anwender** (Terminologieserver, z. B. termgit.elga.gv.at).
9. **Lizenz-Management** (z. B. SNOMED CT national, LOINC frei nach Registrierung).
10. **Validierung-Integration** (Schematron-Regeln, Online-Validator) und Anzeige (Stylesheet → menschen­lesbare Befundansicht).

## Beispiel

Im PDF nicht in einer einzelnen Fallstudie ausgeführt. Implizit: ELGA verwaltet hunderte Value Sets über termgit.elga.gv.at; ELGA-Schematron-Validatoren prüfen automatisch die Code-Konformität gegen die referenzierten Value Sets.

## Abgrenzung

- **Terminologie-Management ≠ Code-Erstellung.** Management umfasst auch Auswahl, Pflege, Lizenzen – nicht nur das Schreiben neuer Codes.
- **Nationales Management ≠ International**: National wird gemappt/profiliert, international wird die Quell-Terminologie gepflegt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Aufgaben fallen unter Terminologie-Management in Österreich?

**Anwendungsfrage:** Beschreiben Sie den Lebenszyklus eines neuen Value Sets von der Bedarfs­erhebung bis zur produktiven Validierung.

**Diskussionsfrage:** Warum ist Lizenz-Management ein eigenständiger Punkt? Welche Lizenz-Modelle gibt es bei SNOMED CT, LOINC, ICD-10?

**Mögliche Anschlussfragen:**
- Wer betreibt termgit.elga.gv.at?
- Wie funktioniert ein Schematron-Validator gegen Value Sets?
- Welche Rolle hat das Stylesheet im Zusammenspiel mit Codes?

## Verwandt

- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Mapping]]
- [[MSI - Terminologie - Mapping in CDA]]
- [[MSI - Terminologie - Funktionen]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 17
