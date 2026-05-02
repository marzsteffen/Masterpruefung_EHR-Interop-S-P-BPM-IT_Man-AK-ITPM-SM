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

# ASP - PF - Business Continuity Management

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Business Continuity Management (BCM) aus ASP. Umfasst Motivation (vier Gründe, zwei Praxisbeispiele), den PDCA-basierten BCMS-Aufbau mit zwei parallelen DO-Strängen, die Business Impact Analyse (BIA) mit drei Phasen, die vier BIA-Kenngrößen (MTPD, RPO, RTO, MBCO), den Soll-Ist-Vergleich (RTO/RPO vs. RTA/RPA), die Abgrenzung von BIA und Risikoanalyse sowie die relevanten Normen (BSI 200-4, BSI 100-4, BSI 100-2, ISO 27005:2022). Alle Konzept-Notes stammen aus VL Business Continuity Management.

## Verlinkte Konzepte

- [[ASP - BCM - Motivation und Beispiele]]
- [[ASP - BCM - Managementsystem]]
- [[ASP - BCM - Business Impact Analyse]]
- [[ASP - BCM - BIA Kenngroessen]]
- [[ASP - BCM - Soll-Ist-Vergleich]]
- [[ASP - BCM - Risikoanalyse]]
- [[ASP - BCM - Normen]]

---

## Karten

### Definition

Frage: Welche vier Gründe für Business Continuity Management im Gesundheitswesen nennt die Vorlesung?

?

Antwort: Laut Folie 2 (VL Business Continuity Management):

1. **Patientenversorgung:** Gewährleistung der kontinuierlichen und zuverlässigen Versorgung von Patienten in Krisen.
2. **Reputations- und Vertrauensschutz:** Bewahrung des Vertrauens von Patienten und der Öffentlichkeit durch kontinuierliche Qualität und Zuverlässigkeit.
3. **Compliance-Anforderungen:** Einhaltung gesetzlicher Vorschriften und regulatorischer Standards.
4. **Risikomanagement:** Proaktive Minimierung von Risiken, um unerwünschte Auswirkungen auf die Gesundheitsdienste zu vermeiden.

**Hintergrund:** Das Gesundheitswesen ist hochgradig abhängig von ununterbrochenen Abläufen für Patientenversorgung und -sicherheit und exponiert gegenüber Naturkatastrophen, Pandemien, Cyberangriffen und technischen Ausfällen.

---

Frage: Was ist eine Business Impact Analyse, und welche drei Phasen hat sie?

?

Antwort: Laut Folien 7, 9–15, 18 (VL Business Continuity Management):

**Definition:** Strukturierte Analyse, die zeitkritische Geschäftsprozesse, Single-Points-of-Failure (SPoFs) und Ressourcenabhängigkeiten im Notbetrieb identifiziert. Wichtige Geschäftsprozesse sind nicht automatisch zeitkritisch.

**Drei Phasen:**

| Phase | Hauptaktivitäten | Ergebnis |
|---|---|---|
| **1. Voranalyse und Vorbereitung** | Geltungsbereich, BIA-Parameter (Schadenskategorien, Untragbarkeitsniveau), organisatorische Planung | klare Rahmen, Kriterien, Methodik |
| **2. Durchführung** | Datenerhebung, Festlegung von MTPD/RPO/RTO/MBCO je Prozess | Kenngrößen pro Geschäftsprozess |
| **3. Auswertung** | qualitätsgesicherte Zusammenfassung, SPoFs, Prozessabhängigkeiten | priorisierte Liste zeitkritischer Prozesse |

**Fünf Schadenskategorien (Folie 11):** Beeinträchtigung der Aufgabenerfüllung · Verstoß gegen Gesetze/Vorschriften/Verträge · Negative Innen- und Außenwirkung · Finanzielle Auswirkungen · Beeinträchtigung der persönlichen Unversehrtheit.

---

Frage: Definiere die vier BIA-Kenngrößen MTPD, RPO, RTO und MBCO. Was misst jede, und welche ist keine Zeit-Angabe?

?

Antwort: Laut Folie 15 und Folie 17 (VL Business Continuity Management):

