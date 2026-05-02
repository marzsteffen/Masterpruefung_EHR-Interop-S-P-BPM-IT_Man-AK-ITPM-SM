---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Initiierung Strukturierung Requirements]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - Pufferzeiten

> [!info] Kurzdefinition
> Pufferzeiten geben einer Aktivität Spielraum, ohne den Endtermin oder den Start nachfolgender Aktivitäten zu gefährden. Es werden zwei Pufferarten unterschieden: **Gesamtpuffer** (max. Verzögerung ohne Projektverzug) und **freier Puffer** (Verzögerung ohne Auswirkung auf den nächsten Vorgang).

## Beschreibung

**Gesamtpuffer einer Aktivität (Folie 50):**
- Zeitraum, um den sich eine Aktivität **maximal verzögern darf**.
- Errechnet sich aus der **Differenz** zwischen frühestmöglichem und spätestmöglichem Start- und Endtermin.

**Freier Puffer einer Aktivität (Folie 50):**
- Zeitraum, in dem sich eine Aktivität verzögern darf, **ohne den frühestmöglichen Starttermin der nächsten Aktivität zu beeinflussen**.

## Bestandteile / Aufbau

| Pufferart | Bezugspunkt | Wirkung bei Verzögerung |
|---|---|---|
| **Gesamtpuffer** | Spielraum bis zum spätesten Endtermin | Solange ≤ Puffer: kein Projektverzug |
| **Freier Puffer** | Spielraum bis zum frühesten Start des nächsten Vorgangs | Solange ≤ Puffer: kein Folgeverzug |

**Praxisempfehlung der Vorlesung (Folie 56):**

- Pufferzeiten machen Sinn, sollten aber **„mit Maß und Ziel"** eingesetzt werden.
- Besonders relevant für Aktivitäten auf dem **kritischen Pfad**.
- Guter Einsatz wirkt sich positiv auf die Projektdurchführung aus.
- **Aber:** Auftraggeber zahlen Pufferzeiten ungern und können dadurch zusätzlichen Druck ausüben (schnellere Durchführung scheint möglich).

## Beispiel

*Im PDF nicht durch konkretes Zahlenbeispiel illustriert.*

## Abgrenzung

- **Gesamtpuffer** ≥ **freier Puffer** (immer): freier Puffer ist eine Teilmenge des Gesamtpuffers.
- Aktivitäten auf dem **kritischen Weg** haben **Gesamtpuffer = 0** (siehe [[ITPM - Kritischer Weg]]).
- Im agilen Kontext werden Puffer durch **Velocity-Schwankung** und **Sprint-Buffer** abgebildet, nicht explizit modelliert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich Gesamtpuffer und freier Puffer?

**Anwendungsfrage:** Eine Aktivität hat Gesamtpuffer = 5 Tage, freier Puffer = 2 Tage. Was bedeutet das praktisch?

**Diskussionsfrage:** Wie kommuniziert man Puffer gegenüber Auftraggebern, ohne den von der Vorlesung beschriebenen Druck zu erzeugen?

**Mögliche Anschlussfragen:**
- Wie verhalten sich Puffer auf dem kritischen Pfad?
- Welche Rolle spielen Puffer bei der Earned Value-Analyse?

## Verwandt

- [[ITPM - Ablauf- und Terminplan]]
- [[ITPM - Kritischer Weg]]
- [[ITPM - Aufwandsschätzung - Drei-Punkt]]
- [[ITPM - Meilenstein]]

## Quelle

- Vorlesung: [[ITPM - VL - Initiierung Strukturierung Requirements]]
- Folien/Seitenangabe: 50, 56
