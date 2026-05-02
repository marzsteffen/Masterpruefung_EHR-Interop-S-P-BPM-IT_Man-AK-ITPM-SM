---
typ: konzept
status: offen
faecher: [asp, itpm]
quellen:
  - "[[ASP - Risikomanagement - Definition Risiko]]"
  - "[[ASP - Risikomanagement - Big Picture]]"
  - "[[ASP - Risikomanagement - Risikomatrix]]"
  - "[[ASP - Risikomanagement - Risikobewertung]]"
  - "[[ASP - Risikomanagement - Risikobehandlung]]"
  - "[[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]"
  - "[[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]]"
  - "[[ASP - Risikomanagement - Risikoidentifikation Ansaetze]]"
  - "[[ASP - Risikomanagement - Asset-basierte Identifikation]]"
  - "[[ASP - Risikomanagement - Strukturanalyse und Schutzbedarf]]"
  - "[[ASP - Risikomanagement - Ueberwachung KPI KRI]]"
  - "[[ASP - Risikomanagement - Risikokommunikation]]"
  - "[[ASP - Risikomanagement - Grundvoraussetzungen]]"
  - "[[ITPM - Risiko - Definition]]"
  - "[[ITPM - Risiko - vs Problem]]"
  - "[[ITPM - Risiko - Sequenz]]"
  - "[[ITPM - Risikomanagement - Grundlagen]]"
  - "[[ITPM - PMI Risikomanagement-Prozess]]"
  - "[[ITPM - Risikoidentifikation]]"
  - "[[ITPM - Risikoanalyse - qualitativ und quantitativ]]"
  - "[[ITPM - Risikomatrix]]"
  - "[[ITPM - Risikobewältigung - Strategien]]"
  - "[[ITPM - Risikoklausur]]"
  - "[[ITPM - ISO 31000 - Risikomanagement]]"
  - "[[ITPM - SEI 7 Prinzipien - Risikomanagement]]"
  - "[[ITPM - Risikokategorien]]"
tags:
  - typ/konzept
  - status/offen
  - cross-fach
  - fach/allgemein/asp
  - fach/vertiefung/itpm
---

# Cross - Risikomanagement zwei Sichten

> [!info] Kurzdefinition
> ASP behandelt Risikomanagement als *Informations­sicherheits-Risikomanagement* nach ISO 27005:2022 mit BSI-200-2-IT-Grundschutz-Bausteinen. ITPM behandelt es als *Projekt-Risikomanagement* nach PMBOK (PMI) und ISO 31000. Beide verwenden dieselbe formale Logik (Risiko = Eintrittswahrscheinlichkeit × Auswirkung; Risikomatrix als visuelles Werkzeug; iterativer Prozess), aber mit verschiedenen Standards, verschiedenen Detail-Schwerpunkten und einem bemerkenswerten Vokabular-Konflikt bei den Behandlungs-Strategien.

## Sicht aus Fach ASP

ASP behandelt Risikomanagement im Kontext der **Informationssicherheit** mit ISO 27005:2022 als Hauptstandard und BSI 200-2 als deutsche Methodik.

**Risiko-Definition** (siehe [[ASP - Risikomanagement - Definition Risiko]], Folie 2):

- Duden: *„möglicher negativer Ausgang einer Unternehmung mit Nachteilen, Verlusten, Schäden"*.
- ISO 27005:2022: *„effect of uncertainty on objectives"* — formal neutral, mit Note 6: „Information security risks are usually associated with a negative effect of uncertainty on information security objectives." Im Sicherheits-Kontext praktisch immer negativ.

**Sieben-Schritte-Prozess nach ISO 27005** (siehe [[ASP - Risikomanagement - Big Picture]], Folie 7):

