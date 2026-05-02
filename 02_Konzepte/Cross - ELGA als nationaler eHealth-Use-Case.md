---
typ: konzept
status: offen
faecher: [ehr, msi]
quellen:
  - "[[EHR - ELGA - Technologie-Architektur]]"
  - "[[EHR - Architektur - Zentral vs Dezentral]]"
  - "[[EHR - Architektur - Registry vs Repository]]"
  - "[[MSI - ELGA - EIS Stufen]]"
  - "[[MSI - HL7 CDA - Levels]]"
  - "[[MSI - HL7 CDA - Implementierungsleitfäden]]"
  - "[[MSI - HL7 CDA - Templates]]"
  - "[[MSI - HL7 CDA - ART-DECOR]]"
  - "[[MSI - IHE XDS - Architektur]]"
  - "[[MSI - IHE XDS - Dokument-Metadaten]]"
  - "[[MSI - Terminologie - Management in Österreich]]"
tags:
  - typ/konzept
  - status/offen
  - cross-fach
  - fach/allgemein/ehr
  - fach/allgemein/msi
---

# Cross - ELGA als nationaler eHealth-Use-Case

> [!info] Kurzdefinition
> ELGA wird in beiden Fächern behandelt, aber komplementär: EHR liefert die *Architektur-Sicht* (HL7-v3 CDA-Dokumente, dezentrale Repositories, zentraler Index, IHE-Profile, zeitlicher Ausbau), MSI liefert die *Standard-Mechanik* (EIS-Konformitätsstufen, ELGA-Implementierungsleitfäden, Templates, ART-DECOR, XDS-Akteure und -Metadaten, Terminologie-Management). Erst beide Sichten zusammen geben ein vollständiges ELGA-Bild für die mündliche Prüfung.

## Sicht aus Fach EHR

EHR betrachtet ELGA als *konkrete nationale EHR-Implementation* — also als Anwendungsfall in der Architektur-Diskussion „zentral vs. dezentral" und „Registry vs. Repository".

**Technologie-Architektur** (siehe [[EHR - ELGA - Technologie-Architektur]], Folien 8–9):

- Datenformat: **HL7-v3 CDA-Dokumente (XML)**, mit eigenem Implementation Guide pro Dokumenttyp.
- Architektur: **dezentrale Repositories** + **zentrales System** für Zugriffsautorisierung und Document-Lookup.
- Document-Lookup über **IHE-Profile (XDS u. a.)** — Cross-Enterprise Document Sharing als Standardisierungsschicht.

**Zeitlicher Ausbau der ELGA-Inhalte** (Folie 8):

| Zeitraum | Hinzugefügt |
|---|---|
| Anfangs | Entlassungsbriefe, Laborbefunde, Radiologiebefunde |
| 2017–2018 | e-Medikation |
| 2021 | e-Impfpass |
| Offen | COVID-19-Test-Ergebnisse, Reha-Berichte, Befunde nicht-stationärer Versorger |

**Architektur-Einordnung**:

- ELGA = **semi-zentralisiert**: dezentrale Daten + zentraler Index — siehe [[EHR - Architektur - Registry vs Repository]] (zentrale Registry, dezentrale Repositories) und [[EHR - Architektur - Zentral vs Dezentral]]. Beide EHR-Architektur-Notes nennen ELGA explizit als Diskussionsbeispiel; die EHR-Vorlesung beantwortet die Frage „Welches Design hat ELGA?" allerdings nicht direkt — sie wird als Übungsfrage gestellt.
- Datenformat ist CDA, **nicht** FHIR (Stand der Vorlesung). FHIR-Migration im Diskurs, im PDF nicht detailliert.

## Sicht aus Fach MSI

MSI behandelt ELGA als *konkretes Anwendungsfeld der CDA-/IHE-Standardfamilie* — also als Beispiel, an dem die Standard-Mechanik durchexerziert wird.

**EIS-Konformitätsstufen** (siehe [[MSI - ELGA - EIS Stufen]], Folie 16):

