---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - IHE XDS - Dokument-Metadaten

> [!info] Kurzdefinition
> Beim „Einbringen" eines CDA-Dokuments in IHE XDS müssen Registrierungsdaten (Metadaten) bereitgestellt werden. Sie leiten sich teilweise direkt aus dem CDA-Header ab. ELGA spezifiziert die wichtigsten in einem eigenen XDS-Metadaten-Leitfaden.

## Beschreibung

Folie 35: „Beim ‚Einbringen' von CDA Dokumenten müssen Registrierungsdaten bereitgestellt werden. Teilweise leiten sich diese Daten direkt aus den CDA-Metadaten ab. Details siehe eigener XDS-Metadaten Leitfaden."

Folie 36 listet die wichtigsten ELGA-XDS-Dokument-Metadaten:

| Art der Information | Vorkommen | Beispiel für Inhalte |
|---|---|---|
| **Autor** (Verfasser) | Immer | Dr. Herbert Mustermann |
| **Organisation des Autors** | Immer | Amadeus Spital - Chirurgie, Mozartgasse 1-7, 1234 St. Wolfgang |
| **Art der Organisation** | Immer, codiert | „Abteilung", „Ambulante Erstversorgung", … |
| **Rolle des Autors** | Sofern bekannt | „Primar", „Abteilungsleiter" (Freitext) |
| **Funktionscode** | Sofern bekannt, codiert | „Fachärztin/Facharzt für Chirurgie", „… für Thoraxchirurgie" |
| **Rechtlicher Unterzeichner** | Immer | Dr. Herbert Mustermann |
| **Erstellungsdatum** | Immer | 2012-08-16 13:20:41 Zeitzone GMT+1 |
| **Gesundheitsdienstleistung** | Optional, codiert | „Gesundheitsdienstleistung i. R. eines stationären Aufenthalts", „Tumormarker", „Toxikologie", „Harndiagnostik" – APPC |
| **Start und Ende der Gesundheitsdienstleistung** | Sofern bekannt | Von 2012-08-14 08:22:20 bis 2012-08-16 12:02:54 GMT+1 |
| **Patientendaten** | Immer | Name, Geburtsdatum, Geschlecht, Adresse zum Zeitpunkt der Dokumenterstellung |
| **Titel des Dokuments** | Immer | „Ultraschalldiagnostik des Abdomens", „Klin.Chem. Laborbefund" |
| **Dokumentenklasse** | Immer, codiert | „Entlassungsbrief", „Laborbefund", „Befund bildgebende Diagnostik" |
| **Dokumententyp** | Immer, codiert | „Entlassungsbrief Ärztlich", „Nuklearmedizinischer Befund", „Echokardiographie-Befund", „Endoskopie-Befund" |
| **Fachrichtung d. Dok.** | Immer, codiert | „Chirurgie", „Herzchirurgie", „Labordiagnostik", „Unfallchirurgie" |
| **Gültigkeit** | Immer, codiert | „Approved", „Deprecated" |
| **ELGA Interoperabilitätsstufe** | Immer, codiert | „EIS Enhanced" |

## Bestandteile / Aufbau

Vier funktionale Cluster:
1. **Wer**: Autor + Organisation + Rolle + Funktionscode + rechtlicher Unterzeichner.
2. **Wann**: Erstellungsdatum + Gesundheitsdienstleistungs-Zeitraum.
3. **Wer (Patient)**: Patientendaten.
4. **Was/Wie**: Titel, Dokumentenklasse, Dokumententyp, Fachrichtung, Gültigkeit, EIS-Stufe.

## Beispiel

Aus der Tabelle (Folie 36): Ein Entlassungsbrief Chirurgie hat als Metadaten z. B. „Entlassungsbrief" (Dokumentenklasse), „Entlassungsbrief Ärztlich" (Dokumententyp), „Chirurgie" (Fachrichtung), „EIS Enhanced" (Interoperabilitäts­stufe), „Approved" (Gültigkeit).

## Abgrenzung

- **XDS-Metadaten ≠ CDA-Header**: viele XDS-Metadaten leiten sich aus dem CDA-Header ab, sind aber separat in der Registry geführt – Suche läuft über die XDS-Metadaten, nicht über den CDA-Inhalt.
- **Dokumentenklasse ≠ Dokumententyp**: Klasse ist die übergeordnete Kategorie (Entlassungsbrief), Typ ist die feinere Unterkategorie (Entlassungsbrief Ärztlich vs. Pflege).
- **EIS-Stufe in XDS ≠ EIS-Stufe als CDA-Eigenschaft**: in XDS wird die EIS-Stufe als Metadatum geführt, damit Konsumenten filtern können.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche XDS-Metadaten muss ein ELGA-Dokument tragen?

**Anwendungsfrage:** Welche Filtermöglichkeiten ergeben sich aus den XDS-Metadaten? (Folie 27 zeigt das ELGA-Portal mit Filtern wie Erstellende Organisation, Quellen, Erstellungsdatum, Fachrichtung, Dokument, APPC-Code.)

**Diskussionsfrage:** Warum wird die EIS-Stufe als XDS-Metadatum geführt? Welcher Use Case wird damit unterstützt?

**Mögliche Anschlussfragen:**
- Welche Codesystem-Quellen nutzen die codierten Metadaten? (Hauptsächlich ELGA-eigene Value Sets, APPC für Gesundheitsdienstleistung.)
- Wie verhält sich „Rolle" (Freitext) zu „Funktionscode" (codiert)?
- Was bedeutet „Approved" vs. „Deprecated" in der Gültigkeit?

## Verwandt

- [[MSI - IHE XDS - Architektur]]
- [[MSI - HL7 CDA - Header]]
- [[MSI - ELGA - EIS Stufen]]
- [[MSI - Daten - Metadaten]]
- [[MSI - LOINC - Verwendung in CDA]] (Dokument-Codes)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 27 (Filter-Beispiel), 35, 36
