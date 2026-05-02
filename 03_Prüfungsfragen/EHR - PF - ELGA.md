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

# EHR - PF - ELGA

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Dieser Kartensatz behandelt ELGA (Elektronische Gesundheitsakte Österreich) aus der Perspektive der CCR/CCD-Vorlesung. Der Schwerpunkt liegt auf Technologie-Stack (CDA, IHE XDS), Architektur (dezentrale Repositories + zentrales Zugriffssystem) und dem zeitlichen Ausbau der Dokumenttypen. Vorsicht: Die Vorlesung liefert einen kompakten Einstieg – viele ELGA-Detailfragen (Privacy-Mechanismen, Governance, konkrete XDS-Abläufe) sind in den Folien nur angerissen oder verweisen auf andere Fächer (MSI).

## Verlinkte Konzepte

- [[EHR - ELGA - Technologie-Architektur]]
- [[EHR - Architektur - Registry vs Repository]]
- [[EHR - Architektur - Zentral vs Dezentral]]
- [[EHR - Healthcare Systems - Zentralisierungs-Modelle]]
- [[EHR - EHDS - European Health Data Space]]

---

## Karten

### Definition

Welche Technologien und Standards bilden den Kern der ELGA-Architektur?
?
ELGA basiert auf vier Komponenten: (1) **HL7-v3 CDA (XML)** – Container-Format für klinische Dokumente (Entlassungsbriefe, Laborbefunde, Radiologiebefunde, e-Medikation, e-Impfpass); (2) **Implementation Guides** – je ein Guide pro Dokumenttyp, der Pflichtfelder, zulässige Codes und Strukturen festlegt; (3) **Dezentrale Repositories** – Daten verbleiben beim datenerzeugenden Versorger (Krankenhaus, Apotheke usw.); (4) **Zentrales System** – indiziert die dezentralen Repositories, prüft Zugriffsrechte und ermöglicht Document-Lookup über **IHE-Profile (insb. XDS – Cross-Enterprise Document Sharing)**. Laut Vorlesung: „Decentralized repositories – Central system for access authorization and document lookup using IHE profiles (XDS, …)."

Welche Dokumenttypen sind in ELGA verfügbar, und wann wurden sie eingeführt?
?
Ursprünglich (bei Einführung): **Entlassungsbriefe**, **Laborbefunde**, **Radiologiebefunde**. 2017–2018: **e-Medikation** hinzugefügt. 2021: **e-Impfpass** hinzugefügt. Offen bzw. nicht vollständig integriert (laut Vorlesung): COVID-19-Testergebnisse, Reha-Berichte, Befunde aus dem nicht-stationären Bereich (niedergelassene Ärzte, Physiotherapie). Faustregel: ELGA ist dokumentenzentriert (kein kontinuierliches Datenmodell), jeder Dokumenttyp hat seinen eigenen Implementation Guide.

Wie ist ELGA in die Architektur-Kategorien zentral/dezentral und Registry/Repository einzuordnen?
?
**Politisch-organisatorisch:** semi-zentralisiert – Österreich ist föderalistisch (Bundesländer mit eigenständigen HIS), ELGA ist die nationale Klammer. **Technisch:** zentrale **Registry** + dezentrale **Repositories**. Das zentrale System ist kein Datenspeicher, sondern ein Zugriffsindex und Autorisierungssystem (Registy-Funktion). Die eigentlichen Dokumente liegen dezentral bei den Versorgern (Repository-Funktion). Muster entspricht IHE-XDS-Architektur: Document Registry (zentral) + Document Repository (dezentral). Konsequenz: Verfügbarkeit eines Dokuments hängt vom jeweiligen Quellsystem ab.

---

### Anwendung

Beschreibe den technischen Ablauf eines ELGA-Dokumentenabrufs – von der Arztanfrage bis zum Dokument.
?
Ablauf (aus dem Vorlesungskontext abgeleitet, im PDF skizziert): (1) **Behandler** (z. B. Arzt in der Notaufnahme) gibt an, dass er auf ELGA zugreifen möchte – Patient autorisiert den Zugriff (aktiv oder über Opt-out-System). (2) Das **zentrale Zugriffssystem** prüft die Berechtigung des Behandlers für diesen Patienten. (3) Das zentrale System führt einen **IHE-XDS-Document-Lookup** durch: es fragt ab, welche Dokumente für den Patienten registriert sind (Document Registry). (4) Aus dem Lookup resultiert eine Liste von Dokumenten mit Metadaten (Dokumenttyp, Datum, Quelle) und Pointer zum jeweiligen Repository. (5) Das gewünschte Dokument wird direkt vom **dezentralen Repository** des Quell-Versorgers abgerufen und dem Behandler angezeigt. Achtung: Schritt 5 ist abhängig von der Verfügbarkeit des Quellsystems.

Welche Versorgungsbereiche sind in ELGA gut abgedeckt – und wo sind die bekannten Lücken?
?
**Gut abgedeckt** (laut Vorlesung): stationärer Bereich (Entlassungsbriefe aus Krankenhäusern), Laborbefunde aus Krankenhäusern, Radiologiebefunde, e-Medikation (Apotheken, niedergelassene Ärzte mit e-Rezept), e-Impfpass. **Bekannte Lücken** (laut Vorlesungsbeispiel und explizit benannten Lücken): Reha-Zentren oft ohne ELGA-Anbindung (Vorlesungsanekdote: 3 Wochen Reha 2020 ohne einen einzigen ELGA-Eintrag); Befunde von Physiotherapeuten, Psychotherapeuten, Hebammen; private Krankenanstalten mit eigenen Systemen; nicht-stationäre Spezialisten. Fazit: ELGA ist stark im akutstationären Bereich, lückenhaft im ambulanten und rehabilitativen Bereich.

