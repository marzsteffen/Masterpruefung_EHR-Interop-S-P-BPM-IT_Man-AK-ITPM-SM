---
typ: konzept
status: offen
faecher: [itm-ak, itpm, asp]
quellen:
  - "[[ITM-AK - Stufenbau der Rechtsordnung]]"
  - "[[ITM-AK - Rechtsakte der EU]]"
  - "[[ITM-AK - Prinzipien des EU-Rechts]]"
  - "[[ITM-AK - EU-Sekundärrechtsakte - DSGVO AI Act EHDS]]"
  - "[[ITM-AK - Vergaberecht]]"
  - "[[ITM-AK - Privatrecht vs Öffentliches Recht]]"
  - "[[ITM-AK - Verwaltungsakte - Verordnung und Bescheid]]"
  - "[[ITM-AK - VfGH und VwGH]]"
  - "[[ITM-AK - Vertragsrecht - Grundbegriffe]]"
  - "[[ITM-AK - Wettbewerbsrecht]]"
  - "[[ITM-AK - Urheberrecht und gewerblicher Rechtsschutz]]"
  - "[[ITPM - Compliance - Definition]]"
  - "[[ITPM - Compliance - Umfang und Themen]]"
  - "[[ITPM - Compliance - Risiken]]"
  - "[[ITPM - Compliance Management System]]"
  - "[[ITPM - CMS - Sieben Elemente]]"
  - "[[ITPM - ISO 37301 und Compliance Officer]]"
  - "[[ITPM - Compliance - Ethik]]"
  - "[[ITPM - Projekt-Compliance]]"
  - "[[ITPM - Projekt-Compliance - Prozess]]"
  - "[[ITPM - IT-Projekt-Compliance]]"
  - "[[ITPM - IT-Projekt-Compliance - Umfang]]"
  - "[[ASP - DSGVO - Grundsaetze]]"
  - "[[ASP - DSGVO - Privacy by Design]]"
  - "[[ASP - DSGVO - Privacy by Default]]"
  - "[[ASP - Security Eigenschaften - Privacy vs Confidentiality]]"
tags:
  - typ/konzept
  - status/offen
  - cross-fach
  - fach/vertiefung/itm-ak
  - fach/vertiefung/itpm
  - fach/allgemein/asp
---

# Cross - Compliance und Recht im eHealth-Kontext

> [!info] Kurzdefinition
> Drei Fächer adressieren die rechtlich-regulatorische Schicht aus drei verschiedenen Höhen. ITM-AK liefert das *Rechts-Fundament* (Stufenbau der Rechtsordnung, EU-Recht-Hierarchie, einzelne Rechtsgebiete von Vertrags- bis Vergaberecht). ITPM liefert das *Compliance-Management-System* (Definition, CMS mit 7 Elementen nach IDW PS 980, ISO 37301 mit Compliance-Officer, IT-Projekt-Compliance mit 5 Schlüsselfragen). ASP liefert die *konkrete DSGVO-Schicht* (vier Grundsätze, Privacy by Design, Privacy by Default). Die drei Sichten ergänzen sich: ITM-AK sagt *was* das Recht ist, ITPM sagt *wie* man es einhält, ASP sagt *welche* technischen Maßnahmen für Datenschutz konkret nötig sind.

## Sicht aus Fach ITM-AK

ITM-AK liefert das *Rechts-Fundament* — also welche Rechtsquellen es gibt, wie sie hierarchisch geordnet sind, welche Rechtsgebiete im IT-Management relevant sind.

**Stufenbau der Rechtsordnung** (siehe [[ITM-AK - Stufenbau der Rechtsordnung]], Folie 10):

Sieben-Stufen-Pyramide mit fallender Allgemeinheit:

| Stufe | Inhalt |
|---|---|
| 1 | EU-Recht (Vorrang vor nationalem Recht — EuGH Rs 11/70) |
| 2 | Grundprinzipien der Verfassung (Baugesetze) |
| 3 | Verfassung |
| 4 | Einfache Gesetze |
| 5 | Verordnungen (national) |
| 6 | Bescheide, Urteile, Verträge |
| 7 | Vollstreckung |

