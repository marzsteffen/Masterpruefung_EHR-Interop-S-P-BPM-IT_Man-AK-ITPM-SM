---
typ: konzept
status: offen
faecher: [asp, ehr, itm-ak]
quellen:
  - "[[ASP - DSGVO - Grundsaetze]]"
  - "[[ASP - DSGVO - Privacy by Design]]"
  - "[[ASP - DSGVO - Privacy by Default]]"
  - "[[ASP - Security Eigenschaften - Privacy vs Confidentiality]]"
  - "[[ASP - Informationssicherheit - CIA-Triade]]"
  - "[[ITM-AK - EU-Sekundärrechtsakte - DSGVO AI Act EHDS]]"
  - "[[EHR - Portal - Patientenportal]]"
  - "[[EHR - Governance - Data Sharing Rollen]]"
  - "[[EHR - EHDS - European Health Data Space]]"
tags:
  - typ/konzept
  - status/offen
  - cross-fach
  - fach/allgemein/asp
  - fach/allgemein/ehr
  - fach/vertiefung/itm-ak
---

# Cross - DSGVO im eHealth-Kontext

> [!info] Kurzdefinition
> Drei-Wege-Brücke: ASP behandelt die DSGVO als *technisch-organisatorische Schutzmaßnahmen* (vier Grundsätze, Privacy by Design / Default), ITM-AK als *EU-Rechtsrahmen* unter mehreren Sekundärrechtsakten (DSGVO/AI Act/Verbraucherrechte/EHDS) mit Spannungsfeld zwischen DSGVO und EHDS, EHR über *Patientenrechte und Data Governance* (Patientenportal, Data-Sharing-Rollen, EHDS) — ohne eine eigene DSGVO-Note. Die drei Sichten ergänzen sich; alle drei zusammen ergeben das Prüfungs-Bild „DSGVO in eHealth".

## Sicht aus Fach ASP

ASP bringt die *operative Schutz-Schicht* — also was technisch und organisatorisch getan werden muss, um DSGVO-konform zu sein.

**Vier Grundsätze für die Verarbeitung personenbezogener Daten** (siehe [[ASP - DSGVO - Grundsaetze]], Folie 16):

| Grundsatz | Kerngedanke |
|---|---|
| Zweckbindung | Daten nur für festgelegten Zweck verwenden |
| Datenminimierung | Nur notwendige Daten erheben |
| Speicherbegrenzung | Nur so lange speichern wie nötig |
| Integrität und Vertraulichkeit | Angemessene Sicherheit gewährleisten |

Quelltreue-Hinweis aus der ASP-Note selbst: Die DSGVO Art. 5 hat zusätzlich „Rechtmäßigkeit, Verarbeitung nach Treu und Glauben, Transparenz", „Richtigkeit" und „Rechenschaftspflicht" — diese werden in der ASP-Vorlesung **nicht** aufgeführt. Wer in der Prüfung sieben Grundsätze nennt, argumentiert nicht aus Vault-Quellen.

**DSGVO-Version**: ASP-PDF spezifiziert sie nicht. ITM-AK ergänzt 2016/679 (als externe Ergänzung markiert).

**Privacy by Design** (siehe [[ASP - DSGVO - Privacy by Design]], Folie 17): DSGVO Artikel 25 Abs. 1 — Datenschutz durch Technikgestaltung von Anfang an. Geeignete technische und organisatorische Maßnahmen, z. B. Pseudonymisierung. Pseudonymisierung im PDF erwähnt, aber nicht definiert.

**Privacy by Default** (siehe [[ASP - DSGVO - Privacy by Default]], Folie 17): DSGVO Artikel 25 Abs. 2 — datenschutzfreundliche Voreinstellungen, vor allem zum Schutz weniger technikversierter Personen, mit aktiver Anpassbarkeit. Beispiel auf der Folie (Add-Blocker) wird in der Note selbst als „eher schwaches Beispiel" markiert.

**Privacy ≠ Confidentiality** (siehe [[ASP - Security Eigenschaften - Privacy vs Confidentiality]], Folie 15): Diese Trennung ist die *technische Begriffs-Klarheit*, die ASP allein liefert.

