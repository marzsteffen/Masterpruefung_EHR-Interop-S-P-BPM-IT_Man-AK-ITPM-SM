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

# MSI - HL7 CDA - Codierte Werte

> [!info] Kurzdefinition
> Drei Varianten für codierte Werte in CDA: (1) **Minimal** = `code` + `codeSystem`. (2) **Gebräuchlich** = zusätzlich `displayName` + `codeSystemName`. (3) **Vollständig** = zusätzlich `codeSystemVersion` + `originalText` (mit reference auf Narrative).

## Beschreibung

Folie 21 zeigt die drei Codierungs-Varianten:

**B.2.2.1.1.1 Minimal-Variante**, um einen Code eindeutig darzustellen:
```xml
<code code="E10" codeSystem="1.2.40.0.34.5.56"/>
```

**B.2.2.1.1.2 Gebräuchlichste Variante** mit zusätzlichem Klartext für Code und Codesystem:
```xml
<code code="E10"
      displayName="Primär insulinabhängiger Diabetes mellitus, Typ-2-Diabetes"
      codeSystem="1.2.40.0.34.5.56"
      codeSystemName="ICD-10 BMG 2014"/>
```

**B.2.2.1.1.3 Vollständige Variante** mit direkter Angabe des Textinhalts:
```xml
<code code="E10"
      displayName="Primär insulinabhängiger Diabetes mellitus, Typ-2-Diabetes"
      codeSystem="1.2.40.0.34.5.56"
      codeSystemName="ICD-10 BMG 2014"
      codeSystemVersion="1.00">
  <originalText>Diabetes mellitus Typ 2</originalText>
</code>
```

Weitere Beispiele aus Folie 21:
- `<code code="1592830" displayName="Ciproxin" codeSystem="1.2.40.0.34.4.16" codeSystemName="Pharmazentralnummer"/>` – Arzneimittel via PZN.
- `<code code="8867-4" displayName="Heart Beat" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"><originalText><reference value="#vitsigtype1"/></originalText></code>` – LOINC-Code mit Reference auf Narrative.
- `<code code="11490-0" displayName="Physician Discharge summary" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>` – Dokumenten­klasse.
- `<code code="48765-2" displayName="Allergies, adverse reactions, alerts" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>` – Section-Code.

Folie 22 ergänzt die Struktur eines codierten Werts mit getrennten code- und value-Elementen am Beispiel Tabakkonsum (Patient Summary Lebensstil-Section):
- `hl7:code` mit Datentyp CE (extensible), F (Fixed), Code `229819007` (SNOMED Tobacco use and exposure (observable entity)), codeSystem `2.16.840.1.113883.6.96` (SNOMED Clinical Terms).
- `hl7:value` mit DT CD, codiert aus Value Set `1.2.40.0.34.10.204 ELGA_CurrentSmokingStatus (DYNAMIC)`.

## Bestandteile / Aufbau

| Variante | Pflichtattribute | Optional-/Zusatzattribute | Wann verwenden? |
|---|---|---|---|
| Minimal | code, codeSystem | – | Nur wenn Empfänger das Code-System kennt |
| Gebräuchlich | + displayName, codeSystemName | – | Standard im ELGA-CDA |
| Vollständig | + codeSystemVersion, originalText | reference im originalText | Wenn Versionierung und Narrative-Verlinkung wichtig |

## Beispiel

Aus Folie 21: ICD-10-Diabetes-Beispiel in allen drei Varianten (siehe oben). Aus Folie 22: SNOMED-Tabakkonsum-Beispiel mit code/value-Trennung.

## Abgrenzung

- **`code`-Element ≠ `value`-Element**: `code` qualifiziert die Beobachtung („Was wurde beobachtet?"), `value` enthält das Resultat („Welches Ergebnis?"). Bei Lab: code = LOINC-Test, value = der Messwert. Bei codiertem Resultat (z. B. Tabakkonsum): code = die Frage, value = die codierte Antwort.
- **`displayName` ≠ `originalText`**: displayName ist der vorgegebene Anzeige­name aus dem Code System; originalText ist der Text, den der Anwender eingegeben hat / der im Narrative steht.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche drei Varianten gibt es, einen Code in CDA anzugeben? Welche Attribute trägt jede?

**Anwendungsfrage:** Welche Variante ist im ELGA-CDA Standard? Welche Variante würden Sie wählen, wenn die Versionsnummer der Terminologie kritisch ist?

**Diskussionsfrage:** Warum gibt es `code` *und* `value` – warum nicht ein einziges Attribut? (Antwort: Trennung von Frage und Antwort.)

**Mögliche Anschlussfragen:**
- Wozu dient `originalText`?
- Wann wird `<reference value="#…"/>` verwendet?
- Welche Datentypen passen zu codierten Elementen? → [[MSI - HL7 CDA - Datentypen]] (CNE/CWE)

## Verwandt

- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - HL7 CDA - Terminology Binding]]
- [[MSI - HL7 CDA - Translation]]
- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Identifikator - OID]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 21, 22
