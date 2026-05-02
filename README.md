# Masterprüfung eHealth – Lern-Vault

Vorbereitung auf die kommissionelle Masterprüfung an der FH JOANNEUM (Studiengang eHealth).

## Prüfungsfächer

**Allgemeines Fachgebiet: Medizinische Informatik**
- Advanced Security and Privacy (ASP)
- Medizinische Standards und Semantische Interoperabilität (MSI)
- Electronic Health Records (EHR)

**Vertiefungsrichtung: IT-Management**
- IT-Projektmanagement (ITPM)
- IT-Management ausgewählte Kapitel (ITM-AK)
- Servicemanagement (SM)
- Business Process Management (BPM)

## Setup

**Erforderliche Plugins:**

- [Spaced Repetition](https://github.com/st3v3nmw/obsidian-spaced-repetition) – Karteikarten-Reviews
- [Excalidraw](https://github.com/zsviczian/obsidian-excalidraw-plugin) – rendert die `.excalidraw.md`-Diagramme aus `_Excalidraw/` und erlaubt das Einbetten via `![[<KÜRZEL> - Diagram - …]]` in andere Notes
- [Obsidian Git](https://github.com/Vinzent03/obsidian-git) – Auto-Backup und Sync mit dem Remote-Repo

**Spaced-Repetition-Konfiguration** (Settings → Spaced Repetition):
- Flashcard tags: `#flashcards`
- Single-line card separator: `::`
- Multi-line card separator: `?`
- Convert highlights to clozes: an
- Tags to ignore: `#status/offen` (optional, falls noch nicht geprüfte Karten ausgeschlossen werden sollen)

**Excalidraw-Konfiguration** (Settings → Excalidraw):
- Default Excalidraw filename: keine speziellen Anpassungen nötig
- Diagramme liegen in `_Excalidraw/` mit Naming `<KÜRZEL> - Diagram - <Titel>.excalidraw.md`

**Obsidian-Git-Konfiguration** (Settings → Obsidian Git):
- Auto-Backup-Intervall: 30 Min (oder nach Geschmack)
- Auto-Pull beim Start: an
- Commit-Message-Template: optional

## Arbeitsablauf

1. **Phase 1 – Extraktion (abgeschlossen):** Vorlesungs-PDFs wurden über Cowork in den Vault eingearbeitet. Pro Chat ein PDF (oder eine Vorlesungseinheit). Cowork hat atomare Konzept-Notes plus eine Vorlesungs-Übersichtsnote erzeugt und das passende Fach-MOC befüllt.
2. **Phase 2 – Karteikarten und Prüfungsfragen (abgeschlossen):** Pro Fach ein Sub-Chat erzeugt PF-Notes in `03_Prüfungsfragen/` mit Karten im Spaced-Repetition-Multi-Line-Format und mündlichen-Prüfungs-Anschlussfragen.
3. **Phase 3 – Excalidraw-Diagramme:** Pro Fach ein Sub-Chat erzeugt visuelle Diagramme in `_Excalidraw/` für Architekturen, Prozess-Flows und Vergleiche.
4. **Phase 4 – Lernen:** Spaced Repetition Plugin, gezielt nach Tag-Hierarchie (z. B. nur `#flashcards` plus Fach-Tag-Filter), in Kombination mit den Diagramm-Embeds und PF-Diskussionsfragen.

## Vault-Struktur

- `00_MOCs/` – Maps of Content als Einstiegspunkte pro Fach (eines pro Prüfungsfach + Cluster-MOCs)
- `01_Fächer/` – atomare Konzept-Notes und Quell-Notes (VL/Paper), gegliedert nach Fach
- `02_Konzepte/` – fachübergreifende Konzepte (Cross-Fach-Brücken, optional)
- `03_Prüfungsfragen/` – Karteikarten und Prüfungsfragen-Notes mit Spaced-Repetition-Format
- `_Excalidraw/` – visuelle Diagramme im Obsidian-Excalidraw-Format
- `_Templates/` – Vorlagen für Notes (Konzept, Vorlesung, MOC, Prüfungsfrage)
- `_Audits/` – Qualitäts-Audit-Berichte aus der Vault-Befüllung
- `_Prompts/` – Sub-Chat-Prompts für die Phasen 2 und 3
- `_Attachments/` – Anhänge / Uploads
- `Folien/` – Original-Vorlesungs-PDFs und -Materialien (per `.gitignore` optional ausgeschlossen)
- `INSTRUCTIONS.md` – Anweisungen für Cowork (in jedem Folge-Chat zuerst lesen lassen!)

## Sprache

Notes, Karten und Templates sind auf **Deutsch**. Englische Fachbegriffe (FHIR, OAuth2, RBAC, ITIL, …) bleiben englisch und werden bei Erstnennung kurz erklärt.
