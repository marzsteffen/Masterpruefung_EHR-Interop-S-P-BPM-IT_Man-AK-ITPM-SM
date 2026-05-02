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

# MSI - PF - HL7 FHIR Terminologie

## Kontext

Tiefenkarte zum FHIR Terminology Framework. Abgedeckt: vier Bausteine (CodeSystem, ValueSet, ConceptMap, Terminology Service), codierte Datentypen (code, Coding, CodeableConcept, Quantity), Binding Strengths (required/extensible/preferred/example), ValueSet-Struktur (compose vs. expansion, intensional vs. extensional), ConceptMap-Äquivalenztypen, die vier Operationen des FHIR Terminology Service ($expand, $lookup, $validate-code, $translate) und IHE-SVCM-Zuordnung. Ergänzend: [[MSI - PF - Terminologieserver]] (Dreischichten-Architektur), [[MSI - PF - Terminologien und Klassifikationen]] (Konzepte und Mapping), [[MSI - PF - HL7 CDA Detail]] (CDA-Terminologievergleich).

## Verlinkte Konzepte

- [[MSI - HL7 FHIR - Terminology Framework]]
- [[MSI - HL7 FHIR - Codierte Elemente Übersicht]]
- [[MSI - HL7 FHIR - Datentyp code]]
- [[MSI - HL7 FHIR - Datentyp Coding]]
- [[MSI - HL7 FHIR - Datentyp CodeableConcept]]
- [[MSI - HL7 FHIR - Terminology Binding Strength]]
- [[MSI - HL7 FHIR - CodeSystem Resource]]
- [[MSI - HL7 FHIR - ValueSet Resource]]
- [[MSI - HL7 FHIR - ConceptMap Resource]]
- [[MSI - HL7 FHIR - Terminology Service]]

---

## Karten

### Definition

Beschreiben Sie das FHIR Terminology Framework. Welche vier Bausteine gehören dazu und wie interagieren sie?

?

Das FHIR Terminology Framework beschreibt das kohärente Zusammenspiel der Terminologie-Bausteine für semantische Interoperabilität.

**Vier Bausteine (vier Schichten):**

1. **CodeSystem** — Terminologie-Quelle: definiert Konzepte mit Code, Bedeutung, Display, Hierarchien, Properties und Namensraum (URI). Beispiele: LOINC, ICD-10, SNOMED CT.

2. **ValueSet** — Auswahl und Kontextualisierung: wählt Codes aus einem oder mehreren CodeSystems für einen bestimmten Verwendungskontext. Kann intensional (Regeln) oder extensional (Aufzählung) definiert sein.

3. **ConceptMap** — Verknüpfung: unidirektionales Mapping zwischen zwei ValueSets oder CodeSystems mit definierten Äquivalenztypen.

4. **Terminology Service** — Operationen zur Laufzeitnutzung:
   - `$expand` → Expansion eines ValueSets
   - `$lookup` → Details zu einem Code
   - `$validate-code` → Gültigkeit eines Codes im ValueSet
   - `$translate` → Übersetzung via ConceptMap

**Einbettung in Ressourcen**: über die Datentypen `code`, `Coding`, `CodeableConcept` + Terminology Binding mit Binding Strength.

---

Welche vier Datentypen für codierte Werte kennt FHIR? Wann verwendet man welchen?

?

| Datentyp | Art | Wann verwenden | Beispiel |
|---|---|---|---|
| **code** | Primitiv | Feste FHIR-Spec-Werte, required Binding, Codesystem implizit | `gender: "male"`, `Bundle.type: "document"` |
| **Coding** | Komplex | Einzelner externer Code mit explizitem system/code/display; selten direkt, meist im CodeableConcept | LOINC `55423-8` |
| **CodeableConcept** | Komplex | Mehrere Codings desselben Konzepts + optionaler Freitext; Standard für medizinische Diagnosen/Codes | ICD-10 + SNOMED + `text` |
| **Quantity** | Komplex | Messwert mit Einheit und Code (UCUM); kein reiner Codierungstyp | `3 capsules`, `55 mg/dL` |

**Entscheidungsregel**:
- `code` → wenn das Binding required ist und das Codesystem durch die Spec fixiert ist
- `Coding` → wenn ein einzelner externer Code mit vollständiger System-Angabe gebraucht wird
- `CodeableConcept` → wenn Mehrfach-Codierung, Freitext oder extensible/preferred Binding

