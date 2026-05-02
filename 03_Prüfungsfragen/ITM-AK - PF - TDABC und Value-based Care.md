---
fach: itm-ak
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/itm-ak
---

# ITM-AK - PF - TDABC und Value-based Care

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Diese PF-Note deckt den Kaplan/Porter-2011-Komplex aus ITM-AK ab: TDABC als Methode, Capacity Cost Rate, die sieben Implementierungsschritte, Care Delivery Value Chain, den Wertbegriff, die drei Costing-Mythen und Value-Based Reimbursement/Bundled Payments. Alle Inhalte stammen aus dem Paper „How to Solve the Cost Crisis in Health Care" (HBR 2011). Die Karten sind stark prüfungsrelevant – TDABC und die drei Costing-Mythen sind explizit als Halluzinations-Honeypots eingestuft. Antworten bleiben strikt papierbasiert.

## Verlinkte Konzepte

- [[ITM-AK - TDABC - Time Driven Activity Based Costing]]
- [[ITM-AK - TDABC - Sieben Schritte der Kostenmessung]]
- [[ITM-AK - Capacity Cost Rate]]
- [[ITM-AK - Care Delivery Value Chain]]
- [[ITM-AK - Value in Healthcare]]
- [[ITM-AK - Bundled Payments und Value-Based Reimbursement]]
- [[ITM-AK - Costing Myth - Charges als Cost Surrogate]]
- [[ITM-AK - Costing Myth - Hospital Overhead too complex]]
- [[ITM-AK - Costing Myth - Healthcare Costs are fixed]]
- [[ITM-AK - Paper - Porter-Kaplan 2011 - TDABC]]

---

## Karten

### Definition

Was ist TDABC (Time-Driven Activity-Based Costing) und wie lautet die Kerngleichung?

?

TDABC ist eine Kostenrechnungsmethode, die einer einzelnen Patientenbehandlung über den vollen Care Cycle exakt diejenigen Ressourcenkosten zuordnet, die tatsächlich verbraucht wurden. Pro Prozess-Schritt werden nur **zwei Parameter** benötigt:

1. **Capacity Cost Rate** der Ressource (€ oder $ pro Stunde)
2. **Tatsächlich genutzte Zeit** des Patienten für diese Ressource (Stunden)

**Kerngleichung:**

```
Zugeordnete Kosten = Capacity Cost Rate × tatsächlich genutzte Zeit
Total Patient Cost = Σ (Capacity Cost Rate_i × Time_i)  für alle Ressourcen i, alle Process Steps
```

Analyseeinheit ist immer: **Patient × medical condition × full care cycle** – nicht Abteilung oder einzelne Prozedur.

---

Was ist der Capacity Cost Rate und wie wird er grundsätzlich berechnet?

?

Der Capacity Cost Rate ist der Kostensatz pro Zeiteinheit (€/h oder €/min), zu dem eine Ressource für patientenrelevante Tätigkeit verfügbar ist.

**Grundgleichung:**

```
Capacity Cost Rate = Expenses Attributable to Resource  /  Available Capacity of Resource
```

- **Zähler**: Alle Kosten der Ressource – Vergütung inkl. Lohnnebenkosten, Supervision, Raum (pro-rata), Equipment, IT/Telekom.
- **Nenner**: **Praktische Kapazität** – tatsächlich verfügbare klinische Stunden nach Abzug von Wochenenden, Urlaub, Feiertagen, Krankheit, Pausen, Meetings, Schulungen, Verwaltung.

Wichtig: Es wird **praktische**, nicht theoretische Kapazität verwendet. Die Differenz zwischen praktischer Kapazität und tatsächlicher Nutzung wird als **„Cost of Unused Capacity"** sichtbar gemacht.

---

Wie definieren Porter und Kaplan Value im Gesundheitswesen?

?

**Value = Outcomes / Cost**

- **Outcomes** umfassen mehrere Dimensionen: Survival, Funktionsfähigkeit, Behandlungsdauer, Diskomfort/Komplikationen, Nachhaltigkeit der Recovery.
- **Cost** umfasst alle Ressourcen über den vollen Care Cycle einer medical condition – inklusive Komplikationen und Komorbiditäten.

Beide Größen müssen auf **Patientenebene über den vollen Care Cycle** gemessen werden – nicht volumen- oder leistungsorientiert. Zentrale These des Papers: „Better outcomes often go hand in hand with lower total care cycle costs." Mehr oder teurere Versorgung ist nicht automatisch höherer Wert.

---

