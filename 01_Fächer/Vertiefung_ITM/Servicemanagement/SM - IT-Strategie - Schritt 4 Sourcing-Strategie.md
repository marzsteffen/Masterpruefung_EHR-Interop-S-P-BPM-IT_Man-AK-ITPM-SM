---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Strategie 7 Schritte]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - IT-Strategie - Schritt 4 Sourcing-Strategie

> [!info] Kurzdefinition
> Vierter Schritt nach Johanning (2019). Beantwortet die klassische Make-or-Buy-Frage: Welche IT-Leistungen bleiben intern, welche werden ausgelagert? Drei Entscheidungsdimensionen: **Grad der Auslagerung**, **Anzahl der Provider**, **Standort der Leistungserbringung**. Vier Sourcing-Arten plus Cloud-Computing als moderne Variante.

## Beschreibung

Schritt 4 (Buchkapitel 8) operationalisiert die Make-or-Buy-Entscheidungen für die in Schritt 3 definierten Applikationen. Leitsatz (Prof. Brenner, Universität St. Gallen):

> „Vertrauen ist das Schlüsselwort für ein erfolgreiches Outsourcing von IT-Leistungen an einen externen Lieferanten."

In der Praxis bedeutet Sourcing meist Outsourcing — daher beleuchtet das Kapitel zuerst Pro/Contra Outsourcing, dann die Wirtschaftlichkeit, dann die konkreten Sourcing-Arten und schließlich die Strategie-Dimensionen.

## Bestandteile / Aufbau

### Motive für Outsourcing (Buy)

- Reduzierung der Fertigungstiefe
- Kostenersparnis durch Skaleneffekte beim Provider
- Variabilisierung der Fixkosten
- Verbesserter Zugang zu Know-how, Kompetenzen, Verfahren, Methoden
- Verbesserung der Qualität der IT-Services
- Flexible Anpassung an den tatsächlichen Bedarf
- Konzentration auf Kernkompetenzen
- Zugriff auf Know-how des Providers

### Motive für Insourcing / Make

- Know-how intern belassen (Schutz von Kernprozessen)
- Wiedererlangung von verlorengegangenem Know-how
- Weniger Zeitaufwand für Koordination
- Geringere Provider-Abhängigkeit
- Reduktion von Qualitätsproblemen / Mängeln

### Make-or-Buy-Matrix

Achsen:
- **X-Achse:** Differenzierung im Wettbewerb (niedrig ↔ hoch)
- **Y-Achse:** Stärken des Unternehmens (niedrig ↔ hoch)

| Quadrant | Empfehlung |
|---|---|
| Stärken hoch + Differenzierung hoch | **Make** (Kernprozess) |
| Stärken hoch + Differenzierung niedrig | Make oder Buy (Supportprozess) |
| Stärken niedrig + Differenzierung hoch | Make oder Buy (Supportprozess) |
| Stärken niedrig + Differenzierung niedrig | **Buy** (Outsourcing) |

Typische Buy-Kandidaten: Commodities (RZ, Hardware, Office). Typische Make-Kandidaten: wertschöpfende Applikationen (z. B. das MES der Produktio weltweit GmbH).

### SWOT-Analyse IT-Outsourcing

| | Intern (S/W) | Extern (O/T) |
|---|---|---|
| Positiv | **S — Stärken:** Reduzierung Fertigungstiefe, Know-how-Zugang, bessere Qualität, flexible Anpassung, Konzentration auf Kernkompetenzen | **O — Chancen:** Kostensenkung, Variabilisierung Fixkosten, flexible Geschäftsprozesse, schnellere Time-to-Market, verbesserte IT-Sicherheit |
| Negativ | **W — Schwächen:** Möglicher Kontroll-/Kompetenzverlust, hoher Koordinationsaufwand, Qualitätsprobleme schwer kontrollierbar | **T — Risiken:** Hohe Abhängigkeit vom Provider, Probleme bei Rückintegration/Insourcing, Gefahr für Geschäftsgeheimnisse, interner Know-how-Verlust |

### Wirtschaftlichkeit: TCO-Betrachtung

Kostenstruktur eines IT-Outsourcing-Vorhabens (nach Gadatsch):

| Block | Inhalte |
|---|---|
| **A) Investitionen** | Vorprojekt-Kosten (Personal, Beratung, Recht), Transferprojekt-Kosten, Wirkungen der Eigentumsübertragung (Verkaufserlöse, Abfindungen, Wegfall Personalkosten) |
| **B) Laufende Betriebskosten** | Fixe und variable Outsourcing-Gebühren + sonstige |
| **C) Wirkungen des Outsourcings** | Direkt (Personalkostenreduktion, Wegfall Raumkosten); Indirekt (geringere Störungen, schnellerer Wiederanlauf, schnellere Inbetriebnahme nach Releases, Pönalen aus SLA-Überschreitungen) |

