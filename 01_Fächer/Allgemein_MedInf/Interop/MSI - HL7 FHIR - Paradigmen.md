---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR Starter (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - Paradigmen

> [!info] Kurzdefinition
> Im Gesundheitswesen existieren vier Paradigmen für den Datenaustausch: nachrichtenbasiert (HL7 v2), dokumentenbasiert (CDA), anwendungsspezifisch (DICOM, CCD) und ressourcenbasiert (FHIR). Jedes Paradigma adressiert andere Use Cases mit unterschiedlichen Stärken und Schwächen.

## Beschreibung

### Paradigma 1: Nachrichtenbasiert
- **Prinzip**: Events werden übertragen (z. B. Aufnahme, Entlassung, Laborbefund)
- **Beispiel**: HL7 v2

### Paradigma 2: Dokumentenbasiert
- **Prinzip**: Arztbrief, Befund – ein Dokument als abgeschlossene Informationseinheit
- **Beispiele**: HL7 v3, HL7 CDA

### Paradigma 3: Anwendungsspezifisch
- **Prinzip**: Auf bestimmte klinische Domänen ausgerichtet
- **Beispiele**: DICOM (Radiologie), HL7 CCD, My Health Record, Patient Summary

### Paradigma 4: Ressourcenbasiert
- **Prinzip**: Atomare Ressourcen (Patient, Medikation, Vitaldaten, …) werden einzeln verwaltet und kombiniert
- **Beispiel**: HL7 FHIR

## Bestandteile / Aufbau

| Paradigma | Ansatz | Beispiel-Standard |
|---|---|---|
| Nachrichtenbasiert | Events/Trigger | HL7 v2 |
| Dokumentenbasiert | Vollständiges Dokument | HL7 CDA |
| Anwendungsspezifisch | Domänen-Fokus | DICOM, CCD |
| Ressourcenbasiert | Atomare Einheiten | HL7 FHIR |

**Vorteile ressourcenbasierter Ansatz:**
- Informationen in Einzelteilen → granulare Abfragen möglich
- Ressourcen unabhängig voneinander änderbar
- Leichtgewichtige Übertragung

**Nachteile ressourcenbasierter Ansatz:**
- Keine Gesamtübersicht (nur via FHIR Documents/Bundles lösbar)
- Keine nativen Prozessmodelle
- Mehrere Übertragungen für mehrere Ressourcen notwendig

## Abgrenzung

- HL7 FHIR ist **nicht nur** ressourcenbasiert – es unterstützt auch Nachrichten, Dokumente und Prozessmanagement. Das ressourcenbasierte Paradigma ist jedoch der Kernansatz.
- CDA (dokumentenbasiert) enthält den narrativen Text als Primärquelle; FHIR-Ressourcen haben den narrativen Text als Ergänzung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Paradigmen gibt es im Gesundheitswesen und welchen Ansatz verfolgt FHIR?

**Anwendungsfrage:** Für welches Szenario würde man CDA vs. FHIR wählen? (Dokument-Paradigma vs. ressourcenbasiert – z. B. bei strukturierten Befunden CDA sinnvoll, bei API-Interoperabilität FHIR)

**Diskussionsfrage:** FHIR ist „mehr als Ressourcen" – es unterstützt auch Nachrichten und Dokumente. Wann ist das klassische Dokumenten-Paradigma (CDA) dem FHIR-Ressourcen-Ansatz vorzuziehen?

**Mögliche Anschlussfragen:**
- Wie überwindet FHIR den Nachteil „keine Gesamtübersicht"? (→ Bundle/Document)
- Was ist der Unterschied zwischen HL7 v2 (Nachrichten) und HL7 FHIR (Ressourcen) auf konzeptioneller Ebene?
- Warum waren ältere Standards ungeeignet für Mobilgeräte?

## Verwandt

- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 CDA - Definition]]
- [[MSI - Datenaustausch - Formen]]
- [[MSI - Interoperabilität - Definition]]
- [[MSI - HL7 - International Patient Summary]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 3–5, 9–10
