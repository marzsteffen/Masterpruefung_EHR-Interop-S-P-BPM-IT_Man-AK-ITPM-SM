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

# SM - PF - ITIL Practices Detail

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Detail-Karten zu den acht im Foliensatz vertieften ITIL 4-Practices (ohne Service Level Management → siehe [[SM - PF - Service Level Management]]): pro Practice 2–3 Karten mit Fokus auf Details, Krankenhaus-Szenarien und prüfungsrelevante Abgrenzungen. Überblick-Karten befinden sich in [[SM - PF - ITIL Practices]], V3-Vergleich in [[SM - PF - ITIL V3 vs ITIL 4]]. Quelle: ITIL 4 Foundation Courseware (Axelos / Van Haren Publishing 2019).

## Verlinkte Konzepte

- [[SM - ITIL Practice - Incident Management]]
- [[SM - ITIL Practice - Problem Management]]
- [[SM - ITIL Practice - Change Enablement]]
- [[SM - ITIL Practice - Service Desk]]
- [[SM - ITIL Practice - Service Request Management]]
- [[SM - ITIL Practice - Monitoring and Event Management]]
- [[SM - ITIL Practice - Release Management]]
- [[SM - ITIL Practice - Service Configuration Management]]
- [[SM - Fallstudie - KI Incident Management]]
- [[SM - ITIL 4 - Management Practices Übersicht]]

---

## Karten

### Definition

### Incident Management – Detail

Warum gibt es in ITIL 4 separate Prozesse für Major Incidents und Informationssicherheits-Incidents?

?

**Major Incidents (Folie 92):** Haben besonders hohe geschäftliche Auswirkungen und erfordern ein temporäres Team mit Vertretern vieler Stakeholder (Service Provider, Lieferanten, Anwender usw.) — ggf. auch Einleitung von Notfallwiederherstellungsplänen. Die erhöhte Komplexität, breitere Kommunikationspflicht (Eskalation bis zur Leitung) und die höhere Koordinationsanforderung rechtfertigen einen eigenen Prozess.
**Informationssicherheits-Incidents:** Erfordern zusätzliche Aspekte, die im regulären Incident Management nicht abgebildet sind:
- Compliance-Anforderungen (z. B. DSGVO-Meldepflicht innerhalb 72h)
- Forensische Sicherung von Beweismitteln (Logfiles, Speicherabbilder)
- Vertraulichkeit des Vorfalls (keine breite Kommunikation, um Angreifer nicht zu warnen)
- Einbeziehung von Datenschutzbeauftragtem und ggf. Behörden.

---

Wie werden Incidents priorisiert, und welche Rolle spielen Ziellösungszeiten?

?

**Priorisierung (Folie 92):** Incidents werden auf Basis einer **vereinbarten Klassifizierung** priorisiert — so dass Incidents mit den **höchsten geschäftlichen Auswirkungen** zuerst gelöst werden. Die Klassifizierung legt Kategorien und deren Prioritätsstufen fest (z. B. kritisch / hoch / mittel / niedrig).
**Ziellösungszeiten:** Werden **vereinbart, dokumentiert und kommuniziert**, um sicherzustellen, dass die Erwartungen von Kunden und Anwendern realistisch sind. Unrealistische Ziellösungszeiten führen zu Unzufriedenheit, auch wenn Incidents technisch gut bearbeitet werden.
**UX-Auswirkung:** Incident Management kann erhebliche Auswirkungen auf die Kunden- und Anwenderzufriedenheit und die Wahrnehmung des Service Providers haben — jeder Incident muss erfasst und innerhalb des vereinbarten Zeitfensters gelöst werden.

---

### Problem Management – Detail

Was passiert in Phase 3 „Fehlersteuerung (Error Control)" des Problem Managements im Detail?

?

**Error Control (Folie 98):** Managt Known Errors — also Probleme, bei denen die anfängliche Analyse abgeschlossen und fehlerhafte Komponenten identifiziert wurden.
**Aktivitäten:**
- Identifizierung möglicher **dauerhafter Lösungen** — führt ggf. zu einem **Change Request** für die Implementierung (aber nur, wenn im Hinblick auf Kosten, Risiken und Nutzen gerechtfertigt).
- **Regelmäßige Neubewertung** des Status von nicht behobenen Known Errors: allgemeine Auswirkungen auf Kunden, Verfügbarkeit und Kosten dauerhafter Lösungen sowie Effektivität der Workarounds.
- **Workaround-Bewertung:** Jedes Mal, wenn ein Workaround verwendet wird, Bewertung seiner Effektivität — ggf. Verbesserung des Workarounds.
**Krankenhaus-Beispiel:** KIS-Lock-Known-Error: Workaround (DB-Query-Limit) wird bei jedem Auftreten bewertet. Nach 3 Monaten steigt die Häufigkeit → Kosten-Nutzen-Analyse → Change Request für permanenten DB-Index-Fix → Release.

