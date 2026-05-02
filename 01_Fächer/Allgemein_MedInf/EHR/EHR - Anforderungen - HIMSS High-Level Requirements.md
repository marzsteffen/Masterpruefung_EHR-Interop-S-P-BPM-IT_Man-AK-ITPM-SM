---
fach: ehr
typ: konzept
status: offen
quelle: "[[EHR - VL - Einführung und Definitionen]]"
tags:
  - fach/allgemein/ehr
  - typ/konzept
  - status/offen
---

# EHR - Anforderungen - HIMSS High-Level Requirements

> [!info] Kurzdefinition
> Vier High-Level-Anforderungsblöcke, die das HIMSS Electronic Health Record Definitional Model (Version 1.0) für EHR-Systeme aufstellt: Access & Reliability, Data Entry, User Friendliness, Data Protection.

## Beschreibung

Die Vorlesung zitiert das **HIMSS Electronic Health Record Definitional Model Version 1.0** als eine von zwei Quellen funktionaler Anforderungen (Folie 42). Die High-Level-Requirements sind kategorisch und werden jeweils mit konkreten Sub-Anforderungen konkretisiert.

## Bestandteile / Aufbau

### High-Level 1 – Access & Reliability
- Sichere, zuverlässige, Echtzeit-Zugriff auf Patientendaten
- 24/7 verfügbar
- Integration in den klinischen Workflow (kein „Bremsen")
- Zugriff dort, wo benötigt (Klinik, PCP = Primary Care Provider, andere Versorger, Patient zu Hause, „on the tram")
- Werkzeuge für Zugriff inkl. **Access Audit Trails** (wer, was, wann)
- Vertraulichkeit und Sicherheit
- Konkretisiert: > 99,9 % Verfügbarkeit, akzeptable Antwortzeit

### High-Level 2 – Data Entry
- Direkte Eingabe (manuell oder automatisch) ins EHR – nicht abtippen
- Datenintegration aus Quellen, auf die das EHR nur verlinkt (Registry vs. Repository)
- Erfordert gute Synchronisation
- **Point-of-Care-Dokumentation**: SOAP-Note vor Verlassen des Patienten abschließen, Vitalwerte am Krankenbett (nicht erst am Schichtende)
- Storage von Bildern/Video/Audio bzw. Verlinkung (RIS, PACS)
- Automatisches Linking von Labordaten, EKG, Wearables, „insideables"
- Granularitäts-Diskussion (z. B. ganzes EKG vs. Interpretation)
- Text-Eingabe (Diktat, Voice Recognition, OCR alter Dokumente: PDF, Word, Excel, HTML)
- Coded Data: HL7-v2, XML, JSON

### High-Level 3 – User Friendliness
- Daten leicht eingeben und abrufen
- Vermeidung von „Typing over"
- Filterbarkeit (Datum, Quelle, Problem)
- Granularität
- Time series, Verlauf
- Gut strukturierte GUIs, gute Navigation, akzeptable Antwortzeiten
- Verständlichkeit für die Zielgruppe
- Dashboards / CTMS-Systeme (Begriff CTMS im PDF nicht definiert)

### High-Level 4 – Data Protection
- Klare Zugriffsregeln (Read/Write/Update)
- Klare Regeln, wer welche Patientendaten sehen darf, und wie lange
- Verschlüsselte Datenbanken/Repositories
- Backup & Recovery
- Sicherer Transport (https)
- Authentifizierung & Passwortsicherheit
- **Logging**: wer hat wann was getan – Patient muss Log einsehen können

## Beispiel

PDF verweist auf einen BBC-News-Bericht zu Datenpannen (Folie 53) – als Mahnung zur Wichtigkeit dieses Blocks.

## Abgrenzung

- HIMSS High-Level Requirements adressieren funktionale Anforderungen einer **einzelnen** EHR-Implementierung. Die [[EHR - Anforderungen - IOM 8 Core Requirements]] sind kategorisch ähnlich, betonen aber stärker den **Versorgungs-Ablauf** (Result Management, Order Management, Reporting).
- Die hier formulierten Sicherheitsanforderungen werden in [[ASP - MOC]] formal vertieft (Authentifizierung, Audit, Verschlüsselung).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier High-Level-Requirements stellt HIMSS an EHR-Systeme?

**Anwendungsfrage:** Welche dieser Anforderungen sind in ELGA umgesetzt – mit welchen Lücken? (Diskussion offen, da im PDF nicht abschließend beantwortet)

**Diskussionsfrage:** Granularität bei Data Entry – ist es sinnvoll, das ganze EKG zu speichern oder nur die Interpretation? Trade-off zwischen Datenmenge, Re-Analyse-Möglichkeit und Performance.

**Mögliche Anschlussfragen:**
- Wie verhält sich der Audit-Trail-Anspruch zu DSGVO-Artikel 15 (Auskunftsrecht)?
- „Replicate the workflow" vs. „integrate with the clinician workflow" – wo ist die Grenze?
- Welche dieser Anforderungen sind 2024 Stand der Technik, welche immer noch Forschungsthemen?

## Verwandt

- [[EHR - Anforderungen - IOM 8 Core Requirements]]
- [[EHR - Anforderungen - Funktional vs Technisch]]
- [[EHR - Funktionen - Basisfunktionen]]
- [[EHR - Architektur - Registry vs Repository]]
- [[ASP - Audit Trail]]
- [[ASP - Verschlüsselung im Transport]]

## Quelle

- Vorlesung: [[EHR - VL - Einführung und Definitionen]]
- Folien/Seitenangabe: Folien 42–53 (HIMSS High-Level Requirements 1–4)
