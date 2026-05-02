---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Identitaetsmanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Identitätsmanagement - Autorisierung

> [!info] Kurzdefinition
> Zuweisen von Zugriffsrechten an eine bereits authentifizierte digitale Identität. Klärt nicht „Wer ist die Person?", sondern „Was darf sie?".

## Beschreibung

Folie 11 zitiert zwei Definitionen:

> *„Authorization is a decision to allow a particular action based on an identifier or attribute." [Clarke]*
> *„Through authorization, rights are assigned to a digital identity." [GINI-SA]*

**Kernpunkte:**
- Zuweisen / Erteilen von Zugriffsrechten auf Informationen.
- z. B. Lese-/Schreibrechte in einem Dokument.
- Wie diese Zugriffsrechte in einer Anwendung / App / einem Unternehmen vergeben werden, ist Sache des **Berechtigungsmodells**.
- Es gibt unterschiedliche Lösungen, daher verschiedene **Berechtigungsmodelle** (siehe [[ASP - Berechtigungsmodelle - Uebersicht]]).

## Bestandteile / Aufbau

| Element | Bedeutung |
|---|---|
| Subject | wer will zugreifen (authentifizierte Identität) |
| Resource / Object | worauf soll zugegriffen werden |
| Action | welche Operation (lesen, schreiben, ausführen, …) |
| Decision | erlaubt / nicht erlaubt |
| Berechtigungsmodell | nach welchen Regeln die Decision getroffen wird |

## Beispiel

In einem Krankenhaus-System: Authentifizierte Ärztin Dr. Müller darf Patienten-Akten ihrer Station lesen und schreiben (Action: read+write). Reinigungspersonal mit derselben Authentifizierung darf gar nicht zugreifen. Beide sind authentifiziert, aber unterschiedlich autorisiert.

## Abgrenzung

- **Autorisierung ≠ Authentifizierung:** Auth. klärt *wer*, Autorisierung klärt *was darf der/die*. Beides gehört zusammen, ist aber technisch und logisch trennbar.
- Autorisierung kann auch ohne explizite Authentifizierung passieren, z. B. anonyme öffentliche Ressourcen – dort sind die Zugriffsrechte für die Identität „anonymous" festgelegt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet Autorisierung, und wie unterscheidet sie sich von Authentifizierung?

**Anwendungsfrage:** Beschreiben Sie an einem eHealth-Beispiel die Trennung Authentifizierung ↔ Autorisierung.

**Diskussionsfrage:** Welche Prinzipien sollten bei der Vergabe von Zugriffsrechten gelten? (Stichworte aus Allgemeinwissen: Least Privilege, Need-to-Know, Separation of Duties – *im PDF nicht erwähnt*.) Welches Modell passt für ein Krankenhaus, welches für ein soziales Netzwerk?

**Mögliche Anschlussfragen:**
- Welche Berechtigungsmodelle kennt die Vorlesung? ([[ASP - Berechtigungsmodelle - Uebersicht]])
- Was passiert, wenn Authentifizierung erfolgreich ist, aber keine Autorisierung erfolgt?
- Welcher DSGVO-Bezug besteht zur Autorisierung? (Zweckbindung, Datenminimierung, Berechtigung nur für legitime Zwecke.)

## Verwandt

- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Berechtigungsmodelle - Uebersicht]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - DSGVO - Grundsaetze]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folie 11
