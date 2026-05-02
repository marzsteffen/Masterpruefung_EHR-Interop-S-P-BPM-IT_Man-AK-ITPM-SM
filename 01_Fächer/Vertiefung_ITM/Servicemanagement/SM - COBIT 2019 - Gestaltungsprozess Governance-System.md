---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - COBIT 2019 Termin 14]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - COBIT 2019 - Gestaltungsprozess Governance-System

> [!info] Kurzdefinition
> Vier-Phasen-Methode aus dem COBIT 2019 Design Guide zur Erstellung eines auf das Unternehmen zugeschnittenen IT-Governance-Systems: 1. Verstehen des Unternehmenskontexts und der Unternehmensstrategie → 2. Bestimmen des anfänglichen Umfangs des Governance-Systems → 3. Weiterentwickeln des Umfangs → 4. Fertigstellen des Designs.

## Beschreibung

Folie 9 zeigt den Gestaltungsprozess als Pfeilkette mit vier Phasen und je 4–7 Aufgaben. Quelle: ISACA (2019) Cobit 2019 Rahmenwerk.

## Bestandteile / Aufbau

| Phase | Aufgaben (Folie 9) |
|---|---|
| **1. Verstehen des Unternehmenskontexts und der Unternehmensstrategie** | • Unternehmensstrategie verstehen<br>• Unternehmensziele verstehen<br>• Risikoprofil verstehen<br>• Aktuelle I&T-bezogene Probleme verstehen |
| **2. Bestimmen des anfänglichen Umfangs des Governance-Systems** | • Unternehmensstrategie berücksichtigen<br>• Unternehmensziele berücksichtigen und **COBIT-Zielkaskade anwenden**<br>• Risikoprofil des Unternehmens berücksichtigen<br>• Aktuelle I&T-bezogene Probleme berücksichtigen |
| **3. Weiterentwickeln des Umfangs des Governance-Systems** | • Bedrohungslandschaft berücksichtigen<br>• Compliance-Anforderungen berücksichtigen<br>• Rolle der IT berücksichtigen<br>• Sourcing-Modell berücksichtigen<br>• IT-Implementierungsmethoden berücksichtigen<br>• IT-Übernahmestrategie berücksichtigen<br>• Unternehmensgröße berücksichtigen |
| **4. Fertigstellen des Designs des Governance-Systems** | • Inhärente Prioritätskonflikte lösen<br>• Design des Governance-Systems fertigstellen |

Die Aufgaben in Phase 2 und 3 nehmen exakt die **Designfaktoren** aus [[SM - COBIT 2019 - Designfaktoren]] auf — Phase 2 nutzt die fünf Faktoren der ersten Reihe, Phase 3 die sechs Faktoren der zweiten Reihe (Folie 6). Damit wird das Designfaktoren-Modell prozessual operationalisiert.

## Beispiel

*Im Foliensatz nicht ausgearbeitet.* Krankenhaus-Anwendung:

1. **Phase 1 Verstehen:** Strategie „digitales Krankenhaus 2030"; Ziele Versorgungsqualität + Wirtschaftlichkeit; Risikoprofil hoch (Patientensicherheit); aktuelle Probleme: KIS-Performance, Personalengpass.
2. **Phase 2 Anfänglicher Umfang:** Strategie + Ziele über Zielkaskade auf IT-Ziele heruntergebrochen; Risikoprofil prägt Schwerpunkte (Verfügbarkeit, Sicherheit); Probleme priorisiert.
3. **Phase 3 Weiterentwickeln:** Cyber-Bedrohungslage berücksichtigen; DSGVO + ELGA-Gesetz als Compliance-Vorgaben; Rolle der IT als strategisch; Sourcing-Mix; Implementierungsmethoden hybrid; Übernahmestrategie konservativ; Größe (mittel).
4. **Phase 4 Fertigstellen:** Konflikt „schnelle Innovation vs. Stabilität" auflösen; Governance-System dokumentieren.

## Abgrenzung

- **Gestaltungsprozess vs. ITIL-CSI-Modell** (siehe [[SM - ITIL Continual Improvement - Modell]]): Beide sind methodische Prozesse mit ähnlicher Logik (Verstehen → Soll bestimmen → Plan → Umsetzung). CSI ist ITSM-spezifisch und iterativ-zyklisch; COBIT-Gestaltungsprozess ist Governance-System-spezifisch und einmalig (Design), wird aber durch Reviews periodisch erneuert.
- **Gestaltungsprozess vs. IT-Strategie 7 Schritte** (siehe [[SM - IT-Strategie - 7 Schritte nach Johanning]]): IT-Strategie-7-Schritte erstellt eine *IT-Strategie*; COBIT-Gestaltungsprozess erstellt ein *IT-Governance-System*. Beide haben Schnittpunkte (Phase 1+2 ↔ Schritt 1+2; Phase 3 ↔ Schritte 3–5).
- **Gestaltungsprozess vs. CMMI-Bewertung** (siehe [[SM - COBIT 2019 - Fähigkeitsstufen]]): Gestaltungsprozess plant das Soll-System; Fähigkeitsstufen bewerten den Reifegrad.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Phasen hat der COBIT-Gestaltungsprozess? — 1. Unternehmenskontext verstehen → 2. Anfänglicher Umfang → 3. Weiterentwickeln → 4. Fertigstellen.

**Anwendungsfrage:** Skizzieren Sie für ein Krankenhaus die vier Phasen mit konkreten Inhalten.

**Diskussionsfrage:** Welche Beziehung besteht zwischen den 11 Designfaktoren und dem Gestaltungsprozess? — Designfaktoren sind die *Inputs* des Gestaltungsprozesses; Phase 1+2 verarbeiten die ersten 5 Faktoren, Phase 3 die übrigen 6. Phase 4 löst die Konflikte zwischen den Anforderungen, die aus den Designfaktoren entstehen.

**Mögliche Anschlussfragen:**
- Was sind „inhärente Prioritätskonflikte" in Phase 4? — Konflikte zwischen widersprüchlichen Anforderungen aus den Designfaktoren (z. B. Innovation vs. Stabilität).
- Wie kommt die Zielkaskade in den Gestaltungsprozess? — Explizit in Phase 2 als Werkzeug zur Verarbeitung der Unternehmensziele.
- Wie hängt der Gestaltungsprozess mit COBIT-Implementierungsguide zusammen? *(im PDF nicht ausgeführt)*

## Verwandt

- [[SM - Standard - COBIT 2019 Framework]]
- [[SM - COBIT 2019 - Komponenten IT-Governance-System]]
- [[SM - COBIT 2019 - Designfaktoren]]
- [[SM - COBIT 2019 - Zielkaskade]]
- [[SM - COBIT 2019 - Fähigkeitsstufen]]
- [[SM - IT-Strategie - 7 Schritte nach Johanning]]
- [[SM - ITIL Continual Improvement - Modell]]

## Quelle

- Vorlesung: [[SM - VL - COBIT 2019 Termin 14]]
- Folien/Seitenangabe: Folie 9; Quelle: ISACA (2019) Cobit 2019 Rahmenwerk

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
