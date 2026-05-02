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

# MSI - PF - Terminologien Detail

## Kontext

Tiefenkarte zu LOINC, UCUM und Identifikatoren im eHealth-Umfeld. Abgedeckt: LOINC-Definition, Sechs-Achsen-Struktur, FSN, Inhaltsbereiche, CDA-Verwendung; UCUM-Definition, Aufbau, Beispiele; OID-Konzept und eHealth-Identifikator-Übersicht.

## Verlinkte Konzepte

- [[MSI - LOINC - Definition]]
- [[MSI - LOINC - Sechs-Achsen-Struktur]]
- [[MSI - LOINC - Fully Specified Name]]
- [[MSI - LOINC - Inhalt]]
- [[MSI - LOINC - Verwendung in CDA]]
- [[MSI - UCUM - Definition]]
- [[MSI - UCUM - Aufbau]]
- [[MSI - UCUM - Beispiele]]
- [[MSI - Identifikator - OID]]
- [[MSI - Identifikator - Übersicht eHealth]]

---

## Karten

### Definition

Was ist LOINC, wer pflegt es, und für welche Zwecke wird es eingesetzt?

?

**LOINC** (*Logical Observation Identifiers Names and Codes*): System zur eindeutigen Kennzeichnung von
- klinischen Untersuchungen
- Laborwerten
- anderen medizinischen Parametern
- medizinischen Dokumententypen

Zweck: Austausch und Zusammenführung von (Labor-)Untersuchungsergebnissen.

Entwickelt seit 1994 als freiwillige Initiative des **Regenstrief Institutes** (non-profit, Indiana University). Browser frei nach Registrierung: `https://search.loinc.org`. OID: `2.16.840.1.113883.6.1`.

---

Welche sechs Achsen hat ein LOINC-Code? Was kodiert jede Achse?

?

Sechs Achsen (Notation: `Component:Property:Time:System:Scale:Method`):

| Achse | Was wird kodiert? | Beispiel |
|---|---|---|
| **Component** | Was wird gemessen (Analyt)? | Leukocytes, Glukose |
| **Property** | Welche physikalisch-chemische Eigenschaft? | NCnc (Zahlenkonzentration), Massenkonzentration |
| **Time** | Zeitbezug | Pt (Point in time), 24h |
| **System** | Untersuchungsmaterial/Probe | Bld (Blut), Urin, CSF |
| **Scale** | Skalen-Typ | Qn (quantitativ), qualitativ |
| **Method** | Messmethode (oft leer) | Manual Count |

Beispiel Code `26464-8`: `Leukocytes:NCnc:Pt:Bld:Qn` → Leukozyten-Zahlenkonzentration, einmaliger Messzeitpunkt, Blut, quantitativ.

---

Was ist UCUM, und welchen Zweck verfolgt es im Verhältnis zu LOINC?

?

**UCUM** (*Unified Code for Units of Measure*): Code-System zur Codierung von Maßeinheiten für den elektronischen Datenaustausch.

Kernzweck: **eindeutige Verarbeitung und automatische Umrechnung auf SI-Basiseinheiten**.

Pflege: Regenstrief Institute. OID: `2.16.840.1.113883.6.8`. Verwendet von HL7, DICOM, FDA.

**Verhältnis zu LOINC:**
- LOINC sagt, *was* gemessen wird (Konzept-Identifikation).
- UCUM sagt, in *welcher Einheit* das Ergebnis ausgedrückt wird.
→ Komplementär, nicht konkurrierend: „UCUM ergänzt LOINC."

---

Welche fünf Bestandteile definieren die UCUM-Sprache?

?

1. **Präfixe** – Symbole für Multiplikatoren (z. B. `d` = Dezi-, `u` = Mikro-)
2. **Basiseinheiten** – Grundgrößen (Länge `m`, Masse `g`, Zeit `s`, …)
3. **Abgeleitete Einheiten** (atomic unit symbols) – weitere Einheiten mit Umrechnungsfaktoren
4. **Syntaxregeln** – Operatoren für Multiplikation (`.`), Division (`/`), Potenzierung, Klammern
5. **Annotationen** – in geschwungenen Klammern `{…}` für Interpretationskontext, ändern die Einheit nicht

Wichtig: UCUM ist primär eine **Schreibweise**, keine geschlossene Einheitsliste — neue Einheiten entstehen kompositorisch.

---

### Anwendung

Welche drei Anwendungsfälle für LOINC kennt CDA (ELGA)? Welche Attribute trägt ein `<code>`-Element?

?

**Drei Anwendungsfälle (Folie 25):**
1. **Laborparameter** (Observation): `<code code="26464-8" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC" displayName="Leukozyten"/>`
2. **Dokumentenklasse**: `<code code="11490-0" displayName="Physician Discharge summary" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>`
3. **Section-Codierung**: `<code code="42349-1" displayName="Reason for Referral" codeSystem="2.16.840.1.113883.6.1" codeSystemName="LOINC"/>`

**Pflicht-Attribute des `<code>`-Elements:**
- `code` – der LOINC-Code
- `codeSystem` – LOINC-OID `2.16.840.1.113883.6.1`
- `codeSystemName` – `"LOINC"`
- `displayName` – sprechende Bezeichnung (ELGA: oft deutsch)

---

Erkennen Sie die folgenden UCUM-Schreibweisen und erklären Sie ihre Struktur: `mm[Hg]`, `10*6/uL`, `[IU]/10*9{RBCs}`.

?

