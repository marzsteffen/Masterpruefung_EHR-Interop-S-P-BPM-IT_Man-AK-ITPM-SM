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

# SM - ITIL 4 Grundprinzip - Iterative Weiterentwicklung mit Feedback

> [!info] Kurzdefinition
> Drittes der sieben ITIL-Grundprinzipien („Progress Iteratively with Feedback"). Selbst umfangreiche Initiativen müssen iterativ in kleinen, handhabbaren Schritten umgesetzt werden. Feedback wird vor, während und nach jeder Iteration eingeholt — Verbesserungsvorschläge können nicht im Vakuum stattfinden.

## Beschreibung

Folien 96–99 der Courseware. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

### Definition (Folie 96)

> - Widerstehen Sie der Versuchung, alles auf einmal umzusetzen. Durch die **Organisation** von Arbeiten in **kleinen Schritten**, die **zeitnah ausgeführt und abgeschlossen** werden können, wird der Fokus auf jede Anstrengung schärfer und leichter **aufeinanderfolgend oder gleichzeitig** aufrechtzuerhalten sein.
> - Jede einzelne **Iteration** sollte sowohl **handhabbar sein**, als auch bewältigt werden, um sicherzustellen, dass es **zeitnah greifbare Ergebnisse** gibt, die als **Basis** für weitere **Verbesserungen** dienen.
> - Das Gesamtprogramm sowie die dazugehörigen Iterationen müssen **fortlaufend neu bewertet** und möglicherweise überarbeitet werden, um geänderte Umstände zu berücksichtigen und sicherzustellen, dass die Wertorientierung nicht verloren gegangen ist.
> - Diese Neubewertung sollte ein **breites Spektrum von Feedback-Kanälen und -Methoden** nutzen, um sicherzustellen, dass der **Status** der Initiative und ihr Fortschritt richtig verstanden werden.

### Die Rolle des Feedbacks (Folie 97)

> „**Verbesserungsvorschläge können nicht im Vakuum stattfinden.**
> Unabhängig davon, ob ein Service, eine Gruppe von Services, eine Practice, ein Prozess, eine technische Umgebung oder ein anderes Service Management-Element verbessert werden soll: **Umstände können sich ändern** und neue Prioritäten entstehen, und die Notwendigkeit für die Iteration kann sich ändern.
> Bitten Sie **vor, während** und **nach der Iteration** um Feedback.
> Eine **Feedbackschleife** ist eine Situation, in der ein Teil des Outputs einer Aktivität als neuer Einput verwendet wird. Feedback muss in der **Wertschöpfungskette aktiv** gesammelt und verarbeitet werden, um Folgendes zu verstehen:
> - **Endanwender- und Kundenwahrnehmung** des geschaffenen Wertes
> - die **Effizienz und Effektivität** von Aktivitäten der Wertschöpfungskette
> - die Effektivität von Service-**Governance** und **Management**kontrollen
> - die **Schnittstellen** zwischen der Organisation und ihrem Netzwerk von Partnern und Lieferanten
> - die **Nachfrage** nach Produkten und Services"

### Iteration und Feedback zusammen (Folie 98)

> „**Zeitgesteuertes**, **iteratives** Arbeiten mit in den Prozess eingebetteten **Feedbackschleifen** bietet Raum für:
> - **größere Flexibilität**
> - **schnellere** Reaktion auf Kunden- und Geschäftsanforderungen
> - die **Befähigung**, Ausfälle schneller **erkennen** und darauf reagieren zu können
> - eine allgemeine **Qualitätsverbesserung**
>
> Durch angemessene Feedback-Schleifen zwischen den Teilnehmern einer Aktivität können sie besser verstehen, woher ihre Aufgaben kommen, wohin ihre Outputs gehen und wie sich ihre Aktionen und Outputs auf die Ergebnisse auswirken, wodurch sie **bessere Entscheidungen** treffen können."

### Anwenden des Prinzips (Folie 99)

Um dieses Prinzip erfolgreich anzuwenden:
- **Das große Ganze zu verstehen ist wichtig, aber Fortschritt auch. Tun Sie etwas.** Manchmal ist der Wunsch, alles verstehen und rechtfertigen zu wollen, der größte Feind iterativer Verbesserungen.
- **Das Umfeld verändert sich ständig, sodass Feedback unerlässlich ist.** Suchen Sie auf allen Ebenen und kontinuierlich nach Feedback.
- **Schnell bedeutet nicht unvollständig.** Erstellen Sie ein minimal funktionsfähiges Produkt oder eine Version, die mit wenig Aufwand ein Höchstmaß an Lernen ermöglicht.

## Bestandteile / Aufbau

| Aspekt | Inhalt |
|---|---|
| Iteration | Kleine, handhabbare Schritte, zeitnah ausgeführt |
| Aufbauen | Jede Iteration als Basis für die nächste |
| Re-Assessment | Fortlaufende Neubewertung des Gesamtprogramms |
| Feedback-Channels | Breites Spektrum, vor/während/nach Iteration |
| Feedbackschleife | Output → Input → bessere Entscheidungen |
| MVP | Minimal funktionsfähiges Produkt mit max. Lernen |

## Beispiel

Krankenhaus-IT führt Telemedizin schrittweise ein:
- **Schritt 1 (MVP):** Pilot in Kardiologie mit 5 Patienten, einfache Video-Konsultation.
- **Feedback nach 2 Wochen:** Patienten haben Login-Probleme, Ärzte wollen Schnittstelle zum KIS.
- **Schritt 2:** Login-Vereinfachung + KIS-Schnittstelle.
- **Schritt 3:** Skalierung auf weitere Fachbereiche.

Vergleich Wasserfall (verboten): Komplette Telemedizin-Plattform 12 Monate entwickeln, dann zentral ausrollen — Risiko: Anforderungen veraltet, Akzeptanz unklar.

## Abgrenzung

- **Iterativ vs. Inkrementell**: Iterativ = wiederholt verbessern; inkrementell = stückweise hinzufügen. Beide werden in modernen Vorgehensweisen kombiniert.
- **MVP vs. fertiges Produkt**: MVP ist absichtlich minimal, um schnelles Lernen zu ermöglichen.
- **Feedback vs. Audit**: Feedback ist kontinuierlich und breit; Audit ist punktuell und compliance-orientiert.
- **CSI-Verbindung** (siehe [[SM - ITIL Continual Improvement - Modell]]): Direkter Bezug zu Schritt 4 „Wie kommen wir dort hin?" — iterative Vorgehensweise ist explizit gefordert.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was bedeutet „Iterative Weiterentwicklung mit Feedback"? — Arbeit in kleinen, handhabbaren Iterationen mit kontinuierlichem Feedback.

**Anwendungsfrage (Folie 119/68 Hauptfoliensatz):** Welches Grundprinzip empfiehlt, Aufgaben in kleinere, handlichere Schritte zu unterteilen? — Antwort C: Iterative Weiterentwicklung mit Feedback.

**Diskussionsfrage:** Warum ist Feedback im Vakuum unmöglich? — Verbesserung verlangt Wissen über Wirkung; ohne Feedback agiert man im Blindflug. Krankenhaus-Beispiel: KI-Klassifizierung braucht Feedback der Service-Desk-MA, ob die Vorschläge stimmen.

**Mögliche Anschlussfragen:**
- Was sind typische Feedbackquellen? — Endanwender-/Kundenwahrnehmung, Effizienz/Effektivität der Wertschöpfungskette, Governance/Managementkontrollen, Schnittstellen zu Partnern, Nachfrage.
- Was ist eine Feedbackschleife? — Output einer Aktivität als neuer Input.
- Welche Vorteile bietet zeitgesteuertes Arbeiten mit Feedbackschleifen? — Flexibilität, schnellere Reaktion, schnellere Ausfallerkennung, allgemeine Qualitätsverbesserung.
- Wie hängt dieses Prinzip mit Agile zusammen?

## Verwandt

- [[SM - ITIL 4 - Sieben Grundprinzipien]]
- [[SM - ITIL 4 - Prinzip Interaktion und Relevanz]]
- [[SM - ITIL 4 - Vergleich Grundprinzipien vs Agile Manifest]]
- [[SM - ITIL Continual Improvement - Modell]]
- [[SM - ITIL 4 - Service-Wertschöpfungskette]]

## Quelle

- Vorlesung: [[SM - VL - ITIL 4 Grundprinzipien Detail]]
- Folien/Seitenangabe: Courseware-Folien 96–99; Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019)

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
