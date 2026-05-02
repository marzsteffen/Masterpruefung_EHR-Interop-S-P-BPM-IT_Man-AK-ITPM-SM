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

# BPM - Methode - FMEA (Fehlermöglichkeits- und Einflussanalyse)

> [!info] Kurzdefinition
> **FMEA** (Failure Mode and Effects Analysis) ist eine Risikoanalyse-Methode zur **präventiven** Identifikation und Bewertung potenzieller Fehler in Systemen, Produkten oder Prozessen. Bewertet wird über die **Risikoprioritätszahl (RPZ) = B × A × E**.

## Beschreibung

Folien 115–119. FMEA als „effektives Werkzeug der Risikoanalyse" für die **präventive Fehlervermeidung statt nachträglicher Korrektur**.

### Vier Schritte der Prozess-FMEA (Folie 116)

1. **Prozessablauf analysieren** (Schritte/Abläufe analysieren).
2. **Potenzielle Schwachstellen** oder Abweichungen vom Soll bestimmen („was kann schiefgehen?").
3. **Bewertung mit RPZ** (Risikoprioritätszahl):
   - **B** = Bedeutung des Fehlers
   - **A** = Auftretenswahrscheinlichkeit
   - **E** = Entdeckungswahrscheinlichkeit
   - **RPZ = B × A × E**
4. **Maßnahmen ableiten und umsetzen**.

### Skalen (Folie 117)

| Faktor | Bedeutung | Skala |
|---|---|---|
| **B** (Bedeutung) | Welche Auswirkungen hat der Fehler? | 1 = unbedeutend, 10 = katastrophal |
| **A** (Auftreten) | Wie häufig? | 1 = sehr selten, 10 = sehr häufig |
| **E** (Entdeckung) | Wie wahrscheinlich, dass der Fehler entdeckt wird, bevor er Schaden anrichtet? | 1 = sehr wahrscheinlich, 10 = sehr unwahrscheinlich |

**Wichtig:** Bei E ist die Skala invers definiert – ein hoher E-Wert bedeutet, dass der Fehler **nicht** rechtzeitig entdeckt wird. Hohes E erhöht damit die RPZ.

### Orientierung Handlungsbedarf (Folie 118)

| RPZ-Bereich | Handlungsbedarf |
|---|---|
| **> 150–250** | Hohe RPZ – dringender Handlungsbedarf |
| **50–150** | Mittlere RPZ – Maßnahmen erforderlich |
| **< 50** | Niedrige RPZ – Maßnahmen empfohlen |

Maximalwert wäre 10×10×10 = 1000. In der klinischen Praxis ist diese Skalierung weit verbreitet, allerdings auch umstritten – siehe Diskussion unten.

### Formular (Folie 119)

In den Folien als „FMEA Formular Muster" gezeigt – die genaue Spaltenstruktur ist nicht im Text erläutert; **im PDF nicht definiert**, welche Spalten ein FMEA-Formular *im Detail* enthält. Standardspalten in der Praxis sind: Prozessschritt, potenzieller Fehler, Folge, Ursache, B, A, E, RPZ, Maßnahme, Verantwortlich, Termin – diese genaue Liste steht jedoch nicht im PDF.

## Bestandteile / Aufbau

- Drei Bewertungsdimensionen B, A, E (jeweils 1–10)
- RPZ = Produkt → 1–1000
- Schwellenwerte für Handlungsbedarf

## Beispiel

Klinisch: FMEA für Medikamentengabe.
- Fehler: falsches Medikament an falsche Patientin.
- B = 10 (potenziell tödlich), A = 2 (selten dank 5R-Regel), E = 4 (Erkennung möglich, aber nicht garantiert) → RPZ = 80 → mittlere bis hohe Priorität, Maßnahmen erforderlich (z. B. Barcode-Scanning).

## Abgrenzung

- **FMEA ≠ Ishikawa.** FMEA ist *prospektiv* (was kann schiefgehen?), Ishikawa ist *retrospektiv* (warum ist es schiefgegangen?). Vgl. [[BPM - Methode - Ishikawa 7M]].
- **FMEA ≠ HAZOP, FTA.** Verwandte Methoden, im PDF nicht erwähnt.
- **RPZ-Schwellen sind heuristisch.** Die Vorlesung gibt 50/150 als Richtwerte – in anderen FMEA-Standards (z. B. AIAG-VDA 2019) wurde die RPZ-Multiplikation zugunsten einer **Risk Priority Number (Action Priority)**-Matrix abgelöst; dies ist im PDF **nicht erwähnt**.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Wie berechnet sich die Risikoprioritätszahl, und welche Skalen verwendet die Vorlesung?"

**Anwendungsfrage:** „Wenden Sie eine FMEA auf den Prozess ‚Patient zur OP vorbereiten‘ an, identifizieren Sie zwei Fehlerquellen und bewerten Sie sie."

**Diskussionsfrage:** Methodische Schwächen der RPZ-Multiplikation: Ein hoher B-Wert kann durch niedrige A oder E ausgemittelt werden – obwohl ein katastrophaler Fehler auch bei niedriger Wahrscheinlichkeit Maßnahmen verdient. Außerdem: 1×10×10 = 100 ist gleichwertig wie 10×10×1 = 100, obwohl die Risikoprofile sehr unterschiedlich sind.

**Mögliche Anschlussfragen:**
- Was bedeutet ein hoher E-Wert?
- Was ist der Unterschied zwischen FMEA und Ishikawa?
- Wo greift FMEA in der 4-Schritte-Methode?

## Verwandt

- [[BPM - Methode - Ishikawa 7M]]
- [[BPM - Methode - Schnittstellenanalyse]]
- [[BPM - Methode - 5-Warum]]
- [[BPM - Methode - Wertschoepfungsanalyse]]
- [[BPM - Phase 2 - 4-Schritte-Methode]]
- [[BPM - Paper - To Err Is Human]]

## Quelle

- Vorlesung: [[BPM - VL - Prozessmanagement Grundlagen (PzM-Kompakt)]]
- Folien/Seitenangabe: Folien 115–119
