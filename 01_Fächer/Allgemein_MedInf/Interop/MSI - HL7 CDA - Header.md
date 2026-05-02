---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - HL7 CDA und e-Befunde]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - HL7 CDA - Header

> [!info] Kurzdefinition
> Der CDA-Header enthält administrative Metadaten des Dokuments: Titel, Erstellungsdatum, Dokumentenklasse + ID + Version, Patient, Patientenkontakt, Verfasser, rechtlicher Unterzeichner, Verwahrer (Custodian), fachlicher Ansprechpartner, einweisender Arzt, Zuweisung/Ordermanagement, Aufnahme- und Entlassungsdatum (ServiceEvent).

## Beschreibung

Folie 12 zeigt die ELGA-Pflicht-Header-Elemente ab EIS Basic (2015):

| CDA-Header-Element | Anwendung ab EIS Basic |
|---|---|
| Titel des Dokuments | Verpflichtend |
| Erstellungsdatum des Dokuments | Verpflichtend |
| Dokumentenklasse (codiert) | Verpflichtend |
| Dokumenten-ID | Verpflichtend |
| Versionsnummer (ggf. mit Verweis auf Vorversion) | Verpflichtend |
| Patient (Name, Geburtsdatum, Adresse, SVNR …) | Verpflichtend |
| Patientenkontakt (Aufenthalt) | Verpflichtend |
| Verfasser des Dokuments (Name, Organisation) | Verpflichtend |
| Rechtlicher Unterzeichner (Name, Organisation) | Verpflichtend |
| Verwahrer des Dokuments (Organisation) | Verpflichtend |
| Fachlicher Ansprechpartner (Name, Organisation) | Verpflichtend |
| Einweisender Arzt (Name, Organisation) | Wenn vorhanden |
| Personen der Dateneingabe | Optional |
| Beabsichtigte Empfänger | Optional |
| Weitere Beteiligte (Hausarzt, Notfallkontakt, Angehörige, Versicherung, Betreuende Organisation) | Optional |
| Zuweisung und Ordermanagement | – |
| Aufnahme- und Entlassungsdatum (ServiceEvent) | Verpflichtend |

Die Header-Pflichten gelten unabhängig vom CDA-Level (siehe Abgrenzung in [[MSI - ELGA - EIS Stufen]]).

## Bestandteile / Aufbau

Vier Hauptcluster im Header:
1. **Dokument-Identität**: Titel, ID, Version, Erstellungsdatum, Dokumentenklasse.
2. **Patient-Bezug**: Patientendaten, Aufenthalt, ServiceEvent.
3. **Verantwortliche**: Verfasser, rechtlicher Unterzeichner, Verwahrer (Custodian), fachlicher Ansprechpartner.
4. **Optionale Beteiligte**: einweisender Arzt, Dateneingabe, Empfänger, weitere Beteiligte.

## Beispiel

Aus Folie 10:
```
<legalAuthenticator>
  <time value="20080530140803"/>
  <signatureCode code="S"/>
  <assignedEntity>
    <id assigningAuthorityName="h.elga" root="1.1.2.3.127.4"/>
    <assignedPerson>
      <name>Dr. Cardiologist</name>
    </assignedPerson>
    <representedOrganization>
      <name>General University Hospital Graz</name>
      <telecom value="tel:+43-316-385.2544"/>
      <addr>...</addr>
    </representedOrganization>
  </assignedEntity>
</legalAuthenticator>
```

Das ist der „Rechtliche Unterzeichner" – verpflichtend ab EIS Basic.

## Abgrenzung

- **Header ≠ Body**: Header trägt Metadaten, Body trägt klinischen Inhalt.
- **Verfasser ≠ Rechtlicher Unterzeichner**: Verfasser hat das Dokument geschrieben, der rechtliche Unterzeichner haftet rechtlich (z. B. Oberarzt unterzeichnet, was der Assistenzarzt geschrieben hat).
- **Custodian ≠ Verfasser**: Custodian ist die *Organisation*, die das Dokument verwaltet/aufbewahrt, der Verfasser ist die Person, die es erstellt hat.

## Prüfungsrelevanz

**Sehr hoch.**

**Typische Definitionsfrage:** Welche Pflichtfelder hat der CDA-Header in ELGA ab EIS Basic?

**Anwendungsfrage:** Identifizieren Sie in einem CDA-Snippet die Header-Elemente und ordnen Sie sie der ELGA-Pflicht-Tabelle zu.

**Diskussionsfrage:** Warum trennt CDA Verfasser, Rechtlicher Unterzeichner und Custodian? Welche Probleme entstehen, wenn man sie zusammenführt?

**Mögliche Anschlussfragen:**
- Was ist eine Dokumenten-ID, was eine Versionsnummer?
- Welche Datentypen werden für Patient verwendet (PN, AD, …)? → [[MSI - HL7 CDA - Datentypen]]
- Wie hängt der Header mit den IHE-XDS-Metadaten zusammen? → [[MSI - IHE XDS - Dokument-Metadaten]]

## Verwandt

- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Eigenschaften]]
- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - IHE XDS - Dokument-Metadaten]]
- [[MSI - ELGA - EIS Stufen]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 10, 12
