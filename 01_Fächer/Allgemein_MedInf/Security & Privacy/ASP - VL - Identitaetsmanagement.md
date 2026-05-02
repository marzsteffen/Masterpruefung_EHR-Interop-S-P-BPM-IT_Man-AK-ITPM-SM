---
fach: asp
typ: vorlesung
status: offen
quelle_pdf: Folien/Advanced Security and Privacy/05 Identitätsmanagement/IVL_ADSP_Identitätsmanagement_…SM-X800_Nov-27-0843-2024_1.pdf
datum_vorlesung: 2024-11-05
tags:
  - fach/allgemein/asp
  - typ/vorlesung
  - status/offen
---

# ASP - VL - Identitätsmanagement

## Überblick

Fünfter Vorlesungsblock. Auf den Krypto-Bausteinen (Hash, Signatur, Zertifikat) wird das Thema Identitätsmanagement aufgesetzt: Wer ist die Person hinter einem Public Key, wie weist sie ihre Identität nach, welche Rechte hat sie auf eine Ressource? Die Vorlesung gliedert sich in fünf Blöcke laut Agenda (Folie 2): Identifikation und Authentifizierung; Berechtigungsmodelle; Identitätsmanagement (IdM-Lebenszyklus); IdM-Modelle (zentrales/isoliertes/benutzer-zentriertes/föderiertes); Identitätsprotokolle (SAML2, OpenID Connect).

## Lernziele (laut Vorlesung)

*Im PDF nicht als eigene Liste ausgewiesen.* Aus dem Aufbau ergeben sich: Begriffe Identifikation/Authentifizierung/Autorisierung sauber trennen; Authentifizierungsklassen und Multifaktor-Auth verstehen; sechs Berechtigungsmodelle (RBAC/ABAC/IBAC/MAC/DAC/CBAC) gegeneinander abgrenzen; IdM-Lebenszyklus und Governance benennen; vier IdM-Modelle vergleichen; SAML2- und OIDC-Flow erklären können.

## Behandelte Konzepte

### Identifikation und Authentifizierung
- [[ASP - Identitaetsmanagement - Digitale Identitaet]]
- [[ASP - Identitaetsmanagement - Identifizierung vs Authentifizierung]]
- [[ASP - Identitaetsmanagement - Authentifizierungsklassen]]
- [[ASP - Identitaetsmanagement - Multifaktor-Authentifizierung]]
- [[ASP - Identitaetsmanagement - Autorisierung]]

### Berechtigungsmodelle
- [[ASP - Berechtigungsmodelle - Uebersicht]]

### Identitätsmanagement-Lebenszyklus
- [[ASP - Identitaetsmanagement - Definition]]
- [[ASP - Identitaetsmanagement - Lebenszyklus]]

### Identitätsmanagement-Modelle
- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Modelle]]

### Identitätsprotokolle
- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsprotokoll - SAML Assertion]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Identitaetsprotokoll - JWT ID-Token]]

## Roter Faden