1. Bestimmung des Kontexts (Clause 6) — Geltungsbereich, Rollen, Bewertungsskalen, Akzeptanz­kriterien.
2. Risikoidentifikation (Clause 7.2) — ereignis- oder asset-basiert.
3. Risikoanalyse (Clause 7.3) — Wahrscheinlichkeit × Auswirkung.
4. Risikoevaluierung (Clause 7.4) — Vergleich mit Akzeptanz­kriterien.
5. Risikobehandlung (Clause 8) — Vermeidung / Reduktion / Transfer / Akzeptanz.
6. Risikokommunikation (Clause 10.3) — Bericht und Reporting.
7. Überwachung und Verbesserung (Clause 10.5) — KPI/KRI.

Plus zwei Querschnitts-Aktivitäten: **Communication and Consultation**, **Monitoring and Review** (laufen über alle Schritte).

Schritte 2–4 zusammen = **Risk Assessment**. Zwei **Risk Decision Points**: (1) ist Assessment satisfactory? (2) ist Risiko akzeptiert?

**Vier Risikobehandlungs-Strategien** (siehe [[ASP - Risikomanagement - Risikobehandlung]], Folie 40):

| Strategie | Mechanismus | Beispiel |
|---|---|---|
| Vermeidung | Tätigkeit weglassen | Onlineshop einstellen |
| Reduktion | Maßnahme implementieren | Firewall, IDS, Patches |
| Transfer | Risiko auslagern | Versicherung, Outsourcing |
| Akzeptanz | Restrisiko hinnehmen | Geschäftsführung dokumentiert |

Strategien sind kombinierbar (Folie 41 zeigt Risiko 1 mit Reduktion + Transfer parallel). Risikobehandlungsplan dokumentiert pro Risiko: Strategie, Maßnahme, Termin, Verantwortlich, Kosten, Auswirkung auf EW/A, Restrisiko.

**Risikomatrix** (siehe [[ASP - Risikomanagement - Risikomatrix]], Folien 12–13):

- 4×4-Matrix mit y=Eintrittswahrscheinlichkeit, x=Auswirkung im Schadensfall.
- Risikoklassen: rot (rechts oben) / gelb (Diagonale) / grün (links unten).
- Folie 13 warnt explizit vor 3×3-Matrizen — feinere Granularität bessere Differenzierung.

**BSI 200-2 IT-Grundschutz-Bausteine** (siehe [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]], Folien 24–27):

- IT-Grundschutz-Kompendium: Bausteine + Gefährdungs- + Maßnahmenkataloge.
- **Prozess-Bausteine** (organisatorisch): ISMS, ORP, CON, OPS.
- **System-Bausteine** (technisch): APP, SYS, IND, NET, INF.
- Pro Baustein: spezifische + elementare Gefährdungen, Anforderungen in 3 Stufen (Basis / Standard / erhöhter Schutzbedarf). Beispiel: SYS.1.5 Virtualisierung.

**Asset-basierte Identifikation** (siehe [[ASP - Risikomanagement - Asset-basierte Identifikation]]) und **Strukturanalyse + Schutzbedarf** (siehe [[ASP - Risikomanagement - Strukturanalyse und Schutzbedarf]]) als Methoden — über Asset-Listen, Bedrohung × Schwachstelle.

**KPI vs. KRI** (siehe [[ASP - Risikomanagement - Ueberwachung KPI KRI]]) als Überwachungs-Mechanik.

## Sicht aus Fach ITPM

ITPM behandelt Risikomanagement im Kontext des **Projektmanagements** mit PMBOK / PMI als Hauptstandard und ISO 31000 als Erweiterung.

**Risiko-Definition** (siehe [[ITPM - Risiko - Definition]], Folien 34–35):

> **Risiko = Eintrittswahrscheinlichkeit × Auswirkung.**

Vier Definitions-Varianten aus der Vorlesung:

- „Risiko ist ein in der Zukunft liegendes mögliches Ereignis im Projektverlauf, welches die Gefährdung oder eingeschränkte Erreichung der Projektziele oder das Scheitern des Projekts zur Folge hat."
- „Ein Risiko ist ein unbestimmtes Ereignis oder eine Bedingung, die im Falle des Eintretens eine **positive oder negative** Auswirkung auf ein oder mehrere Projektziele hat."
- „Ein Risiko ist ein mögliches Ereignis mit unerwünschter Wirkung."
- „Risiko ist die Unwägbarkeit des technischen und wirtschaftlichen Projekterfolgs."