| Stufe | Inhalt |
|---|---|
| **EIS BASIC** und **EIS STRUCTURED** | Einheitlicher CDA-Header, Aufnahme in Dokumentregister, minimale Anforderungen — von „eingebettetes PDF" bis fachlich-inhaltlich konform, aber technisch nicht voll. |
| **EIS ENHANCED** | Einheitliche Strukturierung/Gliederung, barrierefreie Darstellung, Mindest-Anforderungen an Level-3-Codierung. |
| **EIS FULL SUPPORT** | Maschinenlesbare Inhalte, automatische Übernahme in medizinische Informationssysteme, volle Level-3-Codierung. |

Wichtig: Folie 16 trägt explizit den Titel **„ELGA-Interoperabilitätsstufen != CDA-Levels"** — das ist eine bewusste Trennung des Standards von ELGA's Konformitätsbegriff.

**ELGA-Implementierungsleitfäden** (siehe [[MSI - HL7 CDA - Implementierungsleitfäden]], Folie 37):

- **Maximalset**: Nur beschriebene Strukturen sind gültig.
- Vorgaben für Header (Dokumentkennung, Metadaten, Codes, Value Sets), Body (Section-Struktur, Reihenfolge, narrative Anteile) und Entry-Level (codierte Einzelelemente).
- Bausteinartig über wiederverwendbare Templates, modelliert in ART-DECOR.
- Allgemeiner Leitfaden + spezielle Leitfäden (Entlassungsbrief Ärztlich, Entlassungsbrief Pflege, Laborbefund, Befund Bildgebende Diagnostik, eMedikation Rezept/Abgabe/Medikationsliste/Pharmazeutische Empfehlung, Pflegesituationsbericht).

**ELGA-Templates** (siehe [[MSI - HL7 CDA - Templates]], Folien 38, 40, 48):

- Vier Template-Typen: Document, Header, Section, Entry Level.
- Beispielhafte Template-IDs aus dem ELGA-Kontext: eMedikationRezept (`1.2.40.0.34.11.8.1`), Problem/Bedenken Entry (`1.2.40.0.34.11.1.3.5`), Medikation Verordnung (`1.2.40.0.34.11.8.1.3.1`), Medikation Abgabe (`1.2.40.0.34.11.8.2.3.1`).
- Mehrfache Template-IDs auf einem Element möglich — gleichzeitige Konformität zu ELGA, IHE PCC, HL7 CCD.

**ART-DECOR als Modellierungsplattform** (siehe [[MSI - HL7 CDA - ART-DECOR]], Folien 40–41):

- ELGA-Templates werden in ART-DECOR modelliert (URL: `https://elga.art-decor.org/`).
- Output: Schematron-Regeln für den ELGA Online-Validator + HTML/PDF-Dokumentation.
- Trennung: Datasets (konzeptuell) ↔ Templates (technisch) ↔ Terminology (Codes/Value Sets).

**IHE-XDS-Architektur** (siehe [[MSI - IHE XDS - Architektur]], Folie 34) — von ELGA genutzt:

- Akteure: Patient Identity Source, Document Source, Document Repository, Document Registry, Document Consumer, On-Demand Document Source.
- Transaktionen: ITI-8/44 (Patient Identity Feed), ITI-41 (Provide & Register), ITI-42 (Register Document Set), ITI-43 (Retrieve Document Set), ITI-18 (Stored Query), ITI-61 (On-Demand Entry).
- Trennung Speicherung (Repository) vs. Suche (Registry) — ELGA nutzt diese Aufteilung direkt.

**XDS-Metadaten** (siehe [[MSI - IHE XDS - Dokument-Metadaten]], Folien 35–36):

Vier funktionale Cluster, die jedem ELGA-Dokument anhängen müssen:

1. **Wer**: Autor, Organisation des Autors, Art der Organisation, Rolle, Funktionscode, rechtlicher Unterzeichner.
2. **Wann**: Erstellungsdatum, Start/Ende der Gesundheitsdienstleistung.
3. **Wer (Patient)**: Patientendaten zum Zeitpunkt der Dokumenterstellung.
4. **Was/Wie**: Titel, Dokumentenklasse, Dokumententyp, Fachrichtung, Gültigkeit (Approved/Deprecated), **EIS-Interoperabilitätsstufe**.

**Terminologie-Management in Österreich** (siehe [[MSI - Terminologie - Management in Österreich]], Folie 17):

