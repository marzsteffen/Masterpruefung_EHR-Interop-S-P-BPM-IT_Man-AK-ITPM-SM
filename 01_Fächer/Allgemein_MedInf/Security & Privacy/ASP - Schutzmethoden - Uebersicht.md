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

# ASP - Schutzmethoden - Übersicht (Big Picture)

> [!info] Kurzdefinition
> Synoptische Tabelle, die alle in der Vorlesung behandelten Schutzbausteine (Hash, MAC, sym/asym Verschlüsselung, Signatur, Hybrid, PFS) gegen alle acht Angriffe aus dem Angriffsmodell bewertet. Replay und DoS bleiben kryptografisch ungelöst.

## Beschreibung

Die Vorlesung schließt mit zwei Übersichts-Folien:

**Folie 34 – Bausteine-Hierarchie:**
- Niedrige Ebene: **Hash**, **Symmetrische Verschlüsselung**, **Asymmetrische Verschlüsselung**.
- Mittlere Ebene (aus den Bausteinen kombiniert): **MAC (HMAC/CMAC)**, **Digitale Signaturen**, **Hybride Verschlüsselung**.
- Obere Ebene (aus den Mittelschicht-Mechanismen): **Perfect Forward Secrecy**, **Weitere High-Level-Protokolle**.

**Folie 35 – Angriff × Schutz-Matrix:**

| Angriff | Hash | MAC | Sym. Verschl. | Asym. Verschl. | Digitale Signatur | Hybride Verschl. | PFS |
|---|---|---|---|---|---|---|---|
| Nachricht lesen | ❌ | ❌ | ✅ | ✅ | ❌ | ✅ | ✅ |
| Indirektes Ableiten | ❌ | ❌ | ⚠️ | ⚠️ | ❌ | ⚠️ | ⚠️ |
| Aufzeichnung + Schlüssel-Diebstahl | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |
| Nachricht einfügen | ✅ | ✅ | ✅ | ❌ | ✅ | ❌ | ✅ |
| Replay | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Modifikation Plaintext | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Modifikation Ciphertext | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ |
| Impersonation | ❌ | ⚠️ | ⚠️ | ⚠️ | ✅ | ❌ | ✅ |
| Nachricht unterdrücken | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |

(✅ = Angriff verhindert; ⚠️ = szenarioabhängig; ❌ = Angriff erfolgreich)

**Zentrale Aussagen der Übersicht:**
- **Replay** wird auf Protokollebene verhindert (z. B. Timestamps).
- **Nachricht unterdrücken** (DoS) braucht Maßnahmen wie Blackhole Routing gegen DDoS-Angriffe.
- **PFS bietet die umfassendste Abdeckung** unter den Krypto-Bausteinen, schützt aber nicht vor Replay und DoS.
- **Reine Verschlüsselung** (sym/asym/hybrid) schützt nicht gegen Modifikation des Ciphertexts und nicht gegen Impersonation – dafür braucht es Signaturen.
- **Hash und MAC** verhindern Modifikation Plaintext und „Nachricht einfügen", aber nicht das Lesen oder Abhören.
- Die in der Tabelle aufgeführte Spalte „Hybride Verschlüsselung" hat nicht die Signatur-Erweiterung mitberücksichtigt – mit Signatur-Erweiterung würde Hybrid die Impersonation und Modifikation Ciphertext mitabdecken.

## Bestandteile / Aufbau

Die Hierarchie der Bausteine zeigt: Höhere Schutzziele werden aus mehreren Krypto-Primitiven zusammengesetzt. Eine Signatur braucht Hash + asymmetrische Krypto. PFS braucht ECC + DH + Signatur (über die ephemeralen Keys) + symmetrische Verschlüsselung.

## Beispiel

Ein voll abgesichertes eHealth-Messaging mit Vertraulichkeit, Integrität, Authentizität, Non-repudiation und PFS kombiniert: ECC-Schlüsselpaare in Hardware → ephemeraler ECDH-Schlüsselaustausch → Signatur über die ephemeralen Schlüssel mit dem statischen Private Key → AES-Verschlüsselung der Nutzdaten mit dem ausgehandelten Sitzungsschlüssel → HMAC oder digitale Signatur über die Klartextdaten.

## Abgrenzung

- Diese Tabelle ist nur eine **didaktische Zusammenfassung**. In realen Protokollen werden Bausteine kombiniert, sodass mehrere Spalten gleichzeitig zählen.
- **Wichtige Lesart:** Die Spalte „Hybride Verschlüsselung" meint hier die **reine hybride Konstruktion ohne Signatur** (Folie 28 Kap 02). Folie 34 listet „Hybride Verschlüsselung" und „Digitale Signaturen" als zwei getrennte Bausteine in der mittleren Hierarchie-Ebene; die Signatur-Spalte daneben wäre sonst redundant. Wer die hybride Konstruktion *plus* Signatur (Folie 55 Kap 02) einsetzt, erbt die Schutzwirkungen beider Spalten – also auch Schutz gegen Modifikation Ciphertext und Impersonation.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche Schutzmethoden gegen welche Angriffe? (Sehr wahrscheinlich offen formuliert oder als gerichtete Frage „Welcher Schutz schützt gegen Replay?", „Was hilft gegen Impersonation?".)

**Anwendungsfrage:** Geben Sie eine Kombination von Schutzbausteinen an, die alle Angriffe außer Replay und DoS abdeckt. Wie wird der verbleibende Schutz erreicht? (Replay → Timestamps/Nonces; DoS → Netzwerk-/Protokollebene.)

**Diskussionsfrage:** Warum sind ausgerechnet Replay und DoS auch nach allen kryptografischen Bausteinen ungelöst? Wo liegt der grundsätzliche Unterschied zwischen Krypto-Schutz und Protokoll-Schutz? (Krypto schützt einzelne Nachrichten; Replay und DoS sind Eigenschaften des Nachrichten*flusses* und müssen auf Sitzungs- bzw. Netzwerkebene adressiert werden.)

**Mögliche Anschlussfragen:**
- Welcher Baustein adressiert Non-repudiation, welcher nicht?
- Wann brauchen Sie PFS und nicht „nur" Hybrid?
- Welche zusätzlichen Schutzmaßnahmen braucht ein produktives System neben Krypto? (Zugriffskontrolle, Logging, Monitoring – im PDF dieser Vorlesung nur als Vorausblick angerissen.)

## Verwandt

- [[ASP - Hash - Funktion]]
- [[ASP - MAC - Grundlagen]]
- [[ASP - Symmetrische Verschluesselung - Prinzip]]
- [[ASP - Asymmetrische Verschluesselung - Prinzip]]
- [[ASP - Digitale Signatur - Grundlagen]]
- [[ASP - Hybride Verschluesselung - Grundlagen]]
- [[ASP - Kryptografie - Perfect Forward Secrecy]]
- [[ASP - Symmetrische Verschluesselung - Angriffsmodell]]
- [[ASP - Asymmetrische Verschluesselung - Angriffsmodell]]

## Quelle

- Vorlesung: [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]]
- Folien/Seitenangabe: Folien 14, 23, 27, 31 (Zwischenstände); Folien 34, 35 (Big Picture)
