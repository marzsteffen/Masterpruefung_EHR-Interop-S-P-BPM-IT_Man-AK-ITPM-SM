---
fach: msi
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - fach/allgemein/msi
  - typ/pruefungsfrage
  - status/offen
  - flashcards
---

# MSI - PF - HL7 CDA Detail

## Kontext

Tiefenkarte zu HL7 CDA R2 (ISO/HL7 27932:2009). Abgedeckt: Definition, sechs Eigenschaften, drei Levels, Template-Typen, Datentypen, Header-Pflichtfelder, Section-Aufbau, Entry-Hierarchien (Labor, Medikation, Problem), nullFlavor, Translation-Patterns, Schema/Schematron-Validierung, ART-DECOR-Toolchain. Ergänzend: [[MSI - PF - IHE-Profile]] (XDS, XDW), [[MSI - PF - HL7 FHIR Detail]] (Vergleich CDA vs. FHIR).

## Verlinkte Konzepte

- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Eigenschaften]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Header]]
- [[MSI - HL7 CDA - Body und Sections]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - HL7 CDA - Templates]]
- [[MSI - HL7 CDA - Kardinalität und Konformität]]
- [[MSI - HL7 CDA - Stylesheet und Validierung]]
- [[MSI - HL7 CDA - Implementierungsleitfäden]]
- [[MSI - HL7 CDA - Datentypen]]
- [[MSI - HL7 CDA - Codierte Werte]]
- [[MSI - HL7 CDA - nullFlavor]]
- [[MSI - HL7 CDA - R-MIM]]
- [[MSI - HL7 CDA - Terminology Binding]]
- [[MSI - HL7 CDA - ART-DECOR]]
- [[MSI - HL7 CDA - Translation]]
- [[MSI - HL7 CDA - Laborparameter Entry]]
- [[MSI - HL7 CDA - Medikation Entry]]
- [[MSI - HL7 CDA - Problem-Bedenken Entry]]

---

## Karten

### Definition

Was ist HL7 CDA R2, und auf welchem Standard basiert es? Nennen Sie drei Kerneigenschaften des Formats.

?

**CDA** (*Clinical Document Architecture*, Release 2) ist ein XML-basierter Standard für den Austausch klinischer Dokumente.

- **Norm**: ISO/HL7 27932:2009 (internationaler Standard)
- **Familie**: HL7 Version 3 (V3) — basiert auf dem Reference Information Model (RIM)
- **Format**: XML; jedes CDA-Dokument ist ein wohlgeformtes XML-Dokument
- **Zweck**: strukturierter, semantisch reicher Austausch klinischer Dokumente (Befunde, Entlassbriefe, Laborbefunde) zwischen Systemen und Einrichtungen
- **Österreich**: Basis aller ELGA-Dokumente (Entlassungsbrief, Laborbefund, Befund bildgebender Diagnostik, e-Medikation, …)

---

Welche sechs Eigenschaften definieren ein CDA-Dokument laut Standard? Erläutern Sie jede kurz.

?

1. **Persistenz** – Das Dokument existiert über die Zeit der Erstellung hinaus in unveränderter Form.
2. **Verwaltung** – Eine verantwortliche Organisation (Custodian) ist zuständig für Verwaltung und Aufbewahrung.
3. **Kontext** – Anamnese und klinischer Kontext sind im Dokument selbst enthalten (Header-Felder).
4. **Authentisierung** – Das Dokument ist von einem Akteur authentifiziert (Rechtlicher Unterzeichner, legalAuthenticator).
5. **Ganzheit** – Attestierung bezieht sich auf das gesamte Dokument, nicht auf einzelne Teile.
6. **Lesbarkeit** – Das Dokument ist für menschliche Leser lesbar (Narrative Block, Stylesheet).

---

Beschreiben Sie die drei CDA-Levels. Was unterscheidet Level 2 von Level 3 strukturell?

?

| Level | Bezeichnung | Body-Inhalt | Maschinenlesbar? |
|---|---|---|---|
| **Level 1** | NonXMLBody | Beliebiges eingebettetes Dokument (PDF, TIFF, …) als Base64 | Nein – Inhalt als Blob |
| **Level 2** | structuredBody + Sections | Sections mit LOINC-code, title und Narrative Text (`<text>`) | Eingeschränkt – Struktur ja, Semantik nein |
| **Level 3** | structuredBody + Entries | Sections + maschinenlesbare `<entry>`-Elemente (Observations, Acts, …) | Ja – vollständig verarbeitbar |

