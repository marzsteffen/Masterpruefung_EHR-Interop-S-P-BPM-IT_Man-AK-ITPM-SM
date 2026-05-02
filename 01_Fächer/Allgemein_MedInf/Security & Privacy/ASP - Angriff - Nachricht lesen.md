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

# ASP - Angriff - Nachricht lesen

> [!info] Kurzdefinition
> Klassischer Eavesdropping-Angriff: Eve fängt eine Nachricht ab und liest sie. Schutzziel: Vertraulichkeit. Schutz: Verschlüsselung.

## Beschreibung

Aus dem Angriffskatalog der Vorlesung (Folie 19; Übersicht auf Folie 27):

- **Angriff:** Eve (Angreiferin) hat Zugriff auf die Nachricht (Abfangen) und liest sie (Vertraulichkeitsverletzung).
- **Auswirkung:** Vertraulichkeit
- **Typische Sicherheitsfunktion:** Verschlüsselung

Das ist der einfachste und namensgebende Angriff im Alice-Bob-Eve-Modell, das die Vorlesung ab Folie 18 einführt.

## Bestandteile / Aufbau

| Element | Wert (laut Folie 19) |
|---|---|
| Angreifer-Position | Auf der Kommunikationsstrecke (Abfangen) |
| Wirkrichtung | Passiv |
| Verletztes Schutzziel | Vertraulichkeit |
| Gegenmaßnahme | Verschlüsselung (symmetrisch oder asymmetrisch) |

## Beispiel

*Im PDF nicht explizit als Szenario ausgeführt.* Klassisch: HTTP-Verkehr ohne TLS in einem öffentlichen WLAN; Eve liest mit.

## Abgrenzung

- Reine Verschlüsselung schützt nur vor diesem Angriff. Sie schützt nicht vor:
  - [[ASP - Angriff - Traffic Analysis]] (Eve sieht zwar nicht den Inhalt, aber Metadaten wie Größe oder Frequenz).
  - [[ASP - Angriff - Aufzeichnung und Entschluesselung]] (Eve speichert den Ciphertext, kompromittiert später den Schlüssel).
  - [[ASP - Angriff - Modifikation Ciphertext]] (Eve ändert den Ciphertext, ohne ihn zu verstehen).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was passiert beim Angriff „Nachricht lesen", welches Schutzziel ist betroffen?

**Anwendungsfrage:** Welche Krypto-Bausteine wehren diesen Angriff ab? Reicht symmetrische Verschlüsselung aus, oder braucht es asymmetrische?

**Diskussionsfrage:** Warum schützt Verschlüsselung allein nicht gegen alle Vertraulichkeits-Bedrohungen? Beispiele für „Inhalt verschlüsselt, Information dennoch ableitbar" (Stichwort Traffic Analysis, Größe, Timing).

**Mögliche Anschlussfragen:**
- Welche Annahme an Eve trifft das Modell? (Passiv, kann nicht verändern – im PDF implizit.)
- Wie hängt dieser Angriff mit dem DSGVO-Grundsatz „Integrität und Vertraulichkeit" zusammen?

## Verwandt

- [[ASP - Angriff - Traffic Analysis]]
- [[ASP - Angriff - Aufzeichnung und Entschluesselung]]
- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Symmetrische Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folien 18, 19; Übersicht auf Folie 27
