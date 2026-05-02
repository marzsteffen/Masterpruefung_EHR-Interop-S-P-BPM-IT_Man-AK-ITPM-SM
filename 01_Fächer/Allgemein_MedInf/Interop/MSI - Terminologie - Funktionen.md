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

# MSI - Terminologie - Funktionen

> [!info] Kurzdefinition
> „Wozu Terminologien?": Klassifikation für Leistungserfassung/Statistik, Metadaten, semantisch eindeutige Dokumentation, semantische Annotation für Forschung, Bedeutungsrelationen für NLP, Übersetzungen, Verknüpfung von Informationen – insgesamt Mittel zur Herstellung semantischer Interoperabilität.

## Beschreibung

Folie 29 listet die Funktionen von Terminologien:

- **Klassifikation zur Leistungserfassung und Gesundheitsstatistik.**
- **Metadaten** (z. B. Verschlagwortung von Dokumenten).
- **Semantisch eindeutige Dokumentation klinischer Behandlungsdaten.**
- **Semantische Annotation von medizinischen Forschungsdaten.**
- **Bereitstellung von Bedeutungsrelationen für Systeme, die natürlichsprachige Informationen verarbeiten** (NLP-Anwendung).
- **Übersetzungen.**
- **Verknüpfung von Informationen.**
- **Insgesamt: Mittel zur Herstellung semantischer Interoperabilität.**

Die Folie endet mit der Konsequenzen-Liste „Ohne Standards für Terminologien…":
- Sind Gesundheitsdaten nicht vergleichbar.
- Datenaggregation ist schwer oder unmöglich.
- Medizinische IT-Systeme können Daten nicht austauschen.
- Sekundärer Gebrauch (Forschung, Leistungsstatistik, Qualitätsmanagement) nicht möglich.
- Verknüpfung mit Decision Support Systems nicht möglich.

## Bestandteile / Aufbau

Sieben primäre Funktionen + die Kern-Aussage (Mittel zur semantischen Interoperabilität) + fünf Negativ­konsequenzen ohne Standards.

## Beispiel

Aus den jeweiligen Funktionen abgeleitet:
- LKF (Österreich) als Klassifikation zur Leistungserfassung.
- APPC-Codes als Metadaten in CDA-`<serviceEvent>`.
- LOINC-Codes als semantisch eindeutige Dokumentation eines Laborwerts.
- ICD-10-Codes für statistisch verwertbare Diagnoselisten.

## Abgrenzung

- **Funktionen vs. Anforderungen** ([[MSI - Terminologie - Anforderungen]]): Funktionen sagen *wozu* eine Terminologie dient; Anforderungen sagen, *welche Eigenschaften* sie dafür braucht.
- **Funktionen ≠ Cimino-Desiderata.** Cimino schreibt Qualitäts­anforderungen vor; Funktionen sind Anwendungs­fälle.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wozu dienen Terminologien laut Vorlesung? Nennen Sie mindestens fünf Funktionen.

**Anwendungsfrage:** Welche Konsequenzen entstehen, wenn ein Krankenhaus keine standardisierten Terminologien verwendet?

**Diskussionsfrage:** Welcher Funktion käme die größte Bedeutung zu, wenn Sie einen einzigen Anwendungsfall priorisieren müssten – und warum?

**Mögliche Anschlussfragen:**
- Welche Terminologie ist primär für Leistungserfassung gemacht? (LKF, DRG.)
- Welche für klinische Dokumentation? (SNOMED CT.)
- Welche für Lab-Befunde? (LOINC.)
- Wie unterstützen Terminologien NLP konkret? (Bedeutungs­relationen + ID-Pool für Annotation.)

## Verwandt

- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Anforderungen]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Daten - Metadaten]]

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 29
