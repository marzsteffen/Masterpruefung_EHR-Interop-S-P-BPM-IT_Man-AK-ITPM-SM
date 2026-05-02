---
typ: konzept
status: offen
faecher: [msi, ehr]
quellen:
  - "[[MSI - HL7 CDA - Definition]]"
  - "[[MSI - HL7 CDA - Aufbau]]"
  - "[[MSI - HL7 CDA - Eigenschaften]]"
  - "[[MSI - HL7 CDA - Levels]]"
  - "[[MSI - HL7 FHIR - Definition]]"
  - "[[MSI - HL7 FHIR - Versionen]]"
  - "[[MSI - HL7 FHIR - Paradigmen]]"
  - "[[MSI - HL7 FHIR - Ressource Aufbau]]"
  - "[[MSI - HL7 FHIR - Bundle]]"
  - "[[MSI - HL7 FHIR - REST API]]"
  - "[[MSI - HL7 FHIR - Profil]]"
  - "[[MSI - HL7 FHIR - Implementation Guide]]"
  - "[[MSI - Datenaustausch - Formen]]"
  - "[[MSI - HL7 - International Patient Summary]]"
  - "[[EHR - HL7 CDA - RIM-Basis]]"
  - "[[EHR - HL7 CDA - Levels 1 2 3]]"
  - "[[EHR - CCR - Continuity of Care Record]]"
  - "[[EHR - CCD - Continuity of Care Document]]"
  - "[[EHR - C-CDA - Consolidated CDA]]"
  - "[[EHR - HL7 FHIR - 5 Levels]]"
  - "[[EHR - FHIR - Motivation]]"
  - "[[EHR - FHIR - Resource]]"
  - "[[EHR - FHIR - Bundles Document und Message]]"
  - "[[EHR - FHIR - 6 Exchange Paradigms]]"
  - "[[EHR - FHIR - Profiles und Must Support]]"
  - "[[EHR - FHIR - Implementation Guides]]"
tags:
  - typ/konzept
  - status/offen
  - cross-fach
  - fach/allgemein/msi
  - fach/allgemein/ehr
---

# Cross - HL7 FHIR und CDA in MSI vs EHR

> [!info] Kurzdefinition
> HL7 CDA und HL7 FHIR werden in beiden Fächern behandelt, aber aus unterschiedlichen Blickwinkeln. MSI betrachtet die Standards als *Standard-Mechanik* (Spezifikation, RIM-Bezug, Profile, IGs, Versionierung); EHR betrachtet sie als *Anwendungs-Werkzeug* (Motivation, CCR/CCD/C-CDA, Meaningful Use, Exchange Paradigms). In der mündlichen Prüfung tritt die Brücke immer dann auf, wenn ein klinischer Anwendungsfall in eine Standard-Frage kippt – oder umgekehrt.

## Sicht aus Fach MSI

MSI behandelt CDA und FHIR als **Standard-Familie**, mit Fokus auf das, was die Standards selbst spezifizieren.

**CDA – die Standard-Sicht:**

- Definition: ISO/HL7 27932:2009, Teil von HL7 V3, basiert auf RIM (ISO/HL7 21731:2006) — siehe [[MSI - HL7 CDA - Definition]]. Eigene Refinement-Sicht des RIM = R-MIM.
- Sechs definierende **Eigenschaften** (Folie 11): Persistenz, Verwaltung (stewardship), Kontext, Authentisierung, Ganzheit (wholeness), Lesbarkeit (human readability) — siehe [[MSI - HL7 CDA - Eigenschaften]]. Diese sind Voraussetzung dafür, dass ein Dokument als „medizinisches Dokument" im Sinne von CDA gilt.
- Aufbau: `<ClinicalDocument>` → Header (Patient, GDA, Erstellungsdatum, Custodian, Authenticator) + Body → Section (mit `<text>` Narrative Block + Entries als Clinical Statements) — siehe [[MSI - HL7 CDA - Aufbau]].
- **CDA-Levels** (Folie 14, wörtlich): Level 1 = `nonXMLBody` (PDF/Text/Bild, nur Header maschinenlesbar); Level 2 = Section-strukturierter Body mit Section-Codes; Level 3 = Entry-strukturierter Body mit codierten Einzelinformationen — siehe [[MSI - HL7 CDA - Levels]]. Explizite Warnung: „CDA-Level ≠ ELGA-EIS-Stufe".
- Praxis-Schichten in der MSI-Vorlesung: Templates, ART-DECOR, Implementierungsleitfäden, Stylesheet/Validierung, Kardinalität/Konformität, codierte Werte, Terminology Binding, nullFlavor.

