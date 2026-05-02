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

# ASP - PF - Asymmetrische Verschlüsselung Detail

## Kontext

Prüfungskarten für die mündliche Masterprüfung ASP. Thema: Asymmetrische Verschlüsselung – Prinzip, Verfahren (RSA, ECC, DH-Merkle), Hybride Verschlüsselung, Vor-/Nachteile, Angriffsmodell. Grundlage: Kapitel 02 und Kapitel 03 der Vorlesung (Folien 31–55 in Kap 02 / Folien 6–29 in Kap 03).

## Verlinkte Konzepte

- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - Vor- und Nachteile]]
- [[ASP - Asymmetrische Verschluesselung - RSA]]
- [[ASP - Asymmetrische Verschluesselung - Faktorisierungsproblem]]
- [[ASP - Asymmetrische Verschluesselung - ECC]]
- [[ASP - Asymmetrische Verschluesselung - Diffie-Hellman-Merkle]]
- [[ASP - Asymmetrische Verschluesselung - Angriffsmodell]]
- [[ASP - Schluesselaustausch - Problem]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]

---

## Karten

### Definition

Was kennzeichnet asymmetrische Verschlüsselung, und welche zwei Anwendungsfälle hat ein Schlüsselpaar?

?

Jede Partei hat ein **Schlüsselpaar** (Public Key + Private Key). Was mit dem einen verschlüsselt wird, kann nur mit dem anderen entschlüsselt werden. Der Public Key darf global ungeschützt verteilt werden; der Private Key verlässt den Besitzer nie.

**Anwendungsfall 1 – Vertraulichkeit:** Klartext mit **Public Key des Empfängers** verschlüsseln → nur dessen Private Key kann entschlüsseln.

**Anwendungsfall 2 – Integrität / Unveränderbarkeit:** Klartext mit **Private Key des Senders** verschlüsseln → jeder mit dem Public Key kann verifizieren, dass die Nachricht vom Inhaber des Private Keys stammt. Das ist die Grundlage digitaler Signaturen (liefert gleichzeitig Authentizität, Integrität und Non-repudiation).

*(Erste asymmetrische Verschlüsselung 1976, RSA 1977 – Folie 31)*

---

Was sind die Eckdaten von RSA, und wie lauten die Formeln für Ver- und Entschlüsselung?

?

| Merkmal | Wert |
|---|---|
| Veröffentlicht | 1977 |
| Erfinder | Rivest, Shamir, Adleman |
| Sicherheitsbasis | **Faktorisierungsproblem** großer Primzahlprodukte |
| Schlüssellänge (Empfehlung) | mind. **2048 Bit** |
| Anwendung | Verschlüsselung + Signaturverfahren |
| Performance | ca. **Faktor 100 (und mehr) langsamer** als sym. 3DES/AES (Folie 41) |
| Public Key | (e, N) |
| Private Key | (d, N) |

**Verschlüsseln:** `c = mᵉ mod N`
**Entschlüsseln:** `m = cᵈ mod N`

Beispiel (Folie 44): m=9, e=47, N=77 → c = 9⁴⁷ mod 77

---

Was ist Diffie-Hellman-Merkle, und was kann es – und was ausdrücklich nicht?

?

**Diffie-Hellman-Merkle (1976):** Kryptografisches Verfahren zur **Berechnung eines gemeinsamen Schlüssels**, ohne diesen je zu übertragen. Beide Parteien berechnen aus öffentlich übertragenen Zwischenwerten und einer geheim gehaltenen Zufallszahl je denselben Schlüssel.

**Kann:** Schlüsselvereinbarung (Schlüsselaustausch).

**Kann nicht: Eignet sich NICHT zur Erstellung digitaler Signaturen.**

**Mathematische Grundlage (Kap 03, Folie 7):** Multiplikation leicht berechenbar, Umkehrung – der **diskrete Logarithmus** – extrem schwierig.

Öffentlich übertragen werden: p, g, A, B.
Privat bleiben: a, b, K.

---

Was ist ECC, seit wann ist es NIST-Standard, und auf welchem mathematischen Problem basiert seine Sicherheit?

?

**ECC (Elliptic Curve Cryptography, Mitte 1980, NIST-Standard seit 1999):**

