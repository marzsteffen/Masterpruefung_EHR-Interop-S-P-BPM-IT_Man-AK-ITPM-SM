---
fach: bpm
typ: konzept
status: offen
quelle: "[[BPM - VL - ACS-NSQIP]]"
tags:
  - fach/vertiefung/bpm
  - typ/konzept
  - status/offen
---

# BPM - NSQIP - Datenerhebung

> [!info] Kurzdefinition
> Die Datenerhebung in NSQIP basiert auf **klinischen Variablen aus der Krankenakte**, die durch eine **speziell geschulte Datenerhebungskraft (DGK)** pro Standort erfasst, durch **Plausibilitätsfilter** geprüft, durch **Inter-Rater-Reliability-Audits** abgesichert und in einem **Data Warehouse** für Risikoadjustierung verwendet werden.

## Beschreibung

Folie 7 zeigt das Datenerhebungs-Schema. Die Datenerhebung ist die zentrale Voraussetzung für alle nachfolgenden Schritte (Risikoadjustierung, O/E-Ratios, Benchmarking).

### Datenquellen pro Standort

- **Krankenakte** des Patienten – primäre Datenquelle.
- **Telefon-Kontakt** mit dem/der Patient:in oder behandelnden Hausärzt:in zur Erfassung postoperativer Ereignisse innerhalb der **30-Tage-Frist**.
- **Chirurg** – fachliche Klärung bei unklaren Befunden.

### Akteure und Prozessfluss

```
Krankenakte ──┐
              ├─→ DGK ──→ Datenfile ──→ Plausibilitätsfilter ──→ Abteilungs-
Telefon ──────┤                                                  vergleiche
              │                                                       │
Chirurg ──────┘                                                       ▼
                                                              Data Warehouse
                                                  ┌──────────────────┴──────────────────┐
                                                  ▼                                     ▼
                                            Risikofaktoren                          Outcome
                                                                          (Mortalität, Komplikationen)
                                                                                      │
                                          Exakte Definitionen ◄──────────────────────┤
                                                                                      ▼
                                                                              Patientenprofile
                                                  ┌──────────────────┐
                                                  ▼                  ▼
                                          Unadjustierte         Risikoadjustierung
                                          Zahlen
```

### Qualitätssichernde Elemente

| Element | Funktion |
|---|---|
| **Schulung der DGK** | Standardisierte Anwendung der Definitionen |
| **Plausibilitätsfilter** | Auffangen von Eingabefehlern |
| **IR-Reliability** (Inter-Rater-Reliability) | Stichprobenartige Doppelerhebung; Auditkennzahl |
| **Exakte Definitionen** | Was zählt als „Wundinfekt 30 Tage post-OP"? – jede Variable hat eine OP-Definition. |
| **Jährliche Audits** | Standortbezogene Datenqualitätsprüfung |
| **30-Tage-Outcome** | Erfassung auch nach Entlassung (Telefon, Hausarzt-Kontakt) |

### Vergleich Krankenakte vs. Verrechnungsdaten (Folie 5)

NSQIP-Daten aus der Krankenakte zeigen ggü. administrativen (Verrechnungs-)Daten:
- **+61 %** Komplikationen identifiziert
- **+97 %** Infektionen an OP-Stellen
- **+100 %** Harnwegsinfekte

→ Verrechnungsdaten sind systematisch unvollständig für klinische Qualitätsmessung.

## Bestandteile / Aufbau

- Drei Datenquellen pro Patient (Akte, Telefon, Chirurg)
- DGK pro Standort als zentrale Erhebungsperson
- Plausibilitätsfilter, IR-Reliability als Datenqualitäts­tools
- Data Warehouse als Aggregationsebene
- Trennung in Risikofaktoren und Outcome-Variablen

## Beispiel

Patient nach Hernien-OP: Tag 0 in OP, Tag 1–3 stationär (Krankenakte erfasst), Tag 4 Entlassung. DGK ruft am Tag 30 den Patienten an: „Hatten Sie Wundheilungs­störungen, neue Beschwerden, Wiederaufnahmen?" – Ergebnis fließt in das 30-Tage-Outcome-Datenfile ein. Wenn der Patient z. B. eine ambulant behandelte Wundinfektion meldet, wird sie im Komplikations-Set mitgezählt – obwohl sie in der Krankenakte des aufnehmenden Hauses nicht stehen würde.

## Abgrenzung

- **NSQIP-DGK ≠ klinische Pflegekraft mit Doppelaufgabe.** Die DGK ist *ausschließlich* der Datenerhebung gewidmet, nicht der Pflege im Stationsalltag – sonst leidet die Datenqualität.
- **NSQIP-Daten ≠ DRG-Daten.** DRG nutzt Abrechnungs­diagnosen; NSQIP nutzt klinische Beobachtung.
- **30-Tage-Outcome ≠ Hospitalverbleib.** Auch nach Entlassung läuft die Erfassung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** „Wie ist die Datenerhebung im NSQIP-Prozess organisiert?"

**Anwendungsfrage:** „Welche Daten werden über welchen Kanal erfasst?" – Krankenakte für intraop. + initiale postop. Daten; Telefon für 30-Tage-Outcome; Chirurg für klinische Klärung.

**Diskussionsfrage:** Warum scheitern viele Klinik-QM-Initiativen bereits an der Datenerhebung? – Daten werden „nebenbei" durch Stationspersonal erhoben → unvollständig, nicht standardisiert; ohne dedizierte DGK keine vergleichbaren Daten. NSQIP-Lehre: dediziertes, geschultes Personal ist der Engpass.

**Mögliche Anschlussfragen:**
- Was ist die IR-Reliability und wozu dient sie?
- Wie wird das 30-Tage-Outcome konkret erhoben?
- Warum ist die DGK von der Stationspflege getrennt?
- Welche Vorteile hat die Krankenakte gegenüber Verrechnungsdaten?

## Verwandt

- [[BPM - NSQIP - Programm]]
- [[BPM - NSQIP - Risikoadjustierung]]
- [[BPM - NSQIP - O-E-Ratio]]
- [[BPM - Komplikation - Definition]]
- [[BPM - Methode - Wertschoepfungsanalyse]]

## Quelle

- Vorlesung: [[BPM - VL - ACS-NSQIP]]
- Folien/Seitenangabe: Folien 4 (VA-Antwort), 5 (Krankenakte vs. Verrechnung), 7 (Datenerhebungs-Schema)
