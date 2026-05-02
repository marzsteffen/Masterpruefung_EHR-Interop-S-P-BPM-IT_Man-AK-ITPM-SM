---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Einfuehrung und Motivation]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Security Eigenschaften - Verantwortlichkeit (Accountability)

> [!info] Kurzdefinition
> Durchgeführte Handlungen müssen einem Akteur zurechenbar sein (laut Folie 14).

## Beschreibung

Accountability (Verantwortlichkeit) ist die Sicherheits-Eigenschaft, dass jede Handlung im System eindeutig einer handelnden Person oder einem System-Akteur zugeordnet werden kann. Auf der Security-Grafik (Folie 13) ist sie eines der acht Schutzziele, definiert auf Folie 14 mit einer einzigen Zeile.

Die Vorlesung benennt keine konkreten technischen Realisierungen für Accountability. **Im PDF nicht definiert:** typische Mechanismen (in der Praxis: Audit-Logs, eindeutige Benutzerkonten, Login-Tracking, Audit Trails). Diese Konkretisierung gehört vermutlich zur Folge-Vorlesung Identitätsmanagement.

## Beispiel

*Im PDF nicht explizit als Beispiel ausgewiesen.* In eHealth-Systemen wird Accountability klassisch durch Audit Trails realisiert (siehe Cross-Fach-Verbindung [[EHR - MOC]] – Audit Trails).

## Abgrenzung

- **Accountability vs. Authenticity:** Authentizität ist Voraussetzung für Accountability – ohne authentifizierte Identität ist keine Zurechenbarkeit möglich. Accountability geht aber weiter und verlangt zusätzlich eine Spur (Log).
- **Accountability vs. Non-repudiation:** Beide setzen Zurechenbarkeit voraus. Non-repudiation ist der „starke" Beweisbarkeits-Modus (auch gegenüber Dritten/Gerichten); Accountability ist meist die intern-organisatorische Variante. *Im PDF nicht explizit getrennt.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet Accountability als Schutzziel?

**Anwendungsfrage:** Welche technischen und organisatorischen Maßnahmen unterstützen Accountability in eHealth-Systemen?

**Diskussionsfrage:** Warum genügt ein gutes Identitätsmanagement allein nicht, um Accountability zu erfüllen? (Antwort: Auch die Zurechnung der konkreten Aktion benötigt einen Log/Audit Trail.)

**Mögliche Anschlussfragen:**
- Welcher Zusammenhang besteht zwischen Audit-Trails und Accountability?
- Wie hängt DSGVO Art. 5 Abs. 2 (Rechenschaftspflicht) mit Accountability zusammen? (*Hinweis: im PDF dieser Vorlesung nicht enthalten – evtl. Folge-Vorlesung Risikomanagement.*)

## Verwandt

- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Security Eigenschaften - Non-repudiation]]
- [[EHR - Audit Trail - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folien 13, 14
