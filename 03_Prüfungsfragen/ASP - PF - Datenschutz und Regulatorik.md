---
fach: asp
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/asp
---

# ASP - PF - Datenschutz und Regulatorik

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Datenschutz und Regulatorik aus ASP. Umfasst die Abgrenzung Privacy vs. Confidentiality als Schutzziele, die vier von der Vorlesung genannten DSGVO-Grundsätze sowie die beiden Pflichten aus DSGVO Art. 25: Privacy by Design (Abs. 1) und Privacy by Default (Abs. 2). Alle vier Konzept-Notes stammen aus VL Einführung und Motivation (Folien 15–17). Achtung: Die Vorlesung nennt keine Artikelnummern für die vier Grundsätze – nur für Art. 25 (Privacy by Design/Default).

## Verlinkte Konzepte

- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - DSGVO - Privacy by Design]]
- [[ASP - DSGVO - Privacy by Default]]

---

## Karten

### Definition

Frage: Worin unterscheiden sich Vertraulichkeit (Confidentiality) und Privatsphäre (Privacy) als Schutzziele?

?

Antwort: Laut Folie 15 (VL Einführung und Motivation):

| Aspekt | Vertraulichkeit | Privatsphäre |
|---|---|---|
| Kernfrage | **Wer** darf auf Informationen zugreifen? | **Wofür** darf zugegriffen werden? |
| Schutz vor | Unbefugtem Zugriff | Zweckwidriger Verwendung trotz erlaubten Zugriffs |
| Typische Maßnahme | Verschlüsselung, Zugriffskontrolle | Zweckbindung, organisatorische Richtlinien |

**Kernaussage:** Eine Person kann *autorisiert sein zuzugreifen* (Vertraulichkeit erfüllt) und die Daten trotzdem zweckwidrig verwenden (Privatsphäre verletzt).

**Beispiel (Folie 15):** Eine Krankenschwester hat autorisierten Zugriff auf eine Patientenakte → Vertraulichkeit ist gewahrt. Würde sie die Akte privat einer Bekannten zeigen, ist Privatsphäre verletzt – obwohl der Zugriff selbst erlaubt war.

---

Frage: Welche vier Grundsätze für die Verarbeitung personenbezogener Daten nennt die Vorlesung?

?

Antwort: Laut Folie 16 (VL Einführung und Motivation):

1. **Zweckbindung** – Daten dürfen nur für den festgelegten Zweck erhoben und verwendet werden.
2. **Datenminimierung** – Es sollen nur die für den Zweck notwendigen Daten erhoben werden.
3. **Speicherbegrenzung** – Daten dürfen nur so lange gespeichert werden, wie es für den Zweck notwendig ist.
4. **Integrität und Vertraulichkeit** – Angemessene Sicherheit der Daten muss gewährleistet sein.

**Geltungsbereich (laut Folie):** Gilt für alle Unternehmen, die Daten von EU-Bürgern verarbeiten – unabhängig vom Standort.

*(Artikelnummern für diese Grundsätze sind im PDF nicht angegeben. Die Vorlesung nennt ausschließlich diese vier Grundsätze; weitere Grundsätze des Art. 5 DSGVO sind im PDF nicht aufgeführt.)*

---

### Anwendung

Frage: Was bedeutet Privacy by Design, welcher DSGVO-Artikel regelt es, und welche Maßnahme wird in der Vorlesung als Beispiel genannt?

?

Antwort: Laut Folie 17 (VL Einführung und Motivation):

- **Rechtsgrundlage:** DSGVO **Artikel 25 Abs. 1**
- **Kernforderung:** Datenschutz durch Technikgestaltung – **von Anfang an**, nicht nachträglich aufgesetzt.
- **Maßnahmenebene:** Geeignete technische **und** organisatorische Maßnahmen.
- **Beispiel-Maßnahme (laut Folie):** Pseudonymisierung.

