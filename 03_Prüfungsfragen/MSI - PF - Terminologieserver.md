---
fach: msi
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - fach/allgemein/msi
  - typ/pruefungsfrage
  - status/offen
  - flashcards
---

# MSI - PF - Terminologieserver

## Kontext

Karten zu Terminologieservern: Definition, Aufgaben, Drei-Akteur-Architektur und Austauschstandards. Ergänzend zu [[MSI - PF - IHE-Profile]] (SVCM/SVS) und [[MSI - PF - HL7 FHIR Terminologie]] (FHIR Terminology Service im Detail).

## Verlinkte Konzepte

- [[MSI - Terminologieserver - Definition]]
- [[MSI - Terminologieserver - Aufgaben]]
- [[MSI - Terminologieserver - Architektur]]
- [[MSI - Terminologieserver - Austauschstandards]]
- [[MSI - ClaML - Classification Markup Language]]
- [[MSI - IHE SVS - Sharing Value Sets]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]

---

## Karten

### Definition

Was ist ein Terminologieserver, und welche Funktion hat er im eHealth-Umfeld?

?

Ein **Terminologieserver** stellt Terminologien in standardisierter Form für Benutzer zur Verfügung.

Kernfunktion: Unterstützung der **semantischen Interoperabilität** in verteilten Systemen durch Synchronisation von:
- lokal verwalteter Semantik (dezentral) ↔
- zentral vereinbarter und gepflegter Semantik

Zugriff: über **Webservices** (für Primärsysteme, automatisiert) und **Weboberfläche** (für Endbenutzer, manuell).

Voraussetzung: hohe Strukturierung der Terminologiedaten, automatische Verarbeitbarkeit.

Österreichisches Beispiel: `https://termgit.elga.gv.at/` (ELGA Termgit).

---

Welche vier Hauptaufgaben hat ein Terminologieserver? Welche Zusatzfeatures können vorhanden sein?

?

**Vier Hauptaufgaben** (Folie 7):
1. **Anzeige, Auflistung und Suche** von Terminologie-Inhalten (Echtzeitressource ja/nein)
2. **Export** von Terminologien in standardisierten Formaten und Services (Schnittstellen für lokale Systeme)
3. **Wartung**: Import und Update von Terminologien (standardisierte Formate/Services)
4. **Publikation**: Mechanismen zur Verteilung und Benachrichtigung, automatisierbarer Zugriff

**Zusatzfeatures:**
- **Intensionale Value-Set-Definition** – Regeln statt Aufzählung (z. B. „alle Konzepte unterhalb Konzept X")
- **Mapping** – ConceptMaps zwischen Codesystemen

---

### Anwendung

Skizzieren Sie die Drei-Akteur-Architektur eines Terminologieservers (Beispiel ELGA). Welche Import- und Export-Formate kommen vor?

?

```
TERMINOLOGIE-PROVIDER
  ┌── International: ICD-10, HL7, LOINC, UCUM, epSOS …
  └── National: ELGA-CS/VS, ICD-10-BMG, LKF, KAL, PZN, APPC …
         │
         │  Import: ClaML, XML, HTML, CSV
         ▼
TERMINOLOGIESERVER (termgit.elga.gv.at)
  ├── Administration & Pflege
  ├── Suche & Zugriff
  ├── Kollaboration
  └── Webportal + Webservices
         │──── OID-Portal (separates System, OID-Register)
         │
         │  Export: ClaML, XML, HTML, CSV
         ▼
TERMINOLOGIE-CONSUMER
  ├── Primärsysteme (KIS, LIS) → Webservices (automatisiert)
  └── Endbenutzer → Web Browser (manuell)
```

---

Welche Standards für den Austausch von Terminologien kennt die Vorlesung? Welcher ist veraltet?

?

| Standard | Format | Status |
|---|---|---|
| **FHIR Terminology** (Resources + Operationen) | FHIR REST/JSON/XML | aktuell |
| **ClaML** (CEN/TS 14463:2003 / EN 14463:2007) | XML | aktiv |
| **CTS2** (OMG Common Terminology Services 2) | OMG/Webservices | **veraltet** |
| **IHE SVCM** (Sharing Valuesets, Codes and Maps) | FHIR | aktuell |
| **IHE SVS** (Sharing Value Sets) | XML/SOAP | älter (ersetzt durch SVCM) |

Veraltet: **CTS2** — heute durch FHIR Terminology und IHE SVCM abgelöst.

---

### Diskussion / Vergleich

Welchen Standard würden Sie für einen neuen Terminologieserver wählen — FHIR Terminology, IHE SVCM oder ClaML? Begründen Sie.

?

**Empfehlung: FHIR Terminology + IHE SVCM** (kombiniert).

**FHIR Terminology:**
- Standardoperationen: `$expand`, `$lookup`, `$validate-code`, `$translate`
- Breite Unterstützung durch moderne Terminologieserver (Ontoserver, tx.fhir.org)
- Kompatibel mit REST-Infrastruktur

**IHE SVCM darüber:**
- Profiliert FHIR für interoperablen Terminologieaustausch zwischen Systemen (Akteure: Terminology Repository + Consumer)
- Legt Konformitätsanforderungen zusätzlich zum FHIR-Basisverhalten fest

**ClaML ergänzend:**
- Für den Import/Export von Klassifikationen wie ICD-10 (die als ClaML vorliegen) sinnvoll

**Nicht mehr sinnvoll:** CTS2 (veraltet), IHE SVS (SOAP/XML — ersetzt durch SVCM).

---

Warum ist das OID-Portal eine separate Komponente neben dem Terminologieserver?

?

**Unterschiedliche Zuständigkeiten:**
- **OID-Portal**: verwaltet *Identifikatoren* (OIDs für Code Systems, Templates, Value Sets, …). Ausschließlich Identifikations-Funktion.
- **Terminologieserver**: verwaltet *Inhalte* (die Codes, Bezeichnungen, Hierarchien, Value-Set-Einträge).

Ein Code System bekommt eine OID vom OID-Register — aber der inhaltliche Terminologiebeitrag liegt im Terminologieserver. Die OID ist nur der Schlüssel, mit dem das Code System referenziert wird.

**Praktisch (Österreich):** `gesundheit.gv.at/OID_Frontend` (OID-Register) + `termgit.elga.gv.at` (Terminologieserver) sind getrennte Systeme, die zusammen das Gesamtbild ergeben.

---

## Mögliche Anschlussfragen des Prüfers

- Welche FHIR-Operationen adressieren welche Terminologieserver-Aufgabe? ($expand → Suche/Auflistung; $validate-code → Validierung; $translate → Mapping)
- Was ist eine intensionale vs. extensionale Value-Set-Definition?
- Wie synchronisiert ein KIS seine lokalen Codes mit termgit.elga.gv.at?
- Welche Terminologien liefert der ELGA-Terminologieserver? (ELGA-eigene CS/VS, ICD-10-BMG, LOINC-Subsets, APPC …)
- Welchen Standard verwendet ELGA Termgit konkret? (im PDF nicht explizit, aber FHIR-basiert laut Folie)

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
