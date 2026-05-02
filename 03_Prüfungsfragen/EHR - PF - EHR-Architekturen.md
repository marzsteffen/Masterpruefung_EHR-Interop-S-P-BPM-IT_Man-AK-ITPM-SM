---
fach: ehr
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/ehr
---

# EHR - PF - EHR-Architekturen

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz deckt die zentralen Architekturentscheidungen für EHR-Systeme ab, wie sie in den Vorlesungen zu Einführung & Definitionen und Macro-Level Interoperabilität behandelt werden: die Designfragen Zentral vs. Dezentral und Registry vs. Repository, das ISO-23903-Referenzarchitektur-Framework sowie das 5-Level-Schichtmodell von HL7 FHIR. Viele Fragen werden in der Vorlesung explizit offen gelassen und als Diskussionsanstoß formuliert – das spiegelt sich in den Diskussionskarten wider.

## Verlinkte Konzepte

- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - Architektur - Registry vs Repository]]
- [[EHR - Architektur - ISO 23903 3D]]
- [[EHR - HL7 FHIR - 5 Levels]]

---

## Karten

### Definition

Was sind die wesentlichen Vergleichsachsen zwischen einer zentralen und einer dezentralen EHR-Architektur?
?
**Zentral**: alle Patientendaten in einem Repository; direkter Zugriff, keine Aggregationslatenz. Risiken: Single Point of Failure, große Angriffsfläche, politische Frage der Datenhoheit. **Dezentral**: Daten bleiben bei den datenerzeugenden Versorgern; auf Anfrage zusammengeführt. Vorteil: Datenhoheit bei Versorgern, kein zentrales Ausfallrisiko. Risiken: Verfügbarkeit hängt von den Quellsystemen ab, Konsistenz ist schwieriger zu gewährleisten. Vergleichsachsen: (1) Datenhoheit – zentral: ein Betreiber; dezentral: bleibt beim Versorger; (2) Verfügbarkeit – zentral: Single Point of Failure; dezentral: abhängig vom jeweiligen Quellsystem; (3) Privacy – zentral: große Angriffsfläche; dezentral: mehrere kleinere; (4) Synchronisation – zentral: konzeptuell einfacher; dezentral: Konsistenz schwieriger.

Was unterscheidet ein EHR-Repository von einer EHR-Registry – und welche Vergleichsachsen sind entscheidend?
?
**Repository**: das EHR-System speichert alle Daten selbst (lokal kopiert). Vorteil: schneller Zugriff, unabhängig vom Quellsystem. Nachteil: Datendoppelung, aufwendige Synchronisation. **Registry (On-the-fly Accumulation)**: das EHR hält nur Verweise (Pointer/Links) auf Daten, die beim Quellsystem verbleiben; Daten werden bei Bedarf zusammengezogen. Vorteil: immer aktuell, keine Redundanz. Nachteil: Verfügbarkeit und Latenz hängen von den Quellsystemen ab. Vergleichsachsen: Datenhaltung (kopiert vs. verlinkt) · Aktualität (Sync-abhängig vs. live) · Verfügbarkeit (unabhängig vs. Quell-abhängig) · Antwortzeit (typisch schneller vs. Aggregationslatenz). Praxisbeispiel: PACS-Bilder werden in EHRs oft per Registry-Verweis geführt, Diagnosen eher im Repository.

Welche fünf Levels unterscheidet das HL7-FHIR-Schichtmodell – und was adressiert jedes Level?
?
Level 1 – **Foundation**: Technologien zum Encoding von Daten in digitale Formate; Datentypen und Basisstrukturen für Computernetze. Level 2 – **Conformance**: Regeln und Strukturen für Metadaten; Security, Terminologie, Conformance-Beschreibungen und Exchange-Features (z. B. CapabilityStatement). Level 3 – **Master Data**: Stammdaten-Management; Verlinkung von Records zu Personen (Patient, Practitioner), Organisationen, Geräten, Locations, Services. Level 4 – **Operational Data**: operative Versorgungs-Daten; klinische Events (Observation, Condition), Diagnostik, Medikation (MedicationRequest), Workflow, Finanz-Events (Encounter). Level 5 – **Knowledge**: Wissens-Daten; digitales Knowledge Sharing erlaubt schnelles Update klinischer Algorithmen und Medikations-Guidance (z. B. PlanDefinition, ActivityDefinition, Library).

