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

# MSI - PF - Terminologien und Klassifikationen

## Kontext

Themenbereich-Sammelkarte für Terminologien und Klassifikationen in MSI. Abgedeckt werden: semantische Treppe, Ordnungssysteme, Code System vs. Value Set, Präkoordination/Postkoordination, Mehrachsigkeit, Mapping, Value Set Binding, Terminologie-Management und ClaML. Tiefere Cimino-Desiderata-Karten → [[MSI - PF - Cimino Desiderata]].

## Verlinkte Konzepte

- [[MSI - Ordnungssystem - Semantische Treppe]]
- [[MSI - Ordnungssystem - Klassifikation]]
- [[MSI - Ordnungssystem - Nomenklatur]]
- [[MSI - Ordnungssystem - Ontologie]]
- [[MSI - Ordnungssystem - Thesaurus]]
- [[MSI - Ordnungssystem - Taxonomie]]
- [[MSI - Ordnungssystem - Konzeptdomäne]]
- [[MSI - Terminologie - Definition]]
- [[MSI - Terminologie - Vokabular und kontrolliertes Vokabular]]
- [[MSI - Terminologie - Code System]]
- [[MSI - Terminologie - Value Set]]
- [[MSI - Terminologie - Anforderungen]]
- [[MSI - Terminologie - Funktionen]]
- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - Mehrachsigkeit]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]
- [[MSI - Terminologie - Multiple Consistent Views]]
- [[MSI - Terminologie - Pflegediagnose vs ärztliche Diagnose]]
- [[MSI - Value Set - Eigenschaften und Wartung]]
- [[MSI - Value Set - Spezifizierung im CDA-Leitfaden]]
- [[MSI - Terminologie - Mapping in CDA]]
- [[MSI - Terminologie - Management in Österreich]]
- [[MSI - ClaML - Classification Markup Language]]
- [[MSI - Begriff - Konzept Bezeichnung Code]]
- [[MSI - Begriff - Synonyme Homonyme Eponyme]]

---

## Karten

### Definition

Was sind die fünf Stufen der semantischen Treppe, und was kennzeichnet jede Stufe?

?

1. **Glossar** – Begriffe mit Definitionen, keine formalen Relationen.
2. **Nomenklatur** – geregelte Benennungssysteme, systematische Namen.
3. **Klassifikation** – planmäßige, vollständige, disjunkte Einordnung in Klassen; typischerweise monohierarchisch.
4. **Thesaurus** – Nomenklatur + Definitionen + Synonyme + Hinweise auf verwandte Terme.
5. **Ontologie** – formale Modellierung mit is-a, part-of, caused-by, treated-with; maschinell interpretierbar und für Reasoning geeignet.
→ Jede Stufe enthält die Leistungen der darunter liegenden – die Treppe ist kumulativ.

---

Wie unterscheiden sich Code System und Value Set in Definition, Identifikation und Änderbarkeit?

?

**Code System:** Terminologie + Regelwerk; enthält Codes + Anzeigenamen + Attribute; eindeutig durch OID identifiziert; bei Sinnänderung eines Codes → **neue OID** (Concept Permanence).

**Value Set:** anwendungsspezifische Sicht auf Codes aus einem oder mehreren Code Systemen; enthält nur Referenzen auf Konzepte; identifiziert durch Name + optional OID/URL; **änderbar** (versionierte Änderung erlaubt).

→ Code System = Wahrheitsquelle; Value Set = anwendungsspezifische Auswahl daraus.

---

Was ist ein kontrolliertes Vokabular, und warum ist die Abwesenheit von Homonymen zentral?

?

Ein **kontrolliertes Vokabular** ist ein Vokabular, in dem jeder Term eindeutig ist: **keine Homonyme** (ein Begriff, eine Bedeutung) und systematische Synonymkontrolle.

Homonyme verhindern maschinelles Matching: „Herzinsuffizienz" kann in verschiedenen Systemen unterschiedliche Konzepte bezeichnen → semantisch falsche Aggregation bei Auswertungen.

Aus dem Vorlesungsmaterial: Vokabular + Regelwerk = **Code System**; im computerverarbeitbaren Kontext spricht man von einer **Terminologie**.

---

Was unterscheidet Präkoordination von Postkoordination in medizinischen Terminologien?

?

**Präkoordination:** komplexe Konzepte sind als eigenständige, atomare Codes vordefiniert. Beispiel (SNOMED CT): ein Code für „laparoscopic emergency appendectomy".

**Postkoordination:** das komplexe Konzept wird aus Einzelcodes erst zur Dokumentationszeit zusammengesetzt.

Vorteil Präkoordination: einfache Abfragen, ein Code reicht.
Vorteil Postkoordination: flexibel, kein Aufblähen des Vokabulars durch jede Kombination.

SNOMED CT unterstützt beide Strategien; APPC verwendet Postkoordination über vier Achsen (Modalität, Lateralität, Prozedur, Anatomie).

---

### Anwendung

Erklären Sie die Mehrachsigkeit am Beispiel APPC. Welche vier Achsen gibt es, und wozu dient das Konzept?

