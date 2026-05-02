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

# MSI - PF - Cimino Desiderata

## Kontext

Tiefenkarte zu den zwölf Cimino-Desiderata (Cimino 1998, Methods Inf Med). Explizit prüfungsrelevant laut Vorlesung 02 (Semantik Theorie). Im Originalvorlesungs-PDF sind elf Desiderata gelistet (Folien 13–16); das zwölfte (Multiple Consistent Views, Sektion 2.9) ist über Folie 17 (Cimino Fig. 1) inhaltlich abgedeckt, aber nicht eigenständig benannt. Alle zwölf sind hier vertreten.

## Verlinkte Konzepte

- [[MSI - Terminologie - Cimino Desiderata]]
- [[MSI - Paper - Cimino Desiderata]]
- [[MSI - Terminologie - Multiple Consistent Views]]
- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]
- [[MSI - Ordnungssystem - Ontologie]]

---

## Karten

### Definition

Nennen Sie die zwölf Cimino-Desiderata (1998) für kontrollierte medizinische Vokabulare — mindestens acht mit Stichwort.

?

Aus dem Originalpaper (Sektionen 2.1–2.12):
1. **Vocabulary Content** – umfassend, erweiterbar
2. **Concept Orientation** – nonvagueness, nonambiguity, nonredundancy
3. **Concept Permanence** – Bedeutung darf sich nicht ändern
4. **Nonsemantic Concept Identifier** – keine Bedeutung im Code selbst
5. **Polyhierarchy** – Konzepte dürfen mehrere Eltern haben
6. **Formal Definitions** – computer-manipulable Definitionen
7. **Reject „Not Elsewhere Classified"** – keine NEC-catch-all-Terme
8. **Multiple Granularities** – grob und fein im selben Vokabular
9. **Multiple Consistent Views** – anwendungsspezifische, konsistente Sichten
10. **Context Representation** – Definitional / Assertional / Contextual Knowledge
11. **Evolve Gracefully** – Evolution mit dokumentierten, legitimen Gründen
12. **Recognize Redundancy** – Mechanismus zur Erkennung äquivalenter Repräsentationen

---

Was meint Cimino mit **Concept Orientation**? Welche drei Forderungen ergeben sich daraus?

?

**Concept Orientation** (Sektion 2.2): Jedes Konzept ist die symbolische Verarbeitungseinheit des Vokabulars. Drei Forderungen pro Term:

1. **Nonvagueness**: Jeder Term muss mindestens einem Konzept entsprechen (kein leerer Term).
2. **Nonambiguity**: Jeder Term darf höchstens einem Konzept entsprechen (kein Homonym).
3. **Nonredundancy**: Jedes Konzept darf höchstens einem Term entsprechen (kein Synonym ohne Markierung).

