---
fach: itm-ak
typ: audit
datum: 2026-04-30
stufe: 1+2
tags:
  - typ/audit
  - fach/vertiefung/itm-ak
---

# ITM-AK - Audit Stufen 1+2 - 2026-04-30

## Zusammenfassung

- Konzept-Notes geprüft (Strukturaudit): 98
- Quell-Notes geprüft: 6 (5 VL-Notes + 1 Paper-Note)
- Gesamt-Notes im Fach-Ordner: 104
- Stufe-1-Befunde: **1 kritisch** / **1 Empfehlung** / 0 Fehler bei Tags/MOC
- Stufe-2-Befunde: **0 Halluzinations-Verdacht** / **2 teilweise** (davon 1 wegen gescanntem PDF nicht verifizierbar) / **6 sauber**

---

## Stufe 1 – Strukturaudit

### 1.1 Naming-Konvention

**Befund (Empfehlung):** 55 von 98 Konzept-Notes verwenden nur das Ein-Ebenen-Format `ITM-AK - <Thema>` statt des in INSTRUCTIONS.md definierten Pflichtformats `ITM-AK - <Thema> - <Spezifikation>`.

Betroffen sind alle Notes ohne zweiten Bindestrich-Separator, u. a.:

- ITM-AK - Vision
- ITM-AK - Mission
- ITM-AK - Balanced Scorecard
- ITM-AK - BCG-Matrix
- ITM-AK - Bilanz
- ITM-AK - Break-even-Analyse
- ITM-AK - Bundled Payments und Value-Based Reimbursement
- ITM-AK - Capacity Cost Rate
- ITM-AK - Care Delivery Value Chain
- ITM-AK - DRG und LKF
- ITM-AK - Deckungsbeitrag
- ITM-AK - EU-Institutionen
- ITM-AK - Eigenkapitalveränderungsrechnung
- ITM-AK - GAAP und IFRS
- ITM-AK - Gewaltenteilung
- ITM-AK - Gewinn- und Verlustrechnung
- ITM-AK - Grundfreiheiten des EU-Binnenmarkts
- ITM-AK - ICD-10 und MBDS
- ITM-AK - ISO 9001-2015
- ITM-AK - Internationale Zertifikate im Gesundheitswesen
- ITM-AK - Kapitalflussrechnung
- ITM-AK - Markteintrittsstrategien
- ITM-AK - Medizinisches Controlling
- ITM-AK - New Public Management
- ITM-AK - Operatives Controlling
- ITM-AK - PDCA-Zyklus
- ITM-AK - PESTEL-Analyse
- ITM-AK - Porter Generic Strategies
- ITM-AK - Prinzipien des EU-Rechts
- ITM-AK - Privatrecht vs Öffentliches Recht
- ITM-AK - Produktlebenszyklus
- ITM-AK - QM-Instrumente
- ITM-AK - Rechts- und Handlungsfähigkeit
- ITM-AK - Rechtsakte der EU
- ITM-AK - SWOT-Analyse
- ITM-AK - Shareholder vs Stakeholder Value
- ITM-AK - Staatsaufbau Österreich
- ITM-AK - Strategische Preisgestaltung
- ITM-AK - Strategisches Controlling
- ITM-AK - Stufenbau der Rechtsordnung
- ITM-AK - Subjektive Rechte Pflichten Obliegenheiten
- ITM-AK - Subsumption
- ITM-AK - Umgründungsrecht
- ITM-AK - Urheberrecht und gewerblicher Rechtsschutz
- ITM-AK - Value in Healthcare
- ITM-AK - Variable und fixe Kosten
- ITM-AK - Verfassungsrecht und Verwaltungsrecht
- ITM-AK - Vergaberecht
- ITM-AK - Verknüpfung Strategisches und Finanzielles Management
- ITM-AK - VfGH und VwGH
- ITM-AK - Wettbewerbsrecht
- ITM-AK - Wichtige ISO-Normen
- ITM-AK - Zertifizierung und Akkreditierung
- ITM-AK - Zwingendes vs Dispositives Recht
- ITM-AK - Anmerkungen und Lagebericht