?

**APPC** (Austrian Patient Pathology Code) verwendet vier Achsen:
1. **Modalität** – Art der Untersuchung (z. B. Ultraschall)
2. **Lateralität** – Seite (links, rechts, bilateral)
3. **Prozedur** – durchgeführte Maßnahme
4. **Anatomie** – Körperregion

Mehrachsigkeit ermöglicht die Codierung auch seltener Kombinationen ohne eigenen Code pro Kombination → entspricht der Postkoordination.

Zweck in ELGA: Filterung von Dokumenten nach Gesundheitsdienstleistung im ELGA-Portal.

---

Skizzieren Sie die Drei-Stufen-Mapping-Architektur für Laborbefunde in ELGA am Beispiel Transferrin.

?

```
Lokales System (LIS):     Transfe-SerPlas   4,1 g/l   (1,6–3,5)  H
        │  Umkodierung beim Befundexport
        ▼
ELGA CDA Befund:          Transferrin        LOINC 3034-6   UCUM g/l   +
                          (Langtext)         (Code)         (Einheit)  (Bewertungscode)
        │  Import und Überführung in eigene Darstellung
        ▼
System des Empfängers:    TF                0,41 g/dl  (0,16–0,35)  ↑
```

**Sender und Empfänger pflegen je ein Mapping** zur ELGA-CDA-Repräsentation.

Vorteil gegenüber Direkt-Mapping: statt n×(n-1) Mappings zwischen allen Laborpaaren genügen n Mappings (Hub-Architektur).

---

Welche Bestandteile hat eine CONF-Regel im CDA-Leitfaden für ein Value Set Binding?

?

Bestandteile (aus Folie 11):
1. **Element-Pfad** (z. B. `hl7:administrativeGenderCode`)
2. **Datentyp** (z. B. CE = Coded with Equivalents)
3. **Optionalität/Cardinality** (z. B. `1..1 R` = required)
4. **Verbindlichkeit** (muss / sollte)
5. **Value Set Referenz**: OID + Name (z. B. `1.2.40.0.34.10.4 ELGA_AdministrativeGender`)
6. **Bindungs-Modus**: DYNAMIC (erweiterbar) oder STATIC (eingefroren)
7. **nullFlavor**: zugelassene Codes für fehlende Werte (z. B. UNK = unknown)

Beispiel: „Der Wert von @code muss gewählt werden aus dem Value Set 1.2.40.0.34.10.4 ELGA_AdministrativeGender (DYNAMIC). Zugelassene nullFlavor: UNK."

---

Welche Aufgaben umfasst das Terminologie-Management in Österreich? Nennen Sie mindestens sechs.

?

Aus Folie 17 (Terminologie-Management Österreich):
1. Suche nach geeigneten Terminologien + Abstimmung mit Fachexperten/Arbeitsgruppen
2. Value Set Erstellung (Subsets, Anzeigetexte)
3. Übersetzen und Mappen (lokal → international, DE → EN)
4. Einbringen neuer Codes (Antrag bei LOINC, SNOMED CT)
5. Wartung und Versionierung
6. Verteilung (z. B. termgit.elga.gv.at)
7. Lizenz-Management (SNOMED CT national, LOINC frei nach Registrierung)
8. Zusammenspiel mit Anzeige (Stylesheet) und Validierung (Schematron, Online-Validator)

---

### Diskussion / Vergleich

Vergleichen Sie Ontologie, Klassifikation und Thesaurus in Formalität, Relationstypen und typischem Anwendungsfall.

?

| | Klassifikation | Thesaurus | Ontologie |
|---|---|---|---|
| Relationstypen | is-a (monohierarchisch) | is-a + Synonyme + verwandte Terme | is-a, part-of, caused-by, treated-with, … |
| Formalität | niedrig | mittel | hoch (maschinell interpretierbar) |
| Anwendungsfall | Statistik, Abrechnung | Suchindex, Dokumentation | Reasoning, Clinical Decision Support |
| Beispiel | ICD-10 | MeSH | SNOMED CT |

Ontologien sind mächtiger, aber wartungsaufwändiger. Klassifikationen sind bewährt für administrative Zwecke und einfache Abfragen.

---

Aus welchen Gründen reicht ICD-10 für den Pflegebereich nicht aus? Vergleichen Sie ärztliche Diagnose und Pflegediagnose.

?

Vier Vergleichsachsen (Folie 28):

| | Ärztliche Diagnose | Pflegediagnose |
|---|---|---|
| Gegenstand | Krankheit/Organstörung | Reaktion auf (potenzielle) Gesundheitsstörung |
| Bezugsfeld | Patient als Einzelperson | Patient + Familie + soziales Umfeld |
| Zeitliches Verhalten | stabil bis Heilung | fortlaufend veränderlich |
| Beispiel | Mundbodenkarzinom | Beeinträchtigte Mundschleimhaut, Schmerzen, Körperbildstörung, Schluckstörung |

