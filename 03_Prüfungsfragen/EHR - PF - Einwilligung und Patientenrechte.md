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

# EHR - PF - Einwilligung und Patientenrechte

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz behandelt zwei eng verwandte Themenbereiche: (1) **Patientenportale** als Zugangspunkt für Patienten und Versorger zu EHR-Daten – mit konkreten Beispielen (ELGA-Portal, KAGes-Portale, Mayo Clinic) und der konzeptuellen Abgrenzung vom PHR; (2) **Data Sharing Rollen** nach dem im Kurs vorgestellten 10-Rollen-Framework – wer darf was mit Gesundheitsdaten tun, und warum sind klare Rollentrennung und Governance-Strukturen kritisch. Beide Themenbereiche berühren Patientenrechte (Zugang, Kontrolle, Opt-out) und sind prüfungsrelevant für Diskussionsfragen zu Datenschutz, Sekundärnutzung und föderaler EHR-Architektur.

## Verlinkte Konzepte

- [[EHR - Portal - Patientenportal]]
- [[EHR - Governance - Data Sharing Rollen]]
- [[EHR - ELGA - Technologie-Architektur]]
- [[EHR - EHDS - European Health Data Space]]

---

## Karten

### Definition

Was ist ein Patientenportal – welche Kernfunktionen bietet es, und wie unterscheidet es sich konzeptuell von einem PHR?

?

Ein **Patientenportal** ist ein web-basiertes System, das Patienten und/oder Versorgern Zugang zu Gesundheitsdaten ermöglicht. Kernfunktionen (laut Vorlesung): **Zugang zu eigenen Gesundheitsdaten** (Laborbefunde, Diagnosen, Medikation), **Terminbuchung und -erinnerungen**, **Kommunikation mit dem Versorger** (Secure Messaging), **Nachrichtenzustellung** (z. B. Befundbenachrichtigung per E-Mail). Beispiele: ELGA-Portal (gesundheit.gv.at) – national, für alle ELGA-Teilnehmer; KAGes-Portale – zwei getrennte Systeme (Medizin-Portal für Versorger, Patienten-Portal für Patienten); Mayo Clinic – internationales Referenzbeispiel. **Unterschied zu PHR**: Das Portal wird vom Versorger oder einer Institution betrieben und zeigt primär deren Daten. Ein PHR (Personal Health Record) wird vom Patienten selbst geführt und aggregiert Daten aus verschiedenen Quellen – der Patient hat die volle Datenkontrolle. Portal = institutionszentriert; PHR = patientenzentriert.

Welche zehn Data Sharing Rollen unterscheidet das in der Vorlesung vorgestellte Framework – und was ist die jeweilige Kernantwortung?

?

(1) **Data Policy Owner** – definiert übergeordnete Datenpolitik und Nutzungsrechte; trägt ultimative Verantwortung. (2) **Data Steward** – operative Verantwortung für Datenqualität, Konsistenz und Compliance; vermittelt zwischen Policy Owner und technischen Rollen. (3) **Data Provider** – liefert Daten aus Quellsystemen (z. B. Krankenhaus-HIS). (4) **Data Capture** – erfasst Rohdaten (z. B. Gerät, Formular, Sensor). (5) **Data Custodian** – technische Verwahrung und Sicherheit der Daten (Storage, Backup, Access Control). (6) **Data Delivery** – Übermittlung und Verteilung an Konsumenten (z. B. API, Dateiexport). (7) **Data Consumer** – nutzt die Daten für einen definierten Zweck (z. B. behandelnder Arzt, Forscher). (8) **Data Usability** – stellt sicher, dass Daten für den Consumer nutzbar sind (Format, Qualität, Dokumentation). (9) **Data Policy Controller** – prüft Einhaltung der Datenpolitik (Compliance, Audit). (10) **Data Demands / Information Needs** – formuliert den Bedarf und treibt an, welche Daten gesammelt werden müssen. Merkhilfe: Policy Owner setzt den Rahmen, Data Steward lebt ihn operativ, Custodian bewacht, Consumer nutzt – der Rest sind Brückenrollen.

---

### Anwendung

KAGes betreibt zwei getrennte Portale – wer nutzt welches, und warum ist die Trennung sinnvoll?

?

