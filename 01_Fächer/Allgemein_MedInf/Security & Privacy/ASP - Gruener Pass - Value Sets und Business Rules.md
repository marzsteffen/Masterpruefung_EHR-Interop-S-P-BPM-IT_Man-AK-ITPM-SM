---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Gruener Pass]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Grüner Pass - Value Sets und Business Rules

> [!info] Kurzdefinition
> **Value Sets** mappen die im DCC enthaltenen Codes (z. B. `EU/1/20/1528`) auf menschenlesbare Werte (z. B. „Comirnaty"). **Business Rules** definieren die Verifizierungslogik in Validator-Apps – ob ein Zertifikat gültig ist, hängt z. B. von Impfstoff, Dosis und Datum ab. Beide werden vom EU eHealth Network gepflegt; Länder können Business Rules adaptieren.

## Beschreibung

### Value Sets (Folie 11)

- **Value Sets bieten eine Zuordnung zwischen Rohdaten und „vom Menschen lesbaren" Daten** und werden vom JSON-Schema referenziert.
- Der QR-Code enthält **Rohdaten**.
- **Beispiele:**
  - `EU/1/20/1528` verweist auf „Comirnaty" (Impfstoff von BioNTech/Pfizer).
  - `ORG-100030215` verweist auf „BioNTechManufacturing GmbH".
- Value Sets Repository wird **regelmäßig aktualisiert**.
- Rohdaten werden für die **Durchsetzung von Business Rules** (Regeln) verwendet.

### Business Rules (Folie 12)

- **Business Rules stellen die Verifizierungslogik in Validierungs-Apps dar.**
- EU-DCC-Validierungsregeln werden auf den **Payload der Zertifikate** angewandt.
- Länder können die Business Rules **adaptieren**, die bestimmen, ob ein Zertifikat gültig ist oder nicht.

**Mindest-Prüfungen (Folie 14):**

| Feld | Prüfung |
|---|---|
| `tg` (Zielkrankheit) | COVID-19? |
| `mp` (Impfstoff) | Von der European Medicine Agency (EMA) zugelassen? |
| `dn` (Dosisnummer) | Ausreichend? (z. B. `dn ≥ sd`) |
| `dt` (Datum der Impfung) | Vor mind. 14 Tagen / nicht länger als 365 Tage? |

**Beispielregeln aus AT (Folie 20):**
- Pfizer-Impfstoff für 1 Jahr akzeptiert.
- Gültigkeit eines PCR-Tests in Österreich = 48 h.

## Bestandteile / Aufbau

| Element | Funktion | Wer pflegt? |
|---|---|---|
| Value Sets | Code → menschenlesbarer Wert | EU eHealth Network, regelmäßig aktualisiert |
| Business Rules EU | grenzüberschreitende Validierungsregeln | EU |
| Business Rules AT | nationale Validierungsregeln | Österreich |
| Anwendung | Basic Validation + Business Rules Validation in der App | Mitgliedsstaat |

## Beispiel

Aus den Folien: Eine Validator-App in Österreich prüft ein deutsches DCC mit `mp=EU/1/20/1528`. Über Value Sets wird der Code als „Comirnaty" angezeigt. Business Rules AT entscheiden: Comirnaty wird in Österreich für 1 Jahr ab Datum akzeptiert; PCR-Test wäre nur 48 h gültig (anderes Beispiel).

## Abgrenzung

- **Value Sets ≠ Business Rules:** Value Sets sind Übersetzung; Business Rules sind Logik.
- **EU-Regeln vs. AT-Regeln:** EU-Regeln gelten für Einreise zwischen Ländern (festgelegtes Ablaufdatum). AT-Regeln gelten national für Validator-Apps (z. B. Pfizer 1 Jahr).
- **Im PDF nicht ausgeführt:** Konkretes technisches Format der Business Rules (JSON-Logic, CertLogic-DSL) – relevant in der Praxis, hier nicht behandelt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind Value Sets, was sind Business Rules, und wie unterscheiden sie sich?

**Anwendungsfrage:** Welche Mindest-Prüfungen müssen mindestens auf einen DCC-Payload angewendet werden? Wo kann ein Land eigene Regeln einbringen?

**Diskussionsfrage:** Welche Folge hat es, dass jedes Land seine eigenen Business Rules adaptieren kann? Welche Trade-offs zwischen Souveränität und Interoperabilität entstehen? (Beispiel: Land A akzeptiert Pfizer für 1 Jahr, Land B für 9 Monate – ein DCC kann in einem Land gültig, im anderen ungültig sein.)

**Mögliche Anschlussfragen:**
- Was passiert, wenn ein neuer Impfstoff zugelassen wird? (Value Set wird erweitert; Business Rules werden eventuell angepasst.)
- Wer pflegt Value Sets und Business Rules zentral? (EU eHealth Network – im PDF nur indirekt erwähnt.)
- Wie werden die Regeln an Validator-Apps verteilt? ([[ASP - Gruener Pass - AT Architektur]] – via EU Gateway → AT Gateway Client.)

## Verwandt

- [[ASP - Gruener Pass - DCC-Schema]]
- [[ASP - Gruener Pass - AT Architektur]]
- [[ASP - Gruener Pass - Validator-Anforderungen]]
- [[ASP - Gruener Pass - EU Digital COVID Certificate]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folien 11, 12, 13, 14, 20