- Lebenszyklus-Aufgaben: Suche/Auswahl, Value-Set-Erstellung, Übersetzung/Mapping, Code-Einbringung, Wartung, Verteilung, Lizenz-Management, Validierung-Integration.
- Verteilungs-Tool: termgit.elga.gv.at (Terminologieserver).
- Schematron-Validatoren prüfen automatisch Code-Konformität gegen referenzierte Value Sets.

## Gemeinsamkeiten

| Aussage | Beide Fächer |
|---|---|
| Datenformat | HL7-v3 CDA, XML-basiert |
| Konformitäts­schicht über CDA-Standard | EHR: „Implementation Guide pro Dokumenttyp"; MSI: „Maximalset + spezielle Leitfäden" |
| IHE-XDS als Document-Lookup-Layer | EHR nennt es als Architektur-Komponente, MSI führt es technisch aus |
| Dezentrale Datenhaltung + zentraler Index | EHR macht es zur Architektur-Aussage, MSI macht es zur XDS-Akteur-Aussage (Registry vs. Repository) |

## Unterschiede / Konflikte / unterschiedliche Schwerpunkte

**1. Asymmetrische Detailtiefe.**

- EHR-Note `EHR - ELGA - Technologie-Architektur` ist *eine* Note, die alles auf 5 Bestandteile zusammenfasst (Format, IGs, dezentrale Repositories, zentrales System, IHE-Profile).
- MSI hat das Thema auf *mindestens 7 Notes* verteilt (EIS Stufen, Implementierungsleitfäden, Templates, ART-DECOR, XDS Architektur, XDS Metadaten, Terminologie-Management Österreich).

Konsequenz: Wenn der Prüfer bei „ELGA-Architektur" einsteigt, hat man es leicht mit der EHR-Note. Geht er auf Details (EIS-Stufe, Templates, ART-DECOR, XDS-Akteure, ITI-Transaktionen, XDS-Metadaten), kommt die Antwort aus MSI.

**2. „Welches Design hat ELGA?" — nicht beantwortet im EHR-PDF.**

