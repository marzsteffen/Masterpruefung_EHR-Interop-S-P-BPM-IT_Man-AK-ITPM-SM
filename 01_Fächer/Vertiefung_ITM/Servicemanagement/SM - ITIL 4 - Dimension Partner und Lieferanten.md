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

# SM - ITIL 4 - Dimension Partner und Lieferanten

> [!info] Kurzdefinition
> Dritte der Vier Dimensionen von ITIL 4. Adressiert die Beziehungen zu externen Partnern und Lieferanten: deren Abhängigkeit zur Organisation und ihre Beteiligung am Entwurf, der Entwicklung, dem Einsatz, der Bereitstellung, dem Support und/oder der kontinuierlichen Verbesserung der Services.

## Beschreibung

Folie 58 listet für Dimension 3:

- Abhängigkeit
- Beteiligung an Services: Entwurf, Entwicklung, Einsatz, Bereitstellung, Support und/oder kontinuierlicher Verbesserung

Diese Dimension erkennt an, dass moderne Services selten von einer Organisation allein erbracht werden — Lieferanten (Cloud-Anbieter, Software-Hersteller, Outsourcing-Partner) und strategische Partner sind integraler Bestandteil der Service-Erbringung.

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Abhängigkeit | Wie kritisch ist der Partner/Lieferant für die Service-Erbringung? |
| Beteiligung Entwurf | Z. B. Hersteller bringt Spezialwissen ins Service-Design ein |
| Beteiligung Entwicklung | Z. B. externe Entwickler bauen am Service mit |
| Beteiligung Einsatz | Z. B. Implementierungspartner |
| Beteiligung Bereitstellung | Z. B. Cloud-Anbieter stellt Infrastruktur bereit |
| Beteiligung Support | Z. B. Hersteller-Support 2nd/3rd Level |
| Beteiligung kontinuierlicher Verbesserung | Z. B. Hersteller liefert Feature-Updates basierend auf Feedback |

## Beispiel

Aus Krankenhaus-Sicht:

- **KIS-Hersteller** als zentraler Lieferant — Beteiligung an Entwurf (Anforderungsworkshops), Bereitstellung (Hosting), Support (Hotline 2nd Level), Verbesserung (Feature-Updates).
- **Cloud-Anbieter** für ELGA-Anbindung — Bereitstellung (Infrastruktur), Sicherheit (Compliance).
- **Outsourcing-Partner** für 1st-Level-Service-Desk — Bereitstellung, Support.

Die Abhängigkeit ist hoch: Bei Ausfall der Cloud kann KIS nicht mehr genutzt werden — das hat Implikationen für SLAs (siehe [[SM - SLA - Definition und Inhalte]]: Verantwortungsbereich) und für Continuity-Planung.

## Abgrenzung

- **Dimension 3 vs. Dimension 1**: Dimension 1 sind interne Menschen und Organisation; Dimension 3 sind *externe* Partner und Lieferanten.
- **Dimension 3 vs. Supplier Management Practice**: Supplier Management ist die General Management Practice in ITIL 4, die Aspekte dieser Dimension operationalisiert (Auswahl, Verträge, Lieferantenmanagement).
- **Dimension 3 vs. Sourcing-Strategie**: Sourcing ist Teil der IT-Strategie ([[SM - IT-Strategie - 7 Schritte nach Johanning]] Schritt 4) und legt Make-or-Buy fest; Dimension 3 ist die laufende Steuerung der gewählten Sourcing-Konstellationen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Aspekte umfasst Dimension 3 „Partner und Lieferanten"? — Abhängigkeit, Beteiligung an Services (Entwurf, Entwicklung, Einsatz, Bereitstellung, Support, kontinuierliche Verbesserung).

**Anwendungsfrage:** Wer sind typische Partner/Lieferanten einer Krankenhaus-IT? Welche Abhängigkeiten und Beteiligungen? — KIS-Hersteller, Cloud-Anbieter, IT-Outsourcer, eHealth-Plattformen, Hardware-Lieferanten.

**Diskussionsfrage:** Wie verhindern Sie Lock-in bei hoher Abhängigkeit von einem Kern-Lieferanten? — Multi-Vendor-Strategien, Standardschnittstellen (FHIR, HL7), Exit-Klauseln in Verträgen, eigene Kompetenz halten.

**Mögliche Anschlussfragen:**
- Welche Practice operationalisiert diese Dimension? — Supplier Management.
- Wie verhält sich diese Dimension zur Sourcing-Strategie der IT?
- Welche Risiken folgen aus hoher Lieferantenabhängigkeit, und wie werden sie über Service Continuity Management adressiert?

## Verwandt

- [[SM - ITIL 4 - Four Dimensions]]
- [[SM - IT-Strategie - 7 Schritte nach Johanning]]
- [[SM - SLA - Definition und Inhalte]]
- [[SM - ITIL 4 - Cloud Computing Auswirkungen]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 58; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