Wie nutzt ELGA das Konzept der Implementation Guides – und was ist deren Funktion im Vergleich zu FHIR-Profilen?
?
**ELGA Implementation Guides** sind dokumenttyp-spezifische Profile des HL7-v3-CDA-Standards. Sie legen für jeden Dokumenttyp (z. B. Entlassungsbrief, Laborbefund) fest: welche Sektionen Pflicht sind, welche Codes (z. B. LOINC, SNOMED, ICD) zu verwenden sind, wie Datumsfelder zu formatieren sind und wie Metadaten für den XDS-Lookup strukturiert sein müssen. **Vergleich mit FHIR-Profilen**: funktional ähnlich (beide schränken einen Basis-Standard auf einen konkreten Use Case ein), aber technisch verschieden: CDA-Profile sind XML-Schema-basiert (schematron-validierbar), FHIR-Profile sind StructureDefinitions in FHIR selbst (FHIR-native Validierung). ELGA nutzt CDA, weil FHIR bei ELGA-Einführung noch nicht reif genug war (FHIR R1 erschien 2014).

---

### Diskussion

Warum setzt ELGA auf CDA statt FHIR – und wie würde eine FHIR-Migration aussehen?
?
**Historische Begründung** (aus Vorlesungskontext): ELGA wurde in einer Phase konzipiert und eingeführt, in der HL7-v3 CDA der dominante, stabile Standard für klinische Dokumente war. FHIR war 2012–2015 noch in der Entstehung (DSTU-Phasen), kein Produktions-Standard. **Technische Gründe für CDA**: gut geeignet für dokumentenzentrierte Architektur (ein Dokument = eine XML-Datei); bewährte Validierung via Schematron. **Gründe für eine FHIR-Migration**: FHIR ist API-zentriert, ressourcengranular, deutlich einfacher zu implementieren (JSON vs. komplexes CDA-XML), internationaler Mainstream. **Migration-Komplexität**: bestehende CDA-Dokumente müssten gemappt oder parallel geführt werden; alle Implementation Guides müssten als FHIR-Profile neu erstellt werden; XDS müsste durch FHIR-IHE-Profile (z. B. MHD – Mobile access to Health Documents) ersetzt werden. Im PDF nicht detailliert – eine FHIR-Migration wird als laufender Diskurs erwähnt. [Ergänzung außerhalb VL: ELGA GmbH entwickelt seit ca. 2022 FHIR-basierte Erweiterungen (e-Impfpass-FHIR-Piloten).]

Was bedeutet ELGA als „semi-zentralisiertes" System für die Praxis – welche Vor- und Nachteile ergeben sich aus der föderalen Struktur Österreichs?
?
**Föderale Realität**: jedes Bundesland kann eigene HIS für seine Landeskrankenhäuser betreiben (z. B. KAGes in der Steiermark), private Krankenhäuser haben eigene Systeme, niedergelassene Ärzte nutzen verschiedene Ordinationssoftware. ELGA-Anbindung muss für jedes dieser Systeme separat realisiert werden. **Vorteil des semi-zentralisierten Modells**: nationale Interoperabilität ohne politisch unmögliche Vereinheitlichung der Systeme; Bundesländer behalten Systemhoheit. **Nachteile**: ungleichmäßige ELGA-Abdeckung (Lücken bei Reha, Privatkliniken, nicht-stationärem Bereich); hoher Koordinationsaufwand für Implementation; langsamere Erweiterung neuer Dokumenttypen. Kritische Frage: Ist ein föderales Modell langfristig kompatibel mit dem EHDS-Ziel eines europäischen Gesundheitsdatenraums?

Wie positioniert sich ELGA im Kontext des European Health Data Space (EHDS) – und welche Anpassungen wären nötig?
?
EHDS ist die EU-Initiative für einen europaweiten Gesundheitsdatenraum (Primär- und Sekundärnutzung, Verordnung 2024). ELGA ist die österreichische Umsetzung eines nationalen EHR – sie ist der natürliche Andockpunkt für EHDS in Österreich. **Gemeinsamkeiten**: beide zielen auf Datenverfügbarkeit über Organisationsgrenzen, beide setzen auf Patientenrechte (Zugang, Widerspruch). **Spannungsfelder und Anpassungsbedarf**: EHDS setzt auf FHIR (International Patient Summary als Kern-Use-Case), ELGA aktuell auf CDA – Formatanpassung nötig. EHDS fordert grenzüberschreitenden Austausch – ELGA-Infrastruktur ist national konzipiert. EHDS adressiert auch Sekundärnutzung (Forschung, Policy) – ELGA hat dafür keine explizite Architektur (datenschutzrechtliche Hürden). Fazit: ELGA muss für EHDS-Compliance deutlich weiterentwickelt werden, insbesondere in Richtung FHIR und Sekundärnutzungs-Infrastruktur. [Details zu EHDS → [[EHR - EHDS - European Health Data Space]]]

---

## Mögliche Anschlussfragen des Prüfers

- Was ist IHE XDS, und wie unterscheidet es sich von IHE MHD (Mobile access to Health Documents)?
- Welche Privacy-Mechanismen schützt ELGA – wie funktioniert das Opt-out-Prinzip? (im PDF nicht detailliert)
- Warum hat ELGA kein kontinuierliches Datenmodell, sondern ist dokumentenzentriert – und welche Konsequenzen hat das für CDS?
- Welche Rolle spielt die ELGA GmbH als zentraler Betreiber – ist das mit dem dezentralen Repository-Modell vereinbar?
- Welche Dokumenttypen fehlen in ELGA am dringendsten, und warum sind sie schwer zu integrieren?
- Wie würdest du beurteilen, ob ELGA die IOM-8-Core-Requirements erfüllt?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