- Asymmetrisches Verfahren für Schlüsselaustausch und Signatur.
- Basiert auf **Punkten auf elliptischen Kurven** (Menge von (x,y)-Punkten).
- **Wichtige Eigenschaft (Folie 47):** Eine Gerade (Tangente) schneidet die Kurve in 3 Punkten → Punkt-Addition R = P + Q.
- **Skalare Multiplikation:** n·P ergibt einen anderen Punkt auf der Kurve. Die Zahl n lässt sich praktisch nicht rückrechnen → **Hardness-Annahme: diskreter Logarithmus auf elliptischen Kurven**.
- **Schlüssellängen:** 128, 192, 256 Bit – deutlich kürzer als RSA bei vergleichbarer Sicherheit.

---

### Anwendung

Skizziere den Datenfluss bei asymmetrischer Verschlüsselung für Vertraulichkeit (Alice → Bob).

?

1. Bob veröffentlicht seinen **Public Key** (global, ungeschützt).
2. Alice verschlüsselt die Nachricht mit **Bobs Public Key** → Ciphertext.
3. Ciphertext wird über das (unsichere) Internet übertragen.
4. Bob entschlüsselt mit seinem **Private Key** → Klartext.

**Entscheidend:** Alice benötigt keinen vorher ausgetauschten geheimen Schlüssel. Das löst das Schlüsselaustausch-Problem. Nur Bob kann die Nachricht lesen, solange sein Private Key geheim bleibt.

*(Folie 33)*

---

Rechne das DH-Merkle-Protokoll mit p=11, g=6, a=3, b=6 durch. Welche Werte sind öffentlich, welche privat?

?

**Schritt-für-Schritt (Folie 38):**

| Schritt | Alice | Bob |
|---|---|---|
| Öffentliche Parameter | p=11, g=6 | erhält p, g |
| Geheime Zufallszahl | a=3 | b=6 |
| Öffentlicher Wert | A = 6³ mod 11 = **7** | B = 6⁶ mod 11 = **5** |
| Übertragung | sendet A=7 | sendet B=5 |
| Gemeinsamer Schlüssel | K1 = 5³ mod 11 = **4** | K2 = 7⁶ mod 11 = **4** |

**Öffentlich:** p, g, A, B.
**Privat:** a, b, K (=4).

Beide berechnen denselben Schlüssel K, ohne ihn je übertragen zu haben.

---

Erkläre den 6-Schritte-Ablauf hybrider Verschlüsselung, und welches Problem bleibt offen?

?

**Ablauf (Folie 54):**
1. Alice erzeugt zufällig einen **symmetrischen Sitzungsschlüssel**.
2. Alice verschlüsselt die Nachricht **symmetrisch** mit diesem Schlüssel → Ciphertext.
3. Alice verschlüsselt den Sitzungsschlüssel **asymmetrisch** mit **Bobs Public Key**.
4. Alice sendet **beides** (Ciphertext + verschlüsselter Sitzungsschlüssel) an Bob.
5. Bob entschlüsselt den Sitzungsschlüssel asymmetrisch mit seinem **Private Key**.
6. Bob entschlüsselt die Nachricht symmetrisch mit dem so gewonnenen Sitzungsschlüssel.

**Gelöste Probleme:** Schlüsselaustausch-Problem (der sym. Schlüssel reist verschlüsselt) + Performance-Problem (Nachricht selbst symmetrisch).

**Offenes Problem (Folie 55): Keine Authentizität!** – Der Aufbau sagt nichts darüber aus, *von wem* die Nachricht stammt.
**Lösung:** Alice signiert die Nachricht zusätzlich mit ihrem Private Key; Bob verifiziert mit Alice' Public Key.

---

Wie bewertet Folie 51 die acht Angriffe unter asymmetrischer Verschlüsselung?

?

**Annahmen (Folie 50):** Schlüssel nicht kompromittiert, kryptografische Primitive sicher; Angreifer befindet sich in der Kommunikationsverbindung.

| Angriff | Bewertung | Begründung (Folie 51) |
|---|---|---|
| Nachricht lesen | ✅ verhindert | Daten werden verschlüsselt |
| Traffic Analysis | ⚠️ szenarioabhängig | Meta-Infos extrahierbar (z. B. Datenmenge RSA > ECC verrät Algorithmus) |
| Aufzeichnung + Entschlüsselung | ❌ erfolgreich | Aufzeichnung + gestohlener Schlüssel reicht |
| Replay | ❌ erfolgreich | Verschlüsselung allein verhindert keinen Replay-Angriff |
| Modifikation Plaintext | ✅ verhindert | Daten verschlüsselt, Modifikation nicht möglich |
| Modifikation Ciphertext | ❌ erfolgreich | Angreifer kann Ciphertext hinzufügen |
| Impersonation | ⚠️ szenarioabhängig | Asym. Verschlüsselung allein gewährleistet keine Authentizität |
| DoS | ❌ erfolgreich | Möglich |