| Aspekt | Vertraulichkeit | Privatsphäre |
|---|---|---|
| Frage | Wer darf zugreifen? | Wofür darf zugegriffen werden? |
| Lokalisierung | Teil der CIA-Triade | Eigene Eigenschaft im 8er-Katalog |
| Maßnahme | Verschlüsselung, Zugriffskontrolle | Zweckbindung (DSGVO), organisatorische Richtlinien |

Die ASP-Note macht die Konsequenz explizit: Eine Person kann *autorisiert* sein zuzugreifen (Vertraulichkeit erfüllt) und trotzdem die Daten zweckwidrig verwenden (Privatsphäre verletzt).

## Sicht aus Fach ITM-AK

ITM-AK bringt die *rechtsrahmen-orientierte Sicht* — also wo DSGVO im EU-Sekundärrecht verortet ist und welche anderen Rechtsakte daneben stehen.

**EU-Sekundärrechtsakte für eHealth** (siehe [[ITM-AK - EU-Sekundärrechtsakte - DSGVO AI Act EHDS]], Folie 59):

| Rechtsakt | Form | eHealth-Relevanz |
|---|---|---|
| DSGVO (2016/679) | Verordnung | Patientendaten = besondere Kategorien personenbezogener Daten (Art 9 DSGVO); strengere Anforderungen |
| EU AI Act (2024/1689) | Verordnung | Medizinische KI typischerweise „Hochrisiko"; CE-Konformität, Risikomanagement |
| Verbraucherrechterichtlinie (2011/83/EU) | Richtlinie | B2C-Beziehungen Klinik–Patient, Wahlleistungen, Telemedizin |
| EHDS-Verordnung (2024/2025 verabschiedet) | Verordnung | Primär- und Sekundärnutzung von Gesundheitsdaten EU-weit |

Quelltreue-Hinweis: Folie 59 listet nur Schlagwörter; die Inhaltsbeschreibungen sind in der Note explizit als „eigene Antwort, basierend auf Standardwissen" markiert.

**DSGVO ≠ DSG**: DSGVO ist EU-Verordnung (direkt anwendbar), DSG ist österreichisches Datenschutzgesetz (begleitend).

**EHDS ≠ ELGA**: EHDS ist EU-weit, ELGA national. EHDS soll nationale Systeme wie ELGA EU-weit interoperabel machen.

**Patientendaten als „besondere Kategorien personenbezogener Daten" (Art 9 DSGVO)**: nur in ITM-AK explizit. Wer in der Prüfung den Status besonderer Kategorien thematisiert, antwortet aus ITM-AK.

**Spannungsfeld DSGVO ↔ EHDS** (eine zentrale Diskussionsfrage aus der ITM-AK-Note):

- DSGVO: Datenminimierung, Zweckbindung, Einwilligungsschwerpunkt.
- EHDS: erleichterte sekundäre Nutzung von Gesundheitsdaten, opt-out-orientiert.
- Praktische Frage: Wie weit darf Forschung Patientendaten nutzen, ohne individuelle Einwilligung?

## Sicht aus Fach EHR

EHR hat **keine eigene DSGVO-Note**. DSGVO-Aspekte erscheinen indirekt über drei Notes, die aus dem Patient- und Governance-Blickwinkel argumentieren.

**Patientenportal** (siehe [[EHR - Portal - Patientenportal]], Folien 68–72):

- Web-basierter Zugang, über den Patienten auf ihre Gesundheitsdaten zugreifen — Anker für Patient Empowerment.
- Konkrete österreichische Beispiele: ELGA-Portal (`gesundheit.gv.at/gesundheitsleistungen/elga.html`), KAGes-Portale (Versorger-Portal `medizin-portal.kages.at`, Patienten-Portal `patienten-portal.kages.at`).
- Login-/Authentifizierungs-Frage in der EHR-Note offen formuliert (Übungsfragen) — der Verweis im Verwandt-Block geht auf [[ASP - Authentifizierung]], also ASP-Cluster (Identitätsmanagement-Brücke 4).
- DSGVO-Bezug: implizit über das Patientenrecht, eigene Daten einzusehen — die EHR-Note thematisiert DSGVO nicht direkt.

