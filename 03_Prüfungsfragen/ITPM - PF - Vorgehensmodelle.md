---
fach: itpm
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/vertiefung/itpm
---

# ITPM - PF - Vorgehensmodelle

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile
> - Niveau-Konvention: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Themenbereich umfasst klassische (Wasserfall, V-Modell, Spiralmodell, Phasenmodelle) und agile Vorgehensmodelle (Agiles Manifest, Scrum, XP, FDD, Crystal) sowie die Stacey Matrix als Entscheidungshilfe zur Methodenwahl. Die Notes stammen aus den Vorlesungen „Allgemeine Einführung", „Werkzeuge 01" und „Werkzeuge 02 – Agiles PM".

## Verlinkte Konzepte

- [[ITPM - Vorgehensmodelle - Klassisch vs Agile]]
- [[ITPM - Stacey Matrix - Komplexitätseinordnung]]
- [[ITPM - Klassisches PM - Definition]]
- [[ITPM - Klassisches PM - Vorteile und Nachteile]]
- [[ITPM - Wasserfallmodell]]
- [[ITPM - Spiralmodell - Boehm]]
- [[ITPM - V-Modell - Vorgehensmodell]]
- [[ITPM - Phasenmodelle]]
- [[ITPM - Agiles Manifest - 4 Werte]]
- [[ITPM - Agiles Manifest - 12 Grundprinzipien]]
- [[ITPM - Extreme Programming]]
- [[ITPM - Feature Driven Development]]
- [[ITPM - Crystal Family]]

---

## Karten

### Definition

Was ist ein Vorgehensmodell laut Vorlesung, und welche zwei Modell-Familien unterscheidet die Vorlesung grundsätzlich?
?
Ein Vorgehensmodell ist ein „Prozess der gestaltenden Produktion in verschiedene, strukturierte Abschnitte, denen wiederum entsprechende Methoden und Techniken der Organisation zugeordnet sind" (Folie 66). Zwei Familien: **Klassisch** – sequenziell, plan-getrieben, umfangreiche Vorabplanung, Ergebnis erst am Projektende verfügbar, Kunden-Feedback spät. **Agil** – iterativ-inkrementell, leichtgewichtig, flexibler Umfang, kontinuierliches Kunden-Feedback. Die Vorlesung betont: Es gibt kein „Richtig" oder „Falsch" – jedes Projekt muss individuell betrachtet werden.

Wann, wo und von wem wurde das Agile Manifest verfasst? Nennen Sie die vier Werte.
?
2001, Snowbird (Utah), 17 Softwareentwickler und IT-Projektmanager. Vier Werte: (1) **Menschen und Interaktionen** über Prozesse und Werkzeuge. (2) **Funktionierende Software** über umfassende Dokumentation. (3) **Zusammenarbeit mit dem Auftraggeber** über Vertragsverhandlungen. (4) **Reaktion auf Veränderungen** über das Einhalten eines starren Plans.

Welche zwei Achsen hat die Stacey Matrix und welche vier Bereiche entstehen?
?
Achsen: (1) **Klarheit der Anforderungen** (was wollen wir bauen?), (2) **Klarheit der Technik** (wie bauen wir es?). Vier Bereiche: **Einfach** (beide klar), **Kompliziert** (leichte Unklarheiten auf beiden Achsen, Kausalität noch vorhersehbar), **Komplex** (hohe Unsicherheit, Ereignisse haben unvorhersehbare Rückwirkungen), **Chaotisch** (extreme Unsicherheit, Erfolg kaum prognostizierbar).

Was kennzeichnet das Spiralmodell (Boehm), und welche vier Phasen enthält jeder Spiraldurchlauf?
?
Das Spiralmodell (Boehm 1986/1988) beschreibt als eines der ersten Modelle einen **iterativ-inkrementellen** Entwicklungsprozess. Charakteristisch ist die starke Betonung der **Risikoanalyse**, die einem Scheitern vorbeugt oder ein aussichtsloses Projekt frühzeitig beendet. Vier Phasen pro Durchlauf: (1) Klärung der Ziele, Anforderungen, Randbedingungen; (2) **Risikoanalyse**, Entwurf und Prototyp; (3) Implementierung und Anwendertest; (4) Auswertung der Iteration und Planung der nächsten bzw. **Projektstopp**.

