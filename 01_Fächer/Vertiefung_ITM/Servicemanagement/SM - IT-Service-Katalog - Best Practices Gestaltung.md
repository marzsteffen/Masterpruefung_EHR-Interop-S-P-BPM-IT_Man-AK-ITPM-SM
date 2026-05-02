---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - IT-Service-Katalog - Best Practices Gestaltung

> [!info] Kurzdefinition
> Best Practices nach Floerecke 2021 zur Gestaltung eines IT-Service-Katalogs: gemeinsamer Pflegeprozess mit Service-Owner, Katalog-Manager und Policy; einzelne Services über strukturierte Attribute beschreiben; atomare Services und Service Bundles ergänzen; Self-Service-Portal selbsterklärend gestalten (mobile First, Warenkorbfunktion, alphabetische Auflistung, Suchfunktion).

## Beschreibung

Folien 126, 128–132 (Quelle: Floerecke 2021).

### Gestaltungs- und Pflegeprozess (Folie 126)

ITSM-Prozesse und die dafür verantwortlichen Abteilungen agieren auf Basis des IT-Service-Katalogs. Daher:

- Sind alle Bereiche bei der Erstellung einzubeziehen.
- Aufbau des Katalogs muss fortlaufend mit repräsentativen Kunden getestet werden.
- Entscheidungen dürfen nicht im Alleingang getroffen werden.

Sobald die grundlegende Struktur des IT-Service-Katalogs existiert:

- **Service-Owner** müssen genaue Beschreibungen ihrer IT-Services erstellen.
- **Katalog Manager** überprüft einzelne Beschreibungen und überträgt diese in den Katalog.

**Katalog Manager ist verantwortlich für:**
- Pflege des Katalogs
- Sorgt dafür, dass Themen aktuell und richtig sind

**IT-Service-Katalog-Policy** dient der Bekanntmachung der Prozesse und Verantwortlichkeiten.

### Definition und Beschreibung einzelner IT-Services (Folie 128–129)

> „Beziehbare IT-Services der Kundensicht sollten wie IT-Services, und eben nicht vordergründig wie Produkte und Applikationen, bezeichnet und beschrieben werden. Aus der Kundenperspektive stellt der Nutzen das entscheidende Kriterium dar."

Beispiel (Folie 128): „Beim beziehbaren IT-Service Video-Konferenz können die zur Auswahl stehenden Applikationen, wie etwa Skype oder Webex, als Option gewählt werden. Diese Anwendungen stehen für sich allein genommen für keinen IT-Service. Denn dahinter verbergen sich noch eine Vielzahl von Zusatzleistungen wie Support und Wartung und technischen Komponenten wie Server und Netzwerk."

**Attribute der Bezeichnung** (Folie 129):

| Attribut | Attribut |
|---|---|
| Bezeichnung | Versionsnummer |
| Kurzbezeichnung | Hersteller |
| Nutzerhandbücher | Bilder und Videos |
| Gewicht und Maße (bei Hardware) | Vertragslaufzeit |
| SLAs | Preis |
| Service-Owner | Kontaktperson |
| Dauer bis zur Service-Bereitstellung | Wartungsfenster |
| Benötigtes Endgerät zur Nutzung | Ähnliche IT-Services |
| Datum letzter Aktualisierung | Version der Beschreibung |

### Grundsätzliches zur Gestaltung (Folien 130–132)

- Neben atomaren IT-Services sollten **Service Bundles** geschaffen werden — sie erleichtern Kund:innen die Bestellung technisch kompatibler und fachlich sinnvoller Kombinationen.
- Da Besteller mitunter über wenig Kenntnis verfügen, kann es hilfreich sein, **grundlegende Preiskategorien** zur Orientierung einzuführen (zusätzlich zum tatsächlichen Preis).
- Wird ein IT-Service in verschiedenen SLA-Varianten angeboten, sollten diese **als Optionen** geführt werden — nicht als eigene Services. Sonst Aufblähung des Katalogs.
- Service-Individualisierung auf ein Minimum beschränken (Risiken und Kosten).

