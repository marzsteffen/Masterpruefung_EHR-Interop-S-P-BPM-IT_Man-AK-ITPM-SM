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

# SM - PF - ITIL Practices

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Themenbereich-Karten zu den neun im Foliensatz vertieften ITIL 4-Practices (Monitoring/Event Management, Release Management, Service Configuration Management, Change Enablement, Incident Management, Problem Management, Service Desk, Service Level Management, Service Request Management). Überblick über alle 34 Practices und ihre Kategorisierung. Detail-Karten pro Practice und V3-Vergleich befinden sich in [[SM - PF - ITIL Practices Detail]] und [[SM - PF - ITIL V3 vs ITIL 4]]. Relevant für SM (Servicemanagement, FH JOANNEUM eHealth). Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Verlinkte Konzepte

- [[SM - ITIL 4 - Management Practices Übersicht]]
- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL Practice - Problem Management]]
- [[SM - ITIL Practice - Change Enablement]]
- [[SM - ITIL Practice - Service Desk]]
- [[SM - ITIL Practice - Service Request Management]]
- [[SM - ITIL Practice - Monitoring and Event Management]]
- [[SM - ITIL Practice - Release Management]]
- [[SM - ITIL Practice - Service Configuration Management]]
- [[SM - ITIL Practice - Service Level Management]]
- [[SM - ITIL 4 - Service Value System]]
- [[SM - ITIL 4 - Four Dimensions]]
- [[SM - Fallstudie - KI Incident Management]]

---

## Karten

### Definition

Was ist eine ITIL 4 Practice, und in welche drei Kategorien mit wie vielen Practices gliedert ITIL 4?

?

**Definition Practice (Folie 55):** „Eine Reihe von Organisationsressourcen, die zur Durchführung von Aufgaben oder zur Erreichung eines Ziels bestimmt sind." Eine Practice umfasst Menschen, Prozesse, Werkzeuge und Information — also alle vier Dimensionen.

**34 Practices in drei Kategorien:**
| Kategorie | Anzahl | Charakter |
|---|---|---|
| General Management Practices | 14 | Allgemeine Management-Themen, teils auch außerhalb der IT relevant |
| Service Management Practices | 17 | IT-/Service-spezifisch, viele V3-Pendants |
| Technical Management Practices | 3 | Technisch tiefe Practices (Deployment, Infrastruktur, Software-Entwicklung) |

---

Was ist der Zweck der Incident Management Practice, was ist ein Incident, und wer kann Incidents lösen?

?

**Zweck:** „Das Minimieren der negativen Auswirkung von Incidents, indem der normale Servicebetrieb schnellstmöglich wiederhergestellt wird."
**Definition Incident:** „Eine nicht geplante Unterbrechung eines Services oder eine Qualitätsminderung eines Service."
**Lösungs-Hierarchie:**
1. Anwender (Selbsthilfe)
2. Service Desk (1st Level)
3. Support-Team (eskaliert nach Kategorie)
4. Lieferanten/Partner
5. Temporäres Team (bei Major Incidents / besonders komplexen Incidents)
6. Notfallwiederherstellungspläne (in gravierenden Fällen)
Incidents werden priorisiert nach vereinbarter Klassifizierung — höchste geschäftliche Auswirkung zuerst.

---

Was ist der Zweck von Problem Management? Definieren Sie Problem, Workaround und Known Error. Welche drei Phasen hat die Practice?

?

**Zweck:** „Das Reduzieren der Eintrittswahrscheinlichkeit und der Auswirkungen von Incidents durch die Identifizierung tatsächlicher und potenzieller Ursachen von Incidents und das Management von Workarounds und Known Errors."
**Definitionen:**
- **Problem:** „Eine Ursache oder mögliche Ursache eines oder mehrerer Incidents."
- **Workaround:** „Eine Lösung, die die Auswirkungen von Incidents oder Problemen reduziert oder beseitigt, für die noch keine vollständige Lösung verfügbar ist."
- **Known Error:** „Ein Problem, das analysiert, aber noch nicht gelöst wurde."
**Drei Phasen:**
1. **Problemidentifizierung** (Trendanalysen, Muster erkennen)
2. **Problemsteuerung / Problem Control** (Analyse, Workarounds und Known Errors dokumentieren)
3. **Fehlersteuerung / Error Control** (Known Errors managen, dauerhafte Lösungen und ggf. Change Request)