**Einschätzung:** Bei atomaren Konzepten wie „Vision" oder „BCG-Matrix" ist ein Spezifikation-Teil schwer sinnvoll zu erzwingen. Praktische Auswirkung für das Lernen: keine. Das Ein-Ebenen-Format ist im Vault etabliert und konsistent angewendet. Empfehlung: Konvention formal akzeptieren oder explizit als Ausnahmeregel dokumentieren, nicht en masse umbenennen (würde alle bestehenden Wiki-Links brechen).

Keine Verstöße bei: Unterstrichen statt Bindestriche, doppelten Bindestrichen, Slashes im Dateinamen.

---

### 1.2 Frontmatter-Vollständigkeit

**Keine Verstöße.** Alle 104 Notes haben:
- Genau einen Fach-Tag `#fach/vertiefung/itm-ak`
- Genau einen Typ-Tag (`#typ/konzept` oder `#typ/vorlesung`)
- Genau einen Status-Tag (`#status/offen`)

---

### 1.3 Quelle-Wiki-Link

**Fehlend in:** Keine – alle 98 Konzept-Notes enthalten mindestens einen Wiki-Link auf eine VL- oder Paper-Quell-Note.

**Broken Links (kritisch):** Drei Konzept-Notes verlinken auf `[[ITM-AK - Paper - Porter-Lee 2013 - Value-based Healthcare]]`, das **nicht existiert**:

- **ITM-AK - Bundled Payments und Value-Based Reimbursement** (Quelle-Feld)
- **ITM-AK - Care Delivery Value Chain** (Quelle-Feld, Link erscheint zweimal)
- **ITM-AK - Value in Healthcare** (Quelle-Feld)

Hintergrund: Das PDF `02_Porter_Lee_2013___The_Strategy_That_Will_Fix_Healthcare.pdf` liegt im Vault unter `Folien/IT-Management ausgewählte Kapitel/Paper/`, wurde aber nie als Paper-Note angelegt. Diese drei Notes haben keine gültige Quell-Note und hängen damit ohne Verbindung zur Vault-Struktur.

---

### 1.4 Verwaiste Notes (nicht im MOC)

**Keine.** Alle 104 Notes sind im MOC `ITM-AK - MOC.md` verlinkt.

---

### 1.5 Tote MOC-Verweise

**Keine.** Die drei Cross-Fach-Links im MOC-Abschnitt „Cross-Fach-Verbindungen" (`[[SM - MOC]]`, `[[ITPM - MOC]]`, `[[BPM - MOC]]`) lösen sich korrekt auf – die entsprechenden MOC-Dateien existieren in `00_MOCs/`.

*Hinweis zur Prüfmethodik: Mein initialer Bash-Check verortete die MOC-Dateien fälschlicherweise nur im ITM-AK-Ordner. Die zweite Prüfung gegen `00_MOCs/` bestätigte die korrekte Auflösung.*

---

### 1.6 Mögliche Doppelungen

**Keine verdächtigen Überschneidungen.** Alle ähnlich benannten Note-Cluster (TDABC × 2, Costing Myth × 3, Finanzierung × 3, IT-Management × 3, Strategie × 3, VL × 5) sind intentionale thematische Splits, keine Duplikate.

Einzige Beobachtung: `ITM-AK - Balanced Scorecard` (Konzept-Note) und `ITM-AK - VL - Balanced Scorecard und Qualitätsmanagement` (Quell-Note) überschneiden sich thematisch – das ist aber Absicht und template-konform.

---

### 1.7 Status-Verteilung

- `#status/offen`: **104**
- `#status/geprüft`: **0**

Alle Notes sind noch ungeprüft (Neuzustand nach Erstbefüllung). Das ist korrekt für den Workflow-Stand vor Phase 2.

---

## Stufe 2 – Quelltreue-Stichprobe

### Geprüfte Notes