**Unterschied L2 → L3**: Level 3 ergänzt jede Section um `<entry>`-Elemente, die den Narrative Text in codierter, maschinenlesbarer Form wiederholen. Beide Repräsentationen (Narrative + Entry) müssen inhaltlich konsistent sein.

---

Welche vier Template-Typen gibt es in CDA? Was regelt jeder Typ?

?

1. **Document Level Template** – regelt die Gesamtstruktur des Dokuments (erlaubte Sections, Pflicht-Header-Felder, Dokumenttyp-Code).
2. **Header Level Template** – regelt einzelne Header-Elemente (z. B. Format des `<author>`-Blocks, Custodian-Angaben).
3. **Section Level Template** – regelt eine Section (code, title, Textformat, erlaubte Entries).
4. **Entry Level Template** – regelt ein Entry-Element (Observation, Act, Organizer, SubstanceAdministration, …).

**Wichtig**: Ein Dokument kann mehrere Template-IDs tragen (ELGA EIS Basic + EIS Full + spezifisches Leitfaden-Template). Jedes Template hat eine weltweit eindeutige OID als `templateId/@root`.

---

Welche CDA-Datentypen werden für codierte Werte, Messwerte und Zeitangaben eingesetzt? Nennen Sie je ein Beispiel.

?

| Kategorie | Datentyp | Verwendung | Beispiel |
|---|---|---|---|
| Codierter Wert | CE / CD | `<code>`, `<value>` mit code+codeSystem | LOINC-Code für Lab-Parameter |
| Unkodierter Text | ST | Freitextfelder | Zusatzinformation |
| Messwert | PQ | `<value xsi:type="PQ">` | `3.5 g/dL` (UCUM) |
| Intervall-Messwert | IVL_PQ | Referenzbereiche | `<low value="2.2"/><high value="3.5"/>` |
| Zeitpunkt | TS.DATE | Geburtsdatum, Ausstellungsdatum | `20240101` |
| Zeitintervall | IVL_TS | Behandlungsdauer, Wirkungsintervall | `<low value="…"/><high value="…"/>` |
| Periodisches Intervall | PIVL_TS | Einnahmefrequenz Medikation | 1× täglich |
| Identifikator | II | `<id>`, `<templateId>` | `root="2.16.840.1.113883.6.1"` |

---

### Anwendung

Welche Pflichtfelder enthält der CDA-Header für ELGA EIS Basic? Ordnen Sie sie ihrer semantischen Rolle zu.

?

| Header-Element | Semantische Rolle |
|---|---|
| `<title>` | Dokumenttitel (lesbarer Name) |
| `<id>` | Dokumenten-Instanz-ID (II, eindeutig) |
| `<code>` | Dokumenttyp (LOINC-Code) |
| `<effectiveTime>` | Erstellungsdatum (TS.DATE) |
| `<recordTarget / patientRole>` | Patient (inkl. bPK-GH, GDA-spezifische ID) |
| `<author>` | Verfasser (Person + Zeitpunkt der Erfassung) |
| `<legalAuthenticator>` | Rechtlicher Unterzeichner (Authentisierung) |
| `<custodian>` | Verwaltende Organisation (Custodian) |
| `<serviceEvent>` | Klinisches Ereignis (Leistungsdatum) |

Zusätzlich in ELGA: GDA-ID (Gesundheitsdiensteanbieter-Index), ELGA-Zugehörigkeit, Versionsnummer bei Ersetzung.

---

Beschreiben Sie den Aufbau einer CDA-Section (Level 2/3) mit den vier Pflichtbestandteilen. Was ist im `<text>`-Block erlaubt?

?

```xml
<section>
  <templateId root="1.2.40.0.34.6.0.11.2.1"/>    <!-- Template-Identifikation -->
  <code code="11502-2"                             <!-- LOINC: Section-Typ -->
        codeSystem="2.16.840.1.113883.6.1"
        displayName="Laboratory report"/>
  <title>Laborbefund</title>                       <!-- Menschenlesbarer Titel -->
  <text>                                           <!-- Narrative Block (Pflicht L2+) -->
    <table>...</table>                             <!-- Strukturiertes HTML-Subset -->
  </text>
  <entry>                                          <!-- Nur Level 3: maschinenlesbar -->
    <observation>...</observation>
  </entry>
</section>
```

**Im `<text>`-Block erlaubtes Subset**: `<paragraph>`, `<list>`, `<table>`, `<caption>`, `<content>` (mit ID-Referenz auf Entry), `<renderMultiMedia>` für eingebettete Bilder. Kein volles HTML — nur CDA-definiertes Subset.

---

