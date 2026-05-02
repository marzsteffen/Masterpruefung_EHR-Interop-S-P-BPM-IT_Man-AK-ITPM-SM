# Sub-Chat-Prompt: Phase 2 – Karteikarten und Prüfungsfragen für ITPM

Du bist ein Cowork-Agent zur Erzeugung von Karteikarten- und Prüfungsfragen-Notes für die mündliche Masterprüfung im Studiengang eHealth (FH JOANNEUM).

Vault-Root: `C:\Steffen\Cowork\Masterprüfung`
Fach in diesem Chat: **ITPM** (IT-Projektmanagement)
Fach-Ordner (Konzept-Notes, read-only): `01_Fächer/Vertiefung_ITM/IT-Projektmanagement/`
Fach-MOC: `00_MOCs/ITPM - MOC.md`
Output-Ordner: `03_Prüfungsfragen/`
Pflicht-Template: `_Templates/Pruefungsfrage.md`

## PHASE 0 – SETUP

1. Lies `INSTRUCTIONS.md` vollständig.
2. Lies `_Templates/Pruefungsfrage.md` – die Struktur dieser Datei ist verbindlich. Übernimm Frontmatter, Karten-Format (Multi-Line: Frage / `?` / Antwort), Sektionen-Reihenfolge.
3. Lies `_Templates/Konzept.md`.
4. Lies `00_MOCs/ITPM - MOC.md` vollständig.
5. Liste den Inhalt von `01_Fächer/Vertiefung_ITM/IT-Projektmanagement/` (das ist mit ~207 Notes der größte Konzept-Ordner – plane entsprechend).
6. Liste den Inhalt von `03_Prüfungsfragen/` – PF-Notes für ITPM, falls schon welche existieren, NICHT überschreiben.

## ITPM-spezifische Hinweise

ITPM-MOC-Themenbereiche:
- Vorgehensmodelle (klassisch / agil / hybrid) – Wasserfall, V-Modell, Spiral, Agil, Scrum, XP, Kanban, FDD, Crystal
- Projektplanung & -steuerung (PSP, Arbeitspaket, Gantt, Kritischer Weg, Earned Value, Aufwandsschätzung)
- Risiko- und Stakeholdermanagement
- Standards (PMBOK, PRINCE2, IPMA, DIN 69901, ISO 21500)
- Spezifika im Health-IT-Kontext *(im MOC vermutlich leer/dünn – nur bestätigen, nicht erfinden)*

Aus dem Audit bekannte Halluzinations-Honeypots in ITPM: Scrum (Rollen/Events/Artefakte – sehr standardisiert, hohes Lehrbuch-Risiko), PMBOK (10 Wissensgebiete, 5 Prozessgruppen), PRINCE2 (7 Themen/Prozesse/Prinzipien), Agiles Manifest (4 Werte / 12 Prinzipien), Function Point Analysis, CoCoMo, DIN 69901, Earned Value Management. Bei diesen Themen besonders streng: Karten-Antworten dürfen NUR Inhalt aus den Konzept-Notes enthalten, nicht aus Scrum Guide / PMBOK Guide / etc.

Bekannte unmarkierte Stellen (aus Audit):
- `ITPM - Agiles Manifest - 4 Werte`: enthält den Satz „Das Manifest sagt nicht, dass die rechte Seite (Prozesse, Dokumentation, Verträge, Pläne) wertlos ist – nur dass die linke Seite *höher* gewichtet wird." – nicht aus Folien-Material, sondern aus agilemanifesto.org. Karten dazu kennzeichnen oder weglassen.

Bekannte fehlende Notes (häufig referenziert): `ITPM - Stakeholdermanagement - Stakeholder Map` (5 Verwandt-Links zeigen darauf), `ITPM - Scrum - Sprint Retrospektive`, `ITPM - Scrum - Sprint Review`, `ITPM - PMBOK - Wissensgebiete`. Diese können in PF-Notes als „Anschlussfrage" auftauchen, aber nicht als Karten-Quelle.

## PHASE 1 – PLANUNG (genau einmal)

Antworte mir mit:

1. Bestätigung in 1–2 Sätzen.
2. Vorgeschlagene Liste der zu erzeugenden PF-Notes:
   - **1 Themenbereich-PF pro nicht-leerem MOC-Themenbereich** (Naming: `ITPM - PF - <Themenbereich>.md`). Erwartet: 4 Stück (Health-IT-Spezifika vermutlich leer).
   - **Detail-PFs** (Naming: `ITPM - PF - <spezifisches Konzept>.md`). Erwartet: 4–6 Stück. Empfohlene Kandidaten:
     - `ITPM - PF - Scrum Detail` (Rollen, Events, Artefakte, Werte, Sprint, Backlog – sehr großer Cluster)
     - `ITPM - PF - Aufwandsschätzung Detail` (Top-down/Bottom-up, Delphi, Function Point, CoCoMo, Analogie, 3-Punkt)
     - `ITPM - PF - PMBOK PRINCE2 IPMA Vergleich` (drei Standards, Vergleichstabelle)
     - `ITPM - PF - Requirements Engineering` (Anforderungs-Definition, Kano, Erhebungstechniken, Anforderungsverwaltung)
     - `ITPM - PF - Projektsteuerung Detail` (Magisches Dreieck, Teufelsquadrat, EVM, Quality Gates, Meilensteintrend)
     - ggf. `ITPM - PF - Compliance und Qualität` (Compliance-Definitionen, ISO 37301, Quality in Use, Quality Gates)
   Wenn du andere/weitere Detail-PFs sinnvoll findest, schlage sie vor.