Folie 39 der EHR-Vorlesung („Some interesting design questions") stellt explizit die Frage „Welches Design hat ELGA?" und beantwortet sie nicht. [[EHR - Architektur - Zentral vs Dezentral]] markiert das als Diskussionsanstoß. Die Antwort liegt in [[EHR - ELGA - Technologie-Architektur]] (semi-zentralisiert: dezentrale Repositories + zentraler Index) und wird durch die MSI-XDS-Notes mechanisch erklärt.

**3. EIS-Stufe als XDS-Metadatum.**

Beide Fächer behandeln EIS, aber mit anderem Fokus:
- MSI's [[MSI - ELGA - EIS Stufen]] erklärt, *was* die Stufen inhaltlich bedeuten.
- MSI's [[MSI - IHE XDS - Dokument-Metadaten]] führt das XDS-Metadatum „ELGA Interoperabilitätsstufe" — die EIS-Stufe wird also nicht nur am Dokument selbst geführt, sondern auch im XDS-Index, damit Konsumenten filtern können.
- EHR thematisiert EIS-Stufen **nicht**.

**4. Verwechslungsfalle CDA-Level / EIS-Stufe / FHIR-5-Levels.**

Identisch zur Brücke 1: Drei Begriffe mit „Level"/„Stufe", die nichts miteinander zu tun haben:
- CDA-Level 1/2/3 (Body-Strukturierung) — siehe [[MSI - HL7 CDA - Levels]].
- ELGA-EIS-Stufe (BASIC/STRUCTURED/ENHANCED/FULL SUPPORT) — siehe [[MSI - ELGA - EIS Stufen]]. „EIS != CDA-Levels" steht als Folie-Titel.
- FHIR-5-Levels (Foundation/Conformance/Master Data/Operational Data/Knowledge) — gehört nicht direkt zu ELGA, aber dient als Kontrast.

EIS ergibt sich aus *Kombination* aus CDA-Level + Konformität zum ELGA-Leitfaden (Folie 16). Ein Level-3-Dokument kann EIS Enhanced *oder* EIS Full Support sein — die EIS-Stufe sagt zusätzlich, *wie streng* der ELGA-Leitfaden eingehalten ist.

**5. ELGA-spezifische Tools / Plattformen.**

- MSI nennt: ART-DECOR (`https://elga.art-decor.org/`), termgit.elga.gv.at, ELGA-Online-Validator, ELGA-Referenzstylesheet.
- EHR nennt: keine spezifischen Tools.

**6. Dokumenttypen-Liste.**

EHR-Note listet ELGA-Inhalte als zeitlichen Ausbau (Entlassungsbriefe, Laborbefunde, Radiologie, e-Medikation, e-Impfpass). MSI-Note listet ELGA-Dokumenttypen als technische Templates (Entlassungsbrief Pflege/Ärztlich, Laborbefund, Befund Bildgebende Diagnostik, eMedikation Rezept/Abgabe/Medikationsliste/Pharmazeutische Empfehlung, Pflegesituationsbericht). Beide Listen überlappen, aber die MSI-Liste ist genauer (z. B. Entlassungsbrief in zwei Varianten Pflege/Ärztlich, e-Medikation in vier Sub-Templates) und stammt aus den ELGA-Templates direkt.

## Synthese für die mündliche Prüfung

**Diskussions-Achse 1: „Wie funktioniert ELGA technisch?"**

Antwort braucht beide Fächer und führt vom Außen nach Innen:

1. **EHR-Architektur-Frame** ([[EHR - ELGA - Technologie-Architektur]]): semi-zentralisiert — dezentrale Repositories bei Versorgern + zentrales System für Auth + Lookup, IHE-Profile als Standardisierungsschicht.
2. **MSI-Mechanik-Frame** ([[MSI - IHE XDS - Architektur]]): konkret IHE XDS mit sechs Akteuren und ITI-Transaktionen.
3. **MSI-Datenmodell-Frame** ([[MSI - IHE XDS - Dokument-Metadaten]]): XDS-Metadaten als „Wer/Wann/Wer (Patient)/Was-Wie"-Cluster, EIS-Stufe als Filter-Metadatum.
4. **MSI-Konformitäts-Frame** ([[MSI - ELGA - EIS Stufen]] + [[MSI - HL7 CDA - Implementierungsleitfäden]] + [[MSI - HL7 CDA - Templates]] + [[MSI - HL7 CDA - ART-DECOR]]): Implementation Guides als Maximalset, EIS-Stufen als Konformitätsklassifikation, ART-DECOR als Modellierungsplattform.

Saubere Antwort kettet diese vier Frames zusammen. Mit dem dezentralen Architektur-Argument starten, dann die XDS-Mechanik einführen, dann die Dokument-Konformität (EIS) als Brücke zwischen Architektur und Inhalt erklären.

**Diskussions-Achse 2: „Was passiert, wenn ein Krankenhaus einen Entlassungsbrief in ELGA einbringt?"**

Sehr typische Anwendungsfrage. Antwort kombiniert beide Fächer:

1. Krankenhaus erstellt CDA-XML-Dokument konform zu „Entlassungsbrief Ärztlich"-Implementierungsleitfaden (MSI).
2. Konformität zu EIS Enhanced oder Full Support, je nach Codierungsgrad (MSI).
3. Validierung gegen Schematron, gespeist aus ART-DECOR-Modell (MSI).
4. Provide & Register über ITI-41 ins ELGA-Repository (MSI XDS).
5. Repository meldet sich über ITI-42 bei der Registry an (MSI XDS).
6. XDS-Metadaten werden gefüllt, inklusive EIS-Stufe als Filter (MSI XDS-Metadaten).
7. Dokument liegt in dezentralem Repository, ist aber zentral via Registry findbar (EHR Architektur).

**Diskussions-Achse 3: „CDA-Level vs. EIS-Stufe."**

Klassische Verwechslung, in MSI explizit als Folie-Titel benannt: **„ELGA-Interoperabilitätsstufen != CDA-Levels"**. CDA-Level = Body-Strukturierung (Standard). EIS-Stufe = Konformität zum ELGA-Leitfaden + ELGA-Header + ELGA-Templates (Anwendung). Ein Level-3-Dokument muss nicht EIS Full Support sein — die EIS-Stufe ist strenger und erfordert Konformität zu Leitfaden-Vorgaben.

**Diskussions-Achse 4: „Warum CDA und nicht FHIR?"**

EHR-Note stellt die Frage explizit als Diskussionsfrage: „Warum CDA und nicht FHIR? Welche historischen, technischen und organisatorischen Gründe bestehen?" — sie wird im PDF nicht beantwortet. Saubere Antwort: ELGA wurde entwickelt, als CDA der etablierte Standard war (siehe Brücke 1, [[Cross - HL7 FHIR und CDA in MSI vs EHR]]). FHIR-Migration ist im Diskurs, aber nicht produktiv — die existierenden Implementierungsleitfäden, ART-DECOR-Modelle, Schematron-Validatoren, Templates und IHE-XDS-Akteure sind alle CDA-zentriert. Eine FHIR-Migration wäre eine Re-Implementierung der gesamten Konformitätsschicht.

**Diskussions-Achse 5: „Wo ist ELGA in der Architektur-Diskussion ‚zentral vs. dezentral'?"**

Antwort aus EHR + MSI: ELGA ist *zentral indizierter, dezentral gespeicherter* Datenbestand. Es ist also keine reine Repository (das wäre alles zentral) und keine reine Registry (das wäre nur Verweise zentral, ohne Speicher-Garantie) — sondern eine Hybrid-Architektur: zentrale Document Registry (XDS-Akteur), aber dezentrale Document Repositories (XDS-Akteur). Das ist die genaue Antwort auf die in [[EHR - Architektur - Zentral vs Dezentral]] und [[EHR - Architektur - Registry vs Repository]] offen gestellten Diskussionsfragen.

**Anschlussfragen, die ohne Cross-Fach-Verständnis schwer zu beantworten sind:**

- „Welche EIS-Stufe braucht ein Krankenhaus minimal, um ELGA zu beliefern?" → BASIC, MSI-Quelle.
- „Wer ist der Document Registry-Aktor in ELGA?" → MSI-XDS, beantwortet mit Bezug auf EHR-Architektur.
- „Wie wird die EIS-Stufe technisch geführt?" → MSI XDS-Metadaten — als codiertes Filter-Metadatum.
- „Wo werden ELGA-Codes gepflegt?" → termgit.elga.gv.at, MSI Terminologie-Management Österreich.
- „Was sind ART-DECOR-Datasets vs. Templates vs. Terminology?" → MSI ART-DECOR-Note.
- „Wie funktioniert die ELGA-Validierung?" → Schematron, generiert aus ART-DECOR, MSI-Quelle.

## Verwandt

**EHR:**
- [[EHR - ELGA - Technologie-Architektur]]
- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - Architektur - Registry vs Repository]]
- [[EHR - Architektur - ISO 23903 3D]]
- [[EHR - Healthcare Systems - Zentralisierungs-Modelle]]
- [[EHR - EHDS - European Health Data Space]]
- [[EHR - Diagram - ELGA Technologie-Architektur]]

