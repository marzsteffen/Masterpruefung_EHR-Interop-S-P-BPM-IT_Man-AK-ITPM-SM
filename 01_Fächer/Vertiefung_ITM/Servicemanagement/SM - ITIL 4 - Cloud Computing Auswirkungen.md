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

# SM - ITIL 4 - Cloud Computing Auswirkungen

> [!info] Kurzdefinition
> Cloud Computing verschiebt die Service-Erbringung vom betriebsinternen Hosting zum Cloud-Service eines Partners — mit weitreichenden Auswirkungen auf das ITSM: veränderte Kostenstrukturen, höhere Anforderungen an Netzwerkverfügbarkeit, neue Sicherheits- und Compliance-Risiken — und Veränderungen in zahlreichen ITIL-4-Practices.

## Beschreibung

Folien 62–63 vertiefen die Dimension „Informationen und Technologie" am Beispiel **Cloud Computing**.

**Auswirkungen des Cloud Computing auf das ITSM** (Folie 62):

- Ersetzt die zuvor verwaltete Infrastruktur durch einen Cloud Service eines Partners.
- Reduziert oder eliminiert den Bedarf an Fachwissen und Ressourcen für das Infrastrukturmanagement.
- Verschiebt den Schwerpunkt von der Serviceüberwachung und -verwaltung von der betriebsinternen Infrastruktur in die Cloud.
- Ändert die Kostenstrukturen: spezifische Investitionskosten werden eliminiert, neue Betriebskosten eingeführt (CAPEX → OPEX).
- Höhere Anforderungen an die Netzwerkverfügbarkeit.
- Führt zu neuen Sicherheits- und Compliance-Risiken.

**Cloud Computing verändert Practices** (Folie 63). Zu den betroffenen Practices gehören unter anderem:

- Service Level Management
- Measurement and Reporting
- Information Security Management
- Service Continuity Management
- Supplier Management
- Incident Management
- Problem Management
- Service Request Management
- Service Configuration Management

Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Bestandteile / Aufbau

| Veränderung | Auswirkung |
|---|---|
| Infrastruktur-Eigentum | Eigene Hardware → Cloud-Service eines Partners |
| Fachwissen | Weniger eigenes Infrastruktur-Know-how erforderlich |
| Überwachung | Verschiebt sich in die Cloud |
| Kosten | CAPEX → OPEX |
| Netzwerk | Höhere Verfügbarkeitsanforderungen |
| Sicherheit / Compliance | Neue Risikolage (Datenstandort, Datenschutz, Vendor-Lock-in) |

## Beispiel

Aus Krankenhaus-Sicht: Migration der KIS-Datenbank in eine zertifizierte Health-Cloud.

- **Vorher:** eigenes RZ, hohe Investitionskosten, eigene Admins, hauseigene Sicherheit.
- **Nachher:** Cloud-Service, monatliche Betriebskosten, weniger eigene Admins, neue Compliance-Fragen (DSGVO-Datenstandort EU, Patientendaten in Cloud), höhere Anforderungen an die Internet-Anbindung des Hauses (siehe auch SLA-Verfügbarkeit Verantwortungsbereich → [[SM - SLA - Definition und Inhalte]]).

## Abgrenzung

- **Cloud-Computing-Auswirkungen vs. Outsourcing allgemein**: Cloud ist eine spezielle Form des Outsourcing (technologisch vereinheitlicht, oft public). Klassisches Outsourcing kann auch dedicated bleiben. Auswirkungen ähneln sich, aber Cloud ist meist standardisierter.
- **Cloud-Computing vs. SaaS**: SaaS (Software-as-a-Service) ist eine Cloud-Bereitstellungsform; daneben gibt es PaaS und IaaS. *Im Foliensatz nicht weiter differenziert.*
- **Cloud-Computing vs. Dimension 3 (Partner und Lieferanten)** (siehe [[SM - ITIL 4 - Dimension Partner und Lieferanten]]): Cloud-Anbieter sind ein konkretes Beispiel für die in Dimension 3 thematisierten Partner.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Auswirkungen hat Cloud Computing auf das ITSM? — Verschiebung Infrastruktur → Cloud, weniger Infrastruktur-Know-how, Kostenstruktur CAPEX→OPEX, höhere Netzwerkanforderungen, neue Sicherheits-/Compliance-Risiken.

**Anwendungsfrage:** Welche Practices sind besonders betroffen? — SLM, Measurement+Reporting, Information Security, Service Continuity, Supplier, Incident, Problem, Service Request, Service Configuration.

**Diskussionsfrage:** Welche Compliance-Fragen ergeben sich aus der Cloud-Nutzung im Krankenhaus? — DSGVO-Datenstandort (EU), Verarbeitungsverträge, Patientendaten-Hoheit, Auftragsverarbeitung, Privacy-Shield/Standardvertragsklauseln, Datentransfer in Drittländer (USA).

**Mögliche Anschlussfragen:**
- Wie verändert sich die SLA-Logik bei Cloud-Services? — Verantwortungsbereich-Argument: Anbieter kann die eigene Cloud garantieren, nicht aber die Kunden-Internetanbindung.
- Welche Risiken bestehen bei Vendor-Lock-in? — Datenmigration teuer, Abhängigkeit von Anbieterpolitik.
- Wie hängt Cloud Computing mit der „Optimierung und Automatisierung" als Grundprinzip zusammen ([[SM - ITIL 4 - Sieben Grundprinzipien]])?

## Verwandt

- [[SM - ITIL 4 - Dimension Informationen und Technologie]]
- [[SM - ITIL 4 - Dimension Partner und Lieferanten]]
- [[SM - SLA - Definition und Inhalte]]
- [[SM - ITSM - IT-Dienstleistungsverrechnung]]
- [[SM - Privacy by Design - DSGVO]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 62–63; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
