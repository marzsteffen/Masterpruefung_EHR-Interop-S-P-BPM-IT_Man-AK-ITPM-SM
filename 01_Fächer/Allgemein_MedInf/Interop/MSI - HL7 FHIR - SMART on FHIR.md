---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 FHIR Starter (Anna Lin)]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 FHIR - SMART on FHIR

> [!info] Kurzdefinition
> SMART on FHIR (Substitutable Medical Applications, Reusable Technologies) ist ein community-getriebener Sicherheitsstandard für FHIR-Anwendungen, der OAuth2 für Authentifizierung und Autorisierung verwendet. Sicherheit ist kein integraler Bestandteil der FHIR-API, aber essenziel empfohlen.

## Beschreibung

### Grundprinzip

- Sicherheit ist **nicht Teil der FHIR-API** (kein Pflichtbestandteil der REST-Spezifikation)
- Jedoch **empfohlen**: SMART on FHIR als community-Standard
- SMART on FHIR = **essentiell OAuth2**
- Dokumentation: `http://docs.smarthealthit.org/`
- Sicherheitscheckliste für Entwickler: `http://hl7.org/fhir/safety.html`

### SMART on FHIR Scopes

SMART Scopes definieren Zugriffsrechte via OAuth2:
- Verwendung von **SMART Scopes zur Definition von Zugriffsrechten** (OAuth2)
- Beispiel-Scope: `patient/*.read` → lesender Zugriff auf alle Ressourcen des Patienten
- Format: `[context]/[Ressourcentyp].[operation]`

### Security-Metadaten-Labels

- FHIR-Ressourcen können `meta.security`-Labels tragen
- Labels codieren Vertraulichkeitsklassen und Zugriffsbeschränkungen
- Referenz: `http://hl7.org/fhir/security-labels.html`

### Auditing in FHIR

FHIR stellt drei Ressourcen für Auditing und Datenschutz bereit:

| Ressource | Zweck | Verbindlichkeit |
|---|---|---|
| `AuditEvent` | Server-Log bei jedem Ressourcenzugriff | Verpflichtend (für FHIR-Server empfohlen) |
| `Provenance` | Warum wurde eine Ressource modifiziert? | Empfohlen |
| `Consent` | Einwilligung des Patienten für Datenzugriff, Operationen, … | Situationsabhängig |

## Abgrenzung

- **SMART on FHIR** vs. **FHIR-API**: FHIR selbst definiert keine Authentifizierung; SMART on FHIR ist ein separater, empfohlener Standard, der FHIR-Endpunkte mit OAuth2 absichert.
- **AuditEvent** vs. **Provenance**: AuditEvent = wer hat wann auf was zugegriffen (technisches Logging); Provenance = warum wurde eine Ressource angelegt/geändert (fachliche Nachvollziehbarkeit).
- **SMART on FHIR** vs. **IHE XUA / IUA**: SMART ist Community-Standard (OAuth2), IHE XUA/IUA sind IHE-Profile für die gleiche Problematik – oft kombiniert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist SMART on FHIR und welche Technologie liegt zugrunde?

**Anwendungsfrage:** Eine FHIR-App soll auf einem mobilen Gerät nur die Blutdruckmessungen des angemeldeten Patienten lesen dürfen. Wie würde man das mit SMART on FHIR realisieren?

**Diskussionsfrage:** Warum ist Sicherheit kein integraler Bestandteil der FHIR-Spezifikation? Was sind die Implikationen für Implementierungen?

**Mögliche Anschlussfragen:**
- Was ist OAuth2 und warum ist es für FHIR geeignet? (→ Bearer-Token, Scopes, Resource Server)
- Wie unterscheidet sich AuditEvent von Provenance?
- Welche Rolle spielt Consent in einem datenschutzkonformen FHIR-System?
- Wie verhält sich SMART on FHIR gegenüber IHE ATNA (Audit Trail and Node Authentication)?

## Verwandt

- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - REST API]]
- [[ASP - Authentifizierung - OAuth2]]
- [[MSI - IHE XDS - Architektur]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]], [[MSI - VL - Neues in HL7 FHIR (Anna Lin)]]
- Folien/Seitenangabe: Seiten 75–76 (Starter); Seite 6 (Neues in FHIR, Scopes)