→ Deshalb eigenständige Pflegeklassifikationen: NANDA-I, POP, ICNP, NIC, NOC, ENP.
Ein einziger ICD-10-Code bildet die pflegerische Komplexität eines Patienten nicht ab.

---

Warum bekommt ein Code System bei Sinnänderung eines Codes eine neue OID? Welches Cimino-Desideratum steckt dahinter?

?

Dahinter steht **Concept Permanence** (Cimino): Ein Code darf seine Bedeutung nie ändern. Ändert sich die Bedeutung, ist es technisch ein neues Konzept – und damit ein anderes Code System, das eine neue OID benötigt.

OIDs sind global eindeutig und unveränderlich. Ohne neue OID würden Systeme, die auf die alte OID verweisen, stillschweigend falsche Semantik verwenden.

Kontrast Value Set: Value Sets referenzieren nur Codes aus Code Systemen. Sie können sich inhaltlich ändern (neue Codes aufnehmen, veraltete ausschließen), ohne die Semantik der Code Systems zu berühren.

---

Wann würden Sie ClaML einsetzen, wann FHIR CodeSystem? Vergleichen Sie Zweck, Format und Einsatzbereich.

?

| | ClaML | FHIR CodeSystem |
|---|---|---|
| Norm | CEN/TS 14463:2003 / EN 14463:2007 | HL7 FHIR R4/R5 |
| Format | XML | JSON oder XML |
| Zweck | XML-Notation für hierarchische Klassifikationen (ICD-10, SNOMED) | FHIR-Resource für Code Systems im FHIR-Ökosystem |
| Einsatzbereich | WHO-Klassifikationen, nationale Terminologieserver (DIMDI, ELGA) | FHIR-Server, SVCM-konforme Terminologieserver |
| Konvertierung | ClaML → FHIR CodeSystem möglich | – |

→ ClaML: klassische XML-Infrastruktur, etabliert bei Bestandssystemen.
FHIR CodeSystem: wenn das System sowieso FHIR-basiert ist und SVCM (IHE) genutzt wird.

---

Wie unterscheiden sich Polyhierarchie und Multiple Consistent Views in Ciminos Modell?

?

**Polyhierarchie** (Cimino Desideratum 2.8): Eigenschaft der Terminologie – ein Konzept kann mehrere Elternkonzepte haben (z. B. Diabetes Mellitus gehört zu Stoffwechselkrankheiten UND endokrinen Störungen).

**Multiple Consistent Views** (Cimino Desideratum 2.9): anwendungsspezifische Sichten auf das Vokabular, z. B. Kollabieren auf grobgranulare Konzepte, Verstecken von Zwischenebenen oder Konvertierung in strikte Hierarchie.

Konsistenz-Anforderung: in jeder Sicht müssen dieselben Kindkonzepte erscheinen. Nicht akzeptabel (Cimino Fig. 1f): dasselbe Konzept erscheint in zwei Ästen mit *unterschiedlichen* Kindern.

→ Polyhierarchie = Vokabular-Eigenschaft; Multiple Consistent Views = Mechanismus, der Polyhierarchie für Anwendungen nutzbar macht.

---

Welche Negativkonsequenzen entstehen, wenn ein Krankenhaus keine einheitlichen Terminologiestandards verwendet?

?

Fünf Negativkonsequenzen (aus den Konzept-Notes, Terminologie - Funktionen):
1. **Fehlende Wiederverwendbarkeit**: klinische Daten können nicht systemübergreifend aggregiert werden.
2. **Keine Sekundärnutzung**: Forschung und Qualitätssicherung scheitern an inkonsistenten Codes.
3. **Missverständnisse durch Homonyme/Synonyme**: „Protein"/„Eiweiß"/„Totalprotein" werden als drei verschiedene Parameter behandelt.
4. **Redundante, fehlerhafte Daten**: Doubletten durch fehlende Identitätskontrolle.
5. **Keine semantische Interoperabilität**: Systeme tauschen Daten aus, verstehen sie aber nicht gleich.

Klassisches Beispiel: fünf Labore mit fünf Codes, drei Einheiten für denselben Laborparameter (Folie 18, Quelle: Dr. Hübl, HL7 Austria Jahrestagung 2011).

---

## Mögliche Anschlussfragen des Prüfers

- Welche FHIR-Operationen entsprechen welchen Terminologie-Aktionen? (→ FHIR Terminologie PF)
- Wie wird in SNOMED CT Postkoordination technisch realisiert?
- Was ist der Unterschied zwischen DYNAMIC und STATIC Binding in CDA? Welche Risiken hat DYNAMIC?
- Welche Cimino-Desiderata sprechen direkt gegen Homonyme? (Non-ambiguity, Non-vagueness)
- Wie unterscheiden sich Mapping und Cross-Mapping?
- Warum ist Lizenz-Management eine eigenständige Aufgabe? (SNOMED CT national, LOINC open)
- Welche Norm liegt ClaML zugrunde? (CEN/TS 14463:2003 / EN 14463:2007)
- Wie verwendet ELGA APPC? (Filterachse für Gesundheitsdienstleistung in XDS-Metadaten)

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
