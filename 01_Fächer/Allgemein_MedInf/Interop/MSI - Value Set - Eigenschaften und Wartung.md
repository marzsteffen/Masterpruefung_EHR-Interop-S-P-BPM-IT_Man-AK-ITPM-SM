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

# MSI - Value Set - Eigenschaften und Wartung

> [!info] Kurzdefinition
> Eigenschaften von Code Systemen vs. Value Sets in der Praxis: Code Systeme sind fix (mit OID identifiziert, neue OID bei Sinnänderung), Value Sets sind anwendungs­spezifisch und änderbar. Wartungs-Frequenz hängt von Anwendungs­bereich ab (strukturelle Value Sets selten, inhaltliche Value Sets jährlich bis wöchentlich).

## Beschreibung

Folie 10 stellt Code Systeme und Value Sets in der „idealen Welt" gegenüber:

**Code Systeme**
- enthalten Codes mit einem „Anzeigenamen" und Attributen.
- werden durch eine ID (bei CDA: OID) eindeutig identifiziert.
- bei Löschungen oder Sinnänderungen von Codes muss dem Codesystem eine **neue** OID gegeben werden.
- Diskussionsfrage der Folie: „Was ist der Grund dafür?" – Antwort: Cimino's Concept Permanence (Bedeutung darf sich nicht ändern). Wenn sich die Bedeutung ändert, ist es technisch ein anderes Code System.

**Value Sets**
- sind eine **anwendungs­spezifische** Auswahl von Codes aus bestimmten Codesystem-Versionen (1–n).
- enthalten Referenzen auf Konzepte aus Code Systemen (reine „Aufzählung").
- werden durch einen Namen identifiziert (zusätzlich auch OID und/oder URL).
- können geändert werden.
- sollten nur gültige Codes enthalten (Verwendung zur Validierung!).

Folie 16 ergänzt zur Wartung von Value Sets (Beispiel ELGA):

> „Wie häufig Value Sets geändert werden, hängt von der jeweiligen Anwendung ab.
> – Value Sets, die für ‚strukturelle' Elemente benötigt werden (z. B. im CDA-Header, z. B. Fachrichtungen), werden sich selten ändern.
> – ‚Inhaltliche' Value Sets (z. B. für Arzneimittellisten, Laboranalysen, Diagnosen-Codierungen) werden sich entsprechend häufig ändern müssen, hier muss mit jährlichen bis wöchentlichen Änderungen gerechnet werden.
>
> Prüfungen auf geänderte Terminologien sollten von den Benutzern automatisiert werden und regelmäßig erfolgen."

Diskussionsfrage der Folie: „Wer sind die ‚Benutzer'?" – Implementierer/Hersteller, die Value Sets in ihren Systemen führen, sind dafür zuständig.

## Bestandteile / Aufbau

| Aspekt | Code System | Value Set |
|---|---|---|
| Inhalt | Codes + Anzeige­namen + Attribute | Referenzen auf Codes aus 1–n Code Systemen |
| Identifikation | OID | Name + optional OID/URL |
| Änderbarkeit | Neu-OID bei Sinnänderung | Versionierte Änderung erlaubt |
| Wartungs-Zyklus | Selten (große Releases) | Strukturell selten, inhaltlich jährlich–wöchentlich |
| Validierung | Source der Wahrheit | „Sollten nur gültige Codes enthalten" |

## Beispiel

Aus den Folien 11+12:
- Code System: LOINC mit OID `2.16.840.1.113883.6.1`.
- Value Set: `ELGA_Laborparameter` mit Parent-OID `1.2.40.0.34.10.44` – wählt aus LOINC die in ELGA verwendeten Lab-Codes.

Folie 11 zeigt dynamische Value Sets im CDA-Leitfaden mit Beschriftung „(DYNAMIC)" – damit kann das Value Set sich erweitern, ohne dass alle Implementierungen sofort updaten müssen.

## Abgrenzung

- **Statische vs. dynamische Value Sets**: dynamische (DYNAMIC) Value Sets dürfen sich erweitern; statische sind eingefroren.
- **Code System ≠ Snapshot**: Auch wenn das Code System eine Version hat, ist die OID stabil – die Version wird separat geführt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wodurch unterscheiden sich Code System und Value Set in Eigenschaften und Wartung?

**Anwendungsfrage:** Welche Wartungs-Frequenz erwarten Sie für (a) Fachrichtungs-Value-Set, (b) Diagnosen-Value-Set, (c) Arzneimittellisten-Value-Set?

**Diskussionsfrage:** Warum bekommt ein Code System bei Sinnänderung eine neue OID? Und warum reicht es bei Value Sets, sie zu ändern (statt eine neue OID zu vergeben)?

**Mögliche Anschlussfragen:**
- Was bedeutet „DYNAMIC" in einem Value Set Binding?
- Wer ist verantwortlich für die regelmäßige Prüfung auf geänderte Value Sets?
- Wie unterstützt termgit.elga.gv.at diese Prozesse?

## Verwandt

- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Identifikator - OID]]
- [[MSI - Terminologie - Cimino Desiderata]] (Concept Permanence)

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 10, 16
