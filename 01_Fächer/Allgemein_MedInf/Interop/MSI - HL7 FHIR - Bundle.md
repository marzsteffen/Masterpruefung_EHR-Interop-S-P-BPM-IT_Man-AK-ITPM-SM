---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR Starter (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - Bundle

> [!info] Kurzdefinition
> Ein FHIR-Bundle ist ein Container-Ressourcentyp, der mehrere FHIR-Ressourcen in einer einzigen Anfrage/Antwort zusammenfasst. Bundles werden u. a. für Suchergebnisse, FHIR-Dokumente, Transaktionen und Nachrichten verwendet.

## Beschreibung

### Was ist ein Bundle?

Im Vortrag wird „Was ist ein Bundle?" als Workshop-Übungsfrage gestellt (Seite 60: Beispiel 6 – Ergebnis einer `GET /Patient`-Anfrage). Der detaillierte Aufbau des Bundle-Ressourcentyps wird in den Folien nicht textuell beschrieben (Diagramm-Folie, nicht extrahierbar).

Aus dem Vortrag-Kontext erschließbar:
- Das Ergebnis von `GET /Patient` (alle Ressourcen abrufen) **ist ein Bundle** – d. h. beim Lesen aller Ressourcen eines Typs liefert die REST API ein Bundle zurück
- Bundles sind die **empfohlene Alternative zu Contained Resources** (Seite 31): „Es gibt jedoch (fast immer) bessere Lösungen durch FHIR Document (https://www.hl7.org/fhir/documents.html) oder Bundles."
- FHIR unterstützt **Dokumente und Nachrichtenübertragung** via Bundles (Seite 9: „FHIR ist mehr als nur Ressourcen")

> ⚠️ **Hinweis**: Der strukturelle Aufbau des Bundle-Ressourcentyps (Felder, Bundle-Typen wie `document`, `message`, `transaction`, `searchset`, …) ist im PDF **nicht detailliert definiert**. Die folgende Ergänzung stammt aus dem FHIR-Standard (extern).

## Ergänzung außerhalb der Vorlesung

*Aus dem FHIR-Standard (hl7.org/fhir/bundle.html), da im PDF nicht ausreichend erklärt:*

**Bundle-Typen** (das `Bundle.type`-Feld):

| Type | Verwendung |
|---|---|
| `document` | FHIR-Dokument (unveränderliche Momentaufnahme) |
| `message` | FHIR-Nachricht (Event-basiert, wie HL7 v2 Nachricht) |
| `transaction` | Atomare Gruppe von Operationen (alles oder nichts) |
| `transaction-response` | Antwort auf eine Transaction |
| `batch` | Gruppe von Operationen (nicht atomar) |
| `searchset` | Ergebnis einer FHIR-Suchanfrage |
| `collection` | Generische Sammlung von Ressourcen |
| `history` | Versionshistorie |

Ein Bundle enthält: `type`, `total` (bei searchset), `link` (Paginierung), `entry` (Liste von Ressourcen mit URL und Metadaten).

## Abgrenzung

- **Bundle** vs. **Contained Resources**: Contained Resources betten Ressourcen inline in eine andere ein (Anti-Pattern). Bundles sind eigenständige Container-Ressourcen, die als eigenständige Entitäten transportiert werden.
- **Bundle** vs. **Dokument**: Ein FHIR-Dokument ist ein Bundle mit `type=document` und einer Composition-Ressource als erstem Entry – also eine Spezialisierung.
- **Bundle** ist eine `Resource` (nicht `DomainResource`) – kein Narrative, nicht erweiterbar.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein FHIR-Bundle und wann wird es verwendet?

**Anwendungsfrage:** Wie gibt die FHIR REST API das Ergebnis einer Suche (`GET /Patient?name=Muster`) zurück? (→ Als Bundle vom Typ `searchset`)

**Diskussionsfrage:** Wie verwendet FHIR Bundles, um sowohl dokumentenbasierte (CDA-ähnliche) als auch nachrichtenbasierte (HL7v2-ähnliche) Szenarien abzudecken?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen einem Bundle vom Typ `transaction` und `batch`?
- Wie sieht ein FHIR-Dokument (FHIR Document) aus? (→ Bundle type=document, erster Entry ist Composition)
- Was passiert bei Paginierung bei großen Suchergebnissen? (→ Bundle.link mit `next`)

## Verwandt

- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Reference]]
- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Ressourcentypen]]
- [[MSI - HL7 FHIR - Paradigmen]]
- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 - International Patient Summary]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 9, 31, 60 (Bundle-Struktur im PDF nicht textuell definiert – Diagramm)
