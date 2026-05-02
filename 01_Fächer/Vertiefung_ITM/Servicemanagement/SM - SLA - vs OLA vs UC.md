---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - ITSM Einführung Text]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - SLA - vs OLA vs UC

> [!info] Kurzdefinition
> Drei verwandte ITIL-Vereinbarungstypen, die zusammen das Service-Level-Vereinbarungssystem bilden: **SLA** (Service Level Agreement) — extern mit dem Service-Konsumenten/Kunden; **OLA** (Operational Level Agreement) — intern zwischen IT-Einheiten desselben Unternehmens; **UC** (Underpinning Contract) — mit externen Lieferanten und Partnern. SLAs werden typischerweise durch OLAs und UCs „untermauert" (underpinned).

> [!warning] Quellen-Hinweis
> **In den verarbeiteten Vorlesungs-PDFs nicht definiert.** Begriffe SLA wird bei Allweyer und Leutgeb mehrfach erwähnt; OLA und UC werden im Foliensatz und Allweyer-Auszug *gar nicht* genannt. Diese Note ist als „Ergänzung außerhalb der Vorlesung" kennzeichnet und basiert auf dem ITIL-Standardvokabular (ITIL V3 und ITIL 4 Service Level Management).

## Beschreibung

In ITIL bilden SLA, OLA und UC ein verschachteltes Vertragssystem:

- Der Service Provider verpflichtet sich gegenüber dem Kunden in einem **SLA** zu bestimmten Service-Levels (z. B. 99,5 % Verfügbarkeit).
- Damit der Provider diese Zusage halten kann, schließt er **intern** OLAs mit unterstützenden IT-Einheiten (z. B. „Netzwerk-Team garantiert Backbone-Verfügbarkeit 99,9 %"; „Datenbank-Team garantiert DB-Verfügbarkeit 99,8 %").
- Mit **externen** Partnern (Cloud-Anbieter, Hardware-Wartung, Telekommunikations-Provider) schließt er **UCs**, die ähnliche Zusicherungen wie OLAs liefern, aber rechtlich zwischen unterschiedlichen Unternehmen geschlossen sind.

**Mathematische Konsequenz:** Damit die SLA-Zusage von z. B. 99,5 % Service-Verfügbarkeit haltbar ist, müssen die unterstützenden OLAs und UCs jeweils *höhere* Verfügbarkeits-Zusagen leisten — denn die Service-Verfügbarkeit ist (vereinfacht) das Produkt der Komponenten-Verfügbarkeiten.

## Bestandteile / Aufbau

| Vereinbarung | Vertragspartner | Charakter | Beispiel |
|---|---|---|---|
| **SLA** (Service Level Agreement) | Service Provider ↔ Kunde / Service-Konsument | Externer / fachlicher Vertrag | „Verfügbarkeit KIS Mo–Fr 7–19 Uhr ≥ 99,5 %" |
| **OLA** (Operational Level Agreement) | IT-Einheit A ↔ IT-Einheit B (intern, gleicher Anbieter) | Interne Vereinbarung, kein Rechtsvertrag | „Netzwerk-Team garantiert dem KIS-Team 99,9 % Backbone-Verfügbarkeit" |
| **UC** (Underpinning Contract) | Service Provider ↔ externer Lieferant | Externer Rechtsvertrag | „Telekom garantiert Internet-Anbindung 99,99 %" |

**Hierarchie:** Eine SLA wird durch eine oder mehrere OLAs und UCs „untermauert". Der Service-Anbieter ist gegenüber dem Kunden nur so leistungsfähig, wie es die schwächste OLA/UC erlaubt.

## Beispiel

Krankenhaus-IT, Service „Krankenhausinformationssystem":

- **SLA:** IT-Abteilung ↔ Pflegeleitung/Geschäftsführung — „99,5 % Verfügbarkeit Mo–So 24h, Antwortzeit < 3s, Lösungszeit kritischer Incidents < 30 min."
- **OLA 1:** IT-Service-Desk ↔ KIS-Anwendungsteam — „Service Desk eskaliert kritische Incidents binnen 5 min an 2nd Level."
- **OLA 2:** KIS-Anwendungsteam ↔ DB-Administratoren — „DB-Team garantiert Datenbankverfügbarkeit 99,9 %."
- **OLA 3:** KIS-Anwendungsteam ↔ Netzwerk-Team — „Netzwerk-Team garantiert Backbone 99,99 %."
- **UC 1:** IT-Abteilung ↔ KIS-Hersteller — „Hersteller-Support 24h-Reaktion bei Major Bugs."
- **UC 2:** IT-Abteilung ↔ Cloud-Provider — „Cloud-Verfügbarkeit 99,95 %, RPO 15 min."
- **UC 3:** IT-Abteilung ↔ Telekommunikations-Anbieter — „Internet-Anbindung 99,99 %."

Damit die SLA-Zusage von 99,5 % über 24/7 haltbar ist, müssen alle OLAs und UCs *zusammen* ein höheres Niveau bieten — z. B. wenn 4 unabhängige Komponenten mit je 99,9 % verkettet sind, ergibt sich rechnerisch nur (0,999)⁴ ≈ 99,6 %.

