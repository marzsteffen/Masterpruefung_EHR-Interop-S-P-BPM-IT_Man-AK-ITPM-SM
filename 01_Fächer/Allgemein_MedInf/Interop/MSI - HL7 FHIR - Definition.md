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

# MSI - HL7 FHIR - Definition

> [!info] Kurzdefinition
> HL7 FHIR (Fast Healthcare Interoperability Resources) ist ein offener, entwicklerorientierter Interoperabilitätsstandard von HL7 International, der auf modernen Web-Technologien (REST, JSON, XML) basiert und 80 % der Health-IT-Use-Cases out-of-the-box abdeckt.

## Beschreibung

### Kernaussagen aus dem Vortrag

**FHIR = Fast Healthcare Interoperability Resources**

Eigenschaften (laut Vortrag):
- **Fokus auf Entwickler**: niederschwelliger Zugang, vertraute Web-Technologien
- **Entwicklung anhand echter Use Cases**: praxisorientiert, kein rein theoretisches Modell
- **Einsatz moderner Technologien**: REST, JSON, XML, HTTP – Technologien, die Entwickler kennen
- **Ältere Standards ungeeignet für Mobilgeräte**: HL7 v2 und CDA zu schwergewichtig für mobile Apps
- **Open Source**: Implementierungen frei verfügbar

### 80/20-Regel

> „80 % der UseCases abgedeckt – 20 % anpassbar"

- Der Standard deckt die häufigsten Szenarien direkt ab
- Die restlichen 20 % werden über **Profilierung, Extensions und eigene Ressourcen** abgedeckt
- Kurs deckt **Kernkomponenten** ab (nicht die Erweiterungsmechanismen für Spezialfälle)
- Neue Datentypen vorhanden; Ressourcen erweiterbar und einschränkbar; API erweiterbar (Suche, Operationen)

### FHIR ist mehr als nur Ressourcen

FHIR umfasst über das reine Ressourcen-Modell hinaus:
- Nachrichtenübertragung
- Dokumente (FHIR Documents)
- Operationen (Custom Operations mit $)
- Prozessmanagement
- Referenzimplementierungen
- Infrastruktur
- Community-Erweiterungen (CDSHooks, FHIRCast, …)

### Vorteile vs. Nachteile (Standard-Perspektive)

| Vorteile | Nachteile |
|---|---|
| Ressourcen + API | Stabilität (häufige Versionen) |
| Infrastruktur, Frameworks, Community | Schwer zu meistern |
| Gesamtübersicht mit FHIR Documents | |
| Ständige Weiterentwicklung | |
| Auf eigene Anwendungsfälle erweiterbar | |
| Niederschwelliger Zugang | |

## Abgrenzung

- FHIR ist **kein Ersatz** für alle anderen Standards – für bestehende Nachrichtensysteme (HL7 v2) oder Dokumenten-Workflows (CDA) kann ein **FHIR Facade** sinnvoll sein.
- FHIR ist **kein garantierter Interoperabilitätsstandard** per se: „FHIR Server ≠ Interoperabilität" – ohne Profilierung und Implementation Guides bleibt der Standard unausgeschöpft.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet FHIR und was sind seine wesentlichen Eigenschaften?

**Anwendungsfrage:** Warum ist FHIR besonders für mobile und API-basierte Anwendungen geeignet?

**Diskussionsfrage:** Was bedeutet die 80/20-Regel für die Praxis? Wann reichen die 80 % nicht aus und wie begegnet FHIR dem? (→ Profilierung, Extensions, IGs)

**Mögliche Anschlussfragen:**
- Was ist der Unterschied zwischen FHIR als Ressourcen-Standard und FHIR als vollständigem Framework (Nachrichten, Dokumente, Operationen)?
- Welche Schwächen hat FHIR trotz Entwickler-Fokus? (Stabilität, Komplexität bei vollständiger Implementierung)
- Wie verhält sich FHIR zu HL7 v2 und HL7 CDA – Ablösung oder Koexistenz?

## Verwandt

- [[MSI - HL7 FHIR - Paradigmen]]
- [[MSI - HL7 FHIR - Versionen]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Deployment Muster]]
- [[MSI - HL7 CDA - Definition]]
- [[MSI - Datenaustausch - Formen]]
- [[MSI - Standards - Definition]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 6–10
