---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/07 Grüner Pass/IVL_ADSP IT-Basisschutzmethoden in der Praxis (Grüner Pass).pdf
datum_vorlesung: 2024-11-12
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Grüner Pass (EU Digital COVID Certificate)

## Überblick

Siebter Vorlesungsblock und zweites Praxiskapitel („IT-Security Basis-Schutzmethoden in der Praxis"). Anhand des **EU Digital COVID Certificate** (DCC, in Österreich „Grüner Pass") wird gezeigt, wie digitale Signaturen, Zertifikatsketten, JSON-Datenformate und QR-Codes in einem realen pan-europäischen Anwendungsfall zusammenspielen. Aufbau gemäß Agenda (Folie 2): Ausgangssituation, Anforderungen, Konzept und Implementierung, Sicherheitsbedenken.

## Lernziele (laut Vorlesung)

*Im PDF nicht als eigene Liste ausgewiesen.* Aus dem Aufbau ergeben sich: regulatorischen Rahmen des DCC kennen; Vertrauensmodell mit CSCA und DSC verstehen; DCC-Datenstruktur (JSON, Value Sets, Business Rules) lesen können; österreichische Architektur über EU Gateway / AT Gateway Client / BRZ erklären; reale Sicherheitsbedenken (gefälschte Zertifikate, QR-Code-Diebstahl) diskutieren können.

## Behandelte Konzepte

### Ausgangssituation und rechtlicher Rahmen
- [[ASP - Gruener Pass - Ausgangssituation]]
- [[ASP - Gruener Pass - EU Digital COVID Certificate]]

### Vertrauen und Validierung
- [[ASP - Gruener Pass - Vertrauensmodell]]
- [[ASP - Gruener Pass - Validator-Anforderungen]]

### Datenstruktur und Logik
- [[ASP - Gruener Pass - DCC-Schema]]
- [[ASP - Gruener Pass - Value Sets und Business Rules]]

### Implementierung
- [[ASP - Gruener Pass - AT Architektur]]

### Probleme
- [[ASP - Gruener Pass - Sicherheitsbedenken]]

## Roter Faden

**Ausgangssituation:** Februar 2020 erster COVID-Fall in Österreich. Eindämmungs-Maßnahmen, wichtigste war die **3G-Regel** (Geimpft, Genesen, Getestet) als Nachweis eines geringen epidemiologischen Risikos. Statusnachweis sollte digital über Smartphones erfolgen, was die Frage nach EU-weit interoperablen Zertifikaten aufwarf. Drei Herausforderungen: gemeinsamer Vertrauensrahmen, Schutz der Privatsphäre, Fälschungssicherheit.

**Rechtlicher Rahmen:** Verordnung (EU) 2021/953 vom 1. Juli 2021 über das **EU Digital COVID Certificate**. Drei Zertifikatstypen: Impfzertifikat, Testzertifikat, Genesungszertifikat. Jedes enthält einen QR-Code und eine digitale Signatur durch die ausstellende nationale Behörde, validiert über das EU Gateway. Datenminimierungs-Prinzip: nur unbedingt erforderliche personenbezogene Daten.

**Vertrauensmodell:** Zweistufige Zertifikatskette pro Mitgliedsland: **Country Signing Certificate Authority (CSCA)** signiert **Document Signer Certificates (DSC)**, mit denen wiederum die einzelnen DCC ausgestellt werden. Alle CSCA- und DSC-Zertifikate sind öffentlich einsehbar und überprüfbar via **Trust List**.

**Validator-Anforderungen:** Identifizierung der Person via Lichtbildausweis. Offline-Prüfung der Signatur (verhindert Rückverfolgbarkeit). Validator-Apps zeigen nur Vorname, Nachname, Geburtsdatum (bewahrt Privatsphäre). Bearbeitungen über die Verifizierung hinaus sind unzulässig (verhindert Missbrauch).

