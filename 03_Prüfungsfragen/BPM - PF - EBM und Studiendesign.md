---
fach: bpm
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/bpm
---

# BPM - PF - EBM und Studiendesign

## Kontext

Kartenset zur mündlichen Masterprüfung BPM (eHealth, FH JOANNEUM). Themenbereich: Evidenzbasierte Medizin (EBM), Studiendesign und Endpunkte, Evidenz- und Empfehlungsklassen, Bias, Confounding und Kausalität, Validität – alles als Grundlage für leitlinienbasierte klinische Pfade.

## Verlinkte Konzepte

- [[BPM - EBM - Definition]]
- [[BPM - EBM - Ursachen einer Assoziation]]
- [[BPM - Studiendesign - RCT Goldstandard]]
- [[BPM - Studiendesign - Endpunkt]]
- [[BPM - Evidenzklassen - AHRQ]]
- [[BPM - Empfehlungsklassen - AHCPR]]
- [[BPM - Good Clinical Practice (GCP-KKP)]]
- [[BPM - Bias - Definition]]
- [[BPM - Confounder - Definition]]
- [[BPM - Confounder-Kontrolle - Methoden]]
- [[BPM - Kausalitaet vs Korrelation]]
- [[BPM - Validitaet - Interne vs Externe]]

---

## Karten

### Definition

Was ist Evidenzbasierte Medizin (EBM) laut Sackett, und aus welchen Komponenten besteht sie?
?
**Sackett-Definition** (*BMJ* 1996, 312:71–72):

> „Evidence based medicine is the conscientious, explicit, and judicious use of current best evidence in making decisions about the care of individual patients."

Deutsch (Vorlesungs-Fassung): EBM ist die **bewusste, ausdrückliche und verständliche Nutzung der jeweils besten Evidenz** bei Entscheidungen über die Versorgung individueller Patienten – Kombination der besten klinischen Erfahrung mit der besten verfügbaren Evidenz.

**Komponenten (Sackett-Trias):**
1. **Klinische Erfahrung** (clinical expertise)
2. **Externe Evidenz** (best available evidence from systematic research)
3. **Patientenpräferenzen** (Patient:innen-Werte und -Wünsche) → in der Vorlesung nicht ausgeführt; im Prüfungsgespräch erwähnen, nicht als Folienstoff ausgeben.

**Wichtige Abgrenzungen:** EBM ≠ „Kochrezept-Medizin" (Erfahrung + Patientenperspektive bleiben Teil); EBM ≠ Leitlinie (Leitlinie ist ein Werkzeug der EBM, nicht EBM selbst).

---

Nennen Sie die sieben Evidenzklassen der AHRQ-Systematik von der höchsten zur niedrigsten und geben Sie jeweils den zugehörigen Studientyp an.
?
Quelle: AHRQ (Agency for Healthcare Research and Quality, ehemals AHCPR).

| Klasse | Studientyp |
|---|---|
| **Ia** | Mindestens eine **Metaanalyse** auf Basis methodisch hochwertiger RCTs |
| **Ib** | Mindestens ein ausreichend großer, **methodisch hochwertiger RCT** |
| **IIa** | Mindestens eine hochwertige Studie **ohne Randomisierung** |
| **IIb** | Mindestens eine hochwertige Studie eines anderen Typs (**quasi-experimentell**) |
| **III** | Mehr als eine methodisch hochwertige **nicht-experimentelle** Studie (Vergleichs-, Korrelations-, Fall-Kontroll-Studien) |
| **IV** | **Expertenmeinungen**, Überzeugungen angesehener Autoritäten, beschreibende Studien |
| **(V)** | **Fallserie oder Einzel-Expertenmeinung** (in Klammern, nicht durchgängig verwendet) |

**Merke:** Evidenzklassen messen die Eignung für **Kausalitätsaussagen** – eine Fallstudie (III/IV) ist für „Warum ist der Effekt entstanden?" wertvoll, aber schwach für „Wie groß ist der Effekt?"

---

Was ist ein primärer Endpunkt, und warum muss er vor Studienbeginn festgelegt werden?
?
**Definition** (Folie 34):

> Als primärer Endpunkt wird das **primäre (erstrangige) Ziel der Studie** bezeichnet. Am primären Endpunkt kann festgestellt werden, ob die angewendeten Maßnahmen erfolgreich waren. Der Zusammenhang zwischen Intervention und Endpunkt ist der **Effekt**.

**Pflicht-Regel:** Die primären Endpunkte müssen **vor dem Beginn der Studie festgelegt werden**.

**Warum?** Nachträgliche Wahl erlaubt cherry-picking: Man sucht aus vielen gemessenen Größen diejenige heraus, die zufällig signifikant wurde → **Reporting Bias / p-Hacking** → Inflation der Effektgröße.

