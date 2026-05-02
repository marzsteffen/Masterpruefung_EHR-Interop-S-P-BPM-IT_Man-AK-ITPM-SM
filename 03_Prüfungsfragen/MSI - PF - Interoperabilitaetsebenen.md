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

# MSI - PF - Interoperabilitaetsebenen

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz deckt das thematische Fundament von MSI ab: Was ist Interoperabilität, wie wird sie in Ebenen gegliedert (Drei-Schichten-Modell, Vier-Ebenen-Modell Lehne, Benson/Grieve), welche Voraussetzungen und Herausforderungen existieren, und welche Rolle spielen strukturierte Daten, Metadaten, Standards und Datenaustausch-Muster. Quellen sind die Einführungs-Vorlesung (MSI VL Einführung in Standards und Interoperabilität) sowie das Pflichtpaper Lehne et al. 2019 (npj Digital Medicine). Das Thema zieht Anschlussfragen in nahezu alle anderen MSI-Themenbereiche.

## Verlinkte Konzepte

- [[MSI - Interoperabilität - Definition]]
- [[MSI - Interoperabilitätsebenen - Drei-Schichten-Modell]]
- [[MSI - Interoperabilitätsebenen - Technisch]]
- [[MSI - Interoperabilitätsebenen - Syntaktisch]]
- [[MSI - Interoperabilitätsebenen - Semantisch]]
- [[MSI - Interoperabilitätsebenen - Organisatorisch]]
- [[MSI - Interoperabilitätsebenen - Benson Grieve Layer-Modell]]
- [[MSI - Interoperabilitätsebenen - Vier-Ebenen-Modell Lehne]]
- [[MSI - Interoperabilität - Voraussetzungen]]
- [[MSI - Interoperabilität - Herausforderungen]]
- [[MSI - Interoperabilität - Anwendungsbereiche Lehne]]
- [[MSI - Daten - DIKW-Pyramide]]
- [[MSI - Daten - Strukturiert vs Unstrukturiert]]
- [[MSI - Daten - Datentypen]]
- [[MSI - Daten - Metadaten]]
- [[MSI - Datenaustausch - Gerichtet vs Ungerichtet]]
- [[MSI - Standards - Definition]]
- [[MSI - Standards - Nutzen]]
- [[MSI - Paper - Why Digital Medicine Depends on Interoperability]]

---

## Karten

### Definition

Welche zwei Stufen der Interoperabilität unterscheidet die Vorlesung, und worin unterscheiden sie sich konkret?

?

**Interoperabilität (allgemein)** (Folie 4/5, MSI VL Einführung):
- Dokumente und Nachrichten können übertragen werden.
- Befunde und Berichte können in andere Systeme übernommen werden.
- Daten aus anderen Systemen stehen automatisch zur Verfügung.

**Semantische Interoperabilität** (darüber hinaus):
- Dieselben Daten müssen nicht mehrfach eingegeben werden.
- Daten können weiterverarbeitet werden: Warnungen, Erinnerungen, Zusammenfassungen, Berechnungen, Verläufe, Statistiken.

Zentraler Anspruch (Folie 4): „Both ends exchange, understand and act on the data received." – nicht nur Übertragen, sondern Verstehen und Handeln.

---

Welche drei Ebenen unterscheidet das Drei-Schichten-Modell der Interoperabilität, und was charakterisiert jede Ebene?

?

Drei verschachtelte Schichten (Folie 5, MSI VL Einführung):

| Ebene | Kernaussage | Stichworte laut Folie |
|---|---|---|
| **Technical** (innen) | Austausch aus technischer Sicht; garantiert Datensicherheit/Privacy, Datenintegrität, Zugriff auf identifizierten Patienten | Transport protocols, Standards, Profiles, Services and messages, Health metadata |
| **Semantic** (mitte) | Beide Seiten verstehen die Bedeutung der ausgetauschten Information, über kulturelle und sprachliche Grenzen | Standards and profiles, Clinical procedures, Terminologies, Medical guidelines |
| **Organisational** (außen) | Wille und Fähigkeit zusammenzuarbeiten; abhängig von Gesetzen, Policies, Kooperationsvereinbarungen | Legal framework, Cooperative workflows, Policies |