**„Risk" hat im englischen Sprachraum zwei Bedeutungen** (Folie 35): **Threat** (Bedrohung) + **Opportunity** (Chance). Im Deutschen meist nur negativ.

**Eigenschaften:** abschätzbar (oder berechenbar) und auf die Zukunft ausgerichtet. „**Ein Projekt ohne Risiko ist kein Projekt!**"

**Risiko ≠ Problem** (siehe [[ITPM - Risiko - vs Problem]]): Risiko ist unsicher, Problem ist eingetreten.

**Risiko-Sequenz** (siehe [[ITPM - Risiko - Sequenz]]): Ursache → Ereignis → Auswirkung.

**PMI-Risikomanagement-Prozess** (siehe [[ITPM - PMI Risikomanagement-Prozess]], Folien 58–62, 80–82):

Sechs Schritte:

| # | Schritt | Mechanik |
|---|---|---|
| **0** | Risikomanagement planen (einmalig) | Strategisch, kein eigener Risiko-Inhalt; Teil des Projektmanagementplans; ca. 10–50 Seiten; nach Erstellung nicht mehr verändert |
| 1 | Risiken identifizieren | Erkennung + Dokumentation der Merkmale |
| 2 | Qualitative Risikoanalyse | Prioritäten setzen über EW × Auswirkung |
| 3 | Quantitative Risikoanalyse | Zahlenmäßige Analyse von Auswirkungen |
| 4 | Risikobewältigungsmaßnahmen planen | Alternativpläne, Maßnahmen für Chancen + Bedrohungen |
| 5 | Risiken steuern | Bewältigungspläne einführen, Restrisiken überwachen, neue Risiken erkennen |

Schritte 1+2+3 zusammen = **Risk Assessment**.

**ISO 31000:2009 mit 11 Grundsätzen** (siehe [[ITPM - ISO 31000 - Risikomanagement]], Folien 47–49):

- Orientiert sich stark an AS/NZS 4360:2004.
- 11 Grundsätze: schafft Werte / integrierter Teil / Teil der Entscheidungsfindung / befasst sich mit Unsicherheit / systematisch + strukturiert + zeitgerecht / beste verfügbare Informationen / maßgeschneidert / Human- und Kulturfaktoren / transparent + umfassend / dynamisch + iterativ / kontinuierliche Verbesserung.

**SEI 7 Prinzipien** (siehe [[ITPM - SEI 7 Prinzipien - Risikomanagement]]) als software-entwicklungs­spezifische Erweiterung.

**Risikomatrix** (siehe [[ITPM - Risikomatrix]], Folien 72–73, 86–88):

- xy-Darstellung mit x=Tragweite, y=EW.
- Risiken als nummerierte Kreise eingetragen.
- Wahrscheinlichkeitsskala mit konkreten %-Werten:

| Punktwert | Bezeichnung | Wahrscheinlichkeit |
|---|---|---|
| 1 | niedrig | 5–10 % |
| 2 | eher niedrig | 20–30 % |
| 3 | mittel | 40–45 % |
| 4 | eher hoch | 50–60 % |
| 5 | hoch | 70–99 % |

- **„Arrow of Attention"** als hochkritischer Bereich.
- **Maximal 5–10 Risiken** in der grafischen Darstellung.
- **Roter Bereich-Regel:** „Wenn auch nur ein Risiko dort liegt, sollte das Projekt nicht begonnen werden."

**Risikobewältigungs-Strategien** (siehe [[ITPM - Risikobewältigung - Strategien]], Folien 76–79):