Welche drei Gruppen von inhaltlichen Phasenmodellen nennt die Vorlesung, und was sind die zwei Blickwinkel der Phasenteilung?
?
Drei Gruppen: (1) **Grundlegende Prozessmodelle** (z. B. Wasserfall), (2) **Disziplinierte Modelle** (z. B. Spiralmodell, V-Modell), (3) **Agile Modelle** (z. B. Scrum, Crystal Clear). Zwei Blickwinkel: **Phasen des Projektinhalts** (wie das Produkt entsteht – Wasserfall, Scrum etc.) und **Phasen des Projektmanagements** (unabhängig vom Inhalt anfallende Phasen: Initiierung, Planung, Steuerung, Abschluss).

### Anwendung

Ein Krankenhaus plant die Migration auf eine neue Cloud-KIS-Plattform. Die Anforderungen der Pflegekräfte sind noch unklar, die Zieltechnologie für das Haus neu. In welchen Stacey-Bereich ordnen Sie ein, und was folgt für die Methodenwahl?
?
Hohe Unsicherheit auf beiden Achsen (Anforderungen unklar, Technik neu) → Bereich **„Komplex"**. Empfehlung: agiles oder iterativ-inkrementelles Vorgehen (Scrum oder Spiralmodell), um früh Feedback zu generieren und Risiken sichtbar zu machen. Strikt klassisches Vorgehen (Wasserfall) ist ungeeignet, weil Anforderungen am Projektanfang nicht vollständig festlegbar sind und späte Änderungen einen Domino-Effekt auslösen würden.

Welche zwei Achsen bestimmen in der Crystal Family die Methodenwahl, und was folgt aus größerem Team und höherer Kritikalität?
?
X-Achse: maximale Personenzahl im Projekt; Y-Achse: Projektkritikalität (z. B. Komfort, Geld, Lebensgefährdung). Größeres Team + höhere Kritikalität → **strengere Crystal-Variante** mit schwergewichtigeren Prozessen und mehr Kontrollmechanismen (z. B. Crystal Orange oder höher statt Crystal Clear).

Welche der 12 Grundprinzipien des Agilen Manifests setzt Scrum direkt um? Nennen Sie drei konkrete Mappings.
?
Beispiele: Prinzip 1+3 (schnelle, regelmäßige Lieferung → **Sprint-Inkrement** beim Sprint Review), Prinzip 4 (tägliche Abstimmung von Fachexperten und Entwicklern → **Daily Scrum**), Prinzip 12 (regelmäßige Reflexion und Verbesserung → **Sprint Retrospektive**), Prinzip 11 (selbstorganisierte Teams → **Development Team** in Scrum ist selbstorganisiert und entscheidet selbst über die Umsetzung).

### Diskussion

Vergleichen Sie Wasserfallmodell, Spiralmodell und V-Modell nach Linearität, Iterativität und Risikobehandlung.
?
**Wasserfall:** streng sequenziell, keine Iteration, keine explizite Risikobehandlung – Risiken werden durch sorgfältige Vorabplanung reduziert. **V-Modell:** ebenfalls sequenziell, aber mit expliziten, korrespondierenden Testphasen gegenüber den Entwicklungsphasen – strukturierte QS, aber keine Iteration. **Spiralmodell:** iterativ-inkrementell, enthält explizite Risikoanalyse-Phase in jedem Durchlauf und kann das Projekt nach jeder Iteration stoppen. Fazit: Spiralmodell ist am risikosensibelsten, V-Modell am testorientiertesten, Wasserfall am plan-verlässlichsten bei stabilen Anforderungen.

