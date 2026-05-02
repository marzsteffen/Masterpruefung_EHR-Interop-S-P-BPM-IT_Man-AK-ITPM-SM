---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - Grundlagen klinischer Kernprozess]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - Waste - Sechs Domänen

> [!info] Kurzdefinition
> **Sechs Waste-Domänen** sind die in Shrank et al. 2019 (JAMA) systematisierten Bereiche der Verschwendung im US-Gesundheitswesen. Schätzung: 760–935 Mrd. USD pro Jahr (≈ 25 % der Gesundheitsausgaben), davon 191–286 Mrd. USD durch Maßnahmen zur Reduktion einsparbar.

## Beschreibung

Folien 22–25. Hauptarbeit: Shrank WH, Rogstad TL, Parekh N. *Waste in the US Health Care System – Estimated Costs and Potential for Savings.* JAMA 2019; 322(15):1501–1509.

### Aussagen aus den Folien

- Die USA geben mehr für Gesundheitsversorgung aus als jedes andere Land der Welt (**18 % des BIP**).
- Geschätzte Kosten der Verschwendung: **760–935 Mrd. USD/Jahr** (ca. 25 % der gesamten Gesundheitsausgaben).
- Potenzielle Einsparung durch Reduktionsmaßnahmen: **191–286 Mrd. USD** (ca. 25 % der Verschwendung selbst).
- Maßnahmen zur Vermeidung von Verschwendung = Optimierung der Prozesse → reduzieren die Steigerung der US-Gesundheitsausgaben.

### Die sechs Waste-Domänen

Aus der Tabelle 1 von Shrank et al. (in den Folien als Drei-Folien-Set 23–25 dargestellt). Die Kostenspannen sind im PDF *nicht* angegeben – sie stammen aus dem Originalpaper und sind in der Spalte „Geschätzte Kosten/Jahr" als Ergänzung außerhalb der Vorlesung beigefügt:

| # | Domäne (engl.) | Domäne (dt.) | Inhalt | Geschätzte Kosten/Jahr (USD) |
|---|---|---|---|---|
| 1 | **Failure of Care Delivery** | Versorgungslücken | Fehler in der Erbringung der Versorgung selbst (z. B. nicht durchgeführte präventive Maßnahmen, Fehler in der Patientensicherheit). | 102,4 – 165,7 Mrd. |
| 2 | **Failure of Care Coordination** | Versorgungs­koordinationslücken | Brüche zwischen Versorgungsebenen (z. B. unzureichende Übergabe von der Klinik zum Hausarzt → Wieder­einweisungen). | 27,2 – 78,2 Mrd. |
| 3 | **Overtreatment / Low-Value Care** | Übertherapie / wertarme Versorgung | Tests/Therapien ohne klinischen Nutzen (Bezug zu [[BPM - Paper - Choosing Wisely]]). | 75,7 – 101,2 Mrd. |
| 4 | **Pricing Failure** | Preisversagen | Preisanomalien, hohe Preisaufschläge ohne Wertbegründung. | 230,7 – 240,5 Mrd. |
| 5 | **Fraud and Abuse** | Betrug und Missbrauch | Abrechnungsbetrug, missbräuchliche Leistungen. | 58,5 – 83,9 Mrd. |
| 6 | **Administrative Complexity** | Administrative Komplexität | Bürokratie, doppelte Datenerfassung, Verwaltung von Versicherungen, Coding. | 265,6 Mrd. |

Folie 25 markiert die ersten drei Domänen als **„Failure of Care Delivery / Coordination / Overtreatment"** als die für BPM steuerungsrelevanten Bereiche; die letzten drei (Pricing, Fraud, Administrative) sind im US-Kontext besonders bedeutsam und stehen weniger unter direkter klinischer Steuerung.

### Größenrangfolge der Domänen (Originalstudie, im PDF nicht ausgewiesen)

Auf Basis der Punktschätzungen ergibt sich folgende Rangfolge:

1. **Administrative Complexity** – 265,6 Mrd. (= **größte Domäne**)
2. **Pricing Failure** – ca. 235 Mrd.
3. **Failure of Care Delivery** – ca. 134 Mrd.
4. **Overtreatment / Low-Value Care** – ca. 88 Mrd.
5. **Fraud and Abuse** – ca. 71 Mrd.
6. **Failure of Care Coordination** – ca. 53 Mrd.

→ **Die größten Brocken** liegen damit in den *systemischen* Domänen (Admin-Komplexität, Pricing) und sind nicht direkt durch klinische Pfade adressierbar. Die *klinisch beeinflussbaren* Domänen 1–3 machen zusammen ca. 295 Mrd. aus – immer noch der größte zusammenhängende Hebel, den BPM im Krankenhaus heben kann.

### Potenzielle Einsparungen

