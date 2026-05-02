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

# MSI - PF - IHE-Profile

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz deckt die IHE-Profile des MSI-Lehrplans ab: IHE XDS (Cross-Enterprise Document Sharing) mit Akteur-Architektur, Transaktionen und ELGA-Metadaten, sowie die Terminologie-Profile IHE SVS (Sharing Value Sets, SOAP-basiert) und IHE SVCM (Sharing Valuesets, Codes and Maps, FHIR-basiert). Da für IHE kein separates Detail-PF vorgesehen ist, geht dieser Kartensatz tiefer als die übrigen Themenbereich-PFs. Quellen: MSI VL HL7 CDA und e-Befunde (XDS), MSI VL HL7 FHIR und Terminologieserver (SVS, SVCM).

## Verlinkte Konzepte

- [[MSI - IHE XDS - Architektur]]
- [[MSI - IHE XDS - Dokument-Metadaten]]
- [[MSI - IHE SVS - Sharing Value Sets]]
- [[MSI - IHE SVCM - Sharing Value Sets Codes and Maps]]

---

## Karten

### Definition

Welche Akteure kennt IHE XDS (Cross-Enterprise Document Sharing), und welche Transaktionen (mit ITI-Nummern) verbinden sie?

?

Laut Folie 34 (MSI VL HL7 CDA und e-Befunde):

**Akteure:**
- **Patient Identity Source** – stellt Patientenidentitäten bereit
- **Document Source** – sendet Dokumente in das Repository
- **Document Repository** – speichert Dokumente persistent
- **Document Registry** – führt den Index/Inventar, vermittelt Suchanfragen
- **Document Consumer** – fragt Registry ab und holt Dokumente vom Repository
- **On-Demand Document Source** – erzeugt Dokumente erst bei Anfrage

**Transaktionen:**

| ITI-Nr. | Transaktion | Richtung |
|---|---|---|
| ITI-8 | Patient Identity Feed | Patient Identity Source → Document Registry |
| ITI-44 | Patient Identity Feed HL7v3 | Patient Identity Source → Document Registry (HL7 v3-Variante) |
| ITI-41 | Provide & Register Document Set-b | Document Source → Document Repository |
| ITI-42 | Register Document Set-b | Document Repository → Document Registry |
| ITI-43 | Retrieve Document Set | Document Consumer ← Document Repository |
| ITI-18 | Registry Stored Query | Document Consumer ↔ Document Registry |
| ITI-61 | Register On-Demand Document Entry | On-Demand Document Source → Document Registry |

> Hinweis: Die Folie zeigt die Architektur primär als Bild; vertiefte Transaktionsbeschreibungen sind im PDF nicht ausgeführt.

---

Was ist IHE SVS (Sharing Value Sets), welche Akteure und Transaktionen hat es, und auf welcher Technologie basiert es?

?

Laut Folie 11 (MSI VL HL7 FHIR und Terminologieserver):

**IHE SVS** ist ein IHE-Integrationsprofil im IT Infrastructure Technical Framework zur standardisierten Abfrage von Terminologien aus einem Value Set Repository.

**Basis-Technologie**: SOAP und XML.

**Akteure:**
- **Value Set Repository** (server-seitig)
- **Value Set Consumer** (client-seitig)

**Transaktionen:**
- **ITI-48** – Retrieve Value Set (einzelnes Value Set abrufen)
- **ITI-60** – Retrieve Multiple Value Sets (mehrere Value Sets abrufen)

---

Was ist IHE SVCM (Sharing Valuesets, Codes and Maps), welche sieben Transaktionen kennt es, und auf welche FHIR-Operationen mappen sie?

?

Laut Folie 51 (MSI VL HL7 FHIR und Terminologieserver):

**IHE SVCM** ist das aktuelle, FHIR-basierte IHE-Profil zum Terminologieaustausch. Akteure: **Terminology Repository** (server-seitig) + **Terminology Consumer** (client-seitig).

| ITI-Nr. | Transaktion | FHIR-Pendant |
|---|---|---|
| ITI-95 | Query Value Set | ValueSet read/search |
| ITI-96 | Query Code System | CodeSystem read/search |
| ITI-97 | Expand Value Set | `ValueSet/$expand` |
| ITI-98 | Lookup Code | `CodeSystem/$lookup` |
| ITI-99 | Validate Code | `ValueSet/$validate-code` |
| ITI-100 | Query Concept Map | ConceptMap read/search |
| ITI-101 | Translate Code | `ConceptMap/$translate` |

Drei FHIR-Resource-Typen sind beteiligt: **ValueSet, CodeSystem, ConceptMap**.

---

Warum trennt IHE XDS Document Repository und Document Registry? Was ist der architektonische Grundgedanke?