**Data-Sharing-Rollen nach Metsallik** (siehe [[EHR - Governance - Data Sharing Rollen]]):

- Rollen-Modell: **Data Policy Owner**, **Data Steward**, **Data Provider**, **Data Capture**, **Data Custodian**, **Data Delivery**, **Data Consumer**, **Data Usability**, **Data Policy Controller**.
- Vergleich zu DSGVO-Rollen (Verantwortlicher, Auftragsverarbeiter): die EHR-Note stellt diese Frage explizit als Anschlussfrage („Wie verhält sich diese Governance zu DSGVO-Rollen?"), beantwortet sie aber nicht. Der Verwandt-Link auf `[[ASP - DSGVO Rollen]]` zeigt auf eine **nicht existierende Note**.

**EHDS-Sicht aus EHR** (siehe [[EHR - EHDS - European Health Data Space]]):

- Geplanter europäischer Gesundheitsdatenraum für Primär- und Sekundärnutzung.
- Cartography-Übung mit den Achsen WHO participates, WHAT decisions, WHERE, WHO uses, WHAT data.
- Die EHR-Note führt die DSGVO-Spannung explizit auf: „EHDS verlangt Sekundärnutzung von Gesundheitsdaten — wie verträgt sich das mit DSGVO und nationaler Datenschutz-Praxis?"
- Detail-Inhalte (MyHealth@EU, HealthData@EU, Verordnungsnummer) sind als „Ergänzung außerhalb der Vorlesung" markiert.

## Gemeinsamkeiten

| Aussage | Wo |
|---|---|
| DSGVO ist der zentrale Rechtsrahmen für eHealth-Datenverarbeitung in der EU | ASP, ITM-AK |
| Sekundärnutzung (EHDS) erzeugt Spannungen mit DSGVO-Grundsätzen | ITM-AK explizit, EHR explizit |
| Datenminimierung als zentrales Prinzip | ASP-Grundsatz, EHR Patient-Empowerment-Anwendung, ITM-AK Rechtsbezug |
| ELGA als nationaler Anwendungsfall der DSGVO-Anforderungen | implizit in allen drei (ASP-OIDC-ELGA-Beispiel, EHR-Portal, ITM-AK-EHDS↔ELGA-Trennung) |

## Unterschiede / Konflikte / unterschiedliche Schwerpunkte

**1. Schicht-Asymmetrie der drei Fächer.**

- ASP = Schutzmaßnahmen-Schicht (vier Grundsätze + Privacy by Design / Default + Privacy/Confidentiality-Begriffsklarheit).
- ITM-AK = Rechtsrahmen-Schicht (DSGVO als ein Sekundärrechtsakt von vieren, Spannungsfeld zur EHDS, Patientendaten als besondere Kategorie).
- EHR = Anwendungs-/Patientenrechte-Schicht (Portal, Data Sharing Rollen, EHDS-Use-Cases) **ohne eigene DSGVO-Note**.

Drei Schichten = drei verschiedene Antwort-Hebel je nach Frage.

**2. EHR-Lücke.**

EHR hat keine dedizierte DSGVO-Note. Die EHR-Note `Governance - Data Sharing Rollen` verlinkt auf `[[ASP - DSGVO Rollen]]`, das **nicht existiert**. Wer „DSGVO im EHR-Kontext" als Frage bekommt, muss aus EHR-Patient-Empowerment-Notes plus ASP-DSGVO-Notes synthetisieren — keine fertige EHR-DSGVO-Note steht zur Verfügung.

**3. Anzahl der DSGVO-Grundsätze.**

ASP-Vorlesung listet **vier** Grundsätze (Zweckbindung, Datenminimierung, Speicherbegrenzung, Integrität+Vertraulichkeit). Die ASP-Note kennzeichnet selbst, dass die übrigen drei aus Art. 5 DSGVO (Rechtmäßigkeit/Treu und Glauben/Transparenz, Richtigkeit, Rechenschaftspflicht) **nicht** in der Vorlesung sind. ITM-AK listet keine Grundsätze. EHR listet keine.

In der mündlichen Prüfung: Wer „die" DSGVO-Grundsätze erklärt, erklärt entweder die vier aus ASP — oder kennzeichnet, dass weitere drei aus dem Allgemeinwissen kommen.

**4. DSGVO-Version.**

- ASP: nicht spezifiziert.
- ITM-AK: 2016/679 — explizit als „eigene Antwort, basierend auf Standardwissen" markiert.
- EHR: keine Versionsangabe.

Konsequenz: Versionsangabe ist nicht aus den Folien direkt belegbar; in der Prüfung als „Verordnung 2016/679, anwendbar seit 25.05.2018" antworten und den Standard-Wissen-Status anerkennen.

**5. Privacy ≠ Confidentiality — die ASP-Begriffs-Klarheit.**

Diese Trennung (autorisierter Zugriff ≠ zweckgemäße Verwendung) ist *nur in ASP*. ITM-AK und EHR thematisieren sie nicht. Die Konsequenz: Verschlüsselung schützt Vertraulichkeit, nicht Privatsphäre. Wer in der Prüfung argumentiert „DSGVO wird durch Verschlüsselung erfüllt", ist falsch — Verschlüsselung adressiert nur den Grundsatz „Integrität und Vertraulichkeit", nicht die Zweckbindung.

**6. Privacy by Design / Default — nur in ASP.**

DSGVO Art. 25 Abs. 1 / Abs. 2 wird nur in ASP eigenständig behandelt. ITM-AK erwähnt sie nicht; EHR erwähnt sie nicht. Die ASP-Note macht aber selbst klar, dass die Beispiele in der Vorlesung schwach sind (Pseudonymisierung wird nicht definiert; „Add-Blocker" wird selbst kritisiert). Wer Privacy by Design ausführlich erklärt, ergänzt aus dem Allgemeinwissen über das im PDF Hinausgehende.

**7. „Patientendaten als besondere Kategorien" (Art 9 DSGVO) — nur in ITM-AK.**

Diese Aussage ist prüfungsrelevant für eHealth speziell, weil sie strengere Anforderungen begründet. ASP nennt sie nicht, EHR nennt sie nicht. Wer den besonderen Schutz von Gesundheitsdaten begründet, antwortet aus ITM-AK.

**8. Spannungsfeld DSGVO ↔ EHDS.**

Beide Fächer benennen es:
- ITM-AK formuliert es als Diskussionsfrage in der Sekundärrechtsakte-Note.
- EHR formuliert es in der EHDS-Note als Diskussionsfrage.
- ASP thematisiert es nicht.

Saubere Cross-Antwort: DSGVO baut auf Datenminimierung + Zweckbindung + individueller Einwilligung; EHDS verlangt erleichterte sekundäre Nutzung mit Opt-out-Logik. Die Lösungsperspektive (im Vault nicht ausgeführt): Sekundärnutzungen unter EHDS sind über *gesetzliche* Erlaubnisnormen geregelt (Art 9 Abs 2 lit i+j DSGVO), nicht über individuelle Einwilligung.

**9. Data-Sharing-Rollen vs. DSGVO-Rollen — keine direkte Verbindung im Vault.**

EHR-Metsallik-Rollen (Data Capture / Custodian / Steward / Consumer / Policy Owner / Policy Controller) sind nicht zu DSGVO-Rollen (Verantwortlicher, Auftragsverarbeiter, Betroffener) gemappt. Die EHR-Note stellt das selbst als Anschlussfrage. Cross-Synthese-Punkt:

- **Data Policy Owner / Policy Controller** ↔ DSGVO **Verantwortlicher** (decides purposes and means).
- **Data Custodian** ↔ DSGVO **Auftragsverarbeiter** (processes on behalf of controller).
- **Data Subject** = der Patient (in der EHR-Metsallik-Liste fehlt diese Rolle ausdrücklich).

Diese Verbindung ist *Synthese, nicht Quelltreue* — entsprechend in der mündlichen Prüfung als eigene Schlussfolgerung kennzeichnen.

## Synthese für die mündliche Prüfung

**Diskussions-Achse 1: „Wie passt DSGVO in eHealth zusammen?"**

Antwort braucht alle drei Fächer:

1. **Rechtsrahmen-Frame** (ITM-AK): DSGVO als EU-Verordnung 2016/679, neben EU AI Act, Verbraucherrechterichtlinie und EHDS. Patientendaten = besondere Kategorien (Art 9 DSGVO).
2. **Schutz-Schicht-Frame** (ASP): vier Grundsätze (Zweckbindung, Datenminimierung, Speicherbegrenzung, Integrität+Vertraulichkeit) + Privacy by Design (Art 25 Abs 1) + Privacy by Default (Art 25 Abs 2).
3. **Anwendungs-Frame** (EHR): Patientenportal als Patient-Empowerment-Werkzeug, Data-Sharing-Rollen, EHDS-Use-Cases.

**Diskussions-Achse 2: „Wo greift Verschlüsselung — und wo reicht sie nicht?"**

Direkte Anwendung der Privacy-vs-Confidentiality-Trennung aus ASP. Verschlüsselung schützt Vertraulichkeit (CIA), das adressiert den DSGVO-Grundsatz „Integrität und Vertraulichkeit". Privatsphäre (zweckgemäße Verwendung) wird durch Zugriffs-Beschränkung allein nicht gesichert — dafür braucht es organisatorische Maßnahmen (Zweckbindung, Datenminimierung, RBAC mit Need-to-Know-Prinzip, Audit-Trails). Das ist die Brücke zu Brücke 4 ([[Cross - OAuth2 OIDC SAML im eHealth-Kontext]]) und zur potenziellen Brücke 5 (Einwilligung und Audit Trails).

**Diskussions-Achse 3: „DSGVO vs. EHDS — wo ist der Konflikt?"**

ITM-AK + EHR + ASP zusammen:
- DSGVO-Grundsatz Datenminimierung ↔ EHDS-Sekundärnutzung großer Datenmengen.
- DSGVO-Grundsatz Zweckbindung ↔ EHDS-Forschung für noch unbekannte Zwecke.
- DSGVO-Einwilligung ↔ EHDS Opt-out-Modell.

Die Auflösung läuft über Art 9 Abs 2 lit i+j DSGVO (gesetzliche Erlaubnisnormen für öffentliches Gesundheitsinteresse / wissenschaftliche Forschung). Diese Detail-Auflösung ist in keiner Vault-Note ausgeführt — als eigene Schlussfolgerung kennzeichnen.

**Diskussions-Achse 4: „Wer ist Data Custodian in ELGA — und ist das DSGVO-Verantwortlicher oder Auftragsverarbeiter?"**

EHR liefert Custodian-Rolle (Metsallik), ITM-AK liefert die DSGVO-Rollen-Logik, ASP liefert die Schutz-Anforderungen. Die direkte Mapping-Antwort steht in keinem Note — Custodian ist je nach Implementation Verantwortlicher (eigene Datenpolitik) oder Auftragsverarbeiter (im Auftrag eines anderen). Konkret in ELGA: das jeweilige Krankenhaus ist Verantwortlicher seiner Datenerfassung (Art 4 Nr 7 DSGVO), die ELGA-GmbH ist je nach Modell Verantwortlicher des Index oder Auftragsverarbeiter. Diese Detail-Frage ist Synthese.

**Diskussions-Achse 5: „Was schützt DSGVO konkret im EHR?"**

- Patient hat Rechte (Auskunft, Berichtigung, Löschung) → realisiert über Patientenportal (EHR).
- Verarbeitung braucht Rechtsgrundlage → in eHealth meist Art 6 + Art 9 (besondere Kategorien) DSGVO (ITM-AK).
- Technische Maßnahmen → Pseudonymisierung, Verschlüsselung, Zugriffskontrolle, Audit-Logs (ASP).
- Architektur-Maßnahmen → Privacy by Design + Default (ASP).

**Anschlussfragen, die ohne Cross-Fach-Verständnis schwer zu beantworten sind:**

- „Welche DSGVO-Grundsätze nennt die Vorlesung?" — vier (ASP), nicht sieben — Quelltreue-Antwort.
- „Was ist der Unterschied zwischen Privatsphäre und Vertraulichkeit?" — ASP-spezifisch, mit DSGVO-Bezug.
- „Was sind besondere Kategorien personenbezogener Daten?" — ITM-AK-spezifisch (Art 9 DSGVO).
- „Wie verhält sich Privacy by Design zur Datenminimierung?" — ASP-Synthese, beide Konzepte stützen einander, im PDF nicht ausgeführt.
- „Wie reagiert die DSGVO auf den EHDS-Sekundärnutzungs-Druck?" — ITM-AK + EHR-EHDS-Synthese.
- „Welche DSGVO-Rolle hat ein Data Custodian aus dem EHR-Kontext?" — keine direkte Vault-Antwort, eigene Schlussfolgerung.

## Verwandt

**ASP:**
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - DSGVO - Privacy by Design]]
- [[ASP - DSGVO - Privacy by Default]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]
- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Identitaetsmanagement - Autorisierung]]