| Kenngröße | Voller Name | Was misst sie? | Typ |
|---|---|---|---|
| **MTPD** | Maximum Tolerable Period of Disruption | Maximal tolerierbare Ausfallzeit eines Prozesses, bevor das Schadenspotenzial untragbar wird | Zeit |
| **RPO** | Recovery Point Objective | Wie weit darf der Datenstand vor einem Schadensereignis maximal zurückliegen? | Zeit (Datenverlust) |
| **RTO** | Recovery Time Objective | Wie schnell muss der Prozess nach einem Schadensereignis wieder auf Notbetriebsniveau verfügbar sein? | Zeit |
| **MBCO** | Minimum Business Continuity Objective | Auf welches Mindest-Leistungsniveau soll der Prozess im Notbetrieb gebracht werden? | **Niveau** (nicht Zeit) |

**Alle vier sind SOLL-Werte.** Die IST-Pendants sind RTA (Recovery Time Actual) und RPA (Recovery Point Actual). MBCO ist die einzige Kenngröße auf der y-Achse (Leistungsniveau), nicht auf der Zeitachse.

---

### Anwendung

Frage: Was zeigte der WannaCry-Angriff auf den NHS 2017 über Schwächen im BCM – und welche Maßnahmen hätten das verhindert?

?

Antwort: Laut Folie 3 (VL Business Continuity Management):

**Was passierte:** Ein Malware-Angriff (Ransomware) traf den britischen National Health Service – Operationen wurden abgesagt, Notfallzentren geschlossen, digitale Bildgebung und Patientenaktenzugriff eingeschränkt.

**Strukturelle Ursachen (laut Folie):**
- Veraltete Betriebssysteme und gekürzter Sicherheitssupport aufgrund Finanzierungsmangels.
- Fehlende IT-Sicherheitsüberlegungen bei der Digitalisierung.

**Bezug zu den vier BCM-Gründen:**
- *Patientenversorgung:* direkt getroffen (Operationsabsagen).
- *Risikomanagement:* keine proaktiven Maßnahmen gegen Cyberrisiken.
- *Compliance:* fehlende Patch-Pflicht trotz bekanntem Exploit.

**Verhindernde Maßnahmen (Folie 3):** Aktuell gehaltene Software, Schulungen zur IT-Sicherheit, angemessene Finanzierung für IT-Betrieb in Gesundheitssystemen.

---

Frage: Im Soll-Ist-Vergleich ergibt eine Übung: RTA = 8 h, RTO = 4 h, RPA = 6 h, RPO = 1 h. Was bedeutet das, und welche Konsequenzen sind zu ziehen?

?

Antwort: Laut Folie 19 (VL Business Continuity Management):

**Interpretation:**
- RTA (8 h) > RTO (4 h): Die tatsächliche Wiederanlaufzeit überschreitet die geforderte. → Anforderung **nicht erfüllt**.
- RPA (6 h) > RPO (1 h): Der tatsächliche Datenverlust übersteigt das zulässige Maximum. → Anforderung **nicht erfüllt**.

**Logik:** Wenn RTA ≤ RTO und RPA ≤ RPO, sind Anforderungen erfüllt. Wird eine Lücke aufgedeckt, sind zusätzliche Maßnahmen nötig.

**Mögliche Maßnahmen:**
- RTA > RTO → Recovery-Prozess optimieren (z. B. Hot-Standby statt Cold-Restore, schnellere Restore-Skripte).
- RPA > RPO → Backup-Frequenz erhöhen (z. B. stündliche statt tägliche Backups).

**Im PDCA-Kontext:** Der Soll-Ist-Vergleich ist Teil der CHECK-Phase und treibt die Korrektur- und Verbesserungsmaßnahmen an.

---

Frage: Wie ist der PDCA-Zyklus eines BCMS aufgebaut? Welche zwei Stränge laufen in der DO-Phase parallel?

?

Antwort: Laut Folien 5–6 (VL Business Continuity Management):

| PDCA-Phase | Hauptaktivitäten |
|---|---|
| **Initiierung** | Mandat der Leitung, Setup |
| **PLAN** | Analyse der erweiterten Rahmenbedingungen, Dokumentation, BC-Aufbauorganisation |
| **DO** | Zwei parallele Stränge (s. u.) |
| **CHECK** | Üben und Testen, Leistungsüberprüfung und Berichterstattung |
| **Korrektur und Verbesserung** | Aufrechterhaltung, Weiterentwicklung |

