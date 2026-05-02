---
fach: asp
typ: pruefungsfrage
status: offen
niveau: vertiefung
tags:
  - fach/allgemein/asp
  - typ/pruefungsfrage
  - status/offen
---

# ASP - PF - Grüner Pass Detail

## Kontext

Prüfungskarten für die mündliche Masterprüfung ASP. Thema: EU Digital COVID Certificate (Grüner Pass) – Ausgangssituation, Verordnung, Zertifikatstypen, DCC-Format, Vertrauensmodell (CSCA/DSC), Validator-Anforderungen, AT-Architektur, Sicherheitsbedenken.

## Verlinkte Konzepte

- [[ASP - Gruener Pass - Ausgangssituation]]
- [[ASP - Gruener Pass - EU Digital COVID Certificate]]
- [[ASP - Gruener Pass - Vertrauensmodell]]
- [[ASP - Gruener Pass - DCC-Schema]]
- [[ASP - Gruener Pass - Value Sets und Business Rules]]
- [[ASP - Gruener Pass - Validator-Anforderungen]]
- [[ASP - Gruener Pass - AT Architektur]]
- [[ASP - Gruener Pass - Sicherheitsbedenken]]

---

## Karten

### Definition

Welche Ausgangssituation führte zum EU Digital COVID Certificate, und welche drei Herausforderungen mussten gelöst werden?

?

**Ausgangssituation (Folie 3):**
- Im **Februar 2020** erster COVID-19-Fall in Österreich.
- Wichtigste Maßnahme: **3G-Regel** (Geimpft / Genesen / Getestet) – Nachweis eines geringen epidemiologischen Risikos.
- Statusnachweis über **digitale Zertifikate** auf Smartphones.

**EU-Anforderungen (Folie 4):**
- Zertifikate müssen im Rahmen von Zutrittskontrollen verifiziert werden.
- **Interoperable Zertifikate** für freie Beweglichkeit in der EU.
- EU-Mitgliedsstaaten müssen **Authentizität, Gültigkeit und Integrität** der Zertifikate sicherstellen.

**Drei Herausforderungen (Folie 4, rot markiert):**
1. Wie baut man einen gemeinsam gültigen **Vertrauensrahmen** auf?
2. Wie verhindert man die **Rückverfolgung von Bürgern** (Privatsphäre)?
3. Wie verhindert man die **Fälschung von Zertifikaten**?

---

Was ist das EU Digital COVID Certificate, und aus welchen Bestandteilen besteht es?

?

**Rechtsgrundlage (Folie 6):** EU-Verordnung 2021/953, in Kraft getreten **1. Juli 2021**.
- Ausstellung durch nationale Behörden.
- Aus Gründen der **Datenminimierung** nur unbedingt erforderliche personenbezogene Daten.

**Drei Zertifikatstypen:**
1. Impfzertifikat (Vaccination Certificate)
2. Testzertifikat (Test Certificate)
3. Genesungszertifikat (Certificate of Recovery)

**Bestandteile jedes Zertifikats:**
| Bestandteil | Funktion |
|---|---|
| Menschenlesbare Darstellung | Name, Datum, Land, etc. |
| **QR-Code** | Maschinenlesbare, signierte Repräsentation der Zertifikatsdaten |
| **Digitale Signatur** | Authentizitäts- und Integritätsschutz (signiert durch DSC des ausstellenden Landes) |

**Wichtig:** Das DCC ist **NICHT verschlüsselt** – es ist *signiert*. Inhalte sind technisch lesbar; Privatsphäre wird durch Datenminimierung und Validator-App-Beschränkungen geschützt.

---

Wie ist das Vertrauensmodell des EU Digital COVID Certificate aufgebaut (CSCA, DSC, Trust List)?

?

**Zweistufige Zertifikatskette pro Mitgliedsland (Folie 8):**

| Stufe | Akteur | Funktion |
|---|---|---|
| 1 | **Country Signing Certificate Authority (CSCA)** | Vertrauenswürdige Institution pro Land; signiert die Document Signer Certificates (DSC) |
| 2 | **Document Signer Certificate (DSC)** | Mit dem Private Key des DSC werden die einzelnen DCCs signiert |
| 3 | **EU Digital COVID Certificate (DCC)** | Konkretes Zertifikat für eine Person |