**Warum FHIR URI statt OID?** FHIR identifiziert CodeSystems primär via URI (`http://loinc.org`), nicht OID. OIDs existieren als `identifier`-Feld für Kompatibilität mit CDA/HL7 v3.

---

Welche fünf Binding Strengths kennt FHIR (inkl. kein Binding)? Was sagt jede für die Implementierung aus?

?

| Strength | Konformitätspflicht | Bedeutung |
|---|---|---|
| **required** | SHALL aus dem ValueSet | Strikt — kein Abweichen erlaubt. Für international invariante Vokabulare (z. B. `Patient.gender`) |
| **extensible** | SHALL aus dem ValueSet, WENN ein passender Code existiert; sonst alternate codings/text | Wenn kein Code passt, darf man abweichen. Standard für „normalerweise reicht das ValueSet" (z. B. `Patient.maritalStatus`) |
| **preferred** | Empfehlung — keine Konformitätspflicht | Hilfreich für Interoperabilität, aber lokale Variation erwartet (z. B. `Patient.communication.language`) |
| **example** | Informativ — kein Konformitätsziel | Nur Hinweis auf den Typ der Codes. Implementierung definiert eigenes ValueSet (z. B. `Observation.code` auf LOINC) |
| **(kein Binding)** | Vollständig frei | Kein ValueSet angegeben — alles erlaubt |

**Konsequenz für Praxis (Benson & Grieve):**
> „It is amazing how often everyone agrees that a coded element is essential for exchange, but there is no prospect of agreeing to a value set for said exchange."

→ Viele FHIR-Basisbindings sind nur `example` oder `preferred`. **Nationale Interoperabilität entsteht erst durch Profilierung** (z. B. AT Core Profile, ELGA FHIR IG), die Bindings auf `required` oder `extensible` hochsetzt.

---

Was ist eine FHIR-CodeSystem-Resource? Nennen Sie die wichtigsten Bestandteile. Was ist ein CodeSystem-Supplement?

?

**CodeSystem-Resource** (DomainResource): definiert ein Codesystem mit allen seinen Konzepten.

**Wichtigste Bestandteile:**
- `url` (canonical URI, z. B. `http://loinc.org`) — primärer Identifikator
- `identifier` — optional, für OID-Mapping zu CDA/v3
- `version`, `status` (active/retired/draft)
- `caseSensitive` — Groß-/Kleinschreibung relevant?
- `hierarchyMeaning` — Bedeutung der Hierarchie (is-a, part-of, …)
- `compositional` — unterstützt Postkoordination?
- `content` — complete / fragment / supplement
- `concept[0..*]` — ConceptDefinition mit `code`, `display`, `definition`, rekursiv für Hierarchie, `designation` (Sprachvarianten), `property`-Werte

**CodeSystem-Supplement:**
Ergänzt ein bestehendes Codesystem ohne es zu ändern:
- Zusätzliche (lokale) Codes als nationale Erweiterungen
- Zusätzliche Display-Values (z. B. deutsche Übersetzung eines internationalen CodeSystems)
- Zusätzliche Properties (lokale Annotationen)

**Historisch**: In FHIR STU2 war CodeSystem keine eigenständige Ressource — Codes mussten immer einem ValueSet zugeordnet sein. Ab STU3 ist CodeSystem vollständig eigenständig.

---

### Anwendung

Welche Felder hat ein `Coding`-Element? Welche sind Pflicht? Was bedeutet `userSelected`?

?

| Feld | Datentyp | Kard. | Bedeutung |
|---|---|---|---|
| `system` | uri | 0..1 | Namensraum des Codesystems, z. B. `http://loinc.org` |
| `version` | string | 0..1 | Version des Codesystems, falls relevant |
| `code` | code | 0..1 | Der Code-Wert |
| `display` | string | 0..1 | Lesbarer Anzeigename aus dem Codesystem |
| `userSelected` | boolean | 0..1 | Wurde dieses Coding direkt vom Anwender ausgewählt? |

**Kein Pflichtfeld** — alle 0..1. In der Praxis: `system` + `code` sind das Minimum für sinnvolle Verwendung.

**userSelected:**
In einem `CodeableConcept` mit mehreren `Coding`-Einträgen (z. B. ICD-10 + SNOMED für dieselbe Diagnose) markiert `userSelected: true` an genau einem Coding denjenigen Code, den der Anwender aktiv gewählt hat. Die anderen Codings sind Alternativen/Cross-Mappings.

