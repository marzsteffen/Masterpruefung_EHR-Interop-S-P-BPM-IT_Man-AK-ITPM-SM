---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/02 Symetrische Verschlüsselungsmethoden/IVL_ADSP_Symmetrische_Verschlüsselungsmethoden.pdf
datum_vorlesung: 2024-10-23
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Verschlüsselungsmethoden

## Überblick

Zweiter Block der Vorlesung Advanced Security and Privacy. Dieser PDF deckt trotz seines Dateinamens alle drei Verschlüsselungsfamilien ab: **symmetrische**, **asymmetrische** und **hybride** Verschlüsselung. Aufbau: jeweils Prinzip, konkrete Algorithmen, Vor- und Nachteile sowie Bewertung gegen das Angriffsmodell aus der Einführungs-Vorlesung. Die zentrale Lehre: jede Familie für sich hat Schwächen, in der Praxis kombiniert man sie hybrid – und ergänzt eine Signatur, um auch Authentizität zu sichern.

## Lernziele (laut Vorlesung)

*Im PDF nicht explizit als Lernziel-Liste ausgewiesen.* Aus dem Vorlesungsplan (Kapitel 01, Folie 4) hervorgehende Ziele: symmetrische, asymmetrische und hybride Verschlüsselung verstehen, Detailkenntnisse zu DES/3DES/AES, RSA/ECC, Diffie-Hellman, sowie Bewertung gegen das Angriffsmodell.

## Behandelte Konzepte

### Symmetrische Verschlüsselung
- [[ASP - Symmetrische Verschluesselung - Geschichte]]
- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Symmetrische Verschluesselung - Stromchiffre]]
- [[ASP - Symmetrische Verschluesselung - Blockchiffre]]
- [[ASP - Symmetrische Verschluesselung - Unterscheidungsmerkmale]]
- [[ASP - Symmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Symmetrische Verschluesselung - DES]]
- [[ASP - Symmetrische Verschluesselung - Feistel-Funktion]]
- [[ASP - Symmetrische Verschluesselung - S-Box]]
- [[ASP - Symmetrische Verschluesselung - Triple-DES]]
- [[ASP - Symmetrische Verschluesselung - AES]]
- [[ASP - Symmetrische Verschluesselung - Angriffsmodell]]

### Übergang Schlüsselaustausch
- [[ASP - Schluesselaustausch - Problem]]

### Asymmetrische Verschlüsselung
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Asymmetrische Verschluesselung - Faktorisierungsproblem]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]
- [[ASP - Asymmetrische Verschluesselung - Angriffsmodell]]

### Hybride Verschlüsselung
- [[ASP - Hybride Verschluesselung - Grundlagen]]

## Roter Faden

Die Vorlesung baut zuerst die symmetrische Verschlüsselung als historisch älteste und performance-stärkste Familie auf. Über Geschichte (Cäsar, Enigma) und das Prinzip (gleicher Schlüssel auf beiden Seiten) führt sie zur Strom/Block-Unterscheidung und dann zu konkreten Algorithmen: DES (1977, 56-Bit, abgelöst), Triple-DES (Übergangslösung mit 168 Bit) und AES (seit 2000, NIST-Standard, heute meistgenutzt). Bewertet gegen das Angriffsmodell zeigt sich: symmetrische Verschlüsselung allein verhindert nur „Nachricht lesen" (und „Verändern Plaintext", weil keine Klartext-Modifikation mehr möglich ist) – andere Angriffe bleiben offen. Ihr größter Schwachpunkt ist das **Schlüsselaustausch-Problem**: Wie vereinbaren zwei Parteien einen gemeinsamen Schlüssel über einen unsicheren Kanal?

Genau dieses Problem motiviert die **asymmetrische Verschlüsselung** mit Schlüsselpaaren aus Public und Private Key. Die Vorlesung zeigt zwei Lösungswege: (a) den Public Key des Empfängers verwenden, um einen symmetrischen Sitzungsschlüssel verschlüsselt zu übertragen; (b) ein dedizierter Schlüsselaustausch wie Diffie-Hellman-Merkle, bei dem der gemeinsame Schlüssel überhaupt nie übertragen, sondern auf beiden Seiten *berechnet* wird. Konkrete Algorithmen: RSA (basiert auf dem Faktorisierungsproblem) und ECC (basiert auf elliptischen Kurven, viel kleinere Schlüssellängen). Asymmetrische Verfahren sind ca. 100.000-mal langsamer als symmetrische und brauchen pro Empfänger eine separate Verschlüsselung.

