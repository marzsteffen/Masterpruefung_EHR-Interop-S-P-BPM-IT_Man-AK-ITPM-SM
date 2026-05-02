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

# MSI - Interoperabilität - Herausforderungen

> [!info] Kurzdefinition
> „Interoperability is hard": Vier Kategorien von Gründen, warum Interoperabilität in der Praxis schwer bleibt – Bit-perfect-Anforderung, Translation Issues, Developer-Welten, User-Welten. Nach Benson/Grieve.

## Beschreibung

Folie 24 fasst die Gründe als Mindmap zusammen (Quelle: Benson and Grieve, *Principles of Health Interoperability*).

**Bit-perfect**
- Computers work by matching strings.
- Need for perfection.
- Specifications must be stringent.

**Translation issues**
- Computers store data in different ways.
- Double translation (A → wire format, wire format → B).
- Need for a standard interchange language that all systems can use.

**Developers**
- Each system speaks its own language.
- Managers wish to re-use existing software.
- Lack domain knowledge.
- Developers and users fail to understand each other.

**Users**
- Each specialty speaks its own dialect.
- Users do not know what they really want.
- Users won't commit to requirements.
- Users keep asking for changes.
- Users do not understand software development.

## Bestandteile / Aufbau

Vier orthogonale Problemfelder, die gleichzeitig auftreten – kein einziges davon wird durch ein einzelnes Standard-Werk gelöst.

## Beispiel

Die Vorlesung verzichtet auf eigene Beispiele, verweist aber implizit auf das Diskussionsbeispiel der Terminvergabe (Folie 21) und auf den ÖÄK-Zitat „PDF-Müllhalde" (Folie 25), der zeigt, wie man trotz Standards in einem Suboptimum landen kann.

## Abgrenzung

- Diese Sammlung adressiert *strukturelle* Hürden – sie überlappt mit, ist aber unabhängig von, fehlender [[MSI - Interoperabilität - Voraussetzungen|Voraussetzung]] (z. B. fehlender Terminologie). Selbst mit allen Voraussetzungen erfüllt sind die vier Hindernisse weiter aktiv.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Kategorien von Gründen nennt Benson/Grieve dafür, dass Interoperabilität schwer ist?

**Anwendungsfrage:** Beschreiben Sie ein konkretes Projekt-Szenario, in dem alle vier Kategorien gleichzeitig auftreten.

**Diskussionsfrage:** Welche der vier Kategorien wird durch sehr gute Standards (z. B. FHIR + Profile) am stärksten reduziert? Welche bleibt am stabilsten?

**Mögliche Anschlussfragen:**
- Warum fordert „Bit-perfect" so präzise Spezifikationen?
- Was meint „Double translation" technisch?
- Wie verbindet sich „Each specialty speaks its own dialect" mit Terminologien wie SNOMED CT?

## Verwandt

- [[MSI - Interoperabilität - Voraussetzungen]]
- [[MSI - Standards - Definition]]
- [[MSI - Standards - Nutzen]]
- [[MSI - Datenaustausch - Formen]]

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 24 (Quelle: Benson and Grieve, *Principles of Health Interoperability*)