Vergleichen Sie klassisches und agiles Projektmanagement nach fünf Achsen.
?
| Achse | Klassisch | Agil |
|---|---|---|
| Planung | umfangreich, sequenziell, detailliert | leichtgewichtig, iterativ |
| Anforderungen | upfront, festgeschrieben | flexibel, gemeinsam entwickelt |
| Auslieferung | am Ende | inkrementell, kontinuierlich |
| Kunden-Feedback | spät (nach Abschluss) | früh und kontinuierlich |
| Umfang | fix (Änderungen = Change Request) | variabel |

Ist der zweite Wert des Agilen Manifests („Funktionierende Software über umfassende Dokumentation") mit den Anforderungen der Medizinproduktentwicklung (MDR, ISO 13485) vereinbar? Diskutieren Sie.
?
In der Medizinproduktentwicklung ist umfassende Dokumentation (Design History File, Risikoakte, Validierungsnachweise) regulatorisch zwingend – der zweite Wert gerät direkt in Konflikt. Lösungsansatz: agile Entwicklung mit angepasster Dokumentationsdisziplin (z. B. „just enough documentation", Dokumentations-Sprints). Wichtig: Das Manifest sagt nicht, dass Dokumentation wertlos ist – nur dass funktionierende Software **höher** gewichtet wird. [Ergänzung: Diese Nuancierung entstammt dem Originaltext auf agilemanifesto.org, nicht den Vorlesungsfolien.] Fazit: Agile Methoden sind in regulierten Kontexten einsetzbar, erfordern aber explizite Compliance-Maßnahmen.

Inwiefern ist das Spiralmodell ein konzeptueller Vorläufer agiler Methoden – und worin unterscheidet es sich von Scrum?
?
**Gemeinsamkeiten:** iterativ-inkrementell, Stakeholder-Einbezug nach jeder Iteration, mögliche Projektstopp-Entscheidung. **Unterschiede:** Spiralmodell hat keine fixen Sprint-Zeiten (Iterationslänge variabel), enthält eine explizite Risikoanalyse-Phase (Scrum hat keinen Risiko-Quadrant), ist nicht auf selbstorganisierte Teams fokussiert, und definiert keine Scrum-typischen Rollen (Product Owner, Scrum Master, Development Team). Scrum ist prozessual schlanker und team-zentrierter; das Spiralmodell ist risikozentrierter und management-geführter.

Welche agile Methode (Scrum, XP, FDD, Crystal) ist in stark regulierten Health-IT-Projekten konzeptuell am besten geeignet, und warum?
?
**Crystal** ist konzeptuell am nächsten, weil es eine explizite **Kritikalitäts-Achse** hat – Crystal-Varianten für hohe Kritikalität (Lebensgefährdung) enthalten schwergewichtigere Prozesse und Kontrollen. **Scrum** ist in der Praxis am verbreitetsten und lässt sich mit Compliance-Anforderungen kombinieren (z. B. Sprint-Deliverables als Dokumentationsstufen, Definition of Done mit Validierungsnachweis). **FDD** und **XP** sind weniger auf regulierte Kontexte ausgerichtet. Keine der Methoden ersetzt Validierungspflichten nach MDR oder ISO 13485 – sie müssen durch Compliance-Maßnahmen ergänzt werden.

---

## Mögliche Anschlussfragen des Prüfers

- Welche Stacey-Region entspricht am ehesten einem typischen eHealth-Implementierungsprojekt (z. B. ELGA-Anbindung), und wie begründen Sie das?
- Warum wird Royce oft als Erfinder des Wasserfalls bezeichnet, obwohl er das Modell ursprünglich kritisch beschrieb?
- Wie skalieren Scrum, XP und Crystal bei Teams mit über 50 Personen?
- Welche der 12 Grundprinzipien des Agilen Manifests stehen in regulierten Health-IT-Kontexten besonders unter Druck?
- Wo auf der Spezifitäts-Skala (Wasserfall–PRINCE2–Scrum–Agile) verorten Sie PRINCE2, und was folgt daraus für seine Flexibilität?
- Was bedeutet „chaotisch" in der Stacey Matrix – ist das noch projektfähig, oder ist klassisches Krisenmanagement gefragt?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