Höhere Stufen brechen niedrigere (lex superior derogat legi inferiori). EU-Recht hat Anwendungsvorrang vor nationalem Recht.

**Rechtsakte der EU** (siehe [[ITM-AK - Rechtsakte der EU]], Folie 56):

- **Primärrecht**: AEUV, Änderungsverträge (Nizza, Lissabon).
- **Sekundärrecht**:
  - **Verordnungen**: allgemeine Geltung, in allen Teilen unmittelbar in MS gültig (Beispiel: DSGVO, AI Act).
  - **Richtlinien**: Ziel verbindlich, Umsetzung in MS notwendig (Beispiel: Verbraucherrechterichtlinie).

**EU-Sekundärrechtsakte für eHealth** (siehe [[ITM-AK - EU-Sekundärrechtsakte - DSGVO AI Act EHDS]], Folie 59):

DSGVO (2016/679) / EU AI Act (2024/1689) / Verbraucherrechterichtlinie / EHDS-Verordnung. Patientendaten = besondere Kategorien personenbezogener Daten (Art 9 DSGVO). Spannungsfeld DSGVO ↔ EHDS (siehe Brücke 6 [[Cross - DSGVO im eHealth-Kontext]]).

**Rechtsgebiete (Cluster):**

- Privatrecht: Vertragsrecht, Gesellschaftsrecht, Umgründungsrecht, Wettbewerbsrecht, Urheberrecht.
- Öffentliches Recht: Verfassungsrecht und Verwaltungsrecht, Verwaltungsakte (Verordnung, Bescheid), Staatsaufbau Österreich, VfGH/VwGH, **Vergaberecht**.
- EU-Recht: EU-Institutionen, Rechtsakte, Prinzipien, Grundfreiheiten des Binnenmarkts.

**Vergaberecht** (siehe [[ITM-AK - Vergaberecht]], Folien 52–53):

- Bundesvergabegesetz (BVergG) für öffentliche Auftraggeber.
- Grundsätze: Wettbewerb / Transparenz / Gleichbehandlung / Verhältnismäßigkeit.
- Verfahren: Offen / Nichtoffen / Verhandlungs-Verfahren.
- Zuschlag: Bestbieter (Preis + Qualität) oder Billigstbieter (nur Preis).
- Diskussion (Folie): Spannung Innovation vs. Transparenz, Lock-in-Effekte bei IT-Folgeaufträgen.

## Sicht aus Fach ITPM

ITPM liefert das *Compliance-Management-System* — also wie man die Einhaltung von Recht und Vorgaben organisiert, betreibt und kontrolliert.

**Compliance-Definition** (siehe [[ITPM - Compliance - Definition]], Folien 7–8):

> „Compliance liegt vor, wenn alle Vorgaben, die dem Unternehmen extern auferlegt worden sind bzw. die das Unternehmen intern als verbindlich akzeptiert, **nachweislich eingehalten** werden."

Übersetzung: „Regelkonformität". Drei Komponenten: Vorgaben (extern + intern + Verträge) / Nachweisbarkeit / Verantwortung des Vorstands.

**Compliance Management System (CMS)** (siehe [[ITPM - Compliance Management System]], Folie 15):

> „Alle Maßnahmen und Prozesse, die ein Unternehmen einrichtet, um die Einhaltung der geltenden rechtlichen Rahmenbedingungen zu gewährleisten."

**Compliance-Checkliste** (Folie 23): Regelmäßige Analyse gefährdeter Bereiche / Vorleben durch Geschäftsleitung / Maßnahmenkatalog bei Verstößen / Schulung / Interne Richtlinien / Technische Datenschutzmaßnahmen / Buchhaltungs­prüfung.

**Reale Beispiele** (Folie 25): OMV Business Ethics Brochure, Siemens Business Conduct Guidelines.

**Sieben CMS-Elemente nach IDW PS 980** (siehe [[ITPM - CMS - Sieben Elemente]], Folien 16–22):