```json
{
  "system": "http://loinc.org",
  "version": "2.62",
  "code": "55423-8",
  "display": "Number of steps in unspecified time Pedometer",
  "userSelected": true
}
```

---

Wie codieren Sie eine Diagnose mit ICD-10 und SNOMED CT gleichzeitig in FHIR? Was ist der Unterschied zwischen `Coding.display` und `CodeableConcept.text`?

?

**Mehrfach-Codierung via CodeableConcept:**
```json
{
  "code": {
    "coding": [
      {
        "system": "http://hl7.org/fhir/sid/icd-10",
        "code": "M54.9",
        "display": "Rückenschmerzen, nicht näher bezeichnet"
      },
      {
        "system": "http://snomed.info/sct",
        "code": "161891005",
        "display": "Backache",
        "userSelected": true
      }
    ],
    "text": "unspezifische Rückenschmerzen LWS"
  }
}
```

**Wichtige Regel**: Mehrere Codings in einem CodeableConcept sollen *dasselbe* Konzept aus verschiedenen Codesystemen ausdrücken — nicht verschiedene Bedeutungen!

**display vs. text:**
- `Coding.display` = Anzeigename, den das Codesystem vorgibt (aus der CodeSystem-Definition)
- `CodeableConcept.text` = freier Anwender-Text, der den Kontext beschreibt — kann Nuancen enthalten, die kein Code ausdrückt; ersetzt Codings wenn keine geeigneten Codes vorhanden

---

Wie ist eine FHIR-ValueSet-Resource aufgebaut? Erklären Sie `compose` vs. `expansion` und intensionale vs. extensionale Definition.

?

**ValueSet-Resource** (DomainResource), drei Hauptteile:

1. **Metadata**: `url`, `identifier` (OID), `version`, `name`, `title`, `status`, `publisher`, `copyright`
2. **Compose** (Content Logical Definition): Definition der enthaltenen Codes
   - `include[1..*]`: welche CodeSystems und Codes einbezogen (ConceptSet mit system, version, Codes oder Filter)
   - `exclude[0..*]`: welche Codes ausgeschlossen
   - `import`: ein ganzes anderes ValueSet einbeziehen
3. **Expansion**: zur Laufzeit erzeugte Liste aller Konzepte (mit `identifier`, `timestamp`, `contains[*]`)

**Compose ≠ Expansion:**
- Compose = statische Definition (wann immer abgefragt)
- Expansion = zur Laufzeit aufgelöste Liste — kann sich ändern, wenn das zugrunde liegende CodeSystem wächst

**Intensional vs. Extensional:**
- **Extensional**: explizite Aufzählung der Codes (eingefroren)
- **Intensional**: Regel/Filter (z. B. alle SNOMED-Konzepte unterhalb Knoten X via `is-a`-Filter)

**Composition-Operatoren im Filter**: `=`, `is-a`, `is-not-a`, `regex`, `in`, `not-in`

**Drei Identifikatoren eines ValueSets:**
- `id` — serverlokal (kann sich ändern)
- `url` — globale kanonische URI (ändert sich **nie**)
- `identifier` — externe Referenz (z. B. OID für HL7v3/CDA)

---

Welche vier Operationen kennt der FHIR Terminology Service? Erläutern Sie jede mit Aufgabe und typischem Aufruf.

?

| Operation | Ressource | Aufgabe |
|---|---|---|
| **`$expand`** | ValueSet | Compose-Definition zur Laufzeit in explizite Code-Liste auflösen |
| **`$lookup`** | CodeSystem | Details zu einem Code abfragen (Name, Version, Display, Properties) |
| **`$validate-code`** | ValueSet | Prüfen, ob ein Code in einem ValueSet gültig ist |
| **`$translate`** | ConceptMap | Code von einem CodeSystem in ein anderes übersetzen |

**`$lookup`-Beispiel:**
```
GET http://tx.fhir.org/r4/CodeSystem/$lookup?
    system=http://terminology.hl7.org/CodeSystem/v3-MaritalStatus&code=M
```
→ Antwort: `Parameters` mit name: „v3.MaritalStatus", version: „2018-08-12", display: „Married"

