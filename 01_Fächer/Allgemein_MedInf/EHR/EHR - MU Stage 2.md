---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Meaningful Use]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - MU Stage 2

> [!info] Kurzdefinition
> **Meaningful Use Stage 2** (2014–2016): zweite Stufe des Programms mit deutlich stärkerem Fokus auf **Datenaustausch und Interoperabilität** zwischen Versorgern. Erweiterte Core-Anforderungen (z. B. Vital Signs, Lab Results) und neue Menu-Objectives (z. B. strukturierte Progress Notes).

## Beschreibung

Aus den Folien zu Stage 2:

> „More emphasis on the use of EHRs and exchange."

Während Stage 1 die grundlegende **Use** etablierte, verlangt Stage 2 den nachweisbaren **Exchange** elektronischer Gesundheits­informationen zwischen verschiedenen Stellen.

## Bestandteile / Aufbau

### Beispielhafte Core-Anforderungen
- **Vital Signs:** Strukturierte Erfassung in einem zertifizierten EHR
- **Laboratory Results:** Eingang in strukturierter Form ins EHR

### Beispielhaftes Menu-Objective
- **Progress Notes:** Strukturierte elektronische Erstellung

### Stage-2-Logik
- Menu-Objectives bedeuten: Provider kann auswählen, welche von mehreren möglichen Anforderungen erfüllt werden – nicht alle sind verpflichtend.
- Mehr Exchange-Fokus bedeutet: Datenaustausch mit anderen Versorgern (z. B. bei Care Transitions) wird messbar.

### Stage-2-Tracks
- Eligible Professionals: erweiterte Core- und Menu-Sets
- Hospitals: eigene Anforderungs-Sets, abhängig von Medicare-/Medicaid-Spur

## Beispiel

Ein typisches Stage-2-Szenario:
- Krankenhaus muss bei Patienten-Transfer (z. B. Entlassung) elektronisch eine Care-Summary an den nachfolgenden Versorger senden
- Ambulanter Provider muss strukturierte Lab-Ergebnisse in seinem EHR aufnehmen können (nicht nur PDF-Befund anhängen)
- Vital Signs müssen strukturiert (Höhe, Gewicht, BP) eingegeben werden – nicht als Free-Text

## Abgrenzung

- Stage 2 baut auf Stage 1 auf – Provider müssen Stage 1 absolviert haben.
- Stage 2 ist **anspruchsvoller** als Stage 1 (mehr Exchange, höhere Schwellen).
- Stage 2 ist nicht mit Stage 3 gleich­zusetzen: Stage 3 vereinfacht die Struktur (keine Menu-Optionen mehr) und legt Fokus auf Outcomes.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Hauptfokus von Meaningful Use Stage 2 im Vergleich zu Stage 1?

**Anwendungsfrage:** Welche Stage-2-Anforderungen erforderten die größten technischen Investitionen bei Krankenhäusern?

**Diskussionsfrage:** Stage 2 verlangte deutlich mehr Exchange. Warum war das technisch herausfordernd – welche Standards (HL7 v2, CDA, Direct Project) standen zur Verfügung, welche fehlten?

**Mögliche Anschlussfragen:**
- Was bedeutet „strukturierte" Erfassung von Vital Signs konkret?
- Welche Rolle spielten CCDA-Dokumente in Stage 2? (Ergänzung außerhalb der Vorlesung – siehe [[EHR - VL - CCR und CCD]])
- Wie verhielt sich Stage 2 zum Direct Project (sicherer E-Mail-basierter Austausch)?
- Warum wurde das Menu-Optionen-Konzept in Stage 3 abgeschafft?

## Verwandt

- [[EHR - VL - Meaningful Use]]
- [[EHR - MU Stage 1]]
- [[EHR - MU Stage 3]]
- [[EHR - Meaningful Use - 3 Hauptkomponenten]]

## Quelle

- Vorlesung: [[EHR - VL - Meaningful Use]]
- Folien/Seitenangabe: Folien 22–31 (MU Stage 2 Übersicht, Beispiele Core/Menu, Hospitals/Medicaid)
