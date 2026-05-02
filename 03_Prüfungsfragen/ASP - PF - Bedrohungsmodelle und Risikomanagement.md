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

# ASP - PF - Bedrohungsmodelle und Risikomanagement

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Bedrohungsmodelle und Risikomanagement aus ASP. Umfasst grundlegende Sicherheitskonzepte (CIA-Triade, 8 Security-Eigenschaften, IT-Sicherheit vs. Informationssicherheit), den achtteiligen Angriffskatalog des Alice-Bob-Eve-Modells (Folien 19–27), sowie den vollständigen Informationssicherheits-Risikomanagement-Prozess nach ISO 27005 mit Grundvoraussetzungen, 7-Schritte-Big-Picture, Risikomatrix, asset-basierter Identifikation (6 Schritte, BSI 200-2), Risikobehandlung (4 Strategien) und Überwachung (KPI/KRI). Alle Konzepte aus VL Einführung und Motivation sowie VL Informationssicherheits-Risikomanagement.

## Verlinkte Konzepte

- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Informationssicherheit - IT-Sicherheit vs Informationssicherheit]]
- [[ASP - Security Eigenschaften - Uebersicht]]
- [[ASP - Security Eigenschaften - Reliability]]
- [[ASP - Angriff - Nachricht lesen]]
- [[ASP - Angriff - Traffic Analysis]]
- [[ASP - Angriff - Aufzeichnung und Entschluesselung]]
- [[ASP - Angriff - Replay]]
- [[ASP - Angriff - Modifikation Plaintext]]
- [[ASP - Angriff - Modifikation Ciphertext]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Angriff - Denial-of-Service]]
- [[ASP - Risikomanagement - Definition Risiko]]
- [[ASP - Risikomanagement - Grundvoraussetzungen]]
- [[ASP - Risikomanagement - Big Picture]]
- [[ASP - Risikomanagement - Risikomatrix]]
- [[ASP - Risikomanagement - Risikoidentifikation Ansaetze]]
- [[ASP - Risikomanagement - Asset-basierte Identifikation]]
- [[ASP - Risikomanagement - IT-Grundschutz BSI 200-2]]
- [[ASP - Risikomanagement - Risikobehandlung]]
- [[ASP - Risikomanagement - Ueberwachung KPI KRI]]

---

## Karten

### Definition

Frage: Was bedeuten Vertraulichkeit, Integrität und Verfügbarkeit in der CIA-Triade? Für welche Informationsarten gilt die Triade?

?

Antwort: Laut Folie 9 (VL Einführung und Motivation):

| Schutzziel | Bedeutung | Typische Maßnahme (el. Daten) |
|---|---|---|
| **Confidentiality (Vertraulichkeit)** | Schutz vor Offenlegung durch Unbefugte; nur autorisierte Personen lesen und verändern Daten. | Verschlüsselung |
| **Integrity (Integrität)** | Schutz vor Änderungen durch Unbefugte; unveränderbare, nachvollziehbare Änderungen. | Prüfsummen, Hash, Digitale Signaturen |
| **Availability (Verfügbarkeit)** | Gewährleistung, dass autorisierte Parteien bei Bedarf Zugriff erhalten; Ausfallsicherheit. | Redundanzsysteme |

**Reichweite (Folie 8/10):** Gilt nicht nur für elektronische Daten, sondern auch für Wissen (z. B. NDAs), gesprochenes Wort und Dokumente in Papierform.

---

Frage: Welche fünf Sicherheitseigenschaften kommen zur CIA-Triade hinzu? Welche acht Eigenschaften bilden den Gesamtkatalog der Vorlesung?

?

Antwort: Laut Folie 13/14 (VL Einführung und Motivation):

Die Vorlesung stellt acht Security-Eigenschaften vor (Folie 13 als Kreis mit acht Segmenten):

| Eigenschaft | Englisch | Kerngedanke |
|---|---|---|
| Vertraulichkeit | Confidentiality | Wer darf zugreifen? (CIA) |
| Integrität | Integrity | Sind die Daten unverändert? (CIA) |
| Verfügbarkeit | Availability | Sind die Daten erreichbar? (CIA) |
| **Authentizität** | Authenticity | Ist die Partei/Nachricht echt? |
| **Rückverfolgbarkeit** | Non-repudiation | Kann eine Tätigkeit beweisbar nicht abgestritten werden? |
| **Verantwortlichkeit** | Accountability | Wem ist eine Handlung zuzurechnen? |
| **Verlässlichkeit** | Reliability | Funktioniert die Funktion ordnungsgemäß und fehlerfrei? |
| **Privatsphäre** | Privacy | Wofür dürfen die Daten verwendet werden? |