**EHR:**
- [[EHR - Portal - Patientenportal]]
- [[EHR - Governance - Data Sharing Rollen]]
- [[EHR - EHDS - European Health Data Space]]

**ITM-AK:**
- [[ITM-AK - EU-Sekundärrechtsakte - DSGVO AI Act EHDS]]
- [[ITM-AK - Rechtsakte der EU]]
- [[ITM-AK - Prinzipien des EU-Rechts]]

**Andere Brücken:**
- [[Cross - OAuth2 OIDC SAML im eHealth-Kontext]] (Audit-Trails über AuditEvent/Provenance/Consent als technische Umsetzung der Zweckbindung)
- [[Cross - ELGA als nationaler eHealth-Use-Case]] (ELGA als praktische Anwendung der DSGVO-Anforderungen)

**MOCs:**
- [[ASP - MOC]]
- [[EHR - MOC]]
- [[ITM-AK - MOC]]

## Quelle

Cross-Fach-Synthese aus den oben gelisteten ASP-, EHR- und ITM-AK-Konzept-Notes. Externe Ergänzungen sind in den Synthese-Achsen explizit als „eigene Schlussfolgerung" markiert (insbesondere die Mapping-Aussagen Data-Sharing-Rollen ↔ DSGVO-Rollen sowie die Auflösung des DSGVO-EHDS-Spannungsfeldes über Art 9 Abs 2 DSGVO).

**Wichtige Quellen-Beobachtungen:**

- ASP listet *vier* DSGVO-Grundsätze, nicht sieben — die Note kennzeichnet das selbst.
- DSGVO-Versionsangabe (2016/679) ist in den Vault-Folien nicht direkt enthalten; ITM-AK ergänzt sie als Standardwissen.
- EHR hat **keine eigene DSGVO-Note** — DSGVO-Aspekte erscheinen indirekt über Patient-Empowerment- und Governance-Notes.
- Verlinkter Note `[[ASP - DSGVO Rollen]]` aus EHR-Governance existiert im Vault nicht (offene Stelle, gewollt unresolved laut INSTRUCTIONS).

**Fach-Zuordnung der Quellen:**

| Note | Fach |
|---|---|
| ASP - DSGVO - Grundsaetze / Privacy by Design / Privacy by Default | ASP |
| ASP - Security Eigenschaften - Privacy vs Confidentiality, ASP - Informationssicherheit - CIA-Triade | ASP |
| ITM-AK - EU-Sekundärrechtsakte - DSGVO AI Act EHDS | ITM-AK |
| EHR - Portal - Patientenportal / Governance - Data Sharing Rollen / EHDS - European Health Data Space | EHR |
