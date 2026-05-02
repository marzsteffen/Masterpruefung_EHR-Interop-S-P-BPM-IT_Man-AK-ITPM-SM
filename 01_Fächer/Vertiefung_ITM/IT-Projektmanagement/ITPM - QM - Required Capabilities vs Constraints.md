---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Qualitätsmanagement]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - QM - Required Capabilities vs Constraints

> [!info] Kurzdefinition
> In Anforderungsdokumentationen sollten **Required Capabilities** (benötigte Fähigkeiten eines Systems) und **Required Constraints** (erforderliche Designvorgaben) **getrennt** betrachtet werden. Anforderungen sollten **nicht zu engmaschig** definiert sein, damit bei der Erarbeitung der Lösung Freiheiten bleiben.

## Beschreibung

Aus Folie 26:

| Begriff | Bedeutung |
|---|---|
| **Required Capabilities** | Die benötigten **Fähigkeiten eines Systems**. |
| **Required Constraints** | Erforderliche **Designvorgaben**. |

In Anforderungsdokumentationen sollte man diese **beiden Themen getrennt** voneinander betrachten.

> **Wichtig:** Anforderungen sollten **nicht zu engmaschig** definiert sein, da bei der Erarbeitung der Lösung gewisse Freiheiten gegeben sein sollten.

## Bestandteile / Aufbau

| Aspekt | Required Capabilities | Required Constraints |
|---|---|---|
| **Was?** | Was muss das System können? | Welche Vorgaben muss das Design einhalten? |
| **Beispiel** | „System muss Befunde anzeigen" | „System muss in Java geschrieben sein" |
| **Sicht** | funktional / leistungsbezogen | technisch / regulatorisch |

## Beispiel

*Im PDF nicht durch konkrete Beispiele illustriert.* Aus dem User-Story-Beispiel der Vorlesung 3 (Folie 40 Werkzeuge 02):
- Capability: „Als Benutzer kann ich nach Stellen suchen."
- Constraint: „Die Software soll in Java geschrieben werden."

## Abgrenzung

- **Required Capabilities** ähnlich **funktionalen Anforderungen** ([[ITPM - Anforderung - Definition]]).
- **Required Constraints** ähnlich **geforderten Randbedingungen**.
- Beide werden hierarchisch aufgehängt (Business → Stakeholder → System → Component, siehe [[ITPM - QM - Hierarchische Anforderungsdoku]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich Required Capabilities und Required Constraints, und warum sollten sie getrennt dokumentiert werden?

**Anwendungsfrage:** Geben Sie für ein Patientenportal je drei Capabilities und drei Constraints an.

**Diskussionsfrage:** Warum sollten Anforderungen nicht zu engmaschig definiert sein?

**Mögliche Anschlussfragen:**
- Welche Verbindung zu funktionalen Anforderungen vs. Randbedingungen?
- Wie verhält sich Capabilities/Constraints zur User Story?
- Wann werden Constraints zu „starr"?

## Verwandt

- [[ITPM - Anforderung - Definition]]
- [[ITPM - QM - Hierarchische Anforderungsdoku]]
- [[ITPM - Qualitätsplanung]]
- [[ITPM - Critical Qualities]]
- [[ITPM - Agile - User Story]]

## Quelle

- Vorlesung: [[ITPM - VL - Qualitätsmanagement]]
- Folien/Seitenangabe: 26
