---
fach: msi
typ: konzept
status: offen
quelle: "[[MSI - VL - Semantik Theorie]]"
tags:
  - fach/allgemein/msi
  - typ/konzept
  - status/offen
---

# MSI - Terminologie - Cimino Desiderata

> [!info] Kurzdefinition
> Klassischer Anforderungs­katalog von James J. Cimino (1998) an kontrollierte medizinische Vokabulare im 21. Jahrhundert. Im Original­paper sind es **zwölf** Desiderata; die Vorlesung 02 hat elf explizit gelistet (Folien 13–16) und Cimino's Wissens-Modell aus drei Sichten gezeigt (Folie 22, Fig. 2). Die Konzept-Note enthält jetzt alle zwölf Punkte und Paper-Nuancen.

## Beschreibung

Quelle: JJ Cimino (1998) *Desiderata for Controlled Medical Vocabularies in the Twenty-First Century*, Methods Inf Med 37(4–5):394–403. Das vollständige Paper liegt im Vault als [[MSI - Paper - Cimino Desiderata]] vor; die LV-Behandlung in [[MSI - VL - Semantik Theorie]].

Die zwölf Desiderata in der Reihenfolge des Originalpapers (Sektionen 2.1–2.12), mit den in der Vorlesung verwendeten Bezeichnungen in Klammern:

1. **Vocabulary Content** („Content, Content, Content!", Sektion 2.1) – umfassend, erweiterbar. Cimino diskutiert zwei Strategien: ad-hoc-Erweiterung (einfach, aber fragmentiert) oder atom-basierte Komposition (kompositorisch erweiterbar, aber mit dem Atom-vs.-Molekül-Problem: Ist „White" ein Atom? „Wolff-Parkinson-White Syndrome"?). Lösung laut Cimino: **formale Methodologie** für Inhaltserweiterung („more attention to *how* representations are developed").

