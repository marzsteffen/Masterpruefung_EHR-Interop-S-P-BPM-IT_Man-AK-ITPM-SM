---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/08 Businnes Continuity Management/08 Business Continuity Management.pdf
datum_vorlesung: 2024-11-20
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Business Continuity Management (BCM)

## Überblick

Achter Vorlesungsblock. Wechsel von angewandter Krypto zu organisatorischen Themen. **Business Continuity Management** stellt sicher, dass kritische Geschäftsprozesse auch bei Störungen (Cyberangriff, Pandemie, Stromausfall, Server-Ausfall, Naturkatastrophen) weiterlaufen oder schnell wiederherstellbar sind. Aufbau: Motivation und Beispiele, BCM-System (PDCA-Zyklus), Business Impact Analyse, Kenngrößen (RTO/RPO/MTPD/MBCO), Soll-Ist-Vergleich, BCM-Risikoanalyse.

## Lernziele (laut Vorlesung)

*Im PDF nicht als eigene Liste ausgewiesen.* Aus dem Aufbau: Notwendigkeit von BCM im Gesundheitswesen begründen; das BCM-System (PDCA) skizzieren; eine Business Impact Analyse durchführen können; die Kenngrößen RTO/RPO/MTPD/MBCO verstehen und auseinanderhalten; BIA und Risikoanalyse abgrenzen; relevante Normen (BSI 200-4, ISO 27005) benennen.

## Behandelte Konzepte

### Einstieg
- [[ASP - BCM - Motivation und Beispiele]]

### BCM-System
- [[ASP - BCM - Managementsystem]]

### Business Impact Analyse
- [[ASP - BCM - Business Impact Analyse]]
- [[ASP - BCM - BIA Kenngroessen]]

### Bewertung
- [[ASP - BCM - Soll-Ist-Vergleich]]
- [[ASP - BCM - Risikoanalyse]]

### Rahmenwerke
- [[ASP - BCM - Normen]]

## Roter Faden

Im Gesundheitswesen besteht eine **kritische Abhängigkeit** von ununterbrochenen Abläufen für Patientenversorgung und -sicherheit. Risiken: Naturkatastrophen, Pandemien, Cyberangriffe, technische Ausfälle. Vier Gründe für BCM: Patientenversorgung, Reputations- und Vertrauensschutz, Compliance-Anforderungen, Risikomanagement. Zwei reale Beispiele: WannaCry-Cyberangriff auf den NHS 2017 (Operationen abgesagt, Notfallzentren geschlossen, veraltete Betriebssysteme als Hauptursache), COVID-19-Pandemie 2022 (überlastete Intensivstationen, Notwendigkeit von Resilienz und besserer Vorbereitung).

Das **Business Continuity Managementsystem (BCMS)** läuft als PDCA-Zyklus:
- **Initiierung:** Aufsetzen.
- **PLAN:** Analyse erweiterter Rahmenbedingungen, Dokumentation, BC-Aufbauorganisation.
- **DO:** Umsetzung in zwei Strängen – Aufbau/Befähigung der BC-Aufbauorganisation (BAO) und Absicherung der Geschäftsprozesse.
- **CHECK:** Üben und Testen, Leistungsüberprüfung und Berichterstattung.
- **Korrektur und Verbesserung:** Aufrechterhaltung und Weiterentwicklung des BCMS.

Innerhalb der DO-Phase ist die **Business Impact Analyse (BIA)** das zentrale Werkzeug. Ziele: zeitkritische Geschäftsprozesse identifizieren, Single-Points-of-Failure aufdecken, Prozess- und Ressourcenabhängigkeiten im Notbetrieb ermitteln. Der BIA-Prozess hat drei Hauptphasen: **Voranalyse und Vorbereitung** (Festlegung des Geltungsbereichs, der BIA-Parameter, organisatorische Planung), **Durchführung** (Festlegung der Anforderungen für wirtschaftlichen Notbetrieb), **Auswertung** (qualitätsgesicherte Zusammenfassung der Ergebnisse).