---

Welche Schnittstellen hat Problem Management zu anderen ITIL 4-Practices?

?

Laut Folie 99 hat Problem Management relevante Schnittstellen zu:
- **Risk Management:** Problemmanagement-Aktivitäten können als konkreter Fall von Risk Management organisiert werden — Probleme werden als Risiken gemanagt (Wahrscheinlichkeit × Auswirkung).
- **Change Enablement:** Die Implementierung der Problemlösung erfolgt oft *außerhalb* des Problem Managements — über Change Request und Change Enablement.
- **Knowledge Management:** Output des Problem Managements (Workarounds, Known Errors) fließt in die Wissensdatenbank (KEDB) — KEDB ist Voraussetzung für schnelle Incident-Lösung.
- **Continual Improvement:** Problem-Management-Aktivitäten können Verbesserungsmöglichkeiten in allen vier Dimensionen des Service Managements identifizieren.

---

Warum muss nicht jedes Problem analysiert werden — und wie wird priorisiert?

?

**Begründung (Folie 97):** Probleme werden für die Analyse **auf Basis des Risikos** priorisiert, das sie darstellen — und auf Basis der möglichen **Auswirkungen und Wahrscheinlichkeit** als Risiken gemanagt. Es kann sinnvoller sein, Probleme mit höchster Priorität zunächst zu klären.
**Praktische Konsequenz:** Ressourcen (Spezialisten-Know-how, Zeit) sind begrenzt. Ein Problem mit geringer Auswirkung und niedriger Wiederholungswahrscheinlichkeit belegt Kapazitäten, die für kritischere Probleme fehlen.
**Krankenhaus-Beispiel:** Sporadischer Druckerfehler auf Station 3 (Workaround: Neudruck) vs. wiederkehrende KIS-Performance-Probleme im OP — Letzteres hat eindeutig höhere Priorität. Druckerproblem bleibt Known Error mit Workaround, wird nicht aktiv analysiert.

---

### Change Enablement – Detail

Was ist eine Change Autorität, und warum muss sie je Change-Typ passend gewählt werden?

?

**Definition (Folie 87):** „Die Person oder Gruppe, die einen Change autorisiert, wird als eine Change Autorität bezeichnet." Alle Changes sollten von Personen bewertet werden, die in der Lage sind, die **Risiken und den erwarteten Nutzen** zu verstehen.
**Warum je Change-Typ passend (Folie 87):** „Es ist wichtig, dass jedem Change-Typ die richtige Change Autorität zugewiesen wird, damit das Change Enablement sowohl **effizient als auch effektiv** sein kann."
**Beispiele:**
- *Standard Change:* Keine zusätzliche Autorität nötig (vorautorisiert).
- *Normaler Change:* Change Advisory Board (CAB) oder definierter Change Manager.
- *Notfall Change:* Emergency CAB (ECAB) oder dedizierter Emergency Change Manager — kleiner, schnell erreichbarer Kreis.
Falsch zugeordnete Autorität: Standard-Change mit CAB-Prozess → bürokratisch, langsam. Notfall-Change mit vollem CAB → zu langsam für Notfall.

---

Wie wird der Change-Kalender vor und nach einer Change-Bereitstellung genutzt?

?

**Vor der Bereitstellung (Folie 88):**
- **Planung** von Changes unterstützen
- **Kommunikation** vereinfachen (Stakeholder wissen, wann Changes stattfinden)
- **Konflikte vermeiden** (z. B. zwei Major-Changes nicht gleichzeitig; Change nicht während Hochlastzeiten)
- **Ressourcen zuweisen** (Teams, Wartungsfenster)

**Nach der Bereitstellung:**
- Informationen bereitstellen, die für **Incident Management** und **Problem Management** benötigt werden (z. B. Incident kurz nach Change → Change Kalender prüfen: war ein Change der Auslöser?)
- Grundlage für **Verbesserungsplanung** (Continual Improvement): Welche Change-Typen führen häufig zu Incidents?)

---

### Anwendung

### Service Desk – Anwendung

Welche Auswirkungen hat die Service-Desk-Qualität auf die Wahrnehmung der gesamten IT-Abteilung im Krankenhaus?

?

