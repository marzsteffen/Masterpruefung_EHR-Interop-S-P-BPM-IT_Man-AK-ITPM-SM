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

# MSI - HL7 FHIR - Ressource Metadaten

> [!info] Kurzdefinition
> Das `meta`-Element jeder FHIR-Ressource enthält technische Metadaten, die **ausschließlich vom Server verwaltet** werden: Versions-ID, Änderungszeitpunkt, Quelle, angewandte Profile, Sicherheits-Labels und Tags.

## Beschreibung

Die Metadaten einer FHIR-Ressource sind im `meta`-Element enthalten und werden nicht vom Client gesetzt oder verändert – der Server ist alleinig zuständig.

### Felder von `meta`

| Feld | Bedeutung |
|---|---|
| `versionId` | Ressourcen haben eine Versionshistorie; diese ID identifiziert die aktuelle Version |
| `lastUpdated` | Erstelldatum der aktuellen Version (zu `versionId`) |
| `source` | Originale Quelle, aus der die Ressource bereitgestellt wurde |
| `profile` | Profile, die zusätzlich zum Basisprofil angewendet werden |
| `security` | Labels für Sicherheitsschichten (z. B. Vertraulichkeitsklassen) |
| `tag` | Freie Informationen zur Verwendung der Ressource (keine semantischen Bedeutungsfelder) |

### Narrativer Text (`text`)

Als Teil von DomainResources gibt es zusätzlich das `text`-Element:
- **Soll** von jedem FHIR-System angezeigt werden können
- Muss genügend Information enthalten, um die Ressource allein verständlich zu machen
- Beinhaltet **nicht** alle strukturellen Informationen
- Vergleich CDA: In CDA ist der Narrative die Primärquelle; in FHIR ist er ein Anzeige-Ergänzungsfeld

## Bestandteile / Aufbau

```json
"meta": {
  "versionId": "2",
  "lastUpdated": "2024-12-05T10:00:00Z",
  "source": "http://hospital.example.org/fhir",
  "profile": ["http://hl7.at/fhir/3.0/StructureDefinition/AustrianPatient"],
  "security": [{"system": "...", "code": "N", "display": "Normal"}],
  "tag": [{"system": "...", "code": "example-tag"}]
}
```

## Abgrenzung

- `meta.profile` ist **optional** – eine Ressource muss nicht angeben, welche Profile sie erfüllt. Validierung erfolgt unabhängig davon.
- `meta.versionId` ist die **Instanz-Versionshistorie** der Ressource am Server – nicht die FHIR-Spezifikationsversion (R4/R5).
- `meta.tag` ist frei belegbar (kein Terminologie-Binding); `meta.security` hat definierte Wertesets für Vertraulichkeit und Zugriffskontrolle.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Felder enthält das `meta`-Element einer FHIR-Ressource?

**Anwendungsfrage:** Wie kann ein FHIR-Client herausfinden, ob eine Ressource ein bestimmtes nationales Profil erfüllt?

**Diskussionsfrage:** Warum werden Metadaten nur vom Server verwaltet, nicht vom Client? Was würde passieren, wenn Clients `versionId` selbst setzen könnten?

**Mögliche Anschlussfragen:**
- Wie funktioniert die Versionshistorie einer Ressource in FHIR? (→ `_history`-Endpoint)
- Was ist der Unterschied zwischen `meta.profile` und der tatsächlichen Profil-Konformität?
- Wie werden Security-Labels für Datenschutz und Zugriffssteuerung genutzt? (→ SMART on FHIR)

## Verwandt

- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Ressource Identity]]
- [[MSI - HL7 FHIR - Versionen]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - SMART on FHIR]]
- [[MSI - HL7 FHIR - REST API]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 FHIR Starter (Anna Lin)]]
- Folien/Seitenangabe: Seiten 19, 20