Shrank et al. schätzen die durch Reduktionsmaßnahmen erzielbaren Einsparungen auf **191 – 286 Mrd. USD/Jahr** – das entspricht ~25 % der Verschwendungs­kosten. **Wichtig:** Diese Schätzung **schließt Administrative Complexity aus**, weil die Studie für diese Domäne keine wirksamen Einsparungs­interventionen identifizieren konnte. Der größte Brocken ist also potenziell der unbeweglichste.

## Bestandteile / Aufbau

```
Waste (USA, 760–935 Mrd. $/J ≈ 25 % der Gesundheitsausgaben)
├── Klinisch beeinflussbar (BPM-Hebel)
│   ├── 1. Failure of Care Delivery
│   ├── 2. Failure of Care Coordination
│   └── 3. Overtreatment / Low-Value Care
└── Systemisch / nicht-klinisch
    ├── 4. Pricing Failure
    ├── 5. Fraud and Abuse
    └── 6. Administrative Complexity
```

## Beispiel

Klinisch im Hernien-Pfad:
- **Failure of Care Delivery**: SOP wird nicht eingehalten, postop. Atemtherapie unterbleibt → Pneumonie.
- **Failure of Care Coordination**: Entlassung ohne Übergabe an Hausarzt → vermeidbare Wiedereinweisung.
- **Overtreatment**: Routinemäßiges präop. Thorax-Röntgen ohne klinische Indikation (vgl. Choosing Wisely und [[BPM - Paper - BQLL Praeoperative Diagnostik]]).
- **Pricing Failure**: überteuerte Implantate ohne klinischen Mehrwert.
- **Fraud / Abuse**: nicht erbrachte, aber abgerechnete Leistungen.
- **Administrative Complexity**: doppelte Anamnese-Erhebung in Aufnahme und Station.

## Abgrenzung

- **Waste ≠ Sparen.** Waste-Reduktion bedeutet nicht „weniger Versorgung", sondern „dieselbe oder bessere Versorgung mit weniger Aufwand". Shrank et al. betonen: „ohne die Patient:innen schlechter zu versorgen".
- **Waste ≠ Lean-Verschwendung.** Lean-Manufacturing-Verschwendungs­arten (Überproduktion, Wartezeit etc.) überlappen, sind aber nicht identisch mit den 6 JAMA-Domänen.
- **Sechs Domänen ≠ fünf Kategorien der PzM-Wertschöpfungs­analyse.** Die fünf Kategorien (Vorbereitung, Vorarbeiten, Wartezeit, Nacharbeit, Kontrolle) aus [[BPM - Methode - Wertschoepfungsanalyse]] sind feiner und prozessbezogen; die 6 Domänen sind systemisch und gesundheits­wesen­spezifisch.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche sechs Waste-Domänen unterscheidet die JAMA-Studie 2019, und wie hoch ist die geschätzte Verschwendung im US-System?"

**Anwendungsfrage:** „Geben Sie für jede Domäne ein klinisches Beispiel aus dem chirurgischen Bereich."

**Diskussionsfrage:** Ist eine Übertragung der Zahlen auf das österreichische Gesundheitssystem zulässig? – Trade-off: Strukturen unterscheiden sich (USA: privat/Versicherer-getrieben; AT: Sozialversicherung). Die *klinisch beeinflussbaren* Domänen 1–3 sind systemübergreifend ähnlich; die Pricing/Fraud/Admin-Domänen sind im US-System deutlich ausgeprägter.

**Mögliche Anschlussfragen:**
- Was ist die Originalquelle und das Erscheinungsjahr? – Shrank, Rogstad, Parekh, JAMA 2019; 322(15):1501–1509.
- Welche Domäne ist im US-System die größte? – **Administrative Complexity (~266 Mrd.)**, gefolgt von **Pricing Failure (~235 Mrd.)**. Im PDF nicht ausgewiesen, aber durch das Originalpaper belegt; siehe Tabelle oben.
- Welche Domäne ist am direktesten durch klinische Pfade adressierbar? – Failure of Care Delivery, Failure of Care Coordination und Overtreatment (zusammen ~295 Mrd.).
- Warum sind die Einsparungs­schätzungen *ohne* Administrative Complexity berechnet? – Shrank et al. fanden keine Interventionen mit belegter Wirksamkeit für diese Domäne; sie erscheint daher nicht in den 191–286 Mrd. Einsparungs­schätzungen.

## Verwandt

- [[BPM - Paper - Waste in US Health Care]]
- [[BPM - Methode - Wertschoepfungsanalyse]]
- [[BPM - 60-30-10 Herausforderung]]
- [[BPM - Paper - Choosing Wisely]]
- [[BPM - Paper - BQLL Praeoperative Diagnostik]]
- [[BPM - Value-Based Care]]
- [[BPM - Paper - To Err Is Human]]

## Quelle

- Vorlesung: [[BPM - VL - Grundlagen klinischer Kernprozess]]
- Folien/Seitenangabe: Folien 22–25
- Originalpaper: Shrank WH, Rogstad TL, Parekh N. Waste in the US Health Care System: Estimated Costs and Potential for Savings. JAMA. 2019;322(15):1501–1509.