**`mm[Hg]`** – Millimeter Quecksilbersäule (millimeter of mercury):
- Präfix `m` + Basiseinheit `m` = Millimeter; eckige Klammer `[Hg]` = abgeleitete Einheit für Quecksilber-Druckskala.
- Achtung: `mmHg` ohne eckige Klammer ist *nicht* UCUM-konform.

**`10*6/uL`** – Millionen pro Mikroliter:
- `10*6` = Multiplikator 10⁶; `/` = Division; Präfix `u` (Mikro-) + `L` (Liter).

**`[IU]/10*9{RBCs}`** – internationale Einheiten pro Milliarde rote Blutkörperchen:
- `[IU]` = International Unit (abgeleitete Einheit); `/10*9` = pro Milliarde; `{RBCs}` = Annotation (kein Einheitsbestandteil, nur Lesekontext).

---

Welche eHealth-Identifikatoren werden in einem ELGA-CDA-Dokument gleichzeitig verwendet? Ordnen Sie sie ihrem Zweck zu.

?

In einem ELGA-CDA-Dokument können parallel auftreten:

| Identifikator | Identifiziert |
|---|---|
| **bPK-GH** | Person im Bereich Gesundheit (österreichisch) |
| **MPI** (Master Patient Index) | Patientenidentität (technisch) |
| **GDA-Index** | Gesundheitsdiensteanbieter (Aussteller) |
| **Dokumenten-ID + Versionsnummer** | Das einzelne Dokument als Instanz |
| **OID** (`codeSystem`-Attribut) | Code System, Value Set, Template |
| **PZN** | Arzneimittel-Packung |
| **Ländercodes** (ISO 3166) | Staatsangabe |

Wichtige Unterscheidung: OID identifiziert *Klassen* (Code System, Template), Dokumenten-ID identifiziert *Instanzen*.

---

### Diskussion / Vergleich

Sind LOINC-Codes prä- oder postkoordiniert? Erfüllt LOINC Ciminos „Nonsemantic Concept Identifier"? Begründen Sie.

?

**Präkoordiniert:** Jeder LOINC-Code repräsentiert eine fertige Kombination der sechs Achsenwerte. Der Nutzer wählt einen vordefinierten Code aus; er kombiniert keine Achsen zur Laufzeit.

**Ja, Ciminos Nonsemantic Identifier:** Die LOINC-Ziffernfolge (z. B. `26464-8`) trägt **keine Bedeutung**. Die Bedeutung folgt ausschließlich aus dem zugeordneten Fully Specified Name. Es gibt keine eingebettete Hierarchie in den Ziffern.

Kontrast: APPC kodiert Achsen *in der Code-Struktur* (semantischer Code) — das verstößt gegen Ciminos Nonsemantic Identifier. LOINC dagegen erfüllt das Desideratum.

---

Warum wird in ELGA nicht der gesamte LOINC verwendet, sondern das Value Set `ELGA_Laborparameter`? Welche Vor- und Nachteile hat das?

?

**Grund:** LOINC enthält über 95.000 Codes. Für ELGA-Laborbefunde ist nur eine kontrollierte Teilmenge relevant, die eine einheitliche Codierung zwischen Laborinformationssystemen garantiert.

**Vorteile des Value Sets:**
- Klare Erwartungshaltung: Empfänger kennen die möglichen Codes.
- Validierung möglich (Schematron prüft gegen Value Set).
- Kürzere Mapping-Arbeit für Hersteller.

**Nachteile / Risiken:**
- Value Set kann nicht schnell genug wachsen (neuer Parameter, noch kein ELGA-Code).
- Wartungsaufwand bei jedem LOINC-Release.
- DYNAMIC-Binding ermöglicht Erweiterungen ohne Breaking Change — aber Implementierer müssen aktiv prüfen.

---

Wie unterscheiden sich OID und URL als Identifikatoren für Code Systems in CDA vs. FHIR?

?

| | OID (CDA) | URL (FHIR) |
|---|---|---|
| Format | Punkt-getrennte Hierarchie (ISO/IEC 9834), z. B. `2.16.840.1.113883.6.1` | HTTP-URL, z. B. `http://loinc.org` |
| Lesbarkeit | gering (numerisch, opak) | hoch (sprechend) |
| Verwendung in CDA | `codeSystem`-Attribut | — |
| Verwendung in FHIR | `system`-Element (URL) | ja |
| Stabilität | sehr hoch (ISO-Standard) | abhängig von Domaininhaber |
| Erweiterbarkeit | über Registrierungsstellen | offen |

→ CDA verwendet OIDs; FHIR-native verwendet URLs. Konvertierungen sind definiert (HL7 OID-Registry listet FHIR-URIs). Value Sets in ELGA können zusätzlich OID *und* URL tragen.

---

## Mögliche Anschlussfragen des Prüfers

- Welcher LOINC-Code identifiziert die Dokumentenklasse „Physician Discharge Summary"? (`11490-0`)
- Warum hat die Method-Achse in LOINC oft keinen Wert?
- Welche OID identifiziert UCUM? (`2.16.840.1.113883.6.8`)
- Was ist `G/L` in UCUM? (Gramm pro Liter)
- Wie sieht `mg/g{feces}` erklärt aus? (Annotation ändert Einheit nicht — nur Kontext)
- Warum unterscheiden sich `1.2.40.0.34.*`-OIDs von `2.16.840.1.113883.*`? (Österreich-spezifisch vs. HL7-international)
- Was ist der Unterschied zwischen Dokumenten-ID und OID?

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
