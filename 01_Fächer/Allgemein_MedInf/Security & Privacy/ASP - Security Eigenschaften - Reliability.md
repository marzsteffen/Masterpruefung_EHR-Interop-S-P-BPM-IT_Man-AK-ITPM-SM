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

# ASP - Security Eigenschaften - Verlässlichkeit (Reliability)

> [!info] Kurzdefinition
> Die Fähigkeit, eine Funktion ordnungsgemäß und fehlerfrei durchzuführen (laut Folie 14).

## Beschreibung

Verlässlichkeit (Reliability) ist eines der acht Schutzziele auf der Security-Grafik (Folie 13). Sie zielt nicht primär auf Schutz vor Angreifern, sondern auf das korrekte und fehlerfreie Funktionieren einer Sicherheitsfunktion oder eines Systems.

Konkrete Mechanismen oder Metriken werden in der Vorlesung *nicht* genannt. **Im PDF nicht definiert:** typische Realisierungen (z. B. fehlertolerante Systeme, Redundanz, formale Verifikation, Tests). Auch der Zusammenhang zu Verfügbarkeit wird nicht explizit erläutert.

## Bestandteile / Aufbau

*Im PDF nicht in einzelne Bestandteile zerlegt.*

## Abgrenzung

- **Reliability vs. Availability:** Beide klingen ähnlich. Verfügbarkeit beschreibt, ob ein System überhaupt erreichbar ist; Verlässlichkeit beschreibt, ob es korrekt arbeitet, wenn es erreichbar ist. Diese explizite Abgrenzung ist *im PDF nicht ausgeführt*, ergibt sich aber aus den Definitionen.
- Reliability als eigenständiges Schutzziel ist in der Praxis weniger gängig als die anderen sieben – es taucht oft nur in formaleren Sicherheits-Modellen (z. B. RAS-Eigenschaften: Reliability, Availability, Serviceability) auf.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was unterscheidet Verlässlichkeit von Verfügbarkeit?

**Anwendungsfrage:** Wann ist Reliability in einem eHealth-System besonders kritisch? (Beispielsweise medizinische Geräte: Funktionieren der Mess-Software korrekt im Einsatz?)

**Diskussionsfrage:** Ist Reliability ein „echtes" Sicherheitsziel oder eher ein Qualitätsmerkmal? Argumente für beides – die Vorlesung führt es als Sicherheitseigenschaft an.

**Mögliche Anschlussfragen:**
- Wie hängt Reliability mit Business Continuity Management zusammen? (siehe [[ASP - VL - Business Continuity Management]] – folgt.)
- Welche Schutzmaßnahmen erhöhen Reliability gegenüber zufälligen Fehlern?

## Verwandt

- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Security Eigenschaften - Uebersicht]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folien 13, 14