| # | Element | Inhalt |
|---|---|---|
| 1 | Compliance-Kultur | „tone at the top" — Grundeinstellungen Management + Aufsichtsorgan |
| 2 | Compliance-Ziele | festgelegt durch gesetzliche Vertreter, Grundlage für Risikobeurteilung |
| 3 | Compliance-Risiken | systematische Risikoerkennung, EW × Auswirkung |
| 4 | Compliance-Programm | Grundsätze + Maßnahmen zur Risiko-Begrenzung, Verstoß-Reaktion |
| 5 | Compliance-Organisation | Rollen, Verantwortlichkeiten, Aufbau- und Ablauforganisation, Ressourcen |
| 6 | Compliance-Kommunikation | Information der Mitarbeiter, Hinweis-Berichtswege |
| 7 | Compliance-Überwachung und -Verbesserung | Angemessenheit + Wirksamkeit, Dokumentation, Mängelbeseitigung |

Strategisches Fundament: Kultur + Ziele + Risiken. Operative Umsetzung: Programm + Organisation + Kommunikation. Schließt den Regelkreis: Überwachung + Verbesserung.

**ISO 37301 + Compliance-Officer** (siehe [[ITPM - ISO 37301 und Compliance Officer]], Folie 24):

- Internationale Norm mit Richtlinien für CMS-Aufbau und -Betrieb.
- ISO 37301:2021 ersetzt ISO 19600:2014 (Ergänzung außerhalb der Vorlesung).
- Compliance-Officer sorgt für rechtlich und ethisch korrektes Verhalten — als Rolle, kein eigenes CMS-Element.
- Compliance-Officer ≠ Datenschutzbeauftragter (DSB): DSB hat spezifischen Datenschutzfokus, CO ist breiter.

**IT-Projekt-Compliance** (siehe [[ITPM - IT-Projekt-Compliance]], Folien 39–44):

> „IT-Projekt-Compliance liegt vor, wenn alle Vorgaben, die einem IT-Projekt extern auferlegt worden sind bzw. die das Unternehmen für das IT-Projekt als verbindlich akzeptiert, nachweislich eingehalten werden."

Fünf Schlüsselfragen (Folie 40):

1. Welche **Rechtsnormen und sonstigen Regelwerke** sind für die IT relevant?
2. Welche **IT-gestützten Prozesse und Anwendungen** sind betroffen?
3. Welche **Risiken** resultieren aus mangelhafter IT-Compliance?
4. Welche **Compliance-Anforderungen** müssen die einzelnen IT-Bereiche erfüllen?
5. Welche **technischen, organisatorischen und personellen Maßnahmen** sind nötig?

Drei konkrete Beispiele (Folien 42–44):

| Projektkontext | Compliance-Anforderung |
|---|---|
| CRM-Einführung mit personenbezogenen Daten | Datenschutzgesetze (DSGVO) |
| Ersatz alter Server, Entsorgung | Elektroaltgeräteverordnung |
| Einsatz Softwareentwicklungstools | Lizenzbestand: ausreichende Anzahl |

**Compliance-Ethik** (siehe [[ITPM - Compliance - Ethik]]): Ethik geht über das Recht hinaus.

**Compliance-Risiken** (siehe [[ITPM - Compliance - Risiken]]): Compliance ist „spezielles Themenfeld des Risikomanagements".

## Sicht aus Fach ASP

ASP liefert die *konkrete DSGVO-Schicht* — also welche technisch-organisatorischen Maßnahmen aus dem Datenschutzrecht resultieren.

(Im Detail behandelt in Brücke 6 [[Cross - DSGVO im eHealth-Kontext]]. Hier nur Schlaglicht.)

**Vier DSGVO-Grundsätze** (laut ASP-Vorlesung, [[ASP - DSGVO - Grundsaetze]], Folie 16):

- Zweckbindung
- Datenminimierung
- Speicherbegrenzung
- Integrität und Vertraulichkeit

Quelltreue-Hinweis: ASP nennt diese **vier**, nicht die sieben aus Art. 5 DSGVO — die Note kennzeichnet das selbst.

**Privacy by Design** (siehe [[ASP - DSGVO - Privacy by Design]], Folie 17): DSGVO Art. 25 Abs. 1 — Datenschutz durch Technikgestaltung von Anfang an, mit Pseudonymisierung als Beispiel.