1. **ITM-AK - Strategie - Definition** ← ITM-AK - VL - IT-Management Einführung und Finance ← `01_Management und Finance.pdf`
   - Bewertung: ✓ Quelltreu
   - Befund: Alle Kernaussagen direkt aus den Folien ableitbar. Porter-Zitat auf Folie 16 wörtlich übernommen und korrekt attribuiert. Ryanair-Beispiel (Folie 17), Wertvolle-Position-Aussage (Folie 20/21) und Kurz-und-bündig-Tabelle (Folie 28) exakt abgebildet.
   - Keine Ergänzung ohne Kennzeichnung gefunden.

2. **ITM-AK - Five Forces - Porter** ← ITM-AK - VL - Controlling ← `02_Controlling.pdf`
   - Bewertung: ✓ Quelltreu
   - Befund: Folie 9 enthält nur das Diagramm mit 5 Beschriftungen (Neue Marktteilnehmer, Anbieter, Rivalitäten, Kunden, Substitute) – die Note gibt das exakt wieder und markiert die Erläuterungen der einzelnen Kräfte explizit als „eigene Antwort, basierend auf Standardwissen". Das Video-Symbol ist korrekt erwähnt.
   - Marginale Unschärfe: Die Note sagt „bezeichnet Porter explizit nicht", der Folientitel ist aber „Die 5 Kräfte von Porter" – Porter wird also erwähnt. Kein inhaltliches Problem, aber etwas missverständlich formuliert.

3. **ITM-AK - Porter Generic Strategies** ← ITM-AK - VL - Controlling ← `02_Controlling.pdf`
   - Bewertung: ✓ Quelltreu
   - Befund: Folie 16 zeigt exakt die 2×2-Matrix mit den vier Feldern Cost leadership / Differentiation leadership / Cost focus / Differentiation focus und dem Hinweis „Vision – anders sein als andere (Porter)". Note trifft das pixelgenau. Elaborationen zu den Quadranten korrekt als „eigene Antwort" markiert.

4. **ITM-AK - Qualität - Donabedian-Dimensionen** ← ITM-AK - VL - Balanced Scorecard und Qualitätsmanagement ← `03_BSC_QM.pdf`
   - Bewertung: ✓ Quelltreu
   - Befund: Folie 5 nennt exakt „Nebulöser Begriff, viele Definitionen, viele Erwartungen (oder auch nicht)" und die drei Dimensionen (Strukturelle / Prozess / Ergebnis) mit Quelle „Donabedian, 1966, et al." – alles korrekt übernommen. Die Erläuterungstabelle ist explizit als „eigene Antwort, basierend auf Donabedian-Standardliteratur" deklariert.

5. **ITM-AK - Balanced Scorecard** ← ITM-AK - VL - Balanced Scorecard und Qualitätsmanagement ← `03_BSC_QM.pdf`
   - Bewertung: ✓ Quelltreu
   - Befund: Folie 2 enthält zwei Bilder (BSC-Originaldiagramm aus Kaplan/Norton 1992), Text ist nicht extrahierbar (Embedded Image). Die Note attribuiert das Diagramm korrekt als Kaplan/Norton 1992-Original und nennt die vier Perspektiven (Financial, Customer, Internal Business, Innovation and Learning) mit den spezifischen Leitfragen – konsistent mit dem bekannten HBR-Original. Die Ergänzungs-Sektion flaggt die Jahresangaben (1992, 2004) korrekt als nicht im PDF enthalten. BSC ≠ Strategy-Map-Abgrenzung ist als Ergänzung gekennzeichnet.
   - Einschränkung: Diagramm-Inhalt nicht per Textextraktion verifizierbar (Image-Folie).

6. **ITM-AK - ISO 9001-2015** ← ITM-AK - VL - Balanced Scorecard und Qualitätsmanagement ← `03_BSC_QM.pdf`
   - Bewertung: ⚠ Teilweise
   - Befund: Die Hauptkapitel-Tabelle (Folie 11) ist wortgetreu aus dem Folienmaterial übernommen – perfekte Quelltreue für den Kernteil. **Nicht gekennzeichnete Ergänzung:** Die Aussage „Klausel-Nummern beginnen bei 4, weil 1–3 organisatorische Vorworte sind (Anwendungsbereich, normative Verweise, Begriffe)" steht nicht auf den Folien. Ebenso: „Die 2015er-Version führte den PDCA-Zyklus als zentrales Modell und High-Level Structure ein" (Abgrenzungs-Sektion) ist Standardwissen über ISO-Normen, aber nicht im PDF belegt. Beide Stellen fehlen in der Ergänzungs-Sektion.
   - Konkrete Stelle: Folie 6 zeigt lediglich „PDCA-Zyklus – ISO 9001" mit einem Bild-Link; die PDCA-zu-Klausel-Zuordnung (Plan=6, Do=7+8, Check=9, Act=10) ist inhaltlich korrekt, aber das Bild ist nicht extrahierbar – die Note behauptet hier mehr als der zugängliche Folientext hergibt.