Die **hybride Verschlüsselung** kombiniert beide: ein zufälliger symmetrischer Schlüssel wird mit dem Public Key des Empfängers asymmetrisch verschlüsselt und übertragen, die eigentliche Nachricht wird dann symmetrisch verschlüsselt. So vereinen sich Performance der symmetrischen mit der Schlüsselverteilung der asymmetrischen Verfahren. Letzte offene Lücke: keine Authentizität – wird durch eine zusätzliche digitale Signatur über die Nachricht gelöst (siehe Kapitel 04).

## Zentrale Aussagen / Take-aways

- **Symmetrisch:** ein Schlüssel für Ver- und Entschlüsselung. Schnell, aber Schlüsselaustausch ist das Hauptproblem; Anzahl der Schlüssel wächst quadratisch mit der Anzahl der Teilnehmer.
- **Stromchiffre vs. Blockchiffre:** Strom verschlüsselt bitweise (XOR), eignet sich für Echtzeit; Block verschlüsselt feste Bit-Blöcke unabhängig voneinander, parallelisierbar, höhere Sicherheit gegen Manipulation.
- **DES:** 56-Bit-Schlüssel, 64-Bit-Block, 16 Feistel-Runden mit S-Boxen, durch AES abgelöst.
- **Triple-DES:** dreimalige DES-Anwendung mit drei unabhängigen Schlüsseln, 168 Bit Schlüssellänge, EDE-Schema (Encrypt-Decrypt-Encrypt).
- **AES:** NIST-Standard seit 2000, 16-Byte-Block, mehrere Runden mit SubBytes, ShiftRows, MixColumns, AddRoundKey. 128 Bit Schlüssel praktisch unknackbar.
- **Asymmetrisch:** Schlüsselpaar Public/Private. Public Key öffentlich, Private Key bleibt beim Besitzer. Eine Nachricht, die mit dem einen Schlüssel verschlüsselt ist, kann nur mit dem anderen entschlüsselt werden.
- **Diffie-Hellman-Merkle:** Schlüsselaustausch ohne Schlüssel-Übertragung – beide Seiten berechnen denselben Schlüssel aus öffentlich übertragenen Zwischenergebnissen plus eigener geheimer Zufallszahl.
- **RSA:** Sicherheit basiert auf dem Faktorisierungsproblem großer Primzahlprodukte. Empfehlung mind. 2048 Bit. Quantencomputer-anfällig.
- **ECC:** Sicherheit basiert auf elliptischen Kurven; deutlich kürzere Schlüssel (128–256 Bit) bei vergleichbarer Sicherheit.
- **Hybride Verschlüsselung:** löst Schlüsselaustausch *und* Performance, lässt aber Authentizität offen → Signatur ergänzen.

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Einfuehrung und Motivation]] (liefert Angriffsmodell und Schutzziele)
- [[ASP - VL - Asymmetrische Verschluesselung]] (folgt – vermutete Vertiefung in Kapitel 03)
- [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (folgt – schließt die offene Authentizitäts-Lücke)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/02 Symetrische Verschlüsselungsmethoden/IVL_ADSP_Symmetrische_Verschlüsselungsmethoden.pdf`
- Folienanzahl: 56
- Vortragender: Dr. Kevin Theuermann
- Datum laut Folien: 25.10.2023 (Erstellungsdatum) – im Vorlesungsplan auf 23.10.2024 terminiert
- Hinweis: PDF behandelt trotz Dateiname und Ordnername „Symmetrische Verschlüsselung" zusätzlich asymmetrische und hybride Verschlüsselung.

**Wiederholung am 28.10.2024:** Kapitel 03 (`IVL_ADSP_Asymmetrische_Verschlüsselung_…pdf`, 30 Folien) wiederholt den asymmetrischen + hybriden Teil dieser Vorlesung weitgehend deckungsgleich. Inhaltliche Ergänzungen, die nur in Kapitel 03 stehen, sind in den jeweiligen Konzept-Notes markiert (DH/diskreter Logarithmus; zwei Anwendungsfälle der asymmetrischen Verschlüsselung als „Schutz der Vertraulichkeit" und „Schutz der Integrität/Unveränderbarkeit"). Keine eigenständige Vorlesungs-Note für Kapitel 03 angelegt.