Was sind Bundled Payments und wie unterscheiden sie sich von DRG und Capitation?

?

**Definition**: Ein einziger Bundled Payment deckt den vollen Care Cycle einer medical condition ab, inklusive üblicher Komplikationen und Komorbiditäten.

**Abgrenzung:**

| | Bundled Payment | DRG | Capitation |
|---|---|---|---|
| Umfang | Voller Care Cycle | Primär stationäre Akutphase | Alle Leistungen pro Person/Periode |
| Basis | Medical condition | Diagnose-Gruppe (stationär) | Versicherte Person |
| Anreiz | Wert über den Cycle | Effizienz im stationären Aufenthalt | Gesamtversorgungseffizienz |

Laut Paper: TDABC ist die **Voraussetzung** dafür, dass ein Anbieter Bundled Payments kalkulieren und akzeptieren kann – ohne Cycle-Kosten-Kenntnis = Existenzrisiko.

---

Was ist die Care Delivery Value Chain (CDVC) und welche sechs Stages hat sie?

?

Die CDVC ist eine Karte aller Hauptaktivitäten im vollen Care Cycle einer medical condition – über alle beteiligten Anbieter und Lokationen hinweg. Sie ist **Schritt 2 der TDABC-Implementierung** und Voraussetzung für patientenbezogene Kostenmessung.

**Sechs Stages** (Paper, S. 56 – Beispiel Knee Replacement):

```
Monitoring/Preventing → Diagnosing → Preparing → Intervening → Recovering/Rehabbing → Monitoring/Managing
```

Pro Stage werden vier Achsen erfasst: **Care Delivery** (welche Aktivitäten), **Accessing** (wo), **Measuring** (welche Outcomes), **Informing & Engaging** (Patientenaufklärung).

Die CDVC ist gleichzeitig deskriptiv (Ist-Zustand) und präskriptiv (Soll-Zustand).

---

### Anwendung

Berechnen Sie den Capacity Cost Rate für Nurse White aus dem Patient-Jones-Beispiel (Zahlenwerte aus dem Paper).

?

**Zähler – monatliche Gesamtkosten Nurse White:**

| Position | Wert |
|---|---|
| Annual compensation inkl. Fringe Benefits | $65.000 |
| Supervision (10 % Vorgesetztenkosten) | $9.000 |
| Occupancy (9 m² × $1.200/m²/Jahr) | $10.800 |
| Technology and Support | $2.560 |
| **Jahresgesamtkosten** | **$87.360** |
| **Monatsgesamtkosten** | **$7.280** |

**Nenner – praktische Kapazität pro Monat:**

365 − 104 (Wochenenden) − 20 (Urlaub) − 12 (Feiertage) − 5 (Krankheit) = **224 Arbeitstage/Jahr ≈ 18,7/Monat**
7,5 h/Tag − 0,5 h Pausen − 1,0 h Meetings/Schulung/Verwaltung = **6 klinische h/Tag**
→ 18,7 × 6 = **112 klinische Stunden/Monat**

**Capacity Cost Rate:** $7.280 / 112 h = **$65/h**

---

Berechnen Sie die Gesamtkosten des Klinikbesuchs von Patient Jones (Zahlenwerte aus dem Paper).

?

Patient Jones hat einen ambulanten Klinikbesuch mit drei Ressourcen:

| Ressource | Capacity Cost Rate | Zeit | Kosten |
|---|---|---|---|
| Administrator Allen | $45/h | 0,3 h (18 min) | $13,50 |
| Nurse White | $65/h | 0,4 h (24 min) | $26,00 |
| Physician Green | $300/h | 0,15 h (9 min) | $45,00 |
| **Total** | | | **$84,50** |

Formel: Capacity Cost Rate × Zeit je Ressource, dann summieren.

---

Beschreiben Sie die sieben Schritte der TDABC-Implementierung im Healthcare (laut Kaplan/Porter-Sidebar).

?