**Privacy by Default** (siehe [[ASP - DSGVO - Privacy by Default]], Folie 17): DSGVO Art. 25 Abs. 2 — datenschutzfreundliche Voreinstellungen.

**Privacy ≠ Confidentiality** (siehe [[ASP - Security Eigenschaften - Privacy vs Confidentiality]], Folie 15): wer darf zugreifen ≠ wofür darf zugegriffen werden. Verschlüsselung schützt Vertraulichkeit, nicht Privatsphäre — Privatsphäre wird über Zweckbindung gesichert.

## Gemeinsamkeiten

| Aussage | ITM-AK | ITPM | ASP |
|---|---|---|---|
| Rechtsnormen sind extern verbindlich | Stufenbau, EU-Recht | Compliance-Definition: „extern auferlegte Vorgaben" | DSGVO als Verordnung |
| Datenschutz ist eHealth-Pflicht | DSGVO als EU-Sekundärrecht | DSGVO als IT-Projekt-Compliance-Beispiel (CRM) | DSGVO-Cluster |
| Verantwortlichkeiten klar definiert | Vorstand/Geschäftsführung im UGB | Compliance-Definition: „Pflicht des Vorstandes/Geschäftsführers" | DSGVO Verantwortlicher (im Vault nicht detailliert) |
| Risikoorientierung | Risiken aus Recht (Schadenersatz, Strafrecht) | CMS-Element 3 (Compliance-Risiken) | (Datenschutz-Folgenabschätzung — im Vault nicht detailliert) |
| Schulung und Kultur als Erfolgsfaktor | (in Recht-Notes nicht direkt) | Checkliste: „Schulung der Mitarbeiter" + „tone at the top" | (im Vault nicht detailliert) |

## Unterschiede / Konflikte / unterschiedliche Schwerpunkte

**1. Drei Schichten — drei verschiedene Antwort-Hebel.**

- **ITM-AK = Was ist Recht?** Hierarchie der Rechtsquellen, einzelne Rechtsgebiete, EU-Rechtsstruktur.
- **ITPM = Wie hält man Recht ein?** CMS, sieben Elemente, ISO 37301, Compliance-Officer, IT-Projekt-Compliance mit fünf Schlüsselfragen.
- **ASP = Welche technischen Maßnahmen folgen aus DSGVO?** Vier Grundsätze, Privacy by Design, Privacy by Default.

In der Prüfung: Wer „rechtliche Pflichten beim KIS-Projekt" beantworten muss, antwortet aus *allen drei* Fächern. ITM-AK zeigt die Rechtsquelle (DSGVO als EU-Verordnung in Stufenbau-Stufe 1), ITPM zeigt das Management (CMS, fünf Schlüsselfragen für IT-Projekt-Compliance), ASP zeigt die konkreten Maßnahmen (Privacy by Design für CRM-Module).

**2. Vergaberecht — nur ITM-AK.**

ITPM-Compliance-Note thematisiert Vergaberecht **nicht**. Bei öffentlichen IT-Projekten in Krankenhäusern ist das aber zentral: BVergG, Bestbieter/Billigstbieter, offenes/nichtoffenes/Verhandlungs-Verfahren. Wer „IT-Projekt-Compliance bei Krankenhäusern in öffentlicher Trägerschaft" beantworten muss, kombiniert ITPM-IT-Projekt-Compliance (allgemein) mit ITM-AK-Vergaberecht (für die Beschaffungs-Schicht).

**3. CMS-Elemente vs. PMI-Risikomanagement-Prozess — strukturelle Verwandtschaft.**

ITPM-CMS-Note grenzt selbst ab: „Verbindung zum PMI-Risikomanagement-Prozess: identische Struktur (Identifikation → Analyse → Maßnahmen → Überwachung)."