**Harte vs. weiche Endpunkte:**
- **Hart** (objektiv, bias-resistent): Tod, Rezidiv, Re-Operation – Folie: „The only thing you can't lie about is cash!" (Tod = härtester Endpunkt).
- **Weich** (subjektiver Spielraum): Zufriedenheit (VAS, Carlsson 1983), Lebensqualität (FLZ), domain-spezifische Scores (SCORAD).

**Messmethoden laut Vorlesung:** Beobachtung, Interview, Fragebogen, apparative Messungen, Daten aus BI/Routinedatensätzen.

---

### Anwendung

Eine retrospektive Studie zeigt: Patienten, die länger auf eine Hüftprothesen-OP warten, haben eine höhere postoperative Mortalität. Analysieren Sie diesen Befund anhand der vier möglichen Ursachen einer Assoziation.
?
Die vier möglichen Ursachen laut Vorlesung (Folien 7–8):

1. **Kausalität**: Die Verzögerung selbst erhöht das Mortalitätsrisiko (z. B. Bettlägerigkeit, Thrombose, Dekonditionierung). Möglich, aber nicht alleinige Erklärung.

2. **Bias**: Die retrospektive Datenerhebung könnte systematisch verzerrt sein (z. B. Selection Bias: Patienten, die schnell operiert wurden, hatten bessere Prognose; unterschiedliche Dokumentationsqualität).

3. **Confounding (Hauptverdacht)**: Alte und multimorbide Patienten müssen **erst stabilisiert werden** → Verzögerung entsteht *wegen* des Allgemeinzustands. Alter und Komorbiditäten sind gleichzeitig Treiber der Mortalität → typisches HTEP-Beispiel aus Folie 24. Confounder = **Alter und schlechter Allgemeinzustand**.

4. **Zufall**: Bei kleiner Stichprobe könnte das Ergebnis auch zufällig entstanden sein.

**Schlussfolgerung für Studiendesign:** Retrospektive Beobachtung reicht nicht. Zur Kausalitätsüberprüfung: RCT (ethisch schwierig), oder observational + **Risikoadjustierung** auf Alter, ASA, Komorbiditäten (= NSQIP-Ansatz).

---

Welche drei Qualitätsmerkmale machen den RCT zum Goldstandard, und was adressiert jedes Merkmal?
?
**Goldstandard**: Randomisierte, kontrollierte und doppelblinde Studie (Randomised Controlled Trial – RCT).

| Merkmal | Adressiert |
|---|---|
| **Kontrollgruppe** | Ermöglicht Effektaussage: Ohne Vergleichsmaßstab ist nicht klar, ob der Effekt auf die Intervention oder auf den natürlichen Verlauf zurückgeht. |
| **Randomisierung** | Kontrolliert **Confounding**: Zufällige Zuteilung verteilt bekannte und *unbekannte* Einflussfaktoren gleichmäßig. Einzige Methode, unbekannte Störgrößen auszuschalten. |
| **Verblindung** | Kontrolliert **Bias**: Schützt vor Verhaltensänderung durch Erwartung (Patient:in = einfach blind; Behandelnde = doppelblind; Auswertende = dreifach blind). |
| **Statistische Auswertung** | Kontrolliert **Zufall**: p-Werte, Konfidenzintervalle, ausreichende Fallzahl. |

**Empirische Belastung (Ioannidis et al. 2001):** Auswahl von 45 Themenbereichen mit je randomisierten und nicht-randomisierten Studien (408 Studien):
- Bei **60 %** der nicht-randomisierten Studien wurde der Effekt um ≥ **50 %** überschätzt.
- Bei **einem Drittel** Überschätzung um mehr als **200 %**.

→ Randomisierung ist methodisch unverzichtbar; nicht-randomisierte Studien liefern systematisch zu optimistische Ergebnisse.

---

Welche vier Methoden zur Kontrolle von Confoundern lehrt die Vorlesung? Erläutern Sie für jede Methode eine Stärke und eine Schwäche.
?
| Methode | Kern | Stärke | Schwäche |
|---|---|---|---|
| **Randomisierung** | Zufällige Zuteilung in RCT | Kontrolliert auch **unbekannte** Confounder | Ethisch/logistisch nicht immer möglich |
| **Restriktion** | Einschlusskriterien einengen, um Confounder auszuschalten | Einfach, transparent | **Externe Validität sinkt** deutlich; nur bekannte Confounder kontrollierbar; CAVE: nicht alle Confounder sind bekannt |
| **Matching** | Fälle und Kontrollen paarweise nach Confounder zuordnen | Einzelner Confounder vollständig ausschaltbar | **Overmatching**-Gefahr; Population entspricht nicht mehr der Realität |
| **Stratifikation** | Effekt in Schichten der Confounder-Variable analysieren (a posteriori) | Identifiziert auch Effektmodulation (Interaktion) | Unpraktikabel bei vielen Confoundern gleichzeitig |

