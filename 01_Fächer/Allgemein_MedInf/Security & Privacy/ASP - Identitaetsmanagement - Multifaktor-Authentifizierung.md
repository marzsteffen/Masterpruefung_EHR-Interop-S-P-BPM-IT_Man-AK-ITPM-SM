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

# ASP - Identitätsmanagement - Multifaktor-Authentifizierung (MFA)

> [!info] Kurzdefinition
> Kombination von Authentifizierungs-Faktoren aus mindestens zwei verschiedenen Klassen (Wissen, Besitz, Biometrie, Verhaltensmuster) zur Erhöhung der Sicherheit.

## Beschreibung

Folie 10 stellt MFA als Schutzverstärkung vor:

- **Kombination verschiedener Authentifizierungsklassen zur Erhöhung der Sicherheit.**
- z. B. Kombination aus **Besitz und Wissen** (2-Faktor-Authentifizierung):
  - **Handy-Signatur** (Wissen: Signatur-PIN, Besitz: Schlüsselmaterial, Biometrie: Fingerprint).
  - **Online-Banking** (Wissen: Benutzername + PIN, Besitz: Mobiltelefon).
- **Bei der Wahl von Authentifizierungsmethoden sollte auch die Benutzerfreundlichkeit berücksichtigt werden.**

**Kerngedanke:** Wer einen Faktor kompromittieren will, muss nicht nur ein Passwort erraten, sondern zusätzlich physikalisch an ein Gerät kommen oder eine biometrische Eigenschaft fälschen. Das hebt die Hürde drastisch.

## Bestandteile / Aufbau

| Beispiel | Faktor 1 | Faktor 2 | (Faktor 3) |
|---|---|---|---|
| Handy-Signatur | Wissen (Signatur-PIN) | Besitz (Schlüsselmaterial im Smartphone) | Biometrie (Fingerprint zur Geräteentsperrung) |
| Online-Banking (Push-TAN) | Wissen (Benutzername + PIN) | Besitz (Mobiltelefon mit Banking-App) | – |
| ID Austria | Wissen (PIN) | Besitz (registriertes Smartphone) | Biometrie (Face/Fingerprint zur App-Entsperrung) |

## Beispiel

Handy-Signatur (Folie 10): Wissen (Signatur-PIN) + Besitz (Schlüsselmaterial im Sicherheits-Token oder Smartphone) + Biometrie (Fingerprint zur Entsperrung).

## Abgrenzung

- **Echte MFA** kombiniert Faktoren aus *unterschiedlichen* Klassen. Zwei Passwörter sind keine MFA, weil beide aus „Wissen" stammen.
- **2FA vs. MFA:** 2FA = genau zwei Faktoren; MFA = zwei oder mehr.
- Trade-off **Sicherheit ↔ Benutzerfreundlichkeit**: Mehr Faktoren = mehr Sicherheit, aber weniger Komfort. Die Vorlesung weist explizit darauf hin.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Was ist Multifaktor-Authentifizierung, und warum erhöht sie die Sicherheit?

**Anwendungsfrage:** Sind zwei Passwörter eine 2FA? (Nein – beide gehören zur Klasse „Wissen".) Welche Klassen kombiniert die Handy-Signatur?

**Diskussionsfrage:** Welcher Trade-off besteht zwischen Sicherheit und Usability? Gibt es Anwendungsfälle, in denen MFA nicht angemessen ist? (Z. B. Notfall-Zugriff in der Notaufnahme – starre MFA kann lebensbedrohlich werden, Stichwort „Break-the-Glass"; *im PDF nicht behandelt*.)

**Mögliche Anschlussfragen:**
- Welche LoA-Stufe lässt sich nur mit MFA erreichen?
- Wie hängt MFA mit Phishing-Resistenz zusammen?
- Welche neuen Phishing-resistenten Mechanismen (FIDO2, Passkeys) ergänzen MFA? (*Im PDF nicht behandelt.*)

## Verwandt

- [[ASP - Identitaetsmanagement - Authentifizierungsklassen]]
- [[ASP - Authentifizierung - Level of Assurance]]
- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Schluesselspeicherung - Hardware Security]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folie 10