Das ist die Cross-Verbindung zu Brücke 13 [[Cross - Risikomanagement zwei Sichten]]: Compliance-Management ist methodisch ein Risikomanagement-Spezialfall, mit Compliance-Risiken als Risiko-Klasse. Saubere Antwort: CMS und Risikomanagement-Prozess folgen demselben Plan-Do-Check-Act-Schema (siehe Brücke 7 [[Cross - PDCA-Zyklus quer durch die Disziplinen]]).

**4. Compliance-Officer ≠ Datenschutzbeauftragter (DSB).**

ITPM-ISO-37301-Note macht die Trennung explizit. ASP-Notes thematisieren den DSB nicht direkt; in der DSGVO ist der DSB aber explizit verankert (Art 37–39 DSGVO). Cross-Synthese: in einem Krankenhaus existieren typischerweise **beide Rollen** parallel — der DSB für Datenschutz-Spezifika, der CO für die breitere rechtliche Compliance (Vergaberecht, Vertragsrecht, Wettbewerbsrecht, Arbeitsrecht etc.).

**5. „Nachweislich" als ITPM-Schwerpunkt.**

ITPM-Compliance-Definition betont „**nachweislich** eingehalten" — das ist die Dokumentations-Pflicht. ITM-AK thematisiert die Dokumentation nicht direkt; ASP-Note zur DSGVO erwähnt sie auch nicht. Wer „warum Dokumentation?" beantwortet, antwortet aus ITPM. Diese Forderung ergibt sich juristisch aus der DSGVO-Rechenschaftspflicht (Art 5 Abs 2), die ASP aber explizit als „nicht in der Vorlesung" markiert hat — also für die Prüfung nur über ITPM-Compliance-Definition belegt.

**6. „Tone at the top" — ITPM-spezifisch.**

ITPM-CMS-Element 1 (Compliance-Kultur) führt das Konzept „tone at the top" ein. ITM-AK und ASP haben keine vergleichbare kulturelle Verankerung. In der Prüfung: kulturelle Voraussetzungen für funktionierende Compliance werden aus ITPM beantwortet.

**7. Stufenbau-Hierarchie und IT-Projekt-Compliance Schlüsselfrage 1.**

ITPM-IT-Projekt-Compliance-Schlüsselfrage 1: „Welche Rechtsnormen und sonstigen Regelwerke sind für die IT des Unternehmens relevant?" — das verlangt eine Antwort *aus dem Stufenbau* (ITM-AK). Konkret: EU-Recht (DSGVO, AI Act, EHDS), nationale Gesetze (KAKuG, ELGA-Gesetz, ÄrzteG), Verordnungen, interne Richtlinien.

Cross-Synthese: ITPM-Schlüsselfrage 1 wird operationalisiert durch ITM-AK-Stufenbau. Wer „welche Rechtsquellen sind relevant?" beantwortet, geht durch alle Stufen der ITM-AK-Pyramide und filtert die IT-relevanten heraus.

**8. EU-Recht als gemeinsamer Konvergenz-Punkt.**

Alle drei Fächer treffen sich bei EU-Recht:

- ITM-AK: EU-Recht an der Spitze des Stufenbaus, EU-Sekundärrechtsakte (DSGVO, AI Act, EHDS).
- ITPM: IT-Projekt-Compliance mit DSGVO als Beispiel (CRM-Einführung).
- ASP: DSGVO-Grundsätze, Privacy by Design / Default.

Aber: ITM-AK kennt die Hierarchie und Form (Verordnung direktwirkend, Richtlinie umsetzungsbedürftig), ITPM kennt die operative Anwendung (Schlüsselfragen, Maßnahmen), ASP kennt die technische Ausgestaltung (Pseudonymisierung, datenschutzfreundliche Voreinstellungen).

**9. AI Act und EHDS — nur in ITM-AK.**

ITM-AK-Note nennt EU AI Act (2024/1689) und EHDS-Verordnung explizit. ITPM thematisiert sie nicht; ASP thematisiert sie nicht. Wer „aktuelle EU-Regulierung für eHealth jenseits der DSGVO" beantworten muss, antwortet aus ITM-AK.

**10. Quellen-Konflikt: vier vs. sieben DSGVO-Grundsätze.**