7. **ITM-AK - DRG und LKF** ← ITM-AK - VL - Controlling ← `02_Controlling.pdf`
   - Bewertung: ✓ Quelltreu
   - Befund: Folien 50–54 gut abgedeckt. Hintergrund (Folie 50), Kodierungslogik (Folie 51), LKF-Struktur (Folie 53) exakt abgebildet. Die konkreten Punktwerte (1.860 / 3.383) stammen aus einem Screenshot auf Folie 54 (Wörndle 2016, S. 15), der nicht per Text extrahierbar ist – die Note vermerkt das korrekt als Bildquelle. Note ist ehrlich über die Grenzen des Folienmaterials.

8. **ITM-AK - TDABC - Time Driven Activity Based Costing** ← ITM-AK - Paper - Porter-Kaplan 2011 - TDABC ← `04_Porter_Kaplan_2011__How_to_solve_the_cost_crisis_in_health_care.pdf`
   - Bewertung: ⚠ Nicht vollständig verifizierbar (scanned PDF)
   - Befund: Das Quell-PDF ist vollständig als gescanntes Image gespeichert – keine Textextraktion möglich (alle 17 Inhaltsseiten = image-only). Inhaltlich wirkt die Note sehr spezifisch und konsistent: Patient-Jones-Beispiel mit konkreten Namen (Administrator Allen, Nurse White, Physician Green), exakten Cost Rates ($45, $65, $300/h) und der Gesamtkostenberechnung ($84,50). Diese Spezifität ist eher ein Zeichen tatsächlicher Paper-Lektüre als einer Halluzination aus Allgemeinwissen.
   - Empfehlung: Manuelle Stichprobe direkt im PDF (Print/Reader) beim nächsten Lerndurchgang. Besonderes Augenmerk auf die Capacity-Cost-Rate-Formel und das Patient-Jones-Beispiel.

---

### Honeypot-Check

Folgende Honeypot-Themen wurden explizit geprüft:

- **Balanced Scorecard (4 Perspektiven, Strategy Maps, Kausalketten):** ✓ Sauber. Die Note trennt klar zwischen dem Folieninhalt (Diagramm, 4 Perspektiven) und dem Ergänzungswissen (Strategy Maps 2004, Kaplan/Norton-HBR-Einordnung). Die klassische Verwechslungsgefahr BSC ↔ Strategy Map ist korrekt behandelt.
- **Porter Five Forces (5 Kräfte, Branchenstrukturanalyse):** ✓ Sauber. Folie enthält nur das Diagramm; Erläuterungen sind als extern gekennzeichnet. Kein Standard-Lehrbuch-Text eingeschleust.
- **Porter Generic Strategies (Cost Leadership, Differentiation, Focus, Stuck in the Middle):** ✓ Sauber. 2×2-Matrix identisch mit Folie; eigene Beschreibungen pro Quadrant korrekt als extern markiert.
- **TDABC (Time-Driven Activity-Based Costing, Capacity Cost Rate):** ⚠ Nicht verifizierbar wegen gescanntem PDF. Kein offensichtlicher Lehrbuch-Einschub; das 7-Schritte-Konzept ist korrekt in eine separate Note ausgelagert statt eingebettet.
- **Donabedian (Struktur/Prozess/Ergebnis-Qualität):** ✓ Sauber. Folie 5 nennt nur die drei Dimensionen; alle Erläuterungen sind als Ergänzung deklariert. Besonders gut: Urheber und Jahreszahl (Donabedian, 1966) korrekt aus dem PDF übernommen.
- **ISO 9001 (Anforderungskapitel, prozessorientierter Ansatz):** ⚠ Teilweise. Kernkapitel perfekt aus Folie, aber zwei Aussagen ohne Ergänzungs-Kennzeichnung (Klausel-Nummerierungslogik, High-Level-Structure-Verweis).
- **DRG/LKF (Berechnungslogik, Komponenten):** ✓ Sauber. LKF-Systemkomponenten direkt aus Folie 53 übernommen, Einschränkungen bei Bildquellen korrekt vermerkt.

