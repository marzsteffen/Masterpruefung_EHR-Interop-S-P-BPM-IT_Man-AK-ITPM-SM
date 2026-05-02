---
fach: itpm
typ: konzept
status: offen
quelle: "[[ITPM - VL - Werkzeuge 01]]"
tags:
  - fach/vertiefung/itpm
  - typ/konzept
  - status/offen
---

# ITPM - V-Modell - Vorgehensmodell

> [!info] Kurzdefinition
> Das V-Modell (als Vorgehensmodell) ist ein klassisches Softwareentwicklungsmodell, das den Entwicklungsprozess analog zum Wasserfallmodell in Phasen organisiert und zusätzlich jeder Entwicklungsphase eine korrespondierende Testphase gegenüberstellt. Die V-förmige Anordnung gibt dem Modell seinen Namen. Vorgeschlagen 1979 von Barry Boehm.

## Beschreibung

Das V-Modell ist ein Vorgehensmodell, das ursprünglich für die **Softwareentwicklung** konzipiert wurde. Ähnlich dem Wasserfallmodell organisiert es den Softwareentwicklungsprozess in **Phasen**.

Zusätzlich zu diesen Entwicklungsphasen definiert das V-Modell auch das Vorgehen zur **Qualitätssicherung (Testen)**: Den einzelnen Entwicklungsphasen werden **Testphasen gegenübergestellt**.

**Ursprung:**
Vorgeschlagen wurde dieses Vorgehen zuerst vom US-amerikanischen Softwareingenieur **Barry Boehm** im Jahr **1979**.

Das allgemeine V-Modell ist die **Grundlage** von Entwicklungsstandards wie z. B. dem **V-Modell (Entwicklungsstandard) der öffentlichen Hand** in Deutschland (siehe [[ITPM - V-Modell - Entwicklungsstandard]]).

> ⚠️ **Wichtig:** Nicht zu verwechseln mit dem **V-Modell als deutscher Entwicklungsstandard** (siehe [[ITPM - V-Modell - Entwicklungsstandard]]). Die Vorlesung warnt explizit vor dieser Verwechslung.

## Bestandteile / Aufbau

Phasenstruktur (Folie 36):

- **Linker, nach unten führender Ast:** Spezifizierungsphasen, schließt mit der **Realisierungsphase** ab.
- **Rechter, nach oben führender Ast:** **Testphasen**, die zeitlich nachfolgen.
- **Kernprinzip:** Die Phasenergebnisse sind **bindende Vorgaben** für die nächsttiefere Projektphase. Den spezifizierenden Phasen stehen jeweils **testende Phasen** gegenüber – das ergibt das charakteristische **„V"**.

Konkrete Phasennamen werden im PDF nicht aufgelistet. Siehe Sektion „Ergänzung außerhalb der Vorlesung" für die Standard-Phasenpaare.

## Beispiel

Vertiefendes Video laut Vorlesung: `https://youtu.be/P0TgRjj8hQg`. Konkrete Anwendungsbeispiele werden im PDF nicht gegeben.

## Abgrenzung

- **Wasserfallmodell:** linear ohne explizite Testphasen-Korrespondenz.
- **V-Modell (Entwicklungsstandard):** ist die institutionelle, vorschriftsbasierte Variante (deutscher Bundesstandard, IABG, BMI, BMVg). Das **V-Modell als Vorgehensmodell** ist die zugrunde liegende generische Idee.
- **Spiralmodell:** iterativ statt linear.

Die Verwechslungsgefahr V-Modell-Standard ↔ V-Modell-Vorgehensmodell wird in der Vorlesung explizit hervorgehoben.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie unterscheidet sich das V-Modell vom Wasserfallmodell? Was bringt der „rechte Ast"?

**Anwendungsfrage:** In welchen regulierten Health-IT-Kontexten ist das V-Modell besonders nützlich (Medizinproduktentwicklung, Validierung)?

**Diskussionsfrage:** Erklären Sie den Unterschied V-Modell als Vorgehensmodell vs. V-Modell als deutscher Entwicklungsstandard. Warum trägt beides denselben Namen?

**Mögliche Anschlussfragen:**
- Welche typischen Phasenpaare kennt das V-Modell (z. B. Komponententest ↔ Detailentwurf, Systemtest ↔ Systementwurf)? *(im PDF nicht definiert)*
- Welche Schwächen hat das V-Modell gegenüber agilen Modellen?

## Verwandt

- [[ITPM - V-Modell - Entwicklungsstandard]]
- [[ITPM - Wasserfallmodell]]
- [[ITPM - Spiralmodell - Boehm]]
- [[ITPM - Klassisches PM - Definition]]
- [[ITPM - Vorgehensmodelle - Klassisch vs Agile]]

## Quelle

- Vorlesung: [[ITPM - VL - Werkzeuge 01]]
- Folien/Seitenangabe: 35–36

## Ergänzung außerhalb der Vorlesung

> Im PDF werden die konkreten Phasenpaare nicht aufgeführt. Die folgende Aufteilung ist die in Lehrbüchern (Boehm 1979, Tiemeyer 2018) übliche Standard-Variante des allgemeinen V-Modells und wurde zur Lernunterstützung ergänzt – keine Inhalte aus dem PDF.

Standard-Phasenpaare des allgemeinen V-Modells:

| Linker Ast (Spezifikation) | ↔ | Rechter Ast (Test) |
|---|---|---|
| Anforderungsanalyse / Lastenheft | ↔ | **Abnahmetest** (gegen Anforderungen) |
| Funktionaler Systementwurf | ↔ | **Systemtest** (gegen funktionalen Entwurf) |
| Technischer Systementwurf / Architektur | ↔ | **Integrationstest** (gegen Architektur) |
| Komponentenspezifikation / Detailentwurf | ↔ | **Komponententest / Modultest** (gegen Detailentwurf) |
| **Programmierung / Implementierung** (Spitze des V) | | |

Kernidee: Jede Spezifikationsstufe definiert die Akzeptanzkriterien für die ihr **gegenüberliegende Teststufe**. Damit wird Qualitätssicherung von Anfang an mitgeplant – nicht nachträglich.
