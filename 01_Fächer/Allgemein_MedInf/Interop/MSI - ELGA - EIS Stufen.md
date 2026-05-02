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

# MSI - ELGA - EIS Stufen

> [!info] Kurzdefinition
> ELGA-Interoperabilitätsstufen (EIS) sind ELGA-spezifische Konformitäts­stufen zu den ELGA-CDA-Implementierungs­leitfäden. Drei Stufen: **EIS BASIC + STRUCTURED**, **EIS ENHANCED**, **EIS FULL SUPPORT**. Sie sind nicht identisch mit CDA-Levels, sondern fordern zusätzlich Konformität zu Spezifikationsvorgaben.

## Beschreibung

Wörtlich aus Folie 16:

| Stufe | Beschreibung |
|---|---|
| **EIS BASIC** und **EIS STRUCTURED** | Einheitlicher CDA-Header. Verwendung der Dokumente in ELGA (Aufnahme in Dokumentregister, Anzeige für Berechtigte). Minimale Anforderungen an erstellende Systeme („eingebettetes PDF" oder XML ohne Templates). EIS „Structured" erfüllt die fachlich-inhaltlichen, aber nicht die technischen Vorgaben für den Aufbau und die Gliederung des Dokuments aus den speziellen Leitfäden. |
| **EIS ENHANCED** | Einheitliche Dokumentation (Strukturierung, Gliederung), barrierefreie Darstellung. Minimale Anforderungen an Level-3-Codierung, gemäß den speziellen Leitfäden. |
| **EIS FULL SUPPORT** | Maschinenlesbare Inhalte, automatische Übernahme der Daten in ein medizinisches Informationssystem möglich. Volle Unterstützung der Level-3-Codierung, gemäß den speziellen Leitfäden. |

Folie 16 betont mit dem Titel **„ELGA-Interoperabilitätsstufen != CDA-Levels"** die Trennung der beiden Begriffe.

## Bestandteile / Aufbau

EIS-Stufe ergibt sich aus der Kombination aus **CDA-Level** und **Konformität zum ELGA-Implementierungs­leitfaden**:

| EIS-Stufe | CDA-Level | Konformität zum ELGA-Leitfaden | Maschinen­lesbarkeit |
|---|---|---|---|
| EIS BASIC | 1 (PDF im NonXMLBody) | Nur Header | minimal |
| EIS STRUCTURED | meist 2 | Inhaltlich konform, technisch nicht voll | Section-Ebene |
| EIS ENHANCED | 2/3 mit Mindest-Codierung | inhaltlich + technisch | teilweise Level 3 |
| EIS FULL SUPPORT | 3 mit voller Codierung | volle Konformität | vollständig |

## Beispiel

Aus dem CDA-Materialien-Ordner: `ELGA-043-Laborbefund_EIS-FullSupport.xml` ist ein Beispiel für EIS Full Support – mit allen Lab-Werten als Level-3-Entries kodiert.

## Abgrenzung

- **EIS-Stufe ≠ CDA-Level**. Folie 16 macht das explizit: ein Level-3-Dokument kann EIS Enhanced oder EIS Full Support sein – die EIS-Stufe sagt zusätzlich, *wie streng* der ELGA-Leitfaden eingehalten ist.
- **EIS BASIC ≠ Level 1**: meist deckungs­gleich, aber EIS BASIC fordert zusätzlich einen einheitlichen Header.
- **EIS ENHANCED ≠ EIS FULL SUPPORT**: ENHANCED hat Mindest-Codierung; FULL SUPPORT hat volle Codierung.

## Prüfungsrelevanz

**Sehr hoch** – klassische Verwechslungs-Falle.

**Typische Definitionsfrage:** Was sind die ELGA-EIS-Stufen, und wie unterscheiden sie sich von CDA-Levels?

**Anwendungsfrage:** Welche EIS-Stufe ist für ein Krankenhaus minimal vorgeschrieben, das Befunde an ELGA liefert? (BASIC.)

**Diskussionsfrage:** Warum reichen CDA-Levels nicht aus, um die ELGA-Konformität auszudrücken? (Antwort: Levels beschreiben nur den Body; ELGA fordert zusätzlich Header- und Template-Konformität.)

**Mögliche Anschlussfragen:**
- Welche Anforderungen erfüllt ein EIS-Enhanced-Dokument zusätzlich zu Level 2?
- Welche Konsequenzen hat es, wenn ein Krankenhaus nur EIS BASIC erfüllt?
- Wie wird die EIS-Stufe in den XDS-Metadaten codiert? → [[MSI - IHE XDS - Dokument-Metadaten]]

## Verwandt

- [[MSI - HL7 CDA - Levels]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - IHE XDS - Dokument-Metadaten]]
- [[EHR - ELGA - Architektur]]

## Quelle

- Vorlesung: [[MSI - VL - HL7 CDA und e-Befunde]]
- Folien/Seitenangabe: 16
