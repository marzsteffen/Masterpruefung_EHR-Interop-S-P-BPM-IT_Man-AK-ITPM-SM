---
fach: ehr
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/ehr
---

# EHR - PF - Internationale Vergleichssysteme

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz behandelt internationale EHR-Systeme und -Programme: VistA (VA-EHR als Vorläufer), das US-amerikanische Meaningful Use Programm (HITECH Act, 3 Hauptkomponenten, 5 Ziele, Medicare/Medicaid-Anreize, CQM, USCDI, MU-Bilanz, MACRA/Pay for Performance) sowie den European Health Data Space (EHDS). Der Fokus liegt auf dem Überblick – die tiefen Stage-1/2/3-Details sind in [[EHR - PF - Meaningful Use Stages]] ausgelagert.

## Verlinkte Konzepte

- [[EHR - EHDS - European Health Data Space]]
- [[EHR - VistA - Veterans Affairs EHR]]
- [[EHR - HITECH Act und ARRA 2009]]
- [[EHR - Meaningful Use - Definition und Ziele]]
- [[EHR - Meaningful Use - 3 Hauptkomponenten]]
- [[EHR - Medicare und Medicaid Incentives]]
- [[EHR - MACRA und Value Based Care]]
- [[EHR - Clinical Quality Measures CQM]]
- [[EHR - USCDI US Core Data for Interoperability]]
- [[EHR - MU Auswirkungen und Bilanz]]

---

## Karten

### Definition

Was ist der HITECH Act – in welchem Gesamtgesetz ist er eingebettet, welches Ziel verfolgt er, und welches Budget hatte er?
?
**HITECH** = Health Information Technology for Economic and Clinical Health Act. Eingebettet in den **ARRA** (American Reinvestment and Recovery Act, 2009) der Obama-Regierung. Primärziel ARRA: Jobs sichern, Infrastruktur, Bildung, Gesundheit, erneuerbare Energien fördern. Primärziel HITECH: Implementierung von EHR und unterstützender Technologie in den USA fördern – durch Anreize (Medicare/Medicaid) und spätere Payment Adjustments. Budget Health IT: ca. **36 Mrd. US$**. Verwaltende Behörden: **ONC** (Koordination, Zertifizierung) und **CMS** (Auszahlung der Anreize).

Welche fünf Ziele definiert Meaningful Use?
?
„Meaningful Use is using certified EHR technology to:" (1) **Improve quality, safety, efficiency, and reduce health disparities** – Qualität, Sicherheit, Effizienz, Ungleichheitsreduktion; (2) **Engage patients and families** in their health care – aktive Einbindung; (3) **Improve care coordination** – Verbesserung der Versorgungs­koordination zwischen Stellen; (4) **Improve population and public health** – Bevölkerungs- und öffentliche Gesundheit; (5) **Maintaining privacy and security** – durchgängige Anforderung, kein eigenständiges Ziel, sondern Rahmenbedingung. „Meaningful Use mandated in law to receive incentives."

Welche drei Hauptkomponenten von Meaningful Use legt der Recovery Act fest?
?
(1) **Use**: Verwendung zertifizierter EHR-Technologie in sinnvoller Weise – Beispiel: e-Prescribing, CPOE (computerisierte Bestellung). (2) **Exchange**: Nutzung zertifizierter EHR-Technologie für den elektronischen Austausch von Gesundheitsinformationen, um die Versorgungsqualität zu verbessern. (3) **Quality Reporting**: Übermittlung von **Clinical Quality Measures (CQM)** und anderen vom Secretary (HHS) festgelegten Maßen. Reifegrad-Logik: Stage 1 fokussiert auf Use, Stage 2 auf Exchange, Stage 3 auf Outcomes/Quality Reporting.

Was sind Clinical Quality Measures (CQM) – wie sind sie aufgebaut, und wie viele mussten unter MU Stage 1 berichtet werden?
?
CQMs sind **standardisierte, messbare Qualitätsindikatoren** der klinischen Versorgung. Aufbau: **Numerator** (Patienten, die das Qualitätsziel erreichen), **Denominator** (eligible Patienten der Zielpopulation), **Exclusions** (Ausschlüsse z. B. bei Kontraindikationen), **Stratification** (nach Alter, Geschlecht, Ethnizität), **Time Period** (Reporting-Zeitraum). Anforderungen MU Stage 1: Eligible Professionals – **6 CQMs** (3 aus Core/Alternate Core, 3 aus einem Set von 38); Hospitals – **15 CQMs**. CQMs bilden die dritte Hauptkomponente von MU und sind Grundlage des Übergangs zu Pay for Performance.

---

### Anwendung

