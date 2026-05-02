---
fach: msi
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/msi
---

# MSI - PF - HL7-Familie

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz deckt die HL7-Familie auf Überblicks- und Paradigmenebene ab: Datenaustausch-Formen (Nachricht/Dokument/Ressource), die vier Austausch-Paradigmen, HL7 RIM als semantisches Fundament von HL7 V3 und CDA, CDA-Definition und Kerneigenschaften, FHIR-Definition und Versionierung, ELGA-EIS-Stufen, openEHR sowie International Patient Summary. Die CDA- und FHIR-Tiefe (Header, Body, Levels, Resources, REST, Profile) liegt in den Detail-PFs `MSI - PF - HL7 CDA Detail` und `MSI - PF - HL7 FHIR Detail`.

## Verlinkte Konzepte

- [[MSI - Datenaustausch - Formen]]
- [[MSI - HL7 FHIR - Paradigmen]]
- [[MSI - HL7 RIM - Reference Information Model]]
- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Eigenschaften]]
- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - Versionen]]
- [[MSI - ELGA - EIS Stufen]]
- [[MSI - HL7 - International Patient Summary]]
- [[MSI - openEHR - Archetypes]]
- [[MSI - Standards - Definition]]
- [[MSI - Standards - Nutzen]]

---

## Karten

### Definition

Welche drei strukturierten Formen des Datenaustauschs unterscheidet die Vorlesung, und welcher HL7-Standard repräsentiert jeweils welche Form?

?

Laut Folie 19 (MSI VL Einführung in Standards und Interoperabilität):

| Form | HL7-Vertreter | Charakteristik |
|---|---|---|
| **Nachrichten** | HL7 v2 (auch EDIFACT) | Ereignisgetrieben, kurzlebig, Workflow-gekoppelt |
| **Dokumente** | HL7 CDA (HL7 V3) | Persistent, narrativ + strukturiert, human-readable |
| **Ressourcen** | HL7 FHIR | Granular, REST-orientiert, atomare Einheiten |

Ergänzend (Folie 19, ausgegraut): Mündliche Kommunikation, Papierakten und Fax existieren als historische/parallele Modi weiterhin.

---

Welche vier Paradigmen des Datenaustauschs im Gesundheitswesen unterscheidet die Vorlesung (HL7 FHIR Starter)?

?

Laut MSI VL HL7 FHIR Starter (Anna Lin):

| Paradigma | Prinzip | Beispiele |
|---|---|---|
| **Nachrichtenbasiert** | Events werden übertragen (Aufnahme, Entlassung, Laborbefund) | HL7 v2 |
| **Dokumentenbasiert** | Arztbrief, Befund als abgeschlossene Informationseinheit | HL7 V3, HL7 CDA |
| **Anwendungsspezifisch** | Auf bestimmte klinische Domänen ausgerichtet | DICOM (Radiologie), CCD, Patient Summary |
| **Ressourcenbasiert** | Atomare Ressourcen (Patient, Medikation, Vitaldaten) werden einzeln verwaltet und kombiniert | HL7 FHIR |

Vorteile Ressourcenbasiert: Granulare Abfragen möglich, Ressourcen unabhängig änderbar, leichtgewichtige Übertragung. Nachteil: keine native Gesamtübersicht (nur via FHIR Documents/Bundles lösbar).

---

Was ist das HL7 RIM, welche vier Backbone-Klassen und zwei Beziehungsklassen kennt es, und in welchem Verhältnis steht es zu CDA?

?

Laut Folie 6–7 (MSI VL HL7 CDA und e-Befunde):

**HL7 RIM (Reference Information Model)**: standardisiertes Informationsmodell des HL7 V3. ANSI- und ISO-Standard (ISO/HL7 21731:2006). Liefert das semantische Fundament aller V3-Spezifikationen einschließlich CDA.

**Vier Backbone-Klassen:**
- **Entity** – „etwas, das existiert" (Person, Organisation, Material) → Attribute: classCode, id, code, statusCode
- **Role** – „in welcher Rolle wird die Entity wahrgenommen" (Patient, Practitioner) → Attribute: classCode, code, effectiveTime, id
- **Participation** – „wie nimmt eine Role an einem Act teil" (Subject, Performer, Author) → Attribute: typeCode, time, statusCode
- **Act** – „etwas, das geschieht oder geschehen soll" (Observation, Procedure, Encounter) → Attribute: classCode, moodCode, code, effectiveTime, id

**Zwei Beziehungsklassen:**
- **Role Link** – verknüpft Roles untereinander
- **Act Relationship** – verknüpft Acts untereinander

