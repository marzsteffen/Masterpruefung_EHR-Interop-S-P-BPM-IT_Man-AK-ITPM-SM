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

# MSI - HL7 CDA - Kardinalität und Konformität

> [!info] Kurzdefinition
> Implementierungs­leitfäden definieren pro Element **Kardinalität** (z. B. `1..1`, `0..*`) und **Optionalität/Konformität** in den Stufen **M (Mandatory), R (Required), O (Optional)**, ergänzt durch IHE-typische Wörter „shall, should, may" und „must support". Daneben werden Datentyp, Terminology Binding, Referenzen, Basis-Standard und Status angegeben.

## Beschreibung

Wörtlich aus Folie 42:

> „Kardinalität und Optionalität
> – M, R, O, aber auch ‚shall, should, may' (‚IHE uses the normative words Shall, Should, and May according to standards conventions')
> – ‚must support' – Was könnte das bedeuten?
> – siehe auch: ILF:Allgemeiner Implementierungsleitfaden (Version 3) - Allgemeiner Implementierungsleitfaden (Version 3) (hl7.at)"

Weitere Aspekte aus Folie 42:
- **Datentypen** – siehe [[MSI - HL7 CDA - Datentypen]].
- **Terminology Binding** – siehe [[MSI - HL7 CDA - Terminology Binding]].
- **Referenzen auf andere Leitfäden** – z. B. Allgemeiner Leitfaden vs. spezielle Leitfäden.
- **Basis-Standard**: z. B. HL7 CDA.
- **Status**, z. B. Trial Implementation oder Maturity Level in FHIR.

Folie 43 stellt drei Diskussionsfragen:
- Wie wird ein neuer CDA-Leitfaden erstellt?
  - Wie kann man „Richtigkeit" und Praxistauglichkeit sicherstellen?
  - Wie kann Akzeptanz hergestellt werden?
- Wie können Standards verbindlich werden?
  - Wie kann die Umsetzung eines Implementierungsleitfadens verpflichtend gemacht werden?
  - Wie kann die Umsetzung in der Praxis geprüft werden?

> Hinweis Quelltreue: Die Folie liefert nicht eine Definition von „must support", sondern stellt die Frage offen. Standardlehrmeinung (außerhalb des PDFs): „must support" verlangt von einer empfangenden Anwendung, dass sie das Element verarbeiten *kann*, ohne es zwingend anzuzeigen.

## Bestandteile / Aufbau

| Optionalität-Code | Bedeutung |
|---|---|
| **M** | Mandatory – Pflicht |
| **R** | Required – erforderlich |
| **R2** | Required if known/applicable |
| **O** | Optional |
| **shall** | normativ verpflichtend (IHE) |
| **should** | empfohlen (IHE) |
| **may** | erlaubt (IHE) |
| **must support** | empfangsseitig verarbeitbar (offen, siehe Hinweis) |

## Beispiel

Aus den ELGA-Bindings auf Folie 11 von VL „Terminologien Anwendung": `hl7:administrativeGenderCode` mit Datentyp CE, Kardinalität `1..1 R` – ein Pflichtfeld mit genau einem Wert.

Aus Folie 13 ELGA-Entlassungsbrief: Sektion „Aufnahmegrund" trägt `[M]`, „Allergien, Unverträglichkeiten und Risiken" trägt `[R2]` (required if known), „Anamnese" trägt `[O]`.

## Abgrenzung

- **M ≠ shall**: M ist die ELGA/HL7-Notation, shall die IHE-Notation. Inhaltlich vergleichbar, aber Quellen unterschiedlich.
- **R vs. R2**: R = required, R2 = required if applicable/known. R2 ist kein „weicher" R, sondern bedeutet „muss erscheinen, wenn die Information verfügbar ist".
- **must support ≠ Pflicht zur Anzeige**: must support fordert Verarbeitbarkeit, nicht Anzeige. Empfänger muss z. B. das Element parsen können, auch wenn er es nicht im UI anzeigt.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Welche Optionalitäts-Codes verwendet ELGA in seinen Leitfäden? Wie unterscheiden sie sich?

**Anwendungsfrage:** Was bedeutet `1..1 R` für ein Element? Was `0..* O`?

**Diskussionsfrage:** Was könnte „must support" bedeuten? (siehe Folie 42 als Diskussionsanker)

**Mögliche Anschlussfragen:**
- Wie hängen Kardinalität und Optionalität zusammen?
- Welche IHE-Konventionen gibt es zu shall/should/may?
- Wie wird Konformität in einem Schematron geprüft? → [[MSI - HL7 CDA - Stylesheet und Validierung]]

## Verwandt

- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - HL7 CDA - Terminology Binding]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 42, 43
