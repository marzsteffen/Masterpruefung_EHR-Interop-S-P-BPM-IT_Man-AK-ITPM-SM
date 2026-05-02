---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/01 Einführung/IVL_ADSP_Einführung.pdf
datum_vorlesung: 2024-10-23
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Einführung und Motivation

## Überblick

Erste Vorlesungseinheit von Advanced Security and Privacy. Sie führt die grundlegenden Begriffe und Schutzziele der Informationssicherheit ein, grenzt Informationssicherheit von IT-Sicherheit ab, behandelt rechtliche Anforderungen aus der DSGVO (insbesondere Privacy by Design und Privacy by Default) und stellt einen Katalog typischer Angriffsmodelle auf Kommunikation vor. Ziel: eine gemeinsame Begriffsbasis für die folgenden Vorlesungen zu Kryptografie, Identitätsmanagement und Risikomanagement.

## Lernziele (laut Vorlesung)

- Erlernen grundlegender Methoden zum Schutz der IT-Sicherheit
- Kenntnisse über unterschiedliche Konzepte zum Schutz der Informationssicherheit
- Erlernen grundlegender Kenntnisse des Informationssicherheits-Risikomanagements und des Business Continuity Managements

## Behandelte Konzepte

### Grundbegriffe Informationssicherheit
- [[ASP - Informationssicherheit - CIA-Triade]]
- [[ASP - Informationssicherheit - IT-Sicherheit vs Informationssicherheit]]

### Security Eigenschaften (über CIA hinaus)
- [[ASP - Security Eigenschaften - Uebersicht]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Security Eigenschaften - Non-repudiation]]
- [[ASP - Security Eigenschaften - Accountability]]
- [[ASP - Security Eigenschaften - Reliability]]
- [[ASP - Security Eigenschaften - Privacy vs Confidentiality]]

### DSGVO und Privacy
- [[ASP - DSGVO - Grundsaetze]]
- [[ASP - DSGVO - Privacy by Design]]
- [[ASP - DSGVO - Privacy by Default]]

### Angriffsmodelle auf Datenkommunikation
- [[ASP - Angriff - Nachricht lesen]]
- [[ASP - Angriff - Traffic Analysis]]
- [[ASP - Angriff - Aufzeichnung und Entschluesselung]]
- [[ASP - Kryptografie - Perfect Forward Secrecy]]
- [[ASP - Angriff - Replay]]
- [[ASP - Angriff - Modifikation Plaintext]]
- [[ASP - Angriff - Modifikation Ciphertext]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Angriff - Denial-of-Service]]

## Roter Faden

Die Vorlesung baut von „Was ist Informationssicherheit?" zur klassischen CIA-Triade als Schutzziel-Modell auf. Anschließend wird IT-Sicherheit als Teilmenge der Informationssicherheit positioniert (technische vs. nicht-technische Aspekte). Auf der Definitionsebene werden die drei CIA-Schutzziele um fünf weitere Security Eigenschaften erweitert (Authentizität, Rückverfolgbarkeit, Verantwortlichkeit, Verlässlichkeit, Privatsphäre); insbesondere Privatsphäre wird gegen Vertraulichkeit abgegrenzt – Vertraulichkeit regelt, **wer** zugreifen darf, Privatsphäre regelt, **wofür** zugegriffene Daten verwendet werden dürfen. Daraus motiviert sich der DSGVO-Block mit Verarbeitungs-Grundsätzen und den Artikel-25-Anforderungen Privacy by Design / by Default. Im letzten Teil wechselt die Perspektive vom „was schützen" zum „wovor schützen": ein Katalog von acht Angriffsmodellen auf Kommunikation (Alice-Bob-Eve), jeweils mit Auswirkung auf ein Schutzziel und einer typischen Sicherheitsfunktion. Damit ist das Begriffsgerüst für die folgenden Krypto- und Identitäts-Vorlesungen gelegt.

## Zentrale Aussagen / Take-aways

- IT-Sicherheit ist ein Teil der Informationssicherheit. Letztere umfasst auch nicht-technische Aspekte (Papier, gesprochenes Wort, organisatorische Strukturen).
- CIA-Triade (Confidentiality, Integrity, Availability) ist nicht erschöpfend; Authentizität, Non-repudiation, Accountability, Reliability und Privacy sind eigenständige Schutzziele.
- Vertraulichkeit ≠ Privatsphäre. Vertraulichkeit regelt Zugriff, Privatsphäre regelt zweckgemäße Verwendung trotz erlaubten Zugriffs.
- DSGVO-Grundsätze: Zweckbindung, Datenminimierung, Speicherbegrenzung, Integrität und Vertraulichkeit. Artikel 25 fordert Privacy by Design (Abs. 1) und Privacy by Default (Abs. 2).
- Verschlüsselung allein schützt weder vor Modifikation des Ciphertexts noch vor Replay – zusätzlich braucht es HMAC/Signatur und Frische-Mechanismen.
- Schlüsselkompromittierung im Nachhinein bricht aufgezeichnete Kommunikation – außer es wurde Perfect Forward Secrecy verwendet.
- Manche Angriffe (Nachricht unterdrücken/DoS) sind protokollabhängig nur schwer abzuwehren.

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Symmetrische Verschluesselung]] (folgt – Verschlüsselung als Schutz vor „Nachricht lesen")
- [[ASP - VL - Asymmetrische Verschluesselung]] (folgt)
- [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (folgt – Schutz vor Modifikation und Impersonation)
- [[ASP - VL - Identitaetsmanagement]] (folgt – Authentizität in Protokollen)
- [[ASP - VL - Informationssicherheits-Risikomanagement]] (folgt – CIA als Bewertungsdimension)
- [[ASP - VL - Business Continuity Management]] (folgt – Schwerpunkt Verfügbarkeit)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/01 Einführung/IVL_ADSP_Einführung.pdf`
- Folienanzahl: 28
- Vortragender: Dr. Kevin Theuermann
- Datum laut Folie 4: 23.10.2024
- Folie 10 trägt den Vermerk „V3.0 © 2023 TÜV AUSTRIA" (Schutzmaßnahmen-Matrix übernommen aus TÜV-Material).
