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

# SM - ITSM - IT-Dienstleistungsverrechnung

> [!info] Kurzdefinition
> Bezugsgrößen für die Verrechnung von IT-Dienstleistungen werden je nach Servicebereich unterschiedlich gewählt: Rechenzentrum nach CPU-Zeit und Speicherplatz, Systemhaus nach Personentagen und Lizenzkosten, PC/LAN nach Betreuung und SW-Lizenzen, Telekommunikation nach Gebühren und Wartungskosten.

## Beschreibung

Folie 30 (Quelle: Kutscha & Meier 2007) listet vier typische IT-Servicebereiche und ihre jeweiligen Verrechnungsgrößen — eine sehr praxisnahe Zuordnung. Die Folie ist knapp gehalten; die Zuordnung in eine Tabelle ist die kompakteste Darstellung.

## Bestandteile / Aufbau

| Servicebereich | Verrechnungsgrößen |
|---|---|
| Rechenzentrum | CPU-Zeit · Speicherplatz |
| Systemhaus | Personentage · Lizenzkosten |
| PC/LAN | Betreuung · SW-Lizenzen |
| Telekommunikation | Gebühren · Wartungskosten |

## Beispiel

Aus Krankenhaus-Sicht:

- Hosting des KIS auf eigenem Rechenzentrum → Verrechnung an Trägerverband: CPU-Zeit + Speicherplatz pro Mandant.
- Inhouse-Beratung durch das Systemhaus zu einer ELGA-Anbindung → Personentage + Lizenzkosten der erforderlichen Tools.
- PC/LAN-Support für Stationen → Pauschale Betreuung pro Arbeitsplatz + SW-Lizenzen (Office, KIS-Client).
- Telefonie → laufende Gebühren + Wartungskosten der TK-Anlage.

## Abgrenzung

- **Verrechnungsgrößen vs. SLA-Inhalte** (siehe [[SM - SLA - Definition und Inhalte]]): Verrechnung ist Teil des SLA-Inhalts (Punkt „Preise und Verrechnungsmethoden"); die Bezugsgrößen sind die zugrunde liegenden Maßeinheiten.
- **Verrechnung intern vs. extern**: Allweyer (siehe [[SM - IT-Servicemanagement - Aufgaben und Kernprozesse]]) betont, dass intern und extern erbrachte IT-Services im Prinzip dieselbe Verrechnungslogik verwenden — zugehörige Bezugsgrößen sind aber typischerweise Verrechnungspreise statt Marktpreise.
- **Bezugsgrößen vs. Kennzahlen**: Verrechnungsbezugsgrößen messen die Inanspruchnahme; Service-Level-Kennzahlen messen die Service-Qualität.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Nennen Sie typische Bezugsgrößen für die IT-Dienstleistungsverrechnung (laut Kutscha & Meier). — RZ: CPU-Zeit/Speicherplatz; Systemhaus: Personentage/Lizenzkosten; PC/LAN: Betreuung/SW-Lizenzen; Telekommunikation: Gebühren/Wartungskosten.

**Anwendungsfrage:** Welche Verrechnungsmethode ist für welchen Service-Typ angemessen? — Cloud-RZ-Services üblicherweise nutzungsabhängig (CPU-Stunden/Storage-GB); Beratungsleistungen Personentage; Standardarbeitsplatz pauschal.

**Diskussionsfrage:** Wie verändert Cloud Computing die klassische Verrechnungslogik? — Verschiebung von Investitionskosten zu nutzungsabhängigen Betriebskosten (siehe [[SM - ITIL 4 - Cloud Computing Auswirkungen]]). Verrechnungsbezugsgrößen werden granularer (pro API-Call, pro Stunde) und automatischer.

**Mögliche Anschlussfragen:**
- Wie hängt Verrechnung mit dem Servicekatalog zusammen?
- Welche Rolle hat die Verrechnung als „Regulativ" (Folie 28)? — Sie steuert die Nachfrage und macht Service-Konsum sichtbar.
- Welche Practice in ITIL 4 deckt Verrechnung ab? — *Im PDF nicht explizit zugeordnet*; im ITIL-4-Kontext eher Financial Service Management oder Service Financial Management.

## Verwandt

- [[SM - SLA - Definition und Inhalte]]
- [[SM - IT-Servicemanagement - Aufgaben und Kernprozesse]]
- [[SM - ITSM im Gesundheitswesen - Krankenhaus-Architektur]]
- [[SM - IT-Service-Katalog - Best Practices Gestaltung]]
- [[SM - ITIL 4 - Cloud Computing Auswirkungen]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 30; Quelle: Kutscha, A. & Meier, P. (2007), KIS-Tagung

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
