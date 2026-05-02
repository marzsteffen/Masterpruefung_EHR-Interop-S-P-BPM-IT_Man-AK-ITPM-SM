---
fach: itpm
typ: audit
datum: 2026-04-30
stufe: 1+2
tags:
  - typ/audit
  - fach/vertiefung/itpm
---

# ITPM - Audit Stufen 1+2 - 2026-04-30

## Zusammenfassung

- Konzept-Notes geprüft (Strukturaudit): 207
- Quell-Notes geprüft: 16
- Stufe-1-Befunde: 2 kritisch / 3 Empfehlung
- Stufe-2-Befunde: 0 Halluzinations-Verdacht / 1 teilweise / 7 sauber

---

## Stufe 1 – Strukturaudit

### 1.1 Naming-Konvention

**Verstöße gegen das 3-teilige Pflichtformat `ITPM - <Thema> - <Spezifikation>`:**
47 Konzept-Notes verwenden nur 2 Teile (`ITPM - X`) statt des vorgeschriebenen Formats. Das betrifft keine VL-Notes (korrekt) und keine Tipp-/Sonderzeichenfehler – rein die fehlende Spezifikations-Stufe.

Betroffene Notes:

- ITPM - 90% Syndrom
- ITPM - Ablauf- und Terminplan
- ITPM - Abschlussanalyse
- ITPM - Arbeitspaket
- ITPM - Brooks's Law
- ITPM - Compliance Management System
- ITPM - Cone of Uncertainty
- ITPM - Critical Qualities
- ITPM - Crystal Family
- ITPM - Earned Value Management
- ITPM - Extreme Programming
- ITPM - Feature Driven Development
- ITPM - Gantt-Diagramm
- ITPM - ISO 21500
- ITPM - ISO 37301 und Compliance Officer
- ITPM - IT-Projekt-Compliance
- ITPM - Kapazitätsüberwachung
- ITPM - Kick-off-Meeting
- ITPM - Kostenarten und Finanzierung
- ITPM - Kostenplan
- ITPM - Kostentrendanalyse
- ITPM - Kostenüberwachung
- ITPM - Kritischer Weg
- ITPM - Lastenheft
- ITPM - Leistungsüberwachung
- ITPM - Meilenstein
- ITPM - Meilensteintrendanalyse
- ITPM - Pflichtenheft
- ITPM - Phasenmodelle
- ITPM - PMI Risikomanagement-Prozess
- ITPM - Projekt-Compliance
- ITPM - Projektberichtsplan
- ITPM - Projektmarketing
- ITPM - Projektsteuerung
- ITPM - Projektstrukturplan
- ITPM - Pufferzeiten
- ITPM - Quality Gates
- ITPM - Quality in Use vs Product Quality
- ITPM - Qualitätsbezogene Kosten
- ITPM - Qualitätsplanung
- ITPM - Risikodokumente
- ITPM - Risikoidentifikation
- ITPM - Risikokategorien
- ITPM - Risikoklausur
- ITPM - Risikomatrix
- ITPM - Terminüberwachung
- ITPM - Wasserfallmodell

**Bewertung:** Für atomare Konzepte wie „Meilenstein" oder „Wasserfallmodell" ist ein 3-teiliges Format oft künstlich (z. B. `ITPM - Projektplanung - Meilenstein`). Die Konvention ist hier zu starr formuliert oder wurde bei der Befüllung konsistent ignoriert. Entscheidung liegt beim Nutzer, ob Umbenennung gewünscht wird.

Keine Double-Dash-Probleme, keine Unterstriche statt Bindestriche, keine Slashes in Dateinamen.

### 1.2 Frontmatter-Vollständigkeit

**Keine Verstöße.** Alle 223 Notes enthalten exakt:

- 1× `fach/vertiefung/itpm`
- 1× `typ/konzept` (207 Notes) bzw. `typ/vorlesung` (16 Notes)
- 1× `status/offen`

Alle Tags korrekt nach Schema. Keine doppelten, fehlenden oder falsch geschriebenen Tags.

### 1.3 Quelle-Wiki-Link

**Fehlend in:** keine — alle 207 Konzept-Notes haben im Frontmatter (`quelle:`) und im Body (`## Quelle → Vorlesung:`) einen Wiki-Link auf eine Quell-Note.

**Broken Links:** keine — alle referenzierten VL-Notes existieren im Fach-Ordner.

**Zusatzbeobachtung – fehlerhafte Verwandt-Links (kritisch):**
3 Notes verlinken in `## Verwandt` auf `[[ITPM - Agile - Scrum]]` — diese Note existiert **nicht**. Der korrekte Titel ist `[[ITPM - Scrum - Grundlagen]]` (existiert). Das ist kein gewollter offener Link, sondern ein Benennungsfehler:

