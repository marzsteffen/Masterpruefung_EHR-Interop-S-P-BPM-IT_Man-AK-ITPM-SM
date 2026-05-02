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

# EHR - System vs Exchange Format

> [!info] Kurzdefinition
> Konzeptionelle Trennung zwischen einem **EHR-System** (das Daten erfasst und speichert) und einem **EHR-Exchange-Format** (das Daten zwischen Stellen transportiert). Selbst eine homogene Systemwelt benötigt ein Exchange-Format – sobald Daten zwischen Stellen oder zum Patienten fließen.

## Beschreibung

Aus Folie 5:

> „We need to clearly distinguish between EHRs as a system, and standardized exchange of EHRs.
> KAGES uses different internal systems. Can they exchange EHRs?
> Slovenia uses OpenEHR in all hospitals. All patients have full access to their EHRs. Is there an exchange standard?
> HL7-FHIR is an exchange system for EHRs but doesn't impose how the data is captured or stored."

## Bestandteile / Aufbau

| Aspekt | EHR als System | Exchange-Format |
|---|---|---|
| Funktion | Erfassen, Speichern, Abrufen | Transport zwischen Stellen |
| Beispiele | Cerner Millennium, Epic, OpenEHR, Allscripts, ELGA-Repositories | HL7 v2, CDA, CCR/CCD, FHIR, IHE-Profile |
| Verantwortlich | Versorger / Betreiber | Standardisierungs-Organisationen (HL7, ASTM, IHE) |
| Datenmodell | proprietär oder offen, oft DB-spezifisch | offen, dokumentiert, standardisiert |

## Beispiel

Drei Szenarien aus der Vorlesung:

1. **KAGES** (Steirische Krankenanstaltengesellschaft) nutzt intern unterschiedliche Systeme – um Daten zwischen den eigenen Häusern auszutauschen, braucht sie ein Exchange-Format.
2. **Slowenien** nutzt landesweit OpenEHR. Selbst dann braucht es ein Exchange-Format, sobald Daten dezentral aggregiert oder zum Patienten gegeben werden müssen.
3. **HL7-FHIR** ist ein Exchange-System – es macht **keine Vorgabe**, wie die Daten intern erfasst oder gespeichert werden.

## Abgrenzung

- **System ≠ Format:** Ein System produziert und konsumiert Daten in einem Format. Beide sind notwendig, aber verschieden.
- **OpenEHR-Spezialfall:** OpenEHR hat sowohl ein Datenmodell (Reference Model + Archetypes) als auch ein Format – es kann beides sein. FHIR ist primär Format, weniger System.
- **Exchange-Format ≠ Coding-Standard:** Format spezifiziert Struktur (siehe [[EHR - Interoperabilität - Strukturell vs Semantisch]]), Coding-Standards spezifizieren Semantik.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Unterschied zwischen einem EHR-System und einem EHR-Exchange-Format?

**Anwendungsfrage:** Slowenien nutzt OpenEHR landesweit. Warum braucht es trotzdem einen Exchange-Standard?

**Diskussionsfrage:** Manche Hersteller propagieren „integrated suite"-Lösungen, die Exchange-Formate überflüssig machen sollen. Warum ist das illusorisch – auch in homogenen Systemlandschaften?

**Mögliche Anschlussfragen:**
- Wie verhält sich diese Trennung zu LCIM (Schichten-Modell)?
- Welche Exchange-Formate kennen wir? (HL7 v2, CDA, CCR, CCD, C-CDA, FHIR, IHE)
- Warum macht FHIR keine Vorgabe zur internen Datenhaltung?
- Wie liegen System und Exchange in einem ELGA-Setup?

## Verwandt

- [[EHR - Interoperabilität - Strukturell vs Semantisch]]
- [[EHR - Architektur - Registry vs Repository]]
- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - HL7 FHIR - 5 Levels]]

## Quelle

- Vorlesung: [[EHR - VL - CCR und CCD]]
- Folien/Seitenangabe: Folien 4–5 (do we need an exchange format; systems versus exchange)