**Verhältnis zu CDA**: CDA ist ein Teil von HL7 V3 und baut auf dem RIM auf. Das CDA R-MIM (Restricted Message Information Model) ist eine Spezialisierung des RIM für medizinische Dokumente.

---

Definieren Sie HL7 CDA: ISO-Standard, HL7-Familie, Format und sechs Kerneigenschaften.

?

**Definition** laut Folie 3 (MSI VL HL7 CDA und e-Befunde):
- XML-Format für medizinische Befunde (ISO-Standard: **ISO/HL7 27932:2009**)
- Teil von **HL7 V3** (basiert auf RIM: ISO/HL7 21731:2006)
- Für EDV-Weiterverarbeitung optimiert
- Kann maschinenlesbare Informationen (Diagnosen, Laborwerte) tragen
- Anhänge und Bilder können eingebettet werden
- Mit Stylesheet darstellbar; Metadaten für Gesundheitswesen optimiert

**Sechs Eigenschaften** laut Folie 11:

| Eigenschaft | Englisch | Kernaussage |
|---|---|---|
| Persistenz | persistence | Dauerhafte Existenz, unveränderter Zustand |
| Verwaltung | stewardship | Verantwortlicher Custodian |
| Kontext | context | Standard-Kontext für die Inhalte |
| Authentisierung | potential for authentication | Signierung, Vidierung, Validierung |
| Ganzheit | wholeness | Authentisierung bezieht sich auf das gesamte Dokument |
| Lesbarkeit | human readability | Ohne mitgeliefertes Stylesheet darstellbar |

---

### Anwendung

Identifizieren Sie in folgendem CDA-Snippet Entity, Role und Participation laut HL7 RIM:

```xml
<legalAuthenticator>
  <signatureCode code="S"/>
  <assignedEntity>
    <assignedPerson><name>Dr. Cardiologist</name></assignedPerson>
    <representedOrganization><name>General University Hospital Graz</name></representedOrganization>
  </assignedEntity>
</legalAuthenticator>
```

?

Laut Folie 10 (MSI VL HL7 CDA und e-Befunde):

- `<legalAuthenticator>` → **Participation** – beschreibt, wie eine Role an einem Act teilnimmt (hier: als rechtlich Authentisierender)
- `<assignedEntity>` → **Role** – die Rolle, in der die Person wahrgenommen wird (zugewiesene rechtliche Verantwortung)
- `<assignedPerson>` → **Entity** – Dr. Cardiologist als reale, existierende Person
- `<representedOrganization>` → **Entity** – das Krankenhaus als reale, existierende Organisation

Der zugehörige **Act** ist das CDA-Dokument selbst (z. B. Observation im Body). `<signatureCode code="S"/>` markiert die Signierung (adressiert die Eigenschaft **Authentisierung** + **Ganzheit**).

---

Was sind die ELGA-EIS-Stufen, worin unterscheiden sie sich von CDA-Levels, und welche Stufe ist für die Aufnahme in ELGA minimal erforderlich?

?

Laut Folie 16 (MSI VL HL7 CDA und e-Befunde), Titel: „ELGA-Interoperabilitätsstufen != CDA-Levels":

| EIS-Stufe | Anforderung | Maschinenlesbarkeit |
|---|---|---|
| **EIS BASIC / STRUCTURED** | Einheitlicher CDA-Header; Aufnahme in Dokumentregister; Anzeige für Berechtigte; eingebettetes PDF möglich | minimal |
| **EIS ENHANCED** | Einheitliche Strukturierung/Gliederung; barrierefreie Darstellung; Mindest-Level-3-Codierung laut ELGA-Leitfaden | teilweise |
| **EIS FULL SUPPORT** | Maschinenlesbare Inhalte; automatische Übernahme in medizinisches IS möglich; volle Level-3-Codierung laut ELGA-Leitfaden | vollständig |

**Unterschied zu CDA-Levels**: EIS-Stufen drücken zusätzlich aus, *wie streng* der ELGA-Implementierungsleitfaden eingehalten wird (Header-Konformität, Template-Konformität). CDA-Level 1/2/3 beschreiben nur den Body-Aufbau (Fließtext / Sections / Entries) – keine Aussage über Header-Standards oder nationale Template-Pflicht.

**Minimal für ELGA-Aufnahme**: EIS BASIC.

---

Was ist die International Patient Summary (IPS)? Wer trägt sie, wofür dient sie, und welches konkrete Beispiel nennt das Lehne-Paper?

?

Laut Lehne et al. (2019), Sektionen „Medical communication" und „International cooperation":

