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

# MSI - HL7 FHIR - Versionen

> [!info] Kurzdefinition
> HL7 FHIR durchläuft einen ~18-monatigen Versionszyklus. Seit R4 gibt es normative Ressourcen (abwärtskompatibel, stabil). Aktuell ist R5; empfohlen wird stets die neueste Version. Ressourcen haben individuelle Reifegrade (Maturity Level / FMM).

## Beschreibung

### Versionshistorie

| Kurzname | Versionsnummer |
|---|---|
| DSTU1 | 0.0 |
| DSTU2 | 1.0 |
| STU3 | 3.0 |
| R4 | 4.0.1 |
| R5 | 5.0 |

- **Aktuell**: R5 → `http://hl7.org/fhir/`
- **Entwicklungsversion (next)**: `http://build.fhir.org/`

### Veröffentlichungszyklus
- Ungefähr **~18 Monate** zwischen Major Releases
- Ressourcen haben individuelle **Reifegrade** (Maturity Level / FMM = FHIR Maturity Model), in der Dokumentation durch Farben/Nummern neben den Ressourcen markiert

### Normative Ressourcen ab R4

> „Welche FHIR Version ist die richtige für mich? Die neueste! Seit R4 gibt es normative Ressourcen, diese ändern sich nur noch selten, und sind immer abwärtskompatibel."

- Vor R4: alle Ressourcen waren „Standard for Trial Use" (STU) → Änderungen jederzeit möglich
- Ab R4: normative Ressourcen (z. B. Patient, Observation) ändern sich nur bei zwingend nötigem Grund und sind **abwärtskompatibel**
- Nicht alle Ressourcen sind normativ – einige bleiben STU oder sind experimentell

### Kanonische URLs mit Versionsangabe

Kanonische URLs können eine explizite FHIR-Version enthalten:

```
http://hl7.org/fhir/4.0/StructureDefinition/Patient
```

Garantiert den Abruf der korrekten Ressourcendefinition für eine bestimmte Version.

## Abgrenzung

- **Ressourcen-Versionierung**: `meta.versionId` in einer Ressource ist die **Instanz-Version** (serverseitig verwaltet) – nicht die FHIR-Spezifikationsversion.
- **FHIR-Spezifikationsversion** (R4, R5) definiert das Schema und die normativen Anforderungen – verschieden von der Versionierung einzelner Ressourcen-Instanzen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind normative Ressourcen in FHIR, und ab welcher Version wurden sie eingeführt?

**Anwendungsfrage:** Ein Projekt startet eine FHIR-Implementierung. Welche Version sollte gewählt werden – und warum?

**Diskussionsfrage:** FHIR hat eine Stabilitätsschwäche – ständige Weiterentwicklung als Vorteil, aber auch als Nachteil. Wie adressiert das Konzept der normativen Ressourcen diesen Trade-off?

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen STU3 und R4 bezüglich der Ressourcenstabilität?
- Warum ist Abwärtskompatibilität bei normativen Ressourcen besonders wichtig in der Healthcare-IT?
- Was bedeutet der Reifegrad (FMM) einer Ressource für ihren Einsatz in Produktivsystemen?

## Verwandt

- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - Ressource Metadaten]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Reference]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 8, 30