**Kernidee:** Datenschutzfreundliche Mechanismen sollen bereits in der Architektur und im Entwurfsprozess eines Systems verankert sein. Ein nachträgliches Hinzufügen ist typischerweise schwächer, weil bestehende Datenflüsse schwer umzustrukturieren sind.

---

Frage: Was bedeutet Privacy by Default, welcher DSGVO-Artikel regelt es, und für wen ist es besonders gedacht?

?

Antwort: Laut Folie 17 (VL Einführung und Motivation):

- **Rechtsgrundlage:** DSGVO **Artikel 25 Abs. 2**
- **Kernforderung:** Standardmäßig datenschutzfreundliche Voreinstellungen – die Standardeinstellung eines Produkts muss bereits datenschutzfreundlich sein.
- **Schutzfokus (laut Folie):** Dient vor allem dem Schutz **weniger technikversierter Personen**.
- **Mechanik:** Möglichkeit zur aktiven Anpassung der Privatsphäre-Einstellungen muss gegeben sein (z. B. Add-Blocker im Browser als Beispiel für aktive Anpassung).

**Logik:** Wer nie Einstellungen ändert, ist automatisch durch die datenschutzfreundlichen Defaults geschützt. Mehr Funktionalität auf Kosten der Privatsphäre erfordert aktives Opt-in.

---

Frage: Welcher DSGVO-Grundsatz ist in den folgenden eHealth-Szenarien verletzt?
(a) Eine App erhebt SVNR und Anschrift für eine reine Terminbuchung.
(b) Eine Praxis speichert Patientendaten dauerhaft, auch nach Behandlungsende.
(c) Ein Arzt teilt Befunddaten für Marketingzwecke des Praxissoftware-Herstellers.

?

Antwort: Auf Basis der vier DSGVO-Grundsätze (Folie 16, VL Einführung):

**(a) Datenminimierung verletzt** – für die Terminbuchung sind SVNR und Anschrift nicht notwendig; es sollen nur die für den Zweck erforderlichen Daten erhoben werden.

**(b) Speicherbegrenzung verletzt** – Daten dürfen nur so lange gespeichert werden, wie es für den ursprünglichen Zweck notwendig ist.

**(c) Zweckbindung verletzt** – Befunddaten wurden für den Behandlungszweck erhoben; ihre Weitergabe für Marketingzwecke widerspricht dem festgelegten Erhebungszweck.

*(Konkrete Artikel sind in den Szenarien aus dem PDF nicht ableitbar; Grundsatz-Zuordnung basiert auf Folie 16.)*

---

### Diskussion

Frage: Warum reicht es im DSGVO-Kontext nicht aus, „nur" Vertraulichkeit durch Verschlüsselung sicherzustellen?

?

Antwort: Aus den Notes zu Privacy vs. Confidentiality und DSGVO-Grundsätzen (Folien 15–16):

**Vertraulichkeit** adressiert ausschließlich, *wer* auf Daten zugreifen darf – und kann durch technische Maßnahmen wie Verschlüsselung und Zugriffskontrolle sichergestellt werden.

**Datenschutz (DSGVO)** fordert darüber hinaus:
- **Privatsphäre / Zweckbindung:** Auch ein autorisierter Zugriff darf nur für den festgelegten Zweck erfolgen. Verschlüsselung verhindert keinen Missbrauch durch berechtigte Nutzer.
- **Datenminimierung:** Es dürfen nur notwendige Daten erhoben werden – Verschlüsselung ändert nichts an der Tatsache, dass überschüssige Daten vorhanden sind.
- **Speicherbegrenzung:** Daten müssen nach Zweckerfüllung gelöscht werden – Verschlüsselung ist keine Löschung.
- **Privacy by Design / Privacy by Default:** Technische und organisatorische Gestaltung des Systems.