Wie funktioniert das Medicare/Medicaid-Anreizsystem von Meaningful Use – welche Beträge stehen auf dem Spiel, und was passiert bei Nicht-Erfüllung?
?
**Positive Anreize** für Medicare/Medicaid-Provider, die zertifizierte EHRs meaningful nutzen: bis zu **44.000 US$** (Medicare) bzw. **63.000 US$** (Medicaid) pro Eligible Professional. Adoption 2011: 118.819 EPs erhielten Ø 18.600 US$; 2.320 Hospitals erhielten Ø 1,6 Mio. US$. Adoption 2012: 268.461 EPs erhielten Ø 15.200 US$. Gesamtausgaben 2011–2012: ca. 15,2 Mrd. US$ (42 % des Gesamtbudgets). **Negative Konsequenz** bei Nicht-Erfüllung nach 3 Jahren: **Payment Adjustments** – Reimbursement-Kürzung um −1 % (Jahr 1), −2 % (Jahr 2), −3 % (Jahr 3).

Welche Coding-Standards schreibt USCDI für Labortests, Medikamente, Diagnosen und Maßeinheiten vor?
?
USCDI (US Core Data for Interoperability) verknüpft seine Datenklassen mit folgenden Coding-Standards: **Labortests und -ergebnisse** → **LOINC** (Testidentität), UCUM (Einheiten); **Medikamente** → **RxNorm** (Medikamenten-Identität), NDC (Produktebene); **Diagnosen** → **ICD-10-CM** (primäres Billing-Coding), SNOMED CT (klinische Konzepte); **Maßeinheiten** → **UCUM** (Unified Code for Units of Measure). USCDI ist das technische Mindest-Datenset für US-EHR-Interoperabilität (ONC), technisch umgesetzt via HL7 FHIR „US Core"-Profile.