**Hinweis:** Authentizität ist Voraussetzung für Non-repudiation und Accountability. Privatsphäre ist NICHT in Vertraulichkeit enthalten (andere Kernfrage: wofür, nicht wer).

---

Frage: Welche drei Voraussetzungen müssen gleichzeitig erfüllt sein, damit ein Informationssicherheits-Risiko besteht?

?

Antwort: Laut Folien 3–5 (VL Informationssicherheits-Risikomanagement):

**Trias (Venn-Diagramm, Folie 3):**
- **Asset** – schützenswerter Wert (Server, Daten, Gebäude, Mitarbeiter, Reputation).
- **Bedrohung** – mögliche Ursache eines unerwünschten Ereignisses (Feuer, Malware, Hacking, ehemaliger Mitarbeiter).
- **Schwachstelle** – ausnutzbare Verwundbarkeit (fehlendes Patch-Management, schwache Login-Verfahren, fehlender Rechteentzug).

→ **Risiko = Schnittmenge** aller drei. Fehlt eines, gibt es kein Risiko.

**Abgrenzung (Folie 5):**
- Bedrohung allein ≠ Risiko (z. B. „Cyberterroristen haben zugenommen" – ohne Asset + Schwachstelle keine Bewertung).
- Schwachstelle allein ≠ Risiko (abgefahrene Reifen sind nur ein Risiko, wenn man fährt).
- Eingetretenes Ereignis ≠ Risiko – es ist dann ein **Schadensereignis** (Risiko hat sich realisiert).

---

Frage: Wie definieren Duden und ISO 27005:2022 den Risikobegriff? Worin unterscheiden sie sich?

?

Antwort: Laut Folie 2 (VL Informationssicherheits-Risikomanagement):

**Duden:**
> Möglicher negativer Ausgang bei einer Unternehmung, mit dem Nachteile, Verlust, Schäden verbunden sind.

**ISO 27005:2022:**
> „Effect of uncertainty on objectives."
> Note 1: Ein Effekt ist eine Abweichung vom Erwarteten – positiv oder negativ.
> Note 6: Im Kontext der Informationssicherheit sind Risiken üblicherweise mit einem **negativen Effekt** verbunden.

**Unterschied:**

| Aspekt | Duden | ISO 27005:2022 |
|---|---|---|
| Tonart | Explizit negativ | Formal neutral (Note 6 pragmatisch negativ) |
| Reichweite | Allgemeinsprachlich | Formal / international |
| Implikation | Verlust, Schaden | Abweichung von Zielen |

**Schlussfolgerung:** ISO wählt die neutrale Formulierung, weil der Standard auch auf allgemeines Risikomanagement (ISO 31000) aufbaut. Im Praxis-Kontext Informationssicherheit gilt Note 6: negative Abweichung.

---

### Anwendung

Frage: Ordne die acht Angriffstypen des Vorlesungs-Angriffskatalogs den verletzten Schutzzielen und den Gegenmaßnahmen zu.

?

Antwort: Laut Folien 19–27 (VL Einführung und Motivation):

| Angriff | Verletztes Schutzziel | Gegenmaßnahme |
|---|---|---|
| **Nachricht lesen** | Vertraulichkeit | Verschlüsselung |
| **Traffic Analysis** | Vertraulichkeit | Verschlüsselung + Padding/Glätten der Nachrichtengröße |
| **Aufzeichnung & nachträgliche Entschlüsselung** | Vertraulichkeit (evtl. Integrität) | Perfect Forward Secrecy (PFS) |
| **Replay** | Integrität (Authentizität) | Zeitstempel, Sequenznummern, Nonces |
| **Modifikation Plaintext** | Integrität (Authentizität) | HMAC, digitale Signatur |
| **Modifikation Ciphertext** | Integrität | HMAC oder digitale Signatur **zusätzlich** zur Verschlüsselung |
| **Impersonation** | Integrität (Authentizität) | HMAC, digitale Signatur |
| **Denial-of-Service** | Verfügbarkeit | Protokollabhängig; oft schwer zu mitigieren |

**Muster:** Vertraulichkeits-Angriffe → Verschlüsselung; Integritäts-Angriffe → HMAC/Signatur; Verfügbarkeits-Angriff → kryptografische Mittel helfen nicht.

---

Frage: Welche sieben Schritte umfasst der Risikomanagement-Prozess nach ISO 27005? Welche zwei Querschnitts-Aktivitäten begleiten ihn, und welche Schritte bilden das „Risk Assessment"?

?

Antwort: Laut Folie 7 (VL Informationssicherheits-Risikomanagement):

**Sieben Schritte:**
1. **Bestimmung des Kontexts** – Geltungsbereich, Rollen, Bewertungsskalen, Akzeptanzkriterien.
2. **Risikoidentifikation** – ereignis-basiert oder asset-basiert.
3. **Risikoanalyse** – Eintrittswahrscheinlichkeit und Auswirkung bewerten.
4. **Risikoevaluierung** – Vergleich mit Akzeptanzkriterien.
5. **Risikobehandlung** – Vermeidung, Reduktion, Transfer, Akzeptanz.
6. **Risikokommunikation** – Bericht und Reporting.
7. **Überwachung und Verbesserung** – KPI/KRI, kontinuierliche Verbesserung.

**Zwei Querschnitts-Aktivitäten** (laufen über alle Schritte hinweg):
- **Communication and Consultation**
- **Monitoring and Review**

**Risk Assessment** = Schritte 2–4 zusammen (gestricheltes Kästchen im ISO-Diagramm).

**Decision Points:** Ist das Assessment satisfactory? (→ nein: zurück zur Identifikation). Ist das Risiko akzeptiert? (→ nein: zurück zur Behandlung).

---

Frage: Welche sechs Schritte umfasst die asset-basierte Risikoidentifikation nach BSI 200-2, und welches Ergebnis liefert jeder Schritt?

?

Antwort: Laut Folien 19–35 (VL Informationssicherheits-Risikomanagement):

| Schritt | Hauptaktivität | Ergebnis |
|---|---|---|
| **1. Strukturanalyse + Schutzbedarfsfeststellung** | Alle Assets + Abhängigkeiten erfassen; Schutzbedarf C/I/A pro Asset festlegen (Top-Down mit Vererbung) | Asset-Liste mit Schutzbedarfsklassen |
| **2. IT-Grundschutz-Modellierung (BSI 200-2)** | Relevante Bausteine pro Asset zuordnen (APP, SYS, NET, INF, OPS, …) | Bausteine je Asset |
| **3. Gefährdungsübersicht** | Elementare, spezifische und zusätzliche Gefährdungen pro Asset sammeln | Liste relevanter Gefährdungen |
| **4. Anforderungsübersicht** | Soll-Ist-Vergleich: bestehende vs. geforderte Maßnahmen je Baustein-Anforderung | Erfüllungs-Status je Anforderung |
| **5. Schwachstellenanalyse** | Nicht-erfüllte Anforderungen als Schwachstellen identifizieren | Liste offener Schwachstellen |
| **6. Risikoliste** | Pro Risiko: Wer – tut Was – gegen Wen – mit welcher Auswirkung | Strukturierte Risikoliste |

**Abgrenzung:** Diese 6 Schritte entsprechen nur Schritt 2 (Risikoidentifikation) im 7-Schritte-Big-Picture der ISO 27005.

---

Frage: Welche vier Strategien zur Risikobehandlung gibt es, und wie dokumentiert man sie im Risikobehandlungsplan?

?

Antwort: Laut Folien 39–41 (VL Informationssicherheits-Risikomanagement):

**Vier Basis-Strategien:**

| Strategie | Mechanismus | Beispiel |
|---|---|---|
| **Vermeidung** | Gewisse Tätigkeiten/Prozesse werden nicht durchgeführt | Onlineshop schließen |
| **Reduktion** | Risikoreduzierende Maßnahmen implementieren | Firewall einrichten, IDS, Patches |
| **Transfer** | Verantwortung verlagern (z. B. Versicherung) | Cyber-Versicherung abschließen |
| **Akzeptanz** | Restrisiko in Kauf nehmen | Dokumentierte Entscheidung der Geschäftsführung |

**Risikobehandlungsplan (Folie 41):** Tabellarisch pro Risiko mit den Pflichtfeldern: Risiko · Strategie · Konkrete Maßnahme · Umsetzung bis · Verantwortlich · Kosten · Auswirkung auf Risiko · **Restrisiko**.

**Wichtige Eigenschaften:**
- Pro Risiko können **mehrere Strategien kombiniert** werden (z. B. Risiko 1: Reduktion + Transfer).
- **Akzeptanz ≠ Ignorieren** – auch akzeptierte Risiken werden dokumentiert und überwacht.
- **Transfer eliminiert das Risiko nicht** – Versicherung deckt finanzielle Folgen, nicht Reputationsschaden.

---

### Diskussion

Frage: Warum reicht reine IT-Sicherheit nicht aus, um Informationssicherheit im Krankenhaus sicherzustellen?

?

Antwort: Aus der Note zu IT-Sicherheit vs. Informationssicherheit (Folien 8, 10, 11, VL Einführung und Motivation):

**IT-Sicherheit** ist eine **Teilmenge** der Informationssicherheit:
- Schützt technische Systeme (Hardware, Software, Netze).
- Mittel: Zugriffskontrollen, Kryptografie.

**Informationssicherheit** umfasst darüber hinaus:
- **Nicht-technische Informationsträger:** Papierarchive, gesprochenes Wort, Wissen.
- **Betriebliche Strukturen:** Kommunikationswege, Richtlinien, Schulungen.

**Konkrete Beispiele, die IT-Sicherheit nicht abdeckt:**
- Vertraulichkeit von **Wissen:** geschützt durch Vertraulichkeitsvereinbarungen (NDA), nicht durch Verschlüsselung.
- Verfügbarkeit von **Wissen:** gesichert durch Wissenstransfer und Vertretungsregelungen.
- Arztbrief in Papierform: Vertraulichkeit durch physische Zugriffskontrolle, Integrität durch Archivierungs-Prozesse.

**Fazit:** Wer im Krankenhaus nur IT-Sicherheit betreibt und organisatorische Maßnahmen vernachlässigt, hat blinde Flecken für physische, personelle und prozessuale Risiken.

---

Frage: Warum schützt Verschlüsselung allein nicht gegen alle relevanten Angriffe im Vorlesungs-Katalog? Konkret: gegen welche Angriffe hilft Verschlüsselung nicht?

?

Antwort: Aus den Angriff-Notes (Folien 19–27, VL Einführung und Motivation):

Verschlüsselung schützt primär gegen **Nachricht lesen** (Vertraulichkeits-Angriff). Sie hilft **nicht** gegen:

1. **Traffic Analysis (Folie 20):** Eve leitet Informationen aus der Nachrichtengröße ab, ohne sie zu entschlüsseln. Beispiel: 100 KB = positiver COVID-Test, 80 KB = negativer Test → Ergebnis erkennbar trotz Verschlüsselung. Gegenmaßnahme: Padding.

2. **Aufzeichnung & nachträgliche Entschlüsselung (Folie 21):** Eve zeichnet Ciphertext auf, kompromittiert später den Schlüssel. Gegenmaßnahme: Perfect Forward Secrecy.

3. **Replay (Folie 22):** Eve schickt eine ältere, legitime (verschlüsselte) Nachricht erneut – kein Klartext-Zugriff erforderlich. Gegenmaßnahme: Zeitstempel/Nonces.

4. **Modifikation Ciphertext (Folie 24):** Eve manipuliert den Ciphertext, ohne ihn zu verstehen – Integrität ist verletzt, obwohl verschlüsselt. Gegenmaßnahme: HMAC oder Signatur zusätzlich.

5. **Denial-of-Service (Folie 26):** Eve blockiert Nachrichten. Kryptografie hilft hier gar nicht – Schutz liegt auf Netzwerk/Infrastruktur-Ebene.

**Fazit:** Verschlüsselung ≠ vollständige Sicherheit. Integrität, Aktualität und Verfügbarkeit erfordern zusätzliche Bausteine.

---

Frage: Welche Granularität soll eine Risikomatrix haben, und welche Trade-offs entstehen? Welches Problem benennt die Vorlesung explizit bei einer 3×3-Matrix?

?

Antwort: Laut Folie 13 (VL Informationssicherheits-Risikomanagement):

**Aufbau der Matrix:**
- y-Achse: Eintrittswahrscheinlichkeit (1 gering bis 4/5 sehr hoch).
- x-Achse: Auswirkung im Schadensfall.
- Risikowert = Eintrittswahrscheinlichkeit × Auswirkung.
- Farbliche Risikoklassen: Rot (hoch) · Gelb (mittel) · Grün (gering).

**Problem 3×3-Matrix (explizit in Folie 13):** Zwei sehr unterschiedliche Risiken können in derselben Zelle landen – kein erkennbarer Unterschied mehr. Die 3×3-Matrix unterschätzt die Differenzierungsnotwendigkeit.

**Trade-offs:**

| Aspekt | Kleinere Matrix (3×3) | Größere Matrix (4×4, 5×5) |
|---|---|---|
| Übersichtlichkeit | hoch | geringer |
| Differenzierung | gering | höher |
| Aufwand | niedrig | höher |
| Empfehlung Vorlesung | zu grob; nicht empfohlen | bevorzugt |

---

### Vergleich

Frage: Vergleichen Sie den ereignis-basierten und den asset-basierten Ansatz zur Risikoidentifikation: Sicht, Startpunkt, Stärken, Schwächen – und für welche Aufgaben ist welcher Ansatz geeignet?

?

Antwort: Laut Folie 17 (VL Informationssicherheits-Risikomanagement):

| Aspekt | Ereignis-basiert | Asset-basiert |
|---|---|---|
| **Sicht** | Top-Down | Bottom-Up |
| **Startpunkt** | Strategisches Szenario (z. B. Pandemie, Standortausfall) | Einzelnes Asset oder Asset-Gruppe |
| **Detaillierungsgrad** | Grob, übergreifend | Fein, asset-spezifisch |
| **Stärke** | Erkennt Querschnitts-Szenarien (mehrere Assets betroffen) | Erkennt spezifische technische Schwachstellen |
| **Schwäche** | Übersieht ggf. Detail-Lücken | Übersieht ggf. systemübergreifende Szenarien |
| **Einsatz** | Strategische Planung, BCM | Operative IT-Sicherheit, IT-Grundschutz |
| **In der Vorlesung detailliert** | Nur konzeptuell | 6-Schritte-Methodik (BSI 200-2) |

**Kombination:** Beide Ansätze schließen einander nicht aus – in der Praxis werden sie kombiniert.

---

Frage: Was sind KPIs und KRIs, wie unterscheiden sie sich, und was sind Pflicht-Felder für einen KRI?

?

Antwort: Laut Folien 45–46 (VL Informationssicherheits-Risikomanagement):

| Aspekt | KPI (Key Performance Indicator) | KRI (Key Risk Indicator) |
|---|---|---|
| **Fokus** | Erfolg / Effektivität einer Aktivität | Überwachung potenzieller Risiken |
| **Frage** | Läuft es gut? | Droht etwas schief zu laufen? |
| **Beispiele** | Patch-Quote 95 %, MTTR < 4 h | Anzahl erfolgreicher Angriffe/Monat, Phishing-Klickrate |
| **Überschreitung** | Unter Zielwert = Handlungsbedarf | Über Schwellwert = automatisch Maßnahme auslösen |

**Pflicht-Felder eines KRI (Folie 46):** KRI-Beschreibung · Verantwortlicher · **Schwellwert**.

**Beispiel aus der Folie (Folie 46):**
KRI: „Anzahl erfolgreicher Angriffe auf das Netzwerk pro Monat" · Erhebung: Monitoring von Netzwerklogs, IDS-Auswertung · Verantwortlich: IT-Abteilung · Schwellwert: 5 erfolgreiche Angriffe pro Monat.

**Hinweis:** Die richtige Auswahl von KRI und KPI ist laut Folie 45 entscheidend für hohe Aussagekraft und Relevanz. Schwellwerte sollten mit der Risikolage angepasst werden.

---

## Mögliche Anschlussfragen des Prüfers

- Welche Schutzziele werden durch eine reine Verschlüsselung NICHT abgedeckt?
- Warum ist Privatsphäre ein eigenes Schutzziel und nicht in Vertraulichkeit enthalten?
- Warum ist Reliability eine eigene Sicherheitseigenschaft und keine bloße Verfeinerung von Availability?
- Gib ein eHealth-Szenario, in dem Verschlüsselung allein nicht ausreicht (Traffic Analysis).
- Welche Schutzmaßnahmen wirken gegen DoS – im Gegensatz zu kryptografischen Mitteln?
- Wie unterscheiden sich Bedrohung, Schwachstelle, Risiko und Schadensereignis?
- Was passiert am „Decision Point 2" in ISO 27005, wenn das Risiko nicht akzeptiert wird?
- Wie erbt ein Asset seinen Schutzbedarf im IT-Grundschutz-Prozess?
- Welche BSI 200-2-Bausteine passen auf ein zentrales KIS? (APP: Anwendung; SYS: Server; NET: Netzwerk; INF: Serverraum.)
- Wann ist Risikoakzeptanz die richtige Strategie – und was ist dabei trotzdem Pflicht?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