**Laut Folie 100:** Der Service Desk hat **großen Einfluss auf die User Experience**. Als Single Point of Contact (SPOC) ist er die **erste und wiederkehrende Anlaufstelle** für alle Anwender.
**Konsequenz für Krankenhaus-IT:**
- Auch wenn 2nd-Level-Teams technisch einwandfrei arbeiten: Wenn der Service Desk langsam, unfreundlich oder inkompetent kommuniziert, ist das Gesamtbild der IT für Pflegekräfte und Ärzte negativ.
- Pflegekraft ruft an: KIS reagiert nicht → wenn Service Desk kalt, technisch oder nicht erreichbar ist → Frust landet auf der gesamten IT-Abteilung.
- **Service Desk als Markenbotschafter** der IT: Skills (Kommunikation, Empathie, Triage, technisches Grundverständnis) sind genauso wichtig wie der reine Lösungsprozess.

---

### Service Request Management – Anwendung

Nennen Sie die fünf Service-Request-Typen aus ITIL 4 mit Krankenhaus-Beispielen.

?

Laut Folie 105:
1. **Request für eine Servicebereitstellungsaktion:** Ersetzen der Tonerkartusche am Stationsdrucker; Generierung eines Entlassbriefs.
2. **Informationsanfrage:** „Wie erstelle ich einen Laborbefund-Export?" / „Wann ist das Wartungsfenster für das Archiv?"
3. **Request zur Bereitstellung einer Ressource oder eines Service:** Neue Pflegekraft benötigt ein Tablet; IT-Testteam benötigt virtuellen Server für App-Entwicklung.
4. **Request zum Gewähren von Zugriff:** Neue Ärztin benötigt PACS-Berechtigungen; Datei-/Ordner-Zugriff für neues Forschungsprojekt.
5. **Feedback, Lob und Beschwerden:** Lob für schnelle Entstörung; Beschwerde über neue KIS-Benutzeroberfläche.

---

Wie sollten Service Requests standardisiert und im Erwartungsmanagement gestaltet werden?

?

**Standardisierung und Automatisierung (Folie 104):**
- Service Requests und ihr Fulfillment so weit wie möglich **standardisieren und automatisieren** (z. B. Self-Service-Portal für Zugriffsanfragen).
- Richtlinien für Requests definieren, die **ohne zusätzliche Genehmigung** erfüllt werden können → Fulfillment optimieren.
- Verbesserungsmöglichkeiten identifizieren, um **kürzere Fulfillment-Zeiten** zu realisieren.

**Erwartungsmanagement (Folie 104):**
- Fulfillment-Zeiten **klar und realistisch kommunizieren** — basierend auf dem, was die Organisation realistischerweise liefern kann.
- Unrealistische Erwartungen (z. B. Zugangsdaten in 5 Minuten) führen zu Unzufriedenheit, auch wenn der Prozess korrekt läuft.
**Krankenhaus-Beispiel:** Self-Service-Portal: Pflegekraft beantragt Zugangsdaten → automatisiertes Workflow-System, Genehmigung durch Vorgesetzte per App → Zugangsdaten in 2h. Kommunizierte SLA: 4h. → Erwartung übertroffen.

---

### Diskussion

### Monitoring and Event Management – Diskussion

Was ist ein Event laut ITIL 4, welchen Scope hat die Practice, und wie löst ein Event einen Incident aus?

?

**Definition Event (Folie 80):** „Jede Statusänderung, die für das Management eines Service oder eines anderen Configuration Items (CI) von Bedeutung ist. Events werden normalerweise durch Benachrichtigungen erkannt, die von einem IT Service, CI oder Monitoring-Tool erstellt werden."
**Scope der Practice:** Identifiziert und priorisiert Events in den Bereichen:
- IT-Infrastruktur
- Services
- Geschäftsprozesse
- Informationssicherheit

**Event → Incident-Kette:**
1. CPU-Auslastung KIS-Server überschreitet 90 % (Schwellwert) → Monitoring-Tool erzeugt Event.
2. Event wird klassifiziert: „Warnung" (noch kein Ausfall) oder „Ausnahme" (Ausfall droht/eingetreten).
3. Bei „Ausnahme" → Eskalation an Incident Management.
4. Incident wird eröffnet; parallel läuft Monitoring weiter.

---

### Release Management – Diskussion

Wie verhält sich Release Management zu Deployment Management, und wo entsteht Spannung in DevOps-Umgebungen?

?

**Unterschied (Folie 81 + Note):**
- **Deployment Management (Technical Management Practice):** technisches Ausrollen von Software/CIs von einer Umgebung in eine andere (z. B. Test → Produktion).
- **Release Management:** das Zur-Verfügung-Stellen neuer/geänderter Services und Funktionen für Anwender — organisatorische Freigabe aus Nutzerperspektive.

