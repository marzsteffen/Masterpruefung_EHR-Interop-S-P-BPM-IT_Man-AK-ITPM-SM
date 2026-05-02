---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Einführung und Definitionen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Architektur - Registry vs Repository

> [!info] Kurzdefinition
> Designfrage, ob ein EHR-System die eigentlichen Daten **selbst speichert** (Repository) oder nur **Verweise** auf Daten in den Quellsystemen führt (Registry). Beeinflusst Synchronisation, Verfügbarkeit und Latenz.

## Beschreibung

Die Vorlesung adressiert die Frage in Folien 39 und 46:

- Folie 39: „Repository or 'on the fly accumulation'?"
- Folie 46: „Data integration – Data from any source which is not directly in the EHR, but where the EHR has a link to – Requires good synchronization – **Registry versus repository**"

**Repository:** Das EHR-System speichert alle Daten selbst. Vorteil: schneller Zugriff, kein externes System nötig. Nachteil: redundante Speicherung, Synchronisations-Aufwand, doppelte Datenhaltung.

**Registry / On-the-fly Accumulation:** Das EHR-System hält nur Verweise (Pointer/Links) auf Daten, die in den Quellsystemen verbleiben. Die Daten werden bei Bedarf zusammengezogen. Vorteil: keine Doppelung, immer aktuell. Nachteil: Verfügbarkeit hängt von den Quellsystemen ab; Synchronisation muss exakt funktionieren.

## Bestandteile / Aufbau

Vergleichsachsen (aus dem PDF ableitbar):

| Achse | Repository | Registry |
|---|---|---|
| Datenhaltung | Daten lokal kopiert | nur Verweise |
| Aktualität | abhängig von Sync | immer aktuell, sofern Quelle erreichbar |
| Verfügbarkeit | unabhängig von Quelle | abhängig von Quelle |
| Synchronisation | aufwendig | entfällt, aber Quell-Konsistenz nötig |
| Antwortzeit | typischerweise schneller | Latenz beim Zusammenziehen |

## Beispiel

PDF: ein EHR, das Bilder nicht selbst speichert, sondern auf das **PACS** (Picture Archiving and Communication System) verlinkt, ist in diesem Aspekt eine Registry. Ein EHR, das Befunde, Diagnosen und Medikationen lokal als Kopien hält, ist Repository.

Begriffe **PACS, RIS, LIS, HIS** werden im PDF erwähnt, aber nicht erklärt.

## Abgrenzung

- Eng verwandt mit, aber nicht identisch zu [[EHR - Architektur - Zentral vs Dezentral]]: Eine **zentrale Registry** ist möglich (zentraler Index, dezentrale Speicherung) – z. B. als Architekturmuster vieler nationaler EHRs.
- Im PDF wird Folie 46 explizit unter der Anforderung „Data Entry / Data Integration" geführt – das macht es zu einer **funktionalen Anforderung**, nicht nur einer Architekturfrage.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen einem EHR-Repository und einer EHR-Registry?

**Anwendungsfrage:** Welche Daten würdest du im Repository halten, welche per Registry-Verweis – und warum? (z. B. Bilddaten oft nur verlinkt, Diagnosen oft kopiert)

**Diskussionsfrage:** Ist eine reine Registry praktikabel, wenn ein Quellsystem ausfällt – oder braucht es immer Cache-Strategien? Welche Konsequenzen hat das für die Verfügbarkeitsanforderung > 99,9 %?

**Mögliche Anschlussfragen:**
- Wie ist ELGA in dieser Frage einzuordnen?
- Was passiert mit der Datenhoheit, wenn das EHR Daten kopiert (Repository) anstatt zu verlinken?
- Welche Synchronisations-Mechanismen sind typisch für Repository-Architekturen? (im PDF nicht ausgeführt)

## Verwandt

- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - VL - ELGA Architektur]]
- [[MSI - IHE XDS]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folie 39 (Designfrage), Folie 46 (Data Integration: Registry vs Repository)
