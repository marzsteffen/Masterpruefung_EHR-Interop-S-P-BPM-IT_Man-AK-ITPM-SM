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

# ASP - Risikomanagement - Kontextbestimmung

> [!info] Kurzdefinition
> Erster Schritt im ISO-27005-Prozess: Festlegung des Geltungsbereichs (organisatorisch/physisch/technisch), Klärung der Rollen (Risikomanager, Risiko-Eigner) und Definition der Bewertungsskalen für Eintrittswahrscheinlichkeit und Schadenshöhe.

## Beschreibung

Folien 9–11 listen die Aktivitäten der Kontextbestimmung.

### Festlegung des Geltungsbereichs (Scope, Folie 9)
Definition, welche Teile der Organisation unter das Risikomanagement fallen:
- **Organisatorisch:** Bereiche, Abteilungen.
- **Physisch:** Standorte, Gebäude.
- **Technisch:** Systeme, technische Einrichtungen.

### Organisatorische Überlegungen (Folie 9)
Festlegung der Rollen:
- **Risikomanager:** verantwortlich für das Risikomanagement.
- **Risiko-Eigner:** trägt die Risiken als Letztverantwortlicher (oft Abteilungsleitung oder Geschäftsführung).

### Bewertungsskala für die Eintrittswahrscheinlichkeit (Folie 10)

| Stufe | Bezeichnung | Beschreibung Eintrittswahrscheinlichkeit (ETW) |
|---|---|---|
| 4 | sehr hoch | Eintritt sehr wahrscheinlich |
| 3 | hoch | Eintritt wahrscheinlich |
| 2 | mittel | Eintritt eher wahrscheinlich |
| 1 | gering | Eintritt eher unwahrscheinlich |

### Alternativ: Eintrittshäufigkeit (Folie 10)

| Stufe | Bezeichnung | Beschreibung Eintrittshäufigkeit |
|---|---|---|
| 4 | Sehr häufig | öfter als 1× jährlich |
| 3 | Häufig | 1× in 1–5 Jahren |
| 2 | Mittel | 1× in 5–15 Jahren |
| 1 | selten | weniger als 1× in 15 Jahren |

### Schadensklassen (Folie 11)

Definition der Schadensszenarien und ihrer Stufen (1=gering bis 4=sehr hoch). Die Vorlesung listet drei Schadensszenarien als Übung:
- Beeinträchtigung der körperlichen Unversehrtheit.
- Imageschaden / Reputationsverlust.
- Finanzieller Schaden.

(Das Untragbarkeitsniveau wird durch die Institutionsleitung definiert, analog zur BIA – siehe [[ASP - BCM - Business Impact Analyse]].)

## Bestandteile / Aufbau

| Bestandteil | Inhalt | Wer entscheidet |
|---|---|---|
| Geltungsbereich | organisatorisch, physisch, technisch | Geschäftsführung |
| Rollen | Risikomanager, Risiko-Eigner | Geschäftsführung |
| ETW-Skala | 4 Stufen oder Häufigkeitswerte | RiskMgmt + Leitung |
| Schadensskala | 4 Stufen pro Schadensszenario | RiskMgmt + Leitung |

## Beispiel

Krankenhaus: Geltungsbereich umfasst alle IT-Systeme der Notaufnahme und Intensivstation. Risikomanager ist der CISO, Risiko-Eigner sind die jeweiligen Abteilungsleitungen. ETW-Skala 1–4 nach Häufigkeit (selten bis sehr häufig). Schadensskala für „Beeinträchtigung der körperlichen Unversehrtheit": 1 = vorübergehend leicht beeinträchtigt, 4 = irreversibler Schaden / Tod.

## Abgrenzung

- **Geltungsbereich ≠ BIA-Geltungsbereich:** Sehr ähnlich (siehe [[ASP - BCM - Business Impact Analyse]]), aber RiskMgmt deckt mehr ab als nur zeitkritische Prozesse.
- **Eintrittswahrscheinlichkeit vs. Eintrittshäufigkeit:** ETW ist abstrakt-qualitativ; Häufigkeit ist quantitativer (Anzahl pro Zeitraum). In der Praxis werden beide genutzt.
- **Risikomanager ≠ Risiko-Eigner:** Der Manager organisiert den Prozess; der Eigner trägt die Konsequenzen und die Entscheidung über Risikobehandlung.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Aktivitäten fallen in die Kontextbestimmung?

**Anwendungsfrage:** Welche Bewertungsskala bevorzugen Sie für ein eHealth-System – ETW oder Eintrittshäufigkeit – und warum?

**Diskussionsfrage:** Welche Skalierung (3-stufig vs. 4-stufig) hat welche Vor- und Nachteile? (Siehe auch [[ASP - Risikomanagement - Risikomatrix]].) Wer muss das Untragbarkeitsniveau festlegen, und warum nicht der Risikomanager allein?

**Mögliche Anschlussfragen:**
- Was passiert, wenn Geltungsbereich zu eng / zu weit gewählt wird?
- Wie unterscheiden sich Risiko-Eigner und Risikomanager?
- Wie wird der Kontext bei wachsendem Unternehmen angepasst? (Im PDF nicht ausgeführt.)

## Verwandt

- [[ASP - Risikomanagement - Risikomatrix]]
- [[ASP - Risikomanagement - Risikoklassen und Akzeptanz]]
- [[ASP - Risikomanagement - Big Picture]]
- [[ASP - BCM - Business Impact Analyse]]

## Quelle

- Vorlesung: [[ASP - VL - Informationssicherheits-Risikomanagement]]
- Folien/Seitenangabe: Folien 9, 10, 11
