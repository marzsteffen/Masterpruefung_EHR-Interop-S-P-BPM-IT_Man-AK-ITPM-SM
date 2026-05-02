---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - COBIT 2019 Termin 14]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - COBIT 2019 - Prinzipien Governance-System und Rahmenwerk

> [!info] Kurzdefinition
> COBIT 2019 unterscheidet zwei Sätze von Grundprinzipien: **Sechs Prinzipien für ein Governance-System** (was ein gutes IT-Governance-System einer Organisation auszeichnet) und **drei Prinzipien für ein Governance-Rahmenwerk** (welche Eigenschaften das COBIT-Framework selbst als Rahmenwerk haben muss). Beide Sätze sind das Fundament der COBIT-2019-Methodik.

> [!warning] Quellen-Hinweis
> **In den verarbeiteten Vorlesungs-PDFs nicht erklärt — nur als Aufgabe genannt.** Auf Folie 10 des PDFs „Termin 14 ITSM Leutgeb" stehen die Prinzipien als Übungsaufgabe („6 Prinzipien Governance-System ist?", „3 Prinzipien Governance-Rahmenwerk ist?") ohne weitere inhaltliche Auflösung. Diese Note ist als „Ergänzung außerhalb der Vorlesung" gekennzeichnet und folgt dem ISACA-COBIT-2019-Framework (Originalquelle: ISACA, *COBIT 2019 Framework: Introduction and Methodology*, 2018).

## Beschreibung

COBIT 2019 (Control Objectives for Information and Related Technologies) ist das ISACA-Rahmenwerk für IT-Governance und IT-Management. Im Zentrum der Methodik stehen zwei Prinzipien-Sätze:

- **Sechs Prinzipien für ein Governance-System** — sie beschreiben, welche Eigenschaften das *konkret in einem Unternehmen implementierte* Governance-System erfüllen sollte.
- **Drei Prinzipien für ein Governance-Rahmenwerk** — sie beschreiben, welche Eigenschaften ein *generisches Rahmenwerk* (wie COBIT selbst) haben sollte, damit Organisationen daraus ihr individuelles Governance-System ableiten können.

Beide Sätze sind eine Neuerung gegenüber COBIT 5 und entstanden durch Trennung der bisherigen „fünf Prinzipien" in zwei distinkte Ebenen (Implementierungsebene vs. Rahmenwerksebene).

## Bestandteile / Aufbau

### Sechs Prinzipien für ein Governance-System

| # | Prinzip (englisch / deutsch) | Kerngedanke |
|---|---|---|
| 1 | **Provide Stakeholder Value** / Mehrwert für Stakeholder schaffen | Jedes Unternehmen braucht ein Governance-System, das Stakeholder-Interessen in Aktion und Entscheidung übersetzt. |
| 2 | **Holistic Approach** / Ganzheitlicher Ansatz | Ein effektives Governance-System besteht aus mehreren zusammenwirkenden Komponenten (Prozesse, Organisationsstrukturen, Informationen, Menschen, Kultur, Services/Infrastruktur, Richtlinien). |
| 3 | **Dynamic Governance System** / Dynamisches Governance-System | Das Governance-System muss bei jeder Veränderung eines oder mehrerer Designfaktoren angepasst werden — es ist nicht statisch. |
| 4 | **Governance Distinct From Management** / Trennung von Governance und Management | Governance (Bewertung, Steuerung, Überwachung der Stakeholder-Anforderungen) ist klar von Management (Planung, Umsetzung, Betrieb) zu trennen. |
| 5 | **Tailored to Enterprise Needs** / Auf Unternehmensbedürfnisse zugeschnitten | Das Governance-System wird mithilfe der Designfaktoren an das jeweilige Unternehmen angepasst — keine Schablonenlösung. |
| 6 | **End-to-End Governance System** / Durchgängiges Governance-System | Das Governance-System adressiert das *gesamte* Unternehmen end-to-end, nicht nur die IT-Funktion. |

### Drei Prinzipien für ein Governance-Rahmenwerk

