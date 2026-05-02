---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Terminologien Anwendung]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Identifikator - Übersicht eHealth

> [!info] Kurzdefinition
> Im eHealth-Umfeld werden zahlreiche Identifikator-Systeme parallel genutzt: Patientenindex, GDA-Index („Health Provider Directory"), OID, Dokumenten-ID + Versionsnummer, Zulassungsnummer, Pharma-Zentral-Nummer, IDMP, Ländercodes, bPK-GH u. v. m.

## Beschreibung

Folie 6 listet die wichtigsten Identifikator-Systeme:

- **Patientenindex** – Master Patient Index für die eindeutige Patient*innen-Identifikation.
- **GDA-Index** („Health Provider Directory") – Verzeichnis der Gesundheitsdiensteanbieter.
- **OID** (Object Identifier) – siehe [[MSI - Identifikator - OID]].
- **Dokumenten-ID, Versionsnummer …** – pro Dokument eindeutige ID + Version.
- **Zulassungsnummer** – z. B. für Arzneimittel.
- **Pharma-Zentral-Nummer (PZN)** – Identifikation einzelner Arzneimittel-Packungen.
- **IDMP** – Identification of Medical Products (internationaler ISO-Standard).
- **Ländercodes** – z. B. ISO 3166.
- **bPK-GH** – bereichs­spezifisches Personenkennzeichen Gesundheit (Österreich-spezifisch).
- „… und viele weitere".

> Hinweis Quelltreue: Die Folie listet die Systeme nur, definiert sie aber nicht im Detail. Insbesondere die genaue Funktion von bPK-GH, MPI und IDMP wird nicht ausgeführt.

## Bestandteile / Aufbau

| Identifikator | Identifiziert | Quelle |
|---|---|---|
| Patientenindex / MPI | Personen | nationale/regionale Implementierung |
| GDA-Index | Gesundheitsdiensteanbieter | nationaler Index |
| OID | Code System, Value Set, Template … | ISO/IEC 9834 |
| Dokumenten-ID + Version | einzelnes Dokument | pro Aussteller |
| Zulassungsnummer | Arzneimittel-Zulassung | Behörde |
| PZN | Arzneimittel-Packung | Pharma-Zentralnummer |
| IDMP | Medizinprodukt international | ISO-Standard |
| Ländercodes | Staat | ISO 3166 |
| bPK-GH | Person im Bereich Gesundheit | Österreich |

## Beispiel

In einem ELGA-CDA-Dokument können gleichzeitig auftauchen:
- Patient identifiziert über bPK-GH und/oder MPI.
- Aussteller identifiziert über GDA-Index-Eintrag.
- Dokument selbst hat eine Dokumenten-ID + Versionsnummer.
- Inhalts-Codes referenzieren via OIDs auf LOINC, APPC, ELGA-Value-Sets.
- Medikamente identifiziert via PZN bzw. zukünftig IDMP.

## Abgrenzung

- **MPI ≠ bPK-GH**: MPI ist eine technische Architektur, bPK-GH ein konkretes österreichisches Personen­kennzeichen.
- **OID ≠ Dokument-ID**: OID identifiziert *Klassen* von Dingen (Code System, Template); Dokument-ID identifiziert *Instanzen*.
- **PZN ≠ IDMP**: PZN ist national (DACH), IDMP ist international (ISO).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Identifikator-Systeme werden im österreichischen eHealth-Umfeld verwendet?

**Anwendungsfrage:** Welcher Identifikator identifiziert wen oder was in einem ELGA-CDA-Dokument?

**Diskussionsfrage:** Warum braucht ein eHealth-System mehrere Identifikator-Systeme parallel? Welche Konsistenz­probleme entstehen daraus?

**Mögliche Anschlussfragen:**
- Was ist ein MPI (Master Patient Index) konkret? (im PDF nicht definiert)
- Wie verhält sich die bPK-GH zur SVNR? (im PDF nicht behandelt)
- Welche Rolle spielt IDMP im internationalen Arzneimittel­austausch?

## Verwandt

- [[MSI - Identifikator - OID]]
- [[MSI - Interoperabilität - Voraussetzungen]] (eindeutige Identifikation als Voraussetzung)
- [[EHR - ELGA - Architektur]] (MPI, GDA-Index als ELGA-Bausteine)

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 6
