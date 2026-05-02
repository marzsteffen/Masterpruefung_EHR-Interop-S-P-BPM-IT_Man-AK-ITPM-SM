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

# SM - EAM - Architekturebenen

> [!info] Kurzdefinition
> Enterprise Architecture Management (EAM) bedient drei Architekturebenen, die im Foliensatz abgegrenzt werden: BPM auf Geschäftsprozess-Ebene (Optimierung von Geschäftsprozessen), SOA auf Anwendungsebene (Modularisierung von Anwendungen) und ITIL auf Infrastruktur-Ebene (Strukturierung von IT-Betriebsprozessen).

## Beschreibung

Folien 151–152 schließen den Foliensatz mit einem EAM-Brückenschlag ab.

Folie 152 zeigt eine schematische Zuordnung der drei Disziplinen zu Architekturebenen:

| Ebene | Disziplin | Charakter |
|---|---|---|
| **Architekturebenen** (oberste Ebene) | **BPM** | Managementdisziplin zur Optimierung von Geschäftsprozessen |
| **Anwendungen** | **SOA** | Architekturkonzept zur Modularisierung von Anwendungen |
| **Infrastruktur** | **ITIL** | Managementdisziplin zur Strukturierung von IT-Betriebsprozessen |

Die Folie illustriert damit, dass diese drei Disziplinen jeweils auf einer eigenen Architekturebene operieren — und EAM die Klammer um alle drei darstellt. Die Kernaussage: ITIL ist *nicht* die Antwort auf alle IT-Architekturfragen — für die Geschäftsprozess-Sicht braucht es BPM, für die Anwendungs-Sicht SOA. EAM koordiniert diese Sichten.

**Cross-Fach-Verbindung:** EAM ist eigentlich ITM-AK-Thema, wird im Foliensatz nur kurz angerissen. Das Hauptmaterial steht in `EAM Überblick.pdf` und wird dort vertieft (siehe [[ITM-AK - MOC]] *(Cross-Fach-Verweis)*).

## Bestandteile / Aufbau

| Disziplin | Ebene | Adressiert |
|---|---|---|
| BPM | Architekturebenen / Geschäftsprozesse | Optimierung von Geschäftsprozessen |
| SOA | Anwendungen | Modularisierung von Anwendungen |
| ITIL | Infrastruktur | Strukturierung von IT-Betriebsprozessen |

EAM = Enterprise Architecture Management, klammert alle Ebenen.

## Beispiel

Krankenhaus-Architektur:
- **BPM:** Modellierung des Patientenaufnahmeprozesses (Aufnahme → Anamnese → …) — siehe [[BPM - MOC]] und Krankenhaus-Kernprozesse ([[SM - ITSM im Gesundheitswesen - Krankenhaus-Architektur]]).
- **SOA:** Modulare Architektur des KIS mit Services für Patientenstammdaten, Termine, Diagnosen.
- **ITIL:** Betrieb des KIS-Servers, Incident Management bei KIS-Ausfällen, SLM für KIS-Verfügbarkeit.

EAM koordiniert: Wenn ein Geschäftsprozess geändert wird (BPM), folgt eine Anpassung der Anwendung (SOA), die wiederum Auswirkungen auf den Betrieb hat (ITIL).

## Abgrenzung

- **EAM vs. BPM**: EAM ist die Klammer aller Architektursichten; BPM fokussiert auf Geschäftsprozesse als eine Sicht. EAM enthält BPM, ist aber breiter.
- **EAM vs. ITIL**: ITIL strukturiert IT-Betriebsprozesse (Infrastruktur-Ebene); EAM erweitert um Anwendungs- und Business-Ebene. ITIL ist eine *Disziplin innerhalb* der EAM-Sicht, nicht synonym.
- **SOA vs. Microservices**: SOA ist die ältere Schule (oft mit ESB); Microservices ist die moderne Variante. *Im Foliensatz nicht differenziert.*
- **EAM-Bezug zu ITIL 4**: Architecture Management ist eine General Management Practice in ITIL 4 (siehe [[SM - ITIL 4 - Management Practices Übersicht]]) — ITIL 4 erkennt also explizit die EAM-Brücke an.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Architekturebenen bedienen BPM, SOA und ITIL? — BPM: Architekturebenen / Geschäftsprozesse; SOA: Anwendungen; ITIL: Infrastruktur.

**Anwendungsfrage:** Skizzieren Sie für ein Krankenhaus die drei Ebenen mit konkreten Beispielen.

**Diskussionsfrage:** Wo sind die Schnittstellen zwischen BPM, SOA und ITIL — und wer koordiniert sie? — EAM koordiniert. Beispielhafte Schnittstelle: Geschäftsprozess-Änderung → SOA-Service-Änderung → Change Enablement (ITIL) für betriebliche Umsetzung.

**Mögliche Anschlussfragen:**
- Welche ITIL-4-Practice adressiert die Architektur explizit? — Architecture Management.
- Welche Cross-Fach-Verbindungen ergeben sich zu BPM und ITM-AK? — Siehe [[BPM - MOC]] und [[ITM-AK - MOC]].
- Warum ist EAM mehr als nur ITIL? — Weil die Geschäftsprozess- und Anwendungs-Sicht in ITIL nicht primärer Fokus sind.

## Verwandt

- [[SM - ITIL 4 - Management Practices Übersicht]] *(Architecture Management Practice)*
- [[SM - VL - EAM Überblick]] *(geplant — separater Foliensatz)*
- [[BPM - MOC]] *(Cross-Fach)*
- [[ITM-AK - MOC]] *(Cross-Fach: EAM ist ITM-AK-Domäne)*
- [[SM - ITSM im Gesundheitswesen - Krankenhaus-Architektur]]

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 151–152

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
