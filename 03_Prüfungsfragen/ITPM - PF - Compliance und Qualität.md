---
fach: itpm
typ: pruefungsfrage
status: offen
tags:
  - fach/vertiefung/itpm
  - typ/pruefungsfrage
  - status/offen
  - flashcards
---

# ITPM - PF - Compliance und Qualität

Prüfungsfragen-Sammlung zu Qualitätsdefinition, QM/QS, qualitätsbezogene Kosten, Quality Gates, Critical Qualities, Compliance-Grundlagen, CMS und IT-Projekt-Compliance.

---

## Definition

Wie wird Qualität definiert, und welche Formel beschreibt sie? Was ist der Unterschied zwischen QM, QS und Qualitätsverbesserung?

?

**Qualitätsdefinition (Folie 6):** Qualität bedeutet, dass ein Produkt **für den jeweiligen Zweck geeignet** ist.

**Formel:** `Leistung / Erfordernisse = 1`

Bewusst **„Erfordernisse"**, nicht „Anforderungen" – beide können voneinander abweichen. Erfordernisse müssen erkannt und verstanden werden; Leistungen müssen erbracht werden können.

**Drei Begriffe im Überblick:**

| Begriff | Funktion |
|---|---|
| **Qualitätsmanagement (QM)** | Leiten und Lenken einer Organisation in Bezug auf Qualität; legt fest, **wie gut** Ergebnisse werden und **wie** diese Qualität erreicht wird |
| **Qualitätssicherung (QS)** | Teil des QM; stellt sicher, dass Qualitätsanforderungen **erfüllt** werden; beantwortet: Sind Maßnahmen richtig umgesetzt? Wirksam? Ist das Produkt gut genug? |
| **Qualitätsverbesserung** | Teil des QM; erhöht Effektivität (Wirkungsgrad), Effizienz (Wirtschaftlichkeit) und Transparenz |

**Abgrenzung:** Qualität ≠ Maximum – Formel = 1 (nicht > 1) ist bewusst gewählt: Überqualität verursacht unnötige Kosten.

Quelle: [[ITPM - Qualität - Definition]]

---

Wie wird Compliance definiert, wer ist dafür verantwortlich, und was bedeutet „nachweislich"?

?

**Definition (Folie 7–8):** Compliance liegt vor, wenn alle Vorgaben, die dem Unternehmen **extern auferlegt** worden sind bzw. die das Unternehmen intern als **verbindlich akzeptiert**, **nachweislich eingehalten** werden.

**Übersetzung:** „Regelkonformität"

**Drei Komponenten:**

| Komponente | Bedeutung |
|---|---|
| **Vorgaben** | Extern (Gesetze, Standards) + intern (Richtlinien) + vertraglich |
| **Nachweisbarkeit** | Dokumentiert und prüfbar – nicht nur „wir halten uns daran", sondern belegbar |
| **Verantwortung** | **Vorstand / Geschäftsführer** trägt die Pflicht, für Einhaltung zu sorgen |

**Inhaltlich:** Einhaltung gesetzlicher Bestimmungen, Regeln und Normen durch das Unternehmen und seine Mitarbeiter + Gesamtheit aller betrieblichen Maßnahmen zur Sicherstellung regelkonformen Verhaltens.

**Abgrenzung:** Compliance ≠ Ethik (Ethik geht über das Recht hinaus); Compliance ≠ QM.

Quelle: [[ITPM - Compliance - Definition]]

---

Was sind die drei Faktoren qualitätsbezogener Kosten?

?

**Definition (Folie 16):** Qualitätsbezogene Kosten sind Kosten, die für das Erreichen zufriedenstellender Qualität entstehen, sowie Verluste durch Nicht-Erreichen der entsprechenden Qualität.

**Drei Faktoren:**