**TCO** (Total Cost of Ownership) ist die Pflicht-Methode. Risiko: indirekte Kosten (Qualität, Fehlerhäufigkeit, SLA-Einhaltung) sind schwer quantifizierbar.

### Vier Sourcing-Arten

| Art | Inhalt |
|---|---|
| **1. IT-Infrastruktur Outsourcing** | Hardware (Server, Drucker, Netzwerk, Endgeräte), systemnahe Software (Betriebssysteme, Datenbanken), Office-Software, Dienste (E-Mail, Internet), Entwicklungsumgebungen — alles **Commodities**. Typische Bereiche: Desktop Services, Rechenzentrum/Server Room, Netzwerk/Telekommunikation, User Helpdesk/Service Desk. |
| **2. Application Outsourcing** | Ganze IT-Systeme oder Applikationen (oft ERP, CRM). Zwei Formen: **Application Management Outsourcing** (Lizenzen beim Auftraggeber, Provider macht Betrieb/Wartung) und **Software-as-a-Service / ASP** (Lizenzen beim Provider, Mietmodell pro User über die Cloud). |
| **3. Business Process Outsourcing (BPO)** | Höchste Form: nicht nur IT, sondern ganze Geschäftsprozesse ausgelagert. Typisch: operative Personalprozesse (z. B. Lohnabrechnung kuvertieren), Finanz-/Accounting-Prozesse — stark standardisierbare Prozesse ohne Wettbewerbsrelevanz. |
| **4. Cloud Computing** | Modern: Services „on demand" über das Internet. Definition Cunningham: *„Cloud Computing is using the Internet to access someone else's software running on someone else's hardware in someone else's data centre."* |

### Cloud-Sourcing-Modelle

| Modell | Langform | Inhalt |
|---|---|---|
| **SaaS** | Software-as-a-Service | Software über Internet; Provider verantwortet Wartung, Support, Administration, Weiterentwicklung. Beispiel: Salesforce. |
| **IaaS** | Infrastructure-as-a-Service | Provider betreibt Serversysteme (Backup, Archivierung, Serverfarmen). |
| **PaaS** | Platform-as-a-Service | Komplettangebot Hardware + Software (Mischform aus SaaS und IaaS). |

### Cloud-Varianten

| Variante | Inhalt |
|---|---|
| **Public Cloud** | Vollständig beim Provider verwaltet. Maximale Skalierbarkeit, Pay-per-use möglich. |
| **Private Cloud** | IT-Organisation behält Kontrolle. Vorteil: Sicherheit (z. B. ERP-Daten). |
| **Managed Private Cloud** | Hybrid: dedizierte, autarke Infrastruktur bei einem Provider in einer Public-Cloud, mit gesicherter Verbindung (VPN, Direct Ethernet Link). |

Wichtige Abgrenzung Cloud vs. klassisches Outsourcing: Cloud verlangt Anpassung an Provider-Standards (kein Customizing); klassische Outsourcing-Provider passen oft an. Cloud ist schneller rentabel (klassisch: 4–5 Jahre, dabei oft sogar Kostenerhöhung bis 10 %).

### Sourcing-Strategien — Drei Dimensionen

#### Dimension 1: Grad der Auslagerung

