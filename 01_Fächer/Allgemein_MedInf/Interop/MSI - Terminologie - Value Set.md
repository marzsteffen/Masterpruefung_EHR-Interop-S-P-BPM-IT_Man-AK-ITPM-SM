---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Semantik Theorie]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologie - Value Set

> [!info] Kurzdefinition
> Wertemenge: eine eindeutig identifizierbare und versionierte Sicht auf eine oder mehrere Terminologien. Sammlung von Codes (1–n) aus 1–n Terminologien für einen konkreten Anwendungsfall.

## Beschreibung

Wörtlich aus Folie 10:

> „Value Set oder ‚Wertemenge' ist eine eindeutig identifizierbare und versionierte Sicht auf eine oder mehrere Terminologien.
> – Die Werte werden anwendungsabhängig als strukturierte Ausprägungen von Merkmalen verwendet, z. B. für die strukturierte Dokumentation, zur Speicherung in Datenbanken oder zur standardisierten Kommunikation.
> – Ein Value Set kann als Kollektion von 1-n Codes der 1-n Terminologien gesehen werden.
> – Die Spezifikation eines Value Sets wird entweder als Aufzählung (engl. enumeration) oder Definition (intentionale Beschreibung) angegeben. Ein Value Set enthält den Code selbst und die Information über die Herkunft des Codes (die Source-Terminologie)."

Das **Identifizier­bar + versioniert** ist zentral – Value Sets ändern sich, ihre Anwendung muss reproduzierbar sein.

## Bestandteile / Aufbau

- Eindeutige Identifikation des Value Sets (z. B. OID, URI).
- Version.
- Inhalt: Codes.
- Pro Code: Source-Terminologie (Code System).
- Spezifikationsart: Aufzählung (extensional) oder Definition (intentional, z. B. „alle Konzepte unterhalb eines bestimmten Knotens in SNOMED CT").

## Beispiel

Im PDF nicht ausgeführt. Klassisches Anwendungsbeispiel: ein Pflichtfeld „Geschlecht" in einem ELGA-Dokument bekommt ein Value Set vorgeschrieben mit den Codes `M`, `F`, `UN`, `UNK` aus dem HL7-Code-System für Administrative Sex. Diese Verbindung an konkrete Codes für eine konkrete Domäne ist das, was ein Value Set leistet.

## Abgrenzung

- **Value Set vs. Code System**: Code System ist die Quelle (Sammlung der Codes mit Regeln); Value Set ist eine versionierte Auswahl daraus für einen Anwendungsfall.
- **Value Set vs. Konzeptdomäne**: die Konzeptdomäne ist abstrakt („Diagnosen"), das Value Set ist die konkrete Code-Liste, die in einem Implementierungsleitfaden festgelegt wurde.
- **Value Set ≠ Terminologie**: ein Value Set kann Codes aus mehreren Terminologien kombinieren.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Value Set, und worin unterscheidet es sich von einem Code System?

**Anwendungsfrage:** Geben Sie ein Beispiel, in dem ein Value Set Codes aus mehreren Terminologien kombiniert.

**Diskussionsfrage:** Warum ist die Versionierung eines Value Sets entscheidend für reproduzierbare klinische Daten?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen einer extensionalen und einer intentionalen Value-Set-Definition?
- Wie wird ein Value Set in FHIR repräsentiert? (FHIR ValueSet-Resource – im PDF nicht definiert.)
- Welche Rolle spielen Value Sets in ELGA-Implementierungs­leitfäden? (siehe termgit.elga.gv.at, Folie 27.)

## Verwandt

- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Definition]]
- [[MSI - Ordnungssystem - Konzeptdomäne]]
- [[MSI - Terminologie - Referenz vs Interface Terminologie]]

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]]
- Folien/Seitenangabe: 10
