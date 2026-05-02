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

# ASP - Identitätsmanagement - Modelle (zentral, isoliert, benutzer-zentriert, föderiert)

> [!info] Kurzdefinition
> Vier organisatorische Modelle, wie Identity Provider und Service Provider zueinander stehen: zentral (SP = IdP), isoliert (getrennt), benutzer-zentriert (Identitätsdaten beim Benutzer) und föderiert (mehrere IdPs vertrauen einander).

## Beschreibung

Folien 24–27 stellen die vier Modelle mit jeweiligen Vor- und Nachteilen vor.

### 1. Zentrales Modell (Folie 24)
- Service Provider ist auch Identity Provider.
- Authentifizierung findet **direkt beim Service Provider** statt.
- Identifizierungsdaten gespeichert und gewartet beim jeweiligen Service Provider.
- **Vorteile:**
  - Auth.-Prozess kann selbst bestimmt und geändert werden.
  - SP ist unabhängig hinsichtlich Identitätsmanagement.
  - Ausfälle oder Probleme beim Identity Provider werden schnell erkannt.
- **Nachteile:**
  - Auth.-Prozess muss selbst implementiert werden → erhöhte Kosten.
  - Es können Fehler in der Implementierung des Auth.-Prozesses auftreten.
  - SP ist für alles letztverantwortlich.

### 2. Isoliertes Modell (Folie 25)
- **Trennung von Identity Provider (IdP) und Service Provider (SP).**
- IdP speichert Identitätsdaten.
- SP bekommt Identitätsdaten von IdP.
- Benutzer hat keine Kontrolle über Transfer von Identitätsdaten.
- **Vorteile:**
  - Auth.-Prozess wird an einen Spezialisten ausgelagert.
  - Sichere Verwaltung der Identitätsdaten durch den IdP.
  - Keine eigene Implementierung der Authentifizierungsprozesse.
- **Nachteile:**
  - Evtl. laufende Kosten für die Nutzung des IdP.
  - Ausfall des IdP führt dazu, dass Benutzer die Dienste des SP nicht nutzen können.
  - Umsetzung von Änderungswünschen dauert potenziell länger und verursacht höhere Kosten.

### 3. Benutzer-zentriertes Modell (Folie 26)
- Identitätsdaten werden **beim Benutzer** gespeichert.
- Üblicherweise auf einem Sicherheitstoken (Smartcard, …).
- **Explizite Zustimmung des Benutzers zum Teilen der Daten erforderlich.**
- **Vorteile:**
  - Der Benutzer hat die Datenhoheit.
- **Nachteile:**
  - Der Benutzer kann die Identitätsdaten potenziell verlieren / weitergeben / ändern.

### 4. Föderiertes Modell (Folie 27)
- **Identitätsdaten über mehrere IdPs verteilt.**
- Vertrauensbasis zwischen IdPs erforderlich (Federation).
- **Vorteile:**
  - Hohe Ausfallssicherheit.
  - Identitätsdaten von Benutzern können nicht einfach gelöscht werden (verteilt).
- **Nachteile:**
  - Hohe Kosten für den Betrieb und die Synchronisation mehrerer Identity Provider.
  - Eine Vertrauensbasis zwischen den IdPs ist notwendig.

## Bestandteile / Aufbau

| Modell | IdP-SP-Verhältnis | Wo liegen Identitätsdaten? | Typischer Einsatz |
|---|---|---|---|
| Zentral | identisch | beim SP | kleinere Webdienste, einzelnes Unternehmen |
| Isoliert | getrennt | beim IdP | externer Single-IdP-Dienst (z. B. A-Trust für ELGA) |
| Benutzer-zentriert | getrennt, Daten beim User | beim Benutzer | Smartcard-Lösungen, eIDAS-Wallet (EUDI) |
| Föderiert | mehrere IdPs | über mehrere IdPs verteilt | grenzüberschreitende Identitäten (eIDAS-Notifizierung) |

## Beispiel

- **Zentral:** Klassische Webshop-Logins (eigene Benutzerverwaltung).
- **Isoliert:** ELGA-Login über A-Trust (A-Trust = IdP, ELGA = SP).
- **Benutzer-zentriert:** ID Austria mit signierten Daten auf dem Smartphone des Benutzers (Übergangsform); langfristig EUDI Wallet.
- **Föderiert:** eIDAS-Notifizierung – ein deutscher Bürger nutzt seinen deutschen Personalausweis-IdP für einen österreichischen Service Provider.

## Abgrenzung

- **Zentral vs. Isoliert:** Kernkriterium ist die Trennung von IdP und SP.
- **Isoliert vs. Föderiert:** Ein einziger externer IdP (isoliert) vs. mehrere kooperierende IdPs (föderiert).
- **Benutzer-zentriert** ist orthogonal: Es legt die Datenhoheit beim Benutzer, kann technisch in isolierten oder föderierten Setups eingebettet sein.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche vier IdM-Modelle gibt es, und worin unterscheiden sie sich?

**Anwendungsfrage:** Welches Modell wird in ELGA / eIDAS verwendet, und warum? Welches Modell wäre für ein internes Krankenhaus-System angemessen?

**Diskussionsfrage:** Welche Vertrauensbeziehungen sind im föderierten Modell besonders kritisch, und wie werden sie technisch realisiert? (Stichwort: gegenseitig signierte Metadaten, SAML-Federation Trust Anchors – im PDF nicht ausgeführt.) Welches Modell adressiert die DSGVO am besten?

**Mögliche Anschlussfragen:**
- Was ist Single Sign-On, und in welchem Modell ist es typisch? (Föderiert oder isoliert.)
- Welche Schwächen entstehen, wenn der IdP ausfällt – und wie unterscheiden sich die Modelle hier?
- Welches Modell unterstützt am besten Datenhoheit der Nutzer?

## Verwandt

- [[ASP - Identitaetsmanagement - Akteure]]
- [[ASP - Identitaetsmanagement - Definition]]
- [[ASP - Identitaetsprotokoll - SAML2]]
- [[ASP - Identitaetsprotokoll - OpenID Connect]]
- [[ASP - Authentifizierung - Level of Assurance]]
- [[MSI - IHE - XCA]]

## Quelle

- Vorlesung: [[ASP - VL - Identitaetsmanagement]]
- Folien/Seitenangabe: Folien 24, 25, 26, 27