**Kernregel:** Nur Randomisierung kontrolliert **unbekannte** Confounder – die anderen drei setzen Vorwissen voraus. In NSQIP-Beobachtungsstudien wird zusätzlich multivariate Regression als statistische Adjustierung eingesetzt (implizit, nicht explizit als 5. Methode benannt).

---

### Diskussion und Vergleich

„Bias creates an association that is not true, but confounder describes an association that is true, but potentially misleading." Erläutern Sie diesen Folie-17-Satz an je einem klinischen Beispiel.
?
**Kernunterschied:**
- **Bias** = die *Beobachtung selbst ist verzerrt* (die Daten stimmen nicht).
- **Confounder** = die Beobachtung ist *korrekt*, aber die kausale Interpretation ist irreführend.

**Bias-Beispiel (Detection Bias):** In einer offenen Studie wissen Untersucher:innen, welche Patient:innen die Intervention erhalten haben. Bei der Bewertung von Wundschmerz (subjektiver Endpunkt) urteilen sie milder bei der Interventionsgruppe → gemessener Unterschied existiert *in den Daten*, aber er spiegelt Bewerter-Erwartung wider, nicht die wahre Realität. **Gegenmaßnahme:** Verblindung der Auswertenden.

**Confounder-Beispiel (HTEP-Mortalität, Folie 24):** Patienten mit langer Wartezeit auf Hüft-OP haben höhere Mortalität. Die Beobachtung stimmt – beide Größen sind real gemessen. Aber die Ursache ist nicht die Wartezeit, sondern **Alter und Komorbiditäten** (Confounder): Sie verzögern die OP *und* erhöhen die Mortalität. Die Assoziation Wartezeit→Mortalität ist wahr, die Kausalitätsrichtung ist falsch. **Gegenmaßnahme:** Randomisierung oder Risikoadjustierung.

**Praktische Konsequenz:** Bias behebt man durch besseres Studiendesign (Verblindung, klare Definitionen); Confounding behebt man durch Randomisierung oder statistische Modellierung.

---

Erklären Sie den Unterschied zwischen interner und externer Validität und warum es einen fundamentalen Trade-off zwischen beiden gibt.
?
**Interne Validität** (Folie 21): Wie frei ist die Studie von systematischen Fehlern (Bias)? → „Stimmt das Ergebnis *innerhalb* der Studie?" Hauptbedrohung: Bias (Selection, Performance, Detection, Attrition, Reporting).

**Externe Validität** (Folie 31): Können die Ergebnisse auf andere Personen, Situationen, Zeitpunkte übertragen werden? → „Gilt das Ergebnis *außerhalb* der Studie?" Abhängig von Einschlusskriterien, Setting, Population.

**Trade-off:**

| Maßnahme | Interne Validität | Externe Validität |
|---|---|---|
| Enge Restriktion der Population | ↑ (weniger Confounder) | ↓ (gilt nur für Restringierte) |
| Heterogene, breite Population | ↓ (mehr Störgrößen) | ↑ (generalisierbar) |
| Strikt protokollierter RCT | ↑ (efficacy) | ↓ (Kliniksetting anders) |
| Pragmatische Alltagsstudie | ↓ | ↑ (effectiveness) |

**Relevanz für klinische Pfade:** Pfade basieren auf Leitlinien aus RCTs mit hoher *interner* Validität. Die eigentliche Implementierungsfrage ist jedoch: Gilt das für *unsere* Patientenpopulation in *unserem* Krankenhaus? → externe Validitätsfrage. Ein auf US-Universitätszentren basierter Pfad funktioniert in einem österreichischen Schwerpunktkrankenhaus möglicherweise anders.

---

Was sind Empfehlungsklassen (AHCPR), welche drei Grade gibt es, und wie unterscheidet sich GCP/KKP von Grad C?
?
**Empfehlungsklassen** übersetzen Evidenzklassen in Behandlungsempfehlungen in Leitlinien. Quelle: AHCPR (Agency for Health Care Policy and Research, heute AHRQ).

| Grad | Signalwort | Evidenzbasis |
|---|---|---|
| **A** | **„Soll"** | Evidenzklassen **Ia oder Ib** (mindestens ein hochwertiger RCT, direkt anwendbar) |
| **B** | **„Sollte"** | Evidenzklassen **IIa, IIb oder III** (gut durchgeführte Studien ohne Randomisierung, oder extrapolierte Ia-Evidenz) |
| **C** | **„Kann"** | Evidenzklasse **IV** (Expertenmeinungen, klinische Erfahrung; oder extrapolierte II/III) |

