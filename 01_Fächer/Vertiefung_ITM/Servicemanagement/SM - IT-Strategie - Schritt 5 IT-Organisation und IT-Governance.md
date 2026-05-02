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

# SM - IT-Strategie - Schritt 5 IT-Organisation und IT-Governance

> [!info] Kurzdefinition
> Fünfter Schritt nach Johanning (2019). Anpassung der IT-Organisation und IT-Governance-Struktur an die in Schritten 1–4 definierte Strategie. Kern: das **Demand/Supply-Modell** mit klaren Rollen und Schnittstellen, ergänzt um Governance-Vorgaben (Rolle der IT, Compliance, Standards) und einer expliziten Soll-Rolle der IT im Unternehmen.

## Beschreibung

Schritt 5 (Buchkapitel 9) ist mit 47 Seiten das umfangreichste Kapitel und behandelt zwei eng verzahnte Themenkomplexe: **Aufbauorganisation** (klassische und moderne IT-Organisationsformen, vor allem Demand/Supply) und **IT-Governance** (Rolle der IT, Gremien, Standards, Compliance).

Eingangs benannte Herausforderungen:
- Hohe Innovationsgeschwindigkeit, ständig hoher Kapital- und Know-how-Bedarf
- Wandel der IT-Organisationsformen in kurzen Zyklen
- Unklare Einbindung in die Unternehmenshierarchie (oft Reporting an CFO)
- Rollenkonflikt: hoheitliche Aufgaben vs. Dienstleister
- Unklare Rolle bei Digitalisierung — Konkurrenz CIO vs. CDO (Chief Digital Officer)
- Carr-Frage: *„IT doesn't matter"* — ist IT Commodity?

## Bestandteile / Aufbau

### A. IT-Organisationsmodelle

#### Vier klassische Organisationsformen

| Form | Beschreibung | Vorteile | Nachteile |
|---|---|---|---|
| **IT als Abteilung innerhalb eines Bereichs** | IT unter Bereichsleiter (z. B. Finanzen) | Klarer Fokus auf Bereichsanforderungen | Bereichsdominanz, mangelnde Gesamtsicht, oft budgetär ausgerichtet |
| **IT als eigenständiger Bereich** | IT direkt unter Unternehmensleitung | Kunden-/Fachbereichsorientierung, Flexibilität, Autonomie | Mehr Schnittstellen, Bereichsegoismus-Tendenz |
| **IT als Stabsstelle** | Beratende, ausführende Funktion ohne Weisungsbefugnis | Klare Standards, Expertenfokus, weniger Konflikte | Hohes Konfliktpotenzial — Beratung führt informell zu Entscheidungen |
| **IT als Matrix (zentral + dezentral)** | Zentrale IT mit Rahmenrichtlinien + dezentrale Bereichs-IT | Nähe zu Fachbereichen, Business-IT-Alignment | Hohes Koordinationsaufkommen, langsame oder halbherzige Entscheidungen, oft teuer |

#### Plan-Build-Run

Drei IT-Bereiche (Anfang 2000er):
- **PLAN** — Planung, Steuerung, Kontrolle (Anforderungsmgmt, IT-Controlling, IT-Architektur, IT-Projektoffice, IT-Prozesse)
- **BUILD** — Erstellen, Weiterentwickeln, Pflegen der Applikationen + Test-/Qualitätsmanagement
- **RUN** — Betreuung/Wartung Infrastruktur, IT-Betrieb, Hotline

Weiterentwickelt zu **Source-Make-Deliver** (Brenner/Zarnekow 2003, Universität St. Gallen).

#### Shared Service Modelle (Mitte 2000er)

Eigene Gesellschaften / interne Service Center mit Kundenverhältnis. Ziele: Transparenz IT-Kosten, Marktmechanismus, unternehmerisches Handeln, Kundenorientierung, Standardisierung, Benchmarking.

#### Drei Geschwindigkeitslevel

- **klassisch** — Wasserfall
- **agil** — agile Methoden
- **bi-modal** — gemischt: agile Teams + klassische Teams parallel

Empfehlung Johanning: Bi-modal als Übergang zu DevOps.

#### Demand/Supply Organisationsmodell (Kern des Kapitels)

Die IT wird in zwei Hauptzweige geteilt:

| Zweig | Aufgaben | Rollen |
|---|---|---|
| **Demand (Nachfrage-Organisation)** | Anforderungsmanagement (Request, Change), Kosten-/Nutzen-/Wirtschaftlichkeitsanalysen, Prozess-Management | Demand Manager, DIO (Divisional Information Officer) |
| **Supply (Liefer-Organisation)** | Anwendungsentwicklung und -betreuung, IT-Qualitäts-/Test-Management, Betrieb und Infrastruktur | CTO / Supply-CIO, Provider-Manager |

**Querschnittsfunktionen** (im CIO- bzw. CTO-Office):
- CIO-Office: IT-Strategie, IT-Architektur, IT-Controlling, IT-Projektmanagement
- CTO-Office: IT-Providermanagement, Service Management Prozesse

**Drei Eingliederungsvarianten der Demand-IT** (Brenner et al.):

