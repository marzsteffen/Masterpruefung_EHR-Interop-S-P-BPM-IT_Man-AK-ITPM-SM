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

# ITPM - Wasserfallmodell

> [!info] Kurzdefinition
> Das Wasserfallmodell ist ein klassisches Vorgehensmodell, bei dem der Projektablauf in sequentielle Phasen gegliedert ist. Die Teilergebnisse bauen aufeinander auf und führen zum vorher vollständig spezifizierten Projektergebnis. Es gilt als charakteristisch für klassisches Projektmanagement und wird oft mit diesem gleichgesetzt.

## Beschreibung

Das Wasserfallmodell ist ein **Vorgehensmodell**, bei dem der Projektablauf in **sequentielle Phasen** gegliedert ist, deren Teilergebnisse aufeinander aufbauend zum vorher **vollständig spezifizierten** Projektergebnis führen.

Die Vorlesung betont, dass das Wasserfallmodell als **charakteristisch für das traditionelle / klassische Projektmanagement** gilt und mit diesem oft sogar **gleichgesetzt** wird.

**Ursprung:**
Zurückgeführt wird das Wasserfallmodell auf die Publikation: *Royce, W. W.: Managing the Development of Large Software Systems, Proceedings of IEEE WESCON, August 1970.* Royce verwendet selbst nicht den Begriff „waterfall model", stellt sein Vorgehensmodell aber mit Grafiken dar, die intuitiv an einen Wasserfall erinnern.

## Bestandteile / Aufbau

Sequentielle Phasen, die aufeinander aufbauen. Die konkreten Phasennamen werden im PDF nicht aufgelistet – die Vorlesung beschränkt sich auf das Strukturprinzip. Siehe Sektion „Ergänzung außerhalb der Vorlesung" für eine Standard-Phasenstruktur.

## Beispiel

Vertiefendes Video laut Vorlesung: `https://youtu.be/re_MlmtOsKc`. Konkrete Anwendungsbeispiele werden im PDF nicht gegeben.

## Abgrenzung

- **Spiralmodell** (siehe [[ITPM - Spiralmodell - Boehm]]): iterativ-inkrementell, mit Risikofokus.
- **V-Modell-Vorgehensmodell** (siehe [[ITPM - V-Modell - Vorgehensmodell]]): erweitert den Wasserfall um gegenüberliegende Testphasen.
- **Agile Modelle:** Scrum, XP etc. (siehe Vorlesung „Werkzeuge 02").

Wasserfall ≠ klassisches PM, auch wenn beide oft synonym gebraucht werden – Wasserfall ist eine **konkrete Methode**, klassisches PM eine **Methodenfamilie**.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was kennzeichnet das Wasserfallmodell, und woher stammt es?

**Anwendungsfrage:** Welche Voraussetzungen müssen erfüllt sein, damit Wasserfall sinnvoll ist? (Anforderungs-/Technikklarheit, vgl. [[ITPM - Stacey Matrix - Komplexitätseinordnung]])

**Diskussionsfrage:** Royce wird oft als Erfinder des Wasserfalls dargestellt – obwohl er das Modell ursprünglich kritisch beschrieb. Diskutieren Sie diese Ironie.

**Mögliche Anschlussfragen:**
- Welche typischen Phasen enthält ein Wasserfall in der Praxis (Anforderung, Entwurf, Implementierung, Test, Inbetriebnahme)? *(im PDF nicht definiert)*
- In welchen Health-IT-Kontexten ist das Wasserfallmodell heute noch sinnvoll (regulierte Medizinproduktentwicklung)?

## Verwandt

- [[ITPM - Klassisches PM - Definition]]
- [[ITPM - Spiralmodell - Boehm]]
- [[ITPM - V-Modell - Vorgehensmodell]]
- [[ITPM - Vorgehensmodelle - Klassisch vs Agile]]

## Quelle

- Vorlesung: [[ITPM - VL - Werkzeuge 01]]
- Folien/Seitenangabe: 32

## Ergänzung außerhalb der Vorlesung

> Im PDF werden die konkreten Phasennamen nicht aufgeführt. Die folgende Phasenfolge ist die in Lehrbüchern (z. B. Tiemeyer 2018, Timinger 2017) übliche Standard-Aufteilung des Wasserfallmodells und wurde zur Lernunterstützung ergänzt – keine Inhalte aus dem PDF.

Klassische Phasenfolge nach Royce-Lesart (Standardlehrbuch):

1. **Anforderungsanalyse / Anforderungsdefinition** – Erfassen der fachlichen und technischen Anforderungen.
2. **Systemdesign / Entwurf** – Architektur- und Detailentwurf der Lösung.
3. **Implementierung / Realisierung** – Programmierung der einzelnen Komponenten.
4. **Integration und Test** – Zusammenfügen der Komponenten, Verifikation gegen die Spezifikation.
5. **Inbetriebnahme / Auslieferung** – Übergabe an den Betrieb, Schulung, Roll-out.
6. **Betrieb und Wartung** – laufender Betrieb, Fehlerbehebung, Pflege.

Zentrales Prinzip: Eine Phase wird **vollständig** abgeschlossen, bevor die nächste beginnt; Rücksprünge sind möglich, aber teuer.