| Faktor | Beschreibung |
|---|---|
| **Kosten für das Schaffen von Qualität** | Investitionen in qualitätsfördernde Maßnahmen während der Entwicklung |
| **Kosten für das Schaffen von Vertrauen in diese Qualität (QS)** | Aufwand für Tests, Reviews, Audits, Quality Gates |
| **Verluste durch Qualitätsmängel** | **Nach Projektende sichtbar** – Reklamationen, Imageverlust, Nacharbeit, Haftung |

**Wichtig:** Die ersten zwei Faktoren sind **präventive Investitionen**; der dritte sind **reaktive Verluste**, oft sichtbar erst im Betrieb. Die Balance zwischen Investition und Verlustvermeidung bestimmt den wirtschaftlichen Optimalpunkt.

Quelle: [[ITPM - Qualitätsbezogene Kosten]]

---

Was sind Critical Qualities, und wie unterscheiden sich Critical Qualities in Use von Critical Product Qualities?

?

**Critical Qualities (Folie 24)** sind die **wirklich wichtigen Anforderungen** für:
- die Umsetzung der **Business Vision**
- die **Quality in Use** (Eignung im Anwendungskontext)
- den **Projekterfolg**

Es geht explizit um die **kritischen wenigen** – nicht um alle Qualitätsanforderungen.

**Zwei Sichten:**

| Sicht | Bezeichnung | Fokus |
|---|---|---|
| **Anwendersicht** | Critical Qualities in Use | Wie erlebt der Anwender das Produkt in seinem Kontext? |
| **Produktsicht** | Critical Product Qualities | Welche Eigenschaften muss das Produkt kontextunabhängig haben? |

**Verbindung zu Quality in Use vs. Product Quality:**
- Quality in Use = kontextabhängig (ISO/IEC 25010) [Ergänzung außerhalb der Vorlesung]
- Product Quality = kontextunabhängig (Produktspezifikationssicht)

**eHealth-Beispiel:** Critical Quality in Use: „Befundergebnis ist für medizinisches Personal innerhalb 2 Sek. abrufbar" · Critical Product Quality: „Datenverschlüsselung AES-256 für alle gespeicherten Patientendaten"

Quelle: [[ITPM - Critical Qualities]], [[ITPM - Quality in Use vs Product Quality]]

---

Wie wird IT-Projekt-Compliance definiert, und welche fünf Schlüsselfragen sind zu beantworten?

?

**Definition (Folie 39):** IT-Projekt-Compliance liegt vor, wenn alle Vorgaben, die einem IT-Projekt extern auferlegt worden sind bzw. die das Unternehmen für das IT-Projekt als verbindlich akzeptiert, **nachweislich eingehalten** werden.

**Fünf Schlüsselfragen (Folie 40):**
1. **Welche Rechtsnormen und Regelwerke** sind für die IT des Unternehmens relevant?
2. **Welche IT-gestützten Prozesse und Anwendungen** sind betroffen, und welche Anforderungen müssen sie erfüllen?
3. **Welche Risiken** resultieren aus fehlender oder mangelhafter IT-Compliance?
4. **Welche Compliance-Anforderungen** müssen die IT-Bereiche (Infrastruktur, Datenhaltung, Betrieb, Prozesse) erfüllen?
5. **Welche technischen, organisatorischen und personellen Maßnahmen** sind für die Gewährleistung von IT-Compliance erforderlich?

**Praxisbeispiele (Folien 42–44):** CRM-Einführung → DSGVO · Serverentsorgung → Elektroaltgeräteverordnung · Entwicklungstools → Lizenzbestand

Quelle: [[ITPM - IT-Projekt-Compliance]]

---

## Anwendung

Welche sechs QM-Leitfragen helfen, das richtige Maß an Qualitätssicherung festzulegen?

?

**Sechs QM-Leitfragen (Folie 15):**

