---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Einfuehrung und Motivation]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - DSGVO - Privacy by Design

> [!info] Kurzdefinition
> Pflicht aus DSGVO Artikel 25 Abs. 1: Datenschutz durch Technikgestaltung – also von Anfang an in das System eingebaut, nicht nachträglich „aufgesetzt".

## Beschreibung

Die Vorlesung nennt Privacy by Design auf Folie 17 mit zwei Eigenschaften:

- **Datenschutz durch Technikgestaltung, d. h. von Anfang an.**
- **Geeignete technische/organisatorische Maßnahmen** (z. B. Pseudonymisierung).

Der Begriff verlangt also, dass datenschutzfreundliche Voreinstellungen bereits in der Architektur und im Entwurfsprozess eines Systems berücksichtigt werden, nicht erst nachträglich. Genauer technischer Detaillierungsgrad: in dieser Vorlesung sehr gering.

**Im PDF erwähnt, aber nicht erklärt:** „Pseudonymisierung" – wird nur als Beispiel genannt, nicht definiert.

## Bestandteile / Aufbau

| Anker | Inhalt laut Folie 17 |
|---|---|
| Rechtsgrundlage | DSGVO Artikel 25 Abs. 1 |
| Kernforderung | Datenschutz von Anfang an in der Technikgestaltung |
| Maßnahmenebene | Technische und organisatorische Maßnahmen |
| Beispiel-Maßnahme | Pseudonymisierung |

## Beispiel

Aus der Folie: Pseudonymisierung als technische Maßnahme. *Im PDF nicht weiter ausgeführt.* Naheliegend für eHealth: Trennung von Identifikations- und medizinischen Daten in zwei Datenbanken mit eigenem Berechtigungskonzept; Daten-Felder werden nur bei Bedarf zusammengeführt.

## Abgrenzung

- **Privacy by Design vs. Privacy by Default** ([[ASP - DSGVO - Privacy by Default]]): Privacy by Design adressiert die *Architektur und Entwicklung*, Privacy by Default adressiert die *Standard-Einstellungen* eines fertigen Produkts. Beide stehen in Art. 25 DSGVO, aber in unterschiedlichen Absätzen (Abs. 1 vs. Abs. 2).
- Privacy by Design ist **nicht** dasselbe wie der Grundsatz „Integrität und Vertraulichkeit" aus [[ASP - DSGVO - Grundsaetze]] – Letzterer fordert die Sicherheit der Daten, Ersterer fordert das frühe Einbauen von Datenschutz-Mechanismen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet Privacy by Design und in welchem DSGVO-Artikel ist es geregelt?

**Anwendungsfrage:** Welche konkreten Architekturentscheidungen würden Privacy by Design in einem ePA-System unterstützen?

**Diskussionsfrage:** Warum ist nachträglich aufgesetzter Datenschutz typischerweise schwächer als Privacy by Design? (Stichworte: Datenflüsse schwer rückgängig zu machen, Pseudonymisierung nachträglich kaum wirksam, einmal erhobene Daten bleiben erhoben.)

**Mögliche Anschlussfragen:**
- Was ist Pseudonymisierung – und wie unterscheidet sie sich von Anonymisierung? (*Anonymisierung im PDF nicht definiert.*)
- Wie hängt Privacy by Design mit dem Grundsatz Datenminimierung zusammen?
- Welche organisatorischen Maßnahmen können Privacy by Design ergänzen?

## Verwandt

- [[ASP - DSGVO - Privacy by Default]]
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]
- [[ASP - Pseudonymisierung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 17
