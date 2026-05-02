---
fach: asp
typ: pruefungsfrage
status: offen
niveau: gemischt
tags:
  - typ/pruefungsfrage
  - status/offen
  - flashcards
  - fach/allgemein/asp
---

# ASP - PF - Kryptografie Ueberblick

> [!note] Hinweis
> Diese Note enthält Karten für das **Spaced Repetition Plugin**.
> - Single-Line-Format: `Frage::Antwort`
> - Multi-Line-Format: Frage, Leerzeile, `?`, Leerzeile, Antwort, Leerzeile, `<!--SR:...-->`
> - Niveau-Konvention im Frontmatter: `definition` · `anwendung` · `diskussion`

## Kontext

Kryptografie-Überblick aus ASP: symmetrische und asymmetrische Verschlüsselung (Prinzip und Vor-/Nachteile), Schlüsselaustausch-Problem, hybride Verschlüsselung, Hash-Funktionen, MAC (HMAC/CMAC), Digitale Signaturen (inkl. sign-then-encrypt), Perfect Forward Secrecy, Hardware-Schlüsselspeicherung und das Big-Picture der Schutzmethoden gegen Angriffe. Detail-Noten zu DES/AES/RSA/ECC sind in separaten Detail-PFs. Quellen: VL Verschlüsselungsmethoden, VL Hash MAC Digitale Signaturen Zertifikate.

## Verlinkte Konzepte

- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Symmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Schluesselaustausch - Problem]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
- [[ASP - Hash - Funktion]]
- [[ASP - MAC - Grundlagen]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Digitale Signatur - Reihenfolge sign-encrypt]]
- [[ASP - Kryptografie - Perfect Forward Secrecy]]
- [[ASP - Schluesselspeicherung - Hardware Security]]
- [[ASP - Schutzmethoden - Uebersicht]]

---

## Karten

### Definition

Frage: Was ist das Schlüsselaustausch-Problem bei symmetrischer Verschlüsselung, und welche zwei Lösungsklassen kennt die Vorlesung?

?

Antwort: Laut Folie 28 (VL Verschlüsselungsmethoden):

**Problem:** Zwei Parteien (Alice, Bob) müssen sich auf einen gemeinsamen geheimen Schlüssel einigen. Die Übertragung dieses Schlüssels muss selbst sicher erfolgen – es gibt aber keinen sicheren Kanal, bevor der Schlüssel ausgetauscht ist. Ein Henne-Ei-Problem.

**Zwei Lösungsklassen laut Vorlesung:**
1. **Asymmetrische Verschlüsselung des symmetrischen Schlüssels** – der Sitzungsschlüssel wird mit dem Public Key des Empfängers verschlüsselt übertragen → Grundidee der hybriden Verschlüsselung.
2. **Kryptografische Schlüsselaustausch-Protokolle** (Diffie-Hellman) – der gemeinsame Schlüssel wird überhaupt nie übertragen, sondern von beiden Seiten unabhängig berechnet.

---

Frage: Welche fünf Eigenschaften muss eine kryptografische Hash-Funktion haben, und wie wird sie zur Integritätsprüfung eingesetzt?

?

Antwort: Laut Folie 5 (VL Hash/MAC/Signaturen):

**Eigenschaften:**
1. Mathematische **Einwegfunktion**
2. **Nicht invertierbar** (vom Hash lässt sich die Eingabe nicht rekonstruieren)
3. **Kollisionsfrei** (zwei verschiedene Eingaben produzieren praktisch nie denselben Hash)
4. **Beliebige Eingabelänge** → feste Ausgabelänge
5. **Deterministisch** (gleiche Eingabe → immer gleicher Hash)

**Integritätsprüfung (Folie 7):**
1. Sender berechnet Hash der Nachricht.
2. Sender überträgt Nachricht + Hash-Wert.
3. Empfänger berechnet Hash der empfangenen Nachricht neu.
4. Vergleich: stimmen beide überein → Nachricht unverändert.

**Schwäche:** Kann ein Angreifer sowohl Nachricht als auch mitgesendeten Hash manipulieren, fällt die Prüfung positiv aus → ohne separaten sicheren Kanal für den Hash braucht es MAC oder Signatur.

---

Frage: Was ist ein MAC, welche zwei Varianten kennt die Vorlesung, und welches Schutzziel liefert er nicht?

?

Antwort: Laut Folie 9 (VL Hash/MAC/Signaturen):

**MAC (Message Authentication Code):** Obergruppe von Verfahren, die Integrität und Authentizität einer Nachricht durch einen geheimen **symmetrischen Schlüssel** sicherstellen.

