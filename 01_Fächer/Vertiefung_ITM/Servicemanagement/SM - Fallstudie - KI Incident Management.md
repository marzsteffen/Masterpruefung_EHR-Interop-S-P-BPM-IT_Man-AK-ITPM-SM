---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - Fallstudie - KI Incident Management

> [!info] Kurzdefinition
> Fallstudie eines Agrarhandelsunternehmens (Münster, ca. 6.500 Mitarbeitende, 400 Standorte, 46.000 Tickets/Jahr, 120 IT-Mitarbeiter): Hypothese, dass KI die Kategorisierung eingehender Störungen im Incident Management optimieren kann. Aufgabe an Studierende: Vergleich Genfer Wissensmanagement-Modell vs. Münchner Modell.

## Beschreibung

Folien 147–150 (Quelle: Frick, N., Brünker, F., Ross, B. et al. 2019).

**Unternehmenskontext** (Folie 149):
- Agrarhandelsunternehmen
- Münster, Deutschland
- 6.500 Mitarbeitende an über 400 Standorten
- 46.000 Tickets pro Jahr
- Interne IT-Abteilung mit 120 Mitarbeitenden, davon 10 im First Level Support

**Kontaktkanäle** (Folie 149): Telefon, E-Mail, Self-Service-Portal — alle leiten in den First-Level-Support.

**Klassischer Ablauf** (Folie 149): Identifikation → Protokollierung → Kategorisierung → Behebung → Wiederherstellung. Die Klassifizierung weist Tickets einer **Applikation** und einer **Gruppe** zu.

**KI-Hypothese** (Folie 150):
> „Hypothese: Durch den Einsatz von künstlicher Intelligenz kann die Kategorisierung eingehender Störungen im Incident Management optimiert werden."

Im Diagramm (Folie 150): Eingehendes Ticket → KI (Identifikation, Protokollierung, Kategorisierung) → Output Gruppe + Applikation → Behebung + Wiederherstellung in der internen IT-Abteilung (120 Mitarbeitende).

**Fragen zum KI-System** (Folie 150):
- Auf welcher (Daten-)Basis wurde das KI-System entwickelt?
- Was ist ein NLU-Modell? *(NLU = Natural Language Understanding — im PDF nicht weiter definiert)*
- Mit welcher Programmiersprache wurde das neuronale Netzwerk realisiert?
- Wie unterstützt „Wissensmanagement" die Entwicklung künstlicher Intelligenz?

**Aufgabe A2** (Folie 150):
> „Vergleichen Sie das **Genfer Wissensmanagement-Modell** und das **Münchner Modell** im Hinblick auf deren Praxistauglichkeit. Entscheiden Sie sich aus Praxissicht für eines der Modelle und begründen Sie Ihre Entscheidung."

(Quellenangabe: „siehe Moodle" — die Modelle werden im Foliensatz selbst nicht beschrieben. *Im PDF nicht definiert.*)

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Unternehmen | Agrarhandel, Münster, 6.500 MA, 400 Standorte |
| Volumen | 46.000 Tickets/Jahr |
| IT-Größe | 120 IT-MA, davon 10 First Level |
| Kanäle | Telefon, E-Mail, Self-Service-Portal |
| KI-Aufgabe | Kategorisierung eingehender Tickets (Applikation + Gruppe) |
| Verbleibende Schritte | Behebung + Wiederherstellung weiterhin durch IT-Abteilung |
| Forschungsfragen | NLU, Programmiersprache, Trainingsdaten, Wissensmanagement-Modell |

## Beispiel

Das Fallbeispiel selbst — Agrarhandel Münster — ist das Beispiel. Übertragung auf Krankenhaus-IT: 50.000 KIS-/RIS-Tickets/Jahr, KI-Klassifizierung in Kategorien wie „KIS – Performance", „RIS – Bilddarstellung" usw.

## Abgrenzung

- **Klassisches Incident Management vs. KI-unterstütztes Incident Management** (siehe [[SM - ITIL Practice - Incident Management]]): Klassisch — Service Desk klassifiziert manuell. Mit KI — automatisierte Klassifikation, Mensch übernimmt nur bei Unsicherheit. Effizienzgewinn, aber Trainingsdaten und Modellqualität sind kritisch.
- **Wissensmanagement vs. Incident Management**: Wissensmanagement (KEDB) liefert Trainingsdaten für KI; Incident Management nutzt KI-Output zur Steuerung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist die Hypothese der Frick-et-al.-Fallstudie? — KI kann die Kategorisierung im Incident Management optimieren.

**Anwendungsfrage:** Welche Schritte des klassischen Incident-Management-Prozesses werden durch KI ersetzt — und welche bleiben? — KI: Identifikation, Protokollierung, Kategorisierung. Mensch: Behebung, Wiederherstellung.

**Diskussionsfrage:** Welche Risiken birgt der KI-Einsatz im Incident Management? — Falsche Kategorisierung führt zu Fehl-Eskalationen; Trainingsdaten-Bias; mangelnde Erklärbarkeit der KI-Entscheidung; Datenschutz bei Ticketinhalten.

**Mögliche Anschlussfragen:**
- Was ist NLU (Natural Language Understanding)? — *Im PDF nicht definiert.*
- Welche Rolle spielt Wissensmanagement im KI-Lifecycle?
- Wie hängt diese Fallstudie mit „Optimieren und automatisieren" als Grundprinzip zusammen ([[SM - ITIL 4 - Sieben Grundprinzipien]])?
- Welche der vier ITIL-4-Dimensionen werden durch den KI-Einsatz besonders verändert? — Vor allem Dimension 2 (Informationen und Technologie), aber auch Dimension 1 (Veränderung der Service-Desk-Arbeitsprofile).
- Genfer Wissensmanagement-Modell vs. Münchner Modell — Vergleich? *(im PDF nicht beschrieben; Quelle Moodle).*

## Verwandt

- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL V3 Practice - Incident Management]]
- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 - Dimension Informationen und Technologie]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 147–150; Quelle laut Folie: Frick, N., Brünker, F., Ross, B. et al. (2019). Aufgabe A2 verweist auf weitere Modelle in Moodle.

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