| # | Frage | Ziel |
|---|---|---|
| 1 | Was sind die **Erfolgskriterien** für unser Projekt? | Identifikation der Qualitätsziele |
| 2 | **Wie gut** soll unser IT-Projekt werden? | Definition der Qualitätsanforderungen |
| 3 | Was sind die **Folgen**, wenn Qualitätsanforderungen nicht erreicht werden? | Identifikation der Risiken |
| 4 | Welche **Maßnahmen** werden gesetzt, um die Qualitätsanforderungen zu erfüllen? | Erste QS-Maßnahmen |
| 5 | Welche **Maßnahmen** werden gesetzt, um qualitätsbezogene Risiken zu reduzieren? | Risikospezifische QS |
| 6 | Wie viel ist uns die **Qualitätssicherung wert**? | Kosten und Aufwand der QS |

**Anwendungslogik:** Die Fragen bauen aufeinander auf: erst Ziele (1–2), dann Risiken (3), dann Maßnahmen (4–5), dann Ressourcenentscheidung (6). Fragen 3 und 5 sind direkt mit dem Risikomanagement verzahnt.

Quelle: [[ITPM - QM - Leitfragen]]

---

Was ist ein Compliance Management System (CMS), und welche sieben Punkte nennt die Checkliste der Vorlesung?

?

**Definition (Folie 15):** Ein CMS umfasst alle Maßnahmen und Prozesse, die ein Unternehmen einrichtet, um die Einhaltung der geltenden rechtlichen Rahmenbedingungen zu gewährleisten.

**Standardrahmen:** IDW PS 980 (im PDF als Referenz genannt)

**Compliance-Checkliste (Folie 23) – 7 Punkte:**
1. **Regelmäßige Analyse gefährdeter Bereiche**
2. **Vorleben** von Compliance-Regeln durch Geschäftsleitung und Führungskräfte
3. **Maßnahmenkatalog bei Verstößen**
4. **Schulung** der Mitarbeiter zum Thema Compliance
5. **Interne Richtlinien** mit Anweisungen und Maßnahmen für alle Mitarbeiter
6. **Technische Maßnahmen für den Datenschutz**
7. **Regelmäßige Buchhaltungsüberprüfung**

**Praxisbeispiele (Folie 25):** OMV Business Ethics Brochure · Siemens Business Conduct Guidelines

Quelle: [[ITPM - Compliance Management System]]

---

Was ist Projekt-Compliance, und welche zwei Aspekte umfasst sie?

?

**Definition (Folie 31):** Projekt-Compliance liegt vor, wenn alle Vorgaben, die dem Projekt extern auferlegt wurden bzw. intern als verbindlich akzeptiert werden, **nachweislich eingehalten** werden.

**Zwei Aspekte (Folie 32):**
1. **Compliance-Anforderungen für die spätere Nutzung** müssen bereits **im Projekt berücksichtigt** werden (z. B. DSGVO-Anforderungen beim Design eines Patientenportals)
2. **Die Projektarbeit selbst** unterliegt Compliance-Anforderungen (z. B. faire Lieferantenverträge, Schutz von Know-how)

**Nutzen der Projekt-Compliance:**
- Vermeidung von Nachteilen aus Gesetzes- und Vertragsverstößen
- Reduzierung von Projektrisiken (Nachvollziehbarkeit, Komplexitätsreduktion, Kostensenkung)
- Erhöhung der Projektqualität (Prozess- und Ergebnisqualität)

**Compliance als Verhalten:** Ehrlichkeit, Sorgfalt, Kompetenz; Einhaltung aller relevanten Regelwerke; faire Zusammenarbeit mit Lieferanten; Schutz von Projekt-Know-how.

**Non-Compliance-Beispiel (Folie 36):** Kölner U-Bahn-Bau 2010 – QS und Bauüberwachung versagten; Stabilisierungen für Grubenwände fehlten (offenbar gestohlen).

Quelle: [[ITPM - Projekt-Compliance]]

---

## Diskussion

Warum wird die Qualitätsformel als „Leistung / Erfordernisse = 1" formuliert – nicht als „> 1"?

?

**Bewusste Entscheidung der Vorlesung:** Das Gleichheitszeichen = 1 ist gewollt, nicht Zufall.

**Inhaltliche Begründung:**