- **Was**: Spezifikation für Patient-Summary-Daten – relevante, akkurate, aktuelle medizinische Informationen über Systemgrenzen hinweg
- **Träger**: gemeinsam entwickelt von **HL7** und **CEN** (European Committee for Standardization)
- **Zweck**: Klinikern Zugang zu Patienteninformationen geben; adressiert Problem, dass EHRs „disconnected, proprietary solutions buried in systems that do not talk to each other" sind

**Praktisches Beispiel (Paper)**: 2019 erster grenzüberschreitender Austausch in der EU – Electronic Prescription und Digital Patient Summary zwischen EU-Mitgliedstaaten.

**Hürden trotz IPS** (laut Paper): Organisatorische Ebene bleibt Barriere – Infrastruktur, rechtliche Grundlagen, Anreize.

**Grenze der Note**: Welche konkreten FHIR-Resources oder Sektionen IPS umfasst, wird im Paper nicht ausgeführt.

---

### Diskussion

Vergleichen Sie HL7 CDA und HL7 FHIR auf der Paradigmenebene: Stärken, Schwächen, Koexistenz oder Ablösung?

?

Laut MSI VL HL7 CDA und e-Befunde sowie MSI VL HL7 FHIR Starter (Anna Lin):

| Kriterium | HL7 CDA | HL7 FHIR |
|---|---|---|
| **Paradigma** | Dokumentenbasiert | Ressourcenbasiert (+ Nachrichten/Dokumente möglich) |
| **HL7-Familie** | HL7 V3, RIM-basiert (ISO/HL7 27932:2009) | Eigenständig, nicht RIM-basiert |
| **Format** | XML | JSON, XML (moderner Web-Technologie-Stack) |
| **Stärken** | Persistenz, Ganzheit, Authentisierung; bewährt für regulierte Dokumente (ELGA) | Entwicklerfreundlich, granular, API-tauglich, Mobile-fähig, 80 % UseCases out-of-the-box |
| **Schwächen** | Schwergewichtig; ungeeignet für Mobile/APIs (laut FHIR-Vortrag) | Keine native Gesamtübersicht ohne Bundle; Stabilitätsschwäche durch häufige Versionen |

**Koexistenz vs. Ablösung** (laut FHIR-Vortrag): FHIR ist kein Ersatz für alle anderen Standards. Für bestehende Dokumenten-Workflows (CDA/ELGA) kann ein **FHIR Facade** sinnvoll sein. Koexistenz ist die praxisrelevante Antwort.

---

Erklären Sie das Konzept „normative Ressourcen" in FHIR. Ab welcher Version wurden sie eingeführt, was bedeuten sie, und wie adressieren sie den Stabilitäts-Trade-off?

?

Laut MSI VL HL7 FHIR Starter (Anna Lin):

**Versionshistorie** (Kurzfassung):
DSTU1 (0.0) → DSTU2 (1.0) → STU3 (3.0) → **R4 (4.0.1)** → **R5 (5.0, aktuell)**. Zyklus ca. ~18 Monate.

**Normative Ressourcen ab R4**:
- Vor R4: alle Ressourcen waren Standard for Trial Use (STU) → Änderungen jederzeit möglich
- Ab R4: normative Ressourcen (z. B. Patient, Observation) ändern sich **nur bei zwingend nötigem Grund** und sind **abwärtskompatibel**
- Nicht alle Ressourcen sind normativ – einige bleiben STU oder experimentell
- Reifegrad individuell: **FMM (FHIR Maturity Model)**, in Dokumentation durch Farben/Nummern markiert

**Versionsempfehlung**: „Die neueste! Seit R4 gibt es normative Ressourcen, diese ändern sich nur noch selten."

**Trade-off** (laut FHIR-Vortrag): Ständige Weiterentwicklung ist Vorteil (up-to-date) und Nachteil (Implementierungsaufwand bei Versionssprüngen). Normative Ressourcen adressieren dies: Kern stabil, experimentelle Bereiche weiterhin beweglich.

---

Was bedeutet die 80/20-Regel von FHIR in der Praxis, und warum gilt „FHIR Server ≠ Interoperabilität"?

?

Laut MSI VL HL7 FHIR Starter (Anna Lin):

**80/20-Regel**: FHIR deckt 80 % der häufigsten Use Cases direkt out-of-the-box ab. Die verbleibenden 20 % werden abgedeckt durch:
- **Profilierung** – Einschränkung bestehender Ressourcen auf spezifische Kontexte
- **Extensions** – Erweiterung um nicht im Standard vorhandene Felder
- **Eigene Ressourcen / Implementation Guides** – für sehr spezifische Szenarien

