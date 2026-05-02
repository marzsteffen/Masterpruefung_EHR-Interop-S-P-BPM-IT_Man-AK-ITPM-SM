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

# BPM - Methode - Wertschöpfungsanalyse

> [!info] Kurzdefinition
> Eine **Wertschöpfungsanalyse** klassifiziert jeden Prozessschritt in eine von drei Kategorien (wertschöpfend, unterstützend, verschwendend) und berechnet daraus drei Kennzahlen: **Wertschöpfungsgrad**, **Fluss-Rate** und **Wertschöpfungsquotient**.

## Beschreibung

Folien 106–113. Zweck: nicht-wertschöpfende und verschwenderische Tätigkeiten im Prozess identifizieren.

### Drei Kategorien je Prozessschritt

- **WS – wertschöpfend**: schafft direkten Mehrwert für den Kunden.
- **U – unterstützend**: notwendig zur Durchführung, aber kein direkter Wert.
- **V – verschwendend**: nicht-wertschöpfend und nicht notwendig.

### Fünf Typen nicht-wertschöpfender Tätigkeiten (Folie 108)

1. **Vorbereitung**: Tätigkeiten zur Vorbereitung einer nachfolgenden Aktivität (z. B. Anfahrten, Bereitstellen).
2. **Vorarbeiten**: ungeplante/ungefragte Leistungserbringung – „zu viel des Guten" (z. B. Aufräumen online und gedruckt).
3. **Verzögerung / Warten / Lagerung**: Tätigkeiten, bei denen Arbeit auf Erledigung wartet (z. B. Zwischenlagerung, Vorratshaltung).
4. **Nacharbeit**: Tätigkeiten infolge von Fehlern (z. B. Nachbearbeitung, Rückruf).
5. **Kontrolle / Prüfung**: interne Kontrollen wie unaufgeforderte Qualitätskontrollen und Proben.

### Drei Kennzahlen (Folien 112–113)

| Kennzahl | Formel |
|---|---|
| **Wertschöpfungsgrad (WS%)** | Σ wertschöpfender Bearbeitungszeit ÷ Σ aller Bearbeitungszeiten |
| **Fluss-Rate (FR%)** | Σ aller Bearbeitungszeiten ÷ Σ Durchlaufzeiten |
| **Wertschöpfungsquotient (WSQ%)** | Σ wertschöpfender Bearbeitungszeit ÷ Σ Durchlaufzeiten |

**Durchlaufzeit = Liegezeit + Bearbeitungszeit** (Folie 111).

### Beispiel-Tabelle (Folien 110–111, Limonadenstand-Sirup)

10 Schritte, davon 5 WS, 4 U, 1 V. Bearbeitungszeiten: 88 min gesamt (65 WS + 21 U + 2 V). Liegezeit: 790 min. Durchlaufzeit: 878 min.

→ **WS% = 65/88 ≈ 73,9 %**, **FR% = 88/878 ≈ 10,0 %**, **WSQ% = 65/878 ≈ 7,4 %**.

Das illustriert: Auch wenn der Wertschöpfungsgrad bei den *aktiven* Bearbeitungszeiten relativ gut aussieht, dominiert die *Liegezeit* (790 min) den Prozess – der Wertschöpfungsquotient zeigt, dass nur 7,4 % der Gesamtzeit echten Mehrwert schaffen.

### Vorgehen je Schritt (Folie 107, schematisch)

Pro Schritt drei Fragen:
1. Notwendig für die Herstellung eines Outcomes? – Nein → Verschwendung → eliminieren.
2. Wertschöpfend? – Nein → unterstützend → reduzieren.
3. Wertschöpfend? – Ja → optimieren.

## Bestandteile / Aufbau

| Spalte | Inhalt |
|---|---|
| Prozessschritt-Nr. | fortlaufend |
| Kategorie | WS / U / V |
| Bearbeitungszeit | Aktivzeit pro Schritt |
| Liegezeit | passive Wartezeit pro Schritt |

## Beispiel

Klinisch: präoperative Diagnostik. WS = Anamnese, klinische Untersuchung, indikationsbasierte Tests; U = Patiententransport, Akten anfordern; V = nicht-indizierte Routineuntersuchungen (Bezug zu [[BPM - Paper - Choosing Wisely]]). Die WS%-Berechnung quantifiziert das Reduktionspotenzial.

## Abgrenzung

- **Wertschöpfung ≠ wichtig.** Wartung ist wichtig, aber nicht wertschöpfend (= unterstützend).
- **Verschwendung ≠ Faulheit.** „V" entsteht häufig durch System­fehlanreize, nicht durch Mitarbeiter­versagen.
- **Wertschöpfungsanalyse ≠ Lean Manufacturing 7-Verschwendungen** (Toyota: Überproduktion, Wartezeit, Transport, Überarbeitung, Bestände, Bewegung, Defekte). Die Vorlesung listet **fünf** Kategorien (vgl. oben), die nicht 1:1 dem Lean-Klassiker entsprechen. **Im PDF wird Lean nicht erwähnt** – nicht ungeprüft Lean-Begriffe einbringen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Welche drei Kennzahlen liefert eine Wertschöpfungsanalyse, und wie sind sie definiert?"

**Anwendungsfrage:** „Berechnen Sie WS%, FR%, WSQ% für einen kleinen Beispiel­prozess." – Tabelle der Folien 110–111 als Vorlage.

**Diskussionsfrage:** Warum ist im Gesundheitswesen die Wertschöpfungsfrage politisch heikel? – „Verschwendung" wird als Vorwurf gegen Ärzt:innen gehört; Trade-off zwischen Sicherheits-Doppelchecks (zur Risikominimierung) und Effizienz. Vgl. [[BPM - Paper - Waste in US Health Care]] – dort ist Verschwendung im US-System auf 25–30 % geschätzt.

**Mögliche Anschlussfragen:**
- Was sind die fünf Typen nicht-wertschöpfender Tätigkeiten laut Folien?
- Wie unterscheidet sich Fluss-Rate vom Wertschöpfungsgrad?
- Warum ist Liegezeit oft der Hebel mit dem größten Effekt?

## Verwandt

- [[BPM - Grundprinzip - Effizienz und Wertschoepfung]]
- [[BPM - Methode - FMEA]]
- [[BPM - Methode - Schnittstellenanalyse]]
- [[BPM - Prozess-Kennzahlen]]
- [[BPM - Paper - Waste in US Health Care]]
- [[BPM - Paper - Choosing Wisely]]

## Quelle

- Vorlesung: [[BPM - VL - Prozessmanagement Grundlagen (PzM-Kompakt)]]
- Folien/Seitenangabe: Folien 106–113
