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

# ASP - BCM - BIA-Kenngrößen (MTPD, RPO, RTO, MBCO)

> [!info] Kurzdefinition
> Vier zentrale Kenngrößen aus der BIA-Durchführung: MTPD (maximal tolerierbare Ausfallzeit), RPO (maximal zulässiger Datenverlust), RTO (geforderte Wiederanlaufzeit), MBCO (Notbetriebsniveau).

## Beschreibung

Folie 15 nennt die vier Kenngrößen. Folie 17 zeigt sie in einem Zeit-/Geschäftsbetrieb-Diagramm.

### Maximal tolerierbare Ausfallzeit (MTPD)
- **MTPD = Maximum Tolerable Period of Disruption**
- Maximal tolerierbare Ausfallzeit eines Prozesses bevor das Schadenspotenzial untragbar wird.
- Wird in der BIA pro Prozess durch Beobachtung des Schadenspotenzials über Zeit-Horizonte ermittelt.

### Maximal zulässiger Datenverlust (RPO)
- **RPO = Recovery Point Objective**
- Wie weit darf der Datenstand vor einem Schadensereignis maximal zurückliegen?
- Beispiel: RPO = 4 Stunden bedeutet, dass bei einem Vorfall maximal die letzten 4 Stunden Daten verloren gehen dürfen.

### Geforderte Wiederanlaufzeit (RTO)
- **RTO = Recovery Time Objective**
- Wie schnell muss der Prozess nach einem Schadensereignis wieder verfügbar sein?
- Bezieht sich auf den Zeitpunkt zwischen Schadensereignis und (erneutem) Erreichen des Notbetriebsniveaus.

### Notbetriebsniveau (MBCO)
- **MBCO = Minimum Business Continuity Objective**
- Auf welches Mindest-Leistungsniveau soll der Prozess im Notbetrieb gebracht werden?
- Beispiel: 50 % Kapazität reicht in der Notaufnahme aus, um Akutfälle zu versorgen.

### Diagramm (Folie 17)
```
Geschäftsbetrieb 100% ─────────────────● Schadensereignis
                     Letzte             ↓
                     Datensicherung     Detektion/Alarmierung
                                        ↓
Notbetriebsniveau ─────────────────────────●─────────●─→
                                            (Wiederanlauf) (Notbetrieb)
                                            
                     ←── RPO ──→        ←── RTO ──→
                                            ←──── MTPD ──────→
```
- **RPO:** Abstand zwischen letzter Datensicherung und Schadensereignis.
- **RTO:** Abstand zwischen Schadensereignis und Wiederanlauf auf Notbetriebsniveau.
- **MTPD:** Maximaler Gesamt-Abstand vom Schadensereignis bis Erreichen des Notbetriebs.
- **MBCO:** Höhe des Notbetriebsniveau (auf y-Achse).

## Bestandteile / Aufbau

| Kenngröße | Voller Name | Was misst sie? | Beispiel |
|---|---|---|---|
| MTPD | Maximum Tolerable Period of Disruption | maximal tolerierbare Ausfallzeit | 7 Tage |
| RPO | Recovery Point Objective | maximaler Datenverlust | 4 Stunden |
| RTO | Recovery Time Objective | geforderte Wiederanlaufzeit | 3 Tage |
| MBCO | Minimum Business Continuity Objective | Notbetriebsniveau | 50 % Normalleistung |

## Beispiel

Aus Folie 15: Geschäftsprozess „Schlüsselkunden betreuen" – nach Tabelle MTPD = 7 Tage. Wenn Backup täglich (RPO = 24 h) und Wiederanlaufprozess in 3 Tagen (RTO = 3 Tage), passt das in die MTPD-Vorgabe.

## Abgrenzung

- **MTPD ≥ RTO:** Die geforderte Wiederanlaufzeit muss innerhalb der maximal tolerierbaren Ausfallzeit liegen, sonst ist die Vorgabe unerreichbar.
- **RTO ≠ RTA:** RTO ist die geforderte (SOLL), RTA ist die tatsächlich erreichte (IST). Siehe [[ASP - BCM - Soll-Ist-Vergleich]].
- **RPO ≠ RPA:** Analog – RPO ist Soll, RPA ist Ist.
- **MBCO ist eine Niveau-Angabe**, nicht eine Zeit-Angabe – nicht mit den anderen Kenngrößen verwechseln.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Definiere MTPD, RPO, RTO und MBCO. Welche misst Zeit, welche Datenverlust, welche Leistungsniveau?

**Anwendungsfrage:** Skizziere die vier Kenngrößen in einem Zeit-/Leistungs-Diagramm. Wo liegt das Schadensereignis? Wo der Wiederanlauf?

**Diskussionsfrage:** Welche Kenngröße bestimmt die Backup-Strategie, welche die Recovery-Strategie? (RPO bestimmt Backup-Frequenz; RTO bestimmt Recovery-Geschwindigkeit/Hot-Standby vs. Cold-Standby.) Wie hängt MBCO mit RTO zusammen? (Niedrigeres MBCO ist meist schneller erreichbar als 100 %.)

**Mögliche Anschlussfragen:**
- Welche Kenngröße ist „Soll", welche „Ist"? (Alle vier sind Soll-Werte; Ist-Pendants sind RTA, RPA – siehe Soll-Ist-Vergleich.)
- Was passiert, wenn RTO > MTPD? (Die Vorgabe ist unerreichbar; das Geschäft kommt vor Wiederanlauf zum Stillstand.)
- Wie ändern sich die Kenngrößen, wenn man das Notbetriebsniveau (MBCO) absenkt? (RTO sinkt typischerweise.)

## Verwandt

- [[ASP - BCM - Business Impact Analyse]]
- [[ASP - BCM - Soll-Ist-Vergleich]]
- [[ASP - BCM - Risikoanalyse]]
- [[ASP - Informationssicherheit - CIA-Triade]]

## Quelle

- Vorlesung: [[ASP - VL - Business Continuity Management]]
- Folien/Seitenangabe: Folien 15, 17