**FHIR – die Standard-Sicht:**

- Definition: Fast Healthcare Interoperability Resources, entwicklerorientiert, REST/JSON/XML, 80/20-Regel — siehe [[MSI - HL7 FHIR - Definition]].
- **Versionierung**: ~18-Monats-Zyklus, R5 aktuell, **ab R4 normative Ressourcen** (abwärtskompatibel) — siehe [[MSI - HL7 FHIR - Versionen]]. FHIR Maturity Model (FMM) pro Ressource.
- Vier **Paradigmen** des Datenaustauschs im Gesundheitswesen (Folien 3–5, 9–10): Nachrichtenbasiert (HL7 v2), Dokumentenbasiert (HL7 CDA), Anwendungsspezifisch (DICOM, CCD), Ressourcenbasiert (FHIR) — siehe [[MSI - HL7 FHIR - Paradigmen]] und [[MSI - Datenaustausch - Formen]].
- Ressource: `Resource` (technisch, nicht erweiterbar) vs. `DomainResource` (mit `text` / `contained` / `extension`, erweiterbar) — siehe [[MSI - HL7 FHIR - Ressource Aufbau]]. Explizit benannte Inversion zu CDA: „In FHIR sind strukturierte Daten primär; der Narrative-Text ist ein Pflicht-Ergänzungsfeld."
- Bundle: Container-Ressource mit Typ-Feld (`document`, `message`, `transaction`, `transaction-response`, `batch`, `searchset`, `collection`, `history`) — siehe [[MSI - HL7 FHIR - Bundle]]. Strukturelle Bundle-Definition im PDF nicht ausgeführt, als „Ergänzung außerhalb der Vorlesung" markiert.
- REST API: HTTP-Methoden + URL-Pattern, JSON vs. XML via `_format` oder `Accept`-Header, History (`_history`), `DELETE` ist logisch — siehe [[MSI - HL7 FHIR - REST API]].
- Profilierung: StructureDefinition, kann Kardinalitäten verschärfen, Felder verbieten, Extensions hinzufügen, Bindings verstärken, Slicing — siehe [[MSI - HL7 FHIR - Profil]]. Kernaussage: **„FHIR Server ≠ Interoperabilität"** — erst Profilierung schafft echte Interoperabilität.
- Implementation Guide: Bündelt Profile + ValueSets + ConceptMaps + Beispiele — siehe [[MSI - HL7 FHIR - Implementation Guide]]. Differential Table vs. Snapshot Table (im PDF nur als Frage gestellt).
- IPS: HL7 + CEN, grenzüberschreitender EU-Use-Case 2019 — siehe [[MSI - HL7 - International Patient Summary]].

## Sicht aus Fach EHR

EHR behandelt CDA und FHIR als **Werkzeuge in einer Anwendungs-Architektur**, eingebettet in den US-Meaningful-Use-Kontext und die Care-Transition-Praxis.

**CDA – die Anwendungs-Sicht:**

