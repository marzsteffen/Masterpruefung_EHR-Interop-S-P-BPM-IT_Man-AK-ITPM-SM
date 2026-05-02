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

# ASP - Security Eigenschaften - Übersicht

> [!info] Kurzdefinition
> Erweiterter Katalog von acht Sicherheitseigenschaften, der die klassische CIA-Triade um fünf weitere Schutzziele ergänzt.

## Beschreibung

Auf Folie 13 visualisiert die Vorlesung „IT-Sicherheit" als Kreis mit acht Segmenten – die acht Security Eigenschaften. Die drei klassischen CIA-Eigenschaften sind eingebettet, fünf weitere Eigenschaften kommen dazu. Folie 14 erläutert die fünf zusätzlichen Eigenschaften (rot unterstrichen auf der Grafik), Folie 15 stellt Vertraulichkeit und Privatsphäre einander gegenüber.

Die acht Eigenschaften sind:

1. **Integrität** (Integrity) – Teil der CIA-Triade
2. **Verfügbarkeit** (Availability) – Teil der CIA-Triade
3. **Vertraulichkeit** (Confidentiality) – Teil der CIA-Triade
4. **Authentizität** (Authenticity)
5. **Rückverfolgbarkeit** (Non-repudiation)
6. **Verantwortlichkeit** (Accountability)
7. **Verlässlichkeit** (Reliability)
8. **Privatsphäre** (Privacy)

## Bestandteile / Aufbau

| Eigenschaft | Englischer Begriff | Kerngedanke |
|---|---|---|
| Vertraulichkeit | Confidentiality | Wer darf zugreifen? |
| Integrität | Integrity | Sind die Daten unverändert? |
| Verfügbarkeit | Availability | Sind die Daten erreichbar? |
| Authentizität | Authenticity | Ist die Partei echt? |
| Rückverfolgbarkeit | Non-repudiation | Kann eine Tätigkeit nachgewiesen / nicht abgestritten werden? |
| Verantwortlichkeit | Accountability | Wem ist eine Handlung zuzurechnen? |
| Verlässlichkeit | Reliability | Funktioniert die Funktion ordnungsgemäß und fehlerfrei? |
| Privatsphäre | Privacy | Wofür dürfen die Daten verwendet werden? |

## Beispiel

Eine signierte ärztliche Befundnachricht in einem eHealth-Netz tangiert mehrere Eigenschaften gleichzeitig: Verschlüsselung sichert Vertraulichkeit, eine digitale Signatur sichert Integrität und Authentizität, das Logging der Signaturprüfung sichert Rückverfolgbarkeit/Verantwortlichkeit, ein hochverfügbarer Server sichert Verfügbarkeit, und die DSGVO-konforme Zweckbindung sichert Privatsphäre.

## Abgrenzung

- Die Vorlesung trennt CIA-Triade (Folie 9) und „Security Eigenschaften" (Folie 13). Erstere ist die klassische Datensicherheits-Sicht, letztere die erweiterte IT-Sicherheits-Sicht.
- Die Eigenschaften überlappen teils: Authentizität ist eine Voraussetzung für Non-repudiation und Accountability.
- „Privatsphäre" ist NICHT in „Vertraulichkeit" enthalten, auch wenn beide oft synonym verwendet werden ([[ASP - Security Eigenschaften - Privacy vs Confidentiality]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Sicherheitseigenschaften gibt es über die CIA-Triade hinaus, und was bedeuten sie?

**Anwendungsfrage:** Ordne typische Sicherheitsfunktionen den Eigenschaften zu. Beispiel: Welche Eigenschaft adressiert eine digitale Signatur primär? (Authentizität + Non-repudiation.) Welche Eigenschaft adressiert ein Audit-Log? (Accountability.)

**Diskussionsfrage:** Authentizität, Non-repudiation und Accountability werden oft in einem Atemzug genannt – worin unterscheiden sie sich konzeptuell? (Authentizität = Identität ist echt; Non-repudiation = Tätigkeit ist beweisbar; Accountability = Tätigkeit ist einer Person zurechenbar.)

**Mögliche Anschlussfragen:**
- Welche Eigenschaft fehlt der CIA-Triade konkret beim Anwendungsfall „digitaler Vertragsabschluss"? (Non-repudiation, Authenticity.)
- Warum ist Reliability eine eigene Eigenschaft und keine Verfeinerung von Availability?

## Verwandt

- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Security Eigenschaften - Non-repudiation]]
- [[ASP - Security Eigenschaften - Accountability]]
- [[ASP - Security Eigenschaften - Reliability]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folien 13, 14, 15
