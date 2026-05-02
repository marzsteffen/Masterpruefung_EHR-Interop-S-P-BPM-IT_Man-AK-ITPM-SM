---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/04 Hash, MAC, Digitale Signaturen, Zertifikate/IVL_ADSP_Hash_MAC_HMAC_Digitale_Signaturen_…SM-X800_Nov-27-0843-2024_1.pdf
datum_vorlesung: 2024-10-29
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Hash, MAC, Digitale Signaturen, Zertifikate

## Überblick

Vierter Vorlesungsblock. Nach Verschlüsselung folgt die Antwort auf die offenen Schutzziele aus dem Angriffsmodell: **Integrität**, **Authentizität** und **Non-repudiation**. Die Vorlesung baut systematisch von Hash-Funktionen über MACs (HMAC, CMAC) und digitale Signaturen bis zu X.509-Zertifikaten und PKI. Anschließend wird die Frage geklärt, in welcher Reihenfolge signiert und verschlüsselt werden muss („erst signieren, dann verschlüsseln"). Den Abschluss bildet **Perfect Forward Secrecy** und eine Big-Picture-Tabelle, die alle Angriffe gegen alle Schutzbausteine bewertet.

## Lernziele (laut Vorlesung)

*Im PDF nicht als separate Liste ausgewiesen.* Aus dem Aufbau ergeben sich: Hash-Funktionen erklären; MAC, HMAC, CMAC unterscheiden; digitale Signatur-Erstellung und -Verifikation beherrschen; X.509-Zertifikat lesen können; PKI-Bestandteile benennen; PFS verstehen.

## Behandelte Konzepte

### Hash und MAC
- [[ASP - Hash - Funktion]]
- [[ASP - MAC - Grundlagen]]

### Digitale Signaturen
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Digitale Signatur - Reihenfolge sign-encrypt]]

### Zertifikate und PKI
- [[ASP - Zertifikate - X.509]]
- [[ASP - Zertifikate - CSR]]
- [[ASP - Zertifikate - PKI]]
- [[ASP - Zertifikate - Signaturverifikation]]

### Perfect Forward Secrecy & Schlüssel-Sicherheit
- [[ASP - Kryptografie - Perfect Forward Secrecy]]
- [[ASP - Schluesselspeicherung - Hardware Security]]
- [[ASP - Authentifizierung - Level of Assurance]]

### Übersicht
- [[ASP - Schutzmethoden - Uebersicht]]

## Roter Faden

Ausgangsfrage: „Wie schützt man die Integrität (Unveränderbarkeit) von Informationen?" (Folie 2). Erste Antwort: **Hash-Funktion** als mathematische Einwegfunktion mit Kollisionsfreiheit. Sender und Empfänger berechnen unabhängig den Hash der Nachricht und vergleichen sie. Schwäche: Hash schützt nur, wenn der Hash selbst nicht manipulierbar ist – ein Angreifer könnte Nachricht *und* Hash austauschen.

Lösung: **MAC** (Message Authentication Code) bindet eine Hash- oder Verschlüsselungs-Operation an einen geheimen symmetrischen Schlüssel. **HMAC** = Hash + Schlüssel. **CMAC** = letzter Block einer Blockverschlüsselung. Beide setzen voraus, dass beide Seiten den geheimen Schlüssel haben. Schwäche: keine Non-repudiation, da auch der Empfänger den Schlüssel kennt.

Nächster Schritt: **Digitale Signatur**. Statt symmetrischen Schlüssel wird der Private Key des Senders zum Signieren verwendet, der Empfänger verifiziert mit dem Public Key. Damit erreicht man neben Integrität auch Authentizität und Non-repudiation. Die Konstruktion ist: Hash der Nachricht → mit Private Key verschlüsseln = Signatur. Verifizierung: Hash neu berechnen → Signatur mit Public Key entschlüsseln → vergleichen.

Verbleibender Schwachpunkt: Wie weiß ich, dass der Public Key wirklich zur richtigen Person gehört? Lösung: **Digitale Zertifikate** (X.509), ausgestellt von einer **Certification Authority (CA)** im Rahmen einer **Public-Key-Infrastruktur (PKI)**. Der Antragsteller stellt einen **Certificate Signing Request (CSR)**, die CA prüft die Identität und stellt das Zertifikat aus. Eine Signatur-Verifikation hat dann zwei Teile: kryptografische Prüfung (Hash + Signatur) UND Zertifikatsvalidierung (gültig, nicht widerrufen, vertrauenswürdiger Aussteller, korrekte Schlüsselverwendung).