---

Was ist der Zweck von Change Enablement, was ist ein Change, und welche drei Change-Arten gibt es?

?

**Zweck:** „Die Maximierung der Anzahl erfolgreicher Service- und Produktänderungen durch das Sicherstellen, dass Risiken richtig bewertet wurden, die Genehmigung von Changes und die Verwaltung des Change-Kalenders."
**Definition Change:** „Das Hinzufügen, Modifizieren oder Entfernen eines Elements, das direkte oder indirekte Auswirkungen auf Services haben könnte."
**Drei Change-Arten:**
| Art | Beschreibung |
|---|---|
| **Standard** | Vorautorisiert, geringes Risiko, wohlverstanden, keine zusätzliche Autorisierung nötig |
| **Normal** | Standardprozess: Change Request → Risikobewertung → Autorisierung durch Change Autorität |
| **Notfall** | Schnellstmöglich umsetzen; beschleunigter Bewertungs- und Autorisierungsprozess |

---

Was ist der Zweck der Service Desk Practice, und welche Rolle hat der Service Desk im Verhältnis zu den Anwendern?

?

**Zweck (Folie 100):** Der Service Desk
- erfasst Incidents und Service Requests
- ist der **Single Point of Contact (SPOC)** zwischen Service Provider und allen Anwendern
- bietet einen klaren Weg für Anwender, Schwierigkeiten, Fragen und Requests zu melden
- klassifiziert, weist zu, beantwortet und eskaliert
- hat **großen Einfluss auf die User Experience**

Der Service Desk prägt die Wahrnehmung des gesamten IT-Service-Providers — auch wenn 2nd-Level-Teams technisch einwandfrei arbeiten, entscheidet die Service-Desk-Qualität über das Anwender-Image der IT.

---

### Anwendung

Ordnen Sie diese fünf Practices den ITIL 4-Kategorien zu: Incident Management, Architecture Management, Software Development and Management, Service Desk, Risk Management.

?

| Practice | Kategorie |
|---|---|
| Incident Management | **Service Management** |
| Architecture Management | **General Management** |
| Software Development and Management | **Technical Management** |
| Service Desk | **Service Management** |
| Risk Management | **General Management** |

*Hinweis für Prüfung:* Die neun im Foliensatz vertieften Practices sind alle **Service Management Practices**. Practices ohne direktes V3-Pendant (z. B. Workforce and Talent Management, Architecture Management, Strategy Management) sind General Management Practices.

---

Ein KIS-Server fällt im OP-Betrieb aus. Welche vier ITIL 4-Practices greifen in welcher Reihenfolge?

?

1. **Monitoring and Event Management:** Monitoring-Tool erkennt Statusänderung (Event) → erzeugt Benachrichtigung → identifiziert potenziellen Incident.
2. **Service Desk:** Pflegekraft meldet via SPOC den Ausfall → Ticket wird erfasst, klassifiziert (KIS – Verfügbarkeit), priorisiert (kritisch / Major Incident).
3. **Incident Management:** Lösungs-Hierarchie greift — 1st Level, Eskalation DB-Team, ggf. temporäres Major-Incident-Team; Ziel: schnellstmögliche Wiederherstellung.
4. **Problem Management:** Nach Wiederherstellung → Trendanalyse (Wiederholungs-Muster?), Ursachenanalyse → ggf. Known Error → Change Request für dauerhafte Lösung via **Change Enablement**.

---

Unterscheiden Sie Service Request und Incident anhand von vier Krankenhaus-Beispielen.

?

**Service Request** = vereinbarte Standardaktion, Teil der normalen Servicebereitstellung:
- Pflegekraft beantragt KIS-Zugangsdaten für neue Mitarbeiterin *(Zugriff gewähren)*
- Stationsarzt fragt, wie der Entlassbrief-Generator gestartet wird *(Informationsanfrage)*
- IT-Team benötigt virtuellen Testserver für App-Entwicklung *(Ressource bereitstellen)*

