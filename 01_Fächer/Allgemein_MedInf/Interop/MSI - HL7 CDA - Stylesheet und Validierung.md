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

# MSI - HL7 CDA - Stylesheet und Validierung

> [!info] Kurzdefinition
> Praxis-Werkzeuge rund um CDA-Dokumente: das **ELGA_Referenzstylesheet** (XSLT zur HTML-Anzeige), der **ELGA-CDA2PDF-Konverter** (Druck), das **ELGA CDA Schema** (Strukturprüfung) und das **ELGA CDA Schematron** (inhaltliche Constraints + Value Sets), generiert per **ART-DECOR** und nutzbar via **ELGA Online-Validator**.

## Beschreibung

**Anzeige (Folie 28)**: ELGA_Referenzstylesheet
- XSLT zur Darstellung als HTML.
- Rege Weiterentwicklung: regelmäßig über Updates verbessert.
- Verhalten kann über Parameter umfangreich gesteuert werden.
- Base-64-Decoder für die Darstellung von Anhängen (PDF, Grafiken, Multimedia) ist eingebunden.

**Druck (Folie 29)**: ELGA-CDA2PDF Konverter
- Konverter zur Erzeugung eines PDF.
- Der Ausdruck des HTML über den Browser ist NICHT empfohlen.
- Druckansicht kann komprimiert werden.

**Konformitätsprüfung (Folie 31)**:
- Semantische Interoperabilität erfordert exakte Einhaltung der „Constraints" aus den Leitfäden („Leitfadenkonformität").
- Constraints können als **Schematron-Regeln** formuliert werden.
- Implementierung in Schematron (ISO/IEC 19757-3:2006).
- Mit Schematron werden Struktur und Inhalt von XML-Dokumenten validiert.
- Schematron ergänzt die grundsätzliche Schema-Prüfung; Textmeldungen für Fehler und Warnungen können ausgegeben werden.
- Schematron-Prüfung dient als **Unterstützung für Programmierer** und als **Absicherung beim Auslesen**.

**ELGA CDA Schema und Schematron (Folie 32)**:

| Komponente | Funktion |
|---|---|
| **ELGA CDA Schema** | verbessertes originales XML-Schema von HL7. Dient zur groben CDA-Strukturprüfung („Ist ein CDA Dokument"). Prüft Struktur, Datentypen, Elemente. Funktioniert für den Einsatz zur Generierung von Klassen (z. B. in C++). Enthält ELGA-Erweiterungen. |
| **ELGA CDA Schematron** | zur strukturellen und inhaltlichen Prüfung („Ist ein *ELGA* CDA Dokument"). Enthält und prüft Value Sets. Automatisierte Erstellung mit **ART-DECOR**. Download als Set, lokale Anwendung in eigenem Tool oder z. B. in oXygen oder XMLSpy. Grundlage für den ELGA Online-Validator. |

Links auf Folie 32: `http://www.art-decor.org/`, `http://elga.art-decor.org/`, ELGA Online-Validator: `https://ovp.elga-services.at/validation.html`.

## Bestandteile / Aufbau

| Werkzeug | Zweck |
|---|---|
| ELGA_Referenzstylesheet (XSLT) | Anzeige als HTML im Browser |
| ELGA-CDA2PDF | Druck-PDF-Erzeugung |
| ELGA CDA Schema (XSD) | grobe Strukturprüfung |
| ELGA CDA Schematron | inhaltliche Constraints + Value Sets |
| ART-DECOR | automatische Schematron-Generierung aus dem Modell |
| ELGA Online-Validator | Web-Tool zur Validierung |

## Beispiel

Hands-on-Beispiel laut Folie 30: `Entlassungsbrief_BeispielA.xml` öffnen mit Notepad++ (XML-Sicht) und mit `ELGA_Stylesheet_v1.0.xsl` (HTML, empfohlen Chrome). Anwendungs­hinweis im Changelog beachten: `https://gitlab.com/elga-gmbh/CDA_Visualization`.

Hands-on Validierung (Folie 33): die originale Datei Entlassungsbrief_BeispielA prüfen, dann gezielt einen Schema-Fehler und einen Schematron-Fehler „produzieren". Auf Moodle gibt es ein Beispiel mit je einem Schema- und Schematronfehler (`...BeispielA_Fehler`).

## Abgrenzung

- **Schema vs. Schematron**: Schema prüft Struktur (XSD-Ebene); Schematron prüft Inhalts-Constraints, Value Sets, Templates. Beide ergänzen sich, ersetzen sich nicht.
- **Stylesheet ≠ Pflicht**: Das CDA-Dokument muss auch ohne mitgeliefertes Stylesheet lesbar sein (Cimino-Lesbarkeits-Eigenschaft) – das Referenzstylesheet ist Empfehlung, nicht Bedingung.
- **Schema-Fehler ≠ Schematron-Fehler**: Schema-Fehler bedeutet „ist gar kein CDA"; Schematron-Fehler bedeutet „ist CDA, aber nicht ELGA-konform".

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche Werkzeuge prüfen ein ELGA-CDA-Dokument? Was prüft das Schema, was das Schematron?

**Anwendungsfrage:** Sie bekommen eine Fehlermeldung „Code aus Value Set X nicht enthalten" – ist das ein Schema- oder Schematron-Fehler?

**Diskussionsfrage:** Wieso reicht das XML-Schema nicht aus, um ELGA-Konformität sicherzustellen?

**Mögliche Anschlussfragen:**
- Was ist ART-DECOR? → [[MSI - HL7 CDA - ART-DECOR]]
- Wo finde ich den ELGA Online-Validator?
- Wie hilft Schematron Programmierern beim Auslesen?

## Verwandt

- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - ART-DECOR]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - Eigenschaften]] (Lesbarkeit)
- [[MSI - Terminologie - Management in Österreich]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 28, 29, 30, 31, 32, 33
