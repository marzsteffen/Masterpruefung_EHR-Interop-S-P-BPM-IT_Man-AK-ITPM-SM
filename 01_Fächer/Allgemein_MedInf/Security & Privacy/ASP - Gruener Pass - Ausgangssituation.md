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

# ASP - Grüner Pass - Ausgangssituation und Anforderungen

> [!info] Kurzdefinition
> Mit der COVID-19-Pandemie ab Februar 2020 entstand der Bedarf nach einem digitalen Statusnachweis (3G: Geimpft / Genesen / Getestet). Drei Herausforderungen: gemeinsamer Vertrauensrahmen, Schutz der Privatsphäre, Fälschungssicherheit.

## Beschreibung

Folien 3–4:

- Im **Februar 2020** erster COVID-19-Fall in Österreich.
- Diverse Maßnahmen zur Eindämmung der Ausbreitungsgeschwindigkeit.
- Wichtigste Maßnahme: **3G-Regel** (Geimpft, Genesen, Getestet).
- Nachweis eines geringen epidemiologischen Risikos.
- Statusnachweis über **digitale Zertifikate** auf Smartphones.

**Anforderungen aus EU-Sicht (Folie 4):**
- Zertifikate müssen im Rahmen der Zutrittskontrollen verifiziert werden.
- **Interoperable Zertifikate** sind erforderlich, um die freie Beweglichkeit in der EU zu gewährleisten.
- EU-Mitgliedsstaaten müssen **Authentizität, Gültigkeit und Integrität** von Zertifikaten sicherstellen.
- Erforderliche Regeln und Infrastruktur für eine zuverlässige und sichere Ausstellung und Verifizierung.

**Drei Herausforderungen (Folie 4, in Rot):**
1. Wie baut man einen gemeinsam gültigen **Vertrauensrahmen** auf?
2. Wie kann die **Rückverfolgung von Bürgern** verhindert werden, um die Privatsphäre zu schützen?
3. Wie kann man die **Fälschung von Zertifikaten** verhindern?

Diese drei Fragen ziehen sich als Leitmotiv durch den gesamten Vorlesungs-Block: Vertrauensmodell adressiert (1), Validator-Anforderungen adressieren (2), Signatur-Kette und QR-Code-Mitigationen adressieren (3).

## Bestandteile / Aufbau

| Anforderung | Schutzziel | Lösungsskizze in der Vorlesung |
|---|---|---|
| Authentizität | Wer hat das Zertifikat ausgestellt? | CSCA → DSC → DCC (Vertrauensmodell) |
| Gültigkeit | Ist es zeitlich und strukturell ok? | Business Rules Validation |
| Integrität | Wurde es manipuliert? | Digitale Signatur über JSON-Payload |
| Interoperabilität | Pan-europäisch lesbar? | EU Gateway, JSON-Schema, Value Sets |

## Beispiel

Aus den Folien: Ein österreichischer Patient soll mit dem auf seinem Smartphone gespeicherten QR-Code in einem deutschen Restaurant Zugang erhalten. Das setzt Interoperabilität voraus – der deutsche Validator-App muss das österreichische Zertifikat verifizieren können.

## Abgrenzung

- **3G-Regel ist die fachlich-organisatorische Anforderung**, nicht die technische Lösung. Die technische Lösung folgt erst über das EU Digital COVID Certificate.
- **Privatsphäre vs. Vertraulichkeit:** Der Inhalt des QR-Codes ist nicht verschlüsselt, nur signiert; Privatsphäre wird über Datenminimierung und Validator-App-Beschränkungen geschützt, nicht über Verschlüsselung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Ausgangssituation führte zum EU Digital COVID Certificate? Welche drei Herausforderungen mussten gelöst werden?

**Anwendungsfrage:** Ordnen Sie jede der drei Herausforderungen der jeweiligen Lösungsschicht im DCC-System zu.

**Diskussionsfrage:** Welche der drei Herausforderungen wurde am besten gelöst, welche hat in der Praxis Schwächen gezeigt? (Antwort: Fälschungssicherheit ist die Schwachstelle – siehe [[ASP - Gruener Pass - Sicherheitsbedenken]].)

**Mögliche Anschlussfragen:**
- Was bedeutet 3G konkret?
- Welcher DSGVO-Grundsatz adressiert die Privatsphären-Anforderung am direktesten? (Datenminimierung – siehe [[ASP - DSGVO - Grundsaetze]].)
- Welche Krypto-Bausteine kommen für die Lösung der drei Anforderungen zum Einsatz? (Signatur, Zertifikatskette, Hash.)

## Verwandt

- [[ASP - Gruener Pass - EU Digital COVID Certificate]]
- [[ASP - Gruener Pass - Vertrauensmodell]]
- [[ASP - Gruener Pass - Sicherheitsbedenken]]
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folien 3, 4