**Medizin-Portal (für Versorger)**: Zugang für behandelnde Ärzte und klinisches Personal zu Patientendaten im KAGes-Verbund – optimiert für klinische Workflows, vollständiger Datenzugang. **Patienten-Portal (für Patienten)**: Zugang für Patienten zu ihren eigenen Befunden, Terminen und Nachrichten – eingeschränkter Datensatz, angepasste Darstellung, kein medizinisches Rohdaten-Dump. **Begründung der Trennung**: unterschiedliche Nutzungskontexte (klinisch vs. patientenadäquat), unterschiedliche Anforderungen an Datentiefe und -darstellung, unterschiedliche Authentifizierungsmechanismen (Berufsausweis vs. Bürger-Authentifizierung, z. B. Handy-Signatur), unterschiedliche Compliance-Anforderungen. Die Trennung entspricht dem Prinzip, dass nicht jeder Datenzugang dem gleichen Interface-Design folgen kann.

In einem Impfprogramm mit zentraler Impfdatenbank – welche Data Sharing Rollen sind wie zu besetzen, und was ist das „Don't do like this!"-Warnsignal aus der Vorlesung?

?

Plausible Rollenbelegung: **Data Policy Owner** = Gesundheitsministerium; **Data Steward** = zuständige Behörde/Agentur; **Data Provider** = impfende Ärzte, Apotheken; **Data Capture** = Arzt-Software, die den Impfeintrag anlegt; **Data Custodian** = zentrales Register (z. B. AGES); **Data Delivery** = Schnittstelle zu ELGA (e-Impfpass); **Data Consumer** = behandelnder Arzt, Reisebüro (Nachweis), Epidemiologie; **Data Policy Controller** = Datenschutzbehörde. **„Don't do like this!"**-Warnsignal aus der Vorlesung: wenn Rollen vermischt werden – insbesondere wenn derselbe Akteur gleichzeitig Data Custodian (Verwahrung) und Data Consumer (Nutzung) ist, entsteht ein Interessenskonflikt, der Missbrauch ermöglicht und Vertrauen untergräbt. Das ist eine klassische Governance-Schwäche in frühen eHealth-Projekten.

Welche konkreten Funktionen eines Patientenportals können nachweislich die Versorgungsqualität verbessern – welche Evidenz liefert die Vorlesung?

?

Die Vorlesung zitiert eine **Pilotstudie zu E-Mail-Remindern und Termineinhaltung**: Patienten, die über ein Portal automatisierte Erinnerungen erhielten, erschienen signifikant häufiger zu ihren vereinbarten Terminen (konkrete Prozentzahl aus der Vorlesung nicht belegt – als Trendaussage). Allgemein: Portale verbessern **Medikamenten-Compliance** (Patienten sehen ihre Medikationsliste und können Unstimmigkeiten melden), **Selbstmanagement** chronischer Erkrankungen (z. B. Glukosewerte eintragen), **Kommunikation** (asynchrones Secure Messaging reduziert unnötige Besuche). Wichtig: Portale sind kein Selbstläufer – niedriger Health Literacy, fehlender Internetzugang und mangelndes Engagement sind Barrieren, die die Evidenz abschwächen. Laut Vorlesung: Portal-Nutzung korreliert stark mit Bildungsniveau und sozioökonomischem Status.

---

### Diskussion

Portal vs. PHR: Wer kontrolliert die Daten – und welche Konsequenzen hat das für Patientenautonomie und Portabilität?

?

**Portal (institutionszentriert)**: Der Betreiber (Krankenhaus, Behörde) kontrolliert, welche Daten sichtbar sind, wie lange sie abrufbar sind und was der Patient damit tun kann. Patient hat Leserecht, aber meist kein Schreibrecht und kein Export-Recht im freien Format. Konsequenz: Datenbindung an Institution – bei Arztwechsel verliert der Patient de facto den Zugang. **PHR (patientenzentriert)**: Patient kontrolliert alle Daten, kann aus beliebigen Quellen aggregieren, entscheidet über Zugriffsberechtigungen für Versorger. Konsequenz: maximale Autonomie, aber maximale Eigenverantwortung für Korrektheit und Vollständigkeit – kein neutraler Prüfer. **Kritische Abwägung**: In einem fragmentierten Versorgungssystem (wie dem österreichischen) ist ein reines PHR-Modell unrealistisch; Portale sind die pragmatische Lösung, erkauft durch Datenbindung. EHDS versucht diesen Trade-off durch Datenweiterleitungsrechte (Primärnutzung) und Sekundärnutzung aufzubrechen.

Warum ist die Trennung von Data Custodian und Data Consumer besonders kritisch für die Sekundärnutzung von Gesundheitsdaten?

?

