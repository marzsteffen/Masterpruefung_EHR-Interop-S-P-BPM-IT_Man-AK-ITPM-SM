---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - ITSM im Gesundheitswesen - Krankenhaus-Architektur

> [!info] Kurzdefinition
> Ein Krankenhaus lässt sich in drei Dienstebenen modellieren — Kernprozesse (Aufnahme → Anamnese → Diagnostik → Therapie → Entlassung), sekundäre Dienste (Diagnostik, Labor, Pflege, Patientenverwaltung) und tertiäre Dienste (Personalwesen, Finanzen, Einkauf, Reinigung u. a.) —, die alle durch IT als Querschnittsfunktion unterstützt werden.

## Beschreibung

Folien 27–28 (und 30) zeigen das Krankenhaus-Modell nach **Kutscha & Meier** (12. Fachtagung „Praxis der Informationsverarbeitung in Krankenhaus und Versorgungsnetzen", KIS, 2007). Das Modell ist ein konzentrisches Schema:

**Innen — Kernprozesse Krankenhaus** (5 Phasen):
1. Aufnahme
2. Anamnese
3. Diagnostik
4. Therapie
5. Entlassung

**Mittel — Sekundäre Dienste:** Diagnostik, Labor, Pflege, Patientenverwaltung.

**Außen — Tertiäre Dienste:** Personalwesen, Finanzen & Controlling, Einkauf & Materialwirtschaft, Reinigung, Logistik, Gebäudemanagement, Technische Dienste, Hotel Service, Speisenversorgung, Wäscherei.

**IT** wirkt als Querschnitt über alle drei Ebenen — das Buchstaben-„IT" steht laut Folie 27 außen rechts neben dem Modell und betont diesen Charakter.

Folie 28 listet die **Kernpunkte der Serviceorientierung** in einer Krankenhaus-IT (laut Kutscha & Meier):

- Ausrichtung auf Unternehmensziele
- Dienstleister–Kundenbeziehung
- Vereinbarung von Service-Levels (SLA)
- Kennzahlen zur Überwachung der SLAs
- Transparenz der Service-Qualität
- Verrechnung der Leistungen als Regulativ
- Cultural Change in der IT-Organisation
- ITIL als Modell aus Best-Practice-Empfehlungen

## Bestandteile / Aufbau

| Ebene | Inhalt | Rolle der IT |
|---|---|---|
| Kernprozesse | Aufnahme, Anamnese, Diagnostik, Therapie, Entlassung | KIS, eHealth-Anwendungen, Diagnostik-IT, Therapie-Dokumentation, Entlassbriefe |
| Sekundäre Dienste | Diagnostik, Labor, Pflege, Patientenverwaltung | LIS, Pflegedokumentation, Patientenverwaltungssysteme |
| Tertiäre Dienste | Personal, Finanzen, Einkauf, Reinigung, Logistik, Gebäudemanagement, Hotel, Speisen, Wäsche | ERP, HR-Systeme, Materialwirtschaft, Logistik-IT, Building Management Systems |

## Beispiel

Aus den IT-Dienstleistungs-Verrechnungsbereichen (Folie 30, siehe [[SM - ITSM - IT-Dienstleistungsverrechnung]]):

- **Rechenzentrum** → CPU-Zeit, Speicherplatz
- **Systemhaus** → Personentage, Lizenzkosten
- **PC/LAN** → Betreuung, SW-Lizenzen
- **Telekommunikation** → Gebühren, Wartungskosten

## Abgrenzung

- **Kernprozesse vs. sekundäre/tertiäre Dienste:** Kernprozesse sind die direkte Patientenversorgung; sekundäre Dienste unterstützen sie fachlich (Labor, Pflegeorganisation); tertiäre Dienste sind das Hintergrund-Funktionieren (Verwaltung, Hotellerie).
- **Krankenhaus-Modell vs. ITIL-Customer-Facing/Supporting** (siehe [[SM - IT-Service - Customer-Facing vs Supporting]]): Im Krankenhaus-Modell gibt es eine fachliche Hierarchie (Patientenversorgung als Mittelpunkt); im ITIL-Modell eine Service-Hierarchie (Customer-Facing/Supporting). Beide Hierarchien sind orthogonal — man kann sie zusammen darstellen.
- **Krankenhaus-IT vs. allgemeine IT**: Krankenhaus-IT hat zusätzliche Anforderungen (DSGVO, Patientensicherheit, Hochverfügbarkeit, Interoperabilität HL7/FHIR/DICOM).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche fünf Kernprozesse hat ein Krankenhaus laut Kutscha & Meier? — Aufnahme, Anamnese, Diagnostik, Therapie, Entlassung.

**Anwendungsfrage:** Ordnen Sie folgende IT-Services den drei Dienstebenen zu: KIS, ERP, LIS, Wäschereiplanung, Patientenverwaltung, RIS/PACS, Speisenplanung. — KIS, RIS/PACS → Kernprozesse; LIS, Patientenverwaltung → sekundär; ERP, Wäscherei, Speisen → tertiär.

**Diskussionsfrage:** Warum ist „Cultural Change" als eigener Kernpunkt der Serviceorientierung gelistet? — Weil die fachliche IT-Abteilung im Krankenhaus traditionell technikgetrieben ist; Service-Orientierung verlangt einen Mentalitätswechsel von „Wir betreiben Server" zu „Wir liefern messbare Services an Fachabteilungen".

**Mögliche Anschlussfragen:**
- Wie hängt das 5-Phasen-Krankenhausmodell mit den 5 Phasen einer serviceorientierten IT-Organisation zusammen ([[SM - 5 Phasen - serviceorientierte IT-Organisation]])? — Achtung Verwechslungsgefahr — sind unterschiedliche Modelle.
- Welche ITIL-Practices sind für die Krankenhaus-IT besonders relevant? — Incident Management (Hochverfügbarkeit), Information Security Management (DSGVO), Service Level Management (SLAs mit Fachabteilungen).
- Wie verhält sich das Modell zu eHealth-Anwendungen wie Telemedizin? — Erweitert die „Wäschereiplanung-Hierarchie" um patientennahe digitale Services über die Krankenhausgrenzen hinaus.

## Verwandt

- [[SM - 5 Phasen - serviceorientierte IT-Organisation]]
- [[SM - ITSM - IT-Dienstleistungsverrechnung]]
- [[SM - IT-Service - Customer-Facing vs Supporting]]
- [[SM - ITIL Practice - Service Level Management]]
- [[SM - IT-Servicemanagement - Definition Leutgeb]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 27–28; Quelle: Kutscha, A. & Meier, P. (2007), 12. Fachtagung Praxis der Informationsverarbeitung in Krankenhaus und Versorgungsnetzen (KIS)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