**`$validate-code`-Beispiel:**
```
GET http://tx.fhir.org/r4/ValueSet/$validate-code?
    url=http://hl7.org/fhir/ValueSet/marital-status&
    system=http://terminology.hl7.org/CodeSystem/v3-MaritalStatus&code=M
```
→ Code `M` gültig; Code `X` würde fehlschlagen.

**$expand ≠ $validate-code**: Expand liefert *alle* Codes; Validate-Code prüft *einen* Code.
**$lookup ≠ $validate-code**: Lookup = Details ohne ValueSet-Kontext; Validate = Gültigkeit im ValueSet-Kontext.

---

### Diskussion / Vergleich

Was ist der Unterschied zwischen CodeSystem, ValueSet und ConceptMap? Beschreiben Sie das Zusammenspiel an einem konkreten Beispiel.

?

| Ressource | Zweck | Analogie |
|---|---|---|
| **CodeSystem** | Definiert Codes und ihre Bedeutung | Wörterbuch |
| **ValueSet** | Wählt Codes für einen Kontext | Fachjargon-Glossar (Auswahl aus dem Wörterbuch) |
| **ConceptMap** | Mappt zwischen zwei ValueSets/CodeSystems | Übersetzungstabelle |

**Beispiel (LOINC-Lab in ELGA):**
1. `CodeSystem`: `http://loinc.org` — definiert `8480-6` als „Systolic blood pressure"
2. `ValueSet`: `ELGA_Laborparameter` — wählt relevante LOINC-Codes aus (Subset des 95.000-Codes-CodeSystems)
3. FHIR-Element `Observation.code` → Binding (preferred) auf `ELGA_Laborparameter`
4. LIS verwendet lokalen Code → `ConceptMap` mappt Lokal-Code auf LOINC `8480-6` (Equivalence: `equivalent`)
5. Prüfung: `$validate-code?url=ELGA_Laborparameter&code=8480-6` → gültig

---

Warum ist Binding Strength `extensible` eine Zwickmühle für Interoperabilität?

?

**Definition extensible**: Wenn ein passender Code im ValueSet existiert, muss er verwendet werden. Wenn nicht, dürfen alternate codings oder Text verwendet werden.

**Problem — subjektive „Passend"-Beurteilung:**
- Wer entscheidet, ob ein Code „passt"? Die Implementierung.
- Wenn System A sagt „kein passender Code" und System B einen Code findet → unterschiedliche Codierungen desselben Konzepts → semantische Divergenz.

**Benson & Grieve Zitat:**
> „It is amazing how often everyone agrees that a coded element is essential for exchange, but there is no prospect of agreeing to a value set for said exchange."

**Konsequenz**: FHIR-Basisstandard hat viele Bindings nur auf `example` oder `preferred`, weil internationale Einigung auf ein ValueSet oft nicht möglich ist.

**Lösung**: Nationale oder projektspezifische Profile verschärfen Bindings:
- `example` → `required` für nationale Pflicht-ValueSets
- `extensible` → `required` für geschlossene nationale Listen

Beispiel: `Observation.code` hat im FHIR-Basisstandard nur `example`-Binding auf LOINC. ELGA-Profil setzt es auf das verpflichtende `ELGA_Laborparameter`-ValueSet.

---

Was ist eine ConceptMap, warum ist sie unidirektional, und welche Equivalence-Typen gibt es?

?

**ConceptMap**: beschreibt die Beziehung zwischen Konzepten aus zwei ValueSets/CodeSystems. Unidirektional — für Rückrichtung braucht man eine zweite ConceptMap.

**Warum unidirektional?**
- Semantische Äquivalenz ist oft asymmetrisch: ICD-10 `M54.9` (Rückenschmerzen) ist breiter als SNOMED `161891005` (Backache, spezifische Form)
- Aus Sicht von ICD→SNOMED: `wider` (ICD breiter)
- Aus Sicht von SNOMED→ICD: `narrower` (SNOMED enger)
- → Dieselbe Beziehung, aber unterschiedliche Equivalence-Richtung — erfordert zwei separate Maps

**Equivalence-Typen (häufigste):**

| Code | Bedeutung |
|---|---|
| `equivalent` | bedeutungsäquivalent |
| `equal` | identisch |
| `wider` | Target-Konzept ist breiter (verlustbehaftet) |
| `narrower` | Target-Konzept ist enger + Comment Pflicht |
| `relatedto` | irgendwie verwandt (vageste Form) |
| `inexact` | nicht exakt — Comment Pflicht |
| `unmatched` | kein passendes Target |
| `disjoint` | Konzepte schließen sich aus |

