---
fach: sm
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/sm
---

# SM - PF - Service Level Management

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Karten zur Service Level Management Practice (ITIL 4, Folien 101–102) sowie zu SLA-Inhalten, Utility/Warranty-Konzept und Abgrenzungen (Quelle: ITIL 4 Foundation Courseware Axelos/Van Haren 2019 sowie Allweyer, Kap. 8.2). Relevant für SM (Servicemanagement, FH JOANNEUM eHealth).

## Verlinkte Konzepte

- [[SM - ITIL Practice - Service Level Management]]
- [[SM - SLA - Definition und Inhalte]]
- [[SM - Service-Level - Utility vs Warranty]]
- [[SM - IT-Service-Katalog - Sichten und Strukturierung]]
- [[SM - ITIL Practice - Service Request Management]]
- [[SM - 5 Phasen - serviceorientierte IT-Organisation]]

---

## Karten

### Definition

Was ist der Zweck der Service Level Management Practice, und wie definiert ITIL 4 ein SLA?

?

**Zweck (Folie 101):**
> „Das Festlegen klarer geschäftsbezogener Ziele für Service Levels und das Sicherstellen, dass die Erbringung eines Service anhand dieser Ziele entsprechend bewertet, überwacht und gemanagt wird."

**Definition SLA (Folie 101):**
> „Eine dokumentierte Vereinbarung zwischen einem Service Provider und einem Kunden, die sowohl die benötigten Services als auch den erwarteten Service Level identifiziert."

**Merkhilfe:** SLM = Festlegen + Bewerten + Überwachen + Managen von Service Levels. SLA = das Vertragsdokument, das diese Levels schriftlich fixiert.

---

Welche vier Anforderungen stellt ITIL 4 an gute SLAs?

?

**Vier Anforderungen (Folie 102):**

1. **Bezug auf einen Servicekatalog-Service:** SLAs müssen sich auf einen definierten Service im Servicekatalog beziehen — sonst sind es nur Messgrößen ohne Zweck und ohne echte Transparenz.

2. **Outcome-Bezug statt reiner Messgrößen:** SLAs sollen sich auf definierte Ergebnisse beziehen, nicht nur auf betriebliche Kennzahlen. Erreicht durch einen **ausgewogenen Satz von Messgrößen**, z. B. Kundenzufriedenheit.

3. **Vereinbarungs-Charakter:** Ein SLA muss eine echte Vereinbarung sein — Interaktion und Diskussion zwischen Provider und Konsumenten. Alle Stakeholder einbeziehen: Partner, Sponsoren, Anwender und Kunden.

4. **Verständlichkeit:** Einfach geschrieben, für alle Parteien leicht zu verstehen und umzusetzen.

---

Was bedeuten Utility und Warranty — und wie hängen beide mit SLAs zusammen?

?

**Utility (Nutzen):**
> Die bereitgestellte Funktionalität — das, *was* ein Service tut.
> Beispiel: „Pflegekräfte können im KIS Patientendaten abrufen und dokumentieren."

**Warranty (Gewähr):**
> Die Zusicherung, dass der Service den vereinbarten Anforderungen entspricht — das, *wie* der Kunde den Nutzen geliefert bekommt. Diese qualitätsbezogenen Anforderungen werden als **Service-Levels** bezeichnet.
> Aspekte: Verfügbarkeit, Zuverlässigkeit, Performance, Sicherheit, Kontinuität.

**Verhältnis zu SLAs:**
- Utility wird im Servicekatalog beschrieben (Was wird erbracht?)
- Warranty wird im SLA operationalisiert (Wie verlässlich? — Verfügbarkeit, Antwortzeiten, …)
- Ein Service mit voller Utility, aber ohne Warranty-Zusicherung liefert dem Kunden keinen verlässlichen Nutzen

---

Welche typischen Inhalte hat ein SLA laut [BeZi15] / Allweyer?

?

**12 typische SLA-Inhalte:**
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