**Zwei Varianten:**
- **HMAC** (Hash-based MAC): Nachricht → Hash-Funktion → Ergebnis wird mit symmetrischem Schlüssel verschlüsselt.
- **CMAC** (Cipher-based MAC): Nachricht wird im Block-Verschlüsselungs-Modus verarbeitet; der letzte verschlüsselte Block ist der MAC.

**Kernaussage (Folie 9):** Integrität kann nur durch einen bestimmten Empfänger geprüft werden, der im Besitz des symmetrischen Schlüssels ist.

**Nicht geliefertes Schutzziel: Non-repudiation.** Da beide Seiten den Schlüssel kennen, kann der Empfänger die Nachricht theoretisch selbst erzeugt haben → kein Dritter-Beweis möglich.

---

Frage: Was ist eine digitale Signatur, welche drei Schutzziele liefert sie, und welche Schlüssel werden beim Signieren und Verifizieren verwendet?

?

Antwort: Laut Folien 12–13 (VL Hash/MAC/Signaturen):

**Signaturerstellung (Private Key des Senders):**
1. Nachricht erstellen.
2. Hash-Wert der Nachricht berechnen.
3. Hash-Wert mit dem **Private Key** des Senders verschlüsseln → Signatur.
4. Übertragen: Nachricht + Signatur + Public Key (oder Zertifikat).

**Verifikation (Public Key des Senders):**
- Empfänger berechnet Hash der Nachricht neu.
- Entschlüsselt Signatur mit dem **Public Key** des Senders → erhält Original-Hash.
- Stimmen beide Hashes überein: Nachricht unverändert UND nachweislich vom Inhaber des Private Keys.

**Drei Schutzziele:**
- **Integrität** – Manipulation ändert den Hash, Verifikation schlägt fehl.
- **Authentizität** – nur der Private-Key-Inhaber kann signieren.
- **Non-repudiation** – Sender kann Urheberschaft nicht abstreiten.

---

### Anwendung

Frage: Skizzieren Sie den Ablauf hybrider Verschlüsselung. Welche zwei Probleme der reinen Verfahren löst sie – und welche Schwäche bleibt?

?

Antwort: Laut Folien 54–55 (VL Verschlüsselungsmethoden):

**Ablauf (6 Schritte):**
1. Alice erzeugt zufällig einen symmetrischen Sitzungsschlüssel.
2. Alice verschlüsselt die Nachricht **symmetrisch** mit diesem Schlüssel → Ciphertext.
3. Alice verschlüsselt den Sitzungsschlüssel **asymmetrisch** mit Bobs Public Key.
4. Alice sendet: verschlüsselte Nachricht + verschlüsselter Sitzungsschlüssel.
5. Bob entschlüsselt den Sitzungsschlüssel asymmetrisch mit seinem Private Key.
6. Bob entschlüsselt die Nachricht symmetrisch.

**Gelöste Probleme:**
- **Schlüsselaustausch-Problem** (aus symmetrisch) → der Sitzungsschlüssel wird sicher per asymmetrischer Verschlüsselung übertragen.
- **Performance-Problem** (aus asymmetrisch) → die eigentliche Nachricht wird symmetrisch verschlüsselt.

**Verbleibende Schwäche (Folie 55):** Keine Authentizität! Hybride Verschlüsselung allein sagt nichts darüber aus, *von wem* die Nachricht stammt. Lösung: zusätzliche Signatur.

---

Frage: Was ist Perfect Forward Secrecy (PFS), welchen Angriff verhindert es, und welche Schlüsselarten kommen laut Vorlesung zum Einsatz?

?

Antwort: Laut Folien 28–31 (VL Hash/MAC/Signaturen):

**PFS verhindert:** Den Angriff „Aufzeichnung + späterer Schlüsseldiebstahl" – Eve zeichnet verschlüsselte Kommunikation auf und entschlüsselt sie, sobald sie Bobs statischen Private Key stiehlt.

**Konstruktion:**
- Beide Parteien haben **statische** asymmetrische Schlüsselpaare (ECC oder RSA).
- Vor jeder Kommunikation werden **ephemerale ECC-Schlüsselpaare** erzeugt.
- Die ephemeralen Public Keys werden ausgetauscht und **mit dem statischen Private Key signiert** (Vertrauensanker).
- Der symmetrische Sitzungsschlüssel wird über **Diffie-Hellman** aus den ephemeralen Schlüsseln berechnet.
- Nach der Sitzung werden ephemerales Schlüsselpaar und Sitzungsschlüssel **gelöscht**.

**Warum das funktioniert:** Auch mit gestohlenem statischem Private Key kann Eve die gelöschten ephemeralen Schlüssel nicht rekonstruieren → vergangene Sitzungen bleiben geschützt.

