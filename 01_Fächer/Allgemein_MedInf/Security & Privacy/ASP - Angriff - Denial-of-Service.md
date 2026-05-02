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

# ASP - Angriff - Nachricht unterdrücken (Denial-of-Service)

> [!info] Kurzdefinition
> Eve unterdrückt einige oder alle Nachrichten zwischen Sender und Empfänger (Denial-of-Service-Charakter). Schutzziel: Verfügbarkeit. Schutz: vollständig protokollabhängig, in vielen Fällen schwer zu mitigieren.

## Beschreibung

Folie 26 beschreibt den Angriff:

- **Angriff:** Eve unterdrückt einige/alle Nachrichten. Beispiel laut Folie: Denial-of-Service-Attack.
- **Auswirkung:** Verfügbarkeit. Beispiel auf der Folie – selbstfahrendes Auto: Alice ist ein Bremspedal und Bob ist die Bremse. Unterdrücken der Information „Jetzt bremsen" führt dazu, dass die Bremse nicht funktioniert.
- **Typische Sicherheitsfunktion:** Vollständig protokollabhängig, in vielen Fällen schwer abzuschwächen.

Damit ist dies der einzige Angriff im Katalog, der primär das Schutzziel Verfügbarkeit angreift.

## Bestandteile / Aufbau

| Element | Inhalt |
|---|---|
| Angreifer-Aktion | Nachrichten blockieren oder verzögern |
| Verletztes Schutzziel | Verfügbarkeit |
| Realisierung | DoS-Attacke (z. B. Netzwerk-Flooding) |
| Schutzmechanismus | Protokollabhängig; oft schwer zu mitigieren |

## Beispiel

Aus Folie 26: Selbstfahrendes Auto, Alice = Bremspedal, Bob = Bremse. Wird das Signal „jetzt bremsen" unterdrückt, funktioniert die Bremse nicht.

## Abgrenzung

- Im Unterschied zu allen anderen Angriffen aus diesem Katalog adressiert Suppression nicht primär Vertraulichkeit oder Integrität – sondern die schiere Erreichbarkeit.
- Kryptografische Schutzmechanismen (Verschlüsselung, HMAC, Signatur) helfen hier **nicht**: Eve muss die Nachricht nicht verstehen, um sie zu blockieren.
- Schutzmaßnahmen liegen typischerweise auf einer ganz anderen Ebene: Redundanz, Heartbeats, Watchdogs, alternative Kommunikationswege, DDoS-Schutz auf Netzwerkebene. *Im PDF nicht ausgeführt.*

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet „Nachricht unterdrücken" als Angriff, welches Schutzziel ist betroffen?

**Anwendungsfrage:** Welche Klasse von Schutzmaßnahmen wirkt gegen DoS – im Gegensatz zu kryptografischen Schutzmaßnahmen?

**Diskussionsfrage:** Warum ist DoS bei sicherheitskritischen oder lebenskritischen Systemen (z. B. eHealth, autonome Fahrzeuge) besonders schwerwiegend? Wie verschiebt das den Risikoschwerpunkt vom „klassischen" Vertraulichkeitsdenken hin zur Verfügbarkeit?

**Mögliche Anschlussfragen:**
- Wie hängt dieser Angriff mit Business Continuity Management zusammen? (siehe [[ASP - VL - Business Continuity Management]] – folgt.)
- Welche Mechanismen detektieren ausgefallene Nachrichten in einem Protokoll? (Heartbeats, Sequenznummern – im PDF nicht ausgeführt.)
- Welcher Unterschied besteht zwischen DoS und DDoS? (*Im PDF nicht behandelt.*)

## Verwandt

- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - VL - Business Continuity Management]]
- [[ASP - Security Eigenschaften - Reliability]]

## Quelle

- Vorlesung: [[ASP - VL - Einfuehrung und Motivation]]
- Folien/Seitenangabe: Folie 26; Übersicht auf Folie 27
