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

# BPM - Prozesslandkarte - Ebenenmodell

> [!info] Kurzdefinition
> Das Ebenenmodell beschreibt eine sechsstufige Hierarchie zur Darstellung von Prozessen – von der Prozesslandkarte (Ebene 0) bis zu den konkreten Arbeitsanweisungen und mitgeltenden Dokumenten (Ebene 5).

## Beschreibung

Folien 66–67. Das Ebenenmodell ermöglicht es, Prozesse von der strategischen Übersicht bis zur operativen Detailanweisung konsistent zu strukturieren.

### Die sechs Ebenen (laut Folien)

| Ebene | Bezeichnung | Inhalt |
|---|---|---|
| **0** | Prozesslandkarte | Gesamtübersicht aller Prozesse auf einer Seite |
| **1** | Wertschöpfungskette | bestehend aus Hauptprozessen |
| **2** | Hauptprozesse | bestehend aus Prozessen |
| **3** | Prozesse | bestehend aus Prozessschritten und Teilprozessen |
| **4** | Teilprozesse | im Detail beschriebene Arbeitsabläufe |
| **5** | Detailunterlagen und mitgeltende Dokumente | konkrete Arbeitsanweisungen |

Als Beispiel auf Folie 66 ist „Fahrschein verkaufen" (Verkehrsunternehmen):
- Ebene 1 (Wertschöpfungskette): Personenbeförderung
- Ebene 2 (Hauptprozesse): Fahrschein verkaufen, Vertriebskanäle verwalten, Ticketverkauf durchführen, Zahlungen abwickeln
- Ebene 3 (Prozesse): Vertriebskanäle verwalten
- Ebene 4 (Teilprozesse): Onlineshop pflegen
- Ebene 5: Technische Dokumentation der Online-Systeme, FAQ, Handbücher, Vertragsdokumente

### Funktion des Ebenenmodells

- **Vom Groben ins Detail** – jede Ebene ist ein Einstiegspunkt für die nächst-tiefere.
- **Aggregation von Kennzahlen** – Kennzahlen können nach oben aggregiert werden.
- **Konsistente Dokumentation** – jede Ebene hat ihre eigene Granularität, ohne dass Information verloren geht.

## Bestandteile / Aufbau

```
Ebene 0: PLK (Übersicht)
   ↓
Ebene 1: Wertschöpfungskette (Hauptprozesse)
   ↓
Ebene 2: Hauptprozesse (Prozesse)
   ↓
Ebene 3: Prozesse (Prozessschritte, Teilprozesse)
   ↓
Ebene 4: Teilprozesse (Arbeitsabläufe im Detail)
   ↓
Ebene 5: Arbeitsanweisungen, mitgeltende Dokumente
```

## Beispiel

Klinisch übertragen:
- Ebene 0: PLK des Krankenhauses
- Ebene 1: Wertschöpfungskette „Patient stationär versorgen"
- Ebene 2: Hauptprozess „Patient operativ behandeln"
- Ebene 3: Prozess „Präoperative Diagnostik"
- Ebene 4: Teilprozess „Laborentnahme"
- Ebene 5: Arbeitsanweisung „SOP Blutabnahme", Materiallisten, Geräte­handbücher

## Abgrenzung

- **Ebenenmodell ≠ Organigramm.** Wieder: Prozessfluss vs. Hierarchie.
- **Ebenen sind keine harten Standards** – die Folien zeigen sechs Ebenen, andere Modelle in der Literatur verwenden 3–5; im PDF ist die genannte Sechs-Ebenen-Struktur definiert und nur diese sollte zitiert werden.
- **Detail ist nicht Ziel** – nicht jeder Prozess muss bis Ebene 5 dokumentiert werden; das richtet sich nach Steuerungsbedarf und Risiko.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Beschreiben Sie das Ebenenmodell der Prozessdokumentation."

**Anwendungsfrage:** „Auf welcher Ebene würden Sie eine SOP zur Hernien-OP einordnen?" – Ebene 5 (Arbeitsanweisung), eingebettet in Teilprozess „Hernien-OP durchführen" (Ebene 4) als Teil von Prozess „Hernien-Pfad" (Ebene 3).

**Diskussionsfrage:** Warum ist Ebene 0 auf eine Seite begrenzt, während Ebene 5 beliebig umfangreich sein darf? – Übersicht braucht Reduktion; Ausführung braucht Vollständigkeit.

**Mögliche Anschlussfragen:**
- Was steht auf Ebene 0?
- Wo werden SOPs angesiedelt?
- Wie hängt das Ebenenmodell mit dem Prozesslebenszyklus zusammen?

## Verwandt

- [[BPM - Prozesslandkarte - Definition]]
- [[BPM - SOP - Definition]]
- [[BPM - Prozessbeschreibung - Mindestinhalte]]

## Quelle

- Vorlesung: [[BPM - VL - Prozessmanagement Grundlagen (PzM-Kompakt)]]
- Folien/Seitenangabe: Folien 66–67