- Drei Schritte: Maßnahmen entwickeln → Wirkungsanalyse → einplanen.
- **Präventiv-Maßnahmen** reduzieren EW (Schulungen, Redundanz, QS).
- **Korrektiv-Maßnahmen** mindern Auswirkungen (Notfallplan, Versicherung, Backup).
- Restrisiko-Strategien: niedrige EW + hohe Auswirkung → **Versichern**; hohe EW + niedrige Auswirkung → **Akzeptieren**.
- Quelltreue-Hinweis aus der Note: „Standard-Strategien (Avoid/Transfer/Mitigate/Accept) sind im PDF **nicht namentlich genannt**; Vorlesung verwendet das Begriffspaar Präventiv/Korrektiv."

## Gemeinsamkeiten

| Aussage | ASP | ITPM |
|---|---|---|
| Risiko = EW × Auswirkung | Risikoanalyse Clause 7.3 | Folie 34 wörtlich als Formel |
| Formal neutrale Definition (positiv/negativ), praktisch meist negativ | ISO 27005 Note 6 | PMBOK „positive oder negative", deutsch meist negativ |
| Iterativer Prozess statt Einzeldurchlauf | ISO 27005 Big Picture | PMI 6 Schritte iterativ ab Schritt 1 |
| Risikomatrix mit EW × Auswirkung als Visualisierung | 4×4-Matrix | xy-Darstellung mit Arrow of Attention |
| Risk Assessment = Identifikation + Analyse + Evaluierung | Schritte 2–4 | Schritte 1–3 |
| Restrisiko-Logik | dokumentierte Akzeptanz | Versichern bei niedriger EW + hoher Auswirkung |
| Verantwortliche pro Risiko + Plan-Dokumentation | Risikobehandlungsplan (Folie 41) | Risikodokumente |
| Standards-orientiert | ISO 27005, BSI 200-2 | PMBOK, ISO 31000, SEI 7 Prinzipien |

## Unterschiede / Konflikte / unterschiedliche Schwerpunkte

**1. Vokabular-Konflikt: Behandlungs-Strategien.**

Das ist der wichtigste Cross-Fach-Befund:

- **ASP** kennt die *vier klassischen Strategien* explizit (Folie 40): **Vermeidung / Reduktion / Transfer / Akzeptanz**. Diese sind kombinierbar, dokumentiert im Behandlungsplan.
- **ITPM** verwendet ein anderes Begriffspaar: **Präventiv-Maßnahmen** (reduzieren EW) vs. **Korrektiv-Maßnahmen** (mindern Auswirkungen). Die Standard-4er-Strategien (Avoid/Transfer/Mitigate/Accept) sind im ITPM-PDF **nicht namentlich genannt** — die Note kennzeichnet das selbst als Quelltreue-Hinweis.

In der Prüfung: Wer aus ASP heraus „die vier Strategien" beantwortet, antwortet richtig. Wer aus ITPM die ASP-Begriffe nennt, ist über die Vorlesung hinaus. Wer „Präventiv vs. Korrektiv" aus ASP beantwortet, ist über die ASP-Vorlesung hinaus. Beide Vokabulare existieren parallel im Vault, mit klarer Fach-Zuordnung.

**2. Unterschiedliche Standard-Familien.**

| Schwerpunkt | ASP | ITPM |
|---|---|---|
| Hauptstandard | ISO 27005:2022 | PMBOK (PMI) |
| Detail-Standard | BSI 200-2 (deutsch, IT-Grundschutz, Bausteine) | ISO 31000:2009 (international, generisch, 11 Grundsätze) |
| Branchen-Standard | (über BSI 200-4 für BCM) | SEI 7 Prinzipien (Software) |

Konsequenz: Wer „BSI 200-2" oder „IT-Grundschutz-Baustein" hört, ist im ASP-Kontext. Wer „PMI" oder „ISO 31000" oder „11 Grundsätze" hört, ist im ITPM-Kontext.

**3. Anzahl der Prozessschritte.**

- ASP/ISO 27005: **7 Schritte** plus 2 Querschnitts-Aktivitäten plus 2 Decision Points.
- ITPM/PMI: **6 Schritte** (Schritt 0 einmalig, 1–5 iterativ).

