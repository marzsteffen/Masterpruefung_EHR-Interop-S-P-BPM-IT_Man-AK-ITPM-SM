---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Gruener Pass]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Grüner Pass - Validator-Anforderungen

> [!info] Kurzdefinition
> Rechtliche Anforderungen an Personen und Apps, die DCCs verifizieren: Identifizierung mit Lichtbildausweis, Offline-Signaturprüfung, eingeschränkte Datenanzeige (nur Name + Geburtsdatum), Bearbeitungsverbot.

## Beschreibung

Folie 7 listet die Anforderungen an Validatoren.

**Identifizierung der Person:**
- Anhand eines **amtlichen Lichtbildausweises** (verhindert, dass jemand mit einem fremden QR-Code auftritt).

**Offline-Prüfung von Zertifikaten (Signaturprüfung):**
1. Überprüfung auf **syntaktische und inhaltliche Korrektheit** → verhindert die Rückverfolgbarkeit von Bürgern (keine Online-Anfrage an einen zentralen Server, der Logs schreiben könnte).
2. Überprüfung der **zeitlichen Gültigkeit**.

**Elektronische Anwendungen zur Überprüfung von Zertifikaten (Validator-Apps):**
- Angegebene Zertifikatsdaten müssen **eingeschränkt angezeigt** werden (Vorname, Nachname, Geburtsdatum) → bewahrt die Privatsphäre der Bürger.
- **Bearbeitungen von Zertifikaten, die über die Verifizierung hinausgehen, sind unzulässig** → verhindert Missbrauch (z. B. Datenkopie in einer App-Backend-Datenbank).

## Bestandteile / Aufbau

| Anforderung | Schutzziel | Begründung in der Vorlesung |
|---|---|---|
| Lichtbildausweis-Prüfung | Identitätsbindung | sonst kann jeder mit fremdem QR-Code auftreten |
| Offline-Signaturprüfung | Privatsphäre | verhindert Rückverfolgbarkeit über Online-Logs |
| Eingeschränkte Datenanzeige | Privatsphäre | nur das Notwendige |
| Bearbeitungsverbot | Missbrauchsschutz | keine sekundäre Datenspeicherung |

## Beispiel

Aus dem Vorlesungs-Kontext: Beim Eintritt zu einer Veranstaltung scannt der Türsteher mit der Validator-App den QR-Code. Die App zeigt: „gültig", „Vorname Nachname, Geburtsdatum". Mehr nicht. Der Türsteher prüft anschließend den Lichtbildausweis und vergleicht Name und Geburtsdatum.

## Abgrenzung

- **Validator-Anforderungen sind Pflichten der Anwender**, nicht der Krypto-Schicht. Die Krypto liefert die signierten Daten; die App-/Personen-Ebene muss korrekt damit umgehen.
- **Offline-Prüfung** ist ein bewusster Datenschutz-Designentscheid – sie kostet Funktionalität (Echtzeit-Sperren funktionieren nicht), gewinnt aber Privatsphäre.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Anforderungen muss ein Validator (Person + App) erfüllen?

**Anwendungsfrage:** Welche Anforderung adressiert welche der drei Hauptherausforderungen aus der Ausgangssituation? (Lichtbildausweis → Fälschungsschutz; Offline-Prüfung + eingeschränkte Anzeige → Privatsphäre.)

**Diskussionsfrage:** Welcher Trade-off besteht zwischen Offline- und Online-Prüfung? Welche Anwendungsfälle könnten Online-Prüfung rechtfertigen, und welche Privatsphäre-Risiken bringt sie mit?

**Mögliche Anschlussfragen:**
- Was passiert, wenn der Validator den Lichtbildausweis nicht prüft? ([[ASP - Gruener Pass - Sicherheitsbedenken]] – Hitler-Vorfall.)
- Wie wird die Trust List aktuell gehalten, wenn die Prüfung offline ist? ([[ASP - Gruener Pass - AT Architektur]] – stündliche Aktualisierung.)
- Welche DSGVO-Grundsätze adressiert die eingeschränkte Datenanzeige? (Datenminimierung, Zweckbindung.)

## Verwandt

- [[ASP - Gruener Pass - EU Digital COVID Certificate]]
- [[ASP - Gruener Pass - Vertrauensmodell]]
- [[ASP - Gruener Pass - Sicherheitsbedenken]]
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folie 7
