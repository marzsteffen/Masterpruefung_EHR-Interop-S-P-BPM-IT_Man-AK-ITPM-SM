---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Prozessmanagement Grundlagen (PzM-Kompakt)]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - Methode - Schnittstellenanalyse

> [!info] Kurzdefinition
> Eine **Schnittstelle** ist ein Übergabepunkt zwischen Arbeitsabläufen (Prozessen), durchgeführt von Personen oder Maschinen. Die **Schnittstellenanalyse** identifiziert solche Übergaben und prüft sie systematisch auf Verzögerungen, Informations­verluste und Ineffizienz.

## Beschreibung

Folien 121–122. Schnittstellenverluste resultieren aus **Verzögerungen, Informationsverlusten, Ineffizienz** etc. (Folie 121). Bereits Folie 22 hatte die typischen Prozentzahlen gezeigt, wie viel Information an einzelnen Schnittstellen verloren geht.

### Drei Arten von Schnittstellen (Folie 121)

- **Mensch-zu-Mensch**: Kommunikation zwischen zwei Personen.
- **Mensch-zu-System**: Dateneingabe in ein ERP-System.
- **System-zu-System**: Automatisierter Datenaustausch zwischen IT-Systemen.

### Tabellen-Muster (Folie 122)

Pro Prozessschritt werden erfasst:

| Spalte | Inhalt |
|---|---|
| Prozessschritt | Aktivitätsname |
| Von (Stelle/Rolle) | wer übergibt |
| Zu (Stelle/Rolle) | wer empfängt |
| Was wird übergeben | Information / Material |
| In welcher Form | Mail / Formular / mündlich / System |
| Bemerkung oder Maßnahme | inkl. Verantwortlichkeit & Termin |

Beispiele aus den Folien:
- **Limonadenstand**: Inhaber → Helfer, Einkaufsliste, mündlich → Inhaber informiert Helfer täglich um 8:00 Uhr.
- **Verkehrsunternehmen**: Verkehrsplanung → Betriebsleitung, Fahrplan-Dokument (PDF/Excel), per E-Mail und im internen System → Freigabe bis zum 15. des Vormonats durch Planer.

## Bestandteile / Aufbau

- Identifikation aller Schnittstellen entlang des Prozessflusses
- Klassifikation (M↔M, M↔S, S↔S)
- Erfassung von Inhalt, Übergabeform und Verantwortlichkeit

## Beispiel

Klinisch: Schnittstelle Anästhesie → OP-Team. Was wird übergeben: Patient + ASA-Klassifikation + Medikamentenliste; wie: WHO Surgical Safety Checklist mündlich + Anästhesieprotokoll digital. Risiko: unvollständige Übergabe → falsches Medikament. Maßnahme: standardisiertes Übergabe-Tool (SBAR, im PDF nicht erwähnt).

## Abgrenzung

- **Schnittstellenanalyse ≠ Wertschöpfungsanalyse.** Wertschöpfung pro Schritt; Schnittstellenanalyse pro Übergabe zwischen Schritten.
- **Schnittstelle ≠ Aktivität.** Schnittstellen sind Punkte, keine Tätigkeiten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Was sind Schnittstellen, und welche drei Arten unterscheidet die Vorlesung?"

**Anwendungsfrage:** „Identifizieren Sie zwei kritische Schnittstellen im Hernien-Pfad und schlagen Sie eine Maßnahme vor."

**Diskussionsfrage:** Warum sind Mensch-zu-Mensch-Übergaben in der Klinik die größte Fehlerquelle? – Mündlich, situationsabhängig, ohne Protokoll. Bezug zu [[BPM - Paper - To Err Is Human]] (kommunikationsbedingte Fehler als ein Hauptcluster).

**Mögliche Anschlussfragen:**
- Welche Spalten enthält das Schnittstellen-Tabellen-Muster?
- Wie hängt die Schnittstellenanalyse mit der Prozessorientierung zusammen?
- Welche Maßnahmen reduzieren Schnittstellenverluste?

## Verwandt

- [[BPM - Grundprinzip - Prozessorientierung]]
- [[BPM - Methode - Wertschoepfungsanalyse]]
- [[BPM - Methode - FMEA]]
- [[BPM - Phase 2 - Prozessidentifikation und Abgrenzung]]
- [[BPM - Paper - To Err Is Human]]

## Quelle

- Vorlesung: [[BPM - VL - Prozessmanagement Grundlagen (PzM-Kompakt)]]
- Folien/Seitenangabe: Folien 22 (Schnittstellenverluste), 121–122
