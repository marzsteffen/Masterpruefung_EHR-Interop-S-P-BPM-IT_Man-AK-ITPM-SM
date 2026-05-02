---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - CDS Hooks

> [!info] Kurzdefinition
> CDS Hooks (Clinical Decision Support Hooks) ist ein offener Standard, mit dem FHIR-Server auf definierte klinische Ereignisse (Trigger) reagieren und externe Entscheidungslogik (CDS-Logik) aufrufen können. Das Ergebnis kann u. a. als Pop-Up-Meldung im klinischen System erscheinen.

## Beschreibung

Aus Seite 7:

- **Specification:** `https://cds-hooks.org/`
- Reagieren auf bestimmte **Trigger** (z. B. wenn ein Patienten-Eintrag angesehen wird)
- Wenden **CDS-Logik** an
- Können ggf. zu **Pop-Up-Meldungen** führen

Weitere Details (Hook-Typen, Request/Response-Format, Prefetch) wurden im PDF nicht ausgeführt.

## Bestandteile / Aufbau

Im PDF nicht ausgeführt. Erwähnte Konzepte:

| Begriff | Bedeutung laut PDF |
|---|---|
| Hook (Trigger) | Auslösendes Ereignis (z. B. Patientenansicht öffnen) |
| CDS-Logik | Die Entscheidungslogik, die beim Trigger angewendet wird |
| Pop-Up Meldung | Mögliches Ergebnis / Rückmeldung an den klinischen Anwender |

## Beispiel

Trigger: Arzt öffnet Patienteneintrag → CDS Hook wird ausgelöst → externe CDS-Logik prüft z. B. Medikamenteninteraktionen → Pop-Up mit Warnmeldung erscheint im KIS.

## Abgrenzung

- **CDS Hooks ≠ FHIR-Operation**: CDS Hooks sind ein eigener Standard auf Basis von HTTP/JSON, der auf FHIR aufbaut, aber nicht Teil der FHIR-Spezifikation selbst ist.
- **CDS Hooks ≠ CQL**: CQL ist die Sprache für die Entscheidungslogik; CDS Hooks ist der Mechanismus, der diese Logik aufruft (Trigger + Kommunikationsprotokoll).
- **CDS Hooks ≠ SMART on FHIR**: SMART on FHIR regelt die Authentifizierung/Autorisierung; CDS Hooks regelt die event-getriebene Interaktion mit Entscheidungslogik.

## Prüfungsrelevanz

**Mittel.**

**Typische Definitionsfrage:** Was sind CDS Hooks und wie funktionieren sie?

**Anwendungsfrage:** Wie würde man eine Medikamenteninteraktionsprüfung mit CDS Hooks realisieren?

**Diskussionsfrage:** Welche Vorteile hat ein standardisiertes Hooks-Protokoll gegenüber proprietärer CDS-Integration?

**Mögliche Anschlussfragen:**
- Wie hängen CDS Hooks und CQL zusammen? (→ CQL als Sprache für die Logik hinter dem Hook)
- Welche Trigger-Events sind typisch? (→ patient-view, order-sign, order-select – im PDF nicht erwähnt)

## Verwandt

- [[MSI - HL7 FHIR - CQL]]
- [[MSI - HL7 FHIR - SMART on FHIR]]
- [[MSI - HL7 FHIR - REST API]]

## Quelle

- Vorlesung: [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]
- Folien/Seitenangabe: Seite 7