?

Laut Folie 34 und der Prüfungsrelevanz-Sektion in MSI - IHE XDS - Architektur:

Die XDS-Architektur trennt **Speicherung** (Repository) und **Suche** (Registry) bewusst:

- **Document Repository** hält die *Dokumente selbst* persistent – die eigentlichen Bytes (z. B. CDA-XML-Dateien)
- **Document Registry** hält den *Index / die Metadaten* – Dokumentenbeschreibungen (Autor, Datum, Fachrichtung, Klasse, EIS-Stufe, …)

**Vorteil der Trennung:**
- Ein Consumer kann die Registry effizient nach Metadaten durchsuchen, **ohne jedes Dokument herunterladen** zu müssen (Registry Stored Query ITI-18)
- Erst wenn das gesuchte Dokument gefunden ist, wird es gezielt per ITI-43 (Retrieve Document Set) vom Repository geholt
- Mehrere Repositories können in derselben Affinity Domain registriert sein

Das entspricht dem Prinzip von Metadaten als Suchfilter (vgl. MSI - Daten - Metadaten, Folie 17: „Umgang mit dem Dokument möglich, ohne den gesamten Inhalt herunterladen zu müssen").

---

### Anwendung

Skizzieren Sie den vollständigen XDS-Ablauf: Ein Krankenhaus bringt einen Entlassungsbrief in ELGA ein, und ein Hausarzt sucht ihn später. Welche Transaktionen laufen in welcher Reihenfolge?

?

Laut Folie 34 und Beispiel in MSI - IHE XDS - Architektur:

**Einbringen (Document Source = Krankenhaus):**
1. **ITI-8 / ITI-44** – Patient Identity Feed: Patient Identity Source meldet den Patienten bei der Document Registry an.
2. **ITI-41** – Provide & Register Document Set-b: Document Source (Krankenhaus) sendet Dokument + Metadaten an das Document Repository.
3. **ITI-42** – Register Document Set-b: Document Repository registriert die Metadaten automatisch bei der Document Registry.

**Suchen und Abrufen (Document Consumer = Hausarzt):**
4. **ITI-18** – Registry Stored Query: Document Consumer fragt die Document Registry nach Dokumenten zu einem Patienten (z. B. gefiltert nach Fachrichtung, Dokumentklasse, Datum).
5. **ITI-43** – Retrieve Document Set: Document Consumer holt das konkrete Dokument vom Document Repository.

**Kein direkter Kontakt** zwischen Document Source und Document Consumer – das ist das Kennzeichen ungerichteter Kommunikation.

---

Welche XDS-Metadaten muss ein ELGA-Dokument laut Leitfaden zwingend („immer") tragen? Nennen Sie mindestens sechs.

?

Laut Folie 36 (MSI VL HL7 CDA und e-Befunde):

Pflichtfelder (Vorkommen „Immer"):
1. **Autor (Verfasser)** – z. B. Dr. Herbert Mustermann
2. **Organisation des Autors** – z. B. Amadeus Spital, Chirurgie
3. **Art der Organisation** – codiert (z. B. „Abteilung", „Ambulante Erstversorgung")
4. **Rechtlicher Unterzeichner** – z. B. Dr. Herbert Mustermann
5. **Erstellungsdatum** – z. B. 2012-08-16 13:20:41 inkl. Zeitzone
6. **Patientendaten** – Name, Geburtsdatum, Geschlecht, Adresse
7. **Titel des Dokuments** – z. B. „Ultraschalldiagnostik des Abdomens"
8. **Dokumentenklasse** – codiert, z. B. „Entlassungsbrief", „Laborbefund"
9. **Dokumententyp** – codiert, z. B. „Entlassungsbrief Ärztlich"
10. **Fachrichtung** – codiert, z. B. „Chirurgie", „Labordiagnostik"
11. **Gültigkeit** – codiert, z. B. „Approved", „Deprecated"
12. **ELGA-Interoperabilitätsstufe** – codiert, z. B. „EIS Enhanced"

Optionale / „sofern bekannt"-Felder: Gesundheitsdienstleistung (APPC), Zeitraum der Gesundheitsdienstleistung, Rolle und Funktionscode des Autors.

---

Welche ITI-Transaktion aus IHE SVCM verwenden Sie für: (a) Code-Validierung in einem ValueSet, (b) ValueSet-Expansion (alle Konzepte auflisten), (c) Code-Übersetzung via ConceptMap?

?

Laut Folie 51 (MSI VL HL7 FHIR und Terminologieserver):

- **(a) Code-Validierung** → **ITI-99** – Validate Code → FHIR-Pendant: `ValueSet/$validate-code`
- **(b) ValueSet-Expansion** → **ITI-97** – Expand Value Set → FHIR-Pendant: `ValueSet/$expand`
- **(c) Code-Übersetzung** → **ITI-101** – Translate Code → FHIR-Pendant: `ConceptMap/$translate`

Merkhilfe: ITI-97 = Expand (97 > 95 = Query, also schon ein Schritt tiefer: nicht nur suchen, sondern auffalten). ITI-99 = Validate. ITI-101 = Translate (letzter Schritt im Workflow, höchste Nummer).

---

Welche zwei SVS-Transaktionen gibt es, und wann verwendet man welche?

?

Laut Folie 11 (MSI VL HL7 FHIR und Terminologieserver):

- **ITI-48 – Retrieve Value Set**: holt **ein einzelnes** Value Set aus dem Repository. Geeignet, wenn die OID des benötigten Value Sets bekannt ist.
- **ITI-60 – Retrieve Multiple Value Sets**: holt **mehrere** Value Sets in einer Anfrage. Effizienter, wenn ein System bei Startup eine ganze Bibliothek von Value Sets laden muss (z. B. alle ELGA-Value-Sets für ein neues KIS-Release).

---

### Diskussion

Vergleichen Sie IHE SVS und IHE SVCM: Unterschiede, Evolution, warum wurde SVCM eingeführt?

?

Laut MSI - IHE SVS und MSI - IHE SVCM:

| Kriterium | IHE SVS | IHE SVCM |
|---|---|---|
| **Basis-Technologie** | SOAP + XML | HL7 FHIR (REST + JSON/XML) |
| **Akteure** | Value Set Repository / Value Set Consumer | Terminology Repository / Terminology Consumer |
| **Resource-Typen** | Nur Value Sets | ValueSet + CodeSystem + ConceptMap |
| **Transaktionen** | 2 (ITI-48, ITI-60) | 7 (ITI-95 bis ITI-101) |
| **Operationen** | Nur Abrufen | Abrufen, Expand, Lookup, Validate, Translate |
| **Alter** | Älter, rückläufig in Verbreitung | Aktuell, FHIR-Standard-Linie |

**Warum SVCM**: Mit der Verbreitung von FHIR wurde eine FHIR-native Profilierung der Terminologiedienste gebraucht. SVCM bietet mehr Operationen (Code-Lookup, Validation, Translation) und adressiert nicht nur Value Sets sondern auch Code Systems und Concept Maps. SOAP/XML-basiertes SVS gilt als veraltet.

---

Welchen Vorteil hat IHE SVCM gegenüber dem reinen FHIR Terminology Service (ohne IHE-Profilierung)?

?

Laut MSI - IHE SVCM - Sharing Value Sets Codes and Maps:

**Reiner FHIR Terminology Service** (ohne IHE-Profilierung): definiert die FHIR-Operationen ($expand, $validate-code, $translate etc.) und die zugehörigen Resources (CodeSystem, ValueSet, ConceptMap) – legt aber keine bindenden Konformitätsanforderungen an Server-Implementierungen fest.

**IHE SVCM als Profilierung**: legt zusätzlich fest, *welche* dieser Operationen ein konformer Server implementieren muss, welche Akteur-Rollen existieren (Terminology Repository vs. Terminology Consumer) und welche Konformitäts-Zusicherungen gelten müssen.

**Vorteil**: Interoperabilität zwischen verschiedenen Terminologieservern und Clients ist durch die Profilierung stärker sichergestellt. Ein „SVCM-konformer Server" hat definierte Zusagen, ein „FHIR-Server mit Terminology-Support" nicht unbedingt.

Laut Note: „SVCM ≠ FHIR Terminology Service: SVCM ist die *IHE-Profilierung* des FHIR Terminology Service – es legt zusätzlich Konformitätsanforderungen auf das FHIR-Verhalten."

---

Warum ist IHE XDS ein klassisches Beispiel für ungerichtete Kommunikation? Welche Konsequenz ergibt sich daraus für Berechtigungen?

?

Laut MSI - IHE XDS - Architektur und MSI - Datenaustausch - Gerichtet vs Ungerichtet:

**Ungerichtet**: Beim Hochladen (ITI-41) ist der zukünftige Empfänger dem Document Source (z. B. Krankenhaus) zum Zeitpunkt des Sendens **nicht bekannt**. Das Dokument wird ins Repository abgelegt; wer es später per ITI-18/ITI-43 abruft, ist beim Einbringen offen.

Das entspricht dem Pull-Modus: Empfänger holen aktiv aus einem gemeinsamen Repository, statt vom Sender direkt adressiert zu werden.

**Konsequenz für Berechtigungen**: Da jeder berechtigte Consumer das Dokument abrufen kann, braucht es ein explizites Berechtigungsmanagement:
- Wer darf Registry Stored Query (ITI-18) absenden?
- Wer darf Retrieve Document Set (ITI-43) auf das Repository?
- ELGA löst das über APPC (Austrian Privacy Policy Code) in den Metadaten – ein Consumer muss den richtigen APPC-Code abfragen dürfen

Querbezug zu ASP (Datensicherheit und Privacy als technische Interoperabilitäts-Garantie, Folie 5).

---

Was ist der Unterschied zwischen Dokumentenklasse und Dokumententyp in den XDS-Metadaten? Geben Sie ein Beispiel.

?

Laut Folie 36 (MSI VL HL7 CDA und e-Befunde) und MSI - IHE XDS - Dokument-Metadaten:

- **Dokumentenklasse**: übergeordnete Kategorie, grob. Beispiel: „Entlassungsbrief", „Laborbefund", „Befund bildgebende Diagnostik."
- **Dokumententyp**: feinere Unterkategorie innerhalb der Klasse. Beispiel: Klasse „Entlassungsbrief" → Typen „Entlassungsbrief Ärztlich" vs. „Entlassungsbrief Pflege". Klasse „Befund bildgebende Diagnostik" → Typen „Nuklearmedizinischer Befund", „Echokardiographie-Befund", „Endoskopie-Befund".

Beide Felder sind **immer und codiert** erforderlich. Die Codierung kommt aus ELGA-Value-Sets.

**Prüfungsfalle**: Klasse und Typ können denselben Begriff tragen (z. B. „Entlassungsbrief" als Klasse, „Entlassungsbrief Ärztlich" als Typ) – sie sind aber getrennte Metadatenfelder mit unterschiedlicher Granularität.

---

### Vergleich

Welche Beziehung besteht zwischen XDS-Metadaten und CDA-Header? Wo kommen die XDS-Metadaten her, und was ist ihr architektonischer Unterschied zum CDA-Inhalt?

?

Laut Folie 35 (MSI VL HL7 CDA und e-Befunde) und MSI - IHE XDS - Dokument-Metadaten:

**Herkunft**: Viele XDS-Metadaten **leiten sich direkt aus dem CDA-Header ab** – z. B. Autor, Erstellungsdatum, Patientendaten, Dokumentenklasse. Der CDA-Header ist die Quelle; beim Einbringen (ITI-41) extrahiert das System die Metadaten und übergib sie an die Registry.

**Architektonischer Unterschied**:
- **CDA-Header** ist Teil des CDA-Dokuments selbst (XML, im Repository gespeichert). Lesbar nur nach Herunterladen des Dokuments.
- **XDS-Metadaten** sind separat in der **Document Registry** geführt (als eigenständige Einträge). Durchsuchbar **ohne das Dokument öffnen zu müssen** (→ Registry Stored Query ITI-18).

**Konsequenz**: Für die Suche und Filterung (z. B. im ELGA-Portal: nach Fachrichtung, Dokumententyp, Erstellungsdatum) werden ausschließlich die Registry-Metadaten genutzt – nicht der CDA-Inhalt. Erst nach Selektion eines Treffers wird das Dokument per ITI-43 vom Repository geholt.

---

## Mögliche Anschlussfragen des Prüfers

- „Skizzieren Sie die XDS-Architektur an der Tafel und erklären Sie, welcher Akteur welche Funktion hat."
- „Was passiert, wenn der Document Source beim ITI-41 keine Metadaten mitschickt – welcher Schritt im XDS-Ablauf schlägt fehl?"
- „Warum braucht es IHE SVCM, wenn FHIR selbst schon Terminologiedienste (`$expand`, `$validate-code`) definiert?"
- „Was ist der Unterschied zwischen ITI-97 und einer direkten FHIR-REST-Anfrage `GET ValueSet/$expand`?"
- „Wie wird die EIS-Stufe in den XDS-Metadaten geführt, und welcher Use Case rechtfertigt das?"
- „Was meint ‚Approved' vs. ‚Deprecated' in den Gültigkeits-Metadaten – und wann wird ein Dokument auf Deprecated gesetzt?"
- „Welche Konsequenz hat ungerichtete Kommunikation für Privacy und Datenschutz in ELGA?"
- „IHE hat viele Profile (XDS, XCA, XDR, XDM, PIX/PDQ) – welchen kennen Sie, und was unterscheidet XDS von XCA?" *(Anm.: XCA im PDF nur indirekt erwähnt)*

## Eigene Notizen

*Wo bin ich beim Üben unsicher gewommen? Was muss ich nochmal nachschlagen?*