## Abgrenzung

- **SLA vs. OLA**: SLA ist *extern* (vertraglicher Charakter gegenüber dem Kunden); OLA ist *intern* (Vereinbarung zwischen Abteilungen desselben Unternehmens — meist nicht rechtlich bindend, sondern organisatorisch).
- **OLA vs. UC**: OLA ist *intern* (zwischen Einheiten desselben Anbieters); UC ist *extern* (rechtsverbindlicher Vertrag mit Drittunternehmen).
- **SLA vs. UC**: Beide sind externe Verträge, aber unterschiedliche Richtungen — SLA = Anbieter zusagt an Kunden; UC = Lieferant zusagt an Anbieter.
- **Bezug zu Allweyer SLA-Inhalten** (siehe [[SM - SLA - Definition und Inhalte]]): Der bei Allweyer betonte „Verantwortungsbereich" (Anbieter kann nur das garantieren, was in seinem Verantwortungsbereich liegt) ist der Kern, warum OLAs und UCs nötig sind.
- **Bezug zu ITIL 4 Service Level Management Practice** (siehe [[SM - ITIL Practice - Service Level Management]]): SLM-Practice steuert SLAs; OLAs/UCs werden in ITIL 4 weiterhin verwendet, aber weniger formal vorgeschrieben.
- **Bezug zu Cloud Computing** ([[SM - ITIL 4 - Cloud Computing Auswirkungen]]): Ein Cloud-Service-Vertrag ist ein UC — Cloud-Anbieter garantiert über UC bestimmte Verfügbarkeiten, die in den hauseigenen SLA einfließen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen SLA, OLA und UC? — SLA = mit Kunden, OLA = intern, UC = mit externem Lieferanten. SLA wird durch OLAs und UCs untermauert.

**Anwendungsfrage:** Skizzieren Sie für einen konkreten Krankenhaus-IT-Service alle drei Vereinbarungstypen. Welche Konsequenzen hat die Nicht-Einhaltung jeweils?

**Diskussionsfrage:** Warum müssen OLAs und UCs zusammen *strengere* Zusagen leisten als die SLA? — Wegen der Multiplikativität der Verfügbarkeiten in einer Service-Kette: jede unterstützende Komponente reduziert die Gesamtverfügbarkeit. Wenn die SLA-Zusage 99,5 % beträgt und vier kritische Komponenten verkettet sind, muss jede mehr als 99,87 % bieten.

**Mögliche Anschlussfragen:**
- Welche typischen Inhalte haben OLAs / UCs? — Ähnlich SLA-Inhalten (siehe [[SM - SLA - Definition und Inhalte]]): Verfügbarkeit, Zuverlässigkeit, Performance, Reaktionszeiten, Reporting.
- Wie verändert Cloud Computing die OLA/UC-Logik? — Mehr UCs (Cloud-Provider als externe Partner); weniger OLAs (interne IT wird kleiner).
- Was passiert, wenn ein Provider seinen UC verletzt? — Vertragsstrafen können vereinbart werden; SLA-Verletzung gegenüber dem Kunden kann mit „force majeure"-Argument gemildert werden, aber Anbieter bleibt typischerweise haftbar gegenüber dem SLA-Kunden.
- Sind SLAs ohne unterstützende OLAs/UCs valide? — Praktisch nein: Anbieter zusagt etwas, das er nicht halten kann.

## Verwandt

- [[SM - SLA - Definition und Inhalte]]
- [[SM - Service-Level - Utility vs Warranty]]
- [[SM - ITIL Practice - Service Level Management]]
- [[SM - ITIL 4 - Cloud Computing Auswirkungen]]
- [[SM - ITIL 4 - Dimension Partner und Lieferanten]]
- [[SM - IT-Strategie - Schritt 4 Sourcing-Strategie]]
- [[SM - IT-Service-Katalog - Best Practices Gestaltung]]

## Quelle

- Vorlesung: [[SM - VL - ITSM Einführung Text]] *(SLA bei Allweyer/Leutgeb behandelt; OLA/UC nicht)*
- Verwandte Konzept-Note (kein Quell-Anker): [[SM - SLA - Definition und Inhalte]]
- Folien/Seitenangabe: in den Vorlesungs-PDFs nicht definiert

## Ergänzung außerhalb der Vorlesung

**Diese Note ist eine Ergänzung außerhalb der Vorlesung.** Sie löst den unresolved Wiki-Link aus [[SM - SLA - Definition und Inhalte]] auf. OLA und UC werden weder im Allweyer-Auszug („ITSM Einführung Text") noch im Hauptfoliensatz Leutgeb noch im Buchauszug ITIL 4 Foundation Courseware definiert. Die Definitionen folgen dem ITIL-Standardvokabular (ITIL V3 + ITIL 4 Service Level Management Practice). Bei der mündlichen Prüfung sollte transparent gemacht werden, dass diese Begriffsabgrenzung über den Vorlesungsstoff hinausgeht — sie ist aber Standardwissen für jede ITIL-Foundation-Zertifizierung.
