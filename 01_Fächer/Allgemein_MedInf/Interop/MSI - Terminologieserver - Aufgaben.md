---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR und Terminologieserver]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologieserver - Aufgaben

> [!info] Kurzdefinition
> Vier Hauptaufgaben (Folie 7): Anzeige/Auflistung/Suche, Export in standardisierten Formaten, Wartung (Import/Update), Publikation. Zusätzlich Zusatzfeatures: intensionale Value-Set-Definition und Mapping.

## Beschreibung

Wörtlich aus Folie 7:

> „Anzeige, Auflistung und Suche von Terminologie-Inhalten
> – Echtzeitressource ja/nein
>
> Export von Terminologien in standardisierten Formaten und Services, Schnittstellen zur Integration in lokale Systeme
>
> Terminologiewartung: Import und Update von Terminologien
> – Standardisierte Formate und Services
>
> Publikation von Terminologien
> – Mechanismen zur Verteilung und Benachrichtigung
> – Automatisierbarer Zugriff
>
> Zusatzfeatures:
> – intensionale Value Set Definition
> – Mapping"

## Bestandteile / Aufbau

| Aufgabe | Funktion |
|---|---|
| **Anzeige/Auflistung/Suche** | Suche von Terminologie-Inhalten, optional in Echtzeit |
| **Export** | Bereitstellung in standardisierten Formaten und Services für lokale Systeme |
| **Wartung** | Import/Update von Terminologien aus Quellen |
| **Publikation** | Verteilung + Benachrichtigung über Updates, automatisierbarer Zugriff |
| **Intensionale Value-Set-Definition** | Regeln statt Aufzählung (z. B. „alle Konzepte unterhalb X") |
| **Mapping** | ConceptMaps zwischen Codesystemen |

## Beispiel

Termgit ELGA (Folie 33 von VL „Terminologien Anwendung" zeigt das in Aktion): Suche im Frontend, Download als CSV/XML/HTML, Webservice-Zugriff für Primärsysteme.

Bei FHIR-Terminologie­servern (Ontoserver, tx.fhir.org) erfolgt der Zugriff über `$expand`, `$lookup`, `$validate-code`, `$translate` (siehe [[MSI - HL7 FHIR - Terminology Service]]).

## Abgrenzung

- **Anzeige/Suche ≠ Validierung**: Anzeige liefert Codes; Validierung (`$validate-code`) prüft, ob ein Code in einem ValueSet enthalten ist.
- **Wartung ≠ kollaborative Erstellung**: Wartung importiert/aktualisiert; ART-DECOR ist eher kollaborative Erstellung von Leitfäden + Templates.
- **Mapping (Zusatzfeature) ≠ Mapping als Hauptzweck**: ein reiner Terminologieserver muss kein ConceptMap-Repository sein; größere Plattformen integrieren beides.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Welche Aufgaben hat ein Terminologieserver?

**Anwendungsfrage:** Welche Aufgabe wird durch die FHIR-Operation `$expand` adressiert? (Anzeige/Auflistung der Konzepte eines ValueSets.)

**Diskussionsfrage:** Warum sind Mechanismen zur Verteilung und Benachrichtigung wichtig?

**Mögliche Anschlussfragen:**
- Was ist eine intensionale Value-Set-Definition? → [[MSI - HL7 FHIR - ValueSet Resource]]
- Welche Standards adressieren welche Aufgabe? → [[MSI - Terminologieserver - Austauschstandards]]
- Wer ist Provider, wer Consumer? → [[MSI - Terminologieserver - Architektur]]

## Verwandt

- [[MSI - Terminologieserver - Definition]]
- [[MSI - Terminologieserver - Architektur]]
- [[MSI - Terminologieserver - Austauschstandards]]
- [[MSI - HL7 FHIR - Terminology Service]]
- [[MSI - Terminologie - Management in Österreich]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 7
