---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Einführung in Standards und Interoperabilität]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Daten - Strukturiert vs Unstrukturiert

> [!info] Kurzdefinition
> Strukturierte Daten haben einheitliche Datenstruktur, einheitliche Datentypen und ein kontrolliertes Vokabular für die Bedeutung. Unstrukturierte Daten liegen in nicht-formalisierter Struktur vor; Computerprogramme können ihre Einzelinformationen nicht auswerten.

## Beschreibung

**Strukturierte Daten** (Folie 14):
- Besitzen eine einheitliche **Datenstruktur** und **Datentypen**.
- Die **Bedeutung** der Information ist beschrieben durch ein **kontrolliertes Vokabular** = „Codesystem".
- Sind Informationen, die von Computersystemen **eindeutig und unter Bewahrung der Bedeutung** weiterverarbeitet werden können.
- Werden sie zwischen Systemen ausgetauscht: **interoperable Daten**. Bleibt die ursprüngliche Bedeutung erhalten: **semantische Interoperabilität**.

**Unstrukturierte Daten** (Folie 15):
- Informationen, die in **nicht-formalisierter Struktur** vorliegen.
- Computerprogramme können die Einzelinformationen nicht auswerten.
- Beispiele: Freitext, gescannte Bilder, Tonaufzeichnungen natürlicher Sprache, Excel-Tabellen ohne klare Gliederung.
- Wichtige Warnung der Vorlesung: „Nicht alles, was für das Auge strukturiert erscheint, ist auch für Computersysteme strukturiert nutzbar!"

## Bestandteile / Aufbau

Strukturierte Daten = Datenstruktur + Datentypen + kontrolliertes Vokabular. Fehlt eines der drei Elemente, sind die Daten zwar evtl. strukturiert für das Auge, aber nicht für die Maschine vollständig nutzbar.

## Beispiel

Strukturierter Pulswert in CDA (Folie 14):
```
<code code="8867-4" displayName="Heart Beat" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC">
<value xsi:type="PQ" value="59" unit="/min"/>
```
Unstrukturierter Gegenpol (Folie 15): Freitext-Befund „Patient klagt über Herzrasen", gescanntes Befundbild, Audio-Diktat.

## Abgrenzung

- **Strukturiert ≠ tabellarisch**. Eine Excel-Tabelle ohne Gliederung gilt laut Folie 15 als unstrukturiert.
- **Strukturiert ≠ semantisch interoperabel**. Erst mit kontrolliertem Vokabular für die Bedeutung wird aus „strukturiert" auch „bedeutungs­erhaltend".

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Eigenschaften muss ein Datenelement laut Vorlesung haben, damit es als „strukturiert" gilt?

**Anwendungsfrage:** Klassifizieren Sie: PDF-Befund, HL7-v2-Nachricht, gescannter EKG-Streifen, FHIR-Observation, Excel-Liste mit gemischten Zellinhalten.

**Diskussionsfrage:** Warum ist „für das Auge strukturiert" nicht ausreichend? Welche typischen Praxis-Fallen entstehen daraus?

**Mögliche Anschlussfragen:**
- Was ist ein Codesystem konkret? → [[MSI - Terminologie - Codesystem]] (im PDF nur erwähnt, nicht definiert in dieser Vorlesung)
- Wie unterscheiden sich „interoperable Daten" und „semantisch interoperable Daten"?
- Welche Datentypen sind im klinischen Bereich besonders relevant?

## Verwandt

- [[MSI - Daten - Datentypen]]
- [[MSI - Daten - Metadaten]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilität - Definition]]

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 14, 15
