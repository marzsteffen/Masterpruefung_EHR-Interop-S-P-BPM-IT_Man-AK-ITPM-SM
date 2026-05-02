---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - Paper - Why Digital Medicine Depends on Interoperability]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Interoperabilität - Anwendungsbereiche Lehne

> [!info] Kurzdefinition
> Lehne et al. (2019) identifizieren vier Anwendungsbereiche, in denen interoperable Daten und IT-Systeme besonders wertvoll sind: (1) AI & Big Data, (2) Medical Communication, (3) Research, (4) International Cooperation. Diese vier Bereiche bilden Fig. 1 des Papers.

## Beschreibung

Das Paper begründet seine zentrale These an vier Bereichen:

**1. AI and Big Data**
- Provide algorithms with clear data structure and semantics.
- Ensure validity of analysis results.
- Create trust in digital technologies.
- Argument: KI-Algorithmen brauchen strukturierte, eindeutig semantische Eingaben. Auf unstrukturierten/non-standardisierten Daten entstehen systematische Bias-Fehler, die wegen Datenmenge schwer detektierbar sind und am Ende das Vertrauen untergraben. Die größte Hürde sei „not a lack of algorithms but a lack of suitable data".

**2. Medical Communication**
- Enable easy information retrieval.
- Avoid medical errors caused by communication barriers.
- Reduce documentation burden.
- Empower patients.
- Argument: EHRs sind oft „disconnected, proprietary solutions". Interoperable EHRs reduzieren Dokumentationsaufwand (weniger doppelte Eingaben, einfachere Information Retrieval), erlauben Patienten aktivere Rolle im eigenen Behandlungsprozess.

**3. Research**
- Improve the use of real-world data (z. B. large-scale observational studies).
- Create new research hypotheses (with data mining and AI).
- Enable remote development of analysis scripts.
- Argument: Real-world data, in interoperablen Formaten, erlaubt regional/national/global skalierbare Studien, das Verbinden von Primär- und Sekundärnutzung sowie Federated-Analysen, bei denen die Analyse zum Datensatz wandert (statt umgekehrt) – relevant bei Datenschutz-Restriktionen.

**4. International Cooperation**
- Pool data across organizations (z. B. seltene Krankheiten, Precision Medicine).
- Tackle global public health issues (z. B. Infektionskontrolle, Epidemien).
- Provide global access to new technologies.
- Argument: Bei seltenen Krankheiten reichen Patientenzahlen einer Institution nicht. Netzwerke wie UDN (USA) oder ERN (EU) plus Standards/Terminologien (Orphanet, HPO) ermöglichen institutionsübergreifende Zusammenarbeit. Pandemie-Beispiel: 1918 Spanish-flu-Erinnerung als Argument für interoperable Surveillance.

## Bestandteile / Aufbau

Fig. 1 des Papers fasst die Bereiche als 2×2-Layout: AI&Big Data – Medical Communication / Research – International Cooperation.

## Beispiel

Konkrete Beispiele aus dem Paper:
- AI-Risiko: Diabetes-Algorithmus auf unstrukturierten Daten könnte Patienten mit Diabetes-Familienanamnese fälschlich als Diabetiker selektieren.
- Medical Communication: Ein Patient wird re-hospitalisiert, relevante Information aus früheren Visiten in anderen Häusern fehlt – in Deutschland teilweise sogar zwischen Abteilungen desselben Hauses (Datenschutz).
- Research: federated analysis – Analyse-Skript wandert zum Datenort.
- International: 2019 erster Austausch von ePrescription und digital patient summary zwischen EU-Ländern.

## Abgrenzung

- Diese vier Bereiche sind laut Paper **nicht mutual exclusive** – ein Use Case kann mehreren Bereichen gleichzeitig zugehören (z. B. internationale Forschung zu seltenen Krankheiten = Research + International Cooperation).
- Das Paper hat eine **deutsche/europäische Perspektive**, hält die Argumente aber für allgemein übertragbar.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Anwendungsbereiche identifiziert Lehne et al. 2019?

**Anwendungsfrage:** Ordnen Sie folgende Szenarien zu: (a) Krebsregister-Auswertung, (b) Tumor Board zwischen drei Häusern, (c) Diabetes-Risiko-Modell aus EHR-Daten, (d) ePrescription Österreich–Italien.

**Diskussionsfrage:** Welcher Bereich profitiert am stärksten von interoperablen Daten – und welcher leidet am meisten unter ihrem Fehlen?

**Mögliche Anschlussfragen:**
- Warum ist „more data" allein nicht hilfreich für KI?
- Welche Standards/Terminologien sind in welchem Bereich besonders wichtig?
- Welche Rolle spielt federated analysis für Datenschutz?

## Verwandt

- [[MSI - Interoperabilitätsebenen - Vier-Ebenen-Modell Lehne]]
- [[MSI - HL7 - International Patient Summary]]
- [[MSI - Interoperabilität - Definition]]
- [[EHR - MOC]] (interoperable EHRs)
- [[ASP - MOC]] (Datenschutz vs. Datenaustausch)

## Quelle

- Vorlesung: [[MSI - Paper - Why Digital Medicine Depends on Interoperability]]
- Folien/Seitenangabe: Fig. 1 + Sektionen „How interoperability can improve medicine", S. 2–4 des Papers
