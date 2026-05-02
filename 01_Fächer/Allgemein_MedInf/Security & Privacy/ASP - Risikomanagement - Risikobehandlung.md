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

# ASP - Risikomanagement - Risikobehandlung (4 Strategien + Plan)

> [!info] Kurzdefinition
> Vier Basis-Strategien zur Risikobehandlung: Vermeidung, Reduktion, Transfer, Akzeptanz. Maßnahmen werden in einem Risikobehandlungsplan dokumentiert (Risiko, Strategie, Maßnahme, Termin, Verantwortlich, Kosten, Auswirkung, Restrisiko).

## Beschreibung

### Ziele der Risikobehandlung (Folie 39)
- **Reduzierung des Risikos auf ein akzeptables Niveau.**
- Festlegung sinnvoller Maßnahmen.
- Berücksichtigung wirtschaftlicher Aspekte (personelle und finanzielle Ressourcen).

### Vier Basis-Strategien (Folie 40)

1. **Vermeidung:** Gewisse Tätigkeiten/Prozesse werden nicht durchgeführt, um das Risiko zu eliminieren.
2. **Reduktion:** Risikoreduzierende Maßnahmen werden implementiert.
3. **Transfer:** Verlagerung der Verantwortung des Risikos (z. B. Abschluss einer Versicherung).
4. **Akzeptanz:** Restrisiko wird in Kauf genommen.

### Risikobehandlungsplan (Folie 41)

Tabellarische Dokumentation pro Risiko:

| Risiko | Strategie | Konkrete Maßnahme | Umsetzung bis | Verantwortlich | Kosten | Auswirkung auf Risiko | Restrisiko |
|---|---|---|---|---|---|---|---|
| 1 | Reduzierung | Neue Firewall einrichten | 31.03. | Meier | 25 000 € + 5 000 € p.a. | EW −20 % | 52 000 € |
| 1 | Transfer | Cyberversicherung abschließen | 31.04. | Dr. Hubertus | 30 000 € jährlich | A −80 % | 10 000 € |
| 2 | Vermeidung | Onlineshop schließen | 15.03. | Dr. Hubertus | 5 000 € | eliminiert | 0 |
| 3 | Reduzierung | Neue Firewall einrichten | 31.03. | Meier | (25 000 €) | EW −25 % | 60 000 € |
| 3 | Reduzierung | IDS installieren | 15.05. | Meier | 40 000 € + 12 000 € p.a. | EW −10 %, A −40 % | 15 000 € |

(EW = Eintrittswahrscheinlichkeit, A = Auswirkung.)

**Beobachtung aus der Tabelle:**
- Pro Risiko können **mehrere Strategien** kombiniert werden.
- Jede Maßnahme hat einen **Termin und Verantwortlichen**.
- **Restrisiko** wird ausgewiesen (Eingangswert minus Wirkung der Maßnahme).

## Bestandteile / Aufbau

| Strategie | Mechanismus | Beispiel |
|---|---|---|
| Vermeidung | Tätigkeit weglassen | Onlineshop einstellen |
| Reduktion | Maßnahme implementieren | Firewall, IDS, Patches |
| Transfer | Risiko auslagern | Versicherung, Outsourcing |
| Akzeptanz | Restrisiko hinnehmen | Geschäftsführung dokumentiert die Entscheidung |

## Beispiel

Direkt aus Folie 41 oben.

## Abgrenzung

- **Strategien können kombiniert werden.** Folie 41 zeigt das explizit: Risiko 1 wird sowohl reduziert (Firewall) als auch transferiert (Versicherung).
- **Akzeptanz ≠ Ignorieren.** Auch akzeptierte Risiken müssen dokumentiert und überwacht werden.
- **Vermeidung ist nicht immer machbar** – manchmal ist die Tätigkeit Kernbestandteil des Geschäfts.
- **Transfer eliminiert das Risiko nicht** – die Versicherung deckt nur die finanzielle Folge, nicht den Reputationsschaden oder die operativen Folgen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Risikobehandlungs-Strategien gibt es, und wie funktionieren sie?

**Anwendungsfrage:** Ordnen Sie konkrete Maßnahmen (z. B. „Cyber-Versicherung", „Patches einspielen", „Geschäftszweig einstellen", „Risiko dokumentieren und akzeptieren") den vier Strategien zu.

**Diskussionsfrage:** Welche Strategie ist für welches Szenario im Gesundheitswesen am besten geeignet? (Beispiel: Patientensicherheit → Reduktion und ggf. Vermeidung; Reputationsrisiken → ggf. Transfer; Datenverlust → meist Reduktion.) Wann ist Akzeptanz die richtige Strategie?

**Mögliche Anschlussfragen:**
- Wie ändert sich das Restrisiko durch Kombination zweier Strategien?
- Welche wirtschaftlichen Faktoren fließen in die Wahl der Strategie? (Kosten der Maßnahme vs. Schadenshöhe × Wahrscheinlichkeit.)
- Wie wird die Wirksamkeit einer Maßnahme messbar gemacht? (Über KRI – siehe [[ASP - Risikomanagement - Ueberwachung KPI KRI]].)

## Verwandt

- [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]
- [[ASP - Risikomanagement - Big Picture]]
- [[ASP - Risikomanagement - Ueberwachung KPI KRI]]
- [[ASP - Risikomanagement - Risikokommunikation]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 39, 40, 41
