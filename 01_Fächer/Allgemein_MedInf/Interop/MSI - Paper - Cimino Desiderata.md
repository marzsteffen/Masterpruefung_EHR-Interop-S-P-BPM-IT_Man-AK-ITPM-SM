---
fach: msi
typ: vorlesung
status: offen
quelle_pdf: Folien/Medizinische Standards und Semantische Interop/02 Semantik/Desiderata_Cimino.pdf
datum_vorlesung: 1998-11-01
tags:
  - fach/allgemein/msi
  - typ/vorlesung
  - status/offen
---

# MSI - Paper - Cimino Desiderata

## Überblick

Klassisches Perspectives-Paper von James J. Cimino (Department of Medical Informatics, Columbia University, New York), erschienen in *Methods of Information in Medicine* 1998; 37(4–5):394–403. NIH-PMC-Manuskript, eingebettet in der Vorlesung als Pflichtlektüre. Cimino fasst die zwölf Anforderungen zusammen, die ein wiederverwendbares, mehrzweck-fähiges Controlled Medical Vocabulary für das 21. Jahrhundert erfüllen sollte. Das Paper ist die zentrale Referenz für Anforderungen an medizinische Terminologien und wird in der Vorlesung 02 vollständig durchgegangen (dort allerdings ohne explizit „Multiple Consistent Views" als eigenständiges Desideratum).

## Lernziele (laut Paper)

- Alle zwölf Cimino-Desiderata identifizieren und definieren können.
- Die Begriffe „nonvagueness", „nonambiguity", „nonredundancy" als Konkretisierung der Concept Orientation kennen.
- Den Unterschied „Not Elsewhere Classified" (NEC) vs. „Not Otherwise Specified" (NOS) korrekt einordnen.
- Erläutern können, warum sowohl Polyhierarchy als auch Multiple Consistent Views nötig sind.
- Definitional vs. assertional Wissen unterscheiden und ihre Trennung begründen.
- Die Mechanismen erläutern, mit denen Cimino redundante Repräsentationen (z. B. präkoordiniert vs. postkoordiniert) wieder zusammen­führt – Fig. 3 als Schlüsselbild.

## Behandelte Konzepte

- [[MSI - Terminologie - Cimino Desiderata]] (umfassende Note mit allen 12 Desiderata)
- [[MSI - Terminologie - Multiple Consistent Views]] (eigenständig, weil in der Vorlesung 02 nicht explizit gelistet)
- [[MSI - Terminologie - Hierarchien]] (Cimino Fig. 1)
- [[MSI - Ordnungssystem - Ontologie]] (Cimino Fig. 2 + Fig. 3)
- [[MSI - Terminologie - Präkoordination vs Postkoordination]] (Fig. 3 als Äquivalenz­beispiel)

## Roter Faden

1. Einleitung: Bauer:innen medizinischer Informatik-Anwendungen brauchen Controlled Vocabularies; bestehende Standards adressieren noch nicht alle Anforderungen. → 2. Desiderata (12 Stück, je eigene Sektion 2.1–2.12). → 3. Discussion: Mehrere der Desiderata sind technisch bereits erreichbar (z. B. nonsemantic identifiers, polyhierarchies); andere wie graceful evolution und multiple consistent views brauchen weiterhin Forschungsarbeit. → 4. Conclusions: Die Liste ist *partiell*, soll Diskussion anstoßen.

## Zentrale Aussagen / Take-aways

- **Eine gute medizinische Terminologie ist multipurpose** – „capturing clinical findings, natural language processing, indexing medical records, indexing medical literature, representing medical knowledge". Single-purpose-Vokabulare sind ein Hauptgrund für mangelnde Wiederverwendung.
- **Two main routes to expand content**: a) Begriffe ad hoc hinzufügen, wenn sie gebraucht werden; b) Atome enumerieren und kompositorisch kombinieren lassen. Beides hat Trade-offs (Größe vs. Komplexität, „White" vs. „Wolff-Parkinson-White Syndrome" – wann ist ein Begriff atomar?).
- **Concept Orientation** = jeder Term entspricht mindestens einem Konzept (nonvagueness), höchstens einem Konzept (nonambiguity), und jedes Konzept entspricht höchstens einem Term (nonredundancy).
- **Concept Permanence**: Bedeutung darf sich nicht ändern. Beispiel: „non-A-non-B hepatitis" darf NICHT zu „Hepatitis C" umbenannt werden, weil es nicht exakt synonym ist (eine 1980-Diagnose impliziert nicht zwingend Hepatitis C).
- **Nonsemantic Concept Identifier**: Hierarchie-Codes haben Charme (lesbar, klassen­basierte Suche), aber begrenzen Tiefe und brechen, sobald Polyhierarchy nötig wird. Lieber opake Codes + hierarchische Information als Attribut.
- **Polyhierarchy**: viele Vokabulare sind „strict hierarchies"; Cimino plädiert für Polyhierarchy. Beispiel: „hepatorenal syndrome" muss Nachfahre von „liver disease" UND „renal disease" sein.
- **Formal Definitions**: explizite Trennung zwischen *definitional* (was Konzepte definiert) und *assertional* (was über Konzepte ausgesagt wird) Wissen. Beispiel: „Pneumococcal Pneumonia" ist definitional über `is-a` Pneumonia + `caused-by` Streptococcus pneumoniae; `treated-with` Penicillin ist assertional.
- **Reject NEC**: Unterscheidung – „NEC" (Not Elsewhere Classified) ist als catch-all-Term zu vermeiden, weil seine Bedeutung sich mit jeder Erweiterung des Vokabulars subtil ändert (semantic drift). „NOS" (Not Otherwise Specified) ist erlaubt – heißt nur „keine Modifier zum Basiskonzept".
- **Multiple Granularities**: ein und dasselbe Vokabular muss „insulin molecule" und „insulin resistance" beherrschen. Single-Granularitäts-Vokabulare sind oft nicht wiederverwendbar.
- **Multiple Consistent Views**: wenn ein Vokabular polyhierarchisch ist, brauchen unterschiedliche Anwendungen womöglich Sichten mit nur einer Hierarchie – die müssen aber konsistent gemacht werden (Cimino Fig. 1 d–f).
- **Beyond Medical Concepts** (Context Representation): Vokabular sollte nicht nur Konzepte definieren, sondern auch *was-ist-sinnvoll-zu-sagen* (Galen Project, Rector et al.). Fig. 2 zeigt das Schichtenmodell Definitional / Assertional / Contextual Knowledge.
- **Evolve Gracefully**: Änderungen sind unvermeidlich; sie müssen klar dokumentiert werden, damit „good reasons" (addition, refinement, precoordination, disambiguation, obsolescence, discovered redundancy, minor name changes) von „bad reasons" (redundancy, major name changes, code reuse, changed codes) unterscheidbar bleiben.
- **Recognize Redundancy**: redundante Repräsentationen entstehen mit Evolution unweigerlich (Fig. 3 zeigt: postkoordiniert „Pneumonia + Left Lower Lobe" ≡ präkoordiniert „Left Lower Lobe Pneumonia" mit `is-a: Pneumonia, has-site: Left Lower Lobe, participates-in: Finding`). Das Vokabular braucht Mechanismen, diese Äquivalenzen zu erkennen.

