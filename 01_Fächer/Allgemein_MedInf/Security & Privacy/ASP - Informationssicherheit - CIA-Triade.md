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

# ASP - Informationssicherheit - CIA-Triade

> [!info] Kurzdefinition
> Klassisches Schutzziel-Modell der Datensicherheit, bestehend aus den drei Eigenschaften Confidentiality (Vertraulichkeit), Integrity (Integrität) und Availability (Verfügbarkeit).

## Beschreibung

Die CIA-Triade beschreibt die drei grundlegenden Informationssicherheits-Schutzziele. In der Vorlesung wird sie unter dem Titel „Informationssicherheitsschutzziele (Datensicherheit – CIA-Triade)" eingeführt:

- **Confidentiality / Vertraulichkeit:** Schutz von Informationen vor Offenlegung durch Unbefugte. Lesen und Verändern von Daten nur durch autorisierte Personen.
- **Integrity / Integrität:** Schutz von Informationen vor Änderungen durch Unbefugte. Unveränderbarkeit und nachvollziehbare Änderungen.
- **Availability / Verfügbarkeit:** Gewährleistung, dass autorisierte Parteien bei Bedarf Zugriff auf Informationen erhalten. Ausfallsicherheit von Systemen.

Die Vorlesung zeigt explizit, dass diese drei Schutzziele nicht nur auf elektronische Daten anwendbar sind, sondern auch auf Wissen, gesprochenes Wort und Dokumente in Papierform. Pro Kombination *Informationsart × Schutzziel* gibt es typische Schutzmaßnahmen.

## Bestandteile / Aufbau

| Schutzziel | Bedeutung | Beispiel-Schutz für elektronische Daten (Folie 10) |
|---|---|---|
| Confidentiality | Wer darf zugreifen? | Verschlüsselung |
| Integrity | Sind die Daten unverändert? | Prüfsummen (Hash, Digitale Signaturen) |
| Availability | Sind die Daten erreichbar? | Redundanzsysteme |

Für andere Informationsarten (Folie 10) nennt die Vorlesung u. a. Vertraulichkeitsvereinbarungen (Wissen), physische Zugriffskontrolle (Papier) und Wissenstransfer/Vertretungen (Verfügbarkeit von Wissen).

## Beispiel

Patientenakte im Krankenhaus:
- Vertraulichkeit: Nur behandelnde Ärztinnen, Ärzte und Pflegekräfte sehen die Akte (Beispiel laut Folie 15).
- Integrität: Befunde dürfen nicht unbemerkt manipuliert werden; Änderungen sind nachvollziehbar.
- Verfügbarkeit: Die Akte ist im Notfall sofort abrufbar.

## Abgrenzung

- CIA wird in der Vorlesung um weitere Security Eigenschaften erweitert ([[ASP - Security Eigenschaften - Uebersicht]]). CIA allein ist nicht erschöpfend.
- Vertraulichkeit (Confidentiality) ist NICHT dasselbe wie Privatsphäre (Privacy). Siehe [[ASP - Security Eigenschaften - Privacy vs Confidentiality]].
- IT-Sicherheit ist Teilmenge der Informationssicherheit; CIA gilt aber genauso für nicht-technische Informationsträger. Siehe [[ASP - Informationssicherheit - IT-Sicherheit vs Informationssicherheit]].

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was steht hinter „CIA" im Kontext Informationssicherheit, und wie unterscheiden sich die drei Schutzziele?

**Anwendungsfrage:** Ordne typische Sicherheitsmaßnahmen (z. B. Verschlüsselung, Hash, Backup) den jeweiligen Schutzzielen zu. Welche Schutzziele werden durch eine reine Verschlüsselung NICHT abgedeckt (Antwort: Integrität, Verfügbarkeit)?

**Diskussionsfrage:** Reicht die CIA-Triade aus, um den Schutz personenbezogener Gesundheitsdaten zu beschreiben, oder werden weitere Schutzziele (Authentizität, Privatsphäre) benötigt? Trade-off zwischen Verfügbarkeit (Notfallzugriff) und Vertraulichkeit (strenger Zugriffsschutz).

**Mögliche Anschlussfragen:**
- Welche Schutzziele werden durch Verschlüsselung NICHT abgedeckt?
- Wie schützt man Integrität auch bei verschlüsselten Daten?
- Warum ist Privatsphäre ein eigenes Schutzziel und nicht in „Confidentiality" enthalten?
- Welcher DSGVO-Grundsatz adressiert direkt Integrity und Confidentiality? (Antwort siehe [[ASP - DSGVO - Grundsaetze]].)

## Verwandt

- [[ASP - Security Eigenschaften - Uebersicht]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]
- [[ASP - Informationssicherheit - IT-Sicherheit vs Informationssicherheit]]
- [[ASP - DSGVO - Grundsaetze]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 9; ergänzt durch Folie 8 (Informationsarten) und Folie 10 (Schutzmaßnahmen-Matrix, Quelle TÜV AUSTRIA V3.0 © 2023)