- ITPM - Spiralmodell - Boehm
- ITPM - Stacey Matrix - Komplexitätseinordnung
- ITPM - Vorgehensmodelle - Klassisch vs Agile

**Weitere unresolved Verwandt-Links** (laut INSTRUCTIONS gewollt – signalisieren fehlende Notes):

| Unresolved Link | Referenziert von | Handlungsbedarf |
|---|---|---|
| `[[ITPM - Stakeholdermanagement - Stakeholder Map]]` | 5 Notes | Note fehlt, häufig referenziert |
| `[[ITPM - Scrum - Sprint Retrospektive]]` | 3 Notes | Note fehlt |
| `[[ITPM - PMBOK - Wissensgebiete]]` | 3 Notes | Note fehlt |
| `[[ITPM - Scrum - Sprint Review]]` | 2 Notes | Note fehlt |
| `[[ITPM - Projekt - Charakteristika]]` | 1 Note | Note fehlt |
| `[[ITPM - Projektwürdigkeitsprüfung]]` | 1 Note | Note fehlt |
| `[[ITPM - Agile - Scrum]]` | 3 Notes | **Fehler** – sollte `[[ITPM - Scrum - Grundlagen]]` sein |

### 1.4 Verwaiste Notes (nicht im MOC)

**Keine.** Alle 223 `.md`-Dateien im Fach-Ordner sind im MOC verlinkt. Einzige Ausnahme ist `.gitkeep_marker` (kein `.md`, nicht relevant).

### 1.5 Tote MOC-Verweise

**Keine.** Jeder Wiki-Link im MOC hat eine entsprechende Datei im Fach-Ordner.

### 1.6 Mögliche Doppelungen

| Paar | Bewertung |
|---|---|
| `ITPM - V-Modell - Vorgehensmodell` + `ITPM - V-Modell - Entwicklungsstandard` | **Vermutlich gewollt** – konzeptuell verschieden: ersteres ist das generische V-Modell als Prozessform (Phasensymmetrie), letzteres ist V-Modell XT als deutsches Bundesstandard für IT-Projekte. |
| `ITPM - Projektmarketing` + 6× `ITPM - Projektmarketing - X` | **Gewollt** – Übersichtsnote plus atomare Detailnotes. Struktur sauber. |

Keine weiteren verdächtigen Namensvarianten (Singular/Plural, Umlaute, Rechtschreibvarianten).

### 1.7 Status-Verteilung

- `#status/offen`: 223
- `#status/geprüft`: 0

Erwartbar für einen frischen Vault ohne abgeschlossene Lernrunde.

---

## Stufe 2 – Quelltreue-Stichprobe

### Geprüfte Notes

1. **ITPM - Risikomatrix** ← ITPM - VL - Risiko und Stakeholder ← ITPMGT - 7 Risiko- und Stakeholdermanagement.pdf (Folien 72–73, 86–88)
   - **Bewertung:** ✓ Quelltreu
   - **Befund:** Alle Kerninhalte präzise aus dem PDF: „Arrow of Attention" (Folie 72 ✓), exakte 5-stufige Wahrscheinlichkeitsskala mit allen Prozentwerten (Folie 87 ✓), xy-Achsenbeschriftung ✓, „nur ein Risiko im roten Bereich → Projekt nicht beginnen" (Folie 86 ✓), „maximal 5–10 Risiken" ✓. Note differenziert korrekt zwischen Wahrscheinlichkeits-/Auswirkungsmatrix (Folien 72–73) und der Risikomatrix selbst (Folien 86–88).

2. **ITPM - Abschlussanalyse** ← ITPM - VL - Projektabschluss ← ITPMGT - 9 Projektabschluss.pdf (Folien 10–13)
   - **Bewertung:** ✓ Quelltreu
   - **Befund:** Alle drei Bestandteile textgetreu (Folie 10 ✓). Vier Fragen zur Zielanalyse wörtlich übernommen (Folie 12 ✓). Analyseworkshop-Formulierung identisch mit PDF (Folie 13 ✓). Keine Ergänzungen ohne Markierung.

3. **ITPM - RE - Erhebungstechniken** ← ITPM - VL - Initiierung Strukturierung Requirements ← ITPMGT - 4 …Requirements Engineering adaptiert.pdf (Folien 65–66)
   - **Bewertung:** ⚠ Nicht vollständig verifiziert (PDF konnte im Sandbox-Pfad nicht geöffnet werden)
   - **Befund:** Note hat präzise Folienangaben (65–66) und detaillierte Beschreibungen (Dreistufenplan Interview, Apprenticing, Brainstorming-Zyklus). Inhaltlich wirkt die Note quelltreu; keine offensichtlichen Lehrbuch-Formulierungen. **Empfehlung: Manuell gegen PDF abgleichen**, insbesondere den „Dreistufenplan" (Fragen → Zuhören → Wiederholen).