**Fazit:** Bild nahezu identisch mit symmetrischer Verschlüsselung. Der echte Mehrwert liegt im Schlüsselaustausch und in der Signatur, nicht in dieser Tabelle.

---

### Diskussion

Erklären Sie das Faktorisierungsproblem als Sicherheitsbasis von RSA und seine Achillesferse.

?

**Grundprinzip (Folie 42):**
- Zwei große Primzahlen p und q zu multiplizieren ist einfach: 317 × 443 = 140 431.
- Aus dem Produkt N = p·q die Primfaktoren zurückzugewinnen, ist bei 600–1200-stelligen Zahlen in vertretbarer Zeit **praktisch nicht machbar** (klassisch).

**Zwei Sicherheitsanforderungen an RSA-Schlüsselerzeugung:**
1. Schlüssellänge groß genug (Empfehlung: mind. 2048 Bit).
2. Primzahlen aus einem **ausreichend großen, nicht vorhersagbaren Pool** (Zufallsgenerator-Qualität). Folie 42 illustriert: 100 Primzahlen (unsicher) vs. 100 000 Primzahlen (sicher).

**Achillesferse:** Laut Folie 42 explizit: **durch Quantencomputer gefährdet!** (rot markiert) – ein hinreichend großer Quantencomputer könnte RSA-Schlüssel brechen.

---

Warum reicht asymmetrische Verschlüsselung allein nicht aus, und welche Bausteine schließen die Lücken?

?

**Offene Angriffe trotz asymmetrischer Verschlüsselung:**
- **Replay:** Verschlüsselung gibt jeder Nachricht keine Frische-Garantie.
- **Modifikation Ciphertext:** Ein Angreifer kann Ciphertext einschleusen.
- **Impersonation:** Es wird keine Aussage gemacht, *wer* die Nachricht geschickt hat.
- **DoS:** Unterdrückung von Nachrichten nicht verhindert.

**Lücken und ihre Lösungen:**
| Lücke | Lösung |
|---|---|
| Authentizität (wer hat die Nachricht gesendet?) | Digitale Signatur (Private Key des Senders) |
| Frische / Replay | Nonce oder Zeitstempel im Protokoll |
| Ciphertext-Manipulation | Digitale Signatur oder MAC |
| Schlüsselkompromittierung = alle Sitzungen lesbar | Perfect Forward Secrecy (ephemere Schlüssel) |

**Fazit (Folie 51):** Der Wechsel von symmetrisch zu asymmetrisch bringt *für sich allein* keinen großen Sicherheitsgewinn – der echte Mehrwert liegt im Schlüsselaustausch und in der Signaturfähigkeit.

---

Welche zwei grundlegenden Klassen von Lösungen für das Schlüsselaustausch-Problem kennt die Vorlesung, und wie unterscheiden sie sich?

?

Das Schlüsselaustausch-Problem (Folie 28): Für symmetrische Verschlüsselung muss ein gemeinsamer geheimer Schlüssel vereinbart werden, aber der Übertragungskanal dafür ist unsicher.

**Lösung 1 – Asymmetrische Verschlüsselung des symmetrischen Schlüssels (hybride Verschlüsselung):**
- Alice erzeugt einen symmetrischen Sitzungsschlüssel und verschlüsselt ihn mit Bobs Public Key.
- Bob entschlüsselt ihn mit seinem Private Key.
- Der symmetrische Schlüssel wird übertragen – aber verschlüsselt.

**Lösung 2 – Diffie-Hellman-Merkle:**
- Der symmetrische Schlüssel wird **nie übertragen**.
- Beide Parteien berechnen ihn unabhängig aus öffentlich ausgetauschten Zwischenwerten.
- Unterschied: DH ermöglicht Perfect Forward Secrecy (mit ephemeren Schlüsseln), RSA-basierter Schlüsseltransport hingegen nicht.

*(Folien 28/29 + 37/53)*

---

### Vergleich

Vergleiche RSA und ECC hinsichtlich Sicherheitsbasis, Schlüssellänge und Einsatzgebiet.

?