Skizzieren Sie die Entry-Hierarchie eines ELGA-Laborbefunds. Welche Elemente kodieren Wert, Einheit und Normalbereich?

?

```
<act classCode="ACT"> ← Bereich (z.B. Hämatologie)
  <entryRelationship>
    <organizer classCode="BATTERY"> ← Gruppe (z.B. Blutbild)
      <entryRelationship>
        <observation classCode="OBS" moodCode="EVN">
          <code code="26464-8"
                codeSystem="2.16.840.1.113883.6.1"/>   ← LOINC (Was?)
          <value xsi:type="PQ"
                 value="5.5" unit="10*9/L"/>             ← Ergebnis + UCUM-Einheit
          <interpretationCode code="N"
                              codeSystem="…ObservationInterpretation"/>  ← H/L/N
          <referenceRange>
            <observationRange>
              <value xsi:type="IVL_PQ">
                <low value="4.0" unit="10*9/L"/>
                <high value="10.0" unit="10*9/L"/>     ← Referenzbereich
              </value>
            </observationRange>
          </referenceRange>
        </observation>
```

**Wert**: `<value xsi:type="PQ">` — physikalische Größe (Zahl + UCUM-Einheit)
**Normalbereich**: `<referenceRange>` mit `IVL_PQ` (Intervall)
**Bewertung**: `<interpretationCode>` (H/L/N/A)

---

Welche fünf nullFlavor-Ausprägungen kennt CDA? Wann ist nullFlavor konform, wann problematisch?

?

| Kürzel | Bedeutung | Typischer Einsatz |
|---|---|---|
| **NI** | No Information | Keine Information vorhanden (generisch) |
| **UNK** | Unknown | Information sollte bekannt sein, ist es aber nicht |
| **MSK** | Masked | Information existiert, ist aber aus Datenschutzgründen verborgen |
| **NA** | Not Applicable | Frage trifft auf diesen Patienten nicht zu |
| **OTH** | Other | Wert außerhalb des Value Sets — muss mit `<translation>` ergänzt werden |

**Konformitätsregel**: Wenn ein Element nullFlavor trägt, dürfen **keine anderen Attribute oder Kindelemente** (außer `<translation>` bei OTH) gesetzt sein. Validierung schlägt fehl, wenn z. B. `code` und `nullFlavor` gleichzeitig gesetzt sind.

**Problematisch**: Massiver Einsatz von UNK degradiert die Qualität des Dokuments und verhindert Sekundärnutzung — sollte nur gesetzt werden, wenn wirklich keine Information verfügbar ist.

---

Erklären Sie Translation-Pattern A und B in CDA. Wann wird welches Muster verwendet?

?

**Hintergrund**: Wenn der lokale Code nicht im geforderten Value Set liegt, gibt es zwei konforme Muster:

**Pattern A — nullFlavor OTH + translation:**
```xml
<code nullFlavor="OTH">
  <translation code="LOKAL-123"
               codeSystem="1.2.3.4.5"
               displayName="Lokale Bezeichnung"/>
</code>
```
→ Verwendung: wenn **kein** passender Code im Ziel-Value-Set existiert.

**Pattern B — Hauptcode + translation:**
```xml
<code code="LOINC-CODE"
      codeSystem="2.16.840.1.113883.6.1">
  <translation code="LOKAL-123"
               codeSystem="1.2.3.4.5"
               displayName="Lokale Bezeichnung"/>
</code>
```
→ Verwendung: wenn ein **passender** Ziel-Code vorhanden ist, aber das sendende System zusätzlich seinen lokalen Code übermitteln möchte (Traceability).

**Faustregel**: Pattern A = kein passender Code; Pattern B = Hauptcode bekannt, lokaler Code als Zusatz.

---

### Diskussion / Vergleich

Was prüft das CDA-Schema (XSD), was prüft Schematron — und was prüft keines von beiden?

?

| Prüfebene | CDA-Schema (XSD) | Schematron |
|---|---|---|
| **Prüft** | Wohlgeformtheit, Element-Reihenfolge, Datentypen, Existenz von Pflichtattributen (z. B. `@root` bei `<id>`) | Geschäftsregeln: erlaubte Codes aus Value Sets, nullFlavor-Logik, Kardinalität im Kontext von Template-IDs, konditionale Pflichtfelder |
| **Sprache** | W3C XML Schema (XSD) | ISO Schematron (XPath-basierte Regeln) |
| **Tooling** | XML-Parser-Validierung | XSLT-Transformation aus Schematron-Regeln |
| **Was beide NICHT prüfen** | Inhaltliche Plausibilität (Alter passt zum Geburtsdatum), medizinische Korrektheit, Vollständigkeit der Narrative | – |

