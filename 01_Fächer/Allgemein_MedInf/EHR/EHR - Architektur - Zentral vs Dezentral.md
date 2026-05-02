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

# EHR - Architektur - Zentral vs Dezentral

> [!info] Kurzdefinition
> Designfrage, ob Patientendaten in einem **zentralen Repository** abgelegt oder **dezentral** bei den datenerzeugenden Versorgern verbleiben (und nur bei Bedarf zusammengeführt werden). Eine der zentralen Architektur-Entscheidungen für ein EHR.

## Beschreibung

Vorlesung Folie 39: „Some interesting design questions / discussions – Central versus decentral?"

Die Folie ist offen formuliert und führt direkt zur expliziten Übungsfrage: „Welches Design hat ELGA?". Die Frage wird im PDF nicht beantwortet, sondern als Diskussionsanstoß gestellt.

Eng damit verbunden, aber nicht identisch, ist die Frage **Repository versus „on the fly accumulation"** ([[EHR - Architektur - Registry vs Repository]]).

Auch die Folie 86 („Computer Implementation EHRs – considerations") greift es auf: „Distribution versus centralization – How is that again in ELGA?"

## Bestandteile / Aufbau

Die Vorlesung selbst formuliert keine ausdifferenzierte Tabelle. Das PDF gibt nur die Designfrage als solche und den Hinweis auf ELGA als Diskussionsobjekt.

Implizite Vergleichsachsen, die sich aus der Vorlesung ableiten lassen:
- **Datenhoheit**: zentral = ein Betreiber / dezentral = bleibt bei den Versorgern
- **Verfügbarkeit**: zentral = Single Point of Failure / dezentral = Verfügbarkeit hängt vom Versorger ab
- **Performance**: zentral = direkter Zugriff / dezentral = je nach Aggregationszeit
- **Privacy**: zentral = große Angriffsfläche / dezentral = mehrere kleinere
- **Synchronisation**: zentral = einfacher / dezentral = Konsistenz schwieriger

## Beispiel

ELGA wird als Diskussionsbeispiel genannt – die konkrete Architektur-Antwort steht im PDF nicht (siehe spätere Vorlesungen, [[EHR - VL - ELGA Architektur]] – noch nicht angelegt).

## Abgrenzung

- Diese Frage ist **nicht identisch** mit [[EHR - Architektur - Registry vs Repository]]: Auch ein zentrales System kann als Registry (nur Verweise) statt Repository (alle Daten) realisiert werden.
- Auch nicht identisch mit „lokal vs. cloud" – die Frage ist organisatorisch, nicht infrastrukturell.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen einer zentralen und einer dezentralen EHR-Architektur?

**Anwendungsfrage:** Welche Architektur hat ELGA – und welche Argumente sprachen dafür?

**Diskussionsfrage:** Datenhoheit vs. Verfügbarkeit – welche Trade-offs entstehen? Welche Anforderungen aus [[EHR - Anforderungen - HIMSS High-Level Requirements]] werden durch zentral vs. dezentral unterschiedlich gut erfüllt?

**Mögliche Anschlussfragen:**
- Wie bildet die ELGA-Architektur den dezentralen Ansatz konkret ab?
- Was bedeutet Single Point of Failure im Kontext von Gesundheitsdaten?
- Wie verhält sich diese Architekturfrage zur Forderung „accessible by multiple authorized users" aus ISO/TR 20514?

## Verwandt

- [[EHR - Architektur - Registry vs Repository]]
- [[EHR - Definition - ISO TR 20514]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - VL - ELGA Architektur]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folie 39 („Some interesting design questions"), Folie 86 („Computer Implementation EHRs – considerations")
