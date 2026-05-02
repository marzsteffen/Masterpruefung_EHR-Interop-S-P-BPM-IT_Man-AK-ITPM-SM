---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - ITSM Einführung Text]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - IT-Service - Business vs IT Service

> [!info] Kurzdefinition
> Business-Services sind die extern angebotenen Produkte und Dienstleistungen eines Unternehmens; IT-Services sind Leistungen, die mithilfe von IT für die Erbringung dieser Business-Services nötig sind oder direkt als Business-Service an Kunden angeboten werden.

## Beschreibung

Allweyer visualisiert die Beziehung in Abbildung 34 (Seite 127, in Anlehnung an [BuVi08]). Unternehmen bieten ihren Kunden Produkte und Dienstleistungen an — Business-Services. Um diese erbringen zu können, brauchen sie:

- **Mitarbeiter** und **Organisation**
- **Geschäftsprozesse**
- **Technologie** (Maschinen, Anlagen)
- **Vorleistungen** von Lieferanten und Dienstleistern (insbesondere IT-Services)

Analog brauchen IT-Services zur eigenen Erbringung wieder Mitarbeiter, IT-Prozesse, Technologie (Software und Hardware) sowie Vorleistungen von IT-Lieferanten und -Dienstleistern. IT-Services unterstützen also typischerweise Business-Services — sie können aber auch direkt einem externen Kunden angeboten werden, sodass IT-Service und Business-Service zusammenfallen.

Mit zunehmender Digitalisierung sind Business-Services laut Allweyer immer häufiger zugleich IT-Services oder Kombinationen aus IT-Services und sonstigen Dienstleistungen bzw. physischen Produkten. Daraus folgt: Die Bedeutung des IT-Servicemanagements wächst. Teilweise wird ITSM gar nicht mehr als separate IT-Aufgabe betrachtet, sondern als Teil eines übergreifenden Servicemanagements, das auch nicht-IT-Aspekte der Business-Services umfasst.

## Bestandteile / Aufbau

Beziehung laut Abbildung 34 (drei Ebenen):

| Ebene | Akteure / Inputs | Output |
|---|---|---|
| Business | Mitarbeiter / Organisation, Geschäftsprozesse, Maschinen/Anlagen, Partner/Lieferanten | Business-Services |
| IT-Services | (genutzt durch die Business-Ebene) | IT-Services |
| IT | Mitarbeiter / Organisation, IT-Prozesse, Software/Hardware, Partner/Lieferanten | IT-Services (Erbringung) |

Verbindung: Die Business-Ebene **nutzt** IT-Services, die IT-Ebene **erbringt** sie.

## Beispiel

Transportdienstleister (Allweyer):
- **Business-Service:** Transport schwerer Güter
- Erfordert: Geschäftsprozesse zur Planung/Durchführung, Disponenten und Fahrer, LKWs, Verladeeinrichtungen, ggf. Partner-Transporte
- **IT-Service:** Bereitstellung der Planungssoftware inkl. Zugang
- Erfordert: Planungssoftware, Server, IT-Mitarbeiter für Support/Administration, externes Wartungsunternehmen

Variante (rechte Seite Abb. 34): Das Transportunternehmen bietet Kunden eine Webseite, mit der diese ihre Transportaufträge selbst planen und optimieren können — hier ist der IT-Service direkt der Business-Service.

## Abgrenzung

- **Business-Service ≠ IT-Service:** Ein Business-Service ist die Außenleistung an den Kunden; ein IT-Service ist (meist) eine Innenleistung der IT-Abteilung an die Geschäftsbereiche oder Lieferanten-Vorleistung.
- **Servicemanagement vs. ITSM:** Servicemanagement umfasst auch nicht-IT-Aspekte. Eine Beschwerde sollte einheitlich bearbeitet werden — unabhängig davon, ob sie sich auf IT oder andere Leistungen bezieht.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Worin unterscheiden sich Business-Service und IT-Service? — Business-Service = externes Produkt/Dienstleistung des Unternehmens; IT-Service = Leistung mit IT, die meist als Vorleistung in Business-Services einfließt, manchmal aber auch direkt Business-Service ist.

**Anwendungsfrage:** Identifizieren Sie in einem gegebenen Unternehmen Business- und IT-Services. (Krankenhaus-IT-Beispiel anbieten: Business-Service „Patientenversorgung" → IT-Service „KIS-Bereitstellung", „Bildarchiv-Zugang", „Mobiler Visitenwagen-Support".)

**Diskussionsfrage:** Warum verschwimmt die Grenze zwischen Business- und IT-Service mit zunehmender Digitalisierung? Welche organisatorischen Konsequenzen hat das (ITSM als Teil eines übergreifenden Servicemanagements)? Wo liegen die Grenzen — sollten alle nicht-IT-Beschwerden auch im ITSM-Tool laufen?

**Mögliche Anschlussfragen:**
- Wann ist ein IT-Service zugleich ein Business-Service?
- Welche Rolle spielen Partner und Lieferanten in beiden Ebenen?
- Wie hängt das mit dem Source-Make-Deliver-Paradigma zusammen? *(im PDF nur referenziert auf Kap. 3.1.2 — nicht definiert)*

## Verwandt

- [[SM - IT-Service - Definition]]
- [[SM - IT-Service - Customer-Facing vs Supporting]]
- [[SM - IT-Servicemanagement - Aufgaben und Kernprozesse]]
- [[SM - Service-Katalog - Definition und Aufbau]]

## Quelle

- Vorlesung: [[SM - VL - ITSM Einführung Text]]
- Folien/Seitenangabe: Buchseiten 127–128, Abbildung 34 (in Anlehnung an [BuVi08])

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