**Primärnutzung** (Versorgung): Custodian (Datenspeicher) und Consumer (behandelnder Arzt) sind konzeptuell getrennt, aber oft institutionell eng verbunden – das ist tolerierbar, weil die Nutzung dem gleichen Patienten dient. **Sekundärnutzung** (Forschung, Policy, Industrie): Hier droht echter Interessenskonflikt, wenn Custodian und Consumer zusammenfallen – z. B. wenn das Krankenhaus, das Daten verwahrt, auch Forschungslizenzen an Pharma-Unternehmen vergeben kann. Governance-Prinzip: **Functional Separation** – wer Daten verwahrt, darf nicht eigenständig über deren Nutzung entscheiden. Praktische Umsetzung: unabhängige Datentreuhänder (Data Trusts), pseudonymisierte Datenräume, externe Data Policy Controller. EHDS adressiert dies explizit: Datenzugangsanträge für Sekundärnutzung müssen durch eine Health Data Access Body (HDAB) pro Mitgliedsstaat genehmigt werden – institutionelle Trennung wird zum Rechtsrahmen erhoben.

Data Steward vs. Knowledge Steward: Worin liegt der Unterschied – und warum ist die Unterscheidung für EHR-Governance relevant?

?

**Data Steward** (aus dem Vorlesungs-Framework): operativ verantwortlich für Datenqualität, Konsistenz und Compliance; arbeitet auf der Ebene von Instanzen (konkrete Datensätze, Patientenrecords). **Knowledge Steward** [Ergänzung außerhalb VL]: verantwortlich für die Pflege von Wissensstrukturen – Terminologien, Ontologien, Value Sets, klinische Regeln – auf der Ebene der Bedeutung (Semantik). Relevanz für EHR-Governance: ohne einen Knowledge Steward degeneriert ein EHR zur Datengrube – Diagnose-Codes werden inkonsistent vergeben, Medikamentennamen divergieren, CDS-Regeln werden obsolet, ohne dass jemand zuständig ist. In der Praxis übernimmt diese Rolle oft der Chief Medical Information Officer (CMIO) oder ein Terminologie-Team. Die Abgrenzung ist besonders relevant, wenn man ELGA betrachtet: die ELGA GmbH agiert als Custodian und teilweise als Data Steward, aber der Knowledge Steward für CDA-Implementation-Guides ist konzeptuell getrennt (österreichische Gesellschaft für Telematik im Gesundheitswesen, Kodierungskommissionen).

Welche Sicherheitsanforderungen muss ein Patientenportal erfüllen – und wie deckt ELGA-Portal (gesundheit.gv.at) diese ab?

?

Allgemeine Sicherheitsanforderungen für Patientenportale (aus HIMSS/Vorlesungskontext): (1) **Starke Authentifizierung** – mindestens Zwei-Faktor (etwas das man hat + weiß); (2) **Autorisierung** – rollenbasierte Zugriffssteuerung, Patient sieht nur eigene Daten; (3) **Audit Trail** – wer hat wann auf welche Daten zugegriffen (ELGA: Zugriffsprotokoll einsehbar für den Patienten); (4) **Transportverschlüsselung** – TLS/HTTPS; (5) **Session Management** – automatisches Timeout. **ELGA-Portal konkret**: Authentifizierung via Handy-Signatur oder Bürgerkarte (2FA); Patienten können Zugriffsprotokoll einsehen (Transparenz als Datenschutzmechanismus); Opt-out-Möglichkeit (gesamtes ELGA oder einzelne Dokumente); kein direkter Schreibzugang für Patienten (read-only). Kritische Lücken (laut Vorlesung): nicht alle niedergelassenen Ärzte haben ELGA-Zugang; mobile Nutzbarkeit des Portals war initial eingeschränkt; Health Literacy als Zugangsbarriere. [Technische ELGA-Details → [[EHR - ELGA - Technologie-Architektur]]]

---

## Mögliche Anschlussfragen des Prüfers

- Was ist der Unterschied zwischen Opt-in und Opt-out im ELGA-Kontext – und welche ethischen Implikationen hat die Defaultwahl?
- Welche DSGVO-Artikel sind für Patientenportale und Data Sharing Rollen besonders relevant (Art. 9, Art. 15, Art. 17)?
- Wie unterscheidet sich ein Data Policy Controller von einer Datenschutzbehörde?
- Warum ist Health Literacy eine Zugangsbarriere zu Patientenportalen – und was folgt daraus für das Portal-Design?
- Wer ist in ELGA der Data Policy Owner – und wer der Data Steward?
- Was ist ein Data Trust (Datentreuhänder) – und in welchen EU-Ländern gibt es funktionierende Beispiele?
- Wie verhält sich das Portal-Konzept zur IOM-Anforderung „Patient should be able to manage their information"?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
