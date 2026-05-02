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

# ASP - Identitätsmanagement - Identifizierung vs Authentifizierung (vs Authentisierung)

> [!info] Kurzdefinition
> Drei nahe verwandte, aber unterschiedliche Begriffe: **Identifizierung** = Verbindung von Attributen mit einem Individuum (Behauptung). **Authentisierung** = Übergabe eines Identitätsnachweises. **Authentifizierung** = Prüfung des Nachweises auf Gültigkeit.

## Beschreibung

Folien 6–8 trennen die Begriffe sauber.

**Identifizierung (Folie 7):**
> *„Identification is the association of a personal identifier with an individual presenting attributes." [Clarke]*

- Verbindung zwischen persönlichen Attributen und einem Individuum.
- Beispiel: Name „Max Mustermann" identifiziert die Person Max Mustermann.
- Eindeutigkeit kann durch Kombination persönlicher Attribute oder durch eine eigens erzeugte ID gewährleistet werden.
- Traditionell: Reisepass, Führerschein.

**Authentifizierung (Folie 8):**
> *„Authentication is proof of an attribute." [Clarke]*
> *„The process of verifying a subject's identity or other claim, e.g. one or more attributes." [GINI-SA]*

- Prozess der Bestätigung einer behaupteten (digitalen) Identität.

**Drei-Schritt-Sequenz am Reisepass-Beispiel (Folie 8):**
1. Eine Person behauptet bei der Behörde, sie wäre Max Mustermann. → **Identifizierung**
2. Die Behörde verlangt einen Reisepass als Nachweis.
3. Die Person übergibt den Reisepass mit allen Identitätsdaten. → **Authentisierung**
4. Die Behörde überprüft den Reisepass auf Gültigkeit. → **Authentifizierung**

**Online-Beispiele für Identitätsnachweise zur Authentifizierung:**
1. Benutzername + Passwort
2. Fingerprint
3. Digitales Zertifikat

## Bestandteile / Aufbau

| Begriff | Wer | Was wird getan |
|---|---|---|
| Identifizierung | Subjekt | Identität wird **behauptet** (Attribut → Person zuordnen) |
| Authentisierung | Subjekt | Identitätsnachweis wird **übergeben/präsentiert** |
| Authentifizierung | Prüfender | Identitätsnachweis wird **geprüft/verifiziert** |

## Beispiel

Online-Banking-Login:
1. Identifizierung: Eingabe des Benutzernamens.
2. Authentisierung: Eingabe des Passworts.
3. Authentifizierung: Server vergleicht Passwort-Hash mit der Datenbank und entscheidet, ob die behauptete Identität stimmt.

## Abgrenzung

- **Identifizierung ist eine Behauptung**, kein Beweis. Wer „Max Mustermann" als Login eingibt, behauptet nur, Max zu sein.
- **Authentisierung ist Aktivität des Subjekts**, Authentifizierung ist Aktivität des Prüfenden. Die Begriffe werden im deutschen Sprachgebrauch oft verwechselt; in der Vorlesung werden sie sauber getrennt.
- **Authentifizierung ist nicht Autorisierung:** Auth. klärt, *wer* die Person ist; Autorisierung klärt, *was sie darf*. Siehe [[ASP - Identitaetsmanagement - Autorisierung]].

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie unterscheiden sich Identifizierung, Authentisierung und Authentifizierung?

**Anwendungsfrage:** Ordnen Sie konkrete Schritte eines Login-Prozesses (z. B. Reisepass-Vorlage, Smartphone-Entsperren mit Fingerabdruck) den drei Begriffen zu.

**Diskussionsfrage:** Warum ist die saubere Trennung der drei Begriffe wichtig? In welchen Fehlerklassen würden sich Verwechslungen niederschlagen? (Beispiel: Wenn ein System nur Identifizierung verlangt, ohne Authentifizierung, könnte sich jeder als beliebige Person ausgeben.)

**Mögliche Anschlussfragen:**
- Welche Authentifizierungsklassen gibt es? ([[ASP - Identitaetsmanagement - Authentifizierungsklassen]])
- Was ist der Unterschied zwischen Authentifizierung und Autorisierung?
- Wie passt der Begriff „Identitätsnachweis" in die drei Begriffe?

## Verwandt

- [[ASP - Identitaetsmanagement - Digitale Identitaet]]
- [[ASP - Identitaetsmanagement - Authentifizierungsklassen]]
- [[ASP - Identitaetsmanagement - Multifaktor-Authentifizierung]]
- [[ASP - Identitaetsmanagement - Autorisierung]]
- [[ASP - Security Eigenschaften - Authenticity]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folien 6, 7, 8
- Definitionen aus „Clarke" und „GINI-SA" zitiert (im PDF nicht weiter ausgeführt).
