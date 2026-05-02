---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - ITIL Practice - Service Level Management

> [!info] Kurzdefinition
> ITIL-4-Practice (Service Management) zum Festlegen klarer geschäftsbezogener Ziele für Service Levels und Sicherstellen, dass die Erbringung eines Service anhand dieser Ziele entsprechend bewertet, überwacht und gemanagt wird. SLAs sind dokumentierte Vereinbarungen mit dem Kunden über benötigte Services und erwartete Service Levels.

## Beschreibung

Folie 101 definiert:

**Zweck:**
> „Das Festlegen klarer geschäftsbezogener Ziele für Service Levels und das Sicherstellen, dass die Erbringung eines Service anhand dieser Ziele entsprechend bewertet, überwacht und gemanagt wird."

**Definition Service Level Agreement (SLA):**
> „Eine dokumentierte Vereinbarung zwischen einem Service Provider und einem Kunden, die sowohl die benötigten Services als auch den erwarteten Service Level identifiziert."

**Wichtige Anforderungen für SLAs (Folie 102):**

- Sie müssen sich auf einen definierten „Service" im Servicekatalog beziehen; andernfalls sind sie einfach nur einzelne Messgrößen ohne Zweck und bieten keine angemessene Transparenz oder spiegeln die Perspektive des Service nicht wider.
- Sie sollten sich auf definierte Ergebnisse und nicht einfach auf betriebliche Messgrößen beziehen. Dies kann durch einen ausgewogenen Satz von Messgrößen erreicht werden, z. B. Kundenzufriedenheit.
- Sie sollten eine „Vereinbarung" widerspiegeln, d. h. die Interaktion und Diskussion zwischen dem Service Provider und dem Servicekonsumenten. Es ist wichtig, alle Stakeholder zu beteiligen, einschließlich der Partner, Sponsoren, Anwender und Kunden.
- Sie müssen einfach geschrieben und für alle Parteien leicht zu verstehen und umzusetzen sein.

Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Bestandteile / Aufbau

| Anforderung | Inhalt |
|---|---|
| Bezug auf Service | SLA muss sich auf einen Servicekatalog-Service beziehen |
| Outcome-Bezug | Definierte Ergebnisse statt nur betrieblicher Messgrößen; ausgewogener Satz (z. B. Kundenzufriedenheit) |
| Vereinbarungs-Charakter | Beteiligung aller Stakeholder (Partner, Sponsoren, Anwender, Kunden) |
| Verständlichkeit | Einfach geschrieben, für alle Parteien klar |

Definition SLA: „Dokumentierte Vereinbarung zwischen Service Provider und Kunden, die sowohl benötigte Services als auch erwartete Service Levels identifiziert."

## Beispiel

Krankenhaus-IT, SLA für KIS-Service:
- Bezug: Service „Krankenhausinformationssystem" (im Katalog).
- Outcome: 99,5 % monatliche Verfügbarkeit, 5 Sek. mittlere Antwortzeit, Kundenzufriedenheit ≥ 80 %.
- Stakeholder: IT-Leitung, Pflegeleitung, Geschäftsführung, KIS-Hersteller, Datenschutzbeauftragter.
- Sprache: ohne IT-Jargon, mit klaren Definitionen.

## Abgrenzung

- **SLM-Practice vs. SLA-Dokument** (siehe [[SM - SLA - Definition und Inhalte]]): Die Practice ist der Steuerungsprozess; das SLA ist das Vertragsdokument.
- **SLM vs. Service Catalogue Management**: SLM stellt sicher, dass SLAs den Catalogue-Services entsprechen. Beide Practices arbeiten eng zusammen.
- **SLM vs. Reporting / Measurement and Reporting**: SLM definiert die Ziele; Measurement and Reporting misst und berichtet.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Zweck der Service Level Management Practice? — Klare geschäftsbezogene Ziele für Service Levels festlegen; Erbringung anhand dieser Ziele bewerten/überwachen/managen.

**Definition SLA:** Dokumentierte Vereinbarung zwischen Service Provider und Kunde mit Identifikation der benötigten Services und erwarteten Service Levels.

**Welche 4 Anforderungen für SLAs?** Bezug auf Service im Katalog, Outcome-Bezug (statt nur Messgrößen), Vereinbarungs-Charakter, Verständlichkeit.

**Diskussionsfrage:** Warum reicht eine reine SLA-Messgröße (z. B. „99,5 % Verfügbarkeit") nicht aus? — Sie spiegelt nicht die Outcome-Perspektive wider; was nutzt 99,5 % Verfügbarkeit, wenn die Antwortzeit unzumutbar oder der Service nicht das tut, was Anwender brauchen? — daher ausgewogener Satz von Messgrößen inkl. Kundenzufriedenheit.

**Mögliche Anschlussfragen:**
- Wie hängt SLM mit dem Servicekatalog zusammen?
- Was sind typische SLA-Inhalte (siehe [[SM - SLA - Definition und Inhalte]])?
- Welche Rolle spielt Cloud Computing für SLM ([[SM - ITIL 4 - Cloud Computing Auswirkungen]])?
- Wie unterscheidet sich SLA von OLA und UC? — *Im PDF nicht definiert*; OLA/UC werden im Foliensatz nicht thematisiert.

## Verwandt

- [[SM - SLA - Definition und Inhalte]]
- [[SM - Service-Level - Utility vs Warranty]]
- [[SM - ITIL Practice - Service Request Management]]
- [[SM - IT-Service-Katalog - Sichten und Strukturierung]]
- [[SM - 5 Phasen - serviceorientierte IT-Organisation]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 101–102; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
