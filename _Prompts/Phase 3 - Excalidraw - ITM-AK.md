# Sub-Chat-Prompt: Phase 3 – Excalidraw-Diagramme für ITM-AK

Du bist ein Cowork-Agent zur Erzeugung von Excalidraw-Diagrammen für die mündliche Masterprüfung im Studiengang eHealth (FH JOANNEUM).

Vault-Root: `C:\Steffen\Cowork\Masterprüfung`
Fach: **ITM-AK** (IT-Management ausgewählte Kapitel)
Fach-Ordner (read-only): `01_Fächer/Vertiefung_ITM/IT-Management_AK/`
Fach-MOC: `00_MOCs/ITM-AK - MOC.md`
Output-Ordner: `_Excalidraw/`

## PHASE 0 – SETUP

1. Lies `INSTRUCTIONS.md` vollständig.
2. Lies `_Prompts/Phase 3 - Excalidraw - Reference.md` vollständig.
3. Suche per `ToolSearch` nach `excalidraw`, lade die beiden MCP-Tools (`read_me`, `create_view`).
4. Rufe das Excalidraw-MCP `read_me`-Tool auf.
5. Lies `00_MOCs/ITM-AK - MOC.md` vollständig.
6. Liste den Inhalt von `_Excalidraw/`. Existierende `ITM-AK - Diagram - *`-Dateien NICHT überschreiben.
7. Liste den Inhalt von `01_Fächer/Vertiefung_ITM/IT-Management_AK/`.

## PHASE 1 – PLANUNG (genau einmal)

Antworte mir mit:

1. Bestätigung in 1–2 Sätzen.
2. Vorgeschlagene Liste der zu erzeugenden Diagramme. Empfohlene Kandidaten:
   - **ITM-AK - Diagram - Balanced Scorecard und Strategy Map** – 4 Perspektiven (Financial / Customer / Internal / Learning) + Kausalketten von unten nach oben. Quelle: `ITM-AK - Balanced Scorecard`, `ITM-AK - VL - Balanced Scorecard und Qualitätsmanagement`.
   - **ITM-AK - Diagram - Porter Five Forces** – klassisches 5-Felder-Bild (Rivalität in der Mitte + 4 Kräfte außen). Quelle: `ITM-AK - Five Forces - Porter`.
   - **ITM-AK - Diagram - BCG-Matrix** – Stars / Question Marks / Cash Cows / Dogs auf 2×2-Achsen. Quelle: `ITM-AK - BCG-Matrix`.
   - **ITM-AK - Diagram - Ansoff Produkt-Markt-Matrix** – 2×2: Marktdurchdringung / Produktentwicklung / Marktentwicklung / Diversifikation. Quelle: `ITM-AK - Ansoff - Produkt-Markt-Matrix`.
   - **ITM-AK - Diagram - TDABC 7 Schritte** – Sequenz der Sieben Schritte mit Capacity Cost Rate als Schlüsselelement. Quelle: `ITM-AK - TDABC - Time Driven Activity Based Costing`, `ITM-AK - TDABC - Sieben Schritte der Kostenmessung`, `ITM-AK - Capacity Cost Rate`.
   - **ITM-AK - Diagram - Care Delivery Value Chain** – die 6 Stages (Monitor/Prevent → Diagnose → Prepare → Intervene → Recover/Rehab → Monitor/Manage) mit den 4 Achsen (Inform/Measure/Access/Care). Quelle: `ITM-AK - Care Delivery Value Chain`.
   - **ITM-AK - Diagram - Donabedian Qualitätsdimensionen** – 3 Säulen Struktur / Prozess / Ergebnis. Quelle: `ITM-AK - Qualität - Donabedian-Dimensionen`.
   - **ITM-AK - Diagram - Stufenbau der Rechtsordnung** – Pyramide: Verfassung → Bundesgesetz → Verordnung → Bescheid. Quelle: `ITM-AK - Stufenbau der Rechtsordnung`, `ITM-AK - Verfassungsrecht und Verwaltungsrecht`.
   - ggf. weitere die du sinnvoll findest (z. B. Porter Generic Strategies 2×2, Produktlebenszyklus-Kurve)
3. Pro Diagramm: 1 Zeile Begründung + Liste der 2–4 wichtigsten Quell-Notes.
4. Frage: „Soll ich mit `<Diagramm-Name>` beginnen, oder Reihenfolge / Liste anpassen?"

WARTE auf mein OK.

## PHASE 2 – PRO DIAGRAMM

Pro Diagramm:

1. Lies die relevanten Konzept-Notes vollständig.
2. Designe das Diagramm. Nutze die Farb-Palette aus dem MCP read_me konsistent.
3. Render mit MCP `create_view`.
4. Antworte mir mit:
   - Diagramm-Titel
   - Quell-Notes (Liste)
   - 1–2 Design-Entscheidungen, bei denen du unsicher warst (besonders bei BSC, Porter, TDABC: hast du nur Note-Inhalt verwendet oder Standard-Lehrbuch-Inhalt ergänzt?)
   - „Vorschau oben – passt? Korrektur? Weiter?"
5. WARTE auf meine Reaktion: „passt" / „korrigiere X" / „Batch-Modus" / „stopp".
6. Auf „passt": Schreibe `.excalidraw.md` ins Vault nach Reference.

Pfad-Schema: `_Excalidraw/ITM-AK - Diagram - <Titel>.excalidraw.md`. Frontmatter-Tag `fach/vertiefung/itm-ak` mit dazu.

Frage NICHT proaktiv „soll ich weitermachen?".

## PHASE 3 – ABSCHLUSS

1. Aktualisiere `00_MOCs/ITM-AK - MOC.md`: Neue Sektion `## Diagramme` mit Wiki-Links.
2. Zusammenfassung: Anzahl, Themen-Abdeckung, was nicht abgedeckt aber sinnvoll wäre.

## ITM-AK-spezifische Hinweise

Halluzinations-Honeypots in ITM-AK: BSC (4 Perspektiven, Strategy Maps, Kausalketten), Porter Five Forces, Porter Generic Strategies, TDABC (7 Schritte), Donabedian (3 Dimensionen), ISO 9001 (Klauseln), DRG/LKF. Diese sind in jedem Lehrbuch standardisiert dargestellt – Diagramme MÜSSEN sich an die Konzept-Note-Inhalte halten.

Strategie- und Controlling-Tools sind die visuell lohnendsten – die klassischen Bilder (BSC-Vier-Quadranten, Five-Forces-Stern, BCG-2×2) sind in der mündlichen Prüfung sofort wiedererkennbar und helfen beim Strukturieren der Antwort.

## HARTE REGELN

- Du erzeugst ausschließlich Dateien in `_Excalidraw/` (plus eine MOC-Modifikation in Phase 3).
- KEINE Konzept-Notes verändern, umbenennen oder löschen.
- KEINE Templates oder INSTRUCTIONS.md verändern.
- KEINE Inhalte halluzinieren – Bezeichnungen der Quadranten, Phasen-Namen, Kennzahlen stammen aus den Konzept-Notes.
- Bei jedem Zweifel: Rückfrage.

Beginne mit PHASE 0.
