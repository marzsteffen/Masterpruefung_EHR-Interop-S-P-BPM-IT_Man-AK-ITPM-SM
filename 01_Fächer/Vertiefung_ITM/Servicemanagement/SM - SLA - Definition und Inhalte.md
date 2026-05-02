---
fach: sm
typ: konzept
status: offen
quelle: "[[SM - VL - ITSM Einführung Text]]"
tags:
  - fach/vertiefung/sm
  - typ/konzept
  - status/offen
---

# SM - SLA - Definition und Inhalte

> [!info] Kurzdefinition
> Ein Service-Level-Agreement (SLA) ist die schriftliche Festlegung der für einen Service erwarteten und zugesicherten Service-Levels. SLAs können Standard-SLAs sein (vom Anbieter festgelegt) oder individuell zwischen Anbieter und Nutzer ausgehandelt werden.

## Beschreibung

Allweyer beschreibt SLAs als das Dokument, in dem Utility und vor allem Warranty (siehe [[SM - Service-Level - Utility vs Warranty]]) verbindlich festgehalten werden. Es kann sich um Standard-SLAs handeln, die vom Anbieter festgelegt werden, oder um individuell zwischen Anbieter und Nutzern ausgehandelte SLAs.

Standard-SLAs enthalten zum Teil mehrere Service-Levels mit unterschiedlichen Preisen. Die Kunden können dann jeweils benötigte Service-Levels auswählen — Allweyer nennt das Beispiel Standard-Support vs. Premium-Support mit deutlich kürzeren Reaktions- und Störungsbehebungszeiten.

**Verfügbarkeit** ist der prominenteste SLA-Inhalt. Sie wird meist als Prozentsatz innerhalb eines bestimmten Zeitraums angegeben — z. B. 99,5 % monatliche Verfügbarkeit. Wichtig laut Allweyer: Es geht nicht um die Verfügbarkeit einzelner Komponenten wie Server oder Netzwerk, sondern um die vollständige Verfügbarkeit des kompletten Service beim Nutzer.

Der Service-Anbieter kann die Verfügbarkeit nur insoweit garantieren, als die betreffenden Komponenten in seinem Verantwortungsbereich liegen. Werden Services eines externen Anbieters über das Internet genutzt, kann er lediglich sicherstellen, dass im Internet auf seine Anwendungen zugegriffen werden kann — nicht aber, ob die Internet-Anbindung des Kunden funktioniert. Anders bei einer internen IT-Abteilung, die sowohl die Anwendung als auch die Netzwerkanbindung des Arbeitsplatzes verantwortet — hier kann im SLA die tatsächliche Verfügbarkeit am Arbeitsplatz festgelegt werden.

Weitere SLA-Inhalte laut Allweyer:
- **Zuverlässigkeit:** wie oft und wie lange der Service maximal ausfallen darf.
- **Performance:** bei Softwareanwendungen in der Regel maximale Antwortzeiten.
- **Kontinuität:** wie der Service auch in einem Katastrophenfall bereitgestellt bzw. wiederhergestellt wird.
- **Sicherheit:** spezielle Maßnahmen, z. B. hinsichtlich Authentifizierung, Berechtigungen oder Verschlüsselung.
- **Reporting:** wie die Einhaltung der vereinbarten Service-Levels überprüft und berichtet wird. Hat der Nutzer etwa den Eindruck, ein Service sei zu häufig ausgefallen, ist es wichtig, dass die Verfügbarkeit nach einem gemeinsam festgelegten Verfahren gemessen wird. Sonst lässt sich nicht feststellen, ob der vereinbarte Service-Level tatsächlich unterschritten wurde. Zudem können Strafen für Nichteinhaltung vereinbart werden — z. B. Kürzungen bei den Zahlungen.

Allweyer betont: Die obige Gliederung gibt nur einen groben Anhaltspunkt. Sie kann je nach Art des Service variieren. Für eine Dienstleistung wie die Installation eines Arbeitsplatzcomputers ist die Angabe der Verfügbarkeit nicht sinnvoll — nützlicher ist hier die maximale Dauer von der Beauftragung bis zur vollständig abgeschlossenen Installation.

## Bestandteile / Aufbau

Typische Inhalte eines SLA laut [BeZi15] (zitiert bei Allweyer):

- Vertragspartner und Unterschriften
- Beschreibung des Service
- Servicezeiten
- Serviceverfügbarkeit
- Zuverlässigkeit
- Support
- Performance
- Kontinuität
- Sicherheit
- Rollen und Verantwortlichkeiten
- Preise und Verrechnungsmethoden
- Reporting

## Beispiel

99,5 % monatliche Verfügbarkeit als Service-Level — meist gemessen als vollständige Verfügbarkeit des kompletten Service beim Nutzer, nicht als Verfügbarkeit einzelner Komponenten. Bei Nichteinhaltung können Strafen wie Kürzungen bei Zahlungen vereinbart werden.

## Abgrenzung

- **SLA vs. OLA / UC:** Allweyer nennt OLAs (Operational Level Agreements) und UCs (Underpinning Contracts) hier nicht explizit — *im PDF nicht definiert*. Erwartet im Foliensatz / im ITIL-Kursbuch.
- **SLA vs. Service-Level:** Service-Level ist die einzelne Qualitätszusage, SLA ist das Vertragsdokument.
- **Standard-SLA vs. individueller SLA:** Standard-SLAs werden vom Anbieter vorgegeben (ggf. mehrstufig); individuelle SLAs werden ausgehandelt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist ein SLA? — Schriftliche Festlegung der erwarteten/zugesicherten Service-Levels, zwischen Anbieter und Kunde.

**Anwendungsfrage:** Welche typischen Inhalte hat ein SLA? — 12 Punkte nach [BeZi15] (siehe oben). Besser noch: erklären, warum Reporting und Verantwortungsbereich kritische Inhalte sind.

**Diskussionsfrage:** Wer ist verantwortlich, wenn ein Service nicht verfügbar ist, weil die Internet-Anbindung des Kunden ausfällt? — Antwort: Liegt nicht im Verantwortungsbereich des Anbieters, daher nicht durch SLA gedeckt; Konsequenz für die Definition der Verfügbarkeitskenngröße. Bei einer internen IT-Abteilung kann die Verantwortung auch das Netzwerk umfassen — dann andere Verfügbarkeitsdefinition.

**Mögliche Anschlussfragen:**
- Warum reicht „99,9 % Verfügbarkeit" als Aussage nicht aus? (Antwort: Verantwortungsbereich, Messverfahren, Bezugszeitraum, Service-Level vs. Komponenten-Verfügbarkeit.)
- Welche SLA-Inhalte sind für eine einmalige Dienstleistung (z. B. Hardware-Installation) sinnvoll, welche nicht?
- Wie unterscheiden sich Standard-SLAs und ausgehandelte SLAs in einer Krankenhaus-IT?

## Verwandt

- [[SM - Service-Level - Utility vs Warranty]]
- [[SM - IT-Service - Definition]]
- [[SM - Service-Katalog - Definition und Aufbau]]
- [[SM - SLA - vs OLA vs UC]]
- [[SM - SLA - Verfügbarkeit]]

## Quelle

- Vorlesung: [[SM - VL - ITSM Einführung Text]]
- Folien/Seitenangabe: Buchseite 130–131 (Allweyer, Kap. 8.2); Quellenverweis [BeZi15]

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
