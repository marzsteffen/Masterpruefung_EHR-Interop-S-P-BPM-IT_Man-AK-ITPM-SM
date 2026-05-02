---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - Spec - BPHC EMR Functional Specs Cerner]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Beispiel - Cerner PowerChart Office

> [!info] Kurzdefinition
> **PowerChart Clinical Office** war 2003 das EMR-Modul von Cerner Corporation für ambulante (Physician Practice) Versorgung, integriert in die **Cerner Millennium**-Plattform. Erstmals 1997 freigegeben. Dient im BPHC-Dokument als konkretes Vendor-System, dessen Module die einzelnen RFP-Anforderungen zugeordnet werden.

## Beschreibung

Cerner Corporation (Kansas City, MO) hat 2003 mit PowerChart Clinical Office den Großteil der BPHC-Anforderungen abgedeckt – ergänzt durch eine Reihe weiterer Module der Millennium-Plattform, die im Laufe des Dokuments referenziert werden.

## Bestandteile / Aufbau

Im PDF erwähnte Cerner-Module:

| Modul | Funktion |
|---|---|
| **PowerChart Clinical Office** | Kern-EMR, Anchor für die meisten klinischen Funktionen |
| **PowerNote** | Strukturierte klinische Dokumentation (Care Design Templates), durchsuchbar |
| **PowerForms** | Patient/Treatment-Forms, beliebig viele konfigurierbar, kann automatisierte Health-Status-Messungen rechnen |
| **PowerChart Support Office** | Practice Management (Demographics, Adressen, Inactivation statt Löschen) |
| **MediSource Foundation** | Drug-Interaction-Database (Drug-Allergy, Drug-Drug, Drug-Food, Duplicate Therapy) |
| **Discern Expert** | Custom-Rules-Engine für CDS – Trigger, Reports, Alerts |
| **Discern Explorer** | Reporting/Analytik |
| **PowerInsight** | Clinical Outcomes / Data Warehouse / Plotter Support |
| **Clinical Outcomes** | Risk-Faktor-Erfassung, Reports und Variablen aus Diagnose-/Procedure-Codes |
| **InfoX** | ABN-Checking (Advanced Beneficiary Notification, Medicare-Spezifik) |
| **Cerner Medical Terminology (CMT)** | Subscription für automatisches Terminologie-Update (DRG, ICD-9-CM, CPT-4, SNOMED CT, NIC/NOC, NANDA, LOINC, APC, HCPCS) |
| **Cerner Knowledge Network (CKN)** | Repository für Software-Updates und Listserves |
| **Cerner Desktop Manager** | Auto-Update-Mechanismus auf den Endgeräten |

## Beispiel

Die Anforderung „The system controls access to and within the system at multiple levels (e.g. per user, per user role, per area, per section of the chart) through a consistent mechanism of identification and authentication of all users in accordance with the 'Role Based Access Control' (RBAC) standard" wird in der Vendor-Antwort dem Modul „**Core to Cerner's Millennium Architecture**" zugeordnet – also nicht einem einzelnen Produkt, sondern der Plattform.

Die Anforderung „ICD-10" wird mit „To be Determined" (Future Version) beantwortet – ICD-10 war 2003 in den USA noch nicht industry standard.

## Abgrenzung

- PowerChart Clinical Office ist ein **ambulantes** (Physician Practice) EMR, nicht zu verwechseln mit Cerners Krankenhaus-Lösung (in dieser Generation: PowerChart, ohne „Office").
- Cerner Millennium ist die Plattform; PowerChart Office ist ein Anwendungs­bündel auf dieser Plattform.
- Die Modul-Architektur ist 2003 typisch monolithisch / Suite-orientiert – im Gegensatz zu modernen API-First-/FHIR-basierten Plattformen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was war PowerChart Clinical Office, und wofür stand es im Cerner-Portfolio?

**Anwendungsfrage:** Wie würde Cerner heute (2025) auf eine ICD-10- oder FHIR-Anforderung antworten? Welche Module wären relevant?

**Diskussionsfrage:** Eine monolithische Suite wie Cerner Millennium 2003 vs. moderne API-First-Architekturen (Epic mit App Orchard, FHIR-zentrierte Open Architectures): Welche Trade-offs?

**Mögliche Anschlussfragen:**
- Was passierte mit Cerner als Unternehmen seit 2003?
- Welche Rolle spielt heute Discern Expert in CDS-Lösungen?
- Was ist der Unterschied zwischen PowerNote und PowerForms?

## Ergänzung außerhalb der Vorlesung

Cerner Corporation wurde 2022 von Oracle übernommen und firmiert seit 2024 als **Oracle Health**. Die „Millennium"-Plattform existiert weiterhin, wird zunehmend mit Oracle Cloud Infrastructure und FHIR-APIs modernisiert. Das größte konkurrierende EMR-System im US-Markt ist Epic Systems mit dem Produkt **EpicCare**.

## Verwandt

- [[EHR - Spec - BPHC EMR Functional Specs Cerner]]
- [[EHR - Beschaffung - Functional Requirements Document]]
- [[EHR - EMR - 24 Funktionsbereiche]]

## Quelle

- Vorlesung: [[EHR - Spec - BPHC EMR Functional Specs Cerner]]
- Folien/Seitenangabe: Seiten 3–7 (Vendor Profile Cerner), Seiten 9–37 (Modul-Zuordnungen in der Antwort-Matrix)
