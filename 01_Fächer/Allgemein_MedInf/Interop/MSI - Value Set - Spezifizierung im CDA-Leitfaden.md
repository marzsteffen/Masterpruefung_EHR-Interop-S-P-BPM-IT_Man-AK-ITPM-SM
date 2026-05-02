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

# MSI - Value Set - Spezifizierung im CDA-Leitfaden

> [!info] Kurzdefinition
> In einem CDA-Implementierungs­leitfaden wird das **Value Set Binding** über Konformitäts­regeln (CONF-Statements) ausgedrückt: pro Element wird auf das Value Set verwiesen (mit eindeutigem Namen + OID + DYNAMIC/STATIC), das die mögliche Werteauswahl festlegt.

## Beschreibung

Folie 11 zeigt drei konkrete CDA-Bindings (Auszug aus einem CDA-Leitfaden):

| Element | Datentyp | Optionalität | CONF-Regel |
|---|---|---|---|
| `hl7:playingEntity/hl7:code` (Allergie­auslöser) | CE (extensible) | – | „Der Wert von @code sollte gewählt werden aus dem Value Set `1.2.40.0.34.10.180` *ELGA_AllergyOrIntoleranceAgent* (DYNAMIC)" |
| `hl7:administrativeGenderCode` | CE | 1..1 R | „Der Wert von @code muss gewählt werden aus dem Value Set `1.2.40.0.34.10.4` *ELGA_AdministrativeGender* (DYNAMIC). Zugelassene nullFlavor: UNK" |
| `hl7:maritalStatusCode` | CE | 0..1 | „Der Wert von @code muss gewählt werden aus dem Value Set `1.2.40.0.34.10.11` *ELGA_MaritalStatus* (DYNAMIC)" |

Schlüssel-Beobachtungen:
- **Verbindlich­keit** wird durch „muss"/„sollte" + Optionalitäts-Cardinality (`R`/optional) ausgedrückt.
- **Value Set** wird mit eindeutigem Namen UND OID benannt.
- **DYNAMIC** kennzeichnet das Value Set als änderbar; STATIC wäre eingefroren.
- **nullFlavor**: zugelassene Codes für „kein Wert" (z. B. `UNK` für unbekannt).

## Bestandteile / Aufbau

Ein Value Set Binding im CDA-Leitfaden enthält pro Element:
1. **Element-Pfad** (z. B. `hl7:administrativeGenderCode`).
2. **Datentyp** (z. B. CE = Coded with Equivalents).
3. **Optionalität / Cardinality** (z. B. `1..1 R` = required).
4. **CONF-Regel** mit Verbindlichkeit (sollte/muss), OID + Name des Value Sets, DYNAMIC/STATIC, optional zugelassene nullFlavors.

## Beispiel

Aus Folie 11 (Geschlechts-Codierung):
> „Der Wert von @code muss gewählt werden aus dem Value Set 1.2.40.0.34.10.4 ELGA_AdministrativeGender (DYNAMIC). Zugelassene nullFlavor: UNK"

Wenn ein Patient kein bekanntes Geschlecht hat, kann statt eines Codes die nullFlavor `UNK` verwendet werden – ohne dass das CDA-Dokument schema-invalide wird.

## Abgrenzung

- **CONF „muss" vs. „sollte"**: muss = Pflicht; sollte = Empfehlung. Beide referenzieren das Value Set, aber die Strenge der Validierung unterscheidet sich.
- **DYNAMIC vs. STATIC Binding**: DYNAMIC erlaubt zukünftige Erweiterungen des Value Sets, STATIC nicht.
- **nullFlavor ≠ leerer Wert**: nullFlavor codiert den Grund für die Abwesenheit (UNK = unknown, NA = not applicable, NI = no information …).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie wird in einem CDA-Leitfaden auf ein Value Set verwiesen? Welche Bestandteile hat eine CONF-Regel?

**Anwendungsfrage:** Lesen Sie das Binding für `hl7:administrativeGenderCode` und erklären Sie: Welcher Code kommt aus welchem Value Set? Was bedeutet UNK?

**Diskussionsfrage:** Warum wird DYNAMIC verwendet? Welche Risiken hat das für Implementierer?

**Mögliche Anschlussfragen:**
- Was ist eine nullFlavor und wie wird sie verwendet?
- Welche Datentypen kennt CDA für codierte Elemente? (CE, CD, CV, CO …)
- Wie unterscheiden sich CDA-Bindings von FHIR-Bindings (Required, Extensible, Preferred, Example)?

## Verwandt

- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Identifikator - OID]]
- [[MSI - HL7 CDA - Header]] (Querverweis Vorlesung 04 – noch nicht definiert)

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 11, 12