4. **ITPM - Compliance - Definition** ← ITPM - VL - Compliance ← ITPMGT - 9 Compliance.pdf (Folien 7–8)
   - **Bewertung:** ✓ Quelltreu
   - **Befund:** Kerndefinition wörtlich aus Folie 7 ✓. Drei inhaltliche Aufschlüsselungen (Regelkonformität, Pflicht des Vorstands, Gesamtheit der Maßnahmen) exakt aus Folie 8 ✓. Die Aussage „Compliance ≠ Risikomanagement: Compliance ist ein spezielles Themenfeld des Risikomanagements" ist in Folien 7–8 nicht belegt; könnte aus späteren Folien der gleichen VL stammen – kein Ergänzungs-Marker gesetzt. Geringes Risiko, da die Abgrenzung sachlich zutreffend ist.

5. **ITPM - Scrum - Meetings** *(Honeypot)* ← ITPM - VL - Werkzeuge 02 Agiles PM ← ITPMGT - 3 Die Werkzeuge 02 Agiles PM.pdf (Folien 30–31, 49–50, 53–54, 57)
   - **Bewertung:** ✓ Quelltreu
   - **Befund:** Alle fünf Meetings korrekt beschrieben. Teilnehmer Sprint Planning 1 (PO, Entwicklungsteam, Management, Anwender) wörtlich aus Folie 49 ✓. Daily-Scrum-Fragen inklusive Zusatzfrage („Kann ich Kolleginnen oder Kollegen irgendwie helfen…") aus Folie 53 ✓. Sprint Review Timebox 4 h aus Folie 54 ✓. Sprint Retrospektive: „Optimierung der Arbeitsprozesse" + Impediment Backlog aus Folie 57 ✓. Note korrekt angemerkt, dass Scrum Guide 2017 Sprint Planning als ein Event fasst, Vorlesung aber explizit trennt.

6. **ITPM - Aufwandsschätzung - CoCoMo** *(Honeypot)* ← ITPM - VL - Aufwandsschätzung Kosten Personal Controlling ← ITPMGT - 6 …Aufwandsschätzung.pdf (Folien 46–48)
   - **Bewertung:** ✓ Quelltreu
   - **Befund:** Alle Konstanten für Basic CoCoMo exakt aus PDF: Organic (2,4/1,05/2,5/0,38) ✓, Semi-detached (3,0/1,12/2,5/0,35) ✓, Embedded (3,6/1,20/2,5/0,32) ✓. Intermediate-Formel (K1×…×K15) ✓. Detailed-Beschreibung entspricht Folie 48 ✓. Die 15 Kostentreiber korrekt als „im PDF nicht aufgeführt" markiert ✓. Berechnungsbeispiel in Prüfungsrelevanz ist eine korrekte Anwendung der Formel (nachgeprüft: 3,0 × 50^1,12 ≈ 240 PM ✓, 2,5 × 240^0,35 ≈ 17 Monate ✓).

7. **ITPM - Agiles Manifest - 4 Werte** *(Honeypot)* ← ITPM - VL - Werkzeuge 02 Agiles PM ← ITPMGT - 3 …Agiles PM.pdf (Folien 9–10)
   - **Bewertung:** ⚠ Teilweise
   - **Befund:** Alle vier Werte wörtlich aus Folie 10 ✓. Entstehungsjahr 2001, Ort Snowbird (Utah), 17 Personen aus Folie 9 ✓. **Problem:** Note enthält den Satz „Das Manifest sagt nicht, dass die rechte Seite (Prozesse, Dokumentation, Verträge, Pläne) wertlos ist – nur dass die linke Seite *höher* gewichtet wird." Dieser Satz steht **nicht in den Folien 9–10**. Er entstammt der Agile-Manifesto-Originalseite (agilemanifesto.org) und ist gut bekanntes Allgemeinwissen – aber er ist **nicht mit dem Ergänzungs-Marker** versehen, wie es die INSTRUCTIONS verlangen.

8. **ITPM - Earned Value Management** *(Honeypot)* ← ITPM - VL - Werkzeuge 01 ← ITPMGT - 2 Die Werkzeuge 01.pdf (Folien 12–14)
   - **Bewertung:** ✓ Quelltreu
   - **Befund:** Einführung 1967 durch das amerikanische Verteidigungsministerium ✓. Standardmethode PMBOK Guide ✓. EV/AC/PV-Definitionen ✓. CPI = EV/AC, SPI = EV/PV mit Interpretationstabelle identisch mit Folie 13 ✓. Externe Ressourcen (Wikipedia-Link, YouTube-Link) als Verweis korrekt übernommen ✓. Agile-Ergänzung korrekt mit „*(im PDF nicht definiert)*" markiert ✓.

### Honeypot-Check

| Thema | Befund |
|---|---|
| **Scrum – Events/Rollen/Artefakte** | ✓ Sauber. Notes `ITPM - Scrum - Meetings`, `ITPM - Scrum - Rollen` (Stichprobe aus Phase 0), `ITPM - Scrum - Artefakte` – alle eng an Folien. Kein Lehrbuch-Overhead. |
| **Agiles Manifest** | ⚠ Teilweise: 1 Satz ohne Ergänzungs-Marker (s. Note 7 oben). |
| **CoCoMo** | ✓ Sauber. Konstanten exakt, keine erfundenen Kostentreiber-Listen. |
| **Earned Value Management** | ✓ Sauber. Formeln präzise, kein PMBOK-Overhead ergänzt. |
| **PMBOK** | Nicht in Stichprobe gezogen. `ITPM - PMBOK - Grundlagen` hat `[[ITPM - PMBOK - Wissensgebiete]]` als Verwandt-Link – diese Note **fehlt noch**. Empfehlung: bei Phase 2 prüfen, ob PMBOK-Note die Wissensgebiete korrekt nicht behandelt (entsprechend dem Vorlesungsinhalt). |

---

## Empfehlungen

### Sofort handeln (vor Phase 2)

1. **Falscher Verwandt-Link `[[ITPM - Agile - Scrum]]` → `[[ITPM - Scrum - Grundlagen]]` korrigieren** in 3 Notes:
   - ITPM - Spiralmodell - Boehm
   - ITPM - Stacey Matrix - Komplexitätseinordnung
   - ITPM - Vorgehensmodelle - Klassisch vs Agile

2. **Agiles Manifest - 4 Werte:** Satz „Das Manifest sagt nicht, dass die rechte Seite…" mit Ergänzungs-Marker versehen oder in die `## Ergänzung außerhalb der Vorlesung`-Sektion verschieben.

3. **RE - Erhebungstechniken** manuell gegen ITPMGT - 4 …pdf verifizieren, insbesondere Dreistufenplan (Folie 65) und Apprenticing-Beschreibung.

### Nice-to-have (kann warten)

4. **Fehlende Notes anlegen** (oft referenziert, signifikante Lücken):
   - `ITPM - Stakeholdermanagement - Stakeholder Map` (5 Verwandt-Links zeigen darauf)
   - `ITPM - Scrum - Sprint Retrospektive` (3 Links) – Inhalt ist bereits in `ITPM - Scrum - Meetings` integriert; eigene Note wäre sinnvoll für atomare Verlinkung
   - `ITPM - Scrum - Sprint Review` (2 Links) – analog
   - `ITPM - PMBOK - Wissensgebiete` (3 Links)

5. **Naming-Konvention:** Entscheiden, ob die 47 zweiteiligen Notes umbenannt werden sollen. Falls ja, konsistentes Schema festlegen (z. B. `ITPM - Projektplanung - Meilenstein`). Falls nein, INSTRUCTIONS entsprechend anpassen. Keine inhaltliche Auswirkung auf die Prüfungsvorbereitung.

6. **Compliance - Definition:** Quelle für die Abgrenzung „Compliance = spezielles Themenfeld des Risikomanagements" prüfen – sie steht in Folie 7–8 nicht explizit, könnte aber aus späteren Compliance-Folien stammen.

### Beobachtungen / Anmerkungen

- **Granularität insgesamt gut.** Die 207 Konzept-Notes decken das Fach ITPM sehr vollständig ab. Der Detailgrad ist für eine 15–20-minütige mündliche Prüfung angemessen.
- **Prüfungsrelevanz-Sektionen qualitativ stark.** Stichproben zeigen gute Diskussionsfragen, Health-IT-Bezüge und Vergleichsachsen. Das ist die prüfungswichtigste Sektion – passt.
- **Abschnitt „Spezifika im Health-IT-Kontext" im MOC ist leer.** Dies ist eine inhaltliche Lücke für die Prüfung. Querbezüge (z. B. ELGA-Einführung, KIS-Projekte, Medizinprodukte-Zulassung im ITPM-Kontext) fehlen im MOC. Empfehlung für Phase 2: diesen Abschnitt befüllen.
- **Keine toten MOC-Links, keine verwaisten Notes** – strukturelle Integrität des Vaults ist ausgezeichnet.
- **Quelltreue-Niveau hoch.** In der Stichprobe (7 von 8 verifizierten Notes) konnte kein Halluzinations-Fall nachgewiesen werden. Das Agiles-Manifest-Problem ist ein Marker-Fehler, keine inhaltliche Erfindung.