| Variante | Beschreibung |
|---|---|
| **Geschäftsbereichs-integriert / Dezentrale Fachbereichs-IT** | Demand-Aufgaben direkt im Fachbereich, keine dedizierte IT-Demand-Org. — Risiko: IT-Governance unzureichend ausgeführt |
| **Dezentral-koordiniert / Dezentrale Demand-IT** | Dedizierte Demand-Manager / DIOs pro Geschäftsbereich, fachlich geführt von CIO, disziplinarisch von Bereichsleitung |
| **Unternehmensweit-zentralisiert / Zentrale Demand-IT** | Zentrale Demand-Einheit für alle Geschäftsbereiche; Verrichtungsprinzip; ggf. CIO als CPO (Chief Process Officer) |

**Drei Führungsvarianten** (Aufteilung CIO ↔ CTO):
1. **Dezentrale Demand-IT** — eigenes CIO-Office (Demand) + eigenes CTO-Office (Supply)
2. **Zentralisierte Demand-IT** — Anforderungs- und Prozessmanagement direkt bei Demand-Managern
3. **Demand/Supply in einem CIO-Office** — Beide Zweige unter einem CIO

#### Drei Kern-Rollen im Demand/Supply

| Rolle | Standort | Aufgaben |
|---|---|---|
| **Application Owner / System Owner** | Demand-IT | Technische Verantwortung, Bebauungsplanung, Pflichtenheft, Projektleitung bei Upgrades, 2nd-Level-Support technisch, Applikationsbudget |
| **Process Owner** | Fachbereich | Fachliche Verantwortung, Entscheidung über Anforderungsumsetzung, Freigabe nach Neueinspielungen |
| **Process Expert** | Fachbereich | Fachliche Expertise, Lastenheft erstellen, fachliche Tests, 2nd-Level-Support fachlich |

#### Ziele Demand/Supply

1. Business-IT-Alignment — Leistungen aus geschäftlichen Anforderungen herleitbar
2. Trennung von IT-Nachfrage und IT-Angebot — Konflikt individuelle Lösung vs. Standardisierung lösbar
3. Transparenz — Kosten, Leistungen, Aufgaben
4. Effizienzverbesserung — kürzere Entscheidungswege, klare Verantwortlichkeiten
5. Mitarbeitermotivation — klare Aufgaben- und Rollendefinitionen

#### Supply-IT und ITIL

Supply orientiert sich an ITIL. Johanning weist auf Brenner-Kritikpunkte hin:
- ITIL stark im Service Support / Service Delivery, **nicht** vollständiges Org.-Modell
- ITIL beschreibt das *Was*, nicht das *Wie*
- Generisches Modell, keine branchen-/größenspezifischen Hinweise

### B. IT-Governance (Rolle, Gremien, Compliance)

**Aufgaben:**
- Bereitstellung von Führungs- und Organisationsstrukturen + Prozessen zur Unterstützung der Unternehmensstrategie
- Definition der Rolle der IT im Unternehmen
- Klärung der Entscheidungsbefugnisse der IT-Verantwortlichen
- Compliance-Funktionen: Sicherheit (Integrität, Verfügbarkeit, Vertraulichkeit, Verlässlichkeit), Transparenz (Projekt-Bewertung), revisionssichere Strukturierung, Erfüllung gesetzlicher Anforderungen
- Standards: ITIL, COBIT

#### Rolle der IT — zwei Modelle

**Modell 1: Agarwal & Sambamurthy** — drei Rollentypen:

| Rolle | Beschreibung | CIO-Position | Geeignet für |
|---|---|---|---|
| **Partner-Modell** | IT aktiver Partner für geschäftliche Innovationen | CIO direkt an CEO | Unternehmen mit IT-affiner Spitze, Innovations-getriebenes Geschäftsmodell |
| **Plattform-Modell** | IT als Plattform zur Unterstützung der Fachbereiche | CIO an CFO/COO | Einheitliche IT-Anforderungen über Bereiche, hoher IT-Background in Fachbereichen |
| **Skalierbares Modell** | (Beschreibung im PDF abgeschnitten — *im Auszug nicht vollständig*) | CIO direkt an CEO | Stark zyklische Branchen |

**Modell 2: Kienbaum/BITKOM 2016 — fünf IT-Rollen:**
1. Dienstleister (Business Continuity sichern) — ca. 2/3 aller IT-Orgs
2. Transformator (Business-Anforderungen → IT-Lösungen)
3. Initiator (Prozess-Standardisierung und -Optimierung)
4. Technologie-Innovator (technische Innovationen)
5. Business Innovator (Geschäftsinnovationen)

> *Wichtig: Es gibt fast immer eine Differenz zwischen Ist-Rolle und Soll-Rolle der IT. Ebenso gibt es Wahrnehmungsunterschiede — Unternehmensleitung sieht IT oft als Dienstleister, CIO oft als Business Innovator. Die IT-Strategie muss diese Differenzen explizit adressieren.*

## Beispiel

Buch-Beispiel Produktio weltweit GmbH (gekürzt):

