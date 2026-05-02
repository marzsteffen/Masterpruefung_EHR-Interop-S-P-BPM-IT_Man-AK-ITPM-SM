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

# ASP - Risikomanagement - Strukturanalyse und Schutzbedarfsfeststellung

> [!info] Kurzdefinition
> Erster Schritt der asset-basierten Risikoidentifikation. Top-Down-Auflistung aller Assets (von Geschäftsprozess über Anwendungen zu IT-Systemen) und Festlegung des Schutzbedarfs pro Asset für die CIA-Schutzziele. Schutzbedarf kann vererbt werden.

## Beschreibung

### Strukturanalyse (Folie 21)

- **Detaillierte Auflistung aller Assets** und ihrer Abhängigkeiten.
- Beginnt bei **Geschäftsprozessen und Informationen**.
- **Top-Down-Approach:** Von Prozess-Ebene auf Anwendungs-Ebene und danach auf IT-System-Ebene.
- Erleichtert die Schutzbedarfsfeststellung einzelner Assets durch eine **mögliche Vererbung des Schutzbedarfs** (Wenn ein Prozess als hochsensibel klassifiziert ist, sind die darunter liegenden Anwendungen und Systeme typischerweise mindestens genauso sensibel.)

### Visualisierung (Folie 20)

```
Unternehmenskontext: IT, Beschaffung, Produktion, Vertrieb, Verwaltung, HR, ...
        ↓
Unternehmensprozesse (pro Bereich)
        ↓
Unternehmensassets (A1, A2, A3, ..., A17, ...)
        ↓
Filterung: hoch schützenswerte Assets (A2, A3, A5, A8, A9, A11, A14, A15, A17, ...)
```

### Schutzbedarfsfeststellung (Folie 22)

Pro Asset wird der Schutzbedarf für die drei **CIA-Schutzziele** in Klassen (z. B. 1–5) eingestuft – jeweils mit **Begründung**.

**Beispiel Active Directory (Folie 22):**

| Schutzziel | Schutzbedarf | Begründung |
|---|---|---|
| Vertraulichkeit | 5 | Im Active Directory sind sensible Mitarbeiterdaten (z. B. Passwörter) gespeichert. |
| Integrität | 5 | Alle Mitarbeiter identifizieren sich mit Passwörtern; Schutzbedarf der Integrität der gespeicherten Daten ist sehr hoch. |
| Verfügbarkeit | 5 | Bei Ausfall des Authentisierungssystems können Mitarbeiter sich nicht identifizieren; eine Ausführung von IT-Verfahren ist dann nicht möglich. Ein Ausfall von mehr als 4 Stunden ist nicht hinnehmbar. |

## Bestandteile / Aufbau

| Schicht | Inhalt | Beispiel |
|---|---|---|
| Geschäftsprozesse | übergeordnete Abläufe | Patientenaufnahme |
| Anwendungen | Software, die Prozesse unterstützt | KIS, ELGA-Konnektor |
| IT-Systeme | Hardware/OS-Schicht | Server, Datenbanken, Netzwerke |
| Informationen | Datenobjekte | Patientendaten, Befunde |

## Beispiel

Direkt aus Folie 22 oben.

## Abgrenzung

- **Strukturanalyse ≠ vollständiges Asset-Inventar:** Strukturanalyse fokussiert auf das, was für Risikomanagement relevant ist; ein Asset-Inventar im IT-Service-Management kann darüber hinausgehen.
- **Schutzbedarfsfeststellung ≠ Risikoanalyse:** Schutzbedarf bewertet, *wie wichtig* ein Asset ist; Risikoanalyse bewertet, *wie hoch das Risiko* tatsächlich ist (inkl. Wahrscheinlichkeit). Schutzbedarf ist die Vorstufe.
- **Vererbung des Schutzbedarfs** ist die Standard-Annahme; Ausnahmen können dokumentiert werden, sind aber selten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist eine Strukturanalyse, und was ist eine Schutzbedarfsfeststellung? Welcher Approach wird gewählt (Top-Down/Bottom-Up)?

**Anwendungsfrage:** Bestimmen Sie für ein konkretes Asset (z. B. ELGA-Backend) den Schutzbedarf für CIA mit Begründung.

**Diskussionsfrage:** Warum ist die Vererbung des Schutzbedarfs sinnvoll? In welchen Ausnahmefällen ist sie nicht angemessen? (Beispiel: Ein lebenskritisches Frontend hat hohe Verfügbarkeitsanforderungen, das dahinterliegende Statistik-Modul vielleicht nicht.)

**Mögliche Anschlussfragen:**
- Wie hängt die Schutzbedarfsfeststellung mit der CIA-Triade zusammen?
- Welche Klassen-Anzahl ist sinnvoll (3, 4, 5)?
- Wie wird der Schutzbedarf von der Strukturanalyse in die nächsten Schritte übergeben? (Über die Bausteine in Schritt 2.)

## Verwandt

- [[ASP - Risikomanagement - Asset-basierte Identifikation]]
- [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]]
- [[ASP - Informationssicherheit - CIA-Triade]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 20, 21, 22