ASP-Vorlesung listet vier Grundsätze (Zweckbindung / Datenminimierung / Speicherbegrenzung / Integrität-und-Vertraulichkeit). ITM-AK-Note nennt keine Grundsätze. Standard-DSGVO Art. 5 Abs. 1 hat sieben (zusätzlich Rechtmäßigkeit-Treu-und-Glauben-Transparenz, Richtigkeit, Rechenschaftspflicht). ASP-Note kennzeichnet das explizit als „nicht in der Vorlesung". Wer in der Prüfung die DSGVO-Grundsätze nennt, antwortet quelltreu mit den vier aus ASP.

## Synthese für die mündliche Prüfung

**Diskussions-Achse 1: „Welche rechtlichen Pflichten gelten für ein KIS-Projekt?"**

Saubere Drei-Wege-Antwort:

1. **Rechtsquellen-Frame** (ITM-AK): EU-Recht an der Spitze (DSGVO, AI Act, EHDS), nationale Gesetze (ELGA-Gesetz, KAKuG, ÄrzteG), Vergaberecht (BVergG bei öffentlichen Trägern), Vertragsrecht (Hersteller-Verträge).
2. **Compliance-Management-Frame** (ITPM): CMS einrichten mit sieben Elementen, ISO-37301-Compliance-Officer, IT-Projekt-Compliance mit fünf Schlüsselfragen.
3. **Schutzmaßnahmen-Frame** (ASP): Privacy by Design (DSGVO Art. 25 Abs. 1) bei der Architektur, Privacy by Default (Art. 25 Abs. 2) bei der Konfiguration, vier Grundsätze (Zweckbindung, Datenminimierung, Speicherbegrenzung, Integrität+Vertraulichkeit).

**Diskussions-Achse 2: „Was ist Compliance — und was nicht?"**

Antwort aus ITPM, mit ITM-AK-Stützung:

- ITPM: „Compliance ist Regelkonformität, nachweislich eingehalten." Nicht *nur* Recht, sondern auch interne Vorgaben und Verträge.
- ITPM-Abgrenzung: Compliance ≠ Ethik (Ethik geht über Recht hinaus); Compliance ist *spezielles Themenfeld* des Risikomanagements; Compliance ≠ QM (QM zielt auf Eignung, Compliance auf Regelkonformität).
- ITM-AK-Stützung: Recht = einer der Vorgaben-Quellen, eingebettet in den Stufenbau.

**Diskussions-Achse 3: „Welche sieben Elemente hat ein CMS?"**

Ausschließlich aus ITPM (IDW PS 980):

1. Compliance-Kultur (tone at the top)
2. Compliance-Ziele
3. Compliance-Risiken
4. Compliance-Programm (Maßnahmen)
5. Compliance-Organisation (Rollen + Ressourcen)
6. Compliance-Kommunikation (Berichtswege)
7. Compliance-Überwachung und -Verbesserung

Pointe: drei strategisch (Kultur/Ziele/Risiken) + drei operativ (Programm/Organisation/Kommunikation) + Regelkreisschluss (Überwachung). Strukturell identisch zum Risikomanagement-Prozess.

**Diskussions-Achse 4: „Wie hängen DSGVO-Pflichten und IT-Projekt-Compliance zusammen?"**

Cross-Verbindung von ASP und ITPM:

- ITPM-IT-Projekt-Compliance Schlüsselfrage 1: „Welche Rechtsnormen sind relevant?" — Antwort: DSGVO (ITM-AK-Stufenbau Stufe 1).
- ITPM-Schlüsselfrage 5: „Welche technischen, organisatorischen und personellen Maßnahmen?" — Antwort: Privacy by Design + Privacy by Default + technische Maßnahmen für die vier Grundsätze (ASP).
- Das CRM-Beispiel (Folie 42 ITPM) zeigt das konkret: CRM-Einführung mit personenbezogenen Daten triggert DSGVO-Pflichten.

**Diskussions-Achse 5: „Compliance-Officer oder Datenschutzbeauftragter?"**

Aus ITPM-ISO-37301-Note: beide Rollen, verschiedene Reichweite. Der DSB ist DSGVO-spezifisch (Art 37–39 DSGVO), der CO ist breiter (alle Compliance-Felder). In Krankenhäusern existieren typischerweise beide parallel.