Die Reihenfolge-Frage „erst signieren oder erst verschlüsseln?" wird mit klarem Plädoyer beantwortet: **erst signieren, dann verschlüsseln.** Bei umgekehrter Reihenfolge könnte ein Angreifer die verschlüsselte Nachricht mit eigener Signatur versehen, der Empfänger hielte sich für den richtigen Sender getäuscht.

Letzter offener Punkt aus der Hybrid-Konstruktion: Wird der Private Key später kompromittiert, sind alle aufgezeichneten alten Sessions entschlüsselbar. Lösung: **Perfect Forward Secrecy** – ephemerale ECC-Schlüsselpaare pro Sitzung, mit dem statischen Private Key signiert (für Vertrauen), der symmetrische Sitzungsschlüssel wird per Diffie-Hellman daraus berechnet. Ephemerale Schlüssel und Sitzungsschlüssel werden nach der Kommunikation gelöscht.

Offenes Risiko: Schlüsselspeicherung. Software-Keystores sind unsicher; sichere Erzeugung erfordert spezielle Hardware (Secure Elements, Secure Enclaves, HSMs). Dies bestimmt die Qualität der Authentifizierung – formalisiert als **Level of Assurance (LoA)** in der eIDAS-Verordnung (Low / Medium / High).

Abschluss: Big-Picture-Tabelle (Folie 35) zeigt für alle 8 Angriffe aus dem Modell, welche Schutzbausteine (Hash, MAC, sym/asym Verschlüsselung, Signatur, Hybrid, PFS) sie verhindern.

## Zentrale Aussagen / Take-aways

- **Hash** = mathematische Einwegfunktion, kollisionsfrei. Beispiele: MD2, SHA-256.
- **HMAC** = Hash + symmetrischer Schlüssel. **CMAC** = letzter Block einer Blockchiffre.
- **Digitale Signatur** = Hash der Nachricht, mit Private Key verschlüsselt. Liefert Integrität + Authentizität + Non-repudiation.
- **Identitätsbindung** der Schlüssel über digitale Zertifikate (X.509), ausgestellt durch CA in einer PKI.
- **PKI-Bestandteile:** digitale Zertifikate, CA, RA, Zertifikatssperrliste, Verzeichnisdienst, Validierungsdienst.
- **CSR-Prozess:** Antragsteller erzeugt Schlüsselpaar + CSR, signiert ihn mit Private Key, sendet an CA, erhält Zertifikat zurück.
- **Signatur-Verifikation** hat zwei Teile: kryptografische Verifikation (Signatur + Hash) und Zertifikatsvalidierung (Gültigkeit, Sperrstatus, Schlüsselverwendung, Authentizitäts-Qualität).
- **Reihenfolge:** erst signieren, dann verschlüsseln. Sonst kann Eve eine eigene Signatur über den unveränderten Ciphertext setzen.
- **Perfect Forward Secrecy** mit ephemeren ECC-Schlüsseln und Diffie-Hellman; statischer Private Key dient zum Signieren der ephemeren Public Keys.
- **Schlüsselsicherheit** definiert die Qualität der Authentifizierung; formalisiert als eIDAS-LoA (Low / Medium / High).
- **Big-Picture-Tabelle:** Replay und DoS bleiben auch mit allen Krypto-Bausteinen ungelöst – brauchen Schutz auf Protokollebene (Timestamps, Blackhole Routing).

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Verschluesselungsmethoden]] (liefert symmetrisch/asymmetrisch/hybrid; offene Authentizität wird hier geschlossen)
- [[ASP - VL - Identitaetsmanagement]] (folgt – baut auf Zertifikaten und PKI auf)
- [[MSI - IHE - XUA]] (Cross-Fach: signierte SAML-Assertions verwenden dieselben Bausteine)
- [[EHR - Audit Trail - Grundlagen]] (Cross-Fach: Signaturen erzeugen die Beweismittel für Audit Trails)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/04 Hash, MAC, Digitale Signaturen, Zertifikate/IVL_ADSP_Hash_MAC_HMAC_Digitale_Signaturen_…_SM-X800_Nov-27-0843-2024_1.pdf`
- Folienanzahl: 35
- Vortragender: Dr. Kevin Theuermann
- Datum laut Folien: 29.10.2024
