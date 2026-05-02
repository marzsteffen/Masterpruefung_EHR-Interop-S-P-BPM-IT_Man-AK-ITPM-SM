---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - CCR und CCD]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Healthcare Systems - Zentralisierungs-Modelle

> [!info] Kurzdefinition
> Klassifikation nationaler Gesundheitssysteme nach ihrem Zentralisierungsgrad: **zentralisiert** (z. B. UK NHS), **semi-zentralisiert** (z. B. Österreich nach Bundesländern), **dezentralisiert** (z. B. USA). Die Implementierung von EHRs hängt stark vom System-Typ ab.

## Beschreibung

Aus Folie 2:

> „Implementation of EHRs strongly depends on the health care system:
> - centralized healthcare system → example: United Kingdom – NHS
> - semi-centralized healthcare system → example: Austria – each province can have different systems
> - decentralized healthcare system → example: USA"

## Bestandteile / Aufbau

| Modell | Beispiel | Konsequenz für EHR-Implementation |
|---|---|---|
| **Centralized** | UK – NHS | Top-down-Mandat möglich; einheitliches System nationalweit; großes Risiko bei zentralen Roll-outs |
| **Semi-centralized** | Österreich – jedes Bundesland kann eigene Systeme haben | Bundesland-spezifische Systeme; ELGA als nationale Klammer mit dezentralen Repositories |
| **Decentralized** | USA | Anreiz statt Mandat (siehe [[EHR - HITECH Act und ARRA 2009]]); Vielzahl an EHR-Vendoren (Cerner, Epic, Allscripts); Interoperabilität via Exchange-Standards |

## Beispiel

Österreich-Spezifikum (Folie 6):
- Healthcare ist **per Bundesland organisiert**
- HIS unterscheiden sich zwischen Bundesländern für Bundesland-eigene Krankenhäuser
- Private Krankenhäuser haben andere Systeme
- Zahnärzte, Physiotherapeuten, Psychotherapeuten haben oft eigene oder gar keine Systeme
- Reha-Zentren oft ohne ELGA-Anbindung

Persönliches Anekdotenbeispiel des Vortragenden (Folie 7):
- 2019 Mountainbike-Unfall → UKH Graz: einziger ELGA-Eintrag war Blutgruppe; Discharge Letter ca. 1 Seite
- 2020 3 Wochen Reha (gebrochener Oberarm): kein einziger ELGA-Eintrag

## Abgrenzung

- Zentralisierungs-Modell betrifft **politisch/organisatorische Steuerung**, nicht zwangsläufig die technische Architektur.
- Auch ein zentralisiertes System (NHS) kann technisch dezentrale Repositories haben.
- Auch ein dezentrales System (USA) kann lokale Mono­polisten haben (z. B. ein Krankenhausverbund mit Epic in einer Region).
- Nicht zu verwechseln mit [[EHR - Architektur - Zentral vs Dezentral]] (das ist die **technische Architekturfrage**).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei Zentralisierungs-Modelle nationaler Gesundheitssysteme werden unterschieden, und welches Beispielland passt zu welchem Modell?

**Anwendungsfrage:** Warum ist ELGA semi-zentral organisiert, und welche Konsequenzen hat das für EHR-Architektur und Patienten?

**Diskussionsfrage:** Welches Modell ist „besser"? Welche Trade-offs bestehen zwischen Top-down-Effizienz, regionaler Anpassung und Innovationsdynamik?

**Mögliche Anschlussfragen:**
- Wie hat das UK-NHS seine zentrale EHR-Strategie umgesetzt? (Stichwort: National Programme for IT, gescheitert)
- Wie verbindet ELGA als zentrales System die föderale Struktur Österreichs?
- Welche Probleme entstehen für Patienten in fragmentierten Systemen wie den USA?
- Wie lässt sich der ELGA-Mangel bei Reha-Zentren beheben?

## Verwandt

- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - ELGA - Technologie-Architektur]]
- [[EHR - HITECH Act und ARRA 2009]]
- [[EHR - VL - Meaningful Use]]
- [[EHR - Integrated Care - Macro Meso Micro Level]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folien 2, 6–8 (Implementation depends on health care system; Austria-Spezifika)
