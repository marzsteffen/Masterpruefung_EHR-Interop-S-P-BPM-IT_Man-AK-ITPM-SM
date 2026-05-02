---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Informationssicherheits-Risikomanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Risikomanagement - Überwachung und Verbesserung (KPI vs. KRI)

> [!info] Kurzdefinition
> Kontinuierliche Verbesserung des Risikomanagement-Prozesses durch Mess-Indikatoren. **KPI** (Key Performance Indicators) messen Erfolg/Effektivität von Aktivitäten. **KRI** (Key Risk Indicators) überwachen potenzielle Risiken. Beide brauchen Schwellwerte und Verantwortliche.

## Beschreibung

### Kontinuierliche Verbesserung (Folie 44)
Ziel: Erhöhung der Wirksamkeit des Risikomanagement-Prozesses, Optimierung der Schutzmaßnahmen.

Verbesserung in einzelnen Schritten:
- Definition von Zielen und Anforderungen des Risikomanagement-Prozesses.
- Ggf. Neubewertung von Risiken.
- Identifikation von Verbesserungsmöglichkeiten.
- Maßnahmen zur Verbesserung der Risikobewertung und -kontrolle.
- Überwachung der Ergebnisse der Verbesserungsmaßnahmen.

### KPI vs. KRI (Folie 45)

**Key Performance Indicators (KPIs)** sind Messgrößen, die verwendet werden, um den **Erfolg oder die Effektivität** einer bestimmten Aktivität oder eines Prozesses zu bewerten.

**Key Risk Indicators (KRIs)** konzentrieren sich auf die **Überwachung von potenziellen Risiken**.

KRIs dienen dazu:
- Die **Wirksamkeit von Maßnahmen** zur Risikominderung und -kontrolle zu messen und zu bewerten.
- Die Wirksamkeit der **Risikomanagement-Strategie** zu messen, Risiken besser zu verstehen und Ressourcen gezielter einzusetzen.

**Wichtig:**
- Die richtige Auswahl von KRI und KPI ist entscheidend für eine **hohe Aussagekraft und Relevanz**.
- Für KRI/KPI muss immer ein **Zielwert / Schwellwert** definiert werden.

### Beispiel KRI (Folie 46)

| KRI | Beschreibung | Verantwortlicher | Schwellwert |
|---|---|---|---|
| Anzahl erfolgreicher Angriffe auf das Netzwerk pro Monat | Hohe Anzahl erfolgreicher Angriffe auf das Netzwerk kann ein Indiz für Schwachstellen in der Netzwerksicherheit sein. Erhebung: Monitoring von Netzwerklogs, IDS-Auswertung, Schwachstellen-Scans. | IT-Abteilung | 5 erfolgreiche Angriffe pro Monat |

## Bestandteile / Aufbau

| Aspekt | KPI | KRI |
|---|---|---|
| Fokus | Erfolg / Effektivität | Risiko-Überwachung |
| Beispiele | „Patch-Quote 95 %", „MTTR < 4h" | „Erfolgreiche Angriffe / Monat", „Phishing-Klickrate" |
| Pflicht-Felder | Beschreibung, Verantwortlicher, Zielwert | Beschreibung, Verantwortlicher, Schwellwert |
| Überschreitung | unter Zielwert = Handlungsbedarf | über Schwellwert = automatische Maßnahme auslösen |

## Beispiel

KRI „Anzahl gefälschter Login-Versuche pro Stunde". Ziel: Risiko von Brute-Force-Angriffen frühzeitig erkennen. Verantwortlich: IT-Sicherheits-Team. Schwellwert: 100 pro Stunde → ab dann automatisch Account-Sperre und Eskalation.

## Abgrenzung

- **KPI ≠ KRI:** KPI misst, ob etwas gut läuft. KRI misst, ob etwas drohend schief läuft. Beide ergänzen sich.
- **KRI ≠ Risiko selbst:** KRI ist ein *Indikator* (Vorlauf-Größe), das tatsächliche Risiko ergibt sich aus Wahrscheinlichkeit × Auswirkung.
- **Schwellwert ist nicht statisch:** Schwellwerte sollten mit der Risikolage angepasst werden.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was sind KPIs und KRIs, und wie unterscheiden sie sich?

**Anwendungsfrage:** Schlagen Sie drei KRIs für ein Krankenhaus vor – mit Beschreibung, Verantwortlichem, Schwellwert (siehe Folie 46 als Vorlage).

**Diskussionsfrage:** Welche Probleme entstehen bei schlechter Wahl von KRI/KPI? (Falsche Sicherheit, blinde Flecken, Manipulation der Indikatoren.) Wie hängt die Indikator-Wahl mit der Risikomatrix zusammen?

**Mögliche Anschlussfragen:**
- Welche Phase im 7-Schritte-Big-Picture entspricht „Überwachung und Verbesserung"?
- Wie hängt das mit dem PDCA-Zyklus aus dem BCM zusammen? (Beide sind kontinuierliche Verbesserungsschleifen.)
- Welche KPIs sind für den Risikomanagement-Prozess selbst sinnvoll? (Anzahl identifizierter Risiken; Anzahl Risiken in Behandlung; Restrisiko-Summe.)

## Verwandt

- [[ASP - Risikomanagement - Big Picture]]
- [[ASP - Risikomanagement - Risikobehandlung]]
- [[ASP - Risikomanagement - Risikokommunikation]]
- [[ASP - BCM - Managementsystem]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 44, 45, 46