| Sourcing-Art | Beschreibung | Vorteile | Nachteile |
|---|---|---|---|
| **Full Outsourcing** | Komplettes Outsourcing aller Infrastruktur- oder Applikationsdienste an einen Provider | Konzentration auf Kerngeschäft, Kostensenkung, bessere Servicequalität, externes Know-how | Provider-Abhängigkeit, aufwändige Rückabwicklung, wenig Skalierbarkeit, Know-how-Verlust, hohe Transaktions- und versteckte Kosten |
| **Selective Outsourcing** | Auslagerung eines Teils („Best of Breed"-Ansatz) | Konzentration aufs Kerngeschäft, externes Know-how, Kostensenkung | Know-how-Verlust, mehrere Provider erschweren Steuerung |
| **Outtasking / Managed Services** | Teil-Auslagerung | Geringe Provider-Abhängigkeit, Flexibilität, On-Demand, geringe Transaktionskosten | Eingeschränktes Customizing, fehlende Integration, Daten extern |
| **Shared Service Center** | Interne Ausgliederung in eigenes Service-Center (Tochter oder internes Competence Center) | Kostensenkung, bessere Prozess-/Datenkontrolle | Keine externen Best-Practices, Prozesse bleiben weitgehend gleich |

#### Dimension 2: Anzahl der Provider

| Modell | Beschreibung |
|---|---|
| **Single Sourcing** | Auslagerung an *einen* Dienstleister |
| **Generalunternehmerschaft** | Mischform: mehrere Dienstleister, aber gesteuert durch einen Generalunternehmer |
| **Multi Sourcing** | Mehrlieferantenstrategie — Auslagerung an mehrere Dienstleister |

Hintergrund: **Vendor-Lock-In** vermeiden. Klassisches Outsourcing erschwert Provider-Wechsel — Multi Sourcing reduziert Abhängigkeit, erhöht aber Steuerungsaufwand.

#### Dimension 3: Standort der Leistungserbringung

| Modell | Beschreibung |
|---|---|
| **Onshore** | Im eigenen Land — unkompliziert rechtlich, aber geringe Lohnkostenvorteile |
| **Nearshore** | Im benachbarten Ausland (z. B. Deutschland → Polen, Tschechien) |
| **Offshore** | Weit entferntes Ausland (z. B. Indien, Philippinen) — größte Kostenvorteile, aber Risiken bei Sprache, Kultur, Zeitverschiebung, Recht |

## Beispiel

Buch-Beispiel Produktio weltweit GmbH (aus Schritt 2 abgeleitet):
- **Make:** MES (wertschöpfend, Wettbewerbsvorteil), Salesforce-Customizing
- **Buy:** Office-Suite, RZ-Hosting (Commodities)
- **Cloud-SaaS:** Salesforce
- **Onshore + Single Sourcing für unternehmenskritische ERP-Bereiche**, Offshore-Helpdesk denkbar.

## Abgrenzung

- **Sourcing-Strategie vs. Applikationsstrategie** ([[SM - IT-Strategie - Schritt 3 Applikationsstrategie]]): Schritt 3 entscheidet *was* mit den Applikationen geschieht; Schritt 4 entscheidet *wer* sie betreibt.
- **Outsourcing vs. Cloud Computing**: Cloud ist eine spezielle Form moderner Outsourcings mit Standardisierungs-Zwang; klassisches Outsourcing erlaubt Customizing.
- **SaaS vs. ASP**: ASP ist der historische Begriff (vor 2000er Cloud); SaaS ist heute übliche Bezeichnung.
- **BPO vs. IT-Outsourcing**: BPO geht über IT hinaus — auch nicht-IT-Geschäftsprozesse werden ausgelagert.
- **Shared Service Center vs. Outsourcing**: Shared Service ist intern (Konzern-Tochter); Outsourcing ist extern.
- **Drei Säulen der IT** (siehe [[SM - IT-Strategie - Schritt 2 Herausforderungen und IT-Vision]]): Wertschöpfende Prozesse → Make/Insourcing; Standardisierbare Prozesse → BPO; Commodity Services → Outsourcing/Cloud.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Sourcing-Arten unterscheidet Johanning? — IT-Infrastruktur Outsourcing, Application Outsourcing, Business Process Outsourcing, Cloud Computing.

**Anwendungsfrage:** Welche drei Cloud-Sourcing-Modelle gibt es? — SaaS, IaaS, PaaS. Welche drei Cloud-Varianten? — Public, Private, Managed Private Cloud.

**Diskussionsfrage:** Warum ist die TCO-Betrachtung Pflicht bei Outsourcing-Entscheidungen? — Weil indirekte Kosten (Qualitätsprobleme, Wiederanlaufzeiten, SLA-Überschreitungen) oft die scheinbare Kostenersparnis überwiegen — sie müssen erfasst werden, sonst fällt der Business Case in der Praxis falsch aus.

**Mögliche Anschlussfragen:**
- Welche drei Dimensionen hat die Sourcing-Strategie? — Grad der Auslagerung, Anzahl der Provider, Standort.
- Was ist Vendor-Lock-In und wie wird er adressiert? — Multi Sourcing, Cloud-Computing mit standardisierten Schnittstellen.
- Welche Vor- und Nachteile hat Full Outsourcing vs. Selective Outsourcing?
- Welche Risiken birgt Offshore-Outsourcing?
- Was unterscheidet Cloud Computing von klassischem Outsourcing? — Standardisierungs-Zwang, kürzere Verträge, schneller rentabel, weniger Vendor-Lock-In.
- Wie hängt die Make-or-Buy-Matrix mit den Drei Säulen der IT zusammen?

## Verwandt

- [[SM - VL - IT-Strategie 7 Schritte]]
- [[SM - IT-Strategie - Schritt 2 Herausforderungen und IT-Vision]]
- [[SM - IT-Strategie - Schritt 3 Applikationsstrategie]]
- [[SM - IT-Strategie - Schritt 5 IT-Organisation und IT-Governance]]
- [[SM - SLA - Definition und Inhalte]]
- [[SM - ITIL 4 - Cloud Computing Auswirkungen]]
- [[SM - ITIL 4 - Dimension Partner und Lieferanten]]
- [[SM - SWOT-Analyse]]

## Quelle

- Vorlesung: [[SM - VL - IT-Strategie 7 Schritte]]
- PDF: `Folien/Servicemanagement/Folien/IT-Strategie/Schritt 4.pdf` (39 Seiten = Johanning Kap. 8, S. 153–193)
- Quelle: Johanning, V. (2019). *IT-Strategie.* Wiesbaden: Springer Fachmedien
- Im PDF zitiert: Hofmann/Schmidt [25], Cunningham [15], Brenner (Univ. St. Gallen), Gadatsch [18]

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
