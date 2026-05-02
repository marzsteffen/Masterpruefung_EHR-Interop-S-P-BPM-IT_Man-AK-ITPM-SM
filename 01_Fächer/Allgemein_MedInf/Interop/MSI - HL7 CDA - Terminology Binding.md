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

# MSI - HL7 CDA - Terminology Binding

> [!info] Kurzdefinition
> In CDA-Implementierungs­leitfäden wird ein Code-Element an ein Value Set gebunden. Zwei Bindungs-Arten: **DYNAMIC** (immer die aktuell gültige Version des Value Sets ist anzuwenden) und **STATIC** (Bindung an eine bestimmte Version).

## Beschreibung

Folie 23 erklärt:

> „Was kann man sich unter Terminology Binding vorstellen?
> – **DYNAMISCHE** Bindung von Value Sets an Code-Elemente
>   – Immer die aktuell gültige Version des Value Sets ist anzuwenden
>   – Schlüsselwort ‚DYNAMIC'
> – **STATISCHE** Bindung von Value Sets
>   – Bindung an eine bestimmte Version
>   – Schlüsselwort ‚STATIC'"

Das Binding wird in den CONF-Regeln des Implementierungs­leitfadens dokumentiert. Beispiel auf Folie 23 (zeigt Konformitätsregel für `hl7:maritalStatusCode`):

> „Der Wert von @code muss gewählt werden aus dem Value Set 1.2.40.0.34.10.11 *ELGA_MaritalStatus* (DYNAMIC)"

Damit ist das Value Set über OID + Name identifiziert; das Schlüsselwort DYNAMIC sagt: „verwende immer die aktuelle Version".

## Bestandteile / Aufbau

| Binding-Typ | Verhalten | Anwendung |
|---|---|---|
| DYNAMIC | aktuelle Version des Value Sets | empfohlen für inhaltliche Value Sets, die wachsen können |
| STATIC | feste Version | für strukturelle Value Sets oder reproduzierbare Studien-Daten |

## Beispiel

Aus Folie 23 (CDA-Leitfaden-Snippet):
- Element: `hl7:maritalStatusCode`
- Datentyp: CE
- Optionalität: 0..1
- CONF: „Der Wert von @code muss gewählt werden aus dem Value Set 1.2.40.0.34.10.11 *ELGA_MaritalStatus* (DYNAMIC)"

Aus Folie 11 der VL „Terminologien Anwendung" weitere Beispiele: ELGA_AllergyOrIntoleranceAgent (`1.2.40.0.34.10.180`, DYNAMIC), ELGA_AdministrativeGender (`1.2.40.0.34.10.4`, DYNAMIC).

## Abgrenzung

- **DYNAMIC ≠ aktualisierungs­frei**: DYNAMIC heißt nicht, dass der Implementierer keine Updates pflegen muss – er muss aktiv prüfen, ob neue Codes erschienen sind. Das ist die Aufgabe der „Benutzer" laut Folie 16 (siehe [[MSI - Value Set - Eigenschaften und Wartung]]).
- **STATIC ≠ wartungs­frei**: bei einer neuen Version des Implementierungs­leitfadens kann sich auch ein STATIC-Binding ändern.
- **Terminology Binding ≠ Code System**: das Binding bestimmt das Value Set; das Code System ist die Quelle der Codes.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Was unterscheidet DYNAMIC und STATIC Terminology Binding in CDA?

**Anwendungsfrage:** Welches Binding ist für (a) Geschlecht (administrative Codes) und (b) Diagnose-Codierung sinnvoll?

**Diskussionsfrage:** Welche Risiken bringt DYNAMIC für Implementierer? Welche Vorteile?

**Mögliche Anschlussfragen:**
- Wie sieht eine CONF-Regel im CDA-Leitfaden aus?
- Wer ist verantwortlich, eine DYNAMIC-Bindung aktuell zu halten?
- Wie verhält sich Binding zur Wartung von Value Sets? → [[MSI - Value Set - Eigenschaften und Wartung]]

## Verwandt

- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[MSI - Terminologie - Value Set]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 23