**Diskussions-Achse 6: „Stufenbau und Vergaberecht im IT-Projekt."**

Spezifische ITM-AK-Anwendung im IT-Projekt-Kontext:

- Stufenbau lokalisiert Vergaberecht: BVergG ist einfaches Bundesgesetz (Stufe 4), basiert auf EU-Vergaberichtlinien (2014/24/EU usw., Stufe 1).
- IT-Projekt-Compliance bei öffentlichem Auftraggeber muss BVergG erfüllen (Wettbewerb, Transparenz, Gleichbehandlung, Verhältnismäßigkeit).
- Spannung Innovation vs. Transparenz (ITM-AK-Diskussion): innovative IT schwer in starre Verfahren zu pressen; Lösungen (Wettbewerblicher Dialog, Innovationspartnerschaft) sind im Vault nicht detailliert.

**Diskussions-Achse 7: „Welche EU-Sekundärrechtsakte sind für eHealth aktuell?"**

Nur aus ITM-AK (Folie 59 EU-Sekundärrechtsakte): DSGVO / EU AI Act / Verbraucherrechterichtlinie / EHDS. Mit Spannungsfeld DSGVO ↔ EHDS (Datenminimierung vs. erleichterte Sekundärnutzung). Ergänzung der ITM-AK-Note: Versionsangaben (DSGVO 2016/679, AI Act 2024/1689, EHDS 2024/2025 verabschiedet) sind als Standardwissen markiert.

**Anschlussfragen, die ohne Cross-Fach-Verständnis schwer zu beantworten sind:**

- „Welche Rolle hat ein Compliance-Officer vs. ein DSB?" — ITPM-Note + DSGVO-Kenntnis aus ASP/ITM-AK.
- „Was sind die fünf Schlüsselfragen der IT-Projekt-Compliance?" — ITPM-spezifisch.
- „Welche DSGVO-Grundsätze nennt die ASP-Vorlesung?" — vier (nicht sieben), ASP-spezifisch.
- „Wo liegt DSGVO im Stufenbau?" — Stufe 1 (EU-Sekundärrecht, Verordnung), aus ITM-AK.
- „Was bedeutet ‚nachweislich eingehalten' in der Compliance-Definition?" — ITPM-Note plus DSGVO-Rechenschaftspflicht (in ASP nicht behandelt).
- „Wann braucht ein IT-Projekt Vergaberecht?" — ITM-AK-Vergaberecht-Note (öffentliche Auftraggeber, BVergG).
- „Welche Verbindung zwischen CMS und PMI-Risikomanagement?" — ITPM-CMS-Note grenzt explizit ab: identische Struktur (Identifikation → Analyse → Maßnahmen → Überwachung).
- „Was sind die strategischen vs. operativen CMS-Elemente?" — ITPM-CMS-7-Elemente-Note.
- „Welche Rolle spielt die Compliance-Kultur (tone at the top)?" — ITPM-spezifisch.

## Verwandt

**ITM-AK:**
- [[ITM-AK - Stufenbau der Rechtsordnung]]
- [[ITM-AK - Rechtsakte der EU]]
- [[ITM-AK - Prinzipien des EU-Rechts]]
- [[ITM-AK - Grundfreiheiten des EU-Binnenmarkts]]
- [[ITM-AK - EU-Sekundärrechtsakte - DSGVO AI Act EHDS]]
- [[ITM-AK - EU-Institutionen]]
- [[ITM-AK - Vergaberecht]]
- [[ITM-AK - Privatrecht vs Öffentliches Recht]]
- [[ITM-AK - Verfassungsrecht und Verwaltungsrecht]]
- [[ITM-AK - Verwaltungsakte - Verordnung und Bescheid]]
- [[ITM-AK - VfGH und VwGH]]
- [[ITM-AK - Vertragsrecht - Grundbegriffe]]
- [[ITM-AK - Wettbewerbsrecht]]
- [[ITM-AK - Urheberrecht und gewerblicher Rechtsschutz]]
- [[ITM-AK - Diagram - Stufenbau der Rechtsordnung]]