**Fazit:** DSGVO-Konformität erfordert über Verschlüsselung hinaus Prozess-, Organisations- und Architektur-Maßnahmen.

---

Frage: Stellen Sie sich ein Szenario vor, in dem alle vier DSGVO-Grundsätze eingehalten werden, aber dennoch ein Datenschutzproblem entsteht. Wie kann das sein?

?

Antwort: Auf Basis der Vorlesungs-Notes (Folien 15–16):

Die vier Grundsätze (Zweckbindung, Datenminimierung, Speicherbegrenzung, Integrität/Vertraulichkeit) sind eine **Teilmenge** der tatsächlichen DSGVO-Pflichten. Ein Problem kann entstehen, wenn:

- **Transparenz fehlt:** Die betroffene Person weiß nicht, welche Daten zu welchem Zweck erhoben werden – nicht explizit in den vier Grundsätzen adressiert.
- **Einwilligung fehlt oder unwirksam ist:** Auch wenn die Daten minimal und zweckgebunden verarbeitet werden, braucht es eine Rechtsgrundlage.
- **Privacy by Design/Default fehlt:** Art. 25 DSGVO fordert Architektur- und Default-Maßnahmen, die in den vier Grundsätzen nicht explizit stehen.
- **Rechenschaftspflicht:** Der Verantwortliche muss nachweisen können, dass er die Grundsätze einhält – fehlt der Nachweis, ist das ein Problem.

*(Die Vorlesung nennt nur diese vier Grundsätze und weist darauf hin, dass weitere Grundsätze aus Art. 5 DSGVO im PDF nicht aufgeführt werden.)*

---

### Vergleich

Frage: Vergleichen Sie Privacy by Design und Privacy by Default: DSGVO-Artikel, Adressiert, Forderung, typisches Umsetzungs-Beispiel – und welches ist in der Praxis schwerer umzusetzen?

?

Antwort: Laut Folie 17 (VL Einführung und Motivation):

| Aspekt | Privacy by Design | Privacy by Default |
|---|---|---|
| DSGVO-Artikel | Art. 25 **Abs. 1** | Art. 25 **Abs. 2** |
| Zeitpunkt | Architektur & Entwicklung | Fertig-Produkt (Einstellungen) |
| Adressiert | Systemgestaltung | Voreinstellungen |
| Forderung | Datenschutz von Anfang an einbauen | Standardeinstellungen datenschutzfreundlich wählen |
| Maßnahmen-Ebene | technisch + organisatorisch | Produkt-Konfiguration |
| Beispiel (Folie) | Pseudonymisierung | Add-Blocker-Möglichkeit im Browser |

**Praxis-Schwierigkeit:** Privacy by Design ist in der Praxis typischerweise schwerer umzusetzen, weil es strukturelle Architekturentscheidungen in einer frühen Projektphase erfordert, wenn der Umfang noch unklar ist. Privacy by Default ist ein konfigurativer Schritt am Ende der Entwicklung. *(Bewertung nicht explizit im PDF; ergibt sich aus der Prüfungsrelevanz-Sektion der Notes.)*

---

## Mögliche Anschlussfragen des Prüfers

- Geben Sie ein Szenario, in dem Vertraulichkeit erfüllt, aber Privatsphäre verletzt ist.
- Welcher der vier DSGVO-Grundsätze hat den stärksten Bezug zum Schutzziel Privatsphäre?
- Was bedeutet Pseudonymisierung, und welchen DSGVO-Grundsatz unterstützt sie besonders?
- Wie unterscheidet sich Privacy by Design von „Security by Design"?
- Welche Konsequenzen hat ein DSGVO-Verstoß für ein Unternehmen? *(Im PDF nicht ausgeführt.)*
- Welche technischen und organisatorischen Maßnahmen könnten Privacy by Design in einem ePA-System konkret realisieren?
- Warum ist nachträglich aufgesetzter Datenschutz typischerweise schwächer als Privacy by Design?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