Die **Kenngrößen** der BIA sind das mündliche Prüfungs-Filetstück:
- **MTPD** (Maximum Tolerable Period of Disruption): maximal tolerierbare Ausfallzeit.
- **RPO** (Recovery Point Objective): maximal zulässiger Datenverlust.
- **RTO** (Recovery Time Objective): geforderte Wiederanlaufzeit.
- **MBCO** (Minimum Business Continuity Objective): Notbetriebsniveau.
Im Soll-Ist-Vergleich kommen zwei weitere Werte hinzu: **RTA** (Recovery Time Actual, tatsächliche Wiederanlaufzeit) und **RPA** (Recovery Point Actual, tatsächlicher Datenverlust). RTO/RPO sind SOLL-Werte, RTA/RPA sind IST-Werte.

Die **BCM-Risikoanalyse** beantwortet die andere Frage als die BIA: Während die BIA klärt, *was* abgesichert werden muss (ressourcen- und prozessbezogen, wirkungsorientiert, blendet vorhandene Maßnahmen aus, Ergebnis: Zeitwerte), klärt die Risikoanalyse, *wogegen* abgesichert werden muss (ressourcenbezogen, ursachenorientiert, berücksichtigt vorhandene risikoreduzierende Maßnahmen, Ergebnis: Risikowert). Beide überlappen sich im Begriff „Impact". **BCM-Risiken** sind nach BSI 200-4 Risiken, die sich unmittelbar auf die Verfügbarkeit zeitkritischer Ressourcen auswirken. ISO 27005 (2022) definiert Risiko allgemein als „effect of uncertainty on objectives".

## Zentrale Aussagen / Take-aways

- **BCM-Gründe im Gesundheitswesen:** Patientenversorgung, Reputation, Compliance, Risikomanagement.
- **NHS-WannaCry 2017:** veraltete Betriebssysteme; Operationen abgesagt; Patientenakten unzugänglich.
- **BCMS = PDCA:** Initiierung → PLAN → DO (BAO + Geschäftsprozess-Absicherung) → CHECK → Korrektur/Verbesserung.
- **BIA-Ziele:** zeitkritische Prozesse, SPoFs, Abhängigkeiten im Notbetrieb.
- **BIA-Phasen:** Voranalyse, Durchführung, Auswertung.
- **Kenngrößen-Quartett:** MTPD (max. tolerierbare Ausfallzeit), RPO (max. Datenverlust), RTO (geforderte Wiederanlaufzeit), MBCO (Notbetriebsniveau).
- **Soll-Ist-Vergleich:** RTA + RPA als IST gegenüber RTO + RPO als SOLL.
- **BIA vs. Risikoanalyse:** BIA = was absichern (Wirkung); Risikoanalyse = wogegen absichern (Ursache). Beide schneiden sich im Impact.
- **Normen:** BSI 200-4 (BCM), BSI 100-4 (Notfallmanagement), BSI 100-2 (IT-Grundschutz), ISO 27005 (2022) für Risiko-Definitionen.

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Einfuehrung und Motivation]] (Verfügbarkeit als Schutzziel der CIA-Triade; Angriff „Nachricht unterdrücken")
- [[ASP - VL - Informationssicherheits-Risikomanagement]] (folgt – inhaltliche Fortsetzung der Risikoanalyse)
- [[ASP - Security Eigenschaften - Reliability]] (verlässlicher Betrieb)
- [[ASP - Angriff - Denial-of-Service]] (DoS als BCM-relevanter Angriff)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/08 Businnes Continuity Management/08 Business Continuity Management.pdf`
- Folienanzahl: 25
- Vortragender: Dr. Kevin Theuermann
- Datum laut Vorlesungsplan (Kapitel 01, Folie 4): 20.11.2024
- Ordnerschreibweise „Businnes" (statt „Business") ist im Vault vorgegeben; im PDF korrekt geschrieben.