**ITPM:**
- [[ITPM - Compliance - Definition]]
- [[ITPM - Compliance - Umfang und Themen]]
- [[ITPM - Compliance - Risiken]]
- [[ITPM - Compliance Management System]]
- [[ITPM - CMS - Sieben Elemente]]
- [[ITPM - ISO 37301 und Compliance Officer]]
- [[ITPM - Compliance - Ethik]]
- [[ITPM - Projekt-Compliance]]
- [[ITPM - Projekt-Compliance - Prozess]]
- [[ITPM - IT-Projekt-Compliance]]
- [[ITPM - IT-Projekt-Compliance - Umfang]]
- [[ITPM - PMI Risikomanagement-Prozess]]

**ASP:**
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - DSGVO - Privacy by Design]]
- [[ASP - DSGVO - Privacy by Default]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]

**Andere Brücken:**
- [[Cross - DSGVO im eHealth-Kontext]] (Datenschutz-Spezifika in Drei-Fach-Sicht)
- [[Cross - Risikomanagement zwei Sichten]] (Compliance als Risikoklasse)
- [[Cross - PDCA-Zyklus quer durch die Disziplinen]] (CMS als PDCA-Anwendung)

**MOCs:**
- [[ITM-AK - MOC]]
- [[ITPM - MOC]]
- [[ASP - MOC]]

## Quelle

Cross-Fach-Synthese aus den oben gelisteten ITM-AK-, ITPM- und ASP-Konzept-Notes.

**Wichtige Quellen-Beobachtungen:**

- ITM-AK liefert das Rechts-Fundament; ITPM das Management-System; ASP die DSGVO-Schutzmaßnahmen — drei Schichten, drei verschiedene Antwort-Hebel.
- Vergaberecht (BVergG) wird nur in ITM-AK behandelt; ITPM-IT-Projekt-Compliance erwähnt es nicht, obwohl es bei öffentlichen IT-Projekten zentral ist.
- ITPM-CMS-Note grenzt explizit ab: Verbindung zum PMI-Risikomanagement-Prozess mit identischer Struktur — die Cross-Note nutzt diesen Hinweis als Brücke zu [[Cross - Risikomanagement zwei Sichten]].
- ITPM-ISO-37301-Note grenzt Compliance-Officer ≠ DSB explizit ab; ASP-Notes thematisieren den DSB nicht.
- ASP listet vier DSGVO-Grundsätze (nicht sieben); die Note kennzeichnet das selbst als „in der Vorlesung nicht enthalten".
- AI Act (2024/1689) und EHDS-Verordnung sind nur in ITM-AK; ITPM kennt sie nicht, ASP kennt sie nicht.
- Mappings ITPM-Schlüsselfrage 1 ↔ ITM-AK-Stufenbau und ITPM-CMS-Elemente ↔ PMI-Risikomanagement sind Synthese, in den Notes nicht direkt belegt.

**Fach-Zuordnung der Quellen:**

| Note | Fach |
|---|---|
| ITM-AK - Stufenbau der Rechtsordnung / Rechtsakte der EU / Prinzipien des EU-Rechts / EU-Sekundärrechtsakte / Vergaberecht | ITM-AK |
| ITM-AK - Privatrecht-Cluster (Vertragsrecht / Wettbewerbsrecht / Urheberrecht) | ITM-AK |
| ITM-AK - Öffentliches-Recht-Cluster (Verfassung / Verwaltungsakte / VfGH+VwGH) | ITM-AK |
| ITPM - Compliance - Definition / Umfang und Themen / Risiken / Ethik | ITPM |
| ITPM - Compliance Management System / CMS - Sieben Elemente / ISO 37301 und Compliance Officer | ITPM |
| ITPM - Projekt-Compliance / Projekt-Compliance - Prozess / IT-Projekt-Compliance / IT-Projekt-Compliance - Umfang | ITPM |
| ASP - DSGVO - Grundsaetze / Privacy by Design / Privacy by Default | ASP |
| ASP - Security Eigenschaften - Privacy vs Confidentiality | ASP |
