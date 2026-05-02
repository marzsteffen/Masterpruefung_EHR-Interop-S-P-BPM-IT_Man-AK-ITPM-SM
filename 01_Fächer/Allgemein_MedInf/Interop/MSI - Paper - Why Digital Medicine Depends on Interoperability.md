---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/01 Einführung/WhyDigitalMedicineDependsOnInteroperability.pdf
datum_vorlesung: 2019-08-20
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - Paper - Why Digital Medicine Depends on Interoperability

## Überblick

Perspective-Artikel von Lehne, Sass, Essenwanger, Schepers und Thun (npj Digital Medicine, 2019, Vol. 2 Article 79; Open Access, Berlin Institute of Health, Charité, HRW Krefeld). Argumentiert, dass Interoperabilität Voraussetzung für die digitale Transformation der Medizin ist – ohne sie sind KI/Big Data, mobile Apps und Big Analytics nicht in vollem Umfang nutzbar. Pflichtlektüre laut Folie 26 der Einführungs-Vorlesung.

## Lernziele (laut Paper)

- Vier Ebenen der Interoperabilität (technical, syntactic, semantic, organizational) auseinanderhalten und definieren können.
- Vier Anwendungsbereiche identifizieren können, in denen Interoperabilität besonders nützlich ist: AI & Big Data, medizinische Kommunikation, Forschung, internationale Kooperation.
- Konkrete Standards/Terminologien benennen, die jede Ebene und jeden Anwendungsbereich unterstützen.
- Argumentieren können, warum „more data is not enough" – ohne Standards führt Datenfülle nicht automatisch zu Erkenntnis.

## Behandelte Konzepte

### Interoperabilitäts-Ebenen (Vier-Ebenen-Sicht)
- [[MSI - Interoperabilitätsebenen - Vier-Ebenen-Modell Lehne]]
- [[MSI - Interoperabilitätsebenen - Syntaktisch]]

### Anwendungsbereiche
- [[MSI - Interoperabilität - Anwendungsbereiche Lehne]]

### Standards/Spezifikationen
- [[MSI - openEHR - Archetypes]]
- [[MSI - HL7 - International Patient Summary]]

## Roter Faden

Einleitung: Die Digitalisierung verspricht Fortschritte, aber heutige Daten liegen in Silos und proprietären Systemen → KI, Big Data, mobile Apps können ihr Potenzial nicht ausschöpfen. → Definition Interoperabilität (IEEE-Definition als Anker) → Vier-Ebenen-Sicht (technical / syntactic / semantic / organizational) → Vier Anwendungsbereiche (Fig. 1: AI&Big Data, Medical Communication, Research, International Cooperation) jeweils mit detaillierter Argumentation → Schluss: ohne Interoperabilität keine echte digitale Medizin; mit ihr „digital lingua franca" für globalen Datenaustausch.

## Zentrale Aussagen / Take-aways

- **Definition (IEEE 610, Ref. 17)**: „the ability of two or more systems or components to exchange information and to use the information that has been exchanged."
- **Vier Ebenen** (statt der drei der Hauptvorlesung): Technical, Syntactic, Semantic, Organizational.
- **„Big data" oft eher „a large number of disconnected small data"** – ohne Interoperabilität bleibt das Potenzial ungenutzt.
- **Risiko unstrukturierter Daten für KI**: Algorithmen auf unstrukturierten/non-standardisierten Daten können systematische Bias-Fehler einführen, die wegen Datenmenge schwer detektierbar sind.
- **EHRs sind oft „disconnected, proprietary solutions buried in systems that do not talk to each other"** – internationale Standards und Terminologien helfen, das aufzubrechen (z. B. IPS).
- **Interoperabilität reduziert Dokumentationsaufwand** – Patienten-Empowerment, weniger redundante Eingaben, mehr Zeit am Patienten.
- **Cross-Border-Beispiele**: 2019 erste Austausche von International Patient Summary und ePrescription zwischen EU-Ländern.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - Einführung in Standards und Interoperabilität]] (das Paper ergänzt das Drei-Schichten-Modell um die syntaktische Ebene)
- [[MSI - VL - Semantik Theorie]] (Detail Terminologien)
- [[MSI - VL - HL7 FHIR und Terminologieserver]] (FHIR + ~140 Resources)
- [[EHR - MOC]] (IPS, EHR-Disconnected-Problem)

## Erwähnte Terminologien/Standards (als Kurzeinordnung)

| Bezeichnung | Funktion laut Paper |
|---|---|
| HL7, IHE | Standards Development Organizations für IT-Standards und deren Use im Gesundheitswesen |
| HL7 FHIR | Modernes API-orientiertes Austauschformat, ca. 140 Healthcare-Concepts |
| openEHR | Reference-Model + Archetypes; AQL für Querying |
| SNOMED CT | Allzweck-Sprache mit >340.000 medizinischen Konzepten |
| LOINC | Laborbefunde |
| IDMP | Identification of Medicinal Products |
| HGNC | HUGO Gene Nomenclature Committee – Gene |
| HPO | Human Phenotype Ontology – phänotypische Abnormalitäten |
| IPS | International Patient Summary (HL7 + CEN) |
| Orphanet | Rare-disease-Nomenklatur |

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/01 Einführung/WhyDigitalMedicineDependsOnInteroperability.pdf`
- Zitierung: Lehne M, Sass J, Essenwanger A, Schepers J, Thun S. *Why digital medicine depends on interoperability*. npj Digital Medicine (2019) 2:79. DOI: 10.1038/s41746-019-0158-1. Open Access (CC BY 4.0).
- Affiliation: Berlin Institute of Health (BIH), Charité Berlin, HRW Krefeld.