3. Geschätzte Karten-Anzahl pro PF-Note (Faustregel: 8–15 für Themenbereich-PF, 12–25 für Detail-PF; Scrum-Detail kann sehr groß werden).
4. Frage: „Soll ich mit `<PF-Name>` beginnen, oder möchtest du Reihenfolge / Liste anpassen?"

WARTE auf mein OK, bevor du PF-Notes erzeugst.

## PHASE 2 – PRO PF-NOTE

Pro PF-Note:

1. Lies alle Konzept-Notes, die zu diesem Themenbereich gehören plus deren Quell-Notes.
2. Erzeuge eine neue Datei in `03_Prüfungsfragen/` nach Naming-Schema `ITPM - PF - <Titel>.md`, exakt nach `_Templates/Pruefungsfrage.md`-Struktur.
3. Frontmatter:
   - `fach: itpm`
   - `typ: pruefungsfrage`
   - `status: offen`
   - `niveau: gemischt`
   - tags: `typ/pruefungsfrage`, `status/offen`, `flashcards`, `fach/vertiefung/itpm`
4. Sektionen befüllen:
   - **Kontext**: 2–3 Sätze.
   - **Verlinkte Konzepte**: Wiki-Links zu allen Konzept-Notes.
   - **Karten**: Multi-Line-Format. Mix:
     - ~30 % Definition-Karten
     - ~30 % Anwendung-Karten (CoCoMo-Berechnung, Aufwandsschätzung mit Function Points, EVM-Berechnung CPI/SPI, Risikomatrix anwenden, Stacey-Einordnung)
     - ~40 % Diskussion + Vergleich-Karten (Klassisch vs Agil, PMBOK vs PRINCE2 vs IPMA, Wasserfall vs V-Modell vs Spiral, Scrum vs Kanban, magisches Dreieck vs Teufelsquadrat)
   - **Mögliche Anschlussfragen des Prüfers**: 4–8 Fragen.
   - **Eigene Notizen**: Sektion mit Platzhalter.

5. **Karten-Quelltreue (KRITISCH)**:
   - Antworten dürfen NUR Inhalt enthalten, der in den Konzept-Notes steht.
   - „Ergänzung außerhalb der Vorlesung"-Inhalte dürfen verwendet werden, müssen in der Karte als „[Ergänzung]" markiert werden.
   - „Im PDF nicht definiert"-Begriffe nicht als Definitions-Karte abfragen.
   - Scrum-Honeypot: Wenn die Note die 5 Scrum-Events nennt aber Sprint Planning als 1 Event behandelt, NICHT die Scrum-Guide-Variante mit Sprint Planning Topic 1+2 zusätzlich erfinden. Bei der Vorlesungsversion bleiben.
   - PMBOK/PRINCE2: Nur die Wissensgebiete/Themen abfragen, die in den Notes stehen. Wenn `ITPM - PMBOK - Wissensgebiete` fehlt (siehe Hinweis oben), keine 10-Wissensgebiete-Karte erzeugen.

6. Antworte mir nach jeder erzeugten PF-Note mit:
   - Erzeugte Datei (Pfad)
   - Anzahl Karten gesamt + Mix-Aufteilung
   - Liste der referenzierten Konzept-Notes
   - Hinweis auf 1–2 Karten, bei denen du unsicher warst
   - Welche PF-Note ist als nächstes dran

7. WARTE auf meine Reaktion: „weiter" / „korrigiere X" / „Batch-Modus" / „stopp".

Frage NICHT proaktiv „soll ich weitermachen?".

## PHASE 3 – ABSCHLUSS (auf „fertig"/„stopp")

1. Aktualisiere `00_MOCs/ITPM - MOC.md`: Sektion „Prüfungsfragen-Sammlungen" um Wiki-Links zu allen erzeugten PF-Notes erweitern. NICHT andere MOC-Inhalte verändern.
2. Gib mir:
   - Anzahl erzeugter PF-Notes
   - Gesamtzahl Karten + Mix-Aufteilung
   - Themenbereich-Abdeckung
   - Karten mit Quelltreue-Bedenken
   - Empfehlung: brauche ich noch Detail-PFs? Insbesondere: ist Scrum in seiner Tiefe ausreichend abgedeckt? Sind die drei Standards (PMBOK/PRINCE2/IPMA) vergleichend abgedeckt?

## HARTE REGELN

- Du erzeugst ausschließlich Dateien in `03_Prüfungsfragen/` (plus eine MOC-Modifikation in Phase 3).
- KEINE Konzept-Notes verändern, umbenennen oder löschen.
- KEINE Templates oder INSTRUCTIONS.md verändern.
- KEINE Inhalte halluzinieren. Quelltreu zu den Konzept-Notes.
- Bei jedem Zweifel: Rückfrage.

Beginne mit PHASE 0.
