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

# SM - IT-Service-Katalog - Sichten und Strukturierung

> [!info] Kurzdefinition
> Ein IT-Service-Katalog hat zwei Sichten — eine **interne IT-Sicht** mit technischen Details und eine **Kundensicht** in der Sprache der Kunden. Die Strukturierung erfolgt in einer flachen, höchstens dreistufigen Hierarchie aus Top-Level-Kategorie, Sub-Kategorie und beziehbarem IT-Service.

## Beschreibung

Folien 123–127 (Quelle: Floerecke 2021, „Best Practices für die Gestaltung eines IT-Service-Kataloges", DOI 10.1365/s40702-020-00702-y) führen die Best-Practice-Gestaltung des IT-Service-Katalogs ein.

**Zwei Sichten** (Folien 124–125):

- **Interne IT-Sicht**: Beschreibung der IT-Services mit notwendigen technischen Details, z. B.:
  - Genehmigungsprozesse
  - Mapping zwischen IT-Services und IT-Systemen/-Komponenten in einer Configuration-Management-Database (CMDB)

- **Kundensicht**:
  - In der Sprache von Kunden (einfach und leicht verständlich)
  - Technische Details vermeiden

Vergleich (Folie 124): „**Vergleichbar mit Speisekarte** — Kunden wollen eine gegliederte Übersicht über das Angebot. Küchenpersonal interessieren die Zutaten und die Zubereitung."

**Strukturierungsebenen** (Folie 127): Flache, zwei- bis maximal **dreistufige Hierarchie**:

1. **Top-Level-Kategorie** (z. B. PC-Arbeitsplatz, Telefonie, Netzwerk & Server)
2. **Sub-Kategorie** (z. B. mobiler Arbeitsplatz)
3. **Beziehbarer IT-Service** (z. B. Laptop-Business-Klein)

Regeln:
- Einer Top-Level-Kategorie sind eine oder mehrere Sub-Kategorien zugeordnet.
- Sub-Kategorie (mittlere Stufe) kann bei überschaubarem IT-Leistungsportfolio entfallen.
- Jede Ebene sollte nicht mehr als zehn Ebenen enthalten — diese Restriktion bietet Platz für bis zu 1000 IT-Services.

## Bestandteile / Aufbau

| Sicht | Inhalt | Adressat |
|---|---|---|
| Interne IT-Sicht | Genehmigungsprozesse, CMDB-Mapping, technische Details | IT-Mitarbeiter |
| Kundensicht | Verständliche Sprache, ohne Technik-Details | Anwender, Fachabteilungen |

| Ebene | Bezeichnung | Beispiel |
|---|---|---|
| 1 | Top-Level-Kategorie | PC-Arbeitsplatz |
| 2 | Sub-Kategorie | Mobiler Arbeitsplatz |
| 3 | Beziehbarer IT-Service | Laptop-Business-Klein |

## Beispiel

Krankenhaus-IT-Service-Katalog (eigenes Beispiel):

- **Top-Level:** Klinische Anwendungen
  - **Sub:** Patientenbezogene Anwendungen
    - **Service:** KIS-Zugang Standard
    - **Service:** RIS-Zugang
  - **Sub:** Spezialsysteme
    - **Service:** PACS-Zugang Radiologie
- **Top-Level:** Endgeräte
  - **Sub:** Mobile Endgeräte
    - **Service:** Pflege-Tablet
- **Top-Level:** Telekommunikation
  - **Service:** DECT-Telefon Pflege

## Abgrenzung

- **Sichten und Strukturierung vs. Best Practices Gestaltung** (siehe [[SM - IT-Service-Katalog - Best Practices Gestaltung]]): Diese Note fokussiert auf die *Struktur* des Katalogs; die andere Note auf die *Pflege/Bereitstellung*.
- **Service-Katalog vs. Service Portfolio**: Service Portfolio umfasst alle Services (auch geplante, retired); Service-Katalog nur die aktuell beziehbaren.
- **Interne Sicht vs. Kundensicht**: Beide sind dasselbe Inventar mit unterschiedlicher Darstellung — analog zur Datenbank vs. Anwendungsschicht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche zwei Sichten hat ein IT-Service-Katalog laut Floerecke 2021? — Interne IT-Sicht (technisch) und Kundensicht (verständlich).

**Anwendungsfrage:** Skizzieren Sie für eine Krankenhaus-IT eine zweistufige Hierarchie (Top-Level, beziehbarer Service). Wann wäre die Sub-Kategorie sinnvoll?

**Diskussionsfrage:** Warum ist der Vergleich mit der Speisekarte aussagekräftig? — Trennt klar Zubereitungs-Sicht (intern) von Konsum-Sicht (extern); macht die Notwendigkeit beider Sichten plausibel.

**Mögliche Anschlussfragen:**
- Wie groß darf eine Hierarchieebene maximal sein? — 10 Einträge (für bis zu 1000 Services).
- Welche Inhalte gehören in die interne IT-Sicht? — Genehmigungsprozesse, CMDB-Mapping.
- Wie verhält sich die Strukturierung zu den Allweyer-Gliederungspunkten ([[SM - Service-Katalog - Definition und Aufbau]])?

## Verwandt

- [[SM - Service-Katalog - Definition und Aufbau]] *(Allweyer-Sicht)*
- [[SM - IT-Service-Katalog - Best Practices Gestaltung]]
- [[SM - ITIL Practice - Service Configuration Management]]
- [[SM - Paper - Floerecke 2021 Service Catalogue]] *(geplant)*

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 123–125, 127; Quelle: Floerecke (2021), Best Practices für die Gestaltung eines IT-Service-Kataloges, DOI [10.1365/s40702-020-00702-y](https://doi.org/10.1365/s40702-020-00702-y)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