---

### Anwendung

Auf welchem FHIR-Level liegt jeweils: Patient, Practitioner, Observation, MedicationRequest, Condition, PlanDefinition, CapabilityStatement?
?
Level 2 – **Conformance**: CapabilityStatement (beschreibt, was ein FHIR-Server kann). Level 3 – **Master Data**: Patient, Practitioner, Organization, Device, Location. Level 4 – **Operational Data**: Observation (Messwerte, Befunde), MedicationRequest (Medikationsauftrag), Condition (Diagnose), Encounter (Kontakt). Level 5 – **Knowledge**: PlanDefinition (klinische Pfade, CDS-Hooks), ActivityDefinition, Library. Faustregel: „Wer ist wo?" → Level 3; „Was ist passiert?" → Level 4; „Was soll getan werden (Regeln)?" → Level 5.

Welche drei Dimensionen unterscheidet ISO 23903 – und wie ordnet es ein konkretes Element (z. B. FHIR) ein?
?
ISO 23903 ist eine Health-Informatics-Referenzarchitektur mit drei Dimensionen: (1) **Viewpoint** – Requirements, Organization, Tools, Technology; (2) **Components / Composition** – Concepts, Relations, Details; (3) **Domains** – Capability, Purpose, Provision, Custody, Consumption. Einordnung FHIR: im Viewpoint „Technology" (konkretes Protokoll), auf Composition-Ebene „Details" (konkrete Resource-Schemas), in den Domains hauptsächlich „Provision" (Bereitstellung) und „Consumption" (Nutzung). ISO 23903 selbst macht keine Technologievorgaben – es ist das Raster, in das man FHIR, IHE, OpenEHR usw. einsortiert.

Welche Daten würdest du bei einem EHR-Design eher im Repository halten, welche per Registry verlinken – und warum?
?
**Im Repository (lokal kopiert):** Daten, die häufig und schnell abgerufen werden müssen und deren Veralterungsrisiko gering ist: Diagnosen, Medikamentenliste, Allergien, Laborbefunde (Textkopie). Begründung: Zugriff unabhängig vom Quellsystem, keine Latenz bei der Behandlungsentscheidung. **Per Registry (verlinkt):** Daten mit großem Volumen, die selten aktuell abgerufen werden oder im Quellsystem best gehalten werden: Radiologie-Bilder (PACS), Video-/Audiodaten, originale Gerätedaten (EKG-Kurven). Begründung: Datenmenge macht Kopie impraktikabel, Quellsystem ist für diese Daten ohnehin verantwortlich. **Hybrid-Ansatz:** Textbefund des Radiologen ins Repository, Bild selbst per PACS-Link. Das entspricht auch der HIMSS-Anforderung: „Storage of images, video, audio OR linking" (Folie 46).

---

### Diskussion

Wie kombinieren sich Zentral/Dezentral und Repository/Registry – und welche vier Mischformen entstehen?
?
Die beiden Designfragen sind unabhängig und erzeugten vier Mischformen: (1) **Zentral + Repository**: ein zentrales System speichert alle Daten – maximale Effizienz, maximales Single-Point-of-Failure-Risiko. (2) **Zentral + Registry**: ein zentraler Index (Metadaten-Server) verweist auf dezentrale Quellsysteme – „zentraler Türöffner, dezentrale Daten". Typisch für IHE-XDS-Architektur und Varianten von ELGA. (3) **Dezentral + Repository**: jede Organisation hat ihr eigenes vollständiges Repository – keine Zentralabhängigkeit, aber Interoperabilität muss über Exchange-Formate gelöst werden. (4) **Dezentral + Registry**: verteilte Indizes, föderierte Suche – komplex und selten rein umgesetzt. In der Praxis dominieren Hybride: zentrale Registry mit dezentralen Repositories.