**Strang A – Aufbau und Befähigung der BAO (Business Continuity Aufbauorganisation):**
Aufbau der BAO · Detektion, Alarmierung, Eskalation · Sofortmaßnahmen · Notfallkommunikation · Störbetrieb und Deeskalation · Stabsarbeit.

**Strang B – Absicherung der Geschäftsprozesse:**
Voranalyse · BIA · Soll-Ist-Vergleich · BCM-Risikoanalyse · BC-Strategien und -Lösungen · Geschäftsfortführungsplan · Wiederanlauf- und Wiederherstellungsplan.

---

### Diskussion

Frage: Warum reicht eine BIA allein nicht aus, um BC-Strategien zu entwickeln – und warum reicht eine reine Risikoanalyse ebenfalls nicht aus?

?

Antwort: Aus den Notes zu BIA und Risikoanalyse (Folien 22–23, VL Business Continuity Management):

**BIA allein reicht nicht:**
- BIA fragt: „Was muss abgesichert werden?" – sie ist **wirkungsorientiert** und blendet vorhandene Maßnahmen aus (Worst-Case-Annahme).
- Sie sagt nichts über die *Wahrscheinlichkeit* von Bedrohungen. Ohne Eintrittswahrscheinlichkeit kann keine Priorisierung von Gegenmaßnahmen erfolgen.
- Ergebnis sind Zeitwerte (MTPD, RTO, RPO), aber keine Ursachenanalyse.

**Risikoanalyse allein reicht nicht:**
- Risikoanalyse fragt: „Wogegen muss abgesichert werden?" – sie ist **ursachenorientiert** und berücksichtigt vorhandene Maßnahmen.
- Sie sagt nichts über die *operative Schmerzgrenze* eines Prozessausfalls. Ein niedriger Risikowert schließt nicht aus, dass ein Prozessausfall sofort untragbar wird.

**Kombination nötig:** BIA liefert Zeitanforderungen (was ist wann kritisch?). Risikoanalyse liefert Eintrittswahrscheinlichkeiten (womit muss wann gerechnet werden?). Beide schneiden sich im „Impact".

---

Frage: Warum muss das Untragbarkeitsniveau in der BIA von der Institutionsleitung festgelegt werden – und nicht von der IT- oder BCM-Abteilung?

?

Antwort: Aus der Note zu BCM-BIA (Folie 11, VL Business Continuity Management):

Das **Untragbarkeitsniveau** bestimmt, ab welchem Schadenspotenzial ein Prozess als „zeitkritisch" gilt. Diese Entscheidung hat mehrere Dimensionen, die über technische Zuständigkeit hinausgehen:

- **Strategisch-politische Entscheidung:** Was ein Unternehmen als „untragbar" einstuft, ist eine Wertentscheidung – z. B. wie viel Reputationsschaden, wie viel finanzielle Einbuße oder wie viel Betriebsunterbrechung toleriert wird.
- **Ressourcen-Implikation:** Ein niedrig gesetztes Untragbarkeitsniveau bedeutet mehr zeitkritische Prozesse → mehr Investitionsbedarf in BCM-Maßnahmen. Das ist eine unternehmerische Abwägung.
- **Im Gesundheitswesen besonders kritisch:** Die Schadenskategorie „Beeinträchtigung der persönlichen Unversehrtheit" kann nur von der Leitung gegen andere Kategorien abgewogen werden, da es rechtliche und ethische Konsequenzen hat.

**Fazit:** Die IT-Abteilung kann die technischen Auswirkungen beschreiben; die Leitung muss entscheiden, was das Unternehmen tragen kann.

---

Frage: Warum sind die zwei DO-Stränge (BAO-Befähigung und Geschäftsprozess-Absicherung) im BCMS parallel statt sequenziell?

?

Antwort: Aus der Note zu BCM-Managementsystem (Folien 5–6, VL Business Continuity Management):

**Gegenseitige Abhängigkeit:**
- Die **BAO** (Business Continuity Aufbauorganisation) braucht die Ergebnisse der BIA, um Sofortmaßnahmen zu priorisieren und Stab-Strukturen sinnvoll zu besetzen.
- Die **BIA** braucht wiederum Stab-Strukturen und Ansprechpartner aus der BAO, um die Datenerhebung (Interviews, Workshops) organisatorisch durchzuführen.

