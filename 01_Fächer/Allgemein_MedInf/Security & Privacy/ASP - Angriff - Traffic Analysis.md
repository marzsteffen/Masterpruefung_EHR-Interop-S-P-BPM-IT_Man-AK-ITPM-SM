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

# ASP - Angriff - Traffic Analysis (Indirektes Ableiten von Informationen)

> [!info] Kurzdefinition
> Eve leitet Informationen aus den Metadaten verschlüsselter Kommunikation ab (z. B. Nachrichtengröße, Frequenz, Zielgerät), ohne den Inhalt selbst zu entschlüsseln.

## Beschreibung

Folie 20 beschreibt den Angriff:

- **Angriff:** Eve hat Zugriff auf die geschützte Nachricht (Abfangen) und extrahiert *indirekt* Informationen. Beispiel aus der Folie: Eve weiß, dass ein positives COVID-19-Testergebnis aufgrund zusätzlicher Informationen im Vergleich zu einem negativen Ergebnis zu einer größeren Nachrichtengröße führt. In diesem Fall würde Eve den Inhalt der Nachricht selbst dann erkennen, wenn sie verschlüsselt ist, indem sie nur ihre Größe betrachtet (100 KB Positiv vs. 80 KB Negativ).
- **Auswirkung:** Vertraulichkeit
- **Typische Sicherheitsfunktion:** Verschlüsselung *und* Versuch, zusätzliche Informationen einzuschränken (z. B. die Größe jeder Nachricht gleich machen oder Nachrichten „glätten").

Damit zeigt die Vorlesung, dass Verschlüsselung allein für Vertraulichkeit nicht genügt, wenn Metadaten Rückschlüsse auf den Inhalt erlauben.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Angreifer-Position | Auf der Kommunikationsstrecke, beobachtet Metadaten |
| Verletztes Schutzziel | Vertraulichkeit |
| Inhalts-Zugriff | Nicht erforderlich (verschlüsselter Verkehr genügt) |
| Beispiel-Metadaten | Nachrichtengröße (im PDF), allgemein auch Timing/Frequenz |
| Gegenmaßnahmen | Verschlüsselung + Padding/Glätten der Nachrichtengröße |

## Beispiel

Aus der Folie: Positives COVID-19-Testergebnis → 100 KB. Negatives Testergebnis → 80 KB. Eve unterscheidet die Ergebnisse anhand der Größe, ohne die Verschlüsselung zu brechen.

## Abgrenzung

- **Traffic Analysis vs. [[ASP - Angriff - Nachricht lesen]]:** Letzterer braucht Klartext-Zugriff. Traffic Analysis kommt explizit *ohne* Klartext aus.
- Die Bedrohung kann nicht mit Verschlüsselung allein gelöst werden – sie erfordert zusätzliche Mechanismen auf der Protokoll-Ebene (Padding, konstante Paketgrößen, Cover Traffic).

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Traffic Analysis und welches Schutzziel wird verletzt?

**Anwendungsfrage:** Geben Sie ein eHealth-Szenario, in dem Verschlüsselung allein nicht ausreicht, weil Metadaten den Inhalt verraten.

**Diskussionsfrage:** Welche Trade-offs gehen Padding/Glätten von Nachrichten ein? (Mehr Bandbreite, höhere Latenz, schlechter komprimierbar – im PDF nicht ausgeführt.) Warum wird Traffic Analysis in der Praxis selten vollständig adressiert?

**Mögliche Anschlussfragen:**
- Welche anderen Metadaten neben der Größe können relevant sein? (Timing, Frequenz, Empfänger – im PDF nur Größe genannt.)
- Wie verhält sich Tor zu Traffic Analysis? (*Im PDF nicht behandelt.*)
- Wie hängt das mit dem DSGVO-Grundsatz Datenminimierung zusammen?

## Verwandt

- [[ASP - Angriff - Nachricht lesen]]
- [[ASP - Symmetrische Verschluesselung - Grundlagen]]
- [[ASP - Informationssicherheit - CIA-Triade]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 20; Übersicht auf Folie 27