**Datenstruktur:** DCC nutzt **JSON-Schema** mit Schlüssel-Werte-Paaren. Felder umfassen Version, Name, Geburtsdatum, Vaccination-/Test-/Recovery-Block. Codes (z. B. `EU/1/20/1528` für Comirnaty) werden über **Value Sets** auf menschenlesbare Werte gemappt. **Business Rules** stellen die Verifizierungslogik in Validator-Apps dar; Länder können sie adaptieren. Mindestens zu prüfen: Code für Zielkrankheit, Impfstoff (von EMA zugelassen?), Dosisnummer (ausreichend?), Datum (vor 14 Tagen / nicht länger als 365 Tage?).

**Österreichische Architektur:** Das **EU Gateway** verteilt zentral Trust List, Business Rules und Value Sets an die Mitgliedsstaaten. Zugang ist nicht öffentlich – authentifizierte Verbindungen aus den Backend-Diensten der Mitgliedsstaaten. In Österreich: **AT Gateway Client** ruft stündlich Trust List, Business Rules AT/EU und Value Sets ab; **BRZ (Bundesrechenzentrum)** betreibt die Dienste. EU-Komponenten **Basic Validation** (Strukturelle Korrektheit + Authentizität) und **Business Rules Validation** (z. B. Pfizer 1 Jahr akzeptiert, PCR-Test 48 h gültig) prüfen den DCC-QR-Code und reichern ihn für die Anzeige an.

**Sicherheitsbedenken:** Im November 2021 berichtete *Der Standard*, dass eine **Adolf-Hitler-Urkunde** mit verschiedenen Geburtsdaten als gültig anerkannt wurde – signiert von der französischen Sozialversicherung CNAM. Hauptursache: Vertrauenskette ist gebrochen, wenn ein Mitgliedstaat nachlässig signiert. Implementierungs-Risiko bei der HCERT-Erstellung: kompromittierte Software des Gesundheitsdienstleisters könnte Daten ändern; theoretisch können Ärzte beliebige Atteste erstellen. **QR-Code-Foto-Diebstahl:** Wer einen QR-Code zum Scan zeigt, könnte fotografiert und der Pass nachgebaut werden. Daher Lichtbildausweis-Pflicht; Dänemark setzte 3-Tage-Gültigkeit als Mitigationsmaßnahme.

## Zentrale Aussagen / Take-aways

- **Rechtsgrundlage:** EU-Verordnung 2021/953, ab 01.07.2021.
- **Drei Zertifikatstypen:** Impf-, Test-, Genesungszertifikat.
- **Vertrauenskette:** CSCA → DSC → DCC (zweistufig pro Land).
- **Trust List:** zentral verteilt vom EU Gateway, alle DSC öffentlich einsehbar.
- **DCC-Format:** JSON, mit Value Sets für Codes und Business Rules für Verifikationslogik.
- **AT Architektur:** EU Gateway → AT Gateway Client (stündlich) → BRZ-Dienste → Validator-Apps.
- **Validator-App** zeigt nur Vor-/Nachname/Geburtsdatum, Offline-Prüfung gegen Trust List.
- **Sicherheitsschwächen:** gefälschte Zertifikate (Hitler-Vorfall), kompromittierbare Erstellungs-Software, QR-Code-Foto-Klau.
- **Mitigationen:** Lichtbildausweis-Prüfung, kürzere QR-Code-Gültigkeit (Dänemark: 3 Tage).

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (Krypto-Bausteine: Signatur-Verifikation, Zertifikatsketten, X.509)
- [[ASP - VL - Identitaetsmanagement]] (Identifizierung via Lichtbildausweis, eIDAS-LoA)
- [[ASP - VL - Einfuehrung und Motivation]] (Privatsphäre vs. Vertraulichkeit, DSGVO Datenminimierung)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/07 Grüner Pass/IVL_ADSP IT-Basisschutzmethoden in der Praxis (Grüner Pass).pdf`
- Folienanzahl: 25
- Vortragender: Dr. Kevin Theuermann
- Datum laut Folien: 12.11.2024
- Externe Referenz Folie 6: Verordnung (EU) 2021/953 (CELEX 32021R0953)
- Externe Referenz Folie 22: Standard-Artikel zu Hitler-Zertifikat-Vorfall