**Praktische Konsequenz:**
- Eine rein sequenzielle Abfolge (erst BAO aufbauen, dann BIA) würde die BAO ohne inhaltliche Grundlage aufbauen.
- Umgekehrt (erst BIA, dann BAO) würde die BIA ohne organisatorisches Gerüst scheitern.

**Analogie:** Wie bei agilen Entwicklungsprojekten, in denen Architektur und Implementierung iterativ verzahnt sind – nicht erst vollständig geplant, dann vollständig umgesetzt.

---

### Vergleich

Frage: Vergleichen Sie BIA und Risikoanalyse: Leitfrage, Orientierung, Annahmen, Ergebnis – und was haben sie gemeinsam?

?

Antwort: Laut Folie 23 (VL Business Continuity Management):

| Aspekt | Business Impact Analyse | Risikoanalyse |
|---|---|---|
| **Leitfrage** | Was muss abgesichert werden? | Wogegen muss abgesichert werden? |
| **Bezug** | Ressourcen- oder prozessbezogen | Ressourcenbezogen |
| **Orientierung** | Wirkungsorientiert | Ursachenorientiert |
| **Annahme** | Blendet vorhandene Maßnahmen aus (Worst Case) | Berücksichtigt risikomindernde Maßnahmen |
| **Ergebnis** | Zeitwert (MTPD, RTO, RPO) | Risikowert |

**Schnittmenge:** Beide treffen sich im Begriff **„Impact"** – die Auswirkung eines Schadensereignisses ist sowohl für die BIA (wie lange untragbar?) als auch für die Risikoanalyse (wie schwer?) zentral.

---

Frage: Welche vier Normen nennt die Vorlesung für BCM und Risikomanagement – aktuell vs. älter, BSI vs. ISO?

?

Antwort: Laut Folien 7 und 22 (VL Business Continuity Management):

| Norm | Herausgeber | Geltungsbereich | Status |
|---|---|---|---|
| **BSI 200-4** | BSI (Deutschland) | Business Continuity Management | **aktuell** |
| **BSI 100-4** | BSI (Deutschland) | Notfallmanagement | älterer Standard (Vorgänger von BSI 200-4) |
| **BSI 100-2** | BSI (Deutschland) | IT-Grundschutz Vorgehensweise | älterer Standard |
| **ISO 27005:2022** | ISO/IEC | Informationssicherheits-Risikomanagement | **aktuell, Version 2022** |

**Normen-Inhalte (laut Vorlesung):**
- **BSI 200-4** definiert BCM-Risiko als „Risiken, die sich unmittelbar auf die Verfügbarkeit von zeitkritischen Ressourcen auswirken".
- **ISO 27005:2022** definiert Risiko als „effect of uncertainty on objectives"; Informationssicherheitsrisiken beziehen sich auf die Ausnutzung von Schwachstellen von Informationswerten.
- BSI 100-2 und BSI 100-4 werden nur als Kontext genannt, ohne Detailinhalt.

---

## Mögliche Anschlussfragen des Prüfers

- Welche der vier BCM-Gründe sind eHealth-spezifisch, welche universell?
- Wie hängt BCM mit dem Schutzziel Verfügbarkeit aus der CIA-Triade zusammen?
- Was sind typische Single-Points-of-Failure in einem Krankenhaus? (Zentrales KIS, Stromversorgung, Schlüsselpersonal.)
- Welche Kenngrößen bestimmen die Backup-Strategie, welche die Recovery-Strategie? (RPO → Backup-Frequenz; RTO → Recovery-Geschwindigkeit.)
- Was passiert, wenn RTO > MTPD gesetzt wird? (Vorgabe ist unerreichbar; der Prozess kommt vor Wiederanlauf zum Stillstand.)
- Was sind Vor- und Nachteile von BSI vs. ISO für BCM? (BSI: sehr detailliert, deutsch; ISO: international, abstrakter, global auditierbar.)
- Welche Lehren aus COVID-19 sollten Eingang in das BCM-Konzept eines Krankenhauses finden?
- Was ist der Unterschied zwischen BAO und normaler Aufbauorganisation? (BAO greift nur im Notfall als Krisen-Organisation mit Stab.)

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
