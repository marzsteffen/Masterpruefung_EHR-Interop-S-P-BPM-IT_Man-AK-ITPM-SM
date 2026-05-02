---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Digitale Signatur - Reihenfolge: erst signieren, dann verschlüsseln

> [!info] Kurzdefinition
> Wer eine Nachricht sowohl signieren als auch verschlüsseln will, muss **zuerst signieren und dann verschlüsseln**. Die umgekehrte Reihenfolge erlaubt es einem Angreifer, eine eigene Signatur über die unveränderte Ciphertext-Nachricht zu setzen und so die Urheberschaft zu fälschen.

## Beschreibung

Die Vorlesung stellt auf Folie 24 die Frage: „Wird die verschlüsselte oder unverschlüsselte Nachricht signiert?" und zeigt anhand eines Angriffsszenarios (Folien 25, 26), warum die richtige Reihenfolge **sign-then-encrypt** ist.

**Angriffsszenario „Erst verschlüsseln, dann signieren" (Folien 25, 26):**

1. Alice verschlüsselt die Nachricht mit Bobs Public Key.
2. Alice signiert den Ciphertext mit ihrem Private Key.
3. Eve fängt verschlüsselte Nachricht + Signatur ab.
4. Eve **streift Alice' Signatur ab** und erzeugt eine **neue Signatur** mit ihrem eigenen Private Key über die (unveränderte) verschlüsselte Nachricht.
5. Eve sendet verschlüsselte Nachricht + Eves Signatur + ggf. Eves Public Key/Zertifikat an Bob.
6. Bob verifiziert die Signatur erfolgreich (sie passt zum mitgeschickten Public Key) – und glaubt nun, die Nachricht stamme von Eve.
7. Bob entschlüsselt mit seinem Private Key und liest den Inhalt – der zwar inhaltlich unverändert ist, aber falsch zugeordnet wird.

**Daher (Folie 26):** Zuerst signieren, dann verschlüsseln (!).

**Korrekter Ablauf (sign-then-encrypt):**
1. Alice signiert die Klartext-Nachricht mit ihrem Private Key.
2. Alice verschlüsselt Nachricht + Signatur mit Bobs Public Key (bzw. mit einem hybriden Sitzungsschlüssel, der wiederum mit Bobs Public Key gesichert ist).
3. Bob entschlüsselt mit seinem Private Key und erhält Klartext + Signatur.
4. Bob verifiziert die Signatur mit Alice' Public Key – und kann sicher sein, dass die Nachricht von Alice stammt.

In der korrekten Reihenfolge kann Eve die Signatur nicht mehr abstreifen, weil sie verschlüsselt ist – sie sieht weder den Klartext noch die Signatur.

## Bestandteile / Aufbau

| Reihenfolge | Sicherheit | Begründung |
|---|---|---|
| Erst verschlüsseln, dann signieren | ❌ unsicher | Angreifer kann Signatur ersetzen, Urheberschaft fälschen |
| Erst signieren, dann verschlüsseln | ✅ sicher | Signatur ist im Ciphertext eingebettet, für Eve unsichtbar |

## Beispiel

Aus Folie 25: Eve fängt die signierte verschlüsselte Nachricht von Alice ab. Sie ersetzt Alice' Signatur durch ihre eigene (mit ihrem Private Key, signiert auf den unveränderten Ciphertext) und reicht die Nachricht plus eigene Public-Key-Information an Bob weiter. Bobs Signaturprüfung mit Eves Public Key gelingt; Bob hält Eve für die Senderin.

## Abgrenzung

- Diese Reihenfolge gilt für die hybride Konstruktion mit Signatur, nicht für jede beliebige Krypto-Kombination. In manchen Protokollen (z. B. AEAD mit signiertem Channel) verschwimmen die Grenzen, das ist *im PDF nicht behandelt*.
- Die Reihenfolge-Frage ist NICHT mit der allgemeinen „Encrypt-then-MAC vs. MAC-then-Encrypt"-Diskussion zu verwechseln (jene betrifft symmetrische MACs); konzeptuell verwandt, aber technisch andere Bausteine.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Soll man eine Nachricht erst signieren oder erst verschlüsseln, und warum?

**Anwendungsfrage:** Skizziere das Angriffsszenario, das eintritt, wenn man erst verschlüsselt und dann signiert. Welche Eigenschaft des Angriffs macht ihn besonders gefährlich? (Antwort: Der Angreifer braucht den Klartext nicht zu kennen; er manipuliert nur die Urheberschaft.)

**Diskussionsfrage:** Welches Schutzziel wird in der falschen Reihenfolge konkret gebrochen? (Antwort: Authentizität / Non-repudiation – die Vertraulichkeit ist sogar erhalten geblieben.) Welche Konsequenzen hat das für eHealth-Workflows wie signierte Verordnungen oder Befunde?

**Mögliche Anschlussfragen:**
- Warum kann Eve im sign-then-encrypt-Modus die Signatur nicht ersetzen?
- Welche Annahme an die PKI / Zertifikatsprüfung ist zentral, damit der Angriff in der falschen Reihenfolge funktioniert? (Bob muss das Zertifikat / den Public Key zur Signatur akzeptieren – wenn das Protokoll fest an Alice gebunden ist, bricht der Angriff.)

## Verwandt

- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Security Eigenschaften - Authenticity]]
- [[ASP - Security Eigenschaften - Non-repudiation]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folien 24, 25, 26
