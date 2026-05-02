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

# MSI - HL7 CDA - nullFlavor

> [!info] Kurzdefinition
> Das Attribut `@nullFlavor` in CDA kennzeichnet, dass ein Element nicht entsprechungs­gemäß befüllt werden kann. Fünf gängige nullFlavors: **NI** (No Information), **UNK** (Unknown), **MSK** (Masked – vertraulich), **NA** (Not applicable), **OTH** (Other – nur in alternativem Codesystem verfügbar). Ist ein nullFlavor gesetzt, dürfen keine anderen Attribute mit Wert gleichzeitig stehen.

## Beschreibung

Folie 24 listet die fünf nullFlavors:

| nullFlavor | displayName | Deutsche Übersetzung | Anwendung |
|---|---|---|---|
| **NI** | NoInformation | keine Information vorhanden | wenn es keine Informationen gibt |
| **UNK** | Unknown | unbekannt | wenn es Informationen gibt, diese aber unbekannt sind |
| **MSK** | Masked | maskiert | wenn es Informationen gibt, diese aber nicht bekannt gegeben werden (vertraulich, nicht freigegeben) |
| **NA** | Not applicable | nicht anwendbar | wenn keine Codierung verfügbar ist |
| **OTH** | Other | Andere | wenn eine Codierung nur in einem alternativen Codesystem verfügbar ist |

Folie 25 zur **Verwendung im (ELGA-) CDA**:

> „Wenn in einem Element ein nullFlavor angegeben wurde, kann nicht gleichzeitig ein anderes Attribut eingetragen werden.
>
> Die konkrete Anwendung des @nullFlavor Attributs ist im Rahmen der ELGA Implementierungsleitfäden nur erlaubt, wenn er explizit in der Spezifikation eines Elementes angegeben ist.
>
> Für codierte Elemente ist ein nullFlavor für unbekannte und fehlende Information nach Möglichkeit zu vermeiden, bevorzugt ist die Verwendung eines Codes mit demselben Informationsgehalt (etwa für ‚keine Allergie bekannt' das SNOMED Konzept 716186003 ‚No known allergy')."

## Bestandteile / Aufbau

Beispiele aus Folie 25:

```xml
<!-- ID der schreibenden Person, mit nullFlavor UNK -->
<id nullFlavor="UNK"/>

<!-- Zeitintervall mit beidseitig unbekannter Grenze -->
<effectiveTime xsi:type="IVL_TS">
  <low nullFlavor="UNK"/>
  <high nullFlavor="UNK"/>
</effectiveTime>
```

Aus Konformitäts-Tabelle (Folie 25):
> Element/Attribut: `id`, DT II, Kard 1..1, Konf R
> Beschreibung: „Identifikationselement zur Aufnahme der Aufenthaltszahl. Zugelassene nullFlavor: NI … Patient hat keine Aufenthaltszahl. UNK … Patient hat eine Aufenthaltszahl, diese ist jedoch unbekannt."

Damit ist die Granularität sichtbar: NI vs. UNK ist eine *informationelle* Unterscheidung, nicht nur „leeres Feld".

## Abgrenzung

- **NI vs. UNK**: NI = es gibt überhaupt keine Information; UNK = es gibt eine Information, sie ist nur nicht bekannt.
- **MSK vs. NI**: MSK = es gibt Information, sie ist aber bewusst nicht freigegeben (Privacy-Schutz); NI = keine Information vorhanden.
- **OTH vs. Translation**: OTH wird oft *gemeinsam* mit `<translation>` verwendet, um einen Code aus einem alternativen System anzugeben (siehe [[MSI - HL7 CDA - Translation]]).
- **NA**: technisch nicht anwendbar (z. B. „Schwangerschafts­woche bei Mann"), nicht „leer".

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche fünf nullFlavors gibt es in CDA und wann werden sie verwendet?

**Anwendungsfrage:** Welcher nullFlavor passt zu (a) „Patient hat keine Allergien", (b) „Patient hat Allergien, diese sind unbekannt", (c) „Patient verweigert die Auskunft", (d) „Schwangerschafts­woche bei einem männlichen Patienten"?

**Diskussionsfrage:** Warum verlangt der ELGA-Leitfaden, dass nullFlavor *vermieden* werden soll, wenn es einen Code mit gleicher Bedeutung gibt? (Antwort: Codes erlauben semantische Auswertung, nullFlavor markiert nur Abwesenheit.)

**Mögliche Anschlussfragen:**
- Welche Beziehung gibt es zwischen nullFlavor OTH und Translation? → [[MSI - HL7 CDA - Translation]]
- Warum darf bei nullFlavor kein anderer Wert gleichzeitig im Element stehen?
- Welche nullFlavors sind in einem konkreten Element zugelassen?

## Verwandt

- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - Translation]]
- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - HL7 - IPS Allergie-Codierung]] (No-Info-Codes vs. nullFlavor)
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 24, 25
