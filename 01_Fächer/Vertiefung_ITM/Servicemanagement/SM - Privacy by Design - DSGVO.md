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

# SM - Privacy by Design - DSGVO

> [!info] Kurzdefinition
> Privacy by Design verankert Datenschutz im Service-Design. Im Foliensatz werden zwei DSGVO-Komplexe behandelt: die sieben Grundsätze für die Verarbeitung personenbezogener Daten (Artikel 5 DSGVO) und die sieben Betroffenenrechte.

## Beschreibung

Folien 144–146 (Quelle: jusline.at und WKO). Privacy by Design ist im Foliensatz unter „DSGVO im Service Design" geführt — wohl als Designanforderung an Services, die personenbezogene Daten verarbeiten.

### Artikel 5 DSGVO — Grundsätze für die Verarbeitung personenbezogener Daten (Folie 145)

1. **Rechtmäßigkeit** — Verarbeitung muss auf gültiger Rechtsgrundlage basieren.
2. **Zweckbindung** — Daten dürfen nur für den festgelegten Zweck verarbeitet werden.
3. **Datenminimierung** — Es dürfen nur die für den Zweck erforderlichen Daten verarbeitet werden.
4. **Richtigkeit** — Daten müssen sachlich richtig und ggf. aktuell sein.
5. **Speicherbegrenzung** — Daten dürfen nur so lange gespeichert werden, wie für den Zweck nötig.
6. **Integrität und Vertraulichkeit** — Daten müssen vor unbefugtem Zugriff/Verlust geschützt werden.
7. **Rechenschaftspflicht** — Verantwortlicher muss Einhaltung nachweisen können.

Quelle: https://www.jusline.at/gesetz/dsgvo/paragraf/5

### Betroffenenrechte (Folie 146)

1. **Informationspflicht** — Betroffene über Verarbeitung informieren.
2. **Auskunftsrecht** — Betroffene können Auskunft über verarbeitete Daten verlangen.
3. **Recht auf Berichtigung** — Falsche Daten korrigieren lassen.
4. **Recht auf Löschung** („Recht auf Vergessenwerden") — Daten löschen lassen.
5. **Recht auf Einschränkung der Verarbeitung** — Verarbeitung beschränken lassen.
6. **Recht auf Datenübertragbarkeit** — Daten in maschinenlesbarem Format mitnehmen.
7. **Widerspruchsrecht** — Verarbeitung widersprechen.

Quelle: https://www.wko.at/service/wirtschaftsrecht-gewerberecht/EU-Datenschutz-Grundverordnung:-Betroffenenrechte.html

## Bestandteile / Aufbau

| Block | Anzahl | Inhalt |
|---|---|---|
| Grundsätze (Art. 5) | 7 | Rechtmäßigkeit, Zweckbindung, Datenminimierung, Richtigkeit, Speicherbegrenzung, Integrität und Vertraulichkeit, Rechenschaftspflicht |
| Betroffenenrechte | 7 | Informationspflicht, Auskunft, Berichtigung, Löschung, Einschränkung der Verarbeitung, Datenübertragbarkeit, Widerspruch |

## Beispiel

Krankenhaus-IT bei Einführung eines neuen Pflege-Tablets:

- **Rechtmäßigkeit:** Datenverarbeitung auf Basis Behandlungsvertrag.
- **Zweckbindung:** nur für Patientenversorgung, nicht für Marketing.
- **Datenminimierung:** Tablet zeigt nur, was die Pflegekraft für den jeweiligen Patienten braucht.
- **Richtigkeit:** Stammdaten zentral und konsistent.
- **Speicherbegrenzung:** lokaler Cache nach Schichtende leer.
- **Integrität/Vertraulichkeit:** Verschlüsselung, MFA.
- **Rechenschaftspflicht:** Audit-Log, Datenschutz-Folgenabschätzung dokumentiert.

## Abgrenzung

- **Privacy by Design vs. Compliance** (siehe [[SM - Compliance - Definition]]): Compliance ist die Einhaltung gesetzlicher und interner Regeln; Privacy by Design ist die *präventive* Verankerung von Datenschutz im Design (statt nachträglich).
- **DSGVO vs. nationale Datenschutzgesetze**: DSGVO ist EU-Recht; in Österreich ergänzt durch DSG. Inhaltlich überlagern sich die Anforderungen weitgehend.
- **Privacy by Design vs. Information Security Management**: Information Security Management adressiert technische Schutzmaßnahmen; Privacy by Design erweitert auf die Designebene mit besonderem Fokus auf personenbezogene Daten.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche sieben Grundsätze nennt Artikel 5 DSGVO? — Rechtmäßigkeit, Zweckbindung, Datenminimierung, Richtigkeit, Speicherbegrenzung, Integrität und Vertraulichkeit, Rechenschaftspflicht.

**Welche Betroffenenrechte gibt es?** — 7: Informationspflicht, Auskunft, Berichtigung, Löschung, Einschränkung, Datenübertragbarkeit, Widerspruch.

**Anwendungsfrage:** Welche Datenschutz-Anforderungen ergeben sich für eine Telemedizin-Lösung wie Omada Health (siehe [[SM - Fallbeispiel - Omada Health]])?

**Diskussionsfrage:** Was bedeutet „Privacy by Design" konkret bei der Einführung eines mobilen KIS-Zugangs? — Datensparsamkeit (nur Patienten der eigenen Station), Zweckbindung (nur Pflegezweck), Verschlüsselung, lokaler Cache mit Auto-Löschung, Audit-Log, Schulung.

**Mögliche Anschlussfragen:**
- Welche Rolle hat der Datenschutzbeauftragte?
- Welche Bezugspunkte hat Privacy by Design zur ITIL-Practice „Information Security Management"?
- Welche der Betroffenenrechte ist im Krankenhaus-Kontext am schwierigsten umzusetzen? — Recht auf Löschung kollidiert oft mit Aufbewahrungspflichten der Patientenakte.
- Cross-Fach-Bezug: Wie spielt das mit ASP zusammen ([[ASP - DSGVO - Grundsätze]])? *(geplant)*

## Verwandt

- [[SM - Compliance - Definition]]
- [[SM - PESTEL-Analyse]]
- [[SM - Fallbeispiel - Omada Health]]
- [[SM - ITIL V3 Practice - Access Management]]
- [[ASP - DSGVO - Grundsätze]] *(Cross-Fach, unresolved)*

## Quelle

- Vorlesung: [[SM - VL - IT-Servicemanagement Foliensatz WS 23 24]]
- Folien/Seitenangabe: Folien 144–146; Quellen: https://www.jusline.at/gesetz/dsgvo/paragraf/5 und https://www.wko.at/service/wirtschaftsrecht-gewerberecht/EU-Datenschutz-Grundverordnung:-Betroffenenrechte.html

## Ergänzung außerhalb der Vorlesung

*Nicht erforderlich.*