## Querverweise zu anderen Vorlesungen

- [[MSI - VL - Semantik Theorie]] (Hauptbehandlung der Desiderata in den LV-Folien)
- [[MSI - VL - HL7 FHIR und Terminologieserver]] (FHIR Terminology, Terminologieserver als Anwendung der Cimino-Anforderungen)

## Anmerkungen zur Vorlesung

In der Vorlesungs-Note ([[MSI - VL - Semantik Theorie]]) sind elf Desiderata aufgelistet (Folien 13–16). Das im Paper zwölfte Desideratum **Multiple Consistent Views** (Section 2.9) ist in den LV-Slides nicht als eigener Punkt benannt; das Material zu Cimino's Fig. 1 (Folie 17 der LV) gehört inhaltlich aber in dieses Desideratum. Diese Lücke wird durch die Konzept-Note [[MSI - Terminologie - Multiple Consistent Views]] geschlossen. Die zentrale Konzept-Note [[MSI - Terminologie - Cimino Desiderata]] enthält jetzt alle zwölf Punkte plus die im Paper enthaltenen Nuancen (NEC vs. NOS, „non-A-non-B hepatitis"-Beispiel, definitional vs. assertional).

## Quelle

- PDF: `Folien/Medizinische Standards und Semantische Interop/02 Semantik/Desiderata_Cimino.pdf`
- Zitierung: Cimino JJ. *Desiderata for Controlled Medical Vocabularies in the Twenty-First Century*. Methods Inf Med 1998; 37(4–5):394–403. NIH-PMC-Manuskript verfügbar PMC 2012-08-10.
- Schlagworte: Controlled Medical Terminology; Vocabulary; Standards; Review.
- 85 Referenzen im Original-Paper.
