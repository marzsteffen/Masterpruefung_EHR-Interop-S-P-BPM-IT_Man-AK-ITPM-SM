---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Einführung in Standards und Interoperabilität]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Daten - Datentypen

> [!info] Kurzdefinition
> Datentyp = vorgeschriebenes Format, in dem ein Datum vorliegen muss, damit es eindeutig interpretiert werden kann. Die Vorlesung führt vier Familien an: Freitext/String, Zahl (integer oder mit Einheit), Datum/Zeitpunkt, Code.

## Beschreibung

Folie 16 listet die vier Familien:

- **Freitext (unstrukturiert), String.**
- **Zahl**:
  - „integer"
  - „mit Einheit – physical quantity"
- **Datum**: Zeitpunkt, z. B. mit Zeitzone `YYYYMMDDhhmmss+ZZzz`.
- **Codes**: Angabe von Code, Codesystem.

Als Beispiel zeigt die Folie eine Tabelle mit HL7-v2-Datentypen für PID-Felder (Set ID = SI, Patient Identifier List = CX, Patient Name = XPN, Date/Time of Birth = DTM, Administrative Sex = CWE, etc.) – ohne diese Datentypen einzeln zu definieren.

Der Verweis auf den HL7 Austria ILF (Allgemeiner Implementierungsleitfaden, Adress-Elemente) wird auf Folie 16 als externes Beispiel angegeben:
`https://wiki.hl7.at/index.php?title=ILF:Allgemeiner_Implementierungsleitfaden_(Version_3)#Adress-Elemente`

## Bestandteile / Aufbau

Vier Datentyp-Familien:

| Familie | Beispiele aus Folie | Anmerkung |
|---|---|---|
| String | Freitext | Unstrukturiert |
| Zahl | integer; physical quantity (Wert + Einheit) | Mit Einheit ist explizit gefordert |
| Datum | Zeitpunkt mit Zeitzone | Format `YYYYMMDDhhmmss+ZZzz` |
| Code | Code + Codesystem | Voraussetzung für semantische Interoperabilität |

## Beispiel

Pulswert auf Folie 14 als physical quantity (PQ):
```
<value xsi:type="PQ" value="59" unit="/min"/>
```
Codiertes Element auf Folie 14:
```
code="8867-4" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"
```

## Abgrenzung

- **String ≠ codierter Text.** Ein String-Feld kann beliebigen Freitext enthalten; ein Code-Feld erzwingt die Bindung an ein Codesystem.
- **integer ≠ physical quantity.** Eine Zahl ohne Einheit ist mehrdeutig (ist 36,7 °C oder °F?).
- **Datum-Format mit/ohne Zeitzone** ist nicht trivial – fehlende Zeitzone ist im internationalen Austausch ein typischer Fehler.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Datentyp-Familien nennt die Vorlesung?

**Anwendungsfrage:** Klassifizieren Sie folgende Felder einer ELGA-Patientensatzung: Name, Geburtsdatum, Sex, Patient-ID, Diagnose-Code.

**Diskussionsfrage:** Warum ist „integer mit Einheit" unsicher und „physical quantity" sicherer?

**Mögliche Anschlussfragen:**
- Welche HL7-v2-Datentypen kennen Sie? (PID-Tabelle aus Folie 16: SI, ST, CX, XPN, DTM, CWE)
- Wie werden Datentypen in FHIR repräsentiert? (im PDF nicht behandelt)
- Welche Rolle spielen Datentypen für Validatoren und Schemata?

## Verwandt

- [[MSI - Daten - Strukturiert vs Unstrukturiert]]
- [[MSI - Daten - Metadaten]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 16