**Self-Service-Portale** (Folien 131–132):
- Müssen selbsterklärend sein (Nutzer bestellen ggf. nur 2-3-mal jährlich).
- Leichte Handhabung ohne Schulung.
- Zusätzlich zu Desktop-Version auch eine mobile Version (mobile-First-Ansatz).
- Gesamtübersicht für Führungskräfte: Welche Services werden aktuell bezogen?
- Warenkorbfunktion und Favoritenliste.
- Services in eindeutige Kategorien unterteilen.
- Alphabetische Auflistung von Services und eine Hotbar mit den gefragtesten Services.
- Umfangreiche Suchfunktion.
- Möglichkeit, selbst Services vorschlagen zu können (Pflichtfelder, Pflichtinformation).

## Bestandteile / Aufbau

| Bereich | Best Practice |
|---|---|
| Pflegeprozess | Service-Owner liefert Beschreibungen, Katalog Manager pflegt zentral, IT-Service-Katalog-Policy regelt |
| Servicebezeichnung | Aus Kundensicht, nutzenorientiert (nicht produkt-/applikationsorientiert) |
| Beschreibungs-Attribute | 18 strukturierte Attribute (siehe Tabelle Folie 129) |
| Bundles | Atomare Services + Service Bundles |
| SLAs | Als Optionen, nicht als eigene Services |
| Preiskategorien | Zur Orientierung neben tatsächlichem Preis |
| Self-Service-Portal | Selbsterklärend, mobile-First, Warenkorb, Suche, Hotbar, alphabetisch, Self-Vorschläge |

## Beispiel

Krankenhaus-IT-Service „Video-Konferenz für Telemedizin":

- Bezeichnung: „Video-Konferenz Telemedizin Standard"
- Kurzbezeichnung: VC-Tele
- Service-Owner: IT Telemedizin
- SLA: 99,9 % Verfügbarkeit, 24/7-Support
- Preis: € 50 / Monat / User; Preiskategorie „mittel"
- Optionen (Applikationen): Skype, Webex, Microsoft Teams
- Bundle: zusammen mit Headset, Kamera, Endgerät
- Wartungsfenster: Sonntag 02:00–04:00 Uhr
- Ähnliche IT-Services: Standard Video-Konferenz

## Abgrenzung

- **Best Practices vs. Sichten und Strukturierung** (siehe [[SM - IT-Service-Katalog - Sichten und Strukturierung]]): Diese Note ist die *Operationalisierung*; jene die *Strukturvorlage*.
- **Best Practices vs. ITIL Service Catalogue Management Practice**: Service Catalogue Management ist die ITIL-4-Practice; diese Best Practices sind ergänzende, paper-basierte Empfehlungen (Floerecke 2021) zur konkreten Gestaltung.
- **Service Bundle vs. atomarer Service**: Atomar = einzelner Service; Bundle = Kombination aus mehreren atomaren Services für sinnvolle Kunden-Pakete.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Rollen sind im Pflegeprozess des IT-Service-Katalogs verantwortlich? — Service-Owner (Beschreibungen), Katalog Manager (zentrale Pflege), IT-Service-Katalog-Policy.

**Anwendungsfrage:** Erstellen Sie für einen konkreten IT-Service (z. B. Pflege-Tablet) ein vollständiges Beschreibungs-Set anhand der 18 Attribute aus Folie 129.

**Diskussionsfrage:** Warum sollten SLAs als Optionen und nicht als eigene Services geführt werden? — Vermeidet Katalog-Inflation; gleicher Service in 3 Servicelevel = 1 Service mit 3 Optionen, nicht 3 verschiedene Services.

**Mögliche Anschlussfragen:**
- Was ist ein Service Bundle?
- Welche Anforderungen an ein Self-Service-Portal nennt Floerecke?
- Was ist die Rolle des Katalog Managers?
- Warum sollten Services nicht produkt-/applikationsorientiert beschrieben werden?

## Verwandt

- [[SM - IT-Service-Katalog - Sichten und Strukturierung]]
- [[SM - Service-Katalog - Definition und Aufbau]]
- [[SM - ITIL Practice - Service Level Management]]
- [[SM - Paper - Floerecke 2021 Service Catalogue]] *(geplant)*

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 126, 128–132; Quelle: Floerecke (2021), Best Practices für die Gestaltung eines IT-Service-Kataloges, DOI [10.1365/s40702-020-00702-y](https://doi.org/10.1365/s40702-020-00702-y)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