**Hinweis der Vorlesung:** RSA zu langsam für ephemerale Schlüssel → ECC wird verwendet.

---

Frage: Warum muss man zuerst signieren und dann verschlüsseln? Skizzieren Sie das Angriffsszenario bei umgekehrter Reihenfolge.

?

Antwort: Laut Folien 24–26 (VL Hash/MAC/Signaturen):

**Angriffsszenario „erst verschlüsseln, dann signieren":**
1. Alice verschlüsselt Nachricht mit Bobs Public Key.
2. Alice signiert den Ciphertext mit ihrem Private Key.
3. Eve fängt verschlüsselte Nachricht + Alice-Signatur ab.
4. Eve **streift Alice' Signatur ab** und erzeugt eine neue Signatur mit ihrem eigenen Private Key über denselben (unveränderten) Ciphertext.
5. Eve sendet verschlüsselte Nachricht + eigene Signatur + eigenen Public Key an Bob.
6. Bob verifiziert Eves Signatur erfolgreich und glaubt, die Nachricht stamme von Eve – obwohl der Inhalt unverändert von Alice stammt.

**Gebrochenes Schutzziel:** Authentizität / Non-repudiation; Vertraulichkeit bleibt erhalten.

**Richtige Reihenfolge: sign-then-encrypt** – die Signatur wird mit verschlüsselt; Eve sieht weder Klartext noch Signatur und kann die Urheberschaft nicht fälschen.

---

### Diskussion

Frage: Welche Angriffe können durch kryptografische Bausteine (Hash, MAC, sym/asym, Signatur, Hybrid, PFS) nicht verhindert werden – und warum grundsätzlich nicht?

?

Antwort: Laut Folie 35 (VL Hash/MAC/Signaturen – Schutzmethoden-Matrix):

**Nicht verhindert durch Kryptografie:**
- **Replay** – kein Krypto-Baustein verhindert die Wiedereinspielung einer (unveränderten, gültigen) Nachricht. Gegenmittel: **Protokollebene** (Timestamps, Nonces, Sequenznummern).
- **Nachricht unterdrücken / DoS** – kein Krypto-Baustein verhindert, dass Nachrichten schlicht verworfen werden. Gegenmittel: **Netzwerk-/Infrastrukturebene** (z. B. Blackhole Routing gegen DDoS).

**Grundsätzlicher Unterschied:** Kryptografie schützt den **Inhalt** einzelner Nachrichten. Replay und DoS sind Eigenschaften des **Nachrichtenflusses** – wann und ob Nachrichten ankommen. Das ist eine andere Abstraktionsebene.

**Weiterer Befund aus der Matrix:** Reine Verschlüsselung (symmetrisch/asymmetrisch/hybrid) schützt nicht gegen Modifikation des Ciphertexts und nicht gegen Impersonation – dafür ist Signatur nötig.

---

Frage: Warum reicht ein Software-Keystore für kryptografische Schlüssel nicht aus, und welche Konsequenz hat ein unsicherer Keystore für PFS?

?

Antwort: Laut Folie 32 (VL Hash/MAC/Signaturen):

**Software-Keystore:** liegt in normalen Betriebssystem-Speicherbereichen → durch Malware oder Speicher-Auslesefehler angreifbar.

**Sichere Hardware-Alternativen laut Vorlesung:**
- **Secure Element (Android)** / **Secure Enclave (iOS)** – für mobile Geräte.
- **Key Attestation** – Beweis, dass der Schlüssel wirklich in Hardware erzeugt wurde.
- **HSM (Hardware Security Module)** – für Server-Umgebungen.

**Konsequenz für PFS:** Werden ephemerale Schlüssel aus einem unsicheren Software-Speicher abgegriffen, kann die zugehörige Sitzung entschlüsselt werden – PFS bricht für diese Sitzung zusammen. Vergangene und zukünftige Sitzungen mit sauberen Schlüsseln bleiben jedoch geschützt.

**Verbindung zu LoA:** Die Schlüssel-Speicherung beeinflusst direkt den **Level of Assurance** einer Authentifizierung (eIDAS).

---

Frage: In welchen Situationen würden Sie für ein eHealth-System eine Kombination welcher Krypto-Bausteine empfehlen – und welche verbleibenden Lücken müssten außerkryptografisch geschlossen werden?

?

Antwort: Aus dem Big-Picture der Vorlesung (Folie 35 + Folie 55, VL Hash/MAC/Signaturen):

