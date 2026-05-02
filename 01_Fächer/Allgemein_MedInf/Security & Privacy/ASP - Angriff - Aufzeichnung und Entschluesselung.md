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

# ASP - Angriff - Aufzeichnung und nachträgliche Entschlüsselung

> [!info] Kurzdefinition
> Eve zeichnet verschlüsselte Kommunikation auf, kann sie zum Aufzeichnungszeitpunkt nicht lesen, kompromittiert aber später den Schlüssel und entschlüsselt im Nachhinein die gesamte gespeicherte Kommunikation.

## Beschreibung

Folie 21 beschreibt den Angriff:

- **Angriff:** Eve hat die gesamte Kommunikation zwischen Alice und Bob aufgezeichnet und kann zum Zeitpunkt der Aufzeichnung keine Informationen extrahieren (aufgrund der geschützten Nachrichten). Eve wartet jedoch auf den richtigen Moment und stiehlt den Verschlüsselungsschlüssel von Bobs Gerät. Eve kann jetzt die gesamte aufgezeichnete Kommunikation entschlüsseln.
- **Auswirkung:** Vertraulichkeit, evtl. Integrität
- **Typische Sicherheitsfunktion:** Verschlüsselung mit Perfect-Forward-Secrecy (PFS) – siehe [[ASP - Kryptografie - Perfect Forward Secrecy]].

Diese Bedrohung ist insbesondere bei langlebigen geheimen Daten (z. B. Patientendaten) relevant, weil Aufzeichnung und Entschlüsselung zeitlich auseinanderliegen können.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Angreifer-Aktion 1 | Kommunikation aufzeichnen (passiv) |
| Angreifer-Aktion 2 | Schlüssel später kompromittieren (aktiv) |
| Verletztes Schutzziel | Vertraulichkeit, evtl. Integrität |
| Schutzmechanismus | Perfect Forward Secrecy |

## Beispiel

*Im PDF nicht weiter ausgeführt.* Klassisch: TLS-Verbindung mit statischen RSA-Schlüsseln; Eve speichert Ciphertext, kompromittiert Jahre später den privaten Server-Schlüssel und kann sämtliche aufgezeichneten Sessions entschlüsseln.

## Abgrenzung

- Im Unterschied zu [[ASP - Angriff - Nachricht lesen]] braucht dieser Angriff zwei Phasen (Aufzeichnung + spätere Schlüsselkompromittierung). Das macht ihn für Angreifer mit Geduld – etwa staatliche Akteure – attraktiv („store now, decrypt later").
- PFS adressiert genau diese Lücke: Auch ein späterer Schlüssel-Diebstahl entschlüsselt nicht alte Sessions.
- Im PDF wird zusätzlich „evtl. Integrität" angegeben, ohne weitere Erklärung. Vermutlich, weil Eve mit dem entschlüsselten Material auch nachträgliche Manipulations-Belege fälschen könnte – *im PDF nicht ausgeführt*.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Beschreiben Sie das Angriffsszenario „Aufzeichnung und nachträgliche Entschlüsselung". Welche Schutzziele sind betroffen?

**Anwendungsfrage:** Welche Eigenschaft eines Kryptosystems verhindert diesen Angriff? Wie wird sie technisch realisiert?

**Diskussionsfrage:** Warum genügt es nicht, nur den aktuellen Schlüssel sicher zu halten? Warum ist „store now, decrypt later" im Kontext langlebiger Gesundheitsdaten besonders kritisch? Wie verändert die Aussicht auf Quantencomputer dieses Bedrohungsmodell? (*Quantum-Aspekt im PDF nicht behandelt.*)

**Mögliche Anschlussfragen:**
- Was ist Perfect Forward Secrecy?
- In welchen Protokollen ist PFS heute Standard? (*Im PDF nicht beantwortet.*)
- Schützt PFS auch vor Kompromittierung des langfristigen Authentifizierungs-Schlüssels?

## Verwandt

- [[ASP - Kryptografie - Perfect Forward Secrecy]]
- [[ASP - Angriff - Nachricht lesen]]
- [[ASP - Symmetrische Verschluesselung - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - Grundlagen]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 21; Übersicht auf Folie 27