- RIM-Bezug ist der zentrale Hebel: „Each XML-element in a CDA document must correspond to a RIM class or class attribute" — siehe [[EHR - HL7 CDA - RIM-Basis]]. RIM-Hauptklassen: Act, Entity, Role, Participation, ActRelationship.
- **CDA-Levels** als kumulatives Strukturierungsmodell mit explizitem Bezug zu LCIM (Tolk): Level 1 ↔ Technical Integration, Level 2 ↔ + Section-Semantik, Level 3 ↔ Syntax & Semantics — siehe [[EHR - HL7 CDA - Levels 1 2 3]]. Die Note räumt explizit ein, dass die Level-Stufung in der EHR-Vorlesung nicht behandelt wurde und als externe Ergänzung markiert ist.
- **CCR** (ASTM E2369-12): Inhalts-Spezifikation für eine kompakte Versorgungs-Zusammenfassung mit 6 mandated core sections (Provider Info, Patient Identifying Info, Insurance and Financial Info, Patient's Health Status, Care Documentation, Care Plan Recommendation) — siehe [[EHR - CCR - Continuity of Care Record]]. „Fading out" zugunsten von CCD.
- **CCD**: HL7-CDA-Implementation des CCR. Selber Inhalt, anderes Format. In **MU Stage 1** als bevorzugter Exchange-Standard — siehe [[EHR - CCD - Continuity of Care Document]].
- **C-CDA**: Konsolidierung von neun CDA-Dokumenttypen (CCD, Consultation Note, Diagnostic Imaging Report, Discharge Summary, H&P, Operative Note, Procedure Note, Progress Note, Unstructured Document). In **MU Stage 2** verpflichtend für Care Transitions — siehe [[EHR - C-CDA - Consolidated CDA]].

**FHIR – die Anwendungs-Sicht:**

- **Motivation**: CDA hat steile Lernkurve, RIM-Komplexität; HL7 v3 Messaging kaum genutzt; HL7 v2 weit verbreitet aber alt; keine Unterstützung für verteilte Daten; ältere Spezifikationen teils kostenpflichtig — siehe [[EHR - FHIR - Motivation]]. Konkretes Problem: Blutdruckmessung in Graz ↔ Innsbruck — wie kombinieren? FHIR-Antwort: References per URL. Marktdruck: 75 % der Digital-Health-Companies (Folie 2).
- **5 FHIR-Levels** als Spezifikations-Schichtmodell (laut hl7.org/fhir): Foundation → Conformance → Master Data → Operational Data → Knowledge — siehe [[EHR - HL7 FHIR - 5 Levels]]. Zweck: zeigt, dass FHIR von Encoding bis Wissens-Sharing alles abdeckt.
- Resource als „Atom des Health-Information-Exchange", `resourceType`-Pflichtfeld, Anzahl bewusst begrenzt — siehe [[EHR - FHIR - Resource]].
- Bundles als Document/Message-Pattern: **die erste Resource definiert den Charakter** (Composition → Document, MessageHeader → Message). Documents sind immutable und signierbar — siehe [[EHR - FHIR - Bundles Document und Message]]. Konkrete IG-Beispiele: Indien (NDHM Discharge Summary), Saudi-Arabien (Nphies Messaging).
- **6 Exchange Paradigms** (Folie 76, Verweis auf build.fhir.org/exchange-module.html): REST, Documents, Messaging, Services, Database/Persistence, Subscription — siehe [[EHR - FHIR - 6 Exchange Paradigms]].
- Profile + **Must Support vs. Mandatory**: Mandatory = `min ≥ 1` (Pflicht-Wert), Must Support = System muss Verarbeitung beherrschen, Wert kann fehlen — siehe [[EHR - FHIR - Profiles und Must Support]]. US-Core-Beispiel mit Race/Ethnicity-Extensions.
- Implementation Guides als praxisorientiertes Bundle: Profiles + Examples + Exchange Paradigm + Documentation — siehe [[EHR - FHIR - Implementation Guides]]. Konkrete IGs: US Core, AT Core, NDHM, Nphies.

## Gemeinsamkeiten

| Konzept | Beide Fächer sagen … |
|---|---|
| CDA-Verankerung | XML-Format, basiert auf RIM, Header + Body, Sections mit Narrative + Entries |
| CDA-Levels (1/2/3) | Body-Strukturierung von rein narrativ (1) → Sections mit Codes (2) → Entries mit codierten Einzelinformationen (3) |
| FHIR-Definition | Ressourcen-orientiert, REST/JSON/XML, entwicklerfreundlich, 80/20-Regel als Designprinzip |
| FHIR-Resource-Begriff | Atomare Einheit; FHIR hält Resource-Anzahl bewusst begrenzt |
| FHIR-Bundle-Pattern | Bundle als Container mehrerer Ressourcen; Document-Bundle ↔ CDA-funktional ähnlich; signierbar/immutable |
| Profilierung als Notwendigkeit | Beide stellen klar: roher Standard reicht nicht — erst Profile/IG schaffen Interoperabilität |
| IG-Begriff | Bundle aus Profilen + Beispielen + Bindings + Doku |

## Unterschiede / Konflikte / unterschiedliche Schwerpunkte

**1. Begriffs-Konflikt: „Paradigma".**
Das ist der wichtigste Cross-Fach-Befund. Beide Fächer benutzen das Wort, meinen aber zwei verschiedene Dinge:

- **MSI** (siehe [[MSI - HL7 FHIR - Paradigmen]]): „Paradigma" = übergeordnete Datenaustausch-Kategorie im Gesundheitswesen. Vier Stück: Nachrichten (HL7 v2), Dokumente (HL7 CDA), Anwendungsspezifisch (DICOM, CCD), Ressourcen (HL7 FHIR). Der Begriff ordnet ganze Standards ein.
- **EHR** (siehe [[EHR - FHIR - 6 Exchange Paradigms]]): „Exchange Paradigm" = Austausch-Modus *innerhalb* von FHIR. Sechs Stück: REST, Documents, Messaging, Services, Database/Persistence, Subscription. Der Begriff beschreibt, wie FHIR-Ressourcen genutzt werden.

In einer mündlichen Antwort beide Bedeutungen zu mischen, wäre falsch. Korrekt: MSI's vier Paradigmen sind die *Klassen* des Datenaustauschs, EHR's sechs Paradigmen sind die *Modi*, in denen FHIR genutzt werden kann.

**2. Begriffs-Doppelbelegung „Levels".** Drei verschiedene Konzepte tragen den Namen Level:
- CDA-Level 1/2/3 = Body-Strukturierung (in beiden Fächern; siehe [[MSI - HL7 CDA - Levels]] und [[EHR - HL7 CDA - Levels 1 2 3]]).
- FHIR Maturity Level (FMM) = Reifegrad pro Ressource (nur in MSI explizit; [[MSI - HL7 FHIR - Versionen]]).
- HL7 FHIR 5 Levels (Foundation/Conformance/Master Data/Operational Data/Knowledge) = Spezifikations-Schichtmodell (nur in EHR explizit; [[EHR - HL7 FHIR - 5 Levels]]).

Die EHR-Note warnt selbst: „Auch nicht zu verwechseln mit den LCIM nach Tolk" — sie beachtet die Doppelbelegung, ohne sie aufzulösen.

**3. CDA-Eigenschaften (Folie 11).** Die sechs definierenden Eigenschaften (Persistenz, Verwaltung, Kontext, Authentisierung, Ganzheit, Lesbarkeit) sind **nur in MSI** ausgeführt — siehe [[MSI - HL7 CDA - Eigenschaften]]. EHR hat dazu keine eigene Note. Wer die Frage „Was definiert ein CDA-Dokument?" bekommt, antwortet aus MSI heraus.

**4. CCR/CCD/C-CDA.** Diese Konzepte existieren **nur in EHR** ([[EHR - CCR - Continuity of Care Record]], [[EHR - CCD - Continuity of Care Document]], [[EHR - C-CDA - Consolidated CDA]]). MSI hat keine Notes dazu — der ELGA-Vergleich liegt in [[MSI - ELGA - EIS Stufen]] und [[MSI - HL7 CDA - Implementierungsleitfäden]] auf einer anderen Ebene.

**5. Schwerpunkt der RIM-Behandlung.** MSI hat eigene Notes für [[MSI - HL7 RIM - Reference Information Model]] und [[MSI - HL7 CDA - R-MIM]] — also RIM als allgemeines V3-Datenmodell, dann CDA-spezifische Refinement-Sicht. EHR fasst beides in [[EHR - HL7 CDA - RIM-Basis]] zusammen, mit Fokus auf die fünf Hauptklassen Act/Entity/Role/Participation/ActRelationship.

**6. CDA-Levels-Quelltreue.**
- MSI zitiert Folie 14 wörtlich; die Level-Stufung ist Teil des Vorlesungsstoffs.
- EHR markiert die Level-Stufung explizit als „Ergänzung außerhalb der Vorlesung" — die EHR-Vorlesung führt CDA + RIM ein, aber nicht die Level.

Konsequenz für die Prüfung: Wenn der Prüfer „in welcher Vorlesung wurde das gelehrt" prüft, ist die Antwort „aus MSI / HL7 CDA und e-Befunde, Folie 14".

**7. FHIR-Bundle-Vollständigkeit.** MSI listet `transaction-response` als zusätzlichen Bundle-Typ; EHR listet ihn nicht. EHR betont dafür stärker, dass die erste Resource den Charakter (Document vs. Message) bestimmt und dass Document-Bundles immutable und signierbar sind.

**8. Profilierung – Must Support.** Die Mandatory/Must-Support-Distinktion ist **nur in EHR** als eigenes Thema ausgeführt — siehe [[EHR - FHIR - Profiles und Must Support]]. MSI's [[MSI - HL7 FHIR - Profil]] erwähnt die Verschärfung von Kardinalitäten, aber nicht die Must-Support-Marker-Logik.

**9. Differential vs. Snapshot Table.** MSI thematisiert die Frage explizit (PDF stellt sie als Selbststudium-Aufgabe, im PDF nicht beantwortet — siehe [[MSI - HL7 FHIR - Implementation Guide]]). EHR-IG-Note erwähnt es nicht.

## Synthese für die mündliche Prüfung

**Diskussions-Achse 1: „Wann CDA, wann FHIR?"**
Die Antwort braucht beide Fächer. Aus MSI das Paradigmen-Argument: CDA ist dokumentenbasiert (statisch, signiert, narrativ), FHIR ist ressourcenbasiert (granular, REST-fähig, verteilte Daten). Aus EHR das Migrations-Argument: FHIR ist die Antwort auf konkrete Probleme älterer Standards (verteilte Messungen, fehlende Entwicklerfreundlichkeit). Sauber abschließen mit der „beide existieren parallel"-Aussage aus EHR-Motivation und MSI-Definition: ein FHIR Document Bundle bildet CDA-Funktionalität ab, ohne CDA zu ersetzen.

**Diskussions-Achse 2: „Reicht der Standard?"**
Beide Fächer geben dieselbe Antwort, mit unterschiedlichem Schärfegrad. MSI: „FHIR Server ≠ Interoperabilität" (wörtlich aus [[MSI - HL7 FHIR - Profil]]). EHR: „Without IG, FHIR is not productively usable" (sinngemäß aus [[EHR - FHIR - Implementation Guides]]). Die Cross-Fach-Pointe: erst Profile + IG schaffen Interoperabilität; dasselbe gilt für CDA (Templates, ART-DECOR, ELGA-Leitfäden).

**Diskussions-Achse 3: „CDA-Level vs. ELGA-EIS-Stufe vs. FHIR-5-Levels."**
Klassische Verwechslungsfalle. CDA-Level = Body-Strukturierung. EIS-Stufe = ELGA-Konformitäts-Klassifikation. FHIR-5-Levels = Spezifikations-Schichten. In einer Antwort sauber trennen — MSI's Warnung „CDA-Level ≠ ELGA-EIS-Stufe" zitieren, EHR's „nicht mit LCIM verwechseln" ergänzen.

**Diskussions-Achse 4: „CCD/C-CDA als Brücke zwischen Standard und Anwendung."**
CCR ist Inhalts-Spezifikation (ASTM), CCD ist die HL7-CDA-Implementation davon, C-CDA ist die Konsolidierung von neun Dokumenttypen — alle in EHR aus Meaningful Use heraus motiviert. In MSI gibt es das nicht. Wer hier antwortet, antwortet aus EHR. Die saubere Brücke: CDA (MSI-Standard-Sicht) liefert die Mechanik, CCD/C-CDA (EHR-Anwendungs-Sicht) liefert den konkreten Use-Case.

**Diskussions-Achse 5: „Was sagt MSI über IPS, was sagt EHR?"**
IPS ist nur in MSI ausgeführt ([[MSI - HL7 - International Patient Summary]]) — Träger HL7 + CEN, grenzüberschreitender EU-Anwendungsfall. EHR-Side: kein eigener IPS-Note, aber EHDS-Bezug in [[EHR - EHDS - European Health Data Space]]. Die Brücke: IPS ist die Spezifikation, EHDS ist der politisch-rechtliche Rahmen, ELGA ist die nationale Realisierung. (Letzter Punkt aus den jeweiligen Notes; nicht harmonisierend übermalen, dass EHR-Seite ohne IPS-Note keine eigene IPS-Aussage hat.)

**Anschlussfragen, die ohne Cross-Fach-Verständnis schwer zu beantworten sind:**

- „Was bedeutet ‚Paradigma' im Kontext von HL7?" → muss MSI's Vier-Klassen-Sicht *und* EHR's Sechs-Modus-Sicht kennen, sonst Verwechslungsgefahr.
- „Wenn ich im EHR-Kontext über CDA-Levels rede, ist das dasselbe wie ELGA-EIS-Stufen?" → MSI's explizite Trennung.
- „Welche FHIR-Version ist normativ, und seit wann?" → R4, mit abwärtskompatiblen normativen Ressourcen, MSI-Quelle.
- „Mandatory oder Must Support — wo ist der Unterschied in der Sender/Empfänger-Pflicht?" → EHR-Quelle.
- „Wie würde man ein C-CDA-Dokument in FHIR überführen?" → MSI's Bundle-Mechanik + EHR's Document-Bundle-Pattern + die Erkenntnis, dass das funktional äquivalent, strukturell verschieden ist.

## Verwandt

**MSI:**
- [[MSI - HL7 CDA - Definition]]
- [[MSI - HL7 CDA - Aufbau]]
- [[MSI - HL7 CDA - Eigenschaften]]
- [[MSI - HL7 CDA - Levels]]
- [[MSI - HL7 FHIR - Definition]]
- [[MSI - HL7 FHIR - Versionen]]
- [[MSI - HL7 FHIR - Paradigmen]]
- [[MSI - HL7 FHIR - Ressource Aufbau]]
- [[MSI - HL7 FHIR - Bundle]]
- [[MSI - HL7 FHIR - REST API]]
- [[MSI - HL7 FHIR - Profil]]
- [[MSI - HL7 FHIR - Implementation Guide]]
- [[MSI - Datenaustausch - Formen]]
- [[MSI - HL7 - International Patient Summary]]
- [[MSI - ELGA - EIS Stufen]]

**EHR:**
- [[EHR - HL7 CDA - RIM-Basis]]
- [[EHR - HL7 CDA - Levels 1 2 3]]
- [[EHR - CCR - Continuity of Care Record]]
- [[EHR - CCD - Continuity of Care Document]]
- [[EHR - C-CDA - Consolidated CDA]]
- [[EHR - HL7 FHIR - 5 Levels]]
- [[EHR - FHIR - Motivation]]
- [[EHR - FHIR - Resource]]
- [[EHR - FHIR - Bundles Document und Message]]
- [[EHR - FHIR - 6 Exchange Paradigms]]
- [[EHR - FHIR - Profiles und Must Support]]
- [[EHR - FHIR - Implementation Guides]]

**MOCs:**
- [[MSI - MOC]]
- [[EHR - MOC]]

## Quelle

Cross-Fach-Synthese aus den oben gelisteten MSI- und EHR-Konzept-Notes. Keine externen Ergänzungen außerhalb der Vault-Quellen. Inhalts-Konflikte (insbesondere die Doppelbelegung „Paradigma" und „Levels") sind aus den jeweiligen Notes wörtlich entnommen, nicht synthetisch erzeugt.

**Fach-Zuordnung der Quellen:**

| Note | Fach |
|---|---|
| MSI - HL7 CDA - Definition / Aufbau / Eigenschaften / Levels | MSI |
| MSI - HL7 FHIR - Definition / Versionen / Paradigmen / Ressource Aufbau / Bundle / REST API / Profil / Implementation Guide | MSI |
| MSI - Datenaustausch - Formen, MSI - HL7 - International Patient Summary | MSI |
| EHR - HL7 CDA - RIM-Basis / Levels 1 2 3 | EHR |
| EHR - CCR / CCD / C-CDA | EHR |
| EHR - HL7 FHIR - 5 Levels, EHR - FHIR - Motivation / Resource / Bundles Document und Message / 6 Exchange Paradigms / Profiles und Must Support / Implementation Guides | EHR |
