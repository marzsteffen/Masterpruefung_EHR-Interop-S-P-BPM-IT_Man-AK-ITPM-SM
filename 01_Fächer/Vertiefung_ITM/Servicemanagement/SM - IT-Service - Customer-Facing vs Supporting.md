---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - ITSM Einführung Text]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - IT-Service - Customer-Facing vs Supporting

> [!info] Kurzdefinition
> Customer-Facing Services (kundengerichtete Services) werden direkt für Endkunden oder Mitarbeiter der Fachabteilungen bereitgestellt. Supporting Services (unterstützende Services) sind Services, die von anderen IT-Services konsumiert werden und für den Endnutzer nicht direkt sichtbar sind.

## Beschreibung

Allweyer beschreibt in Abbildung 35 (Seite 129, nach [Ko20], modifiziert), dass ein IT-Service selbst wieder andere IT-Services verwenden kann. Beispiel im Text: Der Service „Zugang zum Personalmanagement-System" nutzt unter anderem den unterstützenden Service „Datenbank-Zugang". Auch dieser benötigt wiederum verschiedene Leistungen und Produkte — Mitarbeiter, Prozesse usw.

Die Services, die für Endkunden oder Mitarbeiter der Fachabteilungen bereitgestellt werden, werden als **kundengerichtete Services** (englisch *Customer-Facing Services*) bezeichnet. Die Leistungen in der unteren Ebene können prinzipiell ebenfalls als unterstützende Services betrachtet werden. Hier muss entschieden werden, bis zu welchen detaillierten Einzelleistungen es sinnvoll ist, sie als Services zu definieren und explizite Service-Beschreibungen mit Qualitätsanforderungen zu erstellen.

## Bestandteile / Aufbau

Hierarchie laut Abbildung 35:

| Ebene | Beispiel aus Allweyer |
|---|---|
| Kundengerichtete Services | Service A, Service „Zugang zum Personalmanagement-System", Service B |
| Unterstützende Services | Service X, Service Y, Service „Datenbank-Zugang", Service Z |
| Leistungen / Produkte (unterste Ebene, Team-zugeordnet) | Leistung „Hotline" (Team A), Leistung „Datenbank-Administration" (Team B), Produkt „Datenbank-Lizenz", Produkt „Datenbank-Server", Leistung „Hardware-Support" (Team C) … |

Anmerkung: Die unterste Ebene (Leistungen/Produkte) zeigt, welches Team welche Bausteine erbringt — Service-Erbringung ist also auch eine organisatorische Frage.

## Beispiel

Service „Zugang zum Personalmanagement-System" (kundengerichtet)
→ konsumiert Service „Datenbank-Zugang" (unterstützend)
→ konsumiert Leistung „Datenbank-Administration" (Team B), Produkt „Datenbank-Lizenz" (Team B), Produkt „Datenbank-Server" (Team B), Leistung „Hardware-Support" (Team C) etc.

## Abgrenzung

- **Customer-Facing vs. Business-Service:** Ein Customer-Facing Service kann ein Business-Service sein (extern angeboten) oder ein interner Service für Fachabteilungen — die Abgrenzung zum Business-Service (siehe [[SM - IT-Service - Business vs IT Service]]) verläuft über die Frage, wer der Kunde ist (externer Kunde vs. interne Fachabteilung).
- **Supporting Service vs. Komponente:** Wo Service endet und Komponente beginnt, ist eine Designentscheidung — Allweyer benennt sie explizit als nicht eindeutig.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen einem kundengerichteten und einem unterstützenden Service? — Sichtbarkeit für den Endkunden bzw. Endnutzer; unterstützende Services werden von anderen Services konsumiert.

**Anwendungsfrage:** Zeichnen Sie für eine Service-Hierarchie (z. B. „Mailservice für Mitarbeiter") die Customer-Facing- und Supporting-Ebenen ein.

**Diskussionsfrage:** Bis zu welcher Granularität sollten Supporting Services als eigene Services modelliert werden? Trade-off: zu fein → Verwaltungsaufwand und unklare Verantwortung; zu grob → mangelnde Wiederverwendbarkeit, schlechte SLAs zwischen Teams.

**Mögliche Anschlussfragen:**
- Gehört ein interner Service immer in den Servicekatalog, oder nur Customer-Facing Services?
- Wie verhält sich diese Hierarchie zu den OLAs/UCs in der Service-Erbringung? *(OLA/UC im PDF nicht definiert; wird im Foliensatz erwartet)*
- Welche Konsequenzen hat die Ebene für SLAs (siehe [[SM - SLA - Definition und Inhalte]])?

## Verwandt

- [[SM - IT-Service - Definition]]
- [[SM - IT-Service - Business vs IT Service]]
- [[SM - Service-Katalog - Definition und Aufbau]]
- [[SM - SLA - Definition und Inhalte]]

## Quelle

- Vorlesung: [[SM - VL - ITSM Einführung Text]]
- Folien/Seitenangabe: Buchseite 128–129, Abbildung 35 (nach [Ko20], modifiziert)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