Das Mapping ist nicht 1:1 — die ASP-Schritte 3+4 (Analyse + Evaluierung) entsprechen ITPM-Schritten 2+3 (Qualitativ + Quantitativ). ASP-Schritt 6 (Kommunikation) ist eigener Prozess­schritt; bei ITPM ist Kommunikation in Schritt 5 (Steuerung) eingebettet. ITPM hat einen expliziten **Schritt 0 (Risikomanagement planen)**, der einmalig zu Beginn läuft — ASP hat das nicht als separaten Schritt.

**4. Granularitäts-Skala der Risikomatrix.**

- ASP: 4×4-Matrix, mit expliziter Warnung vor 3×3 (Folie 13).
- ITPM: 5-Punkte-Wahrscheinlichkeitsskala (1–5) mit konkreten Prozent-Bändern (5–10 % bis 70–99 %), kombiniert mit beliebiger Auswirkungs-Achse.

ITPM gibt also präzise Prozent-Anker, ASP gibt nur die Klassen-Anzahl. Das ist ein Methodik-Unterschied: ITPM-Wahrscheinlichkeits­skala ist quantitativ konkret, ASP bleibt qualitativ.

**5. „Arrow of Attention" — ITPM-spezifisch.**

ITPM-Risikomatrix-Note nennt explizit den **„Arrow of Attention"** als hochkritischen Bereich (Pfeil-Form). ASP hat keinen vergleichbaren Spezialbegriff — der rote Bereich ist „nur" rot. Der Begriff stammt aus dem PMBOK-/PMI-Vokabular.

**6. „Roter Bereich"-Konsequenz.**

- ITPM-Risikomatrix-Note: „Wenn auch nur ein Risiko im roten Bereich liegt, sollte das Projekt **nicht begonnen** werden."
- ASP-Risikomatrix-Note: keine vergleichbare „Stop-the-line"-Aussage.

ITPM hat also eine projekt-spezifische Konsequenz: rote Risiken sind Projekt-Showstopper. ASP-Sicherheits-Risikomanagement hat eher ein laufendes System, das auch mit roten Risiken weiterläuft, solange behandelt wird.

**7. Begrenzung der Risiko-Anzahl.**

- ITPM: **maximal 5–10 Risiken** in der grafischen Darstellung (sonst unübersichtlich).
- ASP: keine vergleichbare Zahl — die BSI-Bausteine erlauben sehr viele Risiken pro Asset.

**8. Detailtiefe der Identifikation.**

- ASP: stark *asset- und baustein­basiert* (BSI-Strukturanalyse, Schutzbedarf, IT-Grundschutz-Bausteine als Vorlagen).
- ITPM: stark *projekt­kontext­basiert* (Stakeholder-Workshops, Risikoklausur, Risikokategorien). „Risikoklausur" ist ein ITPM-spezifisches Format (siehe [[ITPM - Risikoklausur]]).

**9. Schritt 0 (Plan) vs. Schritt 1 (Kontext).**

- ITPM-Schritt 0 „Risikomanagement planen" ist *strategisch* (10–50 Seiten Plan, einmalig, danach unverändert).
- ASP-Schritt 1 „Bestimmung des Kontexts" ist *operativ* (Geltungsbereich, Skalen, Akzeptanz­kriterien).

Beide sind Vorbereitungs­schritte, aber mit anderem Charakter: ITPM definiert das *Wie* des Risikomanagements selbst, ASP definiert das *Worin* (welcher Bereich wird betrachtet).

**10. Zukunfts-Aspekt explizit nur in ITPM.**

ITPM-Definition: „auf die Zukunft ausgerichtet" als Risiko-Eigenschaft. ASP-Definition adressiert das nicht direkt — Risiko ist „effect of uncertainty on objectives" und damit zeitneutral formuliert.

**11. „Ein Projekt ohne Risiko ist kein Projekt!" — ITPM-spezifisch.**

ITPM macht explizit, dass Risiken zum Projekt gehören. ASP hat keine vergleichbare Aussage „kein System ohne Risiko" — implizit zwar, aber nicht ausgeschrieben.

## Synthese für die mündliche Prüfung