**GCP / KKP (Klinischer Konsensuspunkt)** (Folie 6): Wird vergeben, wenn:
- das Verfahren klinisch **allgemein üblich** ist,
- experimentelle Studien **fehlen, nicht möglich sind oder nicht angestrebt werden**,
- die Konsensusgruppe Übereinkunft erzielt hat.

**Abgrenzung GCP ↔ Grad C:**
- **Grad C** basiert auf *vorhandener* Expertenmeinung (Evidenzklasse IV), aber es gibt *irgendwelche* Belege.
- **GCP/KKP** greift, wenn keinerlei experimentelle Evidenz existiert und auch keine erreichbar ist – reiner Konsensus.

**Sprachliche Verbindlichkeit:** „Soll"-Empfehlungen (Grad A) dürfen ohne Dokumentation nicht ignoriert werden; Abweichungen erfordern klinische Begründung.

---

Welche drei Kriterien müssen laut Vorlesung für Kausalität erfüllt sein, und warum reicht Korrelation allein nicht aus?
?
**Drei Kausalitätskriterien** (Folie 11):

1. **Zusammenhang**: Ursache und Wirkung hängen statistisch zusammen (Korrelation als *notwendige*, aber *nicht hinreichende* Bedingung).
2. **Zeitlichkeit**: Die Ursache geht der Wirkung *rechtzeitig voraus* (A kommt vor B).
3. **Keine plausiblen Alternativerklärungen**: Bias, Confounding und Zufall als konkurrierende Erklärungen sind ausgeschlossen.

**Warum reicht Korrelation nicht?**

Eine Korrelation beschreibt nur eine *statistische Wechselbeziehung* – sie kann entstehen durch:
- **Confounder** (gemeinsame Drittvariable; Folie 16-Beispiel: mehr Feuerwehrleute bei größeren Bränden → höhere Brandschäden, aber die Feuerwehr verursacht sie nicht).
- **Reverse Causation** (Richtung umgekehrt; Folie 16: längere Krankenhausverweildauer → schlechterer Zustand, aber kausal: schwerer Zustand → lange Verweildauer).
- **Zufall** (in kleinen Stichproben).

**Praktische Konsequenz:** Für Behandlungsentscheidungen auf Pfaden brauchen wir Kausalität – Korrelation rechtfertigt keine Intervention, solange Confounding und Bias nicht ausgeschlossen sind.

---

Wann ist ein RCT nicht der geeignete Studientyp, und welche Alternativen gibt es?
?
Der RCT ist Goldstandard für **Kausalitätsfragen bei intervenier­baren Variablen** – er hat aber klare Grenzen:

**Ethische Nicht-Machbarkeit:** Man kann Patienten nicht randomisiert dem Rauchen, einer Infektion oder einer Behandlungsverzögerung zuteilen → **Kohorten- oder Fall-Kontroll-Studien** mit Risikoadjustierung.

**Chirurgische Innovationen mit Lernkurve:** Die Qualität hängt vom Übungsgrad ab; frühe Randomisierung benachteiligt die Lernkurven-Phase → **Registry-Daten (z. B. NSQIP)** mit Beobachtungsdesign und Risikoadjustierung.

**Seltene Erkrankungen:** Zu wenige Probanden für statistisch ausreichende Fallzahl → **Fallserien (Evidenz V)** oder internationale Register.

**Implementations- und Prozessfragen:** „Wie gut funktioniert ein klinischer Pfad in unserem Krankenhaus?" ist keine Wirksamkeits-, sondern eine Implementierungsfrage → **Process Mining, Beobachtungsstudien, qualitative Studien**.

**Pragmatische Studien (Effectiveness):** Wenn realweltliche Wirksamkeit (effectiveness) gefragt ist statt idealbedingter Wirksamkeit (efficacy), sind pragmatische Studien unter Alltagsbedingungen besser geeignet – aber mit niedrigerer interner Validität (Kompromiss mit externer Validität).

**Merke:** EBM schließt keine Studienform generell aus. Die Hierarchie beschreibt Eignung für Kausalitätsaussagen; andere Forschungsfragen erfordern andere Designs.

---

### Mögliche Anschlussfragen des Prüfers

- Wer hat den Begriff EBM geprägt, und in welchem Journal wurde die Definition 1996 publiziert?
- Was unterscheidet Klasse IIa von IIb in der AHRQ-Klassifikation?
- Welches Signalverb gehört zu welchem Empfehlungsgrad?
- Wie groß war die Effektüberschätzung bei nicht-randomisierten Studien laut Ioannidis 2001?
- Welche Bias-Typen nennt die Vorlesung explizit?
- Was ist ein Mediator, und warum darf er nicht als Confounder kontrolliert werden?
- Kann GCP/KKP in einer AWMF-S1-Leitlinie vorkommen?
- Was ist Overmatching beim Matching-Verfahren?

---

## Eigene Notizen

*(Hier eigene Ergänzungen und Unsicherheiten eintragen)*