**group.unmapped**: definiert den Fallback, wenn kein Mapping greift.

---

Welche FHIR Terminology Service Operationen entsprechen welchen IHE SVCM-Transaktionen?

?

IHE SVCM (Sharing Valuesets, Codes and Maps) profiliert FHIR für interoperablen Terminologieaustausch. Die Transaktionen (ITI-Nummern) entsprechen direkt den FHIR-Operationen:

| FHIR-Operation | IHE-SVCM-Transaktion | Aufgabe |
|---|---|---|
| `$expand` | **ITI-97** | ValueSet expandieren |
| `$lookup` | **ITI-96** | Code-Details nachschlagen |
| `$validate-code` | **ITI-99** | Code in ValueSet validieren |
| `$translate` | **ITI-101** | Code via ConceptMap übersetzen |
| FHIR-Read (GET ValueSet/{id}) | **ITI-95** | Einzelnes ValueSet abrufen |

**IHE SVCM-Akteure:**
- **Terminology Repository** (= FHIR Terminology Server mit diesen Operationen)
- **Terminology Consumer** (= das abfragende System, z. B. KIS, LIS)

**Vergleich IHE SVS (alt) vs. IHE SVCM (neu):**
- SVS: XML/SOAP, nur Value-Set-Retrieval (`$expand`-Äquivalent)
- SVCM: FHIR-basiert, vollständiger Service (alle 4 Operationen) — SVS ist deprecated

---

Vergleichen Sie die Terminologie-Konzepte in CDA und FHIR: Code-Identifikation, Binding, Validierung.

?

| Aspekt | HL7 CDA | HL7 FHIR |
|---|---|---|
| **Code-Identifikation** | OID (`codeSystem`-Attribut, z. B. `2.16.840.1.113883.6.1`) | URI (`system`-Feld, z. B. `http://loinc.org`) |
| **Codierter Datentyp** | CE, CD (mit code, codeSystem, displayName, translation) | code / Coding / CodeableConcept |
| **Mehrfach-Codierung** | `<translation>` (Pattern A mit nullFlavor OTH oder Pattern B) | CodeableConcept.coding[*] (mehrere Codings direkt) |
| **Binding-Verbindlichkeit** | DYNAMIC (aktuelle Version) oder STATIC (fixe Version) in CONF-Regeln | Binding Strength: required / extensible / preferred / example |
| **Binding-Prüfung** | Schematron-Regeln aus ART-DECOR (zur Validierungszeit) | `$validate-code`-Operation (zur Laufzeit) |
| **Wertemenge für ValueSet** | Value Set im Terminologieserver (ELGA Termgit), OID-referenziert | FHIR ValueSet-Resource mit canonical URL |
| **ValueSet-Entwicklung** | DYNAMIC = wächst mit; STATIC = eingefroren | intensionale Compose-Definition = wächst mit; Expansion = eingefroren |

**Key Insight**: CDA nutzt OID, FHIR URI — Konversionstabellen für HL7 OID ↔ FHIR URI sind definiert (z. B. LOINC OID `2.16.840.1.113883.6.1` ↔ `http://loinc.org`).

---

## Mögliche Anschlussfragen des Prüfers

- Was ist `compositional: true` in einem CodeSystem? (Postkoordination unterstützt)
- Wie wird ein ganzes CodeSystem in ein ValueSet einbezogen? (`include` ohne Filter → alle Codes)
- Was ist der Unterschied zwischen `import` und `include` in ValueSet.compose?
- Welche FHIR-Operation entspricht IHE SVCM ITI-97? (`$expand`)
- Welche OID identifiziert LOINC in CDA? (`2.16.840.1.113883.6.1`) — und welche URI in FHIR? (`http://loinc.org`)
- Warum ist "Expand" kein "Erweitern" sondern "Ausklappen"? (intensionale Definition zur expliziten Liste auflösen)
- Was ist der Unterschied zwischen Equivalence `equal` und `equivalent` in einer ConceptMap?
- Wie hängt FHIR Terminology Service mit einem Terminologieserver (z. B. ELGA Termgit) zusammen? (Termgit implementiert FHIR Terminology Service → ist ein Terminology Repository im Sinne von IHE SVCM)

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