| # | Prinzip (englisch / deutsch) | Kerngedanke |
|---|---|---|
| 1 | **Based on Conceptual Model** / Auf konzeptionellem Modell basierend | Ein Rahmenwerk muss auf einem klaren konzeptionellen Modell aufbauen, das Schlüsselkomponenten und Beziehungen definiert (Konsistenz, Automatisierungsfähigkeit). |
| 2 | **Open and Flexible** / Offen und flexibel | Das Rahmenwerk soll offen für neue Inhalte sein und Anpassungen / Erweiterungen ohne Verlust der Kern-Konsistenz zulassen. |
| 3 | **Aligned to Major Standards** / An relevanten Standards ausgerichtet | Das Rahmenwerk sollte zu wichtigen einschlägigen Standards, Frameworks und Vorschriften ausgerichtet sein (z. B. ITIL, ISO/IEC 27001, NIST, ISO/IEC 38500). |

## Beispiel

**Anwendung der sechs Prinzipien (Governance-System) auf ein Krankenhaus:**

1. *Provide Stakeholder Value*: Pflegeleitung, Geschäftsführung und Patient:innen formulieren Erwartungen an die KIS-Verfügbarkeit und Datensicherheit — das Governance-System übersetzt diese in messbare Steuergrößen.
2. *Holistic Approach*: Berücksichtigung von Prozessen (Incident-Management), Strukturen (CIO + IT-Lenkungsausschuss), Kultur (Patientensicherheit zuerst), Technologie (KIS, Netzwerk).
3. *Dynamic Governance System*: Bei Einführung von Cloud-Services (neuer Designfaktor „Sourcing-Modell") wird das Governance-System angepasst.
4. *Governance Distinct From Management*: Aufsichtsrat und Geschäftsführung übernehmen Governance (Strategievorgaben), CIO und IT-Leitung führen das Management aus.
5. *Tailored to Enterprise Needs*: Das öffentliche Krankenhaus implementiert andere Governance-Schwerpunkte als ein privates Universitätsklinikum.
6. *End-to-End*: Governance gilt nicht nur für die IT, sondern auch für klinische Forschung, Verwaltung, Personal.

**Anwendung der drei Prinzipien (Governance-Rahmenwerk) auf COBIT selbst:**

1. *Conceptual Model*: COBIT basiert auf dem Modell der sieben Komponenten und der Zielkaskade.
2. *Open and Flexible*: Designfaktoren erlauben kundenspezifische Anpassung; Erweiterungen wie „COBIT Focus Areas" (z. B. „Information Security", „DevOps") sind möglich.
3. *Aligned to Major Standards*: COBIT ist mit ITIL, ISO/IEC 27001/27002, ISO/IEC 38500, NIST CSF, TOGAF u. a. abgeglichen.

## Abgrenzung

- **Sechs vs. drei Prinzipien**: Die *sechs* Prinzipien betreffen das *implementierte Governance-System einer Organisation*; die *drei* Prinzipien betreffen das *Rahmenwerk* (also Eigenschaften des Werkzeugs, mit dem man das System gestaltet). Beide Ebenen klar trennen!
- **Bezug zu Komponenten** (siehe [[SM - COBIT 2019 - Komponenten IT-Governance-System]]): Das zweite Prinzip „Holistic Approach" wird durch die sieben Komponenten konkretisiert.
- **Bezug zu Designfaktoren** (siehe [[SM - COBIT 2019 - Designfaktoren]]): Die Prinzipien 3 (Dynamic) und 5 (Tailored) werden durch die Designfaktoren operationalisiert.
- **Bezug zur Zielkaskade** (siehe [[SM - COBIT 2019 - Zielkaskade]]): Prinzip 1 „Provide Stakeholder Value" wird durch die Zielkaskade konkret umgesetzt.
- **Bezug zu Trennung Governance ↔ Management** (siehe [[SM - Governance - Definition]] / [[SM - Corporate Governance vs IT-Governance]]): Prinzip 4 ist die methodische Verankerung der Governance-vs.-Management-Trennung in COBIT.
- **Vergleich zu COBIT 5**: COBIT 5 hatte fünf Prinzipien („Meeting Stakeholder Needs", „Covering the Enterprise End-to-End", „Applying a Single Integrated Framework", „Enabling a Holistic Approach", „Separating Governance From Management"). COBIT 2019 hat diese in zwei Ebenen mit insgesamt 9 Prinzipien (6+3) verfeinert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche zwei Sätze von Prinzipien unterscheidet COBIT 2019? — Sechs Prinzipien für das Governance-System einer Organisation und drei Prinzipien für das Governance-Rahmenwerk selbst.

**Aufzähl-Frage (Foliensatz-Aufgabe):**
- 6 Prinzipien Governance-System: Stakeholder-Mehrwert, Ganzheitlicher Ansatz, Dynamisches System, Governance ≠ Management, Maßgeschneidert, End-to-End.
- 3 Prinzipien Governance-Rahmenwerk: Konzeptionelles Modell, Offen und flexibel, An Standards ausgerichtet.

**Diskussionsfrage:** Warum trennt COBIT 2019 die Prinzipien in zwei Ebenen? — Um die Anforderungen an das *konkret zu bauende System* von den Eigenschaften des *Werkzeugs zur Konstruktion* zu trennen. Zwei verschiedene Adressaten: Unternehmens-Architekten (Implementierung) vs. Framework-Designer (ISACA, Erweiterungs-Autoren).

**Mögliche Anschlussfragen:**
- Wie konkretisieren die sieben Komponenten das Prinzip „Holistic Approach"? — Sie listen die *Bausteine* eines ganzheitlichen Systems auf (Prozesse, Strukturen, Informationen, Menschen, Kultur, Services, Richtlinien).
- Wie konkretisieren die Designfaktoren das Prinzip „Tailored to Enterprise Needs"? — Über die 11 Designfaktoren wird das individuelle Profil der Organisation erfasst und das Governance-System angepasst.
- Was bedeutet „Governance Distinct From Management" praktisch? — Governance bewertet/steuert/überwacht (Aufgabe von Aufsichts- bzw. Lenkungsgremien), Management plant/baut/betreibt (Aufgabe der Geschäftsführung und Linienführung).
- Welche Standards sind in COBIT 2019 referenziert? — ITIL 4, ISO/IEC 27001, ISO/IEC 38500, NIST CSF, TOGAF, PMBOK, PRINCE2 u. a.
- Warum ist das Prinzip „End-to-End" wichtig? — Weil reine IT-Governance ohne Anbindung an Geschäfts-Governance ein Insellösungs-Risiko hat.

## Verwandt

- [[SM - VL - COBIT 2019 Termin 14]]
- [[SM - Standard - COBIT 2019 Framework]]
- [[SM - COBIT 2019 - Komponenten IT-Governance-System]]
- [[SM - COBIT 2019 - Designfaktoren]]
- [[SM - COBIT 2019 - Zielkaskade]]
- [[SM - COBIT 2019 - Gestaltungsprozess Governance-System]]
- [[SM - COBIT 2019 - Fähigkeitsstufen]]
- [[SM - Governance - Definition]]
- [[SM - Corporate Governance vs IT-Governance]]

## Quelle

- Vorlesung: [[SM - VL - COBIT 2019 Termin 14]] *(Folie 10 — als Übungsaufgabe ohne Auflösung)*
- Folien/Seitenangabe: PDF „Termin 14 ITSM Leutgeb", Folie 10
- Originalquelle: ISACA, *COBIT 2019 Framework: Introduction and Methodology* (2018), Schedule 2 „Principles".

## Ergänzung außerhalb der Vorlesung

**Diese Note ist eine Ergänzung außerhalb der Vorlesung.** Auf Folie 10 des Vorlesungs-PDFs („Termin 14 ITSM Leutgeb") stehen die zwei Prinzipien-Sätze nur als Aufgabe ohne inhaltliche Auflösung. Die Inhalte folgen wörtlich dem ISACA-Original (COBIT 2019 Framework: Introduction and Methodology). Bei der mündlichen Prüfung sollte transparent gemacht werden, dass diese Ergänzung über den Foliensatz hinausgeht — sie ist aber Standardwissen für jede COBIT-2019-Foundation-Zertifizierung und mit hoher Wahrscheinlichkeit prüfungsrelevant, da sie auf der Folie als Frage gestellt wurde.