**DevOps-Spannungsfeld:** In modernen CI/CD-Pipelines erfolgen Deployments mehrfach täglich automatisiert. Releases (Freigabe für Nutzer) sind davon entkoppelt — z. B. über **Feature-Toggles**: Software ist deployed, aber per Toggle für Endanwender noch nicht sichtbar. Das erlaubt häufige kleine Deployments bei kontrollierten, selteneren Releases.
**Implikation für ITSM:** ITIL 4 kann in DevOps-Umgebungen sinnvoll sein: Deployment = automatisiert; Release = koordiniert mit Change Enablement und Stakeholder-Kommunikation.

---

### Service Configuration Management – Diskussion

Worin unterscheidet sich Service Configuration Management (CMDB-Fokus) von IT Asset Management?

?

**Service Configuration Management (Folie 82):** Stellt sicher, dass genaue und zuverlässige Informationen über die **Konfiguration** von Services und CIs (Configuration Items) verfügbar sind — inklusive der **Beziehungen** zwischen CIs. Werkzeug: CMDB.
**IT Asset Management (Service Management Practice):** Fokus auf **Eigentum, Wert und Lifecycle** von IT-Assets — Einkauf, Lizenzierung, Abschreibung, Ausmusterung.

**Unterschied:**
| | Service Configuration Management | IT Asset Management |
|---|---|---|
| Fokus | Konfiguration + Beziehungen | Eigentum + Wert + Lifecycle |
| Werkzeug | CMDB | Asset-Register |
| Frage | „Wie ist CI X konfiguriert, und mit welchen anderen CIs ist es verbunden?" | „Wem gehört Asset X, wie viel ist es wert, wann wird es ersetzt?" |

Beide sind komplementär: Ein CI in der CMDB hat idealerweise einen Asset-Record im IT Asset Management.

---

Wie unterstützt die CMDB (Service Configuration Management) das Incident und Problem Management konkret?

?

**CMDB bei Incident Management:**
- Incident tritt auf → Analyst sucht betroffenes CI in der CMDB → sieht sofort: welche anderen Services hängen von diesem CI ab? Wie viele Anwender sind betroffen?
- Beispiel: KIS-Datenbankserver fällt aus → CMDB zeigt: Service KIS (primär), Reporting-Service (sekundär), HL7-Interface (tertiär) → alle drei Services sind im Incident-Ticket als betroffen zu dokumentieren → richtige Priorisierung.

**CMDB bei Problem Management:**
- Trendanalyse über Incidents mit demselben CI → Problem identifiziert.
- Known Error mit CI verknüpft → bei jedem neuen Incident dieses CI direkt Workaround vorschlagen.

**Herausforderung:** Die CMDB ist nur nützlich, wenn sie **aktuell** ist. Hoher Pflegeaufwand in dynamischen Umgebungen (Cloud, Container, häufige Changes) ist eine bekannte Schwäche in der Praxis.

---

### Vergleich / Integration

Welche drei Practices sind am engsten miteinander verzahnt, und warum?

?

**Incident Management, Problem Management und Change Enablement** bilden den zentralen operativen ITSM-Kern:

- **Incident → Problem:** Wiederkehrende Incidents lösen Problem-Identifizierung aus; Problem Management liefert Workarounds, die Incident Management nutzt (KEDB).
- **Problem → Change:** Error Control erzeugt Change Requests, wenn dauerhafte Lösungen gerechtfertigt sind.
- **Change → Incident:** Schlecht gesteuerte Changes sind eine der häufigsten Incident-Ursachen. Change-Kalender hilft, Changes als Incident-Auslöser zu identifizieren.

**Unterstützer-Practices:**
- **Monitoring and Event Management** → löst Incidents aus, bevor Anwender sie melden.
- **Service Configuration Management (CMDB)** → ermöglicht Auswirkungs-Analyse bei allen drei Practices.
- **Service Desk** → ist SPOC für Incident-Meldungen, erfasst Service Requests.

---

## Mögliche Anschlussfragen des Prüfers

- In welcher Phase des Problem Managements wird ein Change Request ausgelöst, und unter welcher Bedingung?
- Was passiert mit einem Workaround, wenn er regelmäßig genutzt wird?
- Wie unterscheidet sich ein Emergency CAB von einem regulären CAB?
- Was ist der Unterschied zwischen einem Service Request und einem Change Request?
- Wie entscheidet man, ob ein Incident ein Major Incident ist?
- Warum kann eine schlecht gepflegte CMDB zu langsameren Incident-Lösungen führen?
- Welche Rolle spielen Feature-Toggles beim Entkoppeln von Deployment und Release?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
