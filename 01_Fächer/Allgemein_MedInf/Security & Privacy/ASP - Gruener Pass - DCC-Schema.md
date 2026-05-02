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

# ASP - Grüner Pass - DCC-Schema (JSON-Datenformat)

> [!info] Kurzdefinition
> Das Digital COVID Certificate (DCC) repräsentiert die Zertifikatsdaten als JSON mit definiertem Schema. Pflichtfelder: Schema-Version, Personendaten (Name, Geburtsdatum) und ein Block für Vaccination/Test/Recovery.

## Beschreibung

Folie 10 zeigt das DCC-Format:

- DCC stellt Daten im **JSON-Format** dar (Schlüssel-Werte-Paare).
- Auf JSON basierendes Zertifikatsschema zur Unterstützung der Serialisierung und Deserialisierung der DCC-Nutzdaten.
- Schema unterstützt die Konformität mit der EU-Gesetzgebung in Bezug darauf, was in einem Zertifikat dargestellt werden soll.

**Beispiel-Struktur (Folie 10):**

```json
{
  "ver": "1.2.1",
  "nam": {
    "fn": "Musterfrau-Gößfinger",
    "gn": "Gabriele",
    "fnt": "MUSTERFRAU<GOESSINGER",
    "gnt": "GABRIELE"
  },
  "dob": "1998-02-26",
  "v": [
    {
      "tg": "840539006",
      "vp": "1119349007",
      "mp": "EU/1/20/1528",
      "ma": "ORG-100030215",
      "dn": 1,
      "sd": 2,
      "dt": "2021-02-18",
      "co": "AT",
      "is": "Ministry of Health, Austria",
      "ci": "URN:UVCI:01:AT:10807843F94AEE0EE5093FBC254BD813#B"
    }
  ]
}
```

**Felder (vollständige Bedeutung laut Folie 13/14):**

| Feld | Bedeutung |
|---|---|
| `ver` | Version des JSON-Schemas für den DCC |
| `nam` | Namens-Block (fn = full name, gn = given name, fnt/gnt = transliteriert für Reisepass-Format) |
| `dob` | Date of Birth |
| `v` | Vaccination-Block (Array) |
| `tg` | Code für die **Zielkrankheit** |
| `vp` | Vaccine Prophylaxis (Impfstoff-Typ) |
| `mp` | Code für den verwendeten **Impfstoff** (Medical Product) |
| `ma` | Code für den **Hersteller** (Manufacturer) |
| `dn` | **Dosisnummer** (z. B. 1, 2) |
| `sd` | Anzahl der erforderlichen Dosen für diesen Impfstoff (Standard Doses) |
| `dt` | Datum der Impfung (Date) |
| `co` | Country (z. B. „AT") |
| `is` | Issuer |
| `ci` | Certificate Identifier (Unique Vaccination Certificate Identifier) |

Analoge Blöcke gibt es für `t` (Test) und `r` (Recovery).

## Bestandteile / Aufbau

JSON ist hierarchisch aufgebaut. Die obersten Felder beschreiben Person und Schema-Version; ein Array für Vaccination/Test/Recovery enthält jeweils einen oder mehrere Eintrags-Blöcke. Codes (z. B. EU-Arzneimittelzulassung) werden über Value Sets aufgelöst (siehe [[ASP - Gruener Pass - Value Sets und Business Rules]]).

## Beispiel

Folie 13: zweite Impfung mit BioNTech/Pfizer. Felder: `dn=2`, `sd=2` (zwei von zwei nötigen Dosen), `mp=EU/1/20/1528` (Comirnaty), `dt=2021-02-18`.

## Abgrenzung

- **JSON-Schema ≠ JSON-Daten:** Das Schema definiert Struktur und erlaubte Werte; die konkreten Daten passen sich an. Die Vorlesung zeigt nur Daten-Beispiele, kein Schema-Snippet.
- **DCC ist nicht klassisch X.509:** Das Format der Nutzdaten ist JSON; die *Signatur* erfolgt über CBOR / COSE / CWT (im PDF nicht ausdrücklich genannt). Im PDF wird die Signatur konzeptionell auf der Folie 6 erwähnt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welches Datenformat verwendet das DCC? Welche Pflichtfelder enthält es?

**Anwendungsfrage:** Lesen Sie ein gegebenes DCC-JSON: Welche Person ist gemeint, welcher Impfstoff, welcher Dosisstand?

**Diskussionsfrage:** Warum verwendet das DCC-Schema kurze, kryptische Schlüssel (z. B. `dn`, `sd`, `mp`)? (Antwort: QR-Codes haben begrenzte Datenkapazität; je kürzer die Felder, desto kürzer der QR-Code.)

**Mögliche Anschlussfragen:**
- Wofür dient die `ci` (Certificate Identifier)? (Eindeutige Identifikation, ggf. für Sperrlisten – im PDF nicht detailliert.)
- Wie wird aus dem Code `EU/1/20/1528` der Klartext „Comirnaty"? ([[ASP - Gruener Pass - Value Sets und Business Rules]])
- Was sagt `tg = 840539006` aus? (Code für COVID-19 nach SNOMED-CT – im PDF nicht ausgeführt.)

## Verwandt

- [[ASP - Gruener Pass - EU Digital COVID Certificate]]
- [[ASP - Gruener Pass - Value Sets und Business Rules]]
- [[ASP - Gruener Pass - AT Architektur]]
- [[ASP - DSGVO - Grundsaetze]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folien 10, 13, 14
