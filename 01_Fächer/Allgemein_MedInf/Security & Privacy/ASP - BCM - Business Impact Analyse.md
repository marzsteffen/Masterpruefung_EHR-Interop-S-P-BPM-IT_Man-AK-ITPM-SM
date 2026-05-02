---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Business Continuity Management]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - BCM - Business Impact Analyse (BIA)

> [!info] Kurzdefinition
> Strukturierte Analyse, die zeitkritische Geschäftsprozesse, Single-Points-of-Failure und Ressourcenabhängigkeiten im Notbetrieb identifiziert. Drei Phasen: Voranalyse und Vorbereitung, Durchführung, Auswertung.

## Beschreibung

### Ziele der BIA (Folie 7)
- Identifizierung von **zeitkritischen Geschäftsprozessen**. (Wichtige Geschäftsprozesse sind nicht automatisch zeitkritisch.)
- Identifizierung von **Single-Points-of-Failure** (SpoFs).
- Ermittlung der **Prozess- und Ressourcenabhängigkeiten** im Notbetrieb.

### BIA-Prozess in drei Phasen

**1. Voranalyse und Vorbereitung (Folien 9–13)**

a) **Festlegung des Geltungsbereichs (Folie 10):**
- Institutionsleitung legt abzusichernden Bereich fest.
- Umfasst die Gesamtheit von infrastrukturellen, organisatorischen, personellen und technischen Komponenten.
- Festlegung unterschiedlicher Geltungsbereiche ermöglicht Priorisierung in der Erarbeitung.

b) **Festlegung der BIA-Parameter (Folien 11–12):**
- Konkretisierung des Begriffs „zeitkritisch" (Untersuchungszeitraum z. B. 7 Tage, 14 Tage, 30 Tage).
- Definition der Schadenskategorien und -grenze (Untragbarkeitsniveau durch Institutionsleitung):
  - Beeinträchtigung der Aufgabenerfüllung
  - Verstoß gegen Gesetze, Vorschriften, Verträge
  - Negative Innen- und Außenwirkung (Imageschaden)
  - Finanzielle Auswirkungen
  - Beeinträchtigung der persönlichen Unversehrtheit

**Leitfrage (Folie 11):** „Sind bei einem Ausfall der Geschäftsprozesse dieser Organisationseinheit innerhalb von 7 Tagen zu hohe Schäden für die Institution zu erwarten?"

c) **Organisatorische Planung (Folie 13):**
- Wie werden Informationen erhoben?
  - Selbstauskunft durch Prozesseigentümer
  - Einzelinterviews mit Personen
  - Workshops mit mehreren Personen

**2. Durchführung (Folie 15)**

Festlegung der Anforderungen für wirtschaftlichen Notbetrieb. Für jeden Geschäftsprozess werden die Kenngrößen MTPD, RPO, RTO, MBCO ermittelt – siehe [[ASP - BCM - BIA Kenngroessen]].

Folie 15 zeigt eine Beispiel-Tabelle: Geschäftsprozess × Zeit-Horizonte (24 h, 3 Tage, 7 Tage, 14 Tage, 30 Tage) → Schadenspotenzial (1 gering bis 4 sehr hoch). Daraus wird der MTPD je Prozess abgelesen.

**3. Auswertung (Folie 18)**

Qualitätsgesicherte Zusammenfassung der Ergebnisse:
- Übersicht der zeitkritischen Geschäftsprozesse und zugehöriger Ansprechpartner.
- Übersicht der Prozessabhängigkeiten.
- Übersicht der abhängigen Ressourcen und SpoFs sowie deren RTO bzw. RPO.
- Mögliche Priorisierung von Ressourcen hinsichtlich geforderter Wiederanlaufzeit.

## Bestandteile / Aufbau

| Phase | Hauptaktivitäten | Ergebnis |
|---|---|---|
| Voranalyse | Geltungsbereich, BIA-Parameter, Org. Planung | klare Rahmen, Kriterien, Methodik |
| Durchführung | Datenerhebung, Festlegung Kenngrößen | MTPD/RPO/RTO/MBCO pro Prozess |
| Auswertung | qualitätsgesicherte Zusammenfassung | priorisierte Liste zeitkritischer Prozesse + SpoFs |

## Beispiel

Aus Folie 15: Geschäftsprozess „Kundenanfragen bearbeiten" – Schadenspotenzial 2 (24 h), 3 (3 Tage), 4 (7 Tage), 4 (14 Tage), 4 (30 Tage) → MTPD = 3 Tage. Prozess „Kundenzufriedenheits-Umfragen" – durchgehend 1 (gering) → keine MTPD nötig.

## Abgrenzung

- **BIA ≠ Risikoanalyse:** BIA fragt „Was muss abgesichert werden?", Risikoanalyse fragt „Wogegen muss abgesichert werden?". Beide schneiden sich im Begriff „Impact" – siehe [[ASP - BCM - Risikoanalyse]].
- **BIA ≠ Soll-Ist-Vergleich:** BIA liefert nur die SOLL-Werte (RTO/RPO). Der Vergleich mit IST-Werten (RTA/RPA) ist eine separate Aktivität.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Business Impact Analyse? Welche drei Phasen hat sie?

**Anwendungsfrage:** Sie sollen für ein kleines Krankenhaus eine BIA aufsetzen. Welche Schritte unternehmen Sie in der Voranalyse, welche in der Durchführung?

**Diskussionsfrage:** Warum ist die Festlegung des Untragbarkeitsniveaus durch die Institutionsleitung wichtig? (Strategisch-politische Entscheidung, kann nicht von IT/BCM-Verantwortlichen allein getroffen werden.) Welche Schadenskategorie ist im Gesundheitswesen besonders kritisch? (Beeinträchtigung der persönlichen Unversehrtheit.)

**Mögliche Anschlussfragen:**
- Was sind typische SpoFs in einem Krankenhaus? (Zentrales KIS, Stromversorgung, Schlüsselpersonal.)
- Wie unterscheiden sich Selbstauskunft, Interview und Workshop bei der Datenerhebung?
- Welche Kenngrößen kommen in der Durchführung zum Einsatz?

## Verwandt

- [[ASP - BCM - BIA Kenngroessen]]
- [[ASP - BCM - Soll-Ist-Vergleich]]
- [[ASP - BCM - Risikoanalyse]]
- [[ASP - BCM - Managementsystem]]
- [[ASP - BCM - Normen]]

## Quelle

- Vorlesung: [[ASP - VL - Business Continuity Management]]
- Folien/Seitenangabe: Folien 7, 9–15, 18