| # | Schritt | Kerninhalt |
|---|---|---|
| 1 | **Select the medical condition** | Wahl der medical condition + Definition Anfang/Ende des Care Cycle (bei chronisch: typisch 1 Jahr) |
| 2 | **Define the Care Delivery Value Chain** | Mapping aller Hauptaktivitäten + Lokationen über den vollen Care Cycle |
| 3 | **Develop process maps** | Pro Aktivität: alle eingesetzten Capacity-Supplying-Resources (Personal, Räume, Equipment) + Verbrauchsmaterialien |
| 4 | **Obtain time estimates** | Zeitschätzungen je Ressource und Patientenkontakt; Standardzeiten für kurze/wenig variierende Prozesse |
| 5 | **Estimate cost of each resource** | Direkte Kosten: Personal, Abschreibung/Leasing, Supplies, Operating Expenses; Support-Funktionen zuweisen |
| 6 | **Calculate capacity cost rate** | Praktische Kapazität ermitteln; Capacity Cost Rate = Schritt 5 / Schritt 6 |
| 7 | **Compute total costs over care cycle** | Capacity Cost Rate × Zeit je Schritt; Summe über alle Schritte und Ressourcen |

---

Warum ist TDABC die Voraussetzung dafür, dass ein Anbieter Bundled Payments akzeptieren kann?

?

Ohne genaue Kenntnis der echten Cycle-Kosten kann ein Anbieter nicht beurteilen, ob ein Bundled Payment seine Kosten deckt. Die Annahme eines Bundled Payments ohne verlässliche Datenbasis ist ein **Existenzrisiko** – insbesondere wenn:

- Komplikationen und Komorbiditäten in den Bundle eingeschlossen sind.
- Der Care Cycle mehrere Anbieter und Versorgungsstufen umspannt.
- Cross-Subsidies aus dem bisherigen System wegfallen.

Logik-Kette des Papers: Akkurate TDABC-Daten → Vertrauen in Bundle-Kalkulation → Einführung Value-Based Reimbursement möglich → Anreize verschieben sich von Volumen auf Wert → echte „Bending of the Cost Curve".

---

Welche Ergebnisse erzielte das MD Anderson Cancer Center im TDABC-Pilot (Anesthesia Assessment Center)?

?

Laut VL-Note (Paper S. 63):

- **−16 %** Prozesszeit
- **−12 %** technische Personalkosten
- **−67 %** professionelle Personalkosten
- **−36 %** Gesamtkosten

Diese Größenordnung war nur erreichbar, weil TDABC die tatsächliche Nutzung von Kapazitäten sichtbar machte – insbesondere die hohe ungenutzte Kapazität bei hochbezahlten professionellen Ressourcen. Die Reduktion zeigt, dass Kaplan/Porters These stimmt: Kosten, die als „fix" galten, sind tatsächlich steuerbar.

---

### Diskussion

Nennen Sie die drei Costing-Mythen, die Kaplan/Porter widerlegen, und ihre Kernkritik in je einem Satz.

?

| Mythos | Kurzkritik |
|---|---|
| **Mythos 1**: „Charges sind ein guter Cost-Surrogate" | Charges spiegeln Reimbursement-Logik wider, nicht Ressourcenverbrauch – und erzeugen systematisch verzerrte Kostenzahlen. |
| **Mythos 2**: „Krankenhaus-Overhead ist zu komplex für genaue Allokation" | Die „peanut butter"-Methode (gleichmäßig nach Belegtagen, Kopfzahl etc.) verdeckt echte Treiber; TDABC löst das durch prozessbasierte Allokation. |
| **Mythos 3**: „Die meisten Gesundheitskosten sind fix" | Ca. 95 % der vermeintlich fixen Kosten (Personal, Raum, Equipment) sind tatsächlich steuerbar – „fix" ist Folge von Management-Inattention, nicht Kostennatur. |

---

Erläutern Sie das Schön-Klinik-Beispiel: Wie zeigt es den Fehler der „peanut butter"-Overhead-Allokation?

?

**Ausgangslage** (Paper, S. 57): Schön Klinik (Deutschland) verteilte Support-Kosten für Knee-Replacement-Patienten primär nach Belegtagen. Da Knee-TEP-Patienten ca. **75 % ihrer Belegzeit in der Reha** verbringen, wurden 75 % der Support-Kosten der Reha zugewiesen → Reha erschien **unprofitabel**, Kapazität wurde reduziert.

**TDABC-Korrektur**: Die tatsächliche Demand für viele Support-Services (z. B. Medical Billing, Verwaltung) konzentriert sich auf die **Akutphase**, nicht die Reha. Nach korrekter Zuordnung: Reha war tatsächlich **profitabel** → strategische Empfehlung war das Gegenteil: Reha-Kapazität ausbauen und Support-Kosten in der Akutphase senken.

**Lehre**: Pauschal-Allokation kann strategische Entscheidungen vollständig umkehren.

---

Warum zerstört Fee-for-Service den Value-Begriff von Porter/Kaplan?

?

Fee-for-Service vergütet **Volumen einzelner Leistungen**, nicht Outcomes über den Care Cycle:

- Anbieter haben Anreiz, gut vergütete Services auszuweiten, schlecht vergütete zu meiden – unabhängig vom Patientennutzen.
- **Cross-Subsidies** entstehen: manche Services generieren hohe Margen, andere laufen weit unter Kosten – ohne Bezug zu Value.
- Ohne echte Kostendaten bleibt verborgen, wo Ressourcen verschwendet werden.
- Bessere Frühdiagnose (niedrigere Kosten, bessere Outcomes) wird durch Fee-for-Service systematisch unterfinanziert, weil sie weniger einzelne Leistungen generiert.

Ergebnis laut Paper: kein „healthy dynamic of competition" – stattdessen Zero-sum-Wettbewerb über Reimbursement-Margen.

---

Warum sind laut Kaplan/Porter „Healthcare Costs are fixed" ein gefährlicher Mythos für M&A-Entscheidungen?

?

Das verbreitete Fix-Kosten-Argument rechtfertigt Mergers und Akquisitionen mit Skaleneffekten: Wenn Kosten fix sind, sinken Durchschnittskosten mit steigendem Volumen. Kaplan/Porter widerlegen das empirisch: Die US-Gesundheitskosten steigen trotz jahrzehntelangem Wachstum – was bei echten Fix-Kosten nicht passieren dürfte.

**Konsequenz für M&A:**
- Fusionen werden mit falschen Kostenannahmen begründet.
- Die Synergien materialisierten sich nicht, weil die „fixen" Kosten (Personal, Raum, Equipment) tatsächlich mit dem Volumen skalieren.
- TDABC zeigt, wo ungenutzte Kapazität tatsächlich existiert – erst dann können gezielte Kostenreduktionen statt pauschaler Skalenargumentationen erfolgen.

---

### Vergleich

Worin unterscheidet sich TDABC von klassischem Activity-Based Costing (ABC)?

?

| Merkmal | Klassisches ABC | TDABC |
|---|---|---|
| Datenerhebung | Mitarbeiterbefragungen zu Aktivitäten und Cost Drivers – aufwändig, subjektiv | Zwei Parameter: Capacity Cost Rate + Zeit pro Prozess-Schritt |
| Wartungsaufwand | Hoch – bei Prozessänderungen muss das gesamte Modell neu erhoben werden | Niedrig – Änderungen nur bei veränderten Prozessen oder Ressourcenkosten |
| Komplexität | Steigt exponentiell mit Aktivitäten und Kostentreibern | Steigt linear mit Prozess-Schritten |
| Analyseeinheit | Typisch: Aktivitäten in einem Department | Patient × medical condition × full care cycle |
| Ungenutzte Kapazität | Nicht direkt sichtbar | Explizit als „Cost of Unused Capacity" ausgewiesen |

---

Vergleichen Sie die Analyseeinheit traditioneller Healthcare-Kostensysteme mit der Analyseeinheit von TDABC.

?

| Aspekt | Traditionelle Systeme | TDABC |
|---|---|---|
| Grundeinheit | Abteilung / Department | Patient × medical condition × full care cycle |
| Allokationslogik | Overhead pauschal auf Abteilungen (Charges, Belegtage, RVUs) | Ressourcen × Zeit direkt auf Patientenprozesse |
| Sichtbarkeit | Abteilungskosten bekannt, Patientenkosten unbekannt | Kosten je Patient und je Prozess-Schritt sichtbar |
| Vergleichbarkeit | Klinik-intern nach Abteilung | Zwischen Anbietern, Ärzten, Standorten für dieselbe medical condition |
| Reform-Grundlage | Pauschale Budgetkürzungen | Gezielte Prozessoptimierung + Value-Based Reimbursement |

---

## Mögliche Anschlussfragen des Prüfers

- Wie hängen TDABC und Process Mapping (BPM) zusammen?
- Welche IT-Systeme erleichtern Time Estimates (RFID, Bar-Code, EHR-Time-Stamps)?
- Was bedeutet „Cost of Unused Capacity" konkret – und wer trägt sie?
- Welcher der sieben Schritte ist in der Praxis am schwierigsten umzusetzen und warum?
- Wie würden Sie eine CDVC für eine chronische Erkrankung (z. B. Diabetes Typ 2) aufbauen?
- Wie hängt Bundled Payment mit DRG/LKF in Österreich zusammen?
- Was, wenn der Care Cycle mehrere Anbieter umfasst – wer besitzt die TDABC-Daten?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
