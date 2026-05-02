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

# ASP - Identitätsmanagement - Digitale Identität

> [!info] Kurzdefinition
> Digitales Abbild einer Person oder eines Objekts in der digitalen Welt. Besteht aus drei Teilen: einer eindeutigen ID, Identitätsdaten (Attributen) und Authentifizierungs-/Identifikationsdaten.

## Beschreibung

Folie 4: Eine digitale Identität ist das digitale Abbild einer Person oder eines Objekts in der digitalen Welt. Sie ermöglicht **Identifikation und Authentifizierung**. **Anwendungsbereiche:** Online-Banking, E-Government, E-Commerce, Unternehmensnetzwerke, …

Folie 5 zerlegt die digitale Identität in drei **Teilstücke**:

- **Eindeutige ID:**
  - Grundlage für die eindeutige Zuweisung der digitalen Identität zu einer Entität.
  - z. B. Benutzer-ID, Universally Unique Identifier (UUID).

- **Identitätsdaten (Attribute):**
  - Eigenschaften, die eine Person oder ein Objekt beschreiben.
  - z. B. Name, Geburtsdatum, Geschlecht, Geräteinformationen.

- **Authentifizierungs- und Identifikationsdaten:**
  - Daten, die für eine Anmeldung an einem System mit der digitalen Identität verwendet werden.
  - z. B. Benutzername + Passwort, digitale Zertifikate.

## Bestandteile / Aufbau

| Teil | Funktion | Beispiel |
|---|---|---|
| Eindeutige ID | Zuweisung zur Entität | UUID, Benutzer-ID |
| Identitätsdaten / Attribute | Beschreibung der Person/des Objekts | Name, Geburtsdatum |
| Authentifizierungsdaten | Anmeldung am System | Passwort, Zertifikat |

## Beispiel

Eine ELGA-Identität umfasst: bPK-GH (eindeutige ID im Gesundheitsbereich), Vor-/Nachname/Geburtsdatum (Attribute), Handy-Signatur oder ID Austria (Authentifizierungsmittel). *Im PDF nicht explizit ausgeführt; ergibt sich aus den genannten Anwendungsbereichen.*

## Abgrenzung

- **Digitale Identität ≠ Person:** Eine Person kann mehrere digitale Identitäten haben (z. B. private E-Mail-Adresse, ELGA-Identität, Mitarbeiter-Konto in der Firma).
- **Eindeutige ID ≠ Attribute:** Die ID identifiziert technisch, die Attribute beschreiben inhaltlich.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine digitale Identität, aus welchen drei Teilen besteht sie?

**Anwendungsfrage:** Beschreiben Sie die Teilstücke einer ELGA-Identität (oder eines anderen eHealth-Systems).

**Diskussionsfrage:** Welche Auswirkungen hat es, wenn die eindeutige ID nicht eindeutig genug gewählt wurde (z. B. nur „Vorname Nachname" statt Personenbindungs-ID)? Welche DSGVO-Aspekte sind bei den Identitätsdaten zu beachten?

**Mögliche Anschlussfragen:**
- Was ist eine UUID, und welche Eigenschaften garantiert sie?
- Was sind Beispiele für Authentifizierungsdaten neben Passwort und Zertifikat?
- Wie unterscheidet sich eine digitale Identität einer Person von der eines Geräts (IoT)?

## Verwandt

- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Identitaetsmanagement - Authentifizierungsklassen]]
- [[ASP - Zertifikate - X.509]]
- [[ASP - Authentifizierung - Level of Assurance]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folien 4, 5
