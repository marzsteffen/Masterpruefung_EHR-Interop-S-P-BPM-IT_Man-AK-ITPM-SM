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

# MSI - HL7 CDA - Implementierungsleitfäden

> [!info] Kurzdefinition
> CDA-Implementierungs­leitfäden sind vollständige Beschreibungen mit allen Informationen zur Implementierung. Sie beschreiben das **Maximalset** an gültigen Strukturen, Vorgaben für Header und Body inklusive Value Sets, narrative und entry-strukturierte Inhalte. Bausteinartig aufgebaut über wiederverwendbare Templates, modelliert in ART-DECOR.

## Beschreibung

Wörtlich aus Folie 37:

> „CDA Implementierungsleitfäden sind vollständige Beschreibungen, sie enthalten alle Informationen zur Implementierung.
> – Zielgruppen: ‚Implementierer', SW-Entwickler, Domänenexperten
> – Bausteinartiger Aufbau (wiederverwendbare ‚Templates') → Modellierung in Art-Decor
> – Immer mit Codebeispielen, tabellarischer Aufbau
> – Beispieldateien (Vollständig und Minimal)
>
> Was beschreiben die ELGA CDA-Implementierungsleitfäden?
> – **Maximalset**: Nur beschriebene Strukturen sind gültig
> – Vorgaben für die Dokument-Metadaten (‚Header'), z. B. Dokumentkennung
> – Art der Metadaten, zu verwendende Codes (‚Value Sets')
> – Aussehen und inhaltliche Struktur (‚Narrativer Text')
>   – Abschnitte des Dokuments (verpflichtende und optionale Abschnitte)
>   – Reihenfolge der Abschnitte
>   – Tabellen, wenn notwendig
> – Elektronische Struktur für die Weiterverarbeitung medizinischer Daten (‚Entry Level')
>   – Technische Angaben für Codes (wie z. B. ICD-10 Diagnosen erkannt und ausgelesen werden können)"

## Bestandteile / Aufbau

| Bestandteil | Inhalt |
|---|---|
| **Maximalset** | Welche Strukturen überhaupt zulässig sind |
| **Header-Vorgaben** | Welche Metadaten Pflicht/Optional sind, mit Datentypen + Value Sets |
| **Section-Struktur** | Welche Abschnitte vorhanden sind, in welcher Reihenfolge |
| **Entry-Level** | Wie codierte Einzelelemente aufgebaut sind |
| **Templates** | Wiederverwendbare Bausteine ([[MSI - HL7 CDA - Templates]]) |
| **Codebeispiele** | Vollständige + minimale Beispiel­dokumente |

In ART-DECOR werden diese Bausteine modelliert; daraus wird das Schematron generiert, das den ELGA Online-Validator antreibt.

## Beispiel

Aus der ELGA-LV: „ELGA Allgemeiner Implementierungsleitfaden 2020" gilt als Basis-Leitfaden; daneben gibt es spezielle Leitfäden für Entlassungsbrief Ärztlich, Entlassungsbrief Pflege, Laborbefund, Befund Bildgebende Diagnostik, eMedikation Rezept/Abgabe/Medikationsliste/Pharmazeutische Empfehlung, Pflegesituationsbericht.

Der Allgemeine Leitfaden wird im PDF mehrfach referenziert, z. B. für Datentypen (Folie 17), Adress-Elemente (Folie 16 in VL „Terminologien Anwendung").

## Abgrenzung

- **Implementierungs­leitfaden ≠ CDA-Standard**: Der Standard (ISO/HL7 27932:2009) ist allgemein; der Leitfaden profiliert ihn für ELGA.
- **Allgemeiner Leitfaden ≠ Spezieller Leitfaden**: Allgemeiner gilt für alle ELGA-Dokumente; spezielle Leitfäden ergänzen für je einen Dokumenttyp.
- **Maximalset ≠ Nur-das-was-da-steht**: Strukturen, die nicht im Leitfaden beschrieben sind, sind *nicht* gültig – auch wenn sie das CDA-Schema erlauben würde.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Was beschreibt ein CDA-Implementierungs­leitfaden? Welche Bestandteile hat er?

**Anwendungsfrage:** Sie wollen einen ELGA-konformen Laborbefund implementieren. Welche Leitfäden müssen Sie konsultieren?

**Diskussionsfrage:** Warum ist „Maximalset" eine zentrale Aussage? Welche Konsequenzen hat sie für Implementierer?

**Mögliche Anschlussfragen:**
- Was sind ELGA-Templates? → [[MSI - HL7 CDA - Templates]]
- Wie wird ein Leitfaden technisch nutzbar gemacht? → [[MSI - HL7 CDA - ART-DECOR]]
- Wie verhalten sich allgemeine und spezielle Leitfäden zueinander?

## Verwandt

- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - ART-DECOR]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]]
- [[MSI - HL7 CDA - Kardinalität und Konformität]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 37