**FHIR Server ≠ Interoperabilität** (laut FHIR-Vortrag): Zwei R4-konforme FHIR-Server können trotzdem nicht interoperieren, wenn sie unterschiedliche Profile und Extensions verwenden. Ohne gemeinsame Profilierung und Implementation Guides bleibt der Standard unausgeschöpft. Interoperabilität entsteht erst durch Einigung auf denselben IG (z. B. ELGA FHIR IG, IPS IG).

---

### Vergleich

Was sind openEHR-Archetypes, und in welchem Verhältnis stehen openEHR und HL7 FHIR zueinander laut Lehne-Paper?

?

Laut Lehne et al. (2019), Sektion „Syntactic interoperability":

**openEHR-Archetypes**: Spezifikationen klinischer Konzepte, die auf einem zugrundeliegenden **Reference Model** aufbauen. Klinische Fachpersonen und IT-Experten können damit klinische Inhalte gemeinsam definieren.

openEHR enthält außerdem:
- **AQL (Archetype Querying Language)** – portable Abfragesprache
- Tools zum Definieren und Publizieren der Archetypes

**Verhältnis zu HL7 FHIR** (laut Paper):

| | HL7 FHIR | openEHR |
|---|---|---|
| Interoperabilitätsebene | Syntaktisch | Syntaktisch |
| Architektur | Resource-Set + REST-API | Reference Model + Archetypes + AQL |
| Verhältnis | Parallel, ohne explizite Wertung im Paper | Parallel, ohne explizite Wertung im Paper |

Das Paper beschreibt beide als **parallele Initiativen** für strukturierten Gesundheitsdaten-Austausch – konkurrierend oder komplementär wird nicht bewertet.

**Grenze der Note**: Genaue Modellarchitektur, ISO-13606-Normierung, DACH-Verbreitung werden im Paper nicht ausgeführt.

---

Wann ist ein nachrichtenbasierter (HL7 v2), dokumentenbasierter (CDA) oder ressourcenbasierter (FHIR) Ansatz vorzuziehen?

?

Laut MSI - Datenaustausch - Formen und MSI - HL7 FHIR - Paradigmen:

**Nachrichtenbasiert (HL7 v2)**:
- Geeignet für: ereignisgesteuerte Workflows (Aufnahme, Entlassung, Laborbefund-Bestellung)
- Stärke: bewährt, weit verbreitet, klare Trigger
- Schwäche: schwergewichtig, ungeeignet für Mobilgeräte, schwer erweiterbar (laut FHIR-Vortrag)

**Dokumentenbasiert (CDA)**:
- Geeignet für: regulierte, persistente Dokumente (Entlassungsbriefe, ELGA-Laborbefunde)
- Stärke: Persistenz, Ganzheit, Authentisierung, Stylesheet-Darstellung; bewährt in regulierten Umgebungen
- Schwäche: schwergewichtig; keine granularen API-Abfragen

**Ressourcenbasiert (FHIR)**:
- Geeignet für: API-orientierte Systeme, mobile Apps, granulare Abfragen (z. B. nur eine Observation)
- Stärke: Entwicklerfreundlichkeit, 80 % Use Cases out-of-the-box, moderner Technologie-Stack
- Schwäche: keine native Gesamtübersicht ohne Bundle; ohne gemeinsame Profile keine Interoperabilität

**Fazit** (laut FHIR-Vortrag): Koexistenz ist die Norm. FHIR ersetzt nicht alle älteren Standards; bestehende HL7-v2- und CDA-Systeme werden oft weiter betrieben, evtl. mit FHIR Facade.

---

## Mögliche Anschlussfragen des Prüfers

- „Welche HL7-Datenaustausch-Form ist bei ELGA primär im Einsatz – und warum?"
- „Ordnen Sie folgendem CDA-Snippet Entities, Roles, Participations und Acts zu." (Snippet wird vorgelegt)
- „Ein Krankenhaus erfüllt EIS ENHANCED. Was kann es, was kann es nicht – im Vergleich zu EIS FULL SUPPORT?"
- „Warum war HL7 CDA für mobile Anwendungen ungeeignet, und wie löst FHIR das?"
- „IPS klingt wie die Lösung für grenzüberschreitende Kommunikation – welche Hürden bleiben trotzdem?"
- „Was unterscheidet die syntaktische Ebene von der semantischen am Beispiel FHIR + LOINC?"
- „openEHR und FHIR – sind das Konkurrenten oder Ergänzungen? Wie argumentieren Sie?"
- „Was bedeutet Abwärtskompatibilität bei normativen FHIR-Ressourcen konkret für ein Krankenhaus-IT-Projekt?"

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
