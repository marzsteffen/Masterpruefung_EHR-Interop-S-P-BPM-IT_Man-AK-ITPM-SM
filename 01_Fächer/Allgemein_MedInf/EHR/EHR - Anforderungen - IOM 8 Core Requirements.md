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

# EHR - Anforderungen - IOM 8 Core Requirements

> [!info] Kurzdefinition
> Acht Kernanforderungen an EHR-Systeme, definiert vom **Institute of Medicine (IOM) – 2003**. Sie bilden ein klassisches Bewertungsraster für EHR-Systeme und werden in der Vorlesung als Übungsgrundlage zur Bewertung von ELGA, KAGes-Portal etc. verwendet.

## Beschreibung

Quelle: Institute of Medicine, 2003 (Folien 54–57). Die acht Kernanforderungen sind:

## Bestandteile / Aufbau

| # | Anforderung | Inhalt laut PDF |
|---|---|---|
| 1 | **Health Information and Data** | Der elektronische Chart muss alles enthalten, was im Papier-Chart steht. Alle Informationen müssen entscheidungsrelevant sein. |
| 2 | **Result Management** | Verwaltung aller Test-Ergebnisse (Labor, Radiologie). |
| 3 | **Order Management** | Alle Verschreibungen elektronisch – reduziert Fehler durch unleserliche Handschrift; Orders auch automatisch generierbar. |
| 4 | **Decision Support** | Warnungen/Reminder zur Verbesserung der klinischen Performance. CDS bei: Wechselwirkungen, Verschreibung, Prävention, Outbreak Detection, evidenzbasierte Leitlinien. |
| 5 | **Electronic Communications and Connectivity** | Interoperables System, das mit mehreren Versorgern, dem Patienten, Laboren und Krankenhäusern sicher kommuniziert. |
| 6 | **Patient Support** | Patient kann auf Lehrmaterial zugreifen; selbst Daten eingeben (z. B. Home-Monitoring). |
| 7 | **Administrative Processes** | „Practice Management": Termine, Eligibility-Prüfung Versicherung, Effizienz; in US-Kontext: Medicaid, Medicare. |
| 8 | **Reporting to Authorities** | Standardisierte Reports an Behörden (state, federal, local). |

## Beispiel

Übung aus dem PDF (Folien 58–59): Für jede der 8 Anforderungen analysieren, wie sie durch HIS, ELGA, e-Card und andere Systeme erfüllt werden – und in einer Matrix Anforderungen × Rollen (Provider, Kollegen, Patient) eintragen, ob die Funktionalität verfügbar ist (oder partiell, oder N/A).

## Abgrenzung

- IOM-Anforderungen ergänzen die HIMSS-Liste ([[EHR - Anforderungen - HIMSS High-Level Requirements]]); IOM betont stärker den **klinischen Versorgungsablauf** (Order/Result Management, Reporting), HIMSS stärker **System-Eigenschaften** (Verfügbarkeit, Datenschutz).
- IOM ist **älter** (2003) als die HIMSS-Folien-Quelle, aber im PDF gemeinsam als Anforderungs-Compilation referenziert.
- US-Kontext: „Reporting to Authorities" ist im US-System (HIPAA/Meaningful Use) anders ausgeprägt als in Österreich/EU.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Nenne die 8 IOM Core Requirements für EHR-Systeme.

**Anwendungsfrage:** Wie ist Result Management in ELGA umgesetzt? Und wie unterscheidet sich Order Management in ELGA von US-EHRs?

**Diskussionsfrage:** Decision Support ist die Anforderung, die in der Praxis am häufigsten unterspezifiziert ist. Warum? Was unterscheidet einen einfachen Reminder von echter CDS?

**Mögliche Anschlussfragen:**
- Welche Verbindung besteht zwischen IOM-Anforderung 5 (Connectivity) und HL7 FHIR?
- Welche IOM-Anforderungen werden in „Meaningful Use" wieder aufgegriffen?
- Welche der 8 Anforderungen sind in Österreich primär bei ELGA, welche bei der e-Card adressiert?
- Warum ist „Administrative Processes" historisch für die Akzeptanz von EHR-Systemen so wichtig gewesen?

## Verwandt

- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - Anforderungen - Funktional vs Technisch]]
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - VL - Meaningful Use]]
- [[EHR - Standards - Unterstützte Coding Standards]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 54–57 (8 IOM Core Requirements), Folien 58–59 (Übungsaufgaben dazu)
