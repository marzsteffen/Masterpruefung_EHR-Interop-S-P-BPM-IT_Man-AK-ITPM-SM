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

# ASP - Grüner Pass - Österreichische Architektur (EU Gateway, AT Gateway Client, BRZ)

> [!info] Kurzdefinition
> Das EU Gateway verteilt zentral Trust List, Business Rules und Value Sets an die Mitgliedsstaaten. In Österreich ruft der AT Gateway Client (betrieben vom Bundesrechenzentrum BRZ) diese stündlich ab und stellt sie für die Validator-Apps bereit.

## Beschreibung

Folien 15–20 zeigen die Architektur in der österreichischen Umsetzung.

### EU Gateway (Folie 15)
- Von der EU betriebenes **zentrales Gateway**.
- Verteilt drei Informationen an die Mitgliedsstaaten:
  - **Trust List** (Liste aller vertrauenswürdigen Zertifikate).
  - **Business Rules** (nationale und globale Regeln).
  - **Value Sets** (Bedeutung der Datenfelder im Zertifikat).
- **Zugang zum Gateway nicht öffentlich** – erfordert authentifizierte Verbindungen von Backend-Diensten in EU-Mitgliedsstaaten.

### AT Gateway Client (Folien 16–19)
- Der österreichische Backend-Client stellt eine **authentifizierte Verbindung zum EU-Gateway** her.
- Informationen werden über österreichische Dienste verarbeitet und verbreitet, **betrieben vom Bundesrechenzentrum (BRZ)**.
- **Erstellt stündlich** drei Dateien:
  1. **Trust List:** enthält alle Document Signer Certificates (DSC). Diese Signaturzertifikate werden benötigt, um die Gültigkeit und Authentizität von digitalen Signaturen zu validieren, die über QR-Codes präsentiert werden.
  2. **Business Rules AT/EU:**
     - **EU:** Rechtsvorschriften der verschiedenen Mitgliedsstaaten, anhand derer die Gültigkeit der DCCs bei der Einreise in ein bestimmtes Land überprüft wird (festgelegtes Ablaufdatum von Zertifikaten usw.).
     - **AT:** Nationale Regeln für Validierungs-Apps.
  3. **Value Sets:** Informationen zur Zuordnung von Rohwerten zu menschenlesbaren Werten. Werden aktuell gehalten.

### EU-Komponenten (Folie 20)
- **Basic Validation:** Validierungskomponente zur Überprüfung der **strukturellen Korrektheit und Authentizität** eines DCC.
- **Business Rules Validation:** Komponente zur Validierung der Business Rules gegenüber einem DCC (erlaubte Impfungen, wie lange ein bestimmter Test als gültig angesehen wird usw.).
  - Beispiele: Gültigkeit des PCR-Tests in Österreich = 48 h; Pfizer-Impfstoff für 1 Jahr akzeptiert.

**Datenfluss laut Folien-Diagramm:**

```
EU Gateway
    ↓ (private API für trustlist/valuesets/business rules)
AT Gateway Client (BRZ)
    ↓ (stündliche Aktualisierung)
[Trust List]   [Business Rules AT/EU]   [Value Sets]
    ↓                ↓                       ↓
DCC QR Code → Basic Validation → Business Rules Validation → Enrich content → Display in apps
```

## Bestandteile / Aufbau

| Komponente | Rolle | Betreiber |
|---|---|---|
| EU Gateway | zentrale Quelle für Trust List, Rules, Value Sets | EU |
| AT Gateway Client | stündlicher Abruf | BRZ |
| Trust List | DSC-Liste für Signaturprüfung | EU + AT-Replikation |
| Business Rules AT/EU | Validierungslogik | EU + nationale Anpassung |
| Value Sets | Code-Übersetzung | EU |
| Basic Validation | Struktur + Signatur | EU-Komponente |
| Business Rules Validation | Inhaltliche Gültigkeit | EU-Komponente |
| Enrich content | Validator-App-Aufbereitung | AT |

## Beispiel

Eine österreichische Validator-App lädt sich beim Start die aktuellen Daten vom AT Gateway Client (= BRZ-Dienste) herunter. Beim Scannen eines deutschen DCC führt sie zuerst Basic Validation durch (Signaturprüfung mit deutscher DSC aus Trust List) und dann Business Rules Validation (in Österreich gültig?). Anzeige nur Vorname/Nachname/Geburtsdatum.

## Abgrenzung

- **EU Gateway ist nicht der Aussteller**, sondern nur Verteilstelle der Verifikations-Infrastruktur.
- **Stündliche Aktualisierung** ist Trade-off zwischen Aktualität (z. B. neu hinzugekommene DSCs, Sperrungen) und Last/Latenz.
- **Im PDF nur die AT-Architektur dargestellt.** Andere EU-Länder haben analoge Strukturen, technisch potenziell unterschiedlich umgesetzt.

## Prüfungsrelevanz

**Typische Definitionsfrage:** Wie ist die österreichische DCC-Validierungs-Architektur aufgebaut? Welche Komponenten und Datenflüsse gibt es?

**Anwendungsfrage:** Was passiert, wenn der AT Gateway Client für eine Stunde ausfällt? (Validator-Apps haben veraltete Trust List / Business Rules; neue DSCs/Regeln werden verzögert wirksam.)

**Diskussionsfrage:** Welche Skalierungs- und Datenschutz-Vorteile hat die Architektur mit zentralem EU Gateway plus nationalem Replikat? Welche Single Point of Failure bleiben? (EU Gateway selbst; CSCA-Kompromittierung.)

**Mögliche Anschlussfragen:**
- Warum wird der AT Gateway Client vom BRZ betrieben? (Zentrale Bundesinstitution für IT-Infrastruktur des Staates – im PDF nicht ausgeführt.)
- Was ist der Unterschied zwischen Basic Validation und Business Rules Validation?
- Wie hängt diese Architektur mit der Trust List zusammen?

## Verwandt

- [[ASP - Gruener Pass - Vertrauensmodell]]
- [[ASP - Gruener Pass - Value Sets und Business Rules]]
- [[ASP - Gruener Pass - Validator-Anforderungen]]
- [[ASP - Zertifikate - PKI]]

## Quelle

- Vorlesung: [[ASP - VL - Gruener Pass]]
- Folien/Seitenangabe: Folien 15–20