**Diskussions-Achse 1: „Was ist ein Risiko — und unterscheidet sich die Definition zwischen Sicherheit und Projekt?"**

Saubere Antwort vergleicht beide Quellen:

- ASP/ISO 27005:2022: „effect of uncertainty on objectives" — formal neutral, im Sicherheits­kontext praktisch negativ.
- ITPM/PMBOK: „in der Zukunft liegendes mögliches Ereignis" mit „positive oder negative Auswirkung" — auch formal neutral, im Deutschen meist negativ.
- Beide setzen mathematisch: Risiko = EW × Auswirkung.

Pointe: Definitions­logik ist in beiden Standards identisch (uncertainty / future event mit positive-oder-negative-Auswirkung). Der Unterschied liegt in der Anwendungs­domäne, nicht in der Theorie.

**Diskussions-Achse 2: „ISO 27005 vs. PMBOK — wo liegen die Schritt-Unterschiede?"**

Mapping als Antwort-Struktur:

| Funktion | ASP/ISO 27005 | ITPM/PMI |
|---|---|---|
| Vorbereitung | Schritt 1: Kontext | Schritt 0: Plan |
| Identifikation | Schritt 2 | Schritt 1 |
| Analyse | Schritt 3 | Schritte 2 + 3 (qualitativ + quantitativ) |
| Evaluierung gegen Akzeptanz | Schritt 4 | (in Schritt 2/3 eingebettet) |
| Behandlung | Schritt 5 (4 Strategien) | Schritt 4 (Präventiv/Korrektiv) |
| Steuerung/Überwachung | Schritt 7 | Schritt 5 |
| Kommunikation | Schritt 6 + Querschnitt | (in Schritt 5 eingebettet) |

Pointe: Beide Prozesse haben dieselbe Logik, aber mit verschiedener Schritt-Granularität und verschiedenen Schwerpunkten (ASP: Kommunikation als eigener Schritt; ITPM: Plan als eigener Schritt 0).

**Diskussions-Achse 3: „Welche Behandlungs-Strategien gibt es?"**

Hier ist das Vokabular-Mapping kritisch:

- Aus **ASP** heraus: Vermeidung / Reduktion / Transfer / Akzeptanz (klassische 4-er-Liste).
- Aus **ITPM** heraus: Präventiv (reduziert EW) / Korrektiv (mindert Auswirkung). Plus Restrisiko-Strategien: Versichern / Akzeptieren je nach Profil.

Die ITPM-Note kennzeichnet selbst: „Standard-Strategien (Avoid/Transfer/Mitigate/Accept) sind im PDF nicht namentlich genannt." Wer zwischen Vokabularen wechselt, sollte die Quelle benennen — beide existieren im Vault, aber in verschiedenen Notes.

Cross-Mapping (Synthese, nicht direkt aus den Notes):

- ASP-Reduktion ≈ ITPM-Präventiv und/oder Korrektiv.
- ASP-Transfer ≈ ITPM-Korrektiv (Versicherung).
- ASP-Vermeidung ≈ ITPM-Präventiv (vor dem Eintritt).
- ASP-Akzeptanz ≈ ITPM-Akzeptanz (bei hoher EW + niedriger Auswirkung).

**Diskussions-Achse 4: „Welche Standards stehen jeweils dahinter?"**

| Aspekt | ASP | ITPM |
|---|---|---|
| Hauptnorm | ISO 27005:2022 (informationssicherheits­spezifisch) | PMBOK (projektmanagement­spezifisch) |
| Generischer Standard | (über ISO 31000 nicht explizit als ASP-Quelle gelistet) | ISO 31000:2009 mit 11 Grundsätzen (basiert auf AS/NZS 4360:2004) |
| Methodik | BSI 200-2 IT-Grundschutz mit Bausteinen | SEI 7 Prinzipien für Software |
| Vokabular | „Schutzbedarf", „Asset", „Bedrohung" | „Threats and Opportunities", „Restrisiko" |

