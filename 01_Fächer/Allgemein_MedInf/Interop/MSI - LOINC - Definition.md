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

# MSI - LOINC - Definition

> [!info] Kurzdefinition
> LOINC (*Logical Observation Identifiers Names and Codes*) ist ein System zur eindeutigen Kennzeichnung von klinischen Untersuchungen, Laborwerten, anderen medizinischen Parametern und medizinischen Dokumententypen. Dient zum Austausch und Zusammenführen von (Labor-)Untersuchungsergebnissen.

## Beschreibung

Wörtlich aus Folie 21:

> „LOINC ist ein System zur eindeutigen Kennzeichnung von
> – klinischen Untersuchungen,
> – Laborwerten,
> – anderen medizinischen Parametern und
> – medizinischen Dokumententypen.
>
> Dient zum Austausch und Zusammenführen von (Labor-)Untersuchungsergebnissen.
>
> Seit 1994 entwickelt als freiwillige Initiative des Regenstrief Institutes, eine non-profit Einrichtung für medizinische Forschung an der Indiana University.
>
> Browser (frei nach Registrierung): https://search.loinc.org"

## Bestandteile / Aufbau

- **Code-Vergabe**: Jeder LOINC-Code identifiziert genau ein Konzept (präkoordiniert), z. B. `26464-8` für „Leukozyten – Anzahl­konzentration im Blut, quantitativ".
- **Sechs-Achsen-Struktur**: Component, Property, Time, System, Scale, Method – siehe [[MSI - LOINC - Sechs-Achsen-Struktur]].
- **Inhalts-Bereiche**: Laborteil + Klinischer Teil + Blutbank + Antibiotika-Empfindlichkeit + Molekulargenetik + Panels + Dokumente/Abschnitte – siehe [[MSI - LOINC - Inhalt]].
- **Pflege**: Regenstrief Institute, kontinuierliche Releases.
- **OID**: `2.16.840.1.113883.6.1` (Folie 25).

## Beispiel

Aus Folie 23:
- Code `26464-8`
- Display Name: „Leukozyten"
- LOINC-Notation: `Leukocytes : NCnc : Pt : Bld : Qn :` (Component:Property:Timing:System:Scale:Method – Method bleibt offen).

In CDA (Folie 25):
```
<code code="26464-8" codeSystem="2.16.840.1.113883.6.1"
      codeSystemName="LOINC" displayName="Leukozyten"/>
```

## Abgrenzung

- **LOINC vs. SNOMED CT**: LOINC fokussiert Mess- und Untersuchungs­identifikation („was wurde gemessen, wie, an welchem Material"), SNOMED CT ist eine Allgemein­ontologie. LOINC und SNOMED CT sind komplementär.
- **LOINC vs. UCUM**: LOINC sagt, *was* gemessen wird; UCUM sagt, in *welcher Einheit* das Ergebnis ausgedrückt wird (Folie 27: „UCUM ergänzt LOINC").
- **LOINC ≠ Befundtext**. LOINC codiert das Beobachtungs-/Frage­konzept, nicht den Wert.

## Prüfungsrelevanz

**Sehr hoch.** Klassisches Lab-Codierungs-Thema im DACH-Raum (insb. ELGA).

**Typische Definitionsfrage:** Was ist LOINC? Wofür wird es eingesetzt?

**Anwendungsfrage:** Welcher LOINC-Code würde für „Sauerstoffsättigung im arteriellen Blut" verwendet (Recherche über search.loinc.org)?

**Diskussionsfrage:** Welche Konzeptdomänen deckt LOINC ab, welche nicht? Wo grenzt es an SNOMED CT?

**Mögliche Anschlussfragen:**
- Wer pflegt LOINC?
- Welche Lizenzbedingungen hat LOINC? (im PDF nicht behandelt – im Allgemeinen kostenfrei nutzbar)
- Wie ist LOINC strukturiert? → [[MSI - LOINC - Sechs-Achsen-Struktur]]
- Wie wird LOINC in einem ELGA-Laborbefund verwendet? → [[MSI - LOINC - Verwendung in CDA]]

## Verwandt

- [[MSI - LOINC - Inhalt]]
- [[MSI - LOINC - Sechs-Achsen-Struktur]]
- [[MSI - LOINC - Fully Specified Name]]
- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - UCUM - Definition]]
- [[MSI - Terminologie - Mapping in CDA]]
- [[MSI - Ordnungssystem - Konzeptdomäne]]

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 21, 25 (OID, CDA-Beispiel)