2. **Concept Orientation** (Sektion 2.2) – jedes Konzept ist die symbolische Verarbeitungs­einheit. Drei Anforderungen pro Term: **nonvagueness** (mindestens ein Konzept), **nonambiguity** (höchstens ein Konzept), **nonredundancy** (jede Bedeutung höchstens ein Term). Wichtige Unterscheidung: kontext-sensitiv-Mehrdeutigkeit („MI" als Modifier in „Rule Out Myocardial Infarction" vs. „Family History of Myocardial Infarction") ist legitim; kontext-unabhängige Mehrdeutigkeit ist verboten.

3. **Concept Permanence** (Sektion 2.3) – die Bedeutung eines Konzepts darf sich nicht ändern. Preferred name kann sich ändern (Beispiel: „pacemaker" → „implantable pacemaker", als „percutaneous pacemaker" hinzugefügt wurde). Bedeutung darf nicht ändern – „non-A-non-B hepatitis" darf NICHT zu „Hepatitis C" umbenannt werden, weil die zwei Konzepte nicht exakt synonym sind. Auch nicht löschen, nur als inaktiv/archaisch flaggen.

4. **Nonsemantic Concept Identifier** (Sektion 2.4) – der Konzept-Identifier soll keine Bedeutung tragen. Hierarchische Codes haben Vorteile (lesbar, klassen­basierte Suche durch Präfix-Filter), aber: Tiefen­begrenzung (z. B. Decimal-Code mit 10 Konzepten/Ebene und Tiefe 4); Klassifikations­änderungen brechen den Code; Polyhierarchy wird unmöglich. Lieber opake IDs + hierarchische Information als Attribut.

5. **Polyhierarchy** (Sektion 2.5) – Konzepte sollen mehrere Eltern haben dürfen. Beispiel: „hepatorenal syndrome" muss Nachfahre von „liver disease" UND „renal disease" sein. Cimino argumentiert: strict hierarchies sind technisch einfacher, aber semantisch unzureichend.

6. **Formal Definitions** (Sektion 2.6) – Konzepte sollen formale, computer-manipulable Definitionen haben. Beispiel: „Pneumococcal Pneumonia" über `is-a` Pneumonia + `caused-by` Streptococcus pneumoniae. Trennung **definitional knowledge** (was ein Konzept *ist*) von **assertional knowledge** (was über das Konzept *gesagt* wird) ist Pflicht – „treated-with Penicillin" ist assertional, nicht definitional; „Streptococcus pneumoniae causes Pneumococcal Pneumonia" ist auch nur assertional, weil nicht Teil der Streptokokken-Definition.

7. **Reject „Not Elsewhere Classified" Terms** (Sektion 2.7) – catch-all-Terms wie „NEC" sind zu vermeiden, weil ihre Bedeutung sich mit jeder Erweiterung des Vokabulars subtil ändert (semantic drift) und historische Daten dadurch falsch interpretiert werden. **Wichtige Unterscheidung**: NEC (Not Elsewhere Classified) ist verboten; **NOS** (Not Otherwise Specified) ist erlaubt, weil es nur „keine Modifier zum Basiskonzept" bedeutet, nicht „andere als die existierenden".

8. **Multiple Granularities** (Sektion 2.8) – das Vokabular muss sowohl grobe (z. B. „Diabetes") als auch feine (z. B. „Insulin-Dependent Type II Diabetes Mellitus") Konzepte unterstützen. Single-granularity-Vokabulare sind selten wiederverwendbar, weil je nach Anwendung andere Detail­tiefe gebraucht wird (Hausarzt vs. Endokrinologe).

9. **Multiple Consistent Views** (Sektion 2.9) – ↗︎ siehe eigene Note [[MSI - Terminologie - Multiple Consistent Views]]. Anwendungs­spezifische Sichten müssen erlaubt sein (Kollabieren auf Synonyme, Verstecken von Zwischenebenen, Konversion in strikte Hierarchie), aber sie müssen *konsistent* sein – derselbe Term darf in einer Sicht nicht zwei verschiedene Subbäume haben (Cimino Fig. 1 e/f). **In der Vorlesung 02 nicht eigenständig gelistet**, materiell aber durch Folie 17 (Cimino Fig. 1) abgedeckt.

10. **Beyond Medical Concepts: Representing Context** (Sektion 2.10) – das Vokabular muss nicht nur Konzepte definieren, sondern auch Kontext repräsentieren: „what is sensible to say". Drei Schichten (Fig. 2): **Definitional** (wie Konzepte sich definieren), **Assertional** (wie Konzepte kombiniert werden, z. B. „Body Site modifies Finding"), **Contextual** (wo Konzepte in welchem Dokumenttyp auftauchen, z. B. „Finding part-of Physical Exam", „Progress Note part-of Hospital Admission"). Quelle der Idee: Galen Project, Rector et al. → „grammar of medical vocabulary".

11. **Evolve Gracefully** (Sektion 2.11) – Vokabulare müssen mit dem medizinischen Wissen ko-evolvieren. Änderungen müssen klar dokumentiert sein. **Gute Gründe** für Änderung: addition, refinement, precoordination, disambiguation, obsolescence, discovered redundancy, minor name changes. **Schlechte Gründe**, die zu vermeiden sind: redundancy, major name changes, code reuse, changed codes.

12. **Recognize Redundancy** (Sektion 2.12) – mit Vokabular-Evolution entstehen redundante Repräsentationen unweigerlich. Beispiel (Fig. 3): postkoordiniert „Pneumonia + Left Lower Lobe" ≡ präkoordiniert „Left Lower Lobe Pneumonia" mit `is-a: Pneumonia, has-site: Left Lower Lobe, participates-in: Finding`. Mechanismus zur Erkennung: formal definitions + context representation – mit `is-a`/`has-site`-Beziehungen kann ein System die Äquivalenz automatisch nachweisen. **Synonymie ist erwünscht** (verbessert Lesbarkeit) – andere Formen von Redundanz sollen erkennbar gemacht werden.

### Cimino's Wissens-Modell (Fig. 2 des Papers, Folie 22 der LV)

- **Definitional Knowledge** (how concepts define each other) – Beispiel: „Joint Swelling" über is-a → „Swelling", „Pathologic Function", „Finding"; site-of → „Joint" → is-a „Body Site" → has-abnormality „Right Knee".
- **Assertional Knowledge** (how concepts combine) – Beispiel: „Body Site modifies Finding".
- **Contextual Knowledge** (how concepts are used) – Beispiel: „Finding part-of Physical Exam"; „Progress Note part-of Hospital Admission".

## Bestandteile / Aufbau

Zwölf Desiderata, gegliedert in:
- **Inhalt und Struktur** (1, 2, 3, 4, 5, 6) – was im Vokabular steht und wie es strukturiert ist.
- **Vermeidung schlechter Praktiken** (7) – kein NEC.
- **Anwendbarkeit für mehrere Zwecke** (8, 9) – multipurpose-Fähigkeit.
- **Verbindung zur Anwendungswelt** (10) – Kontextrepräsentation.
- **Lebenszyklus** (11, 12) – Evolution und Redundanz.

## Beispiel

Aus Folie 14 LV (Concept Permanence): Erweiterung „Farben V1: Grün, Gelb, Rot, Blau, Sonstiges" → „Farben V2: Grün, Gelb (mit Subkonzept Orange), Rot, Blau (mit Subkonzept Türkis), Bunt gepunktet, Sonstiges". Konzepte werden hinzugefügt/strukturiert; die existierenden ändern ihre Bedeutung nicht.

Aus Cimino-Paper Fig. 3 (Recognize Redundancy): Postkoordiniert „Pneumonia + Left Lower Lobe" ist äquivalent zu präkoordiniertem „Left Lower Lobe Pneumonia" – mit `is-a: Pneumonia, has-site: Left Lower Lobe` lässt sich diese Äquivalenz automatisch erkennen.

## Abgrenzung

- **Cimino-Desiderata vs. Vorlesungs-Anforderungen** ([[MSI - Terminologie - Anforderungen]]): überlappend, aber Cimino ist detaillierter und konkreter (Concept Permanence, Non-semantic Identifiers, Multiple Consistent Views).
- **Cimino-Desiderata vs. Code System Definition**: Cimino formuliert Qualitäts­kriterien; Code Systems sind Implementierungen, die mehr oder weniger gut die Desiderata erfüllen.
- **NEC vs. NOS**: Cimino verbietet NEC, erlaubt NOS – das ist eine feine, prüfungsrelevante Unterscheidung.

## Prüfungsrelevanz

**Sehr hoch.** Cimino's Desiderata sind ein klassisches Prüfungsthema und werden in der Vorlesung 02 explizit vollständig durchgegangen.

**Typische Definitionsfrage:** Nennen Sie fünf Cimino-Desiderata und erklären Sie sie an einem Beispiel.

**Anwendungsfrage:** Bewerten Sie SNOMED CT, ICD-10 und APPC anhand der Desiderata. Welche werden erfüllt, welche nicht?

**Diskussionsfrage:** Warum verlangt Cimino non-semantic concept identifiers? Was sind die Probleme mit semantischen Codes (z. B. APPC mit eingebauter Achsen-Logik)?

**Mögliche Anschlussfragen:**
- Wie unterscheidet Cimino Definitional, Assertional und Contextual Knowledge?
- Was ist Polyhierarchy und warum reicht eine reine Taxonomie nicht?
- Was ist der Unterschied zwischen NEC und NOS?
- Welche drei Anforderungen formuliert Concept Orientation? (nonvagueness, nonambiguity, nonredundancy)
- Welches Desideratum wird durch SNOMED-Postkoordination am besten erfüllt? (Multiple Granularities, Formal Definition.)
- Wie verhalten sich Multiple Consistent Views zu Polyhierarchy? → [[MSI - Terminologie - Multiple Consistent Views]]
- Welche reale Terminologie verstößt gegen welches Desideratum? (APPC – semantischer Code; ICD-10 – „Sonstiges"-Kategorien; …)

## Verwandt

- [[MSI - Paper - Cimino Desiderata]] (vollständiges Paper als Quelle)
- [[MSI - Terminologie - Multiple Consistent Views]] (eigenständige Note für 12. Desideratum)
- [[MSI - Terminologie - Anforderungen]]
- [[MSI - Terminologie - Hierarchien]]
- [[MSI - Terminologie - Präkoordination vs Postkoordination]]
- [[MSI - Ordnungssystem - Ontologie]]
- [[MSI - Begriff - Synonyme Homonyme Eponyme]]

## Quelle

- Vorlesung: [[MSI - VL - Semantik Theorie]] (Folien 13–16: Desiderata 1/4 bis 4/4; Folie 17: Cimino Fig. 1 für Hierarchien; Folie 22: Cimino Fig. 2 für Wissens-Modell)
- Originalpaper: [[MSI - Paper - Cimino Desiderata]] (vollständige 12 Desiderata mit Begründungen)
- Externe Originalquelle: JJ Cimino (1998) *Desiderata for Controlled Medical Vocabularies in the 21st Century*, Methods Inf Med 37(4-5):394–403.