**Zertifikatskette:** CSCA → DSC → DCC

**Trust List:**
- Alle CSCAs und DSCs sind **öffentlich einsehbar und überprüfbar**.
- Enthält vertrauenswürdige Zertifikate + Metadaten der Mitgliedsstaaten.
- Wird über das EU Gateway verteilt.

**Verifikationslogik:** „Ist die DSC-Signatur am Zertifikat gültig? Stammt das DSC von einer in der Trust List geführten CSCA?"

---

Welche Felder enthält das DCC-JSON, und welches Format wird verwendet?

?

**Format (Folie 10):** Das DCC stellt Zertifikatsdaten im **JSON-Format** dar. Kurze, kryptische Schlüssel wegen QR-Code-Kapazitätsbeschränkung.

**Pflichtfelder (Folien 10, 13/14):**

| Feld | Bedeutung |
|---|---|
| `ver` | Schema-Version (z. B. „1.2.1") |
| `nam` | Namens-Block (fn = family name, gn = given name, fnt/gnt = transliteriert) |
| `dob` | Geburtsdatum (Date of Birth) |
| `v` / `t` / `r` | Vaccination / Test / Recovery Block |

**Im Vaccination-Block:**
| Feld | Bedeutung |
|---|---|
| `tg` | Zielkrankheit (Disease Target) |
| `mp` | Impfstoff (Medical Product, z. B. EU/1/20/1528 = Comirnaty) |
| `ma` | Hersteller (Manufacturer) |
| `dn` | Dosisnummer |
| `sd` | Erforderliche Dosen (Standard Doses) |
| `dt` | Impfdatum |
| `co` | Land |
| `is` | Aussteller |
| `ci` | Certificate Identifier (eindeutig) |

---

### Anwendung

Welche Anforderungen muss ein Validator (Person + App) beim DCC erfüllen, und welches Schutzziel adressiert jede?

?

**Anforderungen (Folie 7):**

| Anforderung | Was | Schutzziel |
|---|---|---|
| **Lichtbildausweis-Prüfung** | Identität der Person per amtlichem Ausweis prüfen | Verhindert, dass jemand mit einem fremden QR-Code auftritt |
| **Offline-Signaturprüfung** | Syntaktische/inhaltliche Korrektheit + zeitliche Gültigkeit **ohne Onlineverbindung** prüfen | Verhindert Rückverfolgung über Server-Logs |
| **Eingeschränkte Datenanzeige** | Validator-App darf nur Vorname, Nachname, Geburtsdatum anzeigen | Schützt Privatsphäre (Datenminimierung) |
| **Bearbeitungsverbot** | Keine Bearbeitung, die über Verifizierung hinausgeht | Verhindert Datenkopie in App-Backends |

**Zuordnung zu den drei Herausforderungen:**
- Herausforderung 1 (Vertrauensrahmen) → gelöst durch Vertrauensmodell + Signaturprüfung
- Herausforderung 2 (Rückverfolgung) → gelöst durch Offline-Prüfung + eingeschränkte Anzeige
- Herausforderung 3 (Fälschung) → teilweise durch Lichtbildausweis + Signatur, aber Schwachstellen verbleiben

---

Skizziere die österreichische DCC-Architektur: EU Gateway, AT Gateway Client, BRZ.

?

**EU Gateway (Folie 15):** Von der EU betriebenes zentrales Gateway. Verteilt an Mitgliedsstaaten:
- **Trust List** (alle vertrauenswürdigen Zertifikate)
- **Business Rules** (nationale + globale Validierungsregeln)
- **Value Sets** (Code-zu-Klartext-Übersetzungen)

Zugang **nicht öffentlich** – nur für authentifizierte Backend-Dienste der Mitgliedsstaaten.

**AT Gateway Client (Folien 16–19):** Betrieben vom **Bundesrechenzentrum (BRZ)**. Stellt authentifizierte Verbindung zum EU Gateway her und erstellt **stündlich** drei Dateien:
1. Trust List (alle DSCs für Signaturprüfung)
2. Business Rules AT + EU (Gültigkeitsregeln, z. B. PCR-Test AT: 48 h, Pfizer-Impfung: 1 Jahr)
3. Value Sets (z. B. EU/1/20/1528 → „Comirnaty")

**Validierungs-Pipeline (Folie 20):**
```
DCC QR-Code
  → Basic Validation (Struktur + Signatur)
  → Business Rules Validation (inhaltliche Gültigkeit)
  → Enrich content
  → Anzeige in Validator-App
```

---

Welche drei realen Sicherheitsbedenken dokumentiert die Vorlesung zum Grünen Pass?

?

**1. „Hitler-Vorfall" – gefälschte Inhalte mit gültiger Signatur (Folie 22):**
- Impfausweis auf „Adolf Hitler" wurde in Validierungs-Apps als **gültig anerkannt**.
- Das Zertifikat hatte eine **gültige Signatur der französischen Sozialversicherungsbehörde CNAM**.
- Ursache: Schwachstelle **nicht** in der Kryptografie, sondern in der **Identitätsprüfung beim Aussteller** – keine Plausibilitätsprüfung der eingegebenen Daten.

**2. HCERT-Implementierungsrisiko (Folie 23):**
- Nach der Impfung gibt der Arzt Daten in seine Software ein → CSCA stellt DCC aus.
- Wenn die **Software des Gesundheitsdienstleisters kompromittiert** wurde, können Daten modifiziert werden.
- Theoretisch können Ärzte für **beliebige Personen** ein Attest erstellen.
- Viele verschiedene Software-Implementierungen = viele Angriffsvektoren.

**3. QR-Code-Diebstahl durch Foto (Folie 24):**
- Wer den QR-Code sieht, kann ihn abfotografieren und wiederverwenden.
- Mitigationen: Lichtbildausweis-Pflicht; **Dänemark:** Gültigkeitsdauer auf **3 Tage** reduziert.

**Generelle Lehre:** Die Kryptografie ist in allen drei Szenarien korrekt. Die Schwachstellen liegen an den **Schnittstellen** – Identitätsprüfung beim Aussteller, Software-Sicherheit, physische Handhabung.

---

Lesen Sie das folgende DCC-JSON-Fragment und beschreiben Sie Inhalt und Status:

```json
{ "ver": "1.2.1", "nam": { "fn": "Musterfrau-Gößfinger", "gn": "Gabriele" },
  "dob": "1998-02-26", "v": [{ "mp": "EU/1/20/1528", "dn": 2, "sd": 2, "dt": "2021-02-18", "co": "AT", "is": "Ministry of Health, Austria" }] }
```

?

**Auswertung (Folie 13/14-Felder):**

| Feld | Wert | Bedeutung |
|---|---|---|
| `ver` | 1.2.1 | Schema-Version |
| `fn` / `gn` | Musterfrau-Gößfinger / Gabriele | Nachname / Vorname |
| `dob` | 1998-02-26 | Geburtsdatum 26. Feb. 1998 |
| `mp` | EU/1/20/1528 | Comirnaty (BioNTech/Pfizer) |
| `dn` | 2 | **2. Dosis** |
| `sd` | 2 | Gesamt 2 Dosen erforderlich |
| `dt` | 2021-02-18 | Impfdatum 18. Feb. 2021 |
| `co` | AT | Österreich |
| `is` | Ministry of Health, Austria | Bundesgesundheitsministerium |

**Status:** Person Gabriele Musterfrau-Gößfinger, geb. 1998, wurde am 18.2.2021 mit Comirnaty vollständig geimpft (Dosis 2/2), ausgestellt vom österreichischen Gesundheitsministerium.

---

### Diskussion

Das DCC ist nicht verschlüsselt. Wie wird trotzdem Privatsphäre gewährleistet – und wo bleibt eine Lücke?

?

**Warum nicht verschlüsselt:** Ziel des DCC ist Verifikation (Authentizität + Integrität), nicht Vertraulichkeit. Jeder Validator soll ohne Schlüsselverteilung prüfen können. Verschlüsselung würde die Offline-Prüfung erschweren.

**Privatsphärenschutz erfolgt über drei Schichten:**
1. **Datenminimierung (DSGVO-Grundsatz):** Im QR-Code nur notwendige Daten (Name, Dob, Impfstatus, kein SVNR, keine Adresse, kein Telefon).
2. **Eingeschränkte Validator-App-Anzeige:** App zeigt nur Vorname/Nachname/Geburtsdatum an.
3. **Offline-Prüfung:** Keine Anfrage an Online-Server, daher kein Server-Logging des Zugriffs.
4. **Bearbeitungsverbot:** App darf keine Daten weiterverarbeiten oder speichern.

**Verbleibende Lücke:**
- Wer den QR-Code sieht/scannt, erhält technisch alle Daten (Impfstoff, Datum, Aussteller).
- Foto-Diebstahl des QR-Codes ist möglich (siehe Sicherheitsbedenken Folie 24).
- Die Privatsphäre-Garantien hängen von **regelkonformem Verhalten des Validators** ab – keine technische Erzwingung.

---

Der Hitler-Vorfall: Warum war die Kryptografie intakt, und welche Schicht hat versagt?

?

**Technischer Sachverhalt (Folie 22):**
- Ein DCC auf „Adolf Hitler" hatte eine **gültige Signatur der CNAM** (französische Sozialversicherung).
- Validierungs-Apps zeigten das Zertifikat als **gültig** an – weil die Signatur technisch korrekt war.

**Warum Kryptografie intakt:**
- Die CSCA → DSC → DCC-Vertrauenskette ist ungebrochen.
- Die digitale Signatur beweist: „Die CNAM hat dieses DCC unterschrieben." Das stimmt.
- Die Kryptografie beantwortet **nicht** die Frage: „Ist der Name korrekt?"

**Welche Schicht versagt hat:**
Die **Identitätsprüfung beim Aussteller** – bevor die Daten an die CSCA gehen. In diesem Fall: kein Abgleich des Namens mit einem Identitätsdokument.

**Generalised Lesson:** Die Vertrauenskette ist **nur so stark wie das schwächste Glied** – wenn der Aussteller keine Plausibilitätsprüfung vornimmt, erzeugt die perfekte Kryptografie technisch korrekte, aber inhaltlich falsche Zertifikate.

**Mitigation:** Identitätsprüfung mit echter Personalausweisbindung beim Aussteller + Lichtbildausweis-Pflicht beim Validator.

---

Welche DSGVO-Spannungsfelder entstehen beim Grünen Pass?

?

| DSGVO-Grundsatz | Anforderung | Spannungsfeld beim DCC |
|---|---|---|
| **Datenminimierung** (Art. 5 Abs. 1c) | Nur notwendige Daten | ✅ Umgesetzt: DCC enthält nur impfbezogene Daten, keine SVNR/Adresse |
| **Zweckbindung** | Daten nur für den definierten Zweck | ⚠️ Validator-Apps dürfen Daten nicht weiterverarbeiten (Bearbeitungsverbot), aber Kontrolle ist schwierig |
| **Speicherbegrenzung** | Daten nur so lange wie nötig | ⚠️ DCC auf Smartphone bleibt bis zur manuellen Löschung; kein automatisches Ablaufdatum im System |
| **Recht auf Vergessenwerden** | Daten müssen gelöscht werden können | ⚠️ Im verteilten System (Trust List, Kopien) ist vollständige Löschung schwierig |
| **Transparenz** | Person weiß, wer Daten verarbeitet | ✅ DCC enthält `is` (Issuer-Feld); Validator-App informiert Nutzer |
| **Sicherheit** | Technische und organisatorische Maßnahmen | ⚠️ QR-Code-Foto-Diebstahl zeigt: technische Sicherheit allein reicht nicht |

---

### Vergleich

Vergleiche die drei Sicherheitsbedenken: Wo greift jedes an, und welche Mitigation gibt es?

?

| Schwachstelle | Angriffsschicht | Mitigation (Folie 22/23/24) |
|---|---|---|
| **Hitler-Vorfall** (gültige Signatur, falscher Name) | Identitätsprüfung beim **Aussteller** | Strengere Identitätsprüfung beim Aussteller; Personalausweis-Bindung |
| **HCERT-Implementierungsrisiko** (kompromittierte Arzt-Software) | **Software** des Gesundheitsdienstleisters | Sichere Software, Audit-Logs, Mehrfaktorauthentifizierung für Ärzte |
| **QR-Code-Foto-Diebstahl** | **Physische Handhabung** des QR-Codes | Lichtbildausweis-Pflicht beim Validator; kürzere Gültigkeitsdauer (Dänemark: 3 Tage) |

**Gemeinsamer Nenner:** In allen drei Fällen ist die **Kryptografie korrekt**. Die Angriffspunkte liegen an menschlichen/organisatorischen Schnittstellen, nicht in der digitalen Signatur selbst.

---

Vergleiche die Offline-Prüfung mit einer hypothetischen Online-Prüfung hinsichtlich Privatsphäre, Aktualität und Ausfallsicherheit.

?

| Aspekt | Offline-Prüfung (DCC-Design) | Online-Prüfung (hypothetisch) |
|---|---|---|
| **Privatsphäre** | ✅ kein Server-Log des Zugriffs | ❌ zentraler Server sieht, wann/wo Person scannt |
| **Rückverfolgung** | ✅ verhindert | ❌ möglich (Server-seitige Bewegungsprofile) |
| **Aktualität** | ⚠️ stündliche Trust-List-Updates (AT: via BRZ) | ✅ Echtzeit-Sperren wirksam |
| **Ausfallsicherheit** | ✅ offline funktionsfähig | ❌ Serverausfall = keine Validierung |
| **Sperrlistenproblem** | ⚠️ kompromittierte DSCs werden nur stündlich wirksam | ✅ sofortige Wirkung |
| **Schwäche** | Zeitfenster für kompromittierte DSCs | Datenschutzrisiko, Abhängigkeit von Verfügbarkeit |

**Trade-off-Entscheidung:** Das DCC-Design wählt bewusst Offline-Prüfung, um Rückverfolgbarkeit zu verhindern – auf Kosten verzögerter Sperrungen.

---

Ordne die drei Herausforderungen (Folie 4) den Lösungsschichten im DCC-System zu.

?

| Herausforderung | Lösungsschicht | Mechanismus |
|---|---|---|
| **1. Gemeinsamer Vertrauensrahmen** | Vertrauensmodell (CSCA → DSC → DCC) + Trust List | Alle Mitgliedsstaaten publizieren CSCAs/DSCs; Trust List verteilt via EU Gateway |
| **2. Rückverfolgbarkeit verhindern** | Validator-Anforderungen + Offline-Prüfung | Eingeschränkte Anzeige, Bearbeitungsverbot, keine Online-Anfragen |
| **3. Fälschungssicherheit** | Digitale Signatur + Lichtbildausweis-Pflicht | Signatur schützt vor Manipulation; Ausweis verhindert Missbrauch fremder QR-Codes |

**Bewertung:** 
- Herausforderung 1 gut gelöst (technisch robuste PKI-ähnliche Struktur).
- Herausforderung 2 gut gelöst (Offline + Datenminimierung).
- Herausforderung 3 mit verbleibenden Schwächen (Hitler-Vorfall zeigt: Krypto ≠ Identitätsprüfung; QR-Foto zeigt: Signaturen ohne Identitätsbindung teilbar).

---

## Mögliche Anschlussfragen

- Was bedeuten die Abkürzungen im DCC-JSON? (z. B. fn = family name, dn = dose number, sd = standard doses)
- Welche DSGVO-Grundsätze rechtfertigen das Datenminimierungsgebot im DCC?
- Was ist der Unterschied zwischen Basic Validation und Business Rules Validation in der AT-Architektur?
- Welcher Akteur betreibt den AT Gateway Client? (BRZ – Bundesrechenzentrum)
- Wie oft wird die Trust List in Österreich aktualisiert? (Stündlich)
- Welche Mitigation wählt Dänemark gegen QR-Code-Diebstahl? (Gültigkeitsdauer 3 Tage)
- Warum kann eine gültige Signatur trotzdem ein falsches Zertifikat bedeuten? (Hitler-Vorfall – Krypto beweist nur Aussteller-Identität, nicht Inhaltswahrheit)

## Eigene Notizen

<!-- Platz für persönliche Ergänzungen, Eselsbrücken, etc. -->