Was war VistA, welche Rolle spielte es vor 2009 – und wie entstand es historisch?
?
**VistA** (Veterans Health Information Systems and Technology Architecture) ist das EHR des **US Department of Veterans Affairs (VA)**, das vor dem Meaningful Use Programm das einzige große, voll integrierte EHR-System der USA war. Zahlen (Stand 2016): 8,7 Mio. Patienten, 1.700 Sites. Entstehungsgeschichte: Ende der 1970er entwickelten Programmierer in VA-Krankenhäusern **inoffiziell** (sog. „Hardhats") ein System für intersite-Informationsaustausch. Ursprünglicher Name: Decentralized Hospital Computer Program (DHCP). Ab 1981–1982 offiziell „legalisiert", später in VistA umbenannt. Seither **Public Domain** – auch international adaptiert (Mexiko, Jordanien, Indien). VistA ist das Paradebeispiel eines **bottom-up** entstandenen großen EHR-Systems.

Wie groß war die Diskrepanz zwischen MU-Anreiz und tatsächlichem Aufwand für einen Eligible Professional im ersten Implementierungsjahr?
?
Im ersten Implementierungsjahr eines EHR unter Meaningful Use entstanden für einen durchschnittlichen Eligible Professional folgende Kosten: **Produktivitätsverlust** ca. 20 % im ersten Monat; **erstjahres-EHR-bedingte Erlösverluste** ca. **11.200 US$**; **Lern- und Anschaffungs­zusatzkosten** ca. **10.325 US$** – zusammen ca. 21.500 US$ Gesamtaufwand. Der durchschnittliche Anreiz 2011 war Ø 18.600 US$ – also ein **Negativsaldo von ca. 2.900 US$** im ersten Jahr, der erst durch Folgejahres-Anreize und langfristige Produktivitätsgewinne ausgeglichen wurde.

---

### Diskussion

Anreize statt Mandat (HITECH/USA) vs. gesetzliches Mandat (ELGA/Österreich) – welche Trade-offs ergeben sich aus beiden Ansätzen?
?
**US-Ansatz (Anreiz)**: Passt zur föderalen Struktur der USA – zentrale Mandate politisch/rechtlich kaum durchsetzbar. Vorteil: Provider-Autonomie, Markt-Wettbewerb unter Vendoren (Epic, Cerner, Allscripts). Nachteil: ungleichmäßige Adoption (wer nicht Medicare/Medicaid abrechnet, hat keinen direkten Anreiz), marktgetriebene Fragmentierung, kein Interoperabilitäts-Mandat. **AT-Ansatz (gesetzliches Mandat)**: ELGA ist gesetzlich verankert, Anschluss für bestimmte Versorger verpflichtend. Vorteil: einheitliche Infrastruktur, schnellere Flächendeckung. Nachteil: politisches Risiko, Systemzwang ohne Marktdifferenzierung, Lücken bei nicht-verpflichteten Sektoren (Reha, Privatkliniken). Synthese: weder reines Mandat noch reine Anreize sind optimal – Hybrid-Modelle (vgl. EHDS mit Verpflichtungen + Finanzierung) sind wahrscheinlich zielführender.

Was ist MACRA, und was verändert der Schritt von „pay for service" zu „pay for performance" grundlegend?
?
**MACRA** (Medicare Access and CHIP Reauthorization Act, 2015) ist das Folgegesetz zu HITECH. Es konsolidiert Anreizprogramme (MU, PQRS, Value-Based Modifier) und forciert den Wandel von **Pay for Service** (Vergütung je erbrachter Leistung: Visite, Test, Eingriff) zu **Pay for Performance** (Vergütung nach Outcomes und Qualitätsergebnissen). Mechanismus: Provider erhalten Boni für gute CQM-Werte und Abschläge bei schlechten. **Unintended consequences**: (1) Risikoselektion – Provider bevorzugen gesunde, einfach zu behandelnde Patienten; (2) Code-Inflation – Outcomes werden durch Dokumentations-Tricks optimiert; (3) Vernachlässigung schwer messbarer Qualitäts­aspekte wie Empathie oder End-of-Life-Care. EHR wird durch MACRA noch kritischer: ohne strukturierte Daten kein CQM-Reporting, kein Bonus.

MU Bilanz: 82 % berichten verbesserte Clinical Decision-Making, 92 % bessere Kommunikation, 82 % weniger Medikationsfehler. Wie valide sind diese Zahlen – und welche Schattenseiten bleiben?
?
Die zitierten Zahlen sind **Self-Report** der EHR-nutzenden Provider – das schafft erheblichen **Bias**: Provider, die viel in ein System investiert haben, tendieren dazu, dessen Nutzen zu überschätzen (Sunk-Cost-Rationalisierung, Social-Desirability-Bias). Keine randomisierte Kontrollgruppe, keine objektiven Outcome-Metriken (Mortalität, Wiederaufnahmerate) auf Programmebene. **Schattenseiten** (in der Vorlesung angerissen): Note-Bloat (→ [[EHR - Progress Notes - EHR Lesbarkeitsproblem]]) – EHR-Dokumente werden durch Copy-Paste und Compliance-getriebene Checkbox-Dokumentation unlesbar; Provider-Burnout durch Click-Burden; Daten-Friedhöfe ohne Sekundärnutzungswert. Fazit: MU war ein Erfolg für EHR-Adoption; ob es ein Erfolg für Patientenversorgung war, ist wissenschaftlich umstritten.

Wie verhält sich der EHDS zum bestehenden ELGA-System – und was müsste an ELGA geändert werden, um EHDS-kompatibel zu sein?
?
**EHDS** (European Health Data Space) ist der supranationale EU-Rahmen für Primär- und Sekundärnutzung von Gesundheitsdaten. ELGA ist der österreichische nationale EHR – primär auf Versorgung (Primärnutzung) ausgerichtet. **Gemeinsamkeiten**: beide adressieren Patientenrechte (Zugang, Widerspruch) und organisationsübergreifenden Datenaustausch. **Anpassungsbedarf für EHDS-Compliance**: (1) **Format-Migration**: EHDS setzt auf FHIR (International Patient Summary als Kern-Use-Case), ELGA aktuell auf CDA → Formatanpassung nötig; (2) **Grenzüberschreitender Austausch**: ELGA-Infrastruktur ist national – Anbindung an MyHealth@EU erforderlich; (3) **Sekundärnutzung**: ELGA hat keine explizite Architektur für Forschungs-/Policy-Nutzung – HealthData@EU-Anbindung ist neu zu schaffen; (4) **Datenkategorien**: EHDS fordert u. a. Patient Summary, ePrescription, Laborbefunde, Bilder – teils in ELGA vorhanden, teils nicht standardisiert genug. [Details zu EHDS → [[EHR - EHDS - European Health Data Space]]]

VistA entstand „underground" von unten – was sind die Lessons Learned für moderne EHR-Einführungen?
?
VistA zeigt, dass ein **bottom-up, kliniker-getriebenes** System langfristig stabiler sein kann als top-down mandatierte Lösungen: Die „Hardhats" lösten ein reales Problem (Informationsaustausch zwischen VA-Standorten), was zu hoher Akzeptanz führte. **Lessons Learned**: (1) **Kliniker als Co-Designer** – Systeme, die Versorgungsprobleme der Nutzer lösen, werden adoptiert; (2) **Bottom-up-Entwicklung kann top-down übertreffen** – aber sie braucht irgendwann formale Governance (VistA wurde 1981 „legalisiert"); (3) **Public Domain als Modell** – Open-Source-EHRs (VistA, OpenMRS, OpenEHR-Implementierungen) reduzieren Vendor-Lock-in; (4) **Risiko**: ohne formale Governance entstehen Inkonsistenzen, fehlende Datenschutz-Frameworks, inkompatible Anpassungen. Kontrast: der Versuch der VA, VistA durch Cerner Millennium/Oracle Health zu ersetzen, ist mit massiven Kosten und Verzögerungen verbunden – ein Warnsignal für top-down-Migrations-Projekte.

---

## Mögliche Anschlussfragen des Prüfers

- Was unterscheidet ONC und CMS in ihren Rollen im Meaningful Use Programm?
- Warum ist e-Prescribing das Beispiel-Paradefall für „meaningful use" der ersten Stunde?
- Welche Provider sind vom US-Anreiz-System ausgeschlossen – und welche Konsequenzen hat das für Health Equity?
- Was sind MIPS und APMs unter MACRA?
- Welche Beziehung besteht zwischen USCDI und dem European Interoperability Framework?
- Hat Meaningful Use die Qualität der EHRs verbessert oder nur deren Verbreitung?
- Was bedeutet „Certified EHR Technology" – wer zertifiziert, und welche Mindestanforderungen bestehen?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