→ Erst Schema-valide Dokumente werden mit Schematron geprüft. Schematron ist mächtiger, aber nicht standardisiert auf Basis des CDA-Schemas allein — der ELGA-Online-Validator kombiniert beide Stufen.

---

Was ist der Unterschied zwischen DYNAMIC und STATIC Binding in CDA? Welches birgt welche Risiken?

?

| | DYNAMIC Binding | STATIC Binding |
|---|---|---|
| **Bedeutung** | Das Dokument muss gegen die **aktuelle Version** des Value Sets validiert werden | Das Dokument muss gegen eine **namentlich fixierte Version** des Value Sets validiert werden |
| **Vorteil** | Value Set wächst automatisch mit — neue Codes ohne Breaking Change nutzbar | Vorhersagbare Validierung auch für ältere Dokumente |
| **Risiko** | Ältere Dokumente können ungültig werden, wenn das Value Set schrumpft oder Codes entfernt werden | Leitfaden muss explizit aktualisiert werden, um neue Codes zu erlauben — Wartungsaufwand |
| **ELGA-Praxis** | Meist DYNAMIC für erweiterbare Sets (z. B. `ELGA_Laborparameter`) | STATIC für Sets mit stabiler, kleiner Codeliste |

Angabe in CONF-Regel: `DYNAMIC` bzw. `STATIC` + Value-Set-OID + ggf. Versionskennung.

---

Welche drei Rollen — Verfasser, Rechtlicher Unterzeichner und Custodian — hat ein CDA-Dokument? Wo liegen die Unterschiede?

?

| Rolle | CDA-Element | Was sie aussagt |
|---|---|---|
| **Verfasser** (Author) | `<author>` | Wer hat das Dokument inhaltlich erstellt? (Arzt, System) — Zeitpunkt der Erfassung |
| **Rechtlicher Unterzeichner** (Legal Authenticator) | `<legalAuthenticator>` | Wer hat das Dokument rechtlich unterzeichnet/freigegeben? (muss natürliche Person sein) |
| **Custodian** | `<custodian>` | Welche Organisation ist für Verwahrung und Verwaltung verantwortlich? (Institution, nicht Person) |

**Unterschiede:**
- Verfasser kann ein Softwaresystem sein (z. B. LIS, KIS) — Rechtlicher Unterzeichner muss Mensch sein.
- Ein Dokument hat genau einen Custodian, aber mehrere Author-Einträge sind möglich (z. B. mehrere Verfasser).
- Der Custodian ist für ELGA-Pflege zuständig und muss im GDA-Index registriert sein.

---

Warum enthält CDA Level 3 sowohl einen Narrative Block als auch maschinenlesbare Entries? Ist das nicht Redundanz?

?

**Bewusste Design-Entscheidung** — beide Schichten haben unterschiedliche Verantwortlichkeiten:

**Narrative Block (`<text>`):**
- Quelle der Wahrheit für den **menschlichen Leser** (Arzt, Patient über Stylesheet)
- Muss immer vollständig, lesbar und renderbar sein
- Enthält Kontext, Nuancen, Freitext — was Maschinen nicht vollständig strukturieren können

**Entries:**
- Quelle der Wahrheit für **maschinelle Verarbeitung** (Decision Support, Aggregation, Suche)
- Erlaubt strukturierte Abfragen (z. B. alle Laborwerte eines Patienten)
- Kann weniger Information enthalten als der Narrative — darf ihn aber inhaltlich **nicht widersprechen**

**Ciminos Reasoning dahinter**: Formal Definitions (Entries) ermöglichen Reasoning — aber für den klinischen Einsatz braucht man immer die menschenlesbare Sicht als rechtlich bindende Grundlage.

**Konsequenz**: Wenn Narrative und Entry divergieren → Narrative ist rechtlich maßgeblich; Entry-Fehler führen zu Validierungswarnung.

---

Erklären Sie die Beziehung R-MIM → CDA → Implementierungsleitfaden → Template. Was wird auf welcher Ebene festgelegt?

?

