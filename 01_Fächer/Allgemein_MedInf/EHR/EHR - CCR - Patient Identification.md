---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - CCR und CCD]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - CCR - Patient Identification

> [!info] Kurzdefinition
> CCR macht **keine Vorgabe** zur Patient-Identifikation. In den USA ist die Verwendung der Social Security Number für Healthcare-Identifikation **untersagt** (AHIMA), und Identifikation per Name + Geburtsdatum ist fehleranfällig. Die Identifikations-Frage bleibt damit ein ungelöstes Problem.

## Beschreibung

Aus Folie 21:

> „In the USA it is not allowed to use the Social Security Number for healthcare identification."

Aus Folie 22:

> „Identification based on name and birth date is very difficult …
> CCR does not impose any identification scheme."

Quelle laut Folie: AHIMA (American Health Information Management Association), Library Document #104465.

## Bestandteile / Aufbau

### Problem

- **SSN-Verbot** für Healthcare-Identifikation in den USA
- **Name + Geburtsdatum** ist nicht eindeutig (Namensänderungen, Tippfehler, identische Geburtsdaten bei häufigen Namen)
- **Master Patient Index (MPI)** ist organisationsspezifisch und nicht national einheitlich

### CCR-Antwort

> „CCR does not impose any identification scheme."

CCR überlässt die Identifikation der jeweiligen Implementierung. In der Praxis verwenden EHR-Systeme:
- Eigene interne Patient-IDs
- Probabilistische Matching-Verfahren über mehrere Attribute (Name, Birth Date, Adresse, Telefon)
- Externe Identifier (Driver's License Number, Insurance Member ID)

## Beispiel

Konkretes Identifikations-Problem: Ein Patient wird im Krankenhaus A unter ID „A-12345" geführt, im Krankenhaus B unter ID „B-67890". Wenn beide ein CCR austauschen, müssen sie die Identität rekonstruieren – ohne nationale ID-Nummer und ohne SSN-Nutzung. Das führt zu Fehlern (Mismatching, Duplicate Records).

## Abgrenzung

- USA ↔ Österreich: In Österreich gibt es die **Sozialversicherungsnummer (SVNR)** und damit eine eindeutige Identifikation – das macht ELGA technisch deutlich einfacher als US-Systeme.
- CCR ↔ FHIR: FHIR's `Patient.identifier` erlaubt mehrere Identifier mit Type/System-Kennzeichnung; das ist eine technische Lösung, ändert aber nicht das organisatorische Problem fehlender nationaler IDs.
- CCR ist **bewusst agnostisch** – keine Vorschrift, sondern Verlagerung des Problems an die Implementierung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie löst CCR die Patient-Identifikation? Welche Probleme bestehen in den USA?

**Anwendungsfrage:** Wie würde Patient-Identifikation in einem CCR-Austausch zwischen zwei US-Krankenhäusern praktisch ablaufen?

**Diskussionsfrage:** Vor- und Nachteile einer nationalen Patient-ID (wie SVNR in Österreich) vs. dezentralem Matching (USA). Privacy- vs. Match-Quality-Tradeoff.

**Mögliche Anschlussfragen:**
- Warum ist die SSN-Nutzung verboten? (Antwort: SSN wurde nie als Healthcare-Identifier konzipiert; SSN-Diebstahl ermöglicht Identitätsklau, daher restriktive Nutzung)
- Was ist ein Master Patient Index?
- Welche probabilistischen Matching-Algorithmen kommen zum Einsatz?
- Wie löst FHIR das Identifier-Problem strukturell?

## Verwandt

- [[EHR - CCR - Continuity of Care Record]]
- [[EHR - CCD - Continuity of Care Document]]
- [[ASP - Patient Identification]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folien 21–22 (Patient Identification in CCR + AHIMA-Verweis)