ITPM-Note erwähnt explizit, dass ISO 31000 die generische Schicht über PMBOK ist. ASP-Note erwähnt ISO 31000 in der Abgrenzung als Ergänzungs-Standard. Die zwei Standards sind also komplementär, mit ITPM näher an ISO 31000 und ASP näher an ISO 27005.

**Diskussions-Achse 5: „Wann ist ein rotes Risiko Projekt-Showstopper?"**

ITPM-spezifische Antwort: laut ITPM-Risikomatrix-Note „sollte das Projekt nicht begonnen werden, wenn auch nur ein Risiko im roten Bereich liegt". ASP hat keine analoge Aussage — das ist eine projekt-spezifische Risiko-Logik.

In der Prüfung: Wer das auf Sicherheits­risiken übertragen will, sollte explizit machen, dass ASP-Sicht (laufendes System) und ITPM-Sicht (Projekt-Entscheidung Go/No-Go) verschiedene Konsequenz-Logiken haben.

**Diskussions-Achse 6: „Wie wird Restrisiko gemessen und akzeptiert?"**

- ASP: Restrisiko im Behandlungsplan ausgewiesen (Beispiel-Tabelle Folie 41 zeigt konkrete Geld-Werte: Restrisiko 52 000 € nach Firewall, 10 000 € nach Zusatz-Versicherung). Geschäftsführung dokumentiert die Akzeptanz.
- ITPM: Restrisiko über Strategien-Mix (niedrige EW + hohe Auswirkung → Versichern; hohe EW + niedrige Auswirkung → Akzeptieren).

Pointe: ASP ist quantitativer (Geldwerte), ITPM ist qualitativer (Risikoprofil-zu-Strategie-Mapping).

**Anschlussfragen, die ohne Cross-Fach-Verständnis schwer zu beantworten sind:**

- „Welche vier Behandlungs-Strategien kennen Sie?" — aus ASP heraus klassisch 4. ITPM-Antwort wäre Präventiv/Korrektiv plus Restrisiko-Strategien, die aber namensmäßig nicht der klassischen 4-er-Liste entsprechen.
- „Wie unterscheidet sich BSI 200-2 von ISO 31000?" — ASP-Sicht (BSI = Bausteine, deutsch, IT-Grundschutz) + ITPM-Sicht (ISO 31000 = generisch, 11 Grundsätze, basiert auf AS/NZS 4360:2004).
- „Welche Wahrscheinlichkeits­skala ist konkret?" — ITPM mit %-Bändern (5–10 % bis 70–99 %); ASP nur mit Klassen-Anzahl.
- „Wann ist Risiko ≠ Problem?" — nur ITPM-spezifisch (Risiko = unsicher, Problem = eingetreten). Aus ITPM-Note.
- „Was ist der ‚Arrow of Attention'?" — nur ITPM-spezifisch.
- „Was bedeutet Schritt 0 in PMI?" — ITPM-spezifisch: einmaliger Plan, 10–50 Seiten, danach unverändert. Anschluss-Frage: hat ASP einen Schritt 0? Antwort: Nein, ASP startet mit Kontextbestimmung (Schritt 1).
- „Welche Schritt-Granularität hat ISO 27005?" — 7 Schritte, 2 Querschnitt-Aktivitäten, 2 Decision Points. Aus ASP-Note.

## Verwandt

**ASP:**
- [[ASP - Risikomanagement - Definition Risiko]]
- [[ASP - Risikomanagement - Big Picture]]
- [[ASP - Risikomanagement - Kontextbestimmung]]
- [[ASP - Risikomanagement - Risikoidentifikation Ansaetze]]
- [[ASP - Risikomanagement - Asset-basierte Identifikation]]
- [[ASP - Risikomanagement - Strukturanalyse und Schutzbedarf]]
- [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]]
- [[ASP - Risikomanagement - Risikomatrix]]
- [[ASP - Risikomanagement - Risikobewertung]]
- [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]
- [[ASP - Risikomanagement - Risikobehandlung]]
- [[ASP - Risikomanagement - Risikokommunikation]]
- [[ASP - Risikomanagement - Ueberwachung KPI KRI]]
- [[ASP - Risikomanagement - Grundvoraussetzungen]]
- [[ASP - BCM - Risikoanalyse]]
- [[ASP - Diagram - Risikomanagement Prozess]]