```
RIM (Reference Information Model)
  └─ HL7 global; allgemein; enthält alle möglichen Klassen und Relationen

      │  Refinement
      ▼
R-MIM (Refined Message Information Model)
  └─ CDA-spezifisches Teilmodell des RIM
  └─ Legt ClinicalDocument als Wurzel fest
  └─ Definiert erlaubte Klassen (Act, Observation, Organizer, …) und Relationen

      │  XML-Serialisierung
      ▼
CDA R2 Standard (ISO/HL7 27932:2009)
  └─ Generisches Schema (XSD) für alle CDA-Dokumente weltweit
  └─ Alle Pflichtattribute laut Standard

      │  Einschränkung durch Templates + Schematron
      ▼
ELGA Implementierungsleitfaden
  └─ Welche Sections verpflichtend/optional (M/R2/O)
  └─ Value-Set-Bindings (DYNAMIC/STATIC)
  └─ ELGA-spezifische Template-IDs

      │  Granularste Ebene
      ▼
Template (Entry Level)
  └─ Exakter Aufbau eines einzelnen Entry-Elements
  └─ Kardinalität, erlaubte Codes, Datentypen
```

---

Warum ist CDA Level 1 (NonXMLBody) auch in modernen ELGA-Implementierungen noch sinnvoll?

?

**Argumente für Level 1:**

1. **Bestehende Dokumente**: Viele klinische Dokumente liegen als PDF oder gescannte Bilder vor und können nicht wirtschaftlich in Level 3 konvertiert werden.
2. **Rechtsverbindlichkeit**: Ein signiertes PDF (qualifizierte elektronische Signatur) kann eingebettet werden — die Signatur bleibt über den CDA-Wrapper hinaus gültig.
3. **Nicht strukturierbare Inhalte**: Pathologie-Freitext, radiologische Befundbeschreibungen — maschinenlesbare Codierung ist oft nicht möglich oder wirtschaftlich nicht vertretbar.
4. **Interoperabilität trotzdem**: Der CDA-Wrapper liefert Header-Metadaten (Patient, Verfasser, Datum, Dokumenttyp) → ermöglicht Suche und Filterung im ELGA-Portal, ohne den Inhalt maschinenlesbar zu machen.

**Einschränkung**: Keine semantische Interoperabilität des Inhalts. Für Clinical Decision Support und Sekundärnutzung ungeeignet — deshalb Entwicklung in Richtung Level 3.

---

Skizzieren Sie die ART-DECOR-Toolchain: von der Dataset-Definition bis zum validierten CDA-Dokument.

?

```
ART-DECOR (Webapplikation)
  │
  ├─ Dataset-Tab
  │    └─ Klinische Konzepte (z. B. „Diagnose", „Laborparameter")
  │    └─ Mapping auf CDA-Elemente und Terminologien
  │
  ├─ Templates-Tab
  │    └─ Document / Section / Entry Level Templates
  │    └─ Template Associations (Section X enthält Entry Y)
  │    └─ Kardinalitäten, Datentypen, Konfidenz-Level (M/R2/O)
  │
  ├─ Terminology-Tab
  │    └─ Terminology Associations (Value-Set-Bindings, DYNAMIC/STATIC)
  │    └─ Verbindung zu externen Terminologieservern (ELGA Termgit)
  │
  ├─ Export: Schematron-Regeln (.sch)
  │    └─ Maschinenlesbare Geschäftsregeln aus Templates generiert
  │
  └─ Export: Implementierungsleitfaden (HTML/PDF)
       └─ Lesbares Spezifikationsdokument

Validierungspipeline für CDA-Instanz:
  1. XML-Wohlgeformtheit prüfen
  2. CDA-Schema (XSD) validieren
  3. Schematron-Regeln (aus ART-DECOR) ausführen
  4. ELGA Online-Validator = Stufen 1–3 kombiniert
```

---

## Mögliche Anschlussfragen des Prüfers

- Welche LOINC-Codes identifizieren Dokumentklassen? (`11490-0` Discharge Summary, `11502-2` Lab Report)
- Warum hat CDA `moodCode="EVN"` bei Observations? (Ereignis, nicht Absicht — `INT` bei Medikation)
- Was ist der Unterschied zwischen `<author>` und `<informant>` im CDA-Header?
- Wie wird die Versionierung von CDA-Dokumenten in ELGA gehandhabt? (relatedDocument + typeCode RPLC)
- Welcher ELGA-Leitfaden regelt den e-Medikations-Eintrag? (Template 1.2.40.0.34.11.8.1.3.1)
- Was versteht man unter „Ganzheit" als CDA-Eigenschaft? Warum darf die Attestierung nicht auf einzelne Sections beschränkt sein?
- Wie unterscheidet sich IVL_TS von PIVL_TS? (`IVL_TS` = Zeitintervall einmalig; `PIVL_TS` = periodisches Intervall, z. B. täglich)
- Welcher Qualifier kodiert die ELGA-Diagnosesicherheit beim Problem Entry? (Qualifier am ICD-10-Code, Value Set ELGA_Diagnosesicherheit)

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
