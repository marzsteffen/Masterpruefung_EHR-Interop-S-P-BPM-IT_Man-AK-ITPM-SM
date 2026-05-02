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

# ASP - Security Eigenschaften - Privatsphäre vs Vertraulichkeit (Privacy vs Confidentiality)

> [!info] Kurzdefinition
> Vertraulichkeit regelt, **wer** auf Informationen zugreifen darf; Privatsphäre regelt, **wofür** zugegriffene Informationen verwendet werden dürfen.

## Beschreibung

Folie 15 stellt die beiden Eigenschaften explizit gegenüber, weil sie umgangssprachlich oft synonym verwendet werden, technisch aber unterschiedliche Schutzbereiche adressieren:

**Vertraulichkeit (Confidentiality) – „Autorisierte Verwendung":**
- Bezieht sich darauf, *wer* auf bestimmte Informationen zugreifen darf.
- Daten dürfen nicht für die Öffentlichkeit oder nicht autorisierte Personen zugänglich sein.
- Beispiel: Ärzte, Krankenschwestern und andere medizinische Fachkräfte haben Zugriff auf Patientenakten.

**Privatsphäre (Privacy) – „Zweckgemäße Verwendung":**
- Bezieht sich darauf, *wie* Informationen verwendet werden, *selbst wenn* sie von autorisierten Personen eingesehen werden.
- Beispiel: Patientenakten dürfen nur für berufliche Zwecke genutzt bzw. eingesehen werden.

Daraus folgt: Eine Person kann *autorisiert sein zuzugreifen* (Vertraulichkeit erfüllt) und trotzdem die Daten zweckwidrig verwenden (Privatsphäre verletzt).

## Bestandteile / Aufbau

| Aspekt | Vertraulichkeit | Privatsphäre |
|---|---|---|
| Frage | Wer darf zugreifen? | Wofür darf zugegriffen werden? |
| Schutz vor | Unbefugtem Zugriff | Zweckwidriger Verwendung trotz erlaubten Zugriffs |
| Typische Maßnahme | Verschlüsselung, Zugriffskontrolle | Zweckbindung (DSGVO), organisatorische Richtlinien |
| Lokalisierung | CIA-Triade | Eigene Eigenschaft im 8er-Katalog |

## Beispiel

Aus Folie 15: Eine Krankenschwester darf die Patientenakte lesen (Vertraulichkeit ist erfüllt – sie ist autorisierte Person). Würde sie die Akte aber privat einer Bekannten zeigen, wäre die Privatsphäre verletzt, obwohl der Zugriff selbst autorisiert war.

## Abgrenzung

- Vertraulichkeit ist Teil der CIA-Triade ([[ASP - Informationssicherheit - CIA-Triade]]). Privatsphäre ist ein eigenständiges Schutzziel im 8er-Katalog der Vorlesung.
- Privatsphäre wird auf der nächsten Folie direkt mit der DSGVO verknüpft ([[ASP - DSGVO - Grundsaetze]]) – dort vor allem mit dem Grundsatz „Zweckbindung".

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich Vertraulichkeit und Privatsphäre?

**Anwendungsfrage:** Geben Sie ein Szenario, in dem Vertraulichkeit erfüllt, aber Privatsphäre verletzt ist (oder umgekehrt).

**Diskussionsfrage:** Wieso reicht es im DSGVO-Kontext nicht aus, „nur" Vertraulichkeit über Verschlüsselung sicherzustellen? Welche Mechanismen sichern dann Privatsphäre?

**Mögliche Anschlussfragen:**
- Welche DSGVO-Grundsätze sind eher Privatsphäre, welche eher Vertraulichkeit?
- Wie wirkt eine Pseudonymisierung auf Vertraulichkeit und Privatsphäre?
- Warum ist diese Unterscheidung gerade in eHealth besonders relevant?

## Verwandt

- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Security Eigenschaften - Uebersicht]]
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - DSGVO - Privacy by Design]]
- [[ASP - DSGVO - Privacy by Default]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 15
