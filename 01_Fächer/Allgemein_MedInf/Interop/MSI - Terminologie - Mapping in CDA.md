---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Terminologien Anwendung]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologie - Mapping in CDA

> [!info] Kurzdefinition
> Praktische Drei-Stufen-Mapping-Architektur für Lab-Daten in ELGA: Lokales LIS → Umkodierung beim Befundexport → ELGA-CDA-Befund mit LOINC + UCUM + Bewertungscode → Import in das System des Empfängers mit Rück-Übersetzung in lokale Darstellung. Damit werden lokale Code-Inseln auf einen einheitlichen Standard abgebildet.

## Beschreibung

Folie 18 stellt das Problem dar: derselbe Laborparameter erscheint in fünf Laboren mit fünf verschiedenen Bezeichnungen, drei verschiedenen Einheiten und fünf verschiedenen Codes:

| Labor | Bezeichnung | Einheit | Code |
|---|---|---|---|
| Labor 1 | Eiweiß im Harn | g/l | 111 |
| Labor 2 | Protein im Urin | g/l | TP |
| Labor 3 | Gesamteiweiß im Harn | mg/l | CK8 |
| Labor 4 | Gesamteiweiß im Urin | mg/dl | S19 |
| Labor 5 | Totalprotein im Harn | g/l | 100 |

Quelle laut Folie: Dr. Hübl, 16.3.2011, HL7 Austria Jahrestagung.

Folie 19 zeigt die Lösung als Drei-Stufen-Mapping (Beispiel Transferrin-Befund):

```
Lokales System (LIS)        Transfe-SerPlas    4,1 g/l    (1,6–3,5)    H
       │
       │  Umcodierung beim Befundexport
       ▼
ELGA CDA Befund             Transferrin (3034-6)   4,1 g/l   (1,6–3,5)   +
                            Langtext   LOINC      UCUM      Bewertungscode
       │
       │  Import und Überführung in eigene Darstellung
       ▼
System des Empfängers       TF                  0.41 g/dl  (0.16–0.35)  ↑
                            Lokale Kürzel, Bewertung und umgerechnete Einheit
```

Die ELGA-Codierung ist die kanonische Mitte: einheitlicher Langtext, LOINC-Code, UCUM-Einheit, Bewertungscode. Sender und Empfänger können lokale Darstellungen behalten – die Brücke ist die ELGA-CDA-Repräsentation.

## Bestandteile / Aufbau

| Stufe | Was | Wer ist verantwortlich |
|---|---|---|
| Lokales System (LIS) | Lokale Kürzel, Bewertung, lokale Einheit | Hersteller/Labor |
| Umcodierung beim Befundexport | Mapping lokal → LOINC + UCUM | Schnittstelle des Senders |
| ELGA CDA Befund | LOINC + UCUM + Bewertung in einheitlicher Form | Standard (ELGA-Leitfaden) |
| Import beim Empfänger | Rück-Mapping in lokale Darstellung, Einheits-Umrechnung | Schnittstelle des Empfängers |

Schlüssel: jede Schnittstelle (Sender + Empfänger) muss das Mapping pflegen.

## Beispiel

Aus Folie 19 (Transferrin):
- Lokal: `Transfe-SerPlas`, `4,1 g/l`, Bewertung `H`.
- ELGA: `Transferrin`, LOINC `3034-6`, UCUM `g/l`, Bewertungscode `+`.
- Empfänger: `TF`, `0.41 g/dl` (umgerechnete Einheit), Bewertung `↑`.

Folie 18 illustriert das gleiche Konzept-Problem für Eiweiß im Harn – ohne Mapping bleiben die Labordaten nicht aggregierbar.

## Abgrenzung

- **Mapping in CDA ≠ Postkoordination.** Postkoordination ist Komposition innerhalb einer Terminologie; Mapping verbindet Codes zwischen lokalen Codes und Standards.
- **Drei-Stufen-Mapping ≠ Direkt-Mapping**. Beim Direktmapping zwischen zwei Systemen bräuchten n×(n-1) Mappings; mit ELGA als Hub reichen n Mappings.
- **Bewertungscode in ELGA ≠ Bewertung lokal**. Lokale Bewertungen wie `H`/`↑` werden auf einen ELGA-Bewertungscode (z. B. `+`) gemappt – das vereinheitlicht klinische Interpretation.

## Prüfungsrelevanz

**Sehr hoch.** Klassisches Praxis-Beispiel.

**Typische Definitionsfrage:** Skizzieren Sie die Drei-Stufen-Mapping-Architektur für Lab-Daten in ELGA.

**Anwendungsfrage:** Sie übernehmen ein Krankenhaus, das einen LIS-Befund nach ELGA exportieren muss. Welche Mapping-Schritte fallen an?

**Diskussionsfrage:** Warum vereinheitlicht ELGA als Hub und nicht durch direktes Mapping zwischen allen Sender-Empfänger-Paaren? Welche Vorteile hat das?

**Mögliche Anschlussfragen:**
- Welche Rolle spielt UCUM bei der Einheits-Umrechnung?
- Wie wird der Bewertungscode normiert?
- Welche Cimino-Desiderata adressiert das Drei-Stufen-Mapping? (Recognize Redundancy, Multiple Consistent Views.)

## Verwandt

- [[MSI - Terminologie - Mapping]]
- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - UCUM - Definition]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Cimino Desiderata]] (Recognize Redundancy)

## Quelle

- Vorlesung: [[MSI - VL - Terminologien Anwendung]]
- Folien/Seitenangabe: 18, 19 (Quelle der Tabelle: Dr. Hübl, HL7 Austria Jahrestagung 16.3.2011)