**MSI:**
- [[MSI - ELGA - EIS Stufen]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - ART-DECOR]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]]
- [[MSI - IHE XDS - Architektur]]
- [[MSI - IHE XDS - Dokument-Metadaten]]
- [[MSI - Terminologie - Management in Österreich]]
- [[MSI - Diagram - IHE XDS Akteure]]

**Andere Brücken:**
- [[Cross - HL7 FHIR und CDA in MSI vs EHR]] (Standard-Vergleich, der CDA-Level vs. EIS-Stufe ebenfalls behandelt)

**MOCs:**
- [[EHR - MOC]]
- [[MSI - MOC]]

## Quelle

Cross-Fach-Synthese aus den oben gelisteten EHR- und MSI-Konzept-Notes. Keine externen Ergänzungen außerhalb der Vault-Quellen.

**Fach-Zuordnung der Quellen:**

| Note | Fach |
|---|---|
| EHR - ELGA - Technologie-Architektur | EHR |
| EHR - Architektur - Zentral vs Dezentral / Registry vs Repository | EHR |
| MSI - ELGA - EIS Stufen | MSI |
| MSI - HL7 CDA - Levels / Implementierungsleitfäden / Templates / ART-DECOR | MSI |
| MSI - IHE XDS - Architektur / Dokument-Metadaten | MSI |
| MSI - Terminologie - Management in Österreich | MSI |