- **Aktuelle Org. (vor Strategie):** IT als eigenständiger Bereich mit drei Abteilungen (IT-Operations, IT-Applikationen, IT-Office); Reporting an kaufmännischen Leiter
- **Probleme:** Anforderungsmanagement intransparent, kein Gremium, Fachbereich frustriert
- **Soll-Org. (nach Strategie):** Demand/Supply-Modell mit drei Demand-Managern (FI/CO/HCM, Logistik/Produktion, Einkauf/QM/Vertrieb) gegenüber fünf Competence Centern in der Supply (FI/CO/HCM, WM/SD+MES, QM/SD, Operations, Infrastructure/Security)
- **CIO als Chief Process Officer (CPO)** für gesamte Geschäftsprozess-Optimierung

## Abgrenzung

- **Klassische IT-Org. vs. Demand/Supply**: Klassisch ist nach Funktionen (Operations/Applikationen/Office) gegliedert; Demand/Supply nach Wertschöpfungsrichtung (Bestellung → Lieferung).
- **Plan-Build-Run vs. Demand/Supply**: PBR hat drei Bereiche (PLAN ist getrennt); Demand/Supply hat zwei (PLAN ist Teil des Demand).
- **CIO vs. CTO**: CIO = Information Officer (eher Demand-/Strategie-Sicht); CTO = Technology Officer (eher Supply-/Technik-Sicht).
- **CIO vs. CDO**: CIO klassisch IT; CDO (Chief Digital Officer) für Digitalisierungsinitiativen — Konkurrenzpotenzial.
- **Carr-These „IT doesn't matter"**: Provokante These, dass IT zur Commodity geworden sei. Johanning widerspricht implizit über die Innovator-Rollen der Kienbaum-Studie.
- **Beziehung zu COBIT 2019** (siehe [[SM - Standard - COBIT 2019 Framework]]): COBIT operationalisiert IT-Governance umfassend; Johanning verweist auf COBIT als Standard, ohne Details auszuführen.
- **Beziehung zu Rüter-Modell** (siehe [[SM - Corporate Governance vs IT-Governance]]): Schritt 5 detailliert die in Folie 12 des Hauptfoliensatzes nur grob skizzierte IT-Governance-Box.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche zwei Hauptzweige hat das Demand/Supply-Modell? — Demand (Nachfrage, Anforderungsmanagement) und Supply (Lieferung, Entwicklung+Betrieb).

**Anwendungsfrage:** Welche drei Eingliederungsvarianten der Demand-IT gibt es nach Brenner? — Geschäftsbereichs-integriert, Dezentral-koordiniert, Unternehmensweit-zentralisiert.

**Diskussionsfrage:** Welche Vor- und Nachteile hat eine zentrale Demand-IT gegenüber einer dezentralen? — Zentral: Skaleneffekte über Bereiche, Standards leichter umsetzbar; Dezentral: bessere Bereichsnähe, gezieltere Lösungen.

**Mögliche Anschlussfragen:**
- Welche drei Rollen hat das Demand/Supply-Modell? — Application/System Owner (IT-Demand), Process Owner (FB), Process Expert (FB).
- Welche Ziele verfolgt Demand/Supply? — Business-IT-Alignment, Trennung Nachfrage/Angebot, Transparenz, Effizienz, Mitarbeitermotivation.
- Welche Geschwindigkeitslevel kennt Johanning? — klassisch, agil, bi-modal.
- Welche fünf IT-Rollen kennt die Kienbaum-Studie? — Dienstleister, Transformator, Initiator, Technologie-Innovator, Business Innovator.
- Welche Kritik äußert Brenner an ITIL? — Kein vollständiges Org-Modell; beschreibt nur Was, nicht Wie; generisch ohne branchen-/größenspezifische Anpassung.
- Was unterscheidet CIO und CDO?

## Verwandt

- [[SM - VL - IT-Strategie 7 Schritte]]
- [[SM - IT-Strategie - Schritt 4 Sourcing-Strategie]]
- [[SM - IT-Strategie - Schritt 6 Umsetzung Roadmap Budget Projektportfolio]]
- [[SM - Corporate Governance vs IT-Governance]]
- [[SM - Governance - Definition]]
- [[SM - Standard - COBIT 2019 Framework]]
- [[SM - COBIT 2019 - Komponenten IT-Governance-System]]
- [[SM - ITIL - Überblick]]
- [[SM - IT-Servicemanagement - Aufgaben und Kernprozesse]]
- [[SM - ITIL 4 - Dimension Organisationen und Menschen]]

## Quelle

- Vorlesung: [[SM - VL - IT-Strategie 7 Schritte]]
- PDF: `Folien/Servicemanagement/Folien/IT-Strategie/Schritt 5.pdf` (47 Seiten = Johanning Kap. 9, S. 193–239)
- Quelle: Johanning, V. (2019). *IT-Strategie.* Wiesbaden: Springer Fachmedien
- Im PDF zitiert: Brenner/Zarnekow [5], Brenner et al. [7], Gadatsch [18], Kienbaum/BITKOM Studie [22], Agarwal & Sambamurthy [1]

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