1. **Qualität bedeutet Eignung, nicht Maximierung:** Ein Produkt, das mehr kann als gefordert, ist nicht besser – es ist teurer und ggf. schlechter nutzbar (Überingenieurswesen)
2. **Überqualität hat Kosten:** Mehr Leistung als nötig → höhere Entwicklungskosten, längere Laufzeiten, komplexere Wartung → Verletzung des Effizienzprinzips
3. **Erfordernisse vs. Anforderungen:** Die Formel verwendet bewusst „Erfordernisse" – was tatsächlich gebraucht wird, nicht was der Kunde explizit formuliert hat. Ein Wert > 1 würde bedeuten, mehr zu liefern als wirklich benötigt.
4. **Verbindung zum Teufelsquadrat:** Qualitätsoptimierung über das Ziel hinaus geht auf Kosten von Zeit, Kosten oder Umfang

**Diskussionspunkt:** Im Wettbewerb kann „> 1" ein Differenzierungsmerkmal sein (z. B. Begeisterungsfaktoren nach Kano). Aber aus PM-Sicht: Overdelivery ist kein Projekterfolg, wenn es nicht vereinbart war.

Quelle: [[ITPM - Qualität - Definition]]

---

Welche Compliance-Risiken entstehen, und welche der drei Folgenkategorien ist langfristig am teuersten?

?

**Ursachen von Compliance-Risiken (Folie 11):**
- **Aktives Tun** (verbotene Handlung)
- **Passives Unterlassen** (Pflicht nicht erfüllt)
- **Vorsätzlich** (bewusst, absichtlich)
- **Fahrlässig** (sorgfaltslos)

**Drei Folgenkategorien:**

| Kategorie | Beispiele |
|---|---|
| **Rechtliche Sanktionen** | Geldbußen, Freiheitsstrafen, Kündigungen, Lizenzverluste |
| **Finanzielle Verluste** | Schadenersatz, Forderungsabschreibungen, Verlust von Kreditsicherheiten |
| **Reputationsschäden** | Kundenverlust, keine neuen Kunden, Marktanteilsverlust |

**Welche ist langfristig am teuersten?**

**Reputationsschäden** – weil:
- Direkte Geldstrafen sind bezifferbar und einmalig
- Reputationsverlust ist kumulativ: Kunden verlassen das Unternehmen, Neukunden kommen nicht, Marktanteil sinkt dauerhaft
- Schwer reparierbar: Vertrauen lässt sich nicht durch PR allein wiederherstellen
- Im Health-IT-Kontext besonders kritisch: Patienten und Kostenträger wählen auf Vertrauensbasis

**Realbeispiel (Vorlesung):** VW Dieselskandal 2015 – direkte Strafen übersteigbar, aber Markenimage langfristig geschädigt.

Quelle: [[ITPM - Compliance - Risiken]]

---

Welche Risiken bestehen, wenn Quality Gates rein formell durchlaufen werden?

?

**Quality Gates** sind definierte Kontrollpunkte an Phasenübergängen. Nur bei Erfüllung vorab festgelegter Qualitätskriterien darf in die nächste Phase übergegangen werden. *(Inhalte im PDF nur als Übungsaufgabe angegeben; folgende Punkte teils Ergänzung außerhalb der Vorlesung)*

**Risiken „formeller" Quality Gates:**

1. **Falsches Sicherheitsgefühl:** Alle Gates „grün" → kein Problembewusstsein, obwohl Qualitätsmängel vorhanden
2. **Zu späte Fehlerentdeckung:** Fehler, die bei echten Gate-Prüfungen auffallen würden, kommen erst in Abnahme oder Betrieb hervor → Kostenmultiplikator (Fehler werden teurer je später gefunden)
3. **Politischer Druck:** Termine werden gewahrt, Qualität geopfert – Gate-Entscheider stimmen zu, um kein Projekthindernis zu sein
4. **Keine Verbindlichkeit:** Wenn Gates ohne Konsequenzen durchlaufen werden, verlieren sie ihre Schutzfunktion für nachfolgende Phasen
5. **Compliance-Problem:** In regulierten Umgebungen (Medizinprodukte, MDR) sind Gate-Freigaben oft dokumentationspflichtig – Fake-Freigaben sind Compliance-Verstöße

