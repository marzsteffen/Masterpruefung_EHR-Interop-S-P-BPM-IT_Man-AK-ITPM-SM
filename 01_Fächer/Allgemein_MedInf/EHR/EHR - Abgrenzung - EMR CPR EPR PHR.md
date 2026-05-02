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

# EHR - Abgrenzung - EMR CPR EPR PHR

> [!info] Kurzdefinition
> Sammlung verwandter, aber inhaltlich verschiedener Record-Begriffe rund um EHR. Sie unterscheiden sich in Reichweite (eine Organisation vs. übergreifend), Lebensdauer (Encounter, Episode, lebenslang) und Kontrolle (Versorger vs. Patient).

## Beschreibung

Die Vorlesung listet die Begriffe als „Subsets / Alternatives" zur EHR (Folie 28). Die zentralen Unterscheidungsachsen sind Reichweite, Lebensdauer und Kontrollinstanz.

## Bestandteile / Aufbau

| Begriff | Definition (laut Vorlesung) | Reichweite | Kontrolle |
|---|---|---|---|
| **EMR** (Electronic Medical Record) | EHR innerhalb einer einzelnen Versorgungs­organisation | eine Organisation | Versorger |
| **CPR** (Computer-based Patient Record) | Lifetime-Record eines Patienten, interoperabel (potenziell international) – Quelle: Richard, 1997 | übergreifend, lebenslang | Versorger |
| **EPR** (Electronic Patient Record) | Wie CPR, **nicht zwingend lebenslang**, nur relevante Informationen | übergreifend, episodisch oder vollständig | Versorger |
| **PHR** (Personal Health Record) | „patient-side view" eines EHR/EMR – vom Patienten gemanagt und kontrolliert | je nach System | **Patient** |

## Beispiel

Aus der Vorlesung ableitbare Zuordnungen:
- HIS einer einzelnen Klinik → typischerweise **EMR**-Charakter
- ELGA (Österreich) → kombiniert EHR-Charakter (organisationsübergreifend) mit Aspekten einer EPR/CPR
- Apps wie patientslikeme oder OpenNotes → eher **PHR**-Sicht

## Abgrenzung

- **EHR vs. EMR:** EMR ist auf eine Organisation beschränkt; EHR ist organisationsübergreifend.
- **CPR vs. EPR:** CPR ist explizit lebenslang, EPR muss das nicht sein.
- **PHR vs. EHR:** PHR liegt in der Hand des Patienten, EHR in der Hand der Versorger.
- Im englischsprachigen US-Diskurs werden EHR und EMR oft synonym verwendet – diese Unschärfe ist in der mündlichen Prüfung vermeidbar.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen EHR, EMR und PHR?

**Anwendungsfrage:** Wie würdest du ELGA in dieses Schema einordnen? Welche Aspekte stützen welche Einordnung?

**Diskussionsfrage:** PHR und EHR – kollaborative oder konkurrierende Modelle? Welche Konsequenzen hat es für die Datenintegrität, wenn der Patient eigene PHR-Daten in eine EHR überführen darf?

**Mögliche Anschlussfragen:**
- Wer „besitzt" die Daten in einem PHR vs. EHR?
- Welche Standards adressieren speziell den PHR-Use-Case (Stichwort: SMART on FHIR)?
- Warum hat sich der Begriff CPR im Diskurs nicht durchgesetzt?
- Welche US-Begriffsverwirrung sollte man bei internationalen Projekten beachten?

## Verwandt

- [[EHR - Definition - ISO TR 20514]]
- [[EHR - Definition - HIMSS]]
- [[EHR - Klassifikation - Waegemann 5 Level]]
- [[EHR - Portal - Patientenportal]]
- [[ASP - Datenhoheit und Eigentum]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folie 28 („Related Definitions (subsets, alternatives)")
