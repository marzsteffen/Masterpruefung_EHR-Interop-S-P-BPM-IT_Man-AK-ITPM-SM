---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR und Terminologieserver]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologieserver - Architektur

> [!info] Kurzdefinition
> Drei-Akteur-Architektur: **Terminologie-Provider** (Quellen) → **Terminologieserver** (zentrale Plattform mit Administration & Pflege, Suche & Zugriff, Kollaboration, Web-Portal/Webservices) → **Terminologie-Consumer** (Webservice-Nutzer für Primärsysteme + Webfrontend-Nutzer für manuelle Recherche). Ergänzt durch ein **OID-Portal** mit OID-Register.

## Beschreibung

Folie 8 zeigt den Aufbau am Beispiel ELGA:

**Terminologie-Provider** (Quellen, in zwei Bündeln):
- *Standards*:
  - International: ICD-10, HL7, LOINC, UCUM, epSOS, TISS-28, SAPS 3 etc.
  - National: HL7 Österreich, PZN, APPC/BURA etc.
- *Kollaborative Erstellung und Wartung von Terminologien*:
  - BMG: ICD-10-BMG 2013, LKF, KAL, TISS-A etc.
  - ELGA: Codesysteme, Value Sets etc.

→ **Import** über CLAML, XML, HTML, CSV.

**Terminologieserver** (zentrale Plattform):
- *Administration & Pflege*
- *Suche & Zugriff*
- *Kollaboration*
- *Webportal, Webservices*
- Datenbank: Terminologien, Vokabulare, Value Sets.

→ Verbunden mit dem **Österreichischen OID-Portal** (separater Block mit OID-Register).

**Terminologie-Consumer**:
- *Webservice-Nutzer (Primärsysteme)* – über Webservices, automatisierte Synchronisation.
- *Webfrontend-Nutzer* – über Web Browser, manuelle Suche/Recherche, Download.

→ **Export** in CLAML, XML, HTML, CSV.

## Bestandteile / Aufbau

| Schicht | Akteur(e) | Funktion | Format/Schnittstelle |
|---|---|---|---|
| Provider | International, National, BMG, ELGA | Quelle der Terminologien | CLAML, XML, HTML, CSV |
| Server | Terminologieserver | Administration, Pflege, Suche, Kollaboration | Webportal + Webservices |
| Register | OID-Portal | OID-Verwaltung | – |
| Consumer | Primärsystem | Automatisierte Synchronisation | Webservices |
| Consumer | Endbenutzer | Manuelle Suche/Download | Web Browser |

## Beispiel

Konkret für Österreich:
- Provider: ELGA-Codesysteme + ICD-10-BMG + LKF/KAL/TISS-A.
- Server: termgit.elga.gv.at.
- OID-Portal: gesundheit.gv.at/OID_Frontend.
- Consumer: Krankenhausinformations­systeme synchronisieren via Webservices, Implementierer recherchieren manuell über Webfrontend.

## Abgrenzung

- **Provider ≠ Consumer**: Provider liefert die Terminologien; Consumer nutzt sie.
- **Server ≠ OID-Portal**: getrennte Systeme. Das OID-Portal verwaltet Identifikatoren, der Server die inhaltliche Terminologie.
- **Webservices vs. Webfrontend**: Maschine vs. Mensch.

## Prüfungsrelevanz

**Hoch.**

**Typische Definitionsfrage:** Skizzieren Sie die Architektur eines Terminologieservers mit Provider, Server, Consumer.

**Anwendungsfrage:** Welche Provider beliefern den ELGA-Termgit?

**Diskussionsfrage:** Warum ist das OID-Portal als separate Komponente neben dem Terminologieserver?

**Mögliche Anschlussfragen:**
- Welche Aufgaben hat der Server selbst? → [[MSI - Terminologieserver - Aufgaben]]
- Welche Standards für Import/Export? → [[MSI - Terminologieserver - Austauschstandards]]
- Welche Rolle spielt der Consumer? Welche Schnittstellen?

## Verwandt

- [[MSI - Terminologieserver - Definition]]
- [[MSI - Terminologieserver - Aufgaben]]
- [[MSI - Terminologieserver - Austauschstandards]]
- [[MSI - Identifikator - OID]]
- [[MSI - Terminologie - Management in Österreich]]
- [[EHR - ELGA - Architektur]] (cross-fach)

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR und Terminologieserver]]
- Folien/Seitenangabe: 8
