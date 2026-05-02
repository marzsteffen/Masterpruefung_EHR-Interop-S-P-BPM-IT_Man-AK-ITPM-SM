---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Informationssicherheits-Risikomanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Risikomanagement - Definition Risiko

> [!info] Kurzdefinition
> Duden: möglicher negativer Ausgang einer Unternehmung mit Nachteilen, Verlusten, Schäden. ISO 27005:2022 abstrakter und neutraler: „effect of uncertainty on objectives" – ein Effekt kann positiv oder negativ sein, im Kontext Informationssicherheit aber meist negativ.

## Beschreibung

Folie 2 stellt zwei Definitionen gegenüber.

### Duden
> *Möglicher negativer Ausgang bei einer Unternehmung, mit dem Nachteile, Verlust, Schäden verbunden sind; mit einem Vorhaben, Unternehmen o. Ä. verbundenes Wagnis.*

### ISO 27005:2022
> *„Effect of uncertainty on objectives"*

- **Note 1 to entry:** *„An effect is a deviation from the expected, positive or negative."*
- **Note 5 to entry:** *„In the context of information security management systems, information security risks can be expressed as effect of uncertainty on information security objectives."*
- **Note 6 to entry:** *„Information security risks are usually associated with a negative effect of uncertainty on information security objectives."*

**Schlussfolgerung:** Risiko ist formal neutral (Abweichung vom Erwarteten, positiv oder negativ), wird aber im Sicherheits-Kontext praktisch immer als negative Abweichung verstanden.

## Bestandteile / Aufbau

| Quelle | Tonart | Reichweite |
|---|---|---|
| Duden | negativ | allgemeinsprachlich |
| ISO 27005:2022 | neutral, mit Note 6 negativ | formal / international |

## Beispiel

- Duden-Sicht: „Das Risiko, dass die Datenbank ausfällt" – impliziert nur Schaden.
- ISO-Sicht: „Effekt der Unsicherheit auf das Schutzziel Verfügbarkeit" – formal könnten auch positive Effekte mitgedacht werden (z. B. unerwartet positive Verfügbarkeit), aber Note 6 macht klar: praktisch geht es um Schäden.

## Abgrenzung

- **Risiko ≠ Bedrohung:** Bedrohung ist nur die Ursache. Risiko entsteht erst aus Asset + Bedrohung + Schwachstelle (siehe [[ASP - Risikomanagement - Grundvoraussetzungen]]).
- **Risiko ≠ Schaden:** Schaden ist die eingetretene Auswirkung. Risiko ist das *vorab* zu erwartende Maß für mögliche Schäden.
- **ISO 27005-Definition vs. BSI 200-4-BCM-Risiko:** ISO ist allgemeiner; BSI 200-4 fokussiert speziell auf Verfügbarkeit zeitkritischer Ressourcen (siehe [[ASP - BCM - Risikoanalyse]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie definieren Duden und ISO 27005:2022 den Risikobegriff? Worin unterscheiden sich die beiden?

**Anwendungsfrage:** Übersetze einen konkreten Fall (z. B. „Server fällt aus") in die ISO-Formulierung.

**Diskussionsfrage:** Warum wählt ISO 27005 die neutrale Formulierung? Welche praktischen Konsequenzen hat es, dass „Risiko" auch positive Effekte umfassen *könnte*?

**Mögliche Anschlussfragen:**
- Welche Voraussetzungen müssen erfüllt sein, damit ein Risiko überhaupt besteht?
- Welcher Zusammenhang besteht zur CIA-Triade?
- Wie würde sich der Risikobegriff im DSGVO-Kontext ändern? (Datenschutz-Folgenabschätzung – im PDF nicht erwähnt.)

## Verwandt

- [[ASP - Risikomanagement - Grundvoraussetzungen]]
- [[ASP - Risikomanagement - Big Picture]]
- [[ASP - BCM - Risikoanalyse]]
- [[ASP - Informationssicherheit - CIA-Triade]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folie 2
- Standard: ISO/IEC 27005:2022 – Information security, cybersecurity and privacy protection — Guidance on managing information security risks