Inwiefern ist ELGA zentral oder dezentral, Repository oder Registry? Was lässt die Vorlesung offen?
?
Die Vorlesung stellt die Frage explizit als offene Diskussion: „Welches Design hat ELGA?" (Folie 39, 86) und gibt keine abschließende Antwort. Aus dem CCR/CCD-VL ergibt sich: Österreich ist **semi-zentralisiert** (nationale Klammer, aber bundeslandspezifische Systeme). Strukturell folgt ELGA dem Muster **zentrale Registry + dezentrale Repositories**: die ELGA-Infrastruktur führt einen zentralen Index (welche Dokumente gibt es für welchen Patienten), während die Dokumente selbst dezentral bei den Versorgern (Krankenhäusern, Ärztekammern) liegen. Kritische Diskussionspunkte: (a) Welche Auswirkung hat dezentrale Speicherung auf Verfügbarkeit? (b) Welche Rolle spielt die ELGA GmbH als zentraler Betreiber der Infrastruktur – de facto zentrales Governance bei dezentraler Datenhaltung? (Hinweis: genaue technische Architektur-Details sind im PDF der VL „Einführung & Definitionen" nicht ausgeführt.)

Warum ist FHIR Level 5 (Knowledge) in der Praxis selten produktiv im Einsatz – und was wäre nötig, um das zu ändern?
?
Level 5 umfasst digitale Wissens-Ressourcen: PlanDefinition, ActivityDefinition, Library – d. h. formalisierte CDS-Regeln, die per FHIR geteilt und geupdated werden können. Gründe für geringe Verbreitung: (1) **Komplexität der Formalisierung** – klinisches Wissen ist schwer in maschinenlesbare Regeln zu überführen; (2) **Haftungsfragen** – wer haftet, wenn eine verteilte Regel zu einem Behandlungsfehler führt?; (3) **Terminologie-Abhängigkeit** – Level 5 setzt voraus, dass Level 3 (Stammdaten) und Level 4 (Operativ) vollständig und semantisch korrekt sind; (4) **Fehlende Governance** – wer pflegt und validiert die Wissens-Ressourcen? Für breiten Einsatz nötig: semantische Interoperabilität auf Levels 3–4, klare Haftungsmodelle, Terminologie-Alignment, vgl. aktuelle Entwicklung mit CDS Hooks als FHIR-nativer CDS-Integration.

Wozu braucht man ISO 23903 als Referenzarchitektur – wenn es schon FHIR, IHE und OpenEHR gibt?
?
FHIR, IHE und OpenEHR sind **konkrete Standards und Implementierungs-Spezifikationen** für spezifische Aspekte (Datenaustausch, Profiling, Datenmodellierung). ISO 23903 ist ein **Meta-Framework**: es ordnet diese Standards in ein gemeinsames Raster ein, ohne selbst Technologievorgaben zu machen. Analogie: ISO 23903 ist die Stadtplanung, FHIR/IHE/OpenEHR sind die Gebäude-Standards für einzelne Gebäudetypen. Praktischer Nutzen: (1) Einheitliche Sprache für Architektur-Diskussionen über Standard-Grenzen hinweg; (2) Identifikation von Lücken (welche Domain ist unabgedeckt?); (3) Basis für nationale eHealth-Architektur-Beschreibungen. Kritik: Referenzarchitekturen sind abstrakt und oft akademisch – sie geben wenig operative Umsetzungshilfe.

---

## Mögliche Anschlussfragen des Prüfers

- Welches Architekturmuster nutzt IHE XDS konkret – zentral/dezentral, Registry/Repository?
- Welche HIMSS-Anforderungen werden durch eine reine Registry-Architektur schwer erfüllbar (Stichwort: Verfügbarkeit > 99,9 %)?
- Was passiert bei einer Repository-Architektur mit Datenhoheit und DSGVO-Löschungsrecht?
- Welches FHIR-Level ist für strukturelle Interoperabilität verantwortlich, welches für semantische?
- Wie verhält sich ISO 23903 zu Zachman: Wo überschneiden sie sich, wo ergänzen sie sich?
- Welche Architektur-Entscheidung (zentral/dezentral, Repository/Registry) hat den größten Einfluss auf die Latenz in der Notaufnahme?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
