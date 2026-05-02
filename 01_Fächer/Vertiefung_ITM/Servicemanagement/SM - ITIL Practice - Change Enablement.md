---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - ITIL Practice - Change Enablement

> [!info] Kurzdefinition
> ITIL-4-Practice (Service Management) zur Maximierung der Anzahl erfolgreicher Service- und Produktänderungen durch Sicherstellung, dass Risiken richtig bewertet wurden, Genehmigung von Changes und Verwaltung des Change-Kalenders. Auch bekannt als Change Control. Drei Change-Arten: Standard, Normal, Notfall.

## Beschreibung

Folien 83–88 vertiefen die Practice. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

**Zweck (Folie 83/84):**
> „Die Maximierung der Anzahl erfolgreicher Service- und Produktänderungen durch das Sicherstellen, dass Risiken richtig bewertet wurden, die Genehmigung von Changes und die Verwaltung des Change Kalenders."

**Definition Change:**
> „Das Hinzufügen, Modifizieren oder Entfernen eines Elements, das direkte oder indirekte Auswirkungen auf Services haben könnte."

**Scope (Folie 85):**
> „Der Umfang der Practice ‚Change Enablement' wird von jeder Organisation definiert. Sie umfasst i. d. R. die gesamte IT-Infrastruktur, Anwendungen, Dokumentation, Prozesse, Lieferantenbeziehungen und alles, was direkt oder indirekt Auswirkungen auf ein Produkt oder einen Service haben kann. Change Enablement muss die Notwendigkeit von Changes, die einen zusätzlichen Nutzen bringen, mit der Notwendigkeit in Einklang bringen, Kunden und Anwender vor den negativen Auswirkungen von Changes zu schützen."

**Wichtige Abgrenzung (Folie 85):**
> „Es ist wichtig, ‚Change Enablement' von ‚Organizational Change Management' zu unterscheiden! Organizational Change Management bearbeitet die mitarbeiterbezogenen Aspekte von Changes, damit Verbesserungen und organisatorische Transformationsinitiativen erfolgreich implementiert werden. Der Fokus des Change Enablements liegt normalerweise auf Changes an Produkten und Services."

**3 Arten von Changes (Folie 86):**

| Art | Beschreibung |
|---|---|
| **Standard Changes** | Vorautorisierte Changes mit geringem Risiko, die wohlverstanden und umfassend dokumentiert sind und die ohne zusätzliche Autorisierung implementiert werden können. |
| **Normale Changes** | Changes, die nach einem Standardprozess geplant, bewertet und autorisiert werden müssen. Change-Modelle, die auf dem Typ von Change basieren, bestimmen die Rollen für die Bewertung und Autorisierung. Auslöser für die Initiierung eines normalen Changes ist das Erstellen eines Change Request. |
| **Notfall Changes** | Changes, die so schnell wie möglich umgesetzt werden müssen. Notfall Changes sind normalerweise nicht in einem Change-Kalender enthalten, und der Prozess der Bewertung und Autorisierung wird beschleunigt, damit sie schnell implementiert werden können. |

**Change Autorität (Folie 87):**
> „Alle Changes sollten von Personen bewertet werden, die in der Lage sind, die Risiken und den erwarteten Nutzen zu verstehen. Danach müssen die Changes – vor ihrer Anwendung – autorisiert werden. Die Person oder Gruppe, die einen Change autorisiert, wird als eine Change Autorität bezeichnet. Es ist wichtig, dass jedem Change-Typ die richtige Change-Autorität zugewiesen wird, damit das Change Enablement sowohl effizient als auch effektiv sein kann."

**Change Kalender (Folie 88):**
> „Der Change-Kalender wird verwendet, um die Planung von Changes zu unterstützen, die Kommunikation zu vereinfachen, Konflikte zu vermeiden und Ressourcen zuzuweisen. Er kann nach der Bereitstellung von Changes verwendet werden, um Informationen zur Verfügung zu stellen, die für das Incident Management, das Problem Management und die Verbesserungsplanung erforderlich sind."

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Definition Change | Hinzufügen, Modifizieren oder Entfernen eines Elements mit Service-Auswirkungen |
| Scope | IT-Infrastruktur, Anwendungen, Dokumentation, Prozesse, Lieferantenbeziehungen |
| Balance | Nutzen vs. Schutz vor negativen Auswirkungen |
| Drei Change-Arten | Standard / Normal / Notfall |
| Change Autorität | Person oder Gruppe, die Change autorisiert |
| Change Kalender | Planungswerkzeug, auch nachträglich für Incident/Problem-Analyse nützlich |

## Beispiel

Krankenhaus-IT:
- **Standard:** Routine-Patch der Office-Tools (vorautorisiert).
- **Normal:** KIS-Update auf neue Major-Version (Change Request, CAB-Bewertung, Test-Phase, geplante Wartungszeit).
- **Notfall:** kritischer Sicherheits-Patch (zero-day) — beschleunigte Bewertung, sofortige Implementierung.

## Abgrenzung

- **Change Enablement vs. Organizational Change Management**: Change Enablement = Changes an Produkten/Services; OCM = mitarbeiterbezogene Aspekte von Changes (Mensch). Wichtig: nicht vermischen.
- **Change Enablement vs. Release Management** ([[SM - ITIL Practice - Release Management]]): Change Enablement autorisiert; Release stellt bereit.
- **Change Enablement vs. Service Validation and Testing**: Validation testet vor Change-Genehmigung.
- **Begriffswandel V3 → V4**: ITIL V3 hieß diese Practice „Change Management"; ITIL 4 nennt sie „Change Control" oder „Change Enablement", um den Aspekt „Befähigung zu Changes" zu betonen — und gegen organisatorisches Change Management abzugrenzen.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist der Zweck der Change Enablement Practice? — Maximierung erfolgreicher Service-/Produkt-Änderungen durch Risikobewertung, Autorisierung und Change-Kalender-Verwaltung.

**Definition Change:** Hinzufügen, Modifizieren oder Entfernen eines Elements mit direkter oder indirekter Service-Auswirkung.

**Welche 3 Arten?** Standard, Normal, Notfall.

**Diskussionsfrage:** Worin unterscheiden sich Change Enablement und Organizational Change Management? — Change Enablement bezieht sich auf technische/Service-Änderungen; OCM auf den Mensch (Akzeptanz, Skills, Kommunikation).

**Mögliche Anschlussfragen:**
- Wer ist eine Change Autorität? Wer für Standard, Normal, Notfall?
- Wie wird der Change-Kalender genutzt — vor und nach Bereitstellung?
- Welcher Trigger initiiert einen normalen Change? — Erstellung eines Change Request.
- Wie verändert DevOps/CI-CD die Change-Logik? — *(im PDF nicht thematisiert)*

## Verwandt

- [[SM - ITIL Practice - Release Management]]
- [[SM - ITIL Practice - Service Configuration Management]]
- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL Practice - Problem Management]]
- [[SM - ITIL 4 - Service-Wertschöpfungskette]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 83–88; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
