---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Identitaetsmanagement]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Identitätsmanagement - Authentifizierungsklassen

> [!info] Kurzdefinition
> Vier Klassen von Authentifizierungs-Faktoren: Wissen („etwas wissen"), Besitz („etwas besitzen"), biometrische Eigenschaft („etwas sein") und Verhaltensmuster („etwas tun").

## Beschreibung

Folie 9 listet die vier Klassen mit Beispielen.

**1. Wissen: „Etwas wissen"**
- Authentifizierung basierend auf nachgewiesenem Wissen.
- z. B. Passwort, PIN.

**2. Besitz: „Etwas besitzen"**
- Authentifizierung basierend auf nachgewiesenem Besitz.
- z. B. Reisepass, Smartcards (Bankomatkarte, Kreditkarte).

**3. Biometrische Eigenschaft: „Etwas sein"**
- Authentifizierung basierend auf physikalischer Eigenschaft.
- z. B. Fingerprint, Gesichtserkennung, Iris-Scanner.

**4. Verhaltensmuster: „Etwas tun"**
- Authentifizierung basierend auf dem Verhalten einer Person.
- z. B. Tippverhalten, Verweildauer in Apps.

## Bestandteile / Aufbau

| Klasse | Slogan | Beispiele | Vorteil | Schwäche |
|---|---|---|---|---|
| Wissen | „etwas wissen" | Passwort, PIN | einfach, billig | Phishing, Erraten, Wiederverwendung |
| Besitz | „etwas besitzen" | Smartcard, Token | physisch trennbar | Diebstahl, Verlust |
| Biometrische Eigenschaft | „etwas sein" | Fingerprint, Iris | nicht vergessbar | unveränderbar bei Kompromittierung; Datenschutz |
| Verhaltensmuster | „etwas tun" | Tippverhalten | passiv, kontinuierlich | unsicher als alleiniger Faktor; Datenschutz |

## Beispiel

Aus Folie 9: Passwort/PIN (Wissen), Bankomatkarte (Besitz), Fingerprint (Biometrie), Tippverhalten (Verhalten).

## Abgrenzung

- Eine **einzelne Klasse** allein wird oft als „Single-Factor" bezeichnet (z. B. nur Passwort). Das ist heute für sicherheitsrelevante Anwendungen meist zu wenig.
- Werden Faktoren aus **mehreren Klassen** kombiniert, spricht man von Multifaktor-Authentifizierung ([[ASP - Identitaetsmanagement - Multifaktor-Authentifizierung]]).
- **Achtung:** Zwei Passwörter sind kein 2-Faktor – sie liegen alle in derselben Klasse.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier Klassen von Authentifizierungs-Faktoren gibt es, und je ein Beispiel?

**Anwendungsfrage:** Ordnen Sie konkrete Authentifizierungs-Mechanismen (z. B. Handy-Signatur, ID Austria, eHealth-Karte) den Klassen zu.

**Diskussionsfrage:** Welche Klasse ist für eHealth-Hochsicherheits-Anwendungen besonders kritisch zu betrachten? (Biometrie – einmal kompromittiert, nicht ersetzbar; Datenschutz besonders sensibel.) Welcher Faktor ist nicht ohne weiteres änderbar, falls er gestohlen wird? (Biometrie und Verhaltensmuster.)

**Mögliche Anschlussfragen:**
- Was bedeutet „Multifaktor-Authentifizierung"?
- Warum sind zwei Passwörter kein echter zweiter Faktor?
- Welche Klasse hat die schlechteste Benutzerfreundlichkeit – und welche die beste?

## Verwandt

- [[ASP - Identitaetsmanagement - Multifaktor-Authentifizierung]]
- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Authentifizierung - Level of Assurance]]
- [[ASP - Schluesselspeicherung - Hardware Security]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folie 9
