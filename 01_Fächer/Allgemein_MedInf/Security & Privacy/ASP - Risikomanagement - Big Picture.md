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

# ASP - Risikomanagement - Big Picture (ISO 27005-Prozess)

> [!info] Kurzdefinition
> Sieben-Schritte-Prozess nach ISO 27005: Bestimmung des Kontexts, Risikoidentifikation, Risikoanalyse, Risikoevaluierung, Risikobehandlung, Risikokommunikation, Überwachung und Verbesserung. Von zwei Querschnitts-Aktivitäten umrahmt: Communication and Consultation, Monitoring and Review.

## Beschreibung

### Warum Risikomanagement (Folie 6)

Systematische Methode, um Risiken auch bei großer Zahl, Komplexität und damit Unüberschaubarkeit sinnvoll und vernünftig zu verwalten:
- Systematische Erfassung von Risiken.
- Vergleichbare Bewertung von Risiken.
- Ermöglichung einer Priorisierung.
- Geregelte Kommunikation von Risiken.
- Formelle Entscheidung zur Risikobehandlung.
- Definierte Verantwortliche (Risiko-Eigner, Risikomanager).
- Regelmäßige Kontrolle / Bewertung, ob bestehende Risiken sich geändert haben oder neue dazugekommen sind.

### Die sieben Schritte (Folie 7, ISO 27005-Diagramm)

1. **Bestimmung des Kontexts** (Clause 6) – Geltungsbereich, Rollen, Bewertungsskalen, Akzeptanzkriterien.
2. **Risikoidentifikation** (Clause 7.2) – ereignis-basiert oder asset-basiert.
3. **Risikoanalyse** (Clause 7.3) – Wahrscheinlichkeit und Auswirkung bewerten.
4. **Risikoevaluierung** (Clause 7.4) – Vergleich mit Akzeptanzkriterien.
5. **Risikobehandlung** (Clause 8) – Vermeidung, Reduktion, Transfer, Akzeptanz.
6. **Risikokommunikation** (Clause 10.3) – Risikobericht und Reporting.
7. **Überwachung und Verbesserung** (Clause 10.5) – KPI/KRI, kontinuierliche Verbesserung.

**Decision Points im Prozess:**
- Risk Decision Point 1: Ist das Assessment satisfactory?
- Risk Decision Point 2: Ist das Risiko akzeptiert?

Bei „Nein" geht der Prozess zurück; bei „Ja" wird die Behandlung angegangen bzw. dokumentiert.

**Querschnitts-Aktivitäten:**
- **Communication and Consultation** läuft über alle Schritte hinweg.
- **Monitoring and Review** ebenso – sichert die kontinuierliche Wirksamkeit.

Schritte 2–4 zusammen bilden das **Risk Assessment** (gestricheltes Kästchen im Diagramm).

## Bestandteile / Aufbau

| Schritt | Inhalt | Konzept-Note |
|---|---|---|
| 1. Kontextbestimmung | Geltungsbereich, Rollen, Skalen | [[ASP - Risikomanagement - Kontextbestimmung]] |
| 2. Risikoidentifikation | Asset/Bedrohung/Schwachstelle finden | [[ASP - Risikomanagement - Risikoidentifikation Ansaetze]] |
| 3. Risikoanalyse | Wahrscheinlichkeit × Auswirkung | [[ASP - Risikomanagement - Risikobewertung]] |
| 4. Risikoevaluierung | Vergleich mit Akzeptanzkriterien | [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]] |
| 5. Risikobehandlung | Vermeidung/Reduktion/Transfer/Akzeptanz | [[ASP - Risikomanagement - Risikobehandlung]] |
| 6. Risikokommunikation | Bericht und Reporting | [[ASP - Risikomanagement - Risikokommunikation]] |
| 7. Überwachung & Verbesserung | KPI, KRI | [[ASP - Risikomanagement - Ueberwachung KPI KRI]] |

## Beispiel

Ein Krankenhaus startet ein RiskMgmt: 1) Definiert Geltungsbereich (zentrales KIS) und Bewertungsskalen. 2) Identifiziert Risiken über Asset-Liste. 3) Bewertet Wahrscheinlichkeit und Auswirkung. 4) Vergleicht mit Akzeptanzkriterien (rot = unzulässig). 5) Plant Maßnahmen (Patches, Backups, Versicherung). 6) Berichtet an die Geschäftsführung. 7) Verfolgt KPIs/KRIs und passt den Prozess an.

## Abgrenzung

- **Risikomanagement-Prozess ≠ einmaliges Projekt:** Es ist ein kontinuierlicher Zyklus.
- **ISO 27005 vs. BSI 200-x:** ISO 27005 ist allgemeiner Rahmen; BSI 200-2/200-4 sind detailliertere methodische Werkzeuge (siehe [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]]).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche sieben Schritte umfasst der Risikomanagement-Prozess nach ISO 27005? Welche zwei Querschnitts-Aktivitäten umrahmen ihn?

**Anwendungsfrage:** Ordnen Sie konkrete Aktivitäten (z. B. „Bewertungsmatrix definieren", „Versicherung abschließen", „KRI festlegen") den jeweiligen Schritten zu.

**Diskussionsfrage:** Welche Schritte sind besonders unternehmenspolitisch heikel und warum? (Kontextbestimmung – Geschäftsführung muss Akzeptanzkriterien festlegen; Behandlung – Investitionsentscheidungen.) Wie hängt der Prozess mit dem PDCA-Zyklus zusammen?

**Mögliche Anschlussfragen:**
- Was passiert bei einem „Nein" am Decision Point 2?
- Warum stehen Communication und Monitoring außerhalb des Hauptzyklus?
- Welcher Standard ergänzt ISO 27005? (ISO 31000 für allgemeines Risikomanagement.)

## Verwandt

- [[ASP - Risikomanagement - Definition Risiko]]
- [[ASP - Risikomanagement - Grundvoraussetzungen]]
- [[ASP - Risikomanagement - Kontextbestimmung]]
- [[ASP - BCM - Risikoanalyse]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 6, 7
- Standard: ISO/IEC 27005:2022 – Diagramm und Clause-Nummern
