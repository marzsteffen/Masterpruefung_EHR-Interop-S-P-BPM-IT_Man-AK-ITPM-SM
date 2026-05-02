---
fach: asp
typ: konzept
status: offen
quelle: "[[ASP - VL - Gruener Pass]]"
tags:
  - fach/allgemein/asp
  - typ/konzept
  - status/offen
---

# ASP - Grüner Pass - Sicherheitsbedenken (Hitler-Vorfall, HCERT-Risiko, QR-Code-Diebstahl)

> [!info] Kurzdefinition
> Drei Klassen von Sicherheitsproblemen am DCC: gefälschte Zertifikate trotz gültiger Signatur (Hitler-Vorfall), kompromittierbare Erstellungs-Software bei Gesundheitsdienstleistern (HCERT-Risiko), QR-Code-Diebstahl durch Foto.

## Beschreibung

Folien 22–24 dokumentieren die wichtigsten realen Schwächen.

### Gefälschte Zertifikate – „Hitler-Vorfall" (Folie 22)

*Der Standard* veröffentlicht im November 2021:
- **Gefälschte Impfausweise werden in Validierungs-Apps als gültig anerkannt.**
- Eine Urkunde von „Adolf Hitler" wurde mit verschiedenen Geburtsdaten akzeptiert.
- Das Zertifikat hatte eine **gültige Unterschrift der französischen Sozialversicherungsbehörde CNAM**.
- Es besteht die Gefahr, dass mehrere gefälschte Zertifikate im Umlauf sind.

**Lehre:** Die kryptografische Vertrauenskette war intakt – die Signatur war gültig. Die Schwachstelle lag *nicht* in der Krypto, sondern in der **Identitätsprüfung beim Aussteller**. Wenn ein Mitgliedsstaat (in diesem Fall Frankreich) bei der Datenübernahme keine ausreichende Plausibilitätsprüfung vornimmt, fließen falsche Daten in technisch korrekt signierte Zertifikate.

### Implementierungs-Risiko bei der DCC-Erstellung (HCERT, Folie 23)

**Beispiel-Implementierung – Erstellung digitaler COVID-Zertifikate (HCERT):**
1. Nach der Impfung gibt der Arzt persönliche Daten in seine Software ein.
2. Die eingegebenen Daten werden an die **Country Signing Certificate Authority (CSCA)** übermittelt, die ein gültiges Zertifikat ausstellt.

**Risiken:**
- Wenn die **Software des Gesundheitsdienstleisters kompromittiert wurde**, könnten eingegebene Daten (z. B. Name einer Person) geändert werden.
- **Theoretisch können Ärzte für jede beliebige Person ein Attest erstellen.**
- Es gibt viele verschiedene Implementierungen von Software zum Auslösen der Erstellung von Digital Covid Certificates (DCC) – jede mit eigenem potenziellem Angriffsvektor.

### Unsachgemäße Verwendung von QR-Codes (Folie 24)

- **Jeder, dem ein QR-Code zum Scannen gezeigt wird, könnte möglicherweise ein Foto des QR-Codes machen.**
- Mit diesem Foto kann der Green Pass ohne Wissen der ursprünglich zugeteilten Person einfach nachgebaut werden.

**Mitigationen:**
- Im Zuge von z. B. Eingangstests ist die Identität einer Person zusätzlich per **Lichtbildausweis** nachzuweisen.
- Der Benutzer der Validierungs-App ist für die Identitätsprüfung verantwortlich.
- **Option:** Dänemark reduziert die Gültigkeit von QR-Codes auf **3 Tage**.

## Bestandteile / Aufbau

| Schwachstelle | Wo greift sie an? | Mitigation |
|---|---|---|
| Hitler-Vorfall | Datenübernahme bei der Behörde | Strengere Identitätsprüfung beim Aussteller |
| HCERT-Implementierung | Software des Gesundheitsdienstleisters | Sichere Software, Mehrfaktorauthentifizierung, Audit-Logs |
| QR-Code-Foto-Diebstahl | Vorzeigen des QR-Codes | Lichtbildausweis-Pflicht, kürzere Gültigkeitsdauer |

## Beispiel

- Hitler-Vorfall: Aus dem PDF zitiert; Original-Artikel verlinkt.
- HCERT: Folie 23 visualisiert: Patient → Arzt-Software → CSCA → DCC, mit Pfeil „Modifizierte Daten" als Angriffsvektor.

## Abgrenzung

- **Krypto ist nicht das Problem.** Die digitale Signatur funktioniert in allen drei Szenarien wie vorgesehen.
- **Probleme liegen an den Schnittstellen** – Identitätsprüfung beim Aussteller, Vertrauen in Aussteller-Software, physische Handhabung des QR-Codes.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Welche realen Sicherheitsbedenken sind beim Grünen Pass dokumentiert worden, und wo greifen sie jeweils an?

**Anwendungsfrage:** Erläutern Sie den Hitler-Vorfall: Warum war das gefälschte Zertifikat trotz gültiger Signatur möglich – und welche Schicht im Sicherheitsmodell hat versagt?

**Diskussionsfrage:** Welche generellen Lehren kann man für den Aufbau zukünftiger eHealth-Identitätssysteme ziehen? (Stichworte: Vertrauenskette ist nur so stark wie das schwächste Glied; Software-Sicherheit beim Aussteller ist ebenso wichtig wie Krypto; physische Mitigationen wie Lichtbildausweis sind unverzichtbar.) Welche Mitigation hätte den Hitler-Vorfall verhindert? (Identitätsprüfung mit echter Personalausweisbindung beim Aussteller.)

**Mögliche Anschlussfragen:**
- Welche Mitigation hat Dänemark gewählt, und welcher Trade-off entsteht? (Kürzere Gültigkeit = häufigeres Erneuern = bessere Diebstahl-Resistenz, aber mehr Aufwand für den Bürger.)
- Welche DSGVO-relevanten Probleme entstehen, wenn QR-Codes abfotografiert werden?
- Wie hängt die Validator-Anforderung Lichtbildausweis-Pflicht mit der QR-Code-Schwäche zusammen?

## Verwandt

- [[ASP - Gruener Pass - Vertrauensmodell]]
- [[ASP - Gruener Pass - Validator-Anforderungen]]
- [[ASP - Gruener Pass - EU Digital COVID Certificate]]
- [[ASP - Angriff - Impersonation]]
- [[ASP - Schluesselspeicherung - Hardware Security]]
- [[ASP - Authentifizierung - Level of Assurance]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folien 22, 23, 24
- Externe Referenz Folie 22: Standard-Artikel https://www.derstandard.at/story/2000131078659/gruener-pass-app-bleibt-unsicher-hitler-zertifikate-funktionieren-weiterhin