**Wichtige Zusatzpunkte (Allweyer):**
- Verfügbarkeit bezieht sich auf den **vollständigen Service beim Nutzer**, nicht auf einzelne Komponenten (Server, Netzwerk)
- Der Provider kann nur garantieren, was in seinem Verantwortungsbereich liegt (externe Internet-Anbindung des Kunden liegt außerhalb)
- Reporting-Methode muss gemeinsam festgelegt sein; sonst lässt sich Unterschreitung nicht nachweisen
- Strafen für Nichteinhaltung können vereinbart werden (z. B. Zahlungskürzungen)

---

### Anwendung

Skizzieren Sie ein SLA für den KIS-Service im Krankenhaus — decken Sie alle vier ITIL-4-Anforderungen ab.

?

**KIS-SLA-Skizze:**

**1. Servicekatalog-Bezug:** Service „Krankenhausinformationssystem (KIS)" — gelistet im IT-Servicekatalog als kritischer klinischer Service.

**2. Outcome-bezogene Messgrößen (ausgewogen):**
- Technisch: 99,5 % monatliche Verfügbarkeit (gemessen am Nutzer-Arbeitsplatz), max. 5 Sek. Antwortzeit
- Outcome: Kundenzufriedenheits-Score ≥ 80 % (monatliche Kurzbefragung Pflegeleitung)
- Zuverlässigkeit: max. 2 ungeplante Ausfälle/Monat, kein Ausfall >30 Min. tagsüber

**3. Vereinbarungsprozess:** Abstimmungsrunde mit IT-Leitung, Pflegeleitung, Ärztevertretung, Geschäftsführung, KIS-Hersteller (als Partner) und Datenschutzbeauftragtem.

**4. Verständlichkeit:** SLA in Klarsprache ohne IT-Jargon; jeder Begriff (Verfügbarkeit, Antwortzeit) mit Definition; Verantwortungsbereiche explizit abgegrenzt.

---

Ordnen Sie diese KIS-bezogenen Eigenschaften den Konzepten Utility oder Warranty zu.

?

| Eigenschaft | Utility oder Warranty? |
|---|---|
| Pflegekräfte können Patientendaten abrufen und dokumentieren | **Utility** — Funktionalität |
| KIS ist Mo–So, 00–24 Uhr verfügbar | **Warranty** — Verfügbarkeit |
| Antwortzeit bei Datenbankabfragen ≤ 5 Sek. | **Warranty** — Performance |
| Laborbefunde werden automatisch ins KIS importiert | **Utility** — Funktionalität |
| 99,5 % monatliche Verfügbarkeit garantiert | **Warranty** — Service-Level-Zusicherung |
| Bei Ransomware-Angriff: Wiederherstellung < 4 Stunden | **Warranty** — Kontinuität |
| Rollenzugriffssteuerung für Pflegekraft vs. Arzt | **Warranty** — Sicherheit |

**Merkhilfe:** Utility = WAS; Warranty = WIE VERLÄSSLICH.

---

Welche Probleme entstehen, wenn ein SLA nur technische Messgrößen (z. B. Server-Uptime 99,9 %) enthält, ohne Outcome-Bezug?

?

**Typische Probleme reiner technischer SLAs:**

1. **Komponentenverfügbarkeit ≠ Serviceverfügbarkeit:** Server-Uptime 99,9 % nützt nichts, wenn das Netzwerk zwischen Server und Arbeitsplatz ausfällt oder die Datenbank hängt. Der Nutzer erlebt einen Ausfall — das SLA wird formal erfüllt.

2. **Verfügbarkeit ≠ Nutzbarkeit:** 99,9 % Uptime bei 5 Minuten Ladezeit pro Seite — der Service ist „verfügbar", aber unbrauchbar. Antwortzeiten fehlen als Dimension.

3. **Kein Kundenzufriedenheitsbezug:** Der Provider optimiert auf Kennzahl statt auf Outcome. Pflegekräfte kämpfen täglich mit Usability-Problemen, die kein SLA-Indikator erfasst.