Verschachtelung: Jede äußere Schicht setzt die inneren voraus.

---

Welche drei Eigenschaften definieren einen Standard laut Benson/Grieve, wie in der Vorlesung dargestellt?

?

Definitions-Triade (Folie 12, Mindmap-Quelle Benson and Grieve, *Principles of Health Interoperability*):

1. **Aim for optimum degree of order** – Anstreben eines optimalen Ordnungsgrades.
2. **Consensus process** – Konsensprozess.
3. **Recognised body** – anerkanntes Gremium.

Zusatz aus Folie 11: Reihenfolge ist zentral – erst Standards verstehen, dann Problem lösen (nicht umgekehrt). Auf den Einwand „Ein Standard schränkt mich ein": Im Idealfall sind Standards Vorgaben, die helfen, eine Herausforderung schneller zu verstehen und zu lösen.

---

Welche Stufen umfasst die DIKW-Pyramide nach Aamodt und Nygård (1995) laut Vorlesung, und welche Operationen verbinden sie?

?

Fünf Stufen (Folie 13, MSI VL Einführung, „nach Aamodt und Nygård, 1995"):

| Stufe | Beispiel (Folie) | Operation zur nächsten Stufe |
|---|---|---|
| Zeichen | H, K, R, 0, 0, 0, 5, € | Erkennen |
| Daten | HR K 5000 € | Verstehen im Kontext |
| Information | Hr. K. hat 5.000 € überwiesen. | In Beziehung setzen |
| Wissen | Ungewöhnlich hoher Betrag für Hr. K. (bisher nie mehr als 1.000 €) | Anwenden |
| Aktion | Überweisung stoppen. Hr. K. kontaktieren. | – |

Prüfungsankerpunkt: Semantische Interoperabilität setzt vor allem an den Übergängen Daten→Information und Information→Wissen an – Standards und Terminologien sichern den Bedeutungstransfer.

---

### Anwendung

Klassifizieren Sie folgende Datenquellen als „strukturiert" oder „unstrukturiert" laut Vorlesung und begründen Sie jeweils: PDF-Befund, HL7-v2-Nachricht, gescanntes EKG-Bild, FHIR-Observation mit LOINC-Code, Excel-Tabelle mit gemischten Zelltypen.

?

Laut Folie 14/15 (MSI VL Einführung): Strukturierte Daten benötigen **einheitliche Datenstruktur + einheitliche Datentypen + kontrolliertes Vokabular** (Codesystem).

- **PDF-Befund** → unstrukturiert. Für das Auge lesbar, aber Computerprogramme können Einzelinformationen nicht auswerten.
- **HL7-v2-Nachricht** → strukturiert (syntaktisch). Definierte Segmente, Felder und Datentypen (z. B. PID-Felder: SI, CX, XPN, DTM, CWE laut Folie 16). Semantische Interoperabilität hängt von der Code-Befüllung ab.
- **Gescanntes EKG-Bild** → unstrukturiert. Bild, keine maschinell auswertbaren Einzelwerte.
- **FHIR-Observation mit LOINC-Code** → strukturiert + semantisch interoperabel. Datentyp (z. B. PQ = physical quantity), codierter Wert (LOINC), Einheit.
- **Excel-Tabelle mit gemischten Zelltypen** → unstrukturiert laut Folie 15. Warnung: „Nicht alles, was für das Auge strukturiert erscheint, ist auch für Computersysteme strukturiert nutzbar!"

---

Ein Projekt führt einen elektronischen Laborbefund zwischen Hausarzt und Labor ein. Welche konkreten Elemente müssen aus den drei Voraussetzungs-Bündeln für semantische Interoperabilität laut Folie 23 festgelegt werden?

?

Laut Folie 23, MSI VL Einführung:

**Inhalt & Syntax:**
- Auswahl eines Standards (z. B. HL7 FHIR oder HL7 V2.x).
- Einigung auf Struktur und Inhalt → Implementierungsleitfaden, Profil.

**Semantik:**
- Gemeinsames Informationsmodell → HL7 RIM (im PDF nur erwähnt, nicht definiert).
- Terminologien: Code-Systeme, Value Sets → z. B. LOINC für Laborparameter, UCUM für Einheiten, ICD-10 für Diagnosen.
- Eindeutige Identifikation von Objekten → OID für Codesysteme, MPI für Patienten-ID (im PDF nur erwähnt, nicht definiert).

**Organisational:**
- Gesetzliche Grundlage (z. B. ELGA-Gesetz, DSGVO).
- Gemeinsames Verständnis und Definition der Prozesse.
- → Akzeptanz!

---

Ordnen Sie folgende Szenarien den vier Anwendungsbereichen nach Lehne et al. (2019) zu: (a) Diabetes-Risiko-Modell aus EHR-Daten, (b) ePrescription Österreich–Italien, (c) Krebsregister-Auswertung über drei Häuser, (d) Krankenhaus-internes EHR ersetzt Doppeleingaben.

?

Laut Lehne et al. (2019), Fig. 1 (MSI - Interoperabilität - Anwendungsbereiche Lehne):

- **(a) Diabetes-Risiko-Modell** → **AI & Big Data**. Algorithmen brauchen strukturierte, semantisch eindeutige Eingaben. Ohne sie entstehen systematische Bias-Fehler, die wegen Datenmenge schwer detektierbar sind. Größte Hürde laut Paper: „not a lack of algorithms but a lack of suitable data."
- **(b) ePrescription AT–IT** → **International Cooperation**. Cross-Border-Datenaustausch. Laut Paper: 2019 erste Austausche von ePrescription und International Patient Summary zwischen EU-Ländern.
- **(c) Krebsregister über drei Häuser** → **Research** + evtl. **International Cooperation**. Real-world data, observational studies, federated analysis (Analyse-Skript wandert zum Datensatz).
- **(d) EHR ersetzt Doppeleingaben** → **Medical Communication**. Reduce documentation burden, enable easy information retrieval, empower patients.

---

Ordnen Sie zu und begründen Sie: (a) Laborauftrag KIS→Labor, (b) ELGA-Entlassungsbrief wird ins Repository hochgeladen, (c) Hausarzt ruft ELGA-Befund ab. Gerichtet oder ungerichtet?

?

Laut Folie 18, MSI VL Einführung:

- **(a) Laborauftrag KIS→Labor** → **gerichtet**. Sender adressiert konkreten Empfänger zum Sendezeitpunkt. Typisches Format: HL7-v2-Bestellnachricht (Folie 19).
- **(b) ELGA-Entlassungsbrief ins Repository** → **ungerichtet** (Sende-Seite). Dokument wird in Document Repository hinterlegt und in Document Registry registriert. Wer es später abruft, ist beim Hochladen unbekannt. IHE-XDS-Transaktion: „Provide and Register Document Set-b."
- **(c) Hausarzt ruft ELGA-Befund ab** → **ungerichtet** (Empfangs-Seite). Pull-Modus: Zuerst „Registry Stored Query" gegen Document Registry, dann „Retrieve Document Set" vom Document Repository (laut IHE-XDS-Architekturskizze, Folie 18).

---

### Diskussion

Warum reicht technische Interoperabilität nicht aus, um klinischen Mehrwert zu erzeugen? Welches Gegenbeispiel verwendet die Vorlesung?

?

Technische Interoperabilität sichert Übertragung, Datensicherheit, Datenintegrität und Zugriff auf den identifizierten Patienten (Folie 5, MSI VL Einführung) – aber nicht das **Verstehen** und **Handeln**. Der Anspruch lautet: „Both ends exchange, understand **and act on** the data received." Reine Übertragung erfüllt nur das erste Drittel.

**Gegenbeispiel aus der Vorlesung (Folie 25)**: Ein PDF kann technisch zwischen Systemen ausgetauscht werden. Sein Inhalt ist für Computerprogramme aber nicht strukturiert auswertbar – keine automatischen Medikamentenwarnungen, kein Verlaufsvergleich, keine Berechnung. Die Vorlesung zitiert die ÖÄK: „PDF-Müllhalde." Erst strukturierte + codierte Daten (semantische Ebene) plus gesetzlicher/prozessualer Rahmen (organisatorische Ebene) erzeugen echten Mehrwert.

---

Worin unterscheidet sich das Vier-Ebenen-Modell von Lehne et al. (2019) vom Drei-Schichten-Modell der Einführungs-Vorlesung, und was ist das Argument für die Trennung?

?

**Drei-Schichten-Modell** (Folie 5): Technical → Semantic → Organisational.
Format/Struktur der Daten ist implizit in beiden inneren Schichten verteilt.

**Vier-Ebenen-Modell Lehne** (Paper): Technical → **Syntactic** → Semantic → Organizational.
Die syntaktische Ebene ist explizit eigenständig.

**Argument für die Trennung** (MSI - Interoperabilitätsebenen - Vier-Ebenen-Modell Lehne):
- **Technical** = Übertragung A→B (Protokoll, Kanal) – laut Paper heute relativ einfach.
- **Syntactic** = Format und Struktur (z. B. XML-Schema einer FHIR-Resource, laut Paper: „HL7 FHIR defines around 140 common healthcare concepts … accessible using modern web technologies").
- **Semantic** = Bedeutung (SNOMED CT, LOINC, IDMP etc.) – FHIR liefert die Hülle, Terminologien die Bedeutung.

Schlüsselargument: Ein FHIR-Server kann syntaktisch korrekte JSON-Ressourcen liefern, deren `code`-Felder aber Freitext enthalten → syntaktisch OK, semantisch nicht interoperabel. Die Trennung macht diesen Unterschied sichtbar.

---

Welche vier Kategorien von Gründen nennen Benson/Grieve dafür, dass Interoperabilität schwer ist? Welche wird durch sehr gute Standards am stärksten reduziert, welche bleibt am stabilsten?

?

Laut Folie 24 (MSI VL Einführung, Quelle: Benson and Grieve, *Principles of Health Interoperability*):

1. **Bit-perfect**: Computers work by matching strings. Need for perfection. Specifications must be stringent.
2. **Translation issues**: Computers store data in different ways. Double translation (A→wire format→B). Need for a standard interchange language.
3. **Developers**: Each system speaks its own language. Lack domain knowledge. Developers and users fail to understand each other.
4. **Users**: Each specialty speaks its own dialect. Users won't commit to requirements. Users keep asking for changes.

**Diskussionsfrage – keine eindeutige Antwort im Vorlesungsmaterial; Argumentation:**
- Durch gute Standards (z. B. FHIR + Profile) **am stärksten reduziert**: Translation issues – ein gemeinsames Austauschformat beseitigt das Double-Translation-Problem. Auch Bit-perfect wird adressiert: präzise Spezifikationen (Profiles, Schemavalidierung) reduzieren Matching-Fehler.
- **Am stabilsten bleibend**: Users – Standards adressieren technische Spezifikationen, nicht das Problem, dass klinische Fachgruppen unterschiedliche Dialekte sprechen und Anforderungen schwer festzulegen sind.

---

### Vergleich

Wie verhalten sich die vier Layer von Benson/Grieve (Technology, Data, Human, Institutional) zum Drei-Schichten-Modell? Wo liegt der wesentliche Unterschied?

?

Laut Folie 6 (MSI VL Einführung):

| Benson/Grieve Layer | Entsprechung im Drei-Schichten-Modell | Stichworte |
|---|---|---|
| **Technology** | Technical | HL7 v2/v3/CDA/FHIR, APIs, Interchange formats |
| **Data** | Semantic | SNOMED CT, Identifiers and Codes, Exchange meaning |
| **Human** | Teil von Organisational | Process Interoperability, Clinical Interoperability, Business processes |
| **Institutional** | Teil von Organisational | Role of Government, Culture, Incentives, Education, Regulation, Information governance |

**Wesentlicher Unterschied**: Im Drei-Schichten-Modell sind Human und Institutional gemeinsam unter „Organisational" gebündelt. Benson/Grieve trennt die **prozessuale/klinische Ebene** (Human) von der **institutionell-regulatorischen Rahmensetzung** (Institutional). Beide Modelle sind laut Vorlesung komplementär – keines wird als „richtiger" ausgezeichnet (Folie 6).

---

Welche vier Hauptnutzen-Kategorien von Standards listet Benson/Grieve? Erklären Sie den „Multiplier Effect" und den „Vendor Lock-in"-Aspekt und nennen Sie den Trade-off der Vorlesung.

?

Laut Folie 9 und Folie 12 (Mindmap, Quelle Benson/Grieve):

1. **Multiplier Effect**: „More use → more benefits." Erstaufwand für Standard-Implementierung evtl. höher, aber jeder weitere Einsatz erhöht den Nutzen (Netzwerk-Logik, nicht Stückkostendegression).
2. **Avoid supplier lock-in**: Standards ermöglichen Wahl, Wettbewerb, Flexibilität, Migration. Ohne offene Standards: Daten „gefangen in einem Silo" – laut Folie 9 „fatal z. B. bei Millionen ELGA-Befunden pro Jahr."
3. **Reduce costs**: Kostensenkung durch Wiederverwendung und Wettbewerb.
4. **Minimise risk**: Risikominimierung bei der Implementierung.

**Trade-off** (Folie 11): Auf den Einwand „Ein Standard schränkt mich ein" antwortet die Vorlesung: Im Idealfall helfen Standards, eine Herausforderung schneller zu verstehen und zu lösen. Kritisch bleibt: Reihenfolge ist entscheidend – nicht zuerst das Problem lösen und dann Standards implementieren (führt zu großem Aufwand), sondern zuerst Standards verstehen.

---

## Mögliche Anschlussfragen des Prüfers

- „Sie haben erklärt, was semantische Interoperabilität ist – welche konkreten Standards decken welche Ebene des Drei-Schichten-Modells ab?"
- „Ordnen Sie SNOMED CT, HL7 FHIR, ein nationales eHealth-Gesetz und ein Schulungsprogramm für Ärzte dem richtigen Benson/Grieve-Layer zu."
- „Was ist der Unterschied zwischen einem Standard und einem Profil/Implementierungsleitfaden?"
- „An welchen Übergängen der DIKW-Pyramide setzt semantische Interoperabilität an – und was verhindert diesen Übergang in der Praxis?"
- „Warum reicht ‚more data' allein nicht für KI im Gesundheitswesen? Was braucht ein ML-Algorithmus stattdessen?"
- „Beschreiben Sie eine Situation, in der technische und semantische Interoperabilität erfüllt sind, die Lösung aber an der organisatorischen Ebene scheitert."
- „Was meint die Vorlesung mit ‚Akzeptanz' als organisatorische Voraussetzung – ist das dasselbe wie ‚rechtlich erlaubt'?"
- „Wie trägt federated analysis dazu bei, die Spannung zwischen Datenschutz und Forschungs-Interoperabilität aufzulösen?"

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