**Vollständige Abdeckung aller kryptografisch lösbaren Angriffe:**
- **Hybride Verschlüsselung** → Vertraulichkeit + Schlüsselaustausch-Problem gelöst.
- **Digitale Signatur (sign-then-encrypt)** → Authentizität + Integrität + Non-repudiation.
- **PFS mit ephemeralen ECC-Schlüsseln** → Schutz gegen nachträglichen Schlüsseldiebstahl.
- **Hardware-Keystore (SE/HSM)** → Schlüssel können nicht abgegriffen werden.

**Verbleibende Lücken (kryptografisch nicht lösbar):**
- **Replay** → Timestamps / Nonces auf Protokollebene.
- **DoS / Nachricht unterdrücken** → Netzwerkebene (z. B. Rate Limiting, DDoS-Schutz).
- **Zugriffskontrolle nach Authentifizierung** → Berechtigungsmodelle (RBAC/ABAC).

*(Diese Kombination entspricht in der Praxis dem Aufbau von TLS 1.3 + qualifizierter Signatur; im PDF nicht explizit so bezeichnet.)*

---

### Vergleich

Frage: Vergleichen Sie Hash, MAC und Digitale Signatur: Welche Schutzziele liefert jeder Baustein, welchen nicht?

?

Antwort: Aus den Notes (VL Hash/MAC/Signaturen):

| Baustein | Schlüsselart | Vertraulichkeit | Integrität | Authentizität | Non-repudiation |
|---|---|---|---|---|---|
| Hash | kein Schlüssel | ❌ | ✅ (wenn separat gesichert) | ❌ | ❌ |
| MAC (HMAC/CMAC) | symmetrisch (geteilt) | ❌ | ✅ | ✅ (gegenüber Schlüsselpartner) | ❌ |
| Digitale Signatur | asymmetrisch (privat/öffentlich) | ❌ | ✅ | ✅ | ✅ |

**Kernunterschied Hash ↔ MAC:** MAC bindet einen geheimen Schlüssel ein – Eve kann ohne Schlüssel keinen gültigen MAC berechnen. Ein reiner Hash kann von Eve für eine manipulierte Nachricht ebenso berechnet werden.

**Kernunterschied MAC ↔ Signatur:** Signatur verwendet asymmetrische Schlüssel → nur der Inhaber des Private Keys kann signieren. MAC hat geteilten Schlüssel → beide Seiten könnten die Nachricht erzeugt haben → keine Non-repudiation.

---

Frage: Vergleichen Sie symmetrische und asymmetrische Verschlüsselung anhand von Schlüsselverwaltung, Performance, Skalierung und Authentifizierung.

?

Antwort: Aus Folien 9 und 34 (VL Verschlüsselungsmethoden):

| Kriterium | Symmetrisch | Asymmetrisch |
|---|---|---|
| Schlüsselverwaltung | Ein gemeinsamer Schlüssel pro Paar; Verteilung schwierig | Schlüsselpaar pro Teilnehmer; Public Key öffentlich verteilbar |
| Performance | Sehr hoch (effiziente Operationen) | Ca. 10.000–100.000× langsamer |
| Skalierung | Schlecht: n·(n-1)/2 Schlüssel für n Teilnehmer | Gut: n Schlüsselpaare |
| Schlüsselaustausch | Problem – sicherer Kanal nötig | Gelöst – Public Key öffentlich |
| Authentifizierung | Nicht direkt möglich | Ja, über Signatur mit Private Key |
| Mehrere Empfänger | Selbe Nachricht (ein Schlüssel) | Pro Empfänger eine eigene Verschlüsselung |

**Konsequenz:** Kein reines Verfahren ist für alle Aufgaben optimal → **Hybride Verschlüsselung** kombiniert die Stärken beider.

---

## Mögliche Anschlussfragen des Prüfers

- Welcher kryptografische Baustein baut auf welchem anderen auf? (Hash → MAC/Signatur; DH + Signatur + sym → PFS)
- Warum kann reine symmetrische Verschlüsselung keine Authentizität liefern?
- Erklären Sie das Pay-TV-Beispiel und seine Schwäche als Illustration des Schlüsselaustausch-Problems.
- Welche verbleibenden Schwächen hat hybride Verschlüsselung ohne Signatur – und wie werden sie geschlossen?
- Welcher Angriff rechtfertigt den Mehraufwand von PFS, und warum ist das für eHealth besonders relevant?
- Warum werden für ephemerale PFS-Schlüssel ECC und nicht RSA verwendet?
- Welcher Schutz bleibt auch nach dem vollständigen Krypto-Stack Replay und DoS?

## Eigene Notizen

*Wo bin ich beim Üben unsicher geworden? Was muss ich nochmal nachschlagen?*