**ITPM:**
- [[ITPM - Risikomanagement - Grundlagen]]
- [[ITPM - Risiko - Definition]]
- [[ITPM - Risiko - vs Problem]]
- [[ITPM - Risiko - Sequenz]]
- [[ITPM - Risikomanagement - Nutzen und Kosten]]
- [[ITPM - Risikokategorien]]
- [[ITPM - Risikodokumente]]
- [[ITPM - PMI Risikomanagement-Prozess]]
- [[ITPM - Risikoidentifikation]]
- [[ITPM - Risikoanalyse - qualitativ und quantitativ]]
- [[ITPM - Risikomatrix]]
- [[ITPM - Risikobewältigung - Strategien]]
- [[ITPM - Risikoklausur]]
- [[ITPM - ISO 31000 - Risikomanagement]]
- [[ITPM - SEI 7 Prinzipien - Risikomanagement]]
- [[ITPM - PRINCE2 - Thema Risiko]]
- [[ITPM - Diagram - Risikomatrix]]

**Andere Brücken:**
- [[Cross - DSGVO im eHealth-Kontext]] (Datenschutz-Folgenabschätzung als Risikomanagement-Variante, in keiner Vault-Note ausgeführt)

**MOCs:**
- [[ASP - MOC]]
- [[ITPM - MOC]]

## Quelle

Cross-Fach-Synthese aus den oben gelisteten ASP- und ITPM-Konzept-Notes.

**Wichtige Quellen-Beobachtungen:**

- ASP nennt vier klassische Behandlungs-Strategien (Vermeidung/Reduktion/Transfer/Akzeptanz) explizit; ITPM nicht — die ITPM-Vorlesung verwendet stattdessen Präventiv/Korrektiv. Die ITPM-Note kennzeichnet das selbst als „im PDF nicht namentlich genannt".
- ITPM-Wahrscheinlichkeits­skala ist mit Prozent-Bändern (1=5–10 %, ..., 5=70–99 %) konkretisiert; ASP-Risikomatrix nur mit Klassen-Anzahl (4×4).
- ITPM-Schritt-0 (Risikomanagement planen) ist ein eigener Strategie-Schritt; ASP/ISO 27005 hat den nicht.
- ITPM-„Arrow of Attention" und „rote Risiken sind Projekt-Showstopper" sind ITPM-spezifisch.
- BSI 200-2 IT-Grundschutz-Bausteine (ISMS/ORP/CON/OPS + APP/SYS/IND/NET/INF) sind ASP-spezifisch.
- ISO 31000 mit 11 Grundsätzen (basiert auf AS/NZS 4360:2004) ist ITPM-spezifisch.
- Die Strategien-Cross-Mapping-Tabelle (ASP-4-Strategien ↔ ITPM-Präventiv/Korrektiv/Versichern/Akzeptieren) ist Synthese, in den Notes nicht direkt belegt.

**Fach-Zuordnung der Quellen:**

| Note | Fach |
|---|---|
| ASP - Risikomanagement - * (insgesamt 14 Notes) | ASP |
| ASP - Diagram - Risikomanagement Prozess | ASP |
| ITPM - Risiko - Definition / vs Problem / Sequenz | ITPM |
| ITPM - Risikomanagement - Grundlagen / Nutzen und Kosten | ITPM |
| ITPM - Risikokategorien / Risikodokumente | ITPM |
| ITPM - PMI Risikomanagement-Prozess | ITPM |
| ITPM - Risikoidentifikation / Risikoanalyse - qualitativ und quantitativ | ITPM |
| ITPM - Risikomatrix / Risikobewältigung - Strategien / Risikoklausur | ITPM |
| ITPM - ISO 31000 - Risikomanagement / SEI 7 Prinzipien - Risikomanagement | ITPM |
| ITPM - Diagram - Risikomatrix | ITPM |