**Incident** = nicht geplante Unterbrechung oder Qualitätsminderung:
- KIS stürzt ab und ist für 20 Minuten nicht erreichbar
- Laborsystem liefert fehlerhafte Werte (Qualitätsminderung)

**Schlüsselunterschied:** Service Request ist **erwartet und vereinbart**; Incident ist **ungeplant und unerwünscht**.

---

Wenden Sie die drei Change-Arten auf KIS-bezogene Änderungen im Krankenhaus an.

?

**Standard Change (vorautorisiert, geringes Risiko):**
Monatlicher Sicherheits-Patch der Office-Anwendungen — definiert, bekannt, risikoarm, keine Extra-Genehmigung.

**Normaler Change (Change Request → CAB → Genehmigung):**
KIS-Update von Version 7.4 auf 8.0 — bedeutende Änderung, Risikobewertung durch Change Autorität (CAB), Test-Phase in Testumgebung, geplantes Wartungsfenster.

**Notfall-Change (beschleunigte Bewertung):**
Kritische Zero-Day-Sicherheitslücke in KIS-Datenbankmodul wird aktiv ausgenutzt — sofortige Patches notwendig; Change-Kalender wird übergangen; beschleunigter Autorisierungsprozess (ggf. Change Autorität telefonisch / per E-Mail).

---

Welche ITIL 4-Practices sind im Krankenhaus-IT-Betrieb besonders kritisch, und welche werden laut Vorlesung oft unterschätzt?

?

**Besonders kritisch:**
- **Incident Management:** Klinische Systeme (KIS, PACS, Laborinformationssystem) müssen hochverfügbar sein — Incidents direkt patientenrelevant.
- **Information Security Management (General):** DSGVO, Krankenhaus-spezifische Datenschutzvorgaben, Ransomware-Risiken.
- **Service Continuity Management:** Katastrophenszenarien (Stromausfall, Ransomware-Angriff) erfordern Notfallpläne.
- **Change Enablement:** Unkontrollierte Changes sind häufige Incident-Ursache.

**Oft unterschätzt (laut Vorlesung):**
- **Workforce and Talent Management:** Fehlendes FHIR-/ITSM-Know-how in IT-Teams.
- **Knowledge Management:** Fehlende oder veraltete KEDB verzögert Incident-Lösung.
- **Architecture Management:** Brücke zu EAM (Enterprise Architecture Management), im Krankenhaus oft nicht mit ITSM verknüpft.

---

### Diskussion

Was ist der fundamentale Unterschied zwischen Incident Management und Problem Management?

?

| | Incident Management | Problem Management |
|---|---|---|
| **Ziel** | Negative Auswirkungen minimieren, Normalbetrieb wiederherstellen | Eintrittswahrscheinlichkeit und Auswirkungen künftiger Incidents reduzieren |
| **Objekt** | Incident (aktueller Vorfall) | Problem (Ursache von Incidents) |
| **Zeitperspektive** | Reaktiv, sofort | Proaktiv/reaktiv, mittel- bis langfristig |
| **Ergebnis** | Wiederherstellung | Workaround, Known Error, dauerhafte Lösung |
| **Output zu anderen Practices** | Known Errors → Problem Management; Events → Monitoring | Change Request → Change Enablement; Informationen → Knowledge Management |

**Klinisches Beispiel:** KIS-Lock = Incident (sofort beheben). Drei KIS-Locks in einem Monat = Problem (Ursache suchen, DB-Index fehlt = Known Error, Patch = Change).

---

Worin unterscheiden sich Change Enablement und Organizational Change Management? Warum ist die Abgrenzung prüfungsrelevant?

?

**Change Enablement (Folie 85):** Practice für Changes an IT-Produkten und -Services — technisch/fachlich: was wird geändert, wie wird es autorisiert, wie werden Risiken bewertet.
**Organizational Change Management (General Management Practice):** Bearbeitet die **mitarbeiterbezogenen Aspekte** von Changes — Akzeptanz, Kommunikation, Training, Widerstandsmanagement, Transformationsinitiativen.