Erlaubt: kontext-sensitive Mehrdeutigkeit (z. B. „MI" in „Rule Out Myocardial Infarction" vs. „Family History of MI" – beide semantisch unterschiedliche Kontexte).
Verboten: kontext-unabhängige Mehrdeutigkeit.

---

Was besagt **Concept Permanence**, und warum ist das Beispiel „non-A-non-B hepatitis" → „Hepatitis C" ein Verstoß?

?

**Concept Permanence** (Sektion 2.3): Die Bedeutung eines Konzepts darf sich nie ändern. Ein Begriff kann inaktiv/archaisch markiert werden, aber nicht in ein neues Konzept umgedeutet werden.

**Warum „non-A-non-B hepatitis" ≠ „Hepatitis C":**
Eine Diagnose von 1980 mit „non-A-non-B hepatitis" impliziert *nicht zwingend* Hepatitis C — damals gab es noch keinen Nachweis. Die Konzepte sind nicht exakt synonym. Wäre der Code umbenannt worden, würden alle historischen Daten falsch interpretiert.

Zulässige Änderung: Preferred Name kann sich ändern, wenn ein neuer, präziserer Name gefunden wird — aber die Bedeutung bleibt dieselbe.

---

Was ist der Unterschied zwischen **NEC** (Not Elsewhere Classified) und **NOS** (Not Otherwise Specified)? Welches verbietet Cimino und warum?

?

**NEC** (Not Elsewhere Classified): Catch-all-Term für alles, was in keine andere Klasse passt. **Verboten** laut Cimino, weil: Mit jeder Vokabular-Erweiterung ändert sich stillschweigend die Bedeutung von NEC (semantic drift). Historische Daten werden falsch interpretiert → Verstoß gegen Concept Permanence.

**NOS** (Not Otherwise Specified): Bedeutet nur „keine weiteren Modifier zum Basiskonzept". Erlaubt, weil die Bedeutung stabil bleibt — NOS gibt keine Auskunft darüber, was noch im Vokabular existiert.

Merkhilfe: NEC = „ich passe nirgendwo sonst rein" (kontextabhängig, instabil); NOS = „ich bin was ich bin, ohne Spezifikation" (stabil).

---

### Anwendung

Wie unterscheidet Cimino **Formal Definitions** von Assertional Knowledge? Erläutern Sie am Beispiel „Pneumococcal Pneumonia".

?

**Definitional Knowledge** (Sektion 2.6): Was ein Konzept *ist* — die notwendigen und hinreichenden Bedingungen.
Beispiel: „Pneumococcal Pneumonia" = `is-a: Pneumonia` + `caused-by: Streptococcus pneumoniae`.

**Assertional Knowledge**: Was über das Konzept *gesagt* wird, aber es nicht definiert.
Beispiel: „treated-with: Penicillin" ist assertional (könnte sich ändern, definiert die Krankheit aber nicht).

Dritte Schicht — **Contextual Knowledge**: Wo ein Konzept in welchem Dokumenttyp vorkommt. Beispiel: „Finding part-of Physical Exam", „Progress Note part-of Hospital Admission".

→ Formal Definitions erlauben Reasoning (z. B. Äquivalenzerkennung); Assertional und Contextual Knowledge sind veränderlich und dürfen Definitionen nicht beeinflussen.

---

Welches Cimino-Desideratum betrifft das APPC-Achsen-Modell? Worin liegt das Problem mit semantischen Codes?

?

**Betroffenes Desideratum: Nonsemantic Concept Identifier** (Sektion 2.4).

APPC-Codes kodieren vier Achsen (Modalität, Lateralität, Prozedur, Anatomie) in der Code-Struktur. Das ist ein **semantischer Code** — die Bedeutung ist im Code eingebaut.

**Probleme:**
- Tiefenbegrenzung: hierarchische Codes lassen sich nur begrenzt vertiefen.
- Polyhierarchy unmöglich: ein Code kann nur einer Position in einer Hierarchie angehören.
- Klassenänderungen brechen den Code: wenn eine Achse umstrukturiert wird, ändern sich alle Codes.

**Ciminos Lösung:** opake IDs (bedeutungslose, stabile Identifier) + hierarchische Information als Attribut (z. B. `is-a`, `has-site`).

---

Skizzieren Sie den **Recognize Redundancy**-Mechanismus anhand von Ciminos Fig. 3 (Pneumonia + Left Lower Lobe).

?

**Redundanz** entsteht, wenn dasselbe klinische Konzept in zwei Repräsentationen vorliegt:

- **Postkoordiniert**: „Pneumonia" + Modifier „Left Lower Lobe" (zwei Codes, verknüpft zur Dokumentationszeit)
- **Präkoordiniert**: „Left Lower Lobe Pneumonia" (ein Code, vordefiniert im Vokabular)

**Recognize Redundancy** (Sektion 2.12): Das Vokabular muss formale Definitionen verwenden, um diese Äquivalenz automatisch zu erkennen:
- Left Lower Lobe Pneumonia: `is-a: Pneumonia`, `has-site: Left Lower Lobe`, `participates-in: Finding`
- Mechanismus: Reasoner gleicht Attribut-Profile ab und erkennt: post- und präkoordinierte Form beschreiben dasselbe Konzept.

→ Synonymie ist erwünscht (verbessert Lesbarkeit); andere Redundanz soll erkennbar gemacht werden, nicht einfach verboten.

---

### Diskussion / Vergleich

Warum ist **Polyhierarchy** für medizinische Terminologien notwendig? Warum reicht eine strikte Taxonomie nicht?

?

**Polyhierarchy** (Sektion 2.5): Ein Konzept kann mehrere Eltern haben.

**Beispiel:** „Hepatorenal Syndrome" muss gleichzeitig Nachfahre von „liver disease" UND „renal disease" sein — weil es tatsächlich beides ist. In einer strikten Taxonomie müsste man willkürlich eines der beiden als Elternteil wählen, was semantisch falsch wäre.

**Warum strikte Taxonomie nicht reicht:**
- Medizinische Konzepte haben inhärent mehrere Klassifikationsachsen (Ätiologie, Lokalisation, Manifestation).
- Ein Konzept in nur einem Ast zu zwingen führt zu falschen Schlussfolgerungen (Reasoning-Fehler).
- Suchende nach „liver disease" würden Hepatorenal Syndrome nicht finden, wenn es nur unter „renal disease" eingehängt ist.

---

Bewerten Sie **ICD-10** und **SNOMED CT** anhand von vier Cimino-Desiderata.

?

| Desideratum | ICD-10 | SNOMED CT |
|---|---|---|
| **Concept Permanence** | Teilweise: Codes werden manchmal für neue Konzepte wiederverwendet (problematisch) | Gut: Codes sind persistent, inaktivierte Konzepte bleiben erhalten |
| **Nonsemantic Identifier** | Schlecht: hierarchische Codes (A00–Z99 = Kapitel eingebaut) | Gut: opake numerische Concept IDs |
| **Polyhierarchy** | Schlecht: streng monohierarchisch | Gut: Polyhierarchie durch multiple is-a-Relationen |
| **Formal Definitions** | Schlecht: keine formalen Definitionen, nur Textbeschreibungen | Gut: Konzepte mit formalen Relationen (is-a, part-of, caused-by, …) |
| **Reject NEC** | Schlecht: viele „Sonstiges"-Kategorien | Besser: weniger NEC-Terme, aber nicht vollständig eliminiert |

→ SNOMED CT erfüllt deutlich mehr Desiderata als ICD-10 — daher für klinischen Einsatz besser geeignet, aber aufwändiger.

---

Was meint **Evolve Gracefully**, und welche Änderungsgründe nennt Cimino als legitim vs. problematisch?

?

**Evolve Gracefully** (Sektion 2.11): Vokabulare müssen mit dem medizinischen Wissen ko-evolvieren, aber Änderungen müssen klar dokumentiert und klassifiziert sein.

**Legitime (gute) Gründe für Änderungen:**
- Addition (neues Konzept)
- Refinement (Verfeinerung bestehender Konzepte)
- Precoordination (Zusammenführen zu einem präkoordinierten Term)
- Disambiguation (Mehrdeutigkeit auflösen)
- Obsolescence (Konzept veraltet, wird inaktiviert)
- Discovered Redundancy (Äquivalenz erkannt, Duplikat markiert)
- Minor Name Changes (Schreibweise, Präzisierung ohne Bedeutungsänderung)

**Problematische (schlechte) Gründe:**
- Redundancy (unkontrolliertes Duplizieren)
- Major Name Changes (Bedeutungsverzerrung)
- Code Reuse (alte Code-ID für neues Konzept — verletzt Concept Permanence!)
- Changed Codes (Identifier-Instabilität)

---

Wie hängen **Multiple Granularities** und **Multiple Consistent Views** zusammen, und warum braucht man beide?

?

**Multiple Granularities** (Sektion 2.8): Das Vokabular muss sowohl grobe als auch feine Konzepte enthalten — z. B. „Diabetes" und „Insulin-Dependent Type II Diabetes Mellitus". Ohne beide Granularitäten ist das Vokabular nicht für unterschiedliche Anwendungen nutzbar.

**Multiple Consistent Views** (Sektion 2.9): Wenn das Vokabular viele Granularitäten und Polyhierarchien hat, brauchen verschiedene Anwendungen unterschiedliche Sichten — z. B. nur Grobgranulares für die Abrechnung, nur eine Hierarchieachse für die Navigation.

**Warum beide nötig:**
- Multiple Granularities stellt sicher, dass das Vokabular *die* Inhalte hat.
- Multiple Consistent Views stellt sicher, dass Anwendungen *selektiv darauf zugreifen* können, ohne die Konsistenz zu verletzen.
- Ohne Multiple Granularities keine sinnvollen Views; ohne Multiple Consistent Views kein sicheres View-Management.

---

## Mögliche Anschlussfragen des Prüfers

- Welche Konzepte im Vault stammen aus Cimino? (Hierarchien, Präkoordination, Multiple Consistent Views)
- Was ist der Unterschied zwischen definitional und assertional knowledge in SNOMED CT?
- Welche Terminologien erfüllen Formal Definitions? Welche nicht?
- Wie unterscheidet sich Cimino's Redundancy von Value Set Redundanz?
- Was bedeutet „Atom vs. Molekül" in Vocabulary Content? (Wann ist ein Begriff atomar?)
- Welche Aussage macht Context Representation über die Einbettung von Konzepten in Dokument­typen?

## Eigene Notizen

<!-- Platz für eigene Ergänzungen während der Lernphase -->