---

## Empfehlungen

### Sofort handeln (vor Phase 2)

1. **Paper-Note für Porter-Lee 2013 anlegen:** `ITM-AK - Paper - Porter-Lee 2013 - Value-based Healthcare.md` erstellen (Quelle: `02_Porter_Lee_2013___The_Strategy_That_Will_Fix_Healthcare.pdf` liegt bereits im Vault). Die drei Notes **Bundled Payments und Value-Based Reimbursement**, **Care Delivery Value Chain** und **Value in Healthcare** haben derzeit broken Quelle-Links und sind damit strukturell verwaist. PDF-Lektüre und Konzept-Notes aus dem Porter-Lee 2013 Paper stehen noch aus – das ist ein inhaltlich bedeutsamer Lücke, da Value-Based Healthcare ein zentrales Prüfungsthema ist.

2. **ISO 9001-2015 Note bereinigen:** Die zwei nicht gekennzeichneten Ergänzungen (Klausel-Nummernlogik 1–3 als Vorwort, Verweis auf High-Level-Structure 2015) in die Ergänzungs-Sektion verschieben. Geringer Aufwand, aber relevant für die Quelltreue-Regel.

### Nice-to-have (kann warten)

3. **TDABC manuell spot-checken:** Da das Paper gescannt ist, beim nächsten Lerndurchgang kurz im PDF-Reader nachschlagen: Patient-Jones-Beispiel (S. 51–52), Capacity-Cost-Rate-Formel, und die 7-Schritte-Liste. 15 Minuten Arbeit für ein Honeypot-Thema.

4. **Naming-Konvention klären:** Entscheiden, ob das Ein-Ebenen-Format (`ITM-AK - <Thema>` ohne Spezifikation) akzeptiert wird oder 55 Notes umbenannt werden sollen. Da alle Wiki-Links intern konsistent sind und das Lernen nicht beeinträchtigt wird, ist Umbenennung kaum sinnvoll. Empfehlung: Konvention in INSTRUCTIONS.md um „Ausnahme bei atomaren Einzelbegriffen" ergänzen.

5. **Porter-Lee 2013 Konzept-Notes nachholen:** Nach Anlage der Paper-Note die wichtigsten Konzepte aus dem Paper extrahieren (Value Equation, VBHC-Definition, Care Delivery Value Chain Details, etc.) – diese sind aktuell über die drei oben genannten Notes verstreut, haben aber keine echte Quell-Note.

### Beobachtungen / Anmerkungen

- **Gesamtqualität überdurchschnittlich gut.** Die Notes unterscheiden konsequent zwischen Folieninhalt und eigener Elaboration. Die Ergänzungs-Sektion wird korrekt und sparsam eingesetzt. Keine einzige Note wurde mit erfundenen Definitionen aus dem Allgemeinwissen aufgebläht, ohne Kennzeichnung.
- **Prüfungsrelevanz-Sektionen durchgehend stark.** Diskussionsfragen und Anschlussfragen sind praxisnah und prüfungsrealistisch formuliert – das ist der lernkritische Teil und er ist in allen geprüften Notes gut ausgearbeitet.
- **5 VL-Notes und 1 Paper-Note als Quell-Anker vorhanden** – der Fach-Ordner ist strukturell vollständig für die bisher verarbeiteten PDFs. Die Lücke ist ausschließlich das Porter-Lee 2013 Paper.
- **0 geprüfte Notes** – das ist der normale Ausgangszustand. Nach Abschluss des manuellen Lernens in Phase 2 sollten geprüfte Notes auf `#status/geprüft` gesetzt werden.
