---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - ITIL 4 Grundprinzipien Detail]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - ITIL 4 - Vergleich Grundprinzipien vs Agile Manifest

> [!info] Kurzdefinition
> Folie 87 der Courseware stellt die vier Werte des **Agilen Manifests** den ITIL-Grundprinzipien gegenüber. Jeder Manifest-Wert lässt sich auf ein bis zwei ITIL-Grundprinzipien abbilden — was die Verträglichkeit von ITIL 4 mit agilen Vorgehensweisen unterstreicht.

## Beschreibung

Der Auszug widmet die Folien 83–87 dem Verhältnis zwischen ITIL und agilen Methoden bzw. DevOps. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

### Agile Methodik (Folie 83)
> „Die Agile-Methode ist eine Methode, die sich auf die **Bereitstellung** und **Ermittlung von Anforderungen** in **kleinen Teams** konzentriert. Es ist ein **zeitlicher**, flexibler und anpassungsfähiger Ansatz, der darauf ausgerichtet ist, **schnell** auf Changes zu reagieren. Teams organisieren sich oft selbst und es besteht ein hohes Maß an Zusammenarbeit zwischen Kunden, Anwendern und Entwicklungsteams für jede sich bietende Gelegenheit."

### ITIL und Agile in Zusammenarbeit (Folie 84)

ITIL kann Agile-Teams ergänzen durch effektivere, schnellere und stabilere Bereitstellung im Rahmen des umfassenderen Servicekonzepts und kann die laufenden Kosten des Services senken. Practices, in denen Agile von ITIL profitiert:

- Continual Improvement
- Problem Management
- Change Enablement
- Release Management
- Deployment Management

### ITIL und DevOps in Zusammenarbeit (Folie 85)

> „DevOps beruht auf dem zunehmenden Erfolg von Agile-Softwareprojekten, wodurch Organisationen häufiger Software einführen. DevOps konzentriert sich auf den Prozess der Bereitstellung von Software in Produktionsumgebungen, wobei der Schwerpunkt auf der **Abstimmung der technischen Verwaltungsarbeit und der Bereitstellung** liegt."

### Alles kommt zusammen (Folie 86)

Agile Rollen können an ITSM-Rollen ausgerichtet werden:
- **Produktmanager / -eigentümer** können die Rolle des **Service-Eigentümers** übernehmen
- **Scrum-Master** können die Rolle des **Change Managers** übernehmen
- **Scrum-Master** führen bereits **Retrospektiven** durch und sorgen für Lehren — Teil der allgemeinen Praxis der **kontinuierlichen Verbesserung**

> „ITIL und Agile können gute Freunde sein. Ein agiles Team, das sich auf die Kundenbedürfnisse und -zufriedenheit konzentriert, wird den gesamten Service in kürzerer Zeit nutzen."

### Prinzipien im Vergleich (Folie 87 — die zentrale Abbildung)

| Agile Manifest | ITIL-Grundprinzipien |
|---|---|
| Der Mensch und Interaktionen stehen über Prozessen und Werkzeugen | Auf Einfachheit und Praktikabilität achten · Dort beginnen, wo man steht |
| Eine funktionierende Software steht über einer umfassenden Dokumentation | Wertorientierung · Ganzheitlich denken und arbeiten |
| Die Mitwirkung des Kunden steht über Vertragsverhandlungen | Wertorientierung · Zusammenarbeiten und Transparenz fördern |
| Auf Veränderung zu reagieren steht über der Verfolgung eines Plans | Iterative Weiterentwicklung mit Feedback · Auf Einfachheit und Praktikabilität achten |

## Bestandteile / Aufbau

| Werte / Prinzipien | Mensch + Interaktion | Funktionierende Software | Mitwirkung Kunden | Reagieren auf Veränderung |
|---|---|---|---|---|
| Wertorientierung |  | ✓ | ✓ |  |
| Dort beginnen, wo man steht | ✓ |  |  |  |
| Iterative Weiterentwicklung mit Feedback |  |  |  | ✓ |
| Zusammenarbeiten und Transparenz fördern |  |  | ✓ |  |
| Ganzheitlich denken und arbeiten |  | ✓ |  |  |
| Auf Einfachheit und Praktikabilität achten | ✓ |  |  | ✓ |
| Optimieren und automatisieren |  |  |  |  |

Hinweis: Das siebte Prinzip (Optimieren und automatisieren) ist im Foliensatz-Vergleich nicht explizit zugeordnet — *im PDF nicht zugeordnet*.

## Beispiel

DevOps-Pipeline mit ITIL-Anbindung im Krankenhaus:
- Entwicklungsteam liefert KIS-Module agil (Sprint-basiert).
- Bereitstellung in Produktionsumgebung läuft über Change Enablement und Release Management.
- Continual Improvement nutzt Retrospektiven der Scrum-Sprints.
- Service-Eigentümer (= Product Owner) verantwortet Service-Outcomes.

## Abgrenzung

- **ITIL 4 vs. ITIL V3**: ITIL V3 wurde als zu starr für agile Vorgehen kritisiert (siehe [[SM - ITIL - Überblick]]). ITIL 4 ist explizit als Brücke zu Agile/DevOps konzipiert.
- **Agile Manifest vs. ITIL-Grundprinzipien**: Beide sind wertorientiert; ITIL ergänzt um IT-Service-spezifische Aspekte (Continual Improvement, Service Value System).
- **Agile vs. DevOps**: Agile ist Vorgehensweise (kleine Teams, Iteration); DevOps fokussiert auf Bereitstellung und Integration zwischen Dev und Ops.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Werte hat das Agile Manifest? — Mensch+Interaktion über Prozesse/Werkzeuge; funktionierende Software über Dokumentation; Kundenmitwirkung über Vertragsverhandlungen; Reaktion auf Veränderung über Plan-Verfolgung.

**Anwendungsfrage:** Ordnen Sie die Agile-Manifest-Werte den ITIL-Grundprinzipien zu (siehe Tabelle Folie 87).

**Diskussionsfrage:** Sind ITIL und Agile wirklich kompatibel — oder ist die Vereinbarung in der Praxis schwierig? — Argumentationsraum: ITIL bringt Stabilität (Change Enablement, SLAs); Agile bringt Geschwindigkeit. Bei richtiger Aufteilung (DevOps-Pipeline mit ITIL-Gates) komplementär; bei rein zeremonieller ITIL-Umsetzung Spannung.

**Mögliche Anschlussfragen:**
- In welchen Practices profitiert Agile besonders von ITIL? — Continual Improvement, Problem Management, Change Enablement, Release Management, Deployment Management.
- Welche Agile-Rollen finden ihre ITSM-Entsprechung? — Product Owner ↔ Service Owner; Scrum Master ↔ Change Manager / kontinuierliche Verbesserung.
- Was ist DevOps-Schwerpunkt? — Abstimmung zwischen technischer Verwaltung und Bereitstellung.

## Verwandt

- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 - Prinzip Interaktion und Relevanz]]
- [[SM - ITIL - Überblick]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - ITIL Practice - Change Enablement]]
- [[SM - ITIL Practice - Release Management]]
- [[SM - Fallstudie - KI Incident Management]]

## Quelle

- Vorlesung: [[SM - VL - ITIL 4 Grundprinzipien Detail]]
- Folien/Seitenangabe: Courseware-Folien 83–87; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
