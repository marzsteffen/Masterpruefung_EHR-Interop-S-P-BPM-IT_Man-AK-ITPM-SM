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

**Erforderliches Plugin:** [Spaced Repetition](https://github.com/st3v3nmw/obsidian-spaced-repetition)

Plugin-Konfiguration (Settings → Spaced Repetition):
- Flashcard tags: `#flashcards`
- Single-line card separator: `::`
- Multi-line card separator: `?`
- Convert highlights to clozes: an
- Tags to ignore: `#status/offen` (optional, falls noch nicht geprüfte Karten ausgeschlossen werden sollen)

## Arbeitsablauf

1. **Phase 1 – Extraktion (aktuell):** Vorlesungs-PDFs werden über Cowork in den Vault eingearbeitet. Pro Chat ein PDF (oder eine Vorlesungseinheit). Cowork erzeugt atomare Konzept-Notes plus eine Vorlesungs-Übersichtsnote und befüllt das passende Fach-MOC.
2. **Phase 2 – Lernmaterial:** Nach Abschluss der Extraktion werden im Claude-Projekt Zusammenfassungen, Karteikarten und Prüfungsfragen generiert.
3. **Phase 3 – Lernen:** Spaced Repetition Plugin, gezielt nach Tag-Hierarchie (z. B. nur `#flashcards/allgemein/msi`).

## Wichtige Dateien

- `INSTRUCTIONS.md` – Anweisungen für Cowork (in jedem Folge-Chat zuerst lesen lassen!)
- `_Templates/` – Vorlagen für Notes
- `00_MOCs/` – Maps of Content als Einstiegspunkte pro Fach und Bereich

## Sprache

Notes, Karten und Templates sind auf **Deutsch**. Englische Fachbegriffe (FHIR, OAuth2, RBAC, ITIL, …) bleiben englisch und werden bei Erstnennung kurz erklärt.
