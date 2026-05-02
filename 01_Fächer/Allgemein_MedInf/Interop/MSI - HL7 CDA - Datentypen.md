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

# MSI - HL7 CDA - Datentypen

> [!info] Kurzdefinition
> Übersicht der Datentypen, die in CDA verwendet werden: Zeichenketten (ST), Identifikatoren (II), codierte Elemente (CNE/CWE), Zeit­elemente (TS.DATE/IVL_TS), Kontaktdaten (TEL), Namen (PN), Messwerte (PQ/IVL_PQ/INT/IVL_INT), zusammengesetzte Elemente (Adresse).

## Beschreibung

Folie 17 listet:

- **Zeichenketten**: ST.
- **ID-Elemente**: Instance Identifier (II) – siehe [[MSI - HL7 CDA - II Instance Identifier]].
- **Codierte Elemente**: CNE (*Coded with No Exceptions*) und CWE (*Coded with Exceptions*).
- **Zeitelemente**: TS.DATE (Zeitstempel), IVL_TS (Zeitintervall).
- **Kontaktdaten-Elemente**: TEL.
- **Namen-Elemente**: PN (Person Name).
- **Messwert-Elemente**: PQ (Physical Quantity – Wert + Einheit), IVL_PQ (Physical-Quantity-Intervall), INT (Integer), IVL_INT (Integer-Intervall).
- **Komplexe, zusammengesetzte Elemente**: Adresse.

Die Folie verlinkt für Details:
- ELGA Allgemeiner Implementierungsleitfaden (Datentypen-Sektion): `https://wiki.hl7.at/index.php?title=ILF:Allgemeiner_Implementierungsleitfaden_2020#Datentypen`
- HL7 V3 Datentypen R2: `http://www.hl7.org/documentcenter/private/standards/v3/edition_web/infrastructure/datatypes_r2/datatypes_r2.html`

## Bestandteile / Aufbau

| Datentyp | Bedeutung | Beispiel |
|---|---|---|
| ST | String | Freitext |
| II | Instance Identifier | OID + extension |
| CNE | Coded with No Exceptions | strikt aus Value Set |
| CWE | Coded with Exceptions | aus Value Set, mit Möglichkeit für Translation |
| TS.DATE | Datum | `20121201` |
| IVL_TS | Zeitintervall | low/high |
| TEL | Telekom-Kontakt | `tel:+43-…` |
| PN | Person Name | given/family/prefix/suffix |
| PQ | Physical Quantity | `value + unit (UCUM)` |
| IVL_PQ | PQ-Intervall | low/high mit Einheit |
| INT | Integer | ganzzahlig |
| IVL_INT | Integer-Intervall | low/high |
| AD | Adresse | streetName/houseNumber/postalCode/city |

## Beispiel

Aus Folie 25 (Lab-Observation):
- `<value xsi:type="PQ" value="26" unit="G/L"/>` – PQ.
- `<low value="4.0" unit="G/L"/> <high value="10.0" unit="G/L"/>` als Teil von `<value xsi:type="IVL_PQ">` – IVL_PQ.
- `<effectiveTime value="20121201073406+0100"/>` – TS.

Aus Folie 10 (legalAuthenticator):
- `<addr><streetName>Auenbruggerplatz</streetName><houseNumber>15</houseNumber><postalCode>8036</postalCode><city>Graz</city></addr>` – AD.
- `<telecom value="tel:+43-316-385.2544"/>` – TEL.

## Abgrenzung

- **CNE vs. CWE**: CNE erlaubt nur Codes aus dem definierten Value Set (No Exceptions). CWE erlaubt Codes außerhalb mittels Translation und nullFlavor OTH (With Exceptions).
- **PQ ≠ INT**: PQ ist eine physikalische Größe (Wert + Einheit), INT eine reine Ganzzahl ohne Einheit.
- **TS.DATE ≠ IVL_TS**: TS ist ein einzelner Zeitstempel, IVL_TS ein Intervall mit low/high.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Welche Datentypen kennt CDA für codierte Elemente und Messwerte?

**Anwendungsfrage:** Welcher Datentyp passt zu (a) Pulswert, (b) Patientenname, (c) ICD-Code, (d) Geburtsdatum?

**Diskussionsfrage:** Worin liegt der praktische Unterschied zwischen CNE und CWE für die Implementierung?

**Mögliche Anschlussfragen:**
- Wie verhält sich PQ zu UCUM? → [[MSI - UCUM - Definition]]
- Wie sieht eine Translation in CWE konkret aus? → [[MSI - HL7 CDA - Translation]]
- Welche Datentypen verlangen welche Pflichtattribute?

## Verwandt

- [[MSI - HL7 CDA - II Instance Identifier]]
- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - Translation]]
- [[MSI - UCUM - Definition]]
- [[MSI - Daten - Datentypen]] (allgemein, VL 01)

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 17