**Prüfungsrelevanz:** Die Courseware betont explizit (Folie 85): „Es ist wichtig, Change Enablement von Organizational Change Management zu unterscheiden!" Ein KIS-Systemwechsel braucht beide: Change Enablement für die technische Einführung + OCM für Schulung und Akzeptanz der Pflegekräfte. Werden beide verwechselt, fehlt einer der wesentlichen Aspekte.

---

Wie unterscheiden sich Release Management und Deployment Management in ITIL 4?

?

**Release Management:** Zweck = „das Zur-Verfügung-Stellen neuer und geänderter Services und Funktionen" für Anwender. Fokus: Verfügbarkeit aus Nutzerperspektive.
**Deployment Management (Technical Management Practice):** Fokus: technisches Ausrollen von Softwarekomponenten in Umgebungen (z. B. von Test nach Produktion).

**Unterschied:** Deployment ist der technische Akt; Release ist die organisatorische Freigabe für Anwender. In DevOps-Umgebungen können Deploys häufig sein (mehrmals täglich per CI/CD), während Releases seltener und koordiniert erfolgen — z. B. über Feature-Toggles: deployed, aber noch nicht released.

---

Beschreiben Sie die Prozesskette: Event → Incident → Problem → Change. Welche Practices sind beteiligt?

?

1. **Monitoring and Event Management:** Monitoring-Tool erkennt Statusänderung eines CI → Event. Wenn Event auf potenziellen Fehler hindeutet → Eskalation an Incident Management.
2. **Incident Management:** Incident wird erfasst, klassifiziert, priorisiert → Lösungs-Hierarchie → Wiederherstellung. Parallele Nutzung der **Service Desk** Practice (SPOC).
3. **Problem Management — Problemidentifizierung:** Trendanalyse zeigt wiederkehrende Incidents gleicher Kategorie → Problem identifiziert. Ursachenanalyse → Workaround und Known Error dokumentiert.
4. **Problem Management — Error Control:** Kosten-Risiko-Nutzen der dauerhaften Lösung gerechtfertigt → Change Request erstellt.
5. **Change Enablement:** Change Request → Bewertung → Autorisierung → Implementierung. **Release Management** stellt neue Version bereit. **Service Configuration Management** (CMDB) wird aktualisiert.
**Ergebnis:** Incident-Häufigkeit sinkt → Continual Improvement Modell misst und bestätigt den Effekt.

---

Welche der 34 ITIL 4-Practices haben kein direktes ITIL V3-Pendant — und warum wurden sie neu eingeführt?

?

**Neue Practices in ITIL 4 (laut Note, kein V3-Pendant):**
- **Workforce and Talent Management** — in V3 nicht explizit; adressiert, dass ITSM-Skills gezielt entwickelt und gehalten werden müssen.
- **Architecture Management** — Brücke zu Enterprise Architecture; in V3 implizit in Strategy/Design.
- **Strategy Management** — in V3 als Lifecyclephase; in ITIL 4 explizite Practice.

**Begründung:** ITIL 4 erweitert den Scope von reinen IT-Prozessen auf allgemeine Management-Kompetenzen, die für Servicequalität maßgeblich sind. „Workforce and Talent Management" ist besonders im Gesundheitswesen relevant — der Fachkräftemangel bei FHIR/HL7-kompetenten IT-Mitarbeitern ist ein reales Problem.

*Hinweis: Die Note vermerkt, dass nur die 9 im Foliensatz vertieften Practices detailliert beschrieben sind — die anderen werden nur namentlich aufgeführt. Diese Karte basiert auf der Kategorisierungs-Note.*

---

## Mögliche Anschlussfragen des Prüfers

- Welche zwei eigenen Prozesse hat Incident Management für spezielle Szenarien? (Major Incidents, Informationssicherheits-Incidents)
- Muss jedes Problem analysiert werden? Warum nicht?
- Was ist eine Change Autorität, und warum muss sie je Change-Typ passend gewählt werden?
- Wie nutzt man den Change-Kalender nach einer Change-Bereitstellung (Post-Deployment)?
- Was ist der Unterschied zwischen Service Desk und Help Desk?
- Wie kann KI das Incident Management verbessern? (Siehe Fallstudie KI Incident Management)
- Was ist eine CMDB, und wie unterstützt sie Incident und Problem Management?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
