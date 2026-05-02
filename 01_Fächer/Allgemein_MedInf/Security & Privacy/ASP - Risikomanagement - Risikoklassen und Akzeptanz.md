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

# ASP - Risikomanagement - Risikoklassen und Akzeptanzkriterien

> [!info] Kurzdefinition
> Pro Risikoklasse (hoch/mittel/gering) werden Vorgaben zum Umgang (Meldepflicht, Behandlungspflicht) und Akzeptanzkriterien (wer entscheidet, was akzeptabel ist) festgelegt.

## Beschreibung

### Vorgaben zum Umgang mit Risiken (Folie 14)

| Risikoklasse | Vorgaben zum Umgang |
|---|---|
| **hoch** | Meldepflichtig, Meldung muss umgehend erfolgen. Risiko muss im Risikomanagement aufgenommen, dokumentiert und im regelmäßigen Reporting aufgeführt werden. **Risikobehandlung ist zwingend erforderlich.** |
| **mittel** | Meldepflichtig. Risiko muss im RiskMgmt aufgenommen, dokumentiert, regelmäßig berichtet werden. Risikobehandlung ist erforderlich; **Ausnahmen sind durch die Geschäftsführung zu genehmigen**. |
| **gering** | Meldepflichtig. **Risikobehandlung nur erforderlich, wenn vom Aufwand vertretbar.** Analysieren, ob Kumulierungseffekte auftreten könnten. |

### Risikoakzeptanzkriterien (Folie 15)

| Risikoklasse | Akzeptanz |
|---|---|
| **hoch** | unzulässig (kein Akzeptanz-Spielraum) |
| **mittel** | Bei Leib & Leben: unzulässig. Bei anderen Schadensszenarien: Geschäftsführung entscheidet. |
| **gering** | Abteilungsleitung kann nur eigene Risiken akzeptieren. |

**Kerngedanken:**
- **Wer akzeptiert, ist abhängig von der Klasse:** Je höher das Risiko, desto höher in der Hierarchie muss die Entscheidung liegen.
- **Leib & Leben** ist eine Sonder-Achse: Auch ein „mittel"-Risiko ist unzulässig, wenn es körperliche Unversehrtheit gefährdet.
- **Kumulierungseffekte:** Mehrere geringe Risiken können zusammen nicht mehr gering sein.

## Bestandteile / Aufbau

| Klasse | Meldepflicht | Behandlung | Akzeptanz |
|---|---|---|---|
| hoch | umgehend | zwingend | unzulässig |
| mittel | ja | ja, mit Ausnahmen durch GF | nur durch GF, bei Leib & Leben unzulässig |
| gering | ja | aufwandsabhängig | Abteilungsleitung |

## Beispiel

Krankenhaus: Risiko „Ransomware-Befall des KIS" → Klasse hoch → meldepflichtig, sofortige Behandlung, keine Akzeptanz möglich. Risiko „Ausfall eines einzelnen Druckers in der Verwaltung" → Klasse gering → Akzeptanz durch Abteilungsleitung der Verwaltung möglich.

## Abgrenzung

- **Risikoklasse ≠ Risikoauswirkung allein:** Klasse ergibt sich aus Wahrscheinlichkeit × Auswirkung über die Risikomatrix (siehe [[ASP - Risikomanagement - Risikomatrix]]).
- **Akzeptanz vs. Behandlung:** Akzeptanz ist eine Variante der Behandlung – siehe [[ASP - Risikomanagement - Risikobehandlung]] (4 Strategien).
- **Akzeptanz ≠ Ignorieren:** Auch akzeptierte Risiken müssen dokumentiert und überwacht werden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Vorgaben gelten für hohe, mittlere und geringe Risiken? Wer darf jeweils welche Risiken akzeptieren?

**Anwendungsfrage:** Welche Klasse hat ein konkretes Risiko? Wer entscheidet bei einer Klassen-mittel-Bedrohung der körperlichen Unversehrtheit? (Antwort: Unzulässig – nicht akzeptabel.)

**Diskussionsfrage:** Warum wird bei Leib-&-Leben-Risiken auch in Klasse „mittel" unzulässig markiert? (Wertentscheidung: persönliche Unversehrtheit hat einen anderen Stellenwert als finanzielle Schäden.) Welche Vorteile hat die explizite Eskalations-Hierarchie für Akzeptanzentscheidungen?

**Mögliche Anschlussfragen:**
- Was sind Kumulierungseffekte? (Mehrere geringe Risiken summieren sich zu einem höheren Risiko.)
- Wie ändert sich die Klasse durch eine Risikobehandlungs-Maßnahme?
- Wie hängt das mit der Risiko-Eigner-Rolle zusammen?

## Verwandt

- [[ASP - Risikomanagement - Risikomatrix]]
- [[ASP - Risikomanagement - Kontextbestimmung]]
- [[ASP - Risikomanagement - Risikobehandlung]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 14, 15
