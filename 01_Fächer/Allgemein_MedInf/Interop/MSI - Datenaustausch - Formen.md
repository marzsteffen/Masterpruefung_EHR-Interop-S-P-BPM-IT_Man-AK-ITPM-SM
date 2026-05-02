---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Einführung in Standards und Interoperabilität]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Datenaustausch - Formen

> [!info] Kurzdefinition
> Drei Hauptformen, in denen Daten zwischen Akteuren ausgetauscht werden: Nachrichten (z. B. EDIFACT, HL7 v2/v3), Dokumente (z. B. CDA) und Ressourcen (FHIR-Resource-orientiert). Klassisch ergänzt durch Mündlich/Papier/Fax.

## Beschreibung

Folie 19 listet die Wege des Datenaustauschs:

- **Mündlich, (gemeinsam genutzte) Papierakten, Fax** (in der Folie ausgegraut – als historischer/parallel existenter Modus markiert).
- **Nachrichten** – Beispiele in der Folie:
  - EDIFACT-Snippet (`UNA`, `UNB`, `UNH`, `BGM` …)
  - HL7-v2-Snippet (`MSH|^~\&|NSI|...|ADT^A01^ADT_A01|...`)
- **Dokumente.**
- **Ressourcen.**

Die drei strukturierten Modi (Nachrichten / Dokumente / Ressourcen) sind in der Folie nicht weiter erläutert; sie entsprechen der HL7-Familie (v2/v3 als Nachrichten, CDA als Dokument, FHIR als Resource-Sammlung), ohne dass die Folie das explizit so verknüpft.

Folie 18 ergänzt: Im Gesundheitswesen gibt es **sehr viele Wege der Kommunikation**:
1. Zwischen Patient und Arzt (GDA).
2. Innerhalb eines Teams, z. B. im KH.
3. Teams zwischen Krankenanstalten, etwa Tumor Boards.
4. Zwischen Auftraggeber und Labor, Radiologieinstitut.
5. Zwischen niedergelassenen Ärzten und KH.
6. Abrechnungstransaktionen.

Sowie die Unterscheidung **gerichtete vs. ungerichtete Kommunikation** (siehe [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]).

## Bestandteile / Aufbau

| Form | Repräsentanten in der Folie | Bemerkung |
|---|---|---|
| Mündlich/Papier/Fax | – | Ausgegraut – nicht-digitaler Modus |
| Nachrichten | EDIFACT, HL7 (v2 als Snippet) | Ereignisgetrieben, kurzlebig |
| Dokumente | (HL7 CDA implizit) | Persistent, narrativ + strukturiert |
| Ressourcen | (FHIR implizit) | Granular, REST-orientiert |

## Beispiel

Folie 19 enthält ein konkretes HL7-v2-Beispiel:
```
MSH|^~\&|NSI||LAB||20140306271207599||ADT^A01^ADT_A01|NSI1|P|2.8
EVN|A01|201403271207599
PID|1||444-22-2222^^^HC^MR|Everywoman^Eve^E||19780113000000|F|||220 Home Street^^ANN ARBOR^^99999
NK1|1|Everyman^Adam|SPO|220 Home Street|555-555-2004
PV1|1|||301|R|||1436^Primary^Patricia^P|1026^Admit^Alan|998^Attend^Aaron|MED|||A|4|A0|N|1026^Sender^Sam|OB|H0100240
```

## Abgrenzung

- **Nachrichten ≠ Dokumente.** Nachrichten transportieren Ereignisse (Aufnahme, Entlassung) und sind eng in Workflows gekoppelt; Dokumente sind als Ganzes persistierbar und human-readable.
- **Dokumente ≠ Ressourcen.** Ein FHIR-Bundle kann ein Dokument simulieren, FHIR ist aber granular auf Resource-Ebene.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche drei strukturierten Formen des Datenaustauschs nennt die Vorlesung?

**Anwendungsfrage:** Welcher HL7-Vertreter passt zu welcher Form? (v2 → Nachrichten, CDA → Dokumente, FHIR → Ressourcen.)

**Diskussionsfrage:** Wann ist eine Nachricht der bessere Ansatz, wann ein Dokument, wann eine Ressource? Welche Kriterien ziehen Sie heran?

**Mögliche Anschlussfragen:**
- Welcher Form entspricht ELGA hauptsächlich? (Dokumente)
- Was sind typische Workflow-Trigger für HL7-v2-Nachrichten?
- Wie wird die FHIR-Resource-Logik in einem Bundle gebündelt? → [[MSI - HL7 FHIR - Bundle]]

## Verwandt

- [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]
- [[MSI - HL7 v2 - Nachrichtenstruktur]] (im PDF nur durch Beispiel erwähnt)
- [[MSI - HL7 CDA - Header]] (Querverweis Vorlesung 04)
- [[MSI - HL7 FHIR - Resource]] (Querverweis Vorlesung 06)
- [[MSI - Interoperabilitätsebenen - Technisch]]

## Quelle

- Vorlesung: [[MSI - VL - Einführung in Standards und Interoperabilität]]
- Folien/Seitenangabe: 18, 19
