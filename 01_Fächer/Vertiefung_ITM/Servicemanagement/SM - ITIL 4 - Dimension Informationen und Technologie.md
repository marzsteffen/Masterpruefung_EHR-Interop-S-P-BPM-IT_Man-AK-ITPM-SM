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

# SM - ITIL 4 - Dimension Informationen und Technologie

> [!info] Kurzdefinition
> Zweite der Vier Dimensionen von ITIL 4. Adressiert die Informations- und Technologiekomponenten, die Service-Erbringung ermöglichen: Workflow-Management-Systeme, Wissensdatenbanken, Bestandssysteme, Kommunikationssysteme, Analysetools sowie Sicherheit und Compliance.

## Beschreibung

Folie 58 listet für Dimension 2:

- Workflow-Management-Systeme
- Wissensdatenbanken
- Bestandssysteme
- Kommunikationssysteme
- Analysetools
- Sicherheit und Compliance

Diese Dimension umfasst zwei Begriffspaare:
- **Information:** Daten, Wissen, Informationsflüsse, Informationsstruktur (Wissensdatenbanken, Bestandssysteme).
- **Technologie:** Werkzeuge und Systeme zur Service-Erbringung (Workflow-Management, Kommunikationssysteme, Analysetools). Sicherheit und Compliance werden hier als Querschnittsthema platziert.

Folie 61 (Test-Frage) klärt eine wichtige Abgrenzung: „Rollen und Verantwortlichkeiten" gehört *nicht* zu Dimension 2, sondern zu Dimension 1.

Folien 62–63 vertiefen die Dimension am Beispiel **Cloud Computing** (siehe [[SM - ITIL 4 - Cloud Computing Auswirkungen]]).

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Workflow-Management-Systeme | Tools zur Prozesssteuerung (Ticketing, Approvals) |
| Wissensdatenbanken | Strukturiertes Wissen, KEDB (Known-Error-Database), Service-Knowledge-Management |
| Bestandssysteme | CMDB, Asset-Management |
| Kommunikationssysteme | E-Mail, Chat, Telefonie, Collaboration-Tools |
| Analysetools | Reporting, Dashboards, KI/Analytics |
| Sicherheit und Compliance | Information Security, Datenschutz, regulatorische Anforderungen |

## Beispiel

Aus Krankenhaus-Sicht:

- **Workflow-Management:** ITSM-Tool für Tickets (z. B. ServiceNow, OTRS).
- **Wissensdatenbanken:** KEDB für wiederkehrende KIS-Probleme; Knowledge Base für 1st-Level-Support.
- **Bestandssysteme:** CMDB mit allen Krankenhaus-Geräten (Server, OP-Geräte, Mobil-Devices).
- **Kommunikationssysteme:** DECT-Telefonie, Pflegeruf-Systeme.
- **Analysetools:** Power BI für Service-Level-Reporting.
- **Sicherheit:** DSGVO, Klinikum-Sicherheitsrichtlinien, ggf. ISO 27001.

## Abgrenzung

- **Dimension 2 vs. Dimension 1**: Dimension 2 ist *Werkzeuge und Daten*; Dimension 1 ist *Menschen und Organisation*. Beide hängen voneinander ab — die beste Wissensdatenbank nützt nichts, wenn sie nicht von Menschen befüllt und genutzt wird.
- **Dimension 2 vs. Compliance** (siehe [[SM - Compliance - Definition]]): Compliance wird hier als ein Aspekt von Dimension 2 geführt — als Sicherheits- und Regelthema. Compliance reicht aber breiter (Verträge, Buchhaltung etc.), das ist im PDF nicht weiter ausgeführt.
- **Dimension 2 vs. EBEL-„IT"**: EBEL hat eine simple „IT"-Komponente; ITIL 4 differenziert in Information *und* Technologie und betont Wissensaspekte explizit.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Aspekte umfasst Dimension 2 „Informationen und Technologie"? — Workflow-Management-Systeme, Wissensdatenbanken, Bestandssysteme, Kommunikationssysteme, Analysetools, Sicherheit und Compliance.

**Anwendungsfrage:** Was ist *kein* zentraler Fokus dieser Dimension? — Rollen und Verantwortlichkeiten (gehört zu Dimension 1).

**Diskussionsfrage:** Warum ist „Sicherheit und Compliance" in dieser Dimension verankert und nicht in einer eigenen Dimension? — Weil Sicherheit und Compliance maßgeblich technologisch und informationsbasiert umgesetzt werden (Verschlüsselung, Zugriffsmanagement, Audit-Logs); allerdings haben sie auch organisatorische Anteile (Dimension 1).

**Mögliche Anschlussfragen:**
- Welche Auswirkungen hat Cloud Computing auf diese Dimension? — Siehe [[SM - ITIL 4 - Cloud Computing Auswirkungen]].
- Welche ITIL-4-Practices fallen schwerpunktmäßig in diese Dimension? — Information Security Management, Knowledge Management, Service Configuration Management.
- Wie verhält sich diese Dimension zur CMDB?

## Verwandt

- [[SM - ITIL 4 - Four Dimensions]]
- [[SM - ITIL 4 - Cloud Computing Auswirkungen]]
- [[SM - ITIL Practice - Service Configuration Management]]
- [[SM - Compliance - Definition]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folie 58 (Aspekte), Folie 61 (Test-Frage), Folien 62–63 (Cloud-Beispiel); Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