**Vergleich mit Sprint Review (agil):** Im agilen Kontext erfüllt der Sprint Review ähnliche Funktion – auch hier kann „Stempel-Review" entstehen, wenn der PO nicht wirklich prüft.

**Fazit:** Quality Gates haben nur Wert, wenn sie mit **echten Entscheidungsbefugnissen** ausgestattet sind und von **unabhängigen Prüfern** abgenommen werden.

Quelle: [[ITPM - Quality Gates]]

---

Wo liegt die Grenze zwischen Compliance und Ethik im Projektkontext?

?

**Compliance:** Einhaltung extern aufgelegter und intern akzeptierter Vorgaben – **messbar und nachweisbar**. Bezieht sich auf Gesetze, Normen, Verträge, Richtlinien.

**Ethik:** Geht **über das Recht hinaus** – normativer Rahmen, der auch dann gilt, wenn nichts verboten ist. Nicht immer messbar oder erzwingbar.

**Verhältnis:**
- Compliance = **Mindeststandard**: Das Recht setzt die untere Grenze
- Ethik = **freiwilliger Mehrwert**: Handlungen, die rechtlich erlaubt, aber moralisch fragwürdig sind

**Grauzonenbeispiele im Projektkontext:**
- Einen Subunternehmer zu beauftragen, der **legal**, aber unter schlechten Arbeitsbedingungen produziert → Compliance ok, Ethik fraglich
- Einen Kunden über technische Risiken **nicht aktiv informieren** (nicht lügen, aber schweigen) → Compliance ok (ggf.), Ethik fraglich
- **Pricing-to-win** (bewusst zu tief anbieten) → Legal, aber Frage der Projektintegrität

**Konsequenz für Projekt-Compliance (Folie 35):** Die Vorlesung formuliert Projekt-Compliance als Verhalten mit „Ehrlichkeit, Sorgfalt und Kompetenz" – das geht über reine Regelkonformität hinaus und berührt die ethische Dimension.

**Fazit:** Ein Projektleiter, der „nur" compliant ist, aber ethische Grundsätze verletzt, handelt im Sinne der Vorlesung nicht vollständig korrekt.

Quelle: [[ITPM - Compliance - Definition]], [[ITPM - Projekt-Compliance]]

---

Warum ist Projekt-Compliance präventiv, nicht reaktiv – und welche konkreten Projektkostenvorteile entstehen?

?

**Kernaussage der Vorlesung (Folie 33–34):** Der **Nutzen von Projekt-Compliance** liegt in der **Präventivfunktion** – Nachteile werden vermieden, bevor sie entstehen.

**Dreifacher Nutzen:**

**1. Vermeidung von Nachteilen:**
- Aus **Gesetzesverstößen** (Geldstrafen, Lizenzverluste)
- Aus **Vertragsverstößen** (Schadenersatz, Nacharbeit)

**2. Reduzierung von Projektrisiken:**
- Höhere **Nachvollziehbarkeit** → bessere Steuerbarkeit
- **Reduzierung von Komplexität** → weniger unvorhergesehene Ereignisse
- **Senkung von Projektkosten** (kein nachträgliches Reparieren)
- **Schutz von Unternehmensressourcen**

**3. Erhöhung der Projektqualität:**
- Steigerung der **Prozessqualität**
- Erhöhung der Qualität von **Projektergebnissen und -prozessen**

**Warum präventiv billiger?**
- Compliance-Nacharbeit nach Projektende ist exponentiell teurer (ähnlich dem Fehler-Kosten-Prinzip in der QS)
- Reputationsschäden und rechtliche Folgen sind kaum durch Nacharbeit reparierbar
- Im Health-IT-Kontext: Zulassungsprobleme (MDR, CE-Kennzeichnung) nach Fertigstellung kosten mehr als Integration von Anfang an

Quelle: [[ITPM - Projekt-Compliance]]
