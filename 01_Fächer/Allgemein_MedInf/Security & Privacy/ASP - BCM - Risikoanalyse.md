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

# ASP - BCM - Risikoanalyse (vs. BIA)

> [!info] Kurzdefinition
> BCM-Risiken sind nach BSI 200-4 Risiken, die sich unmittelbar auf die Verfügbarkeit zeitkritischer Ressourcen auswirken. Im Gegensatz zur BIA („was muss abgesichert werden?") fragt die Risikoanalyse „wogegen muss abgesichert werden?".

## Beschreibung

### Definition Risiko (Folie 22)

**ISO 27005:2022:**
- „Effect of uncertainty on objectives".
- Im Kontext von Informationssicherheit: „Information security risks can be expressed as effect of uncertainty on information security objectives".
- **Informationssicherheits-Risiken** beziehen sich auf die **Ausnutzung von Schwachstellen von Informationswerten**.

**BSI 200-4:**
- **BCM-Risiken** sind Risiken, die sich unmittelbar auf die **Verfügbarkeit von zeitkritischen Ressourcen** auswirken.
- Aber: Auch Verlust der Integrität einer zeitkritischen Ressource kann zu nicht tolerierbaren Geschäftsunterbrechungen führen.

### BIA vs. Risikoanalyse (Folie 23)

| Aspekt | Business Impact Analyse | Risikoanalyse |
|---|---|---|
| Leitfrage | Was muss abgesichert werden? | Wogegen muss abgesichert werden? |
| Bezug | Ressourcen- oder Prozessbezogen | Ressourcenbezogen |
| Orientierung | Wirkungsorientiert | Ursachenorientiert |
| Annahme | Blendet vorhandene Maßnahmen aus (worst case) | Berücksichtigt vorhandene Risiko-reduzierende Maßnahmen |
| Ergebnis | Zeitwert (MTPD, RTO, RPO) | Risikowert |

**Schnittmenge:** Beide treffen sich im Begriff **„Impact"** (Folie 23 visualisiert das als Venn-Diagramm).

## Bestandteile / Aufbau

| Element | Bedeutung |
|---|---|
| Bedrohung | Ursache (z. B. Stromausfall, Cyberangriff) |
| Schwachstelle | Verwundbarkeit (z. B. fehlendes USV-Backup) |
| Eintrittswahrscheinlichkeit | wie oft tritt die Bedrohung auf? |
| Auswirkung (Impact) | wie schwer? – siehe BIA |
| Risikowert | Eintrittswahrscheinlichkeit × Auswirkung |

## Beispiel

Bedrohung „Stromausfall" mit Schwachstelle „fehlendes USV-Backup":
- BIA-Sicht: Welche Prozesse fallen aus, wie schnell wird das untragbar? → MTPD = 4 h, RTO = 2 h, RPO = 1 h.
- Risikoanalyse-Sicht: Wie wahrscheinlich ist ein Stromausfall? Welche Maßnahmen reduzieren das Risiko (USV, Generator)? → Risikowert (z. B. „mittel").

## Abgrenzung

- **BIA blendet bestehende Maßnahmen aus** und arbeitet im Worst-Case-Szenario. Risikoanalyse zieht bestehende Maßnahmen ein und bewertet das Restrisiko.
- **Wirkungs- vs. Ursachen-Orientierung:** BIA fragt „was passiert, wenn etwas ausfällt?". Risikoanalyse fragt „was kann ausfallen, und warum?".
- **ISO 27005 vs. BSI 200-4:** ISO 27005 ist allgemeiner Rahmen für Informationssicherheits-Risiken. BSI 200-4 ist spezifisch für BCM-Risiken (Fokus auf Verfügbarkeit zeitkritischer Ressourcen).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie wird Risiko in ISO 27005:2022 und in BSI 200-4 definiert? Worin unterscheiden sich BIA und Risikoanalyse?

**Anwendungsfrage:** Skizzieren Sie an einem konkreten Beispiel (z. B. zentrales KIS) den Beitrag von BIA und Risikoanalyse. Wo überlappen sie sich, wo ergänzen sie sich?

**Diskussionsfrage:** Warum reicht eine BIA allein nicht aus, um BC-Strategien zu entwickeln? Warum reicht eine reine Risikoanalyse ebenfalls nicht aus? (BIA sagt nichts über Eintrittswahrscheinlichkeit; Risikoanalyse sagt nichts über die operative Schmerzgrenze.) Welche Kombination ist praktisch nötig?

**Mögliche Anschlussfragen:**
- Was bedeutet „effect of uncertainty on objectives" konkret im Krankenhaus-Kontext?
- Warum nennt BSI 200-4 explizit auch die Integrität als BCM-relevant?
- Wie hängt das mit der CIA-Triade zusammen?

## Verwandt

- [[ASP - BCM - Business Impact Analyse]]
- [[ASP - BCM - Soll-Ist-Vergleich]]
- [[ASP - BCM - Normen]]
- [[ASP - VL - Informationssicherheits-Risikomanagement]]
- [[ASP - Informationssicherheit - CIA-Triade]]

## Quelle

- Vorlesung: [[ASP - VL - Business Continuity Management]]
- Folien/Seitenangabe: Folien 22, 23