| Aspekt | RSA | ECC |
|---|---|---|
| Veröffentlicht | 1977 | Mitte 1980 (NIST-Standard 1999) |
| Sicherheitsbasis | Faktorisierungsproblem (N = p·q) | Diskreter Logarithmus auf elliptischen Kurven |
| Empfohlene Schlüssellänge | mind. 2048 Bit | 128 / 192 / 256 Bit |
| Performance | Langsamer (größere Schlüssel, aufwändigere Operationen) | Schneller bei gleicher Sicherheit |
| Anwendung | Verschlüsselung + Signatur | Schlüsselaustausch + Signatur |
| Einsatzgebiet | Weit verbreitet, einfacher zu implementieren | Mobile, IoT, Smartcards, modernes TLS |
| Quantencomputer | Gefährdet (Folie 42) | Ebenfalls gefährdet (Shor-Algorithmus) |

**Faustformel:** ECC bietet mit deutlich kürzeren Schlüsseln vergleichbare Sicherheit, weil der beste bekannte Angriff auf den elliptischen diskreten Logarithmus ineffizienter ist als die Faktorisierungs-Algorithmen auf RSA.

---

Vergleiche DH-Merkle und RSA hinsichtlich Zweck, Signatureignung und Schlüsselübertragungs-Modell.

?

| Aspekt | Diffie-Hellman-Merkle | RSA |
|---|---|---|
| Hauptzweck | Schlüsselvereinbarung | Verschlüsselung + Signatur |
| Signatur möglich? | **Nein** – explizit nicht geeignet (Folie 37) | **Ja** |
| Schlüsselübertragung | Kein Schlüssel übertragen; wird beidseitig berechnet | Schlüssel wird asymmetrisch verschlüsselt übertragen (hybride Konstr.) |
| Sicherheitsbasis | Diskreter Logarithmus modulo p | Faktorisierungsproblem |
| Perfect Forward Secrecy | Möglich mit ephemeren Werten (DHE/ECDHE) | Nicht mit klassischem Schlüsseltransport |
| Anfang | 1976 | 1977 |

---

Erstelle eine Vergleichstabelle: Symmetrisch vs. Asymmetrisch vs. Hybrid.

?

| Aspekt | Symmetrisch | Asymmetrisch | Hybrid |
|---|---|---|---|
| Schlüssel | 1 geteilter Schlüssel | Public/Private-Key-Paar | Sym. Sitzungsschlüssel + asym. Transport |
| Performance | Sehr schnell | 10.000–100.000× langsamer | Schnell (Inhalt sym., Schlüssel asym.) |
| Schlüsselaustausch-Problem | ❌ ungelöst | ✅ gelöst | ✅ gelöst |
| Authentifizierung (Signatur) | ❌ nicht möglich | ✅ möglich (Private Key signiert) | ✅ möglich (mit Signatur kombinierbar) |
| Skalierung (n Teilnehmer) | n·(n-1)/2 Schlüssel | n Schlüsselpaare | n Schlüsselpaare |
| Mehrere Empfänger | Gleicher Schlüssel | Je Empfänger extra verschlüsseln | Sym. Ciphertext 1×; Sitzungsschlüssel je Empfänger |
| Offenes Problem | Schlüsselaustausch, Authentizität | Authentizität (ohne Signatur), Performance | Authentizität (ohne zusätzliche Signatur) |
| Typische Verfahren | AES, 3DES | RSA, ECC, DH-Merkle | TLS (ECDHE + AES-GCM) |

*(Folien 27/34/52/53–55)*

---

## Mögliche Anschlussfragen

- Welche Anwendungsfälle nennt die Vorlesung für asymmetrische Verschlüsselung? (TLS, HTTPS, digitale Signatur)
- Warum verlässt der Private Key den Besitzer in der Regel nie?
- Was ist der diskrete Logarithmus, und in welchen Verfahren ist er die Sicherheitsbasis? (DH: modulo p; ECC: auf elliptischen Kurven)
- Welche Schwäche bleibt bei hybride Verschlüsselung ohne Signatur? (Keine Authentizität)
- Warum ist Pay-TV trotz Schlüsselverteilung per Chipkarte unsicher? (Chipkarte gibt keine Authentizität – kann von jedem genutzt werden)
- Wie hängt Perfect Forward Secrecy mit ephemeren DH-Schlüsseln zusammen? (Jede Sitzung neuer a, b → K kompromittiert nur diese Sitzung)
- Was unterscheidet RSA-Schlüsseltransport von DH-Schlüsselvereinbarung in Bezug auf PFS?

## Eigene Notizen

<!-- Platz für persönliche Ergänzungen, Eselsbrücken, etc. -->