Eine **digitale Identität** ist das digitale Abbild einer Person oder eines Objekts. Sie besteht aus drei Teilstücken: einer **eindeutigen ID** (z. B. UUID), **Identitätsdaten/Attributen** (Name, Geburtsdatum, …) und **Authentifizierungs- bzw. Identifikationsdaten** (Benutzername+Passwort, Zertifikat). Damit lassen sich drei nahe verwandte Begriffe trennen, die in der Prüfung gerne durcheinander geraten: **Identifizierung** = Verbindung Attribute → Individuum (Behauptung „Ich bin Max Mustermann"). **Authentisierung** = Übergabe eines Identitätsnachweises (Reisepass vorzeigen). **Authentifizierung** = Prüfung des Nachweises auf Gültigkeit (Behörde prüft Reisepass). Authentifizierung erfolgt nach vier möglichen Klassen – Wissen, Besitz, biometrische Eigenschaft, Verhaltensmuster – die in der **Multifaktor-Authentifizierung** kombiniert werden.

Daran schließt **Autorisierung** an: das Zuweisen von Rechten an eine bestätigte Identität. Wie diese Rechte vergeben werden, hängt vom **Berechtigungsmodell** ab. Die Vorlesung kennt sechs: **RBAC** (Role-Based), **ABAC** (Attribute-Based), **IBAC** (Identity-Based), **MAC** (Mandatory), **DAC** (Discretionary), **CBAC** (Context-Based). Eine Vergleichstabelle (Folie 16) zeigt Vor- und Nachteile.

**Identitätsmanagement (IdM)** umfasst die Prozesse rund um den Lebenszyklus einer digitalen Identität: **Erstellung** (Registrierung), **Verwendung** (Authentifizierung, Autorisierung), **Wartung** (Attributänderung), **Löschung** (Widerruf). Über allem schwebt **Governance** – Richtlinien, Überwachung, oft auf rechtlicher Basis.

In der Praxis wird IdM nach einem von vier **Modellen** organisiert: **zentral** (SP = IdP), **isoliert** (getrennte SP und IdP, z. B. mit A-Trust), **benutzer-zentriert** (Identitätsdaten beim Benutzer, z. B. auf Smartcard), **föderiert** (mehrere IdPs vertrauen einander). Akteure sind: Benutzer, Identity Provider (z. B. A-Trust), Service Provider (z. B. ELGA), Kontrollorgan (z. B. Staat).

Den Abschluss bilden zwei zentrale **Identitätsprotokolle**: **SAML2** (XML-basierte Assertions, klassisch in älteren Webanwendungen) und **OpenID Connect** (OIDC, JSON Web Tokens, modern für Web/Mobile). Beide werden anhand eines ELGA-Logins durchgespielt.

## Zentrale Aussagen / Take-aways

- **Drei Begriffe trennen:** Identifizierung (Behauptung) ≠ Authentisierung (Nachweis übergeben) ≠ Authentifizierung (Nachweis prüfen).
- **Vier Authentifizierungsklassen:** Wissen / Besitz / Biometrische Eigenschaft / Verhaltensmuster.
- **Sechs Berechtigungsmodelle:** RBAC, ABAC, IBAC, MAC, DAC, CBAC – jedes mit eigenen Stärken/Schwächen; in eHealth dominiert RBAC mit ABAC-Erweiterungen, oft kombiniert mit MAC (zentrale Sicherheitsregeln).
- **IdM-Lebenszyklus:** Erstellung → Verwendung → Wartung → Löschung, dauerhaft umgeben von Governance.
- **Vier IdM-Modelle:** zentral, isoliert, benutzer-zentriert, föderiert. Föderiert ist das Modell für eHealth-Netzwerke (z. B. eIDAS-Notifizierung, IHE XUA).
- **Zwei Hauptprotokolle:** SAML2 (XML, ältere Web-Apps) vs. OIDC (JWT, moderne Apps).
- **OIDC nutzt das ID-Token (JWT)** zur Identitätsbestätigung; SAML2 nutzt **SAML-Assertions (XML)**.

## Querverweise zu anderen Vorlesungen

- [[ASP - VL - Hash MAC Digitale Signaturen Zertifikate]] (Krypto-Bausteine, auf denen Identitätsprotokolle aufsetzen)
- [[ASP - Authentifizierung - Level of Assurance]] (eIDAS-LoA, hier vertieft)
- [[MSI - IHE - XUA]] (Cross-Identity Assertion in IHE-Profilen, basiert auf SAML)
- [[EHR - ELGA - Architektur]] (ELGA als prominentestes österreichisches IdM-Beispiel)

## Quelle

- PDF: `Folien/Advanced Security and Privacy/05 Identitätsmanagement/IVL_ADSP_Identitätsmanagement_…SM-X800_Nov-27-0843-2024_1.pdf`
- Folienanzahl: 35
- Vortragender: Dr. Kevin Theuermann
- Datum laut Folien: 05.11.2024
