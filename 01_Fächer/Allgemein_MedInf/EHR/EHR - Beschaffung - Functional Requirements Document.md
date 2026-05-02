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

# EHR - Beschaffung - Functional Requirements Document

> [!info] Kurzdefinition
> Strukturiertes Anforderungsdokument, mit dem Krankenhäuser/Behörden bei einer EHR-Ausschreibung von Vendoren standardisierte Antworten zu konkreten funktionalen Fähigkeiten einholen. Kombiniert eine Anforderungsmatrix mit Min/Opt-Markierung und einer **Vendor Capability Matrix**.

## Beschreibung

Das BPHC-Dokument ist ein typisches Beispiel für ein Functional Requirements Document, das im EHR-Beschaffungsprozess eingesetzt wird. Die Struktur ist methodisch wichtig:

> „Functions considered of primary importance have a dot (•) in the 'Min' column, indicating that the function described by the statement represents a minimum requirement. Features considered desirable but not mandatory have a dot (•), in the 'Opt' (Optional) column. The vendor should review each of these requirements against their proposed system."

> „Where the function is provided, the vendor should indicate that capability by placing an 'X' in the 'Yes' column, followed by the name of the proposed software module or menu function that provides the stated capability under the Module Name column."

## Bestandteile / Aufbau

| Spalte | Bedeutung |
|---|---|
| **Requirement** | Eine konkret formulierte Anforderung (z. B. „The system supports HL7 transactions") |
| **Min** | Pflichtanforderung – Vendor ohne Erfüllung fällt aus der Auswahl |
| **Opt** | Optional – wünschenswert, aber nicht ausschließend |
| **Yes** | Vendor markiert „X", wenn aktuell erfüllt |
| **Module Name** | Name des konkreten Software-Moduls, das die Anforderung erfüllt (z. B. „PowerChart Clinical Office with PowerNote") |
| **Future Version (Date)** | Geplante Version + Datum, falls aktuell noch nicht erfüllt |
| **3rd Party Provided (Name)** | Drittsystem, das via Interface die Anforderung erfüllt – Vendor übernimmt dann die Verantwortung für das Interface |

Vor der eigentlichen Matrix steht typischerweise ein **Vendor Profile** mit:
- Firmenname, Adresse, Kontaktinformationen
- Jahresumsatz, Years in Business
- Anzahl Klienten, größte installierte Systeme
- Produktnamen, Lizenzbedingungen, Wartungs- und Trainingsmodelle
- Upgrade-Frequenz, User Groups, RUGs (Regional User Groups), SIGs (Special Interest Groups)

## Beispiel

Eine konkrete Zeile aus dem Cerner-Dokument:

```
Requirement: The system supports the HIPAA Standards for Electronic Transactions
Min: •
Yes: X
Module: PowerChart Clinical Office with PowerNote
```

Eine andere:

```
Requirement: ICD-10
Min: •
Yes: (leer)
Future Version: To be Determined (ICD-10 will be available when it becomes industry standard)
```

→ Cerner erfüllt die Min-Anforderung nicht, hat aber Future-Version-Plan – das schafft Verhandlungsbasis, würde in einem strikten RFP aber Punktabzug bedeuten.

## Abgrenzung

- Functional Requirements Document ≠ Technical Requirements Document: ersteres beschreibt **was** das System können muss, letzteres **wie** (siehe [[EHR - Anforderungen - Funktional vs Technisch]]).
- Functional Requirements Document ≠ ISO 18308: Letzteres ist eine **normative** Anforderungsspezifikation auf internationaler Ebene; ein RFP-Dokument ist **organisationsspezifisch** und betriebswirtschaftlich motiviert.
- Functional Requirements Document ≠ Use Case Document: Use Cases beschreiben Szenarien, Functional Requirements beschreiben Fähigkeiten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein Functional Requirements Document, und welche Spalten hat eine typische Anforderungs­matrix?

**Anwendungsfrage:** Wie würdest du die Min/Opt-Markierung nutzen, um zwei konkurrierende Vendoren-Angebote zu vergleichen?

**Diskussionsfrage:** Was passiert, wenn ein Vendor eine Min-Anforderung nur über „3rd Party Provided" erfüllt? Welche Risiken trägt der Auftraggeber?

**Mögliche Anschlussfragen:**
- Wo liegt der Nachteil eines zu detaillierten Functional Requirements Document?
- Wie verhalten sich Functional Requirements Documents zu agilen Beschaffungs­ansätzen?
- Welche Rolle spielen User Groups (RUGs, SIGs) bei der Auswahl eines Vendors?
- Wie würde ein modernes RFP-Dokument 2025 anders aussehen als 2003 (Stichwort: API-First, FHIR, Cloud)?

## Verwandt

- [[EHR - Anforderungen - Funktional vs Technisch]]
- [[EHR - EMR - 24 Funktionsbereiche]]
- [[EHR - Anforderungen - HIMSS High-Level Requirements]]
- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[EHR - Beispiel - Cerner PowerChart Office]]

## Quelle

- Vorlesung: [[EHR - Spec - BPHC EMR Functional Specs Cerner]]
- Folien/Seitenangabe: Seiten 1–2 (Erläuterung der Matrix-Struktur), Seiten 3–7 (Vendor Profile), Seiten 9–37 (Anforderungs-Matrix)