4. **Goodhart-Gesetz (vgl. Guiding Principles):** Wenn eine Metrik zum Ziel wird, hört sie auf, eine gute Metrik zu sein — Teams optimieren die Kennzahl, nicht die tatsächliche Servicequalität.

**ITIL-4-Antwort:** Ausgewogener Messgröße-Satz (balanced scorecard-Ansatz) inkl. Kundenzufriedenheit.

---

### Diskussion

Warum ist der „Vereinbarungs-Charakter" einer der wichtigsten Punkte in den ITIL-4-Anforderungen an SLAs?

?

**Problem ohne echten Vereinbarungsprozess:**
- IT-Abteilung setzt SLAs unilateral fest → Ziele spiegeln IT-Kapazitäten wider, nicht Geschäftsbedürfnisse
- Stakeholder (Pflegedirektion, Ärzte, Partner) kennen das SLA nicht → keine gemeinsame Erwartungsgrundlage
- Bei Verletzung: Streit über „war das so vereinbart?" ohne gemeinsam getragenes Dokument

**Was echter Vereinbarungsprozess bringt:**
- Stakeholder sehen ihre Anforderungen im SLA — Akzeptanz steigt
- IT versteht Geschäfts-Kontext besser (warum ist KIS-Verfügbarkeit nachts kritisch für Notaufnahme?)
- SLA wird zum geteilten Steuerungsdokument, nicht zum Provider-Dokument
- Möglichkeit, unrealistische Forderungen frühzeitig zu adressieren

**Krankenhaus-Kontext:** Ein SLA, das ohne Pflegeleitung und Ärztevertreter erstellt wurde, wird bei einer Prüfung im Rahmen der Krankenhausakreditierung nicht anerkannt. Der Vereinbarungsprozess ist hier auch regulatorisch relevant.

---

Wie unterscheiden sich Standard-SLAs und individuell ausgehandelte SLAs — und wann ist welche Form sinnvoll?

?

**Standard-SLAs (Allweyer):**
- Vom Anbieter vorgegeben; Kunde wählt aus vordefinierten Levels (z. B. Standard-Support vs. Premium-Support)
- Meist mit unterschiedlichen Preisen für verschiedene Warranty-Stufen
- Vorteil: skalierbar, schnell einzuführen, geringer Verhandlungsaufwand
- Nachteil: passt möglicherweise nicht zu spezifischen Geschäftsanforderungen

**Individuell ausgehandelte SLAs:**
- Anbieter und Nutzer definieren gemeinsam Service-Levels
- Alle vier ITIL-4-Anforderungen gezielt adressierbar
- Vorteil: maßgeschneidert, Outcome-Bezug möglich
- Nachteil: Zeit- und kostenintensiv; Verhandlungskompetenz auf beiden Seiten nötig

**Wann welche Form:**
| Szenario | Empfehlung |
|---|---|
| Cloud-SaaS-Dienst (z. B. Microsoft 365) | Standard-SLA (Provider setzt Bedingungen) |
| Kritischer klinischer Service (KIS, PACS) | Individuelles SLA mit allen Stakeholdern |
| Standardisierte Infrastruktur-Services | Standard-SLA mit Premium-Option |
| Neue, einmalige Dienstleistung (z. B. Hardware-Migration) | Individuell; andere Inhalte als Verfügbarkeit relevant |

---

## Mögliche Anschlussfragen des Prüfers

- Was ist der Unterschied zwischen Service-Level und SLA?
- Welche Rolle spielt der Servicekatalog für gute SLAs?
- Warum kann ein externer Cloud-Anbieter keine vollständige Verfügbarkeit am Nutzer-Arbeitsplatz garantieren?
- Was ist der Unterschied zwischen Zuverlässigkeit und Verfügbarkeit im SLA-Kontext?
- Welche Konsequenzen hat die Nichteinhaltung eines SLAs (Strafen, Vertrauensverlust)?
- Wie hängt SLM mit der ITIL-4-Practice Continual Improvement zusammen?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
